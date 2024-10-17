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
-	[`rust:1.81`](#rust181)
-	[`rust:1.81-alpine`](#rust181-alpine)
-	[`rust:1.81-alpine3.19`](#rust181-alpine319)
-	[`rust:1.81-alpine3.20`](#rust181-alpine320)
-	[`rust:1.81-bookworm`](#rust181-bookworm)
-	[`rust:1.81-bullseye`](#rust181-bullseye)
-	[`rust:1.81-slim`](#rust181-slim)
-	[`rust:1.81-slim-bookworm`](#rust181-slim-bookworm)
-	[`rust:1.81-slim-bullseye`](#rust181-slim-bullseye)
-	[`rust:1.81.0`](#rust1810)
-	[`rust:1.81.0-alpine`](#rust1810-alpine)
-	[`rust:1.81.0-alpine3.19`](#rust1810-alpine319)
-	[`rust:1.81.0-alpine3.20`](#rust1810-alpine320)
-	[`rust:1.81.0-bookworm`](#rust1810-bookworm)
-	[`rust:1.81.0-bullseye`](#rust1810-bullseye)
-	[`rust:1.81.0-slim`](#rust1810-slim)
-	[`rust:1.81.0-slim-bookworm`](#rust1810-slim-bookworm)
-	[`rust:1.81.0-slim-bullseye`](#rust1810-slim-bullseye)
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
$ docker pull rust@sha256:0757ed8c0609498399dfde17ad6e5ac4adc5da04096fbd3d9c2301c62b93546b
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
$ docker pull rust@sha256:62afc139057dc9d3eda02e490677911b55a208ba22d6f7315f3c5c5851e31a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533623479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3b0145b0fabfa9f7bfc382e163449775329c6b95cb5704237a770a9e6e52a1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba0b3d08b81baa192d30dbb2257b8227f2a4eab719c79ef1c419e3a07b39dbc`  
		Last Modified: Thu, 17 Oct 2024 01:10:04 GMT  
		Size: 64.4 MB (64393080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bc85537ac7c401eea9ed38d4a75fddbe5d75d5570921f1c435a8342b3cef15`  
		Last Modified: Thu, 17 Oct 2024 01:10:40 GMT  
		Size: 211.3 MB (211281151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97b348fbebca67b25f027e550f95573ba6aff2f81f748dbf3e11e96d7fc6da6`  
		Last Modified: Thu, 17 Oct 2024 02:57:32 GMT  
		Size: 184.3 MB (184341137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:afd613e0c8388610680d95743ce6b0519e2e288ab2180009d03fdee5263cf66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ce36b1a51263afe43943de85c9d45999d4fd4b9197ac8e48278804e18c1582`

```dockerfile
```

-	Layers:
	-	`sha256:7b956ebc4fdf5bc354458d55f06403a6a7feff6dbe43975c601c444a5d70edc5`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde1eebb12461b3cf18799768782571274684aa61647d4c0e77a0b7d51d3c40`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 13.0 KB (13004 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:27b6e9bd919166bac1fb9211e9e52449d5fb725a70122e2280b3f235eef01f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.5 MB (523464584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd1ab1a770c8f7aa48d8b41c6152318ce574fb409b4620f8fea171c3ba763c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea668db82ddd31e7300e905d69bfbcc24fd0c70cd7c7212c915763a9e47f3e7`  
		Last Modified: Fri, 27 Sep 2024 07:39:33 GMT  
		Size: 175.2 MB (175207938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807abecaed8d4cffae0b7d1da027197029821fd16d2bbce8c0f8a1f90fd349f3`  
		Last Modified: Sat, 28 Sep 2024 04:08:11 GMT  
		Size: 221.5 MB (221511519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:ee2cbc5b0aa8369395392c722b55ad9ac0bd4916118b0cdf63d4d0f13269a299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15270591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa74c1d6fa4c9dda9c706f2706450a4b81da24d4559310f49de7e46773f9700`

```dockerfile
```

-	Layers:
	-	`sha256:45c0558bf77c60592fcc61666d1d55c2e8062c13eee2815becd8547e5fe62df5`  
		Last Modified: Sat, 28 Sep 2024 04:08:07 GMT  
		Size: 15.3 MB (15257523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab9e3cff7b672ef6b62a3eecbf1b9c661a226d91214cd3d7b68a9fd5b262ff05`  
		Last Modified: Sat, 28 Sep 2024 04:08:06 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f5fbbf475717a8e1fcfda24fc26c60200eb95e19b03291f3e43e60995a4d406e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.7 MB (588709463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d76e87cace62dbdc9c3a6c3fae1623de64a44b8b274d79b8e95bcd89b6f1e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71ace0e8bbdcfcf795b836e24a37a6ed0054100e14d6aa6e5a63f7e162ba729`  
		Last Modified: Fri, 27 Sep 2024 05:25:40 GMT  
		Size: 202.7 MB (202651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c70a9d34bb788145305c907ff9a5ed64690b67c5abbc4b676ff607611081e0`  
		Last Modified: Fri, 27 Sep 2024 23:30:32 GMT  
		Size: 248.5 MB (248529120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:be6c0d1bdd139e794a093f63bbdcf7c53acbacba5babbcf59b54af8fd37f7cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15494574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23350ebe95ee44b5c009236d86e0a9d13772ae5689fa9c3449fec0987bd7b81d`

```dockerfile
```

-	Layers:
	-	`sha256:7c227d855755631f9fc25b4280c874ce996590e6446ce7c7399e0c496bd31670`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 15.5 MB (15481248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a10530d2c00a615465f62c3a9b01ff478facbfb4d920cbbf7d0d386c559eb44`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:cae43437babe4a513bfaf1ebaed7b47e916e1a96bea4496ee763708f2a2b5bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549225958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af64455d7089be15c70fda713c93555e12afb877f65a7b29d2b3dddfab02d1f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9dd8137152c295fb3624be3ee13689c34dc13bc115d0032a5a2a581001f14f`  
		Last Modified: Thu, 17 Oct 2024 01:09:36 GMT  
		Size: 24.9 MB (24895435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbad5c607546fed7ceeb86b3cef161781f7cb90e39cb2c8da1b7774aa73975d4`  
		Last Modified: Thu, 17 Oct 2024 01:09:58 GMT  
		Size: 66.2 MB (66210908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c0ef7e16c4ea3f5643d06ea746c15f35cca787121e7078904f6a16114c48`  
		Last Modified: Thu, 17 Oct 2024 01:10:44 GMT  
		Size: 210.2 MB (210196330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f818dcff8930802b82fed8fbd3b89feef62a7b69bc64cebb8df64281a6dd9`  
		Last Modified: Thu, 17 Oct 2024 02:57:36 GMT  
		Size: 197.3 MB (197346451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:bc528a75faa20afa57e2c7e4b6f51d9b57b5485d2d379eea44c3bf52d6fbd4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808162f63c550251d4aaa7a5eee4f171d732b78e387b1137976a4a926ec4476c`

```dockerfile
```

-	Layers:
	-	`sha256:cecf68aacf4ab8230e1cd8e54fe8e2c4fe0ecb15f64b69df35db646913b7bdd2`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73cb9933a9869db1cc6fb4636124d96cbfd43111b4b05b820c4e12217bc5b56`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:4d19fbcc0f0bb56e4a6b711398e5de3a634385319d0e8b2bbc0171c109260070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.1 MB (606115637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3374c6411cbaed1bfb06437a6e1edc6a41bd7b83e37ca5ecc6a1aaec09413300`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e2f2830e2003232ca51768518e8eb9e372430ea0c0445d3ec3c8d96672cb8c`  
		Last Modified: Fri, 27 Sep 2024 06:05:25 GMT  
		Size: 214.3 MB (214285718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83748e1ac06a3fcddae1dc3110de6342c4531f82f43779a5fabf89719505db6a`  
		Last Modified: Sat, 28 Sep 2024 05:54:49 GMT  
		Size: 242.7 MB (242735060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:606824019a2d5065cd43eaea75ffe3725a698dd0f28a75d3e050d7cccc157b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15440370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa45a38a900b92dbf585c0410238a0e5b5c4b9b926802c9c7acad6c298aeda8f`

```dockerfile
```

-	Layers:
	-	`sha256:9ab533a7bde3dae7d525cc723b7c2e2eeb5504de5e82bb10f2a6051c078f243c`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 15.4 MB (15427343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c830e1f96c43a12bb0b2d3f79e8307d9635fb3e3532b2762ab339dff8d8738fd`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 13.0 KB (13027 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:0d9fc54c3ca5405db6f5892b2d90b374c38cab322301c88c164cb3d632dcacbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587261517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe66d1e8a70bea815ee500895b94596821696d893861c02b693a4f83ae31166c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1411196315040fbdc5fb36f5519fcdf47619046fa9476d4e7607333bcbd8131`  
		Last Modified: Fri, 27 Sep 2024 03:21:02 GMT  
		Size: 183.3 MB (183287662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35ddee15ec8c9e03e7f842b910c8fd17fe9bfef5ca8c21b7f32fbff8bbcc496`  
		Last Modified: Fri, 27 Sep 2024 17:40:49 GMT  
		Size: 268.5 MB (268487969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:03ac78767400c1d1b9c984acca6bd90df72cac0fb00e9100b2c5a8ee2438346e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15278999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1375e7d3522dd5c1a611790297f685c2fe0704944053af8e43e7d8a89930cc3`

```dockerfile
```

-	Layers:
	-	`sha256:f28e04508e5f7206d96f053f77275ef0c0bb7fa9f8a03c918a24d3fb10588e28`  
		Last Modified: Fri, 27 Sep 2024 17:40:44 GMT  
		Size: 15.3 MB (15266033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1a546a507332436c927687563a98866a316dbc8fab3ac46845bfa34cbe62b1`  
		Last Modified: Fri, 27 Sep 2024 17:40:43 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:d6e876ca5fe200f4ac60312b95606f0b042699c4cf6a19493b7d2a2ebbfb337b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:03b96a6b633cc6d3d1168e1afa2357ba5ccce128da909ba3b57487f0cc228428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283243467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c2a31537b2eac7656edddd62805b51abda9efb6f3761a92363fd35bac462ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7a6c0b92f840b647ad3fdd4fc8c1739f833da486d7e51793f4c1ebe411333`  
		Last Modified: Fri, 06 Sep 2024 23:25:12 GMT  
		Size: 55.3 MB (55309249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d299bec348b12e4baacefd5ece1f43bfb77ef3abe2e52f56ad4d5e67c263b056`  
		Last Modified: Fri, 06 Sep 2024 23:25:20 GMT  
		Size: 224.3 MB (224310411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:1d57ee624f00a8ce856aa31ba4730a87c91d9a11b9fd595f3d385f5bb44ece20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6497981077302a8c905b5e4e2dfffd9ac14137a0cfc7497d4dcafc806053e7`

```dockerfile
```

-	Layers:
	-	`sha256:da26bdf9689b6139ac3ee467c818e036ca25e103dae29ddb9f158f48efec517d`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2530f84e604ec82ab6979568cbfe879a3721c0a3adea3f06fb87cda5819f968e`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 11.7 KB (11678 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d577dfa9ebb3576ed0824cd4a6665ce2a1a37b908bf767ed0f96c10360f19e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291454748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193dfcd4e8418a0b3ab51d24dd2601d67cb5f6f7446bdcf55c7fc139421a0836`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dae75a7979f5c823e78faad77f0683f4120db209a14f80f65d35ffcfb6465c`  
		Last Modified: Sat, 07 Sep 2024 11:56:50 GMT  
		Size: 52.9 MB (52946235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d0ba6d79ddcc7adb2e073c295844423f77032e7b03bc7973c24f60d3d5ae3`  
		Last Modified: Sat, 07 Sep 2024 11:56:54 GMT  
		Size: 234.4 MB (234420867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:09413672bd07b597f07a8cc58f505f88e517959490527c39693b43a71c238377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f7960713521b5f6f4f75e0f419a67822c4ca3ac34eedb0753910785c0c3881`

```dockerfile
```

-	Layers:
	-	`sha256:b85be6b172df08e0e211efd0e6354594a97df69970d84ea800b01169be9286f4`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486ea238c8b03b69cfc3df4c2c5336edce93eb2ae87385c5b1b31951f59bdef2`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:5b6bdc02ef966d208c7edc309d3cdf75725b3a0fe6535f4460f9d2d7fb88322b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:c45cc04288af707001a7a90382d16dc29309508b0d274a4c61282bad7ecd8345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283076960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e2a973eb4a9819fb599046858b1ccd486ae9157ed0d695bb65d7016cb83135`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b596d4da02c982671dbf6bed836470acee3a2fadc6863ba9e1cce5e388c93ab`  
		Last Modified: Fri, 06 Sep 2024 23:24:43 GMT  
		Size: 55.3 MB (55346883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872d9e0d3eae5459c9159c8cc624a3c35789017552614cda7063b19930cfda94`  
		Last Modified: Fri, 06 Sep 2024 23:24:47 GMT  
		Size: 224.3 MB (224310371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:e32690943c1038ed26065af835abea2eb061b1715bfd4330fe65d48ec1198103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdc2c73e311f0afde5234e3a30984507a7113be703884269be015f6a435cf5d`

```dockerfile
```

-	Layers:
	-	`sha256:612b4526cbae481700ab36cb68a6c9c0af9f27506d9f7dbe6867e3fb2e9a3ddd`  
		Last Modified: Fri, 06 Sep 2024 23:24:42 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e67ae8c135e6a6076ec3f5355c54c343cef04d8f379ed48c426f2dd6ba2622c9`  
		Last Modified: Fri, 06 Sep 2024 23:24:42 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2ad5d810439717463a3ad522bfe9c626490ca35176488b753a9e57d23f35d9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290775337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e25ee6035525a540920de98ffd4b96c964d2195252fb1dc32743828b84b0b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74da714a92090eec171b9fdcc6c89c6591ba432fdeeaa10d5c10538ede56c8a`  
		Last Modified: Sat, 07 Sep 2024 11:55:42 GMT  
		Size: 53.0 MB (52995429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b56e9f588d67bf61a8465ec612c0b1095ef03b2d5afe03498b7ad4fed2fd38f`  
		Last Modified: Sat, 07 Sep 2024 11:55:47 GMT  
		Size: 234.4 MB (234420805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:f9446358434100ac647f0d3dd9a0e1b2005a6f8910ede685cdc2e9e9c2ec5eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644500100d93dbb3715254eb9f6a6028976c644a3ea440840fa3de87e015593a`

```dockerfile
```

-	Layers:
	-	`sha256:5318473dfb1acaa5a3766971ec81932624e4e3e24520ff1226b8de3a4d1eabbc`  
		Last Modified: Sat, 07 Sep 2024 11:55:41 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5f4a984e365a0132171af9a5448f3da92750593f5660cb7358ca62cbe7b3b30`  
		Last Modified: Sat, 07 Sep 2024 11:55:40 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:d6e876ca5fe200f4ac60312b95606f0b042699c4cf6a19493b7d2a2ebbfb337b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:03b96a6b633cc6d3d1168e1afa2357ba5ccce128da909ba3b57487f0cc228428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283243467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c2a31537b2eac7656edddd62805b51abda9efb6f3761a92363fd35bac462ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7a6c0b92f840b647ad3fdd4fc8c1739f833da486d7e51793f4c1ebe411333`  
		Last Modified: Fri, 06 Sep 2024 23:25:12 GMT  
		Size: 55.3 MB (55309249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d299bec348b12e4baacefd5ece1f43bfb77ef3abe2e52f56ad4d5e67c263b056`  
		Last Modified: Fri, 06 Sep 2024 23:25:20 GMT  
		Size: 224.3 MB (224310411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1d57ee624f00a8ce856aa31ba4730a87c91d9a11b9fd595f3d385f5bb44ece20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6497981077302a8c905b5e4e2dfffd9ac14137a0cfc7497d4dcafc806053e7`

```dockerfile
```

-	Layers:
	-	`sha256:da26bdf9689b6139ac3ee467c818e036ca25e103dae29ddb9f158f48efec517d`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2530f84e604ec82ab6979568cbfe879a3721c0a3adea3f06fb87cda5819f968e`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 11.7 KB (11678 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d577dfa9ebb3576ed0824cd4a6665ce2a1a37b908bf767ed0f96c10360f19e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291454748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193dfcd4e8418a0b3ab51d24dd2601d67cb5f6f7446bdcf55c7fc139421a0836`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dae75a7979f5c823e78faad77f0683f4120db209a14f80f65d35ffcfb6465c`  
		Last Modified: Sat, 07 Sep 2024 11:56:50 GMT  
		Size: 52.9 MB (52946235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d0ba6d79ddcc7adb2e073c295844423f77032e7b03bc7973c24f60d3d5ae3`  
		Last Modified: Sat, 07 Sep 2024 11:56:54 GMT  
		Size: 234.4 MB (234420867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:09413672bd07b597f07a8cc58f505f88e517959490527c39693b43a71c238377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f7960713521b5f6f4f75e0f419a67822c4ca3ac34eedb0753910785c0c3881`

```dockerfile
```

-	Layers:
	-	`sha256:b85be6b172df08e0e211efd0e6354594a97df69970d84ea800b01169be9286f4`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486ea238c8b03b69cfc3df4c2c5336edce93eb2ae87385c5b1b31951f59bdef2`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:0757ed8c0609498399dfde17ad6e5ac4adc5da04096fbd3d9c2301c62b93546b
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
$ docker pull rust@sha256:62afc139057dc9d3eda02e490677911b55a208ba22d6f7315f3c5c5851e31a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533623479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3b0145b0fabfa9f7bfc382e163449775329c6b95cb5704237a770a9e6e52a1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba0b3d08b81baa192d30dbb2257b8227f2a4eab719c79ef1c419e3a07b39dbc`  
		Last Modified: Thu, 17 Oct 2024 01:10:04 GMT  
		Size: 64.4 MB (64393080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bc85537ac7c401eea9ed38d4a75fddbe5d75d5570921f1c435a8342b3cef15`  
		Last Modified: Thu, 17 Oct 2024 01:10:40 GMT  
		Size: 211.3 MB (211281151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97b348fbebca67b25f027e550f95573ba6aff2f81f748dbf3e11e96d7fc6da6`  
		Last Modified: Thu, 17 Oct 2024 02:57:32 GMT  
		Size: 184.3 MB (184341137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:afd613e0c8388610680d95743ce6b0519e2e288ab2180009d03fdee5263cf66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ce36b1a51263afe43943de85c9d45999d4fd4b9197ac8e48278804e18c1582`

```dockerfile
```

-	Layers:
	-	`sha256:7b956ebc4fdf5bc354458d55f06403a6a7feff6dbe43975c601c444a5d70edc5`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde1eebb12461b3cf18799768782571274684aa61647d4c0e77a0b7d51d3c40`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 13.0 KB (13004 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:27b6e9bd919166bac1fb9211e9e52449d5fb725a70122e2280b3f235eef01f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.5 MB (523464584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd1ab1a770c8f7aa48d8b41c6152318ce574fb409b4620f8fea171c3ba763c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea668db82ddd31e7300e905d69bfbcc24fd0c70cd7c7212c915763a9e47f3e7`  
		Last Modified: Fri, 27 Sep 2024 07:39:33 GMT  
		Size: 175.2 MB (175207938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807abecaed8d4cffae0b7d1da027197029821fd16d2bbce8c0f8a1f90fd349f3`  
		Last Modified: Sat, 28 Sep 2024 04:08:11 GMT  
		Size: 221.5 MB (221511519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ee2cbc5b0aa8369395392c722b55ad9ac0bd4916118b0cdf63d4d0f13269a299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15270591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa74c1d6fa4c9dda9c706f2706450a4b81da24d4559310f49de7e46773f9700`

```dockerfile
```

-	Layers:
	-	`sha256:45c0558bf77c60592fcc61666d1d55c2e8062c13eee2815becd8547e5fe62df5`  
		Last Modified: Sat, 28 Sep 2024 04:08:07 GMT  
		Size: 15.3 MB (15257523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab9e3cff7b672ef6b62a3eecbf1b9c661a226d91214cd3d7b68a9fd5b262ff05`  
		Last Modified: Sat, 28 Sep 2024 04:08:06 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f5fbbf475717a8e1fcfda24fc26c60200eb95e19b03291f3e43e60995a4d406e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.7 MB (588709463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d76e87cace62dbdc9c3a6c3fae1623de64a44b8b274d79b8e95bcd89b6f1e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71ace0e8bbdcfcf795b836e24a37a6ed0054100e14d6aa6e5a63f7e162ba729`  
		Last Modified: Fri, 27 Sep 2024 05:25:40 GMT  
		Size: 202.7 MB (202651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c70a9d34bb788145305c907ff9a5ed64690b67c5abbc4b676ff607611081e0`  
		Last Modified: Fri, 27 Sep 2024 23:30:32 GMT  
		Size: 248.5 MB (248529120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:be6c0d1bdd139e794a093f63bbdcf7c53acbacba5babbcf59b54af8fd37f7cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15494574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23350ebe95ee44b5c009236d86e0a9d13772ae5689fa9c3449fec0987bd7b81d`

```dockerfile
```

-	Layers:
	-	`sha256:7c227d855755631f9fc25b4280c874ce996590e6446ce7c7399e0c496bd31670`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 15.5 MB (15481248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a10530d2c00a615465f62c3a9b01ff478facbfb4d920cbbf7d0d386c559eb44`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:cae43437babe4a513bfaf1ebaed7b47e916e1a96bea4496ee763708f2a2b5bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549225958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af64455d7089be15c70fda713c93555e12afb877f65a7b29d2b3dddfab02d1f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9dd8137152c295fb3624be3ee13689c34dc13bc115d0032a5a2a581001f14f`  
		Last Modified: Thu, 17 Oct 2024 01:09:36 GMT  
		Size: 24.9 MB (24895435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbad5c607546fed7ceeb86b3cef161781f7cb90e39cb2c8da1b7774aa73975d4`  
		Last Modified: Thu, 17 Oct 2024 01:09:58 GMT  
		Size: 66.2 MB (66210908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c0ef7e16c4ea3f5643d06ea746c15f35cca787121e7078904f6a16114c48`  
		Last Modified: Thu, 17 Oct 2024 01:10:44 GMT  
		Size: 210.2 MB (210196330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f818dcff8930802b82fed8fbd3b89feef62a7b69bc64cebb8df64281a6dd9`  
		Last Modified: Thu, 17 Oct 2024 02:57:36 GMT  
		Size: 197.3 MB (197346451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bc528a75faa20afa57e2c7e4b6f51d9b57b5485d2d379eea44c3bf52d6fbd4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808162f63c550251d4aaa7a5eee4f171d732b78e387b1137976a4a926ec4476c`

```dockerfile
```

-	Layers:
	-	`sha256:cecf68aacf4ab8230e1cd8e54fe8e2c4fe0ecb15f64b69df35db646913b7bdd2`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73cb9933a9869db1cc6fb4636124d96cbfd43111b4b05b820c4e12217bc5b56`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:4d19fbcc0f0bb56e4a6b711398e5de3a634385319d0e8b2bbc0171c109260070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.1 MB (606115637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3374c6411cbaed1bfb06437a6e1edc6a41bd7b83e37ca5ecc6a1aaec09413300`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e2f2830e2003232ca51768518e8eb9e372430ea0c0445d3ec3c8d96672cb8c`  
		Last Modified: Fri, 27 Sep 2024 06:05:25 GMT  
		Size: 214.3 MB (214285718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83748e1ac06a3fcddae1dc3110de6342c4531f82f43779a5fabf89719505db6a`  
		Last Modified: Sat, 28 Sep 2024 05:54:49 GMT  
		Size: 242.7 MB (242735060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:606824019a2d5065cd43eaea75ffe3725a698dd0f28a75d3e050d7cccc157b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15440370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa45a38a900b92dbf585c0410238a0e5b5c4b9b926802c9c7acad6c298aeda8f`

```dockerfile
```

-	Layers:
	-	`sha256:9ab533a7bde3dae7d525cc723b7c2e2eeb5504de5e82bb10f2a6051c078f243c`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 15.4 MB (15427343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c830e1f96c43a12bb0b2d3f79e8307d9635fb3e3532b2762ab339dff8d8738fd`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 13.0 KB (13027 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:0d9fc54c3ca5405db6f5892b2d90b374c38cab322301c88c164cb3d632dcacbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587261517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe66d1e8a70bea815ee500895b94596821696d893861c02b693a4f83ae31166c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1411196315040fbdc5fb36f5519fcdf47619046fa9476d4e7607333bcbd8131`  
		Last Modified: Fri, 27 Sep 2024 03:21:02 GMT  
		Size: 183.3 MB (183287662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35ddee15ec8c9e03e7f842b910c8fd17fe9bfef5ca8c21b7f32fbff8bbcc496`  
		Last Modified: Fri, 27 Sep 2024 17:40:49 GMT  
		Size: 268.5 MB (268487969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:03ac78767400c1d1b9c984acca6bd90df72cac0fb00e9100b2c5a8ee2438346e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15278999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1375e7d3522dd5c1a611790297f685c2fe0704944053af8e43e7d8a89930cc3`

```dockerfile
```

-	Layers:
	-	`sha256:f28e04508e5f7206d96f053f77275ef0c0bb7fa9f8a03c918a24d3fb10588e28`  
		Last Modified: Fri, 27 Sep 2024 17:40:44 GMT  
		Size: 15.3 MB (15266033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1a546a507332436c927687563a98866a316dbc8fab3ac46845bfa34cbe62b1`  
		Last Modified: Fri, 27 Sep 2024 17:40:43 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:8328d21407009f8a2d17b0327f32c63411a8c3d5590b71ab87ea993cd2ffd169
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
$ docker pull rust@sha256:c0c156a4887bdbf6abea8f98258d9d27cfe4c3f2794f674dfb6f5d237de67687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.0 MB (506995658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f511550e16ed987835311ad1d9c0da1b2b1d597b933aed15e44eb452187f9a9b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06817e07ed0f03c17ad0a7aa8ef22b2a6fcf2b939d6212ab0861571ef18a45b`  
		Last Modified: Thu, 17 Oct 2024 01:10:51 GMT  
		Size: 15.8 MB (15764889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173ffc78585eeabe33105e00a7be99b0cad17d5e6edebf7f760d7824fa76969`  
		Last Modified: Thu, 17 Oct 2024 01:11:06 GMT  
		Size: 54.7 MB (54723650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe335f0e34a87e4cbd05c121253490f0c293f8ff29540aa8cd3fc22d4519931`  
		Last Modified: Thu, 17 Oct 2024 01:11:36 GMT  
		Size: 197.1 MB (197085334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66586d4b6a786f40aa4eede68f290dbb5be4152d931746d9bbb17b4b085fcf7`  
		Last Modified: Thu, 17 Oct 2024 02:57:35 GMT  
		Size: 184.3 MB (184341174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7db843194e10c40a284a5f8742a0e692118d3bd1809aa01d16105ab7ec0823ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15063552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c6e3fd4ce8ce97591522bfaf2a495aa59ca89437e220dc586da3fde58d8f0e`

```dockerfile
```

-	Layers:
	-	`sha256:3e0db2ae8efc7a4b906bc15ffdce2bbda5f1c7cbea6015ea958b7c95523d700f`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 15.1 MB (15052438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2033b7ff7e29ef72ea44cc8fe20a94267d7ca6eaded58686e78d093bb6c8ed7f`  
		Last Modified: Thu, 17 Oct 2024 02:57:30 GMT  
		Size: 11.1 KB (11114 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:84331046d2e6bbfe4845d2ef8384cc8281fcbcf0e28fd1071709a3aa34eab212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.8 MB (504758766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d19257130fa88be44790843793cd4e706a1b61733f0e90388b767119ffb2bb`
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
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec523352a6e63a855ebebdbc8288b9cccf719fe4121211d5e0cae3f11e4f6b2`  
		Last Modified: Fri, 27 Sep 2024 07:39:46 GMT  
		Size: 14.9 MB (14879678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bfb8add2d4bda22b21df2a3eff38a6f4f66c2ef9fe110e7714a93f720a4f47`  
		Last Modified: Fri, 27 Sep 2024 07:40:06 GMT  
		Size: 50.6 MB (50618560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f69bcefdc97cf5fabaf3b01d416ce54278fa217058c4433beb68d39a6e1bc1`  
		Last Modified: Fri, 27 Sep 2024 07:40:47 GMT  
		Size: 167.5 MB (167508654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc16697bf56cf2fe7d356c600c48e8a13b2fb6f003a40aec403b77bf1e5a1777`  
		Last Modified: Mon, 07 Oct 2024 20:10:32 GMT  
		Size: 221.5 MB (221511494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3c9b6060fce57e62fb04164d07286dabb9431d2eb979eb665cf468a807fbe9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14864469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873edee47bb20240914debd5c61b9dd61ca27e7d1d73fc95f7657eb67d1419a4`

```dockerfile
```

-	Layers:
	-	`sha256:9e1a11645f7ce0d9026d44c1007e1f6ba2b3f0765e25fa435075743651016034`  
		Last Modified: Mon, 07 Oct 2024 20:10:28 GMT  
		Size: 14.9 MB (14853318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c5c9edc1a5a4d7481d377fa24e5662235f1ce8b366e78cd64a8bc412ee69cb7`  
		Last Modified: Mon, 07 Oct 2024 20:10:27 GMT  
		Size: 11.2 KB (11151 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:230f0887e9953ba599f30462d1601b3af95d1136cf8c1057b77533f0ea13993d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.8 MB (562811378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7fd17cd619497e8cf227bc8f6b6be5a4ceaf9020f09b88694555ccf79d7f65`
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
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4bba36b8add5e5ec5da6aa2c18637b64bce2d5f3f7d83723817e2139a11bcc`  
		Last Modified: Fri, 27 Sep 2024 05:25:50 GMT  
		Size: 15.7 MB (15749698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f212bcfdd3a473cde2991df3e1cf5373d8f097a630557a35fa77d891acce93d6`  
		Last Modified: Fri, 27 Sep 2024 05:26:04 GMT  
		Size: 54.8 MB (54834694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09310330a122777457e6d6b3094e1d1391aa246ba1b028adeb03cd353d0d29`  
		Last Modified: Fri, 27 Sep 2024 05:26:28 GMT  
		Size: 190.0 MB (189964252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da761adc8113e8e908061d91c6af387f04a41e668d2f111540d11a9ef01e5f0`  
		Last Modified: Mon, 07 Oct 2024 20:28:00 GMT  
		Size: 248.5 MB (248528870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f7218307ed60ee81340e8a569d237e241c8e97cac632dc78555ab6083d40909e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15065824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fecd41b23cc4f020e9f319dbf75f1613baa97e283f738646f4a549d49a0a29`

```dockerfile
```

-	Layers:
	-	`sha256:fecaccd039897250aae8a94b1523d4955c0726ff860d9f3a605565fd7b63d201`  
		Last Modified: Mon, 07 Oct 2024 20:27:55 GMT  
		Size: 15.1 MB (15054645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:357925a5449c30f481550c08a6e83d080b7faa1982dfdb43af76649057e41280`  
		Last Modified: Mon, 07 Oct 2024 20:27:54 GMT  
		Size: 11.2 KB (11179 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:0b74763c0c9110dc9342754e733f284101a3090b083abd7c9eb73f9e9162fee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.7 MB (525706874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01cf6a6c0b6626ce6748e3de2ff0182d8febe57f7c55eac503d91d6f9a3e1c7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000ce4e381f50a8f76ae5a1d4bcd9702f5146bac4fb30afc4e12c284ee68ca9`  
		Last Modified: Thu, 17 Oct 2024 01:10:55 GMT  
		Size: 16.3 MB (16268542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d0b1f51e6e34773cde9f3b41201942ff88384d907912b25ff3349f296f69b8`  
		Last Modified: Thu, 17 Oct 2024 01:11:14 GMT  
		Size: 56.0 MB (56032019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b257135cb04b7c9d5ceaf0572a0941a80b7eb3f7dd31444289a12b792e314e8`  
		Last Modified: Thu, 17 Oct 2024 01:12:01 GMT  
		Size: 200.0 MB (199982090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3420ca7067654974fc0f1971890285287aef101e8c0ad81c1d01689969ded4ec`  
		Last Modified: Thu, 17 Oct 2024 02:57:46 GMT  
		Size: 197.3 MB (197346400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f58b08210121da703d98863e10d84097f158a04b4f053e9f579b47a0ecd6819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b309ca17610165025ded60cffba70e585bf2294d8a81fe1ff260572e71d460d`

```dockerfile
```

-	Layers:
	-	`sha256:c660bef212dab636443f1060b4e1e7ca7a48a89cdf8c12a8d6298cf1ed6616f6`  
		Last Modified: Thu, 17 Oct 2024 02:57:42 GMT  
		Size: 15.0 MB (15040975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f6ca99ad4fa67ac8b5d8bd3b23ad2542d63b6634953bb2057d5c3e1a4443b8`  
		Last Modified: Thu, 17 Oct 2024 02:57:42 GMT  
		Size: 11.1 KB (11085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:5f54e4f0f25ffcb8493d73f38cbd7dd5f6b83ca78d6a33224fc326f6d654d16f
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
$ docker pull rust@sha256:45966c8f3e8348b7643bd40eb846b87015a6f1694ed2a13ca8475c5be35df8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284254306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b63b5bcc9542ec50795afee904fd719f71dbf5f3cd84e74de4c92f7808a727f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0607d7c68e964f9d197627ffe492db8c9ce40d39951ee73a3182e028b0be4e`  
		Last Modified: Thu, 17 Oct 2024 01:30:10 GMT  
		Size: 255.1 MB (255128017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:f17aeca9415c8c8b3eec6d14b5a90f91bbe302ef815e6513d5763f9b1d2b645c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010e722839b0079d58e9aa6bcd3b6446f5bd6702bbfe47fc984b869d24c68e15`

```dockerfile
```

-	Layers:
	-	`sha256:e6e2cf59070156e4177eabcbb570b524e550d23ecba4082cc0876549b6a34458`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78cde42d64af02ec433aba2279aede7b5ce92746174556b598fd74de7abd9517`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 13.1 KB (13090 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:08dbf3d9d24bae232365620c62410ec5d83596ff380aad5f49e27cdec7317513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294070169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e6abf46c4d525890ed87fc173518b54a4bd6a1b01b96fe447fb1d17e08346a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4408bd841243a9a42a8e256c364029c480e1b0b2865b22e70a46bde0100c866`  
		Last Modified: Fri, 27 Sep 2024 18:42:06 GMT  
		Size: 269.4 MB (269352024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:df722b016f3cca3b94348d0bc6f597be00e94961777ca5cb428cf4cdd0af6f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e61fad66437481804743201bd550faf73c0e8846ddb64f6d8bf18e0dff7a4a3`

```dockerfile
```

-	Layers:
	-	`sha256:e090a867d43bfae1fb514bbb85985f7c87fff9bd5a411d0ec1cdcf062ed1c5f1`  
		Last Modified: Fri, 27 Sep 2024 18:42:01 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffb56d93014b97c2bf56f856a3b3c0c1c6de63989a9e8fca173c3abc901f156`  
		Last Modified: Fri, 27 Sep 2024 18:42:00 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3ba3fbf62527788a60c4908b3c389bab7f5ab6fb919ea3c771aeb9a278966253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343526226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233c27109e17c04665f9ed9ede09369aacd1865fc09fd1a6f5ac4863e32fc4a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995fd26d021eddb871651f81a432e2662de3c5b719d2248d4552105c40a67e47`  
		Last Modified: Fri, 27 Sep 2024 23:32:02 GMT  
		Size: 314.4 MB (314369857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:e4a5a923d2e13d83eb71aa2cb933b273577721a70c5ff55a15af8cd5f4d21978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633019f2483a2e86da7ee1384084a836d087aab2347f626c8490a683b80397fc`

```dockerfile
```

-	Layers:
	-	`sha256:45375e55489ffbdb8bd47dbec3eee1f67a6679081f46e4dc1ac6c76ce18b1904`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f968eae71eae982a4adc164da8a72a293dd418f197ba71ede38a68bb18be6c05`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:ba4ee661bb466ab49f6ceb8c6d9e9f9784bba7c6e45225187cd3c7fb1fbc12ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295093589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e4df283163309e2fdaa8101fa73b670d133162155d4cd23424016dd87db8e4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a718584a1346679f83b1655ad2ac313c29bec26411eeb7c34dad2a91b6577448`  
		Last Modified: Thu, 17 Oct 2024 01:30:07 GMT  
		Size: 264.9 MB (264949322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4c72332e16899bfc022e891c90f0d93e00f555271f92b2e38817f8afa453c722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ca94475147e0318e9bad8ec073ef9dd87fef510c2eed0171a3f48a81c843a`

```dockerfile
```

-	Layers:
	-	`sha256:12434a1e188136de888271297f6eb4670c269905a0833cb0c26866ab817a1eac`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11e3392f42511d72755c775a9cd45fb9f2d612485058889a5a61cbb5dda587f`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 13.0 KB (13043 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:46bcce128e6ab5402c648739e95aa56eb2ed32d840ff42da0975ec8428034ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344618727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4f6cbc6fd8ecc671e77ece602998ab1fa543c11db83d5d64fa6bc051b111c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097a47a9153a9d3d44374a545c87a489f3842a16e291caf5a817ebaa5a0f1552`  
		Last Modified: Sat, 28 Sep 2024 04:15:09 GMT  
		Size: 311.5 MB (311496564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:fa335487319e81174f0920ee7efa014f25d5cdbbfdf8648c77cfeb1f771129bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f51b298cbeb650a1f7674e47e0ff5da39045f7a1c1b12678284013db4153e2`

```dockerfile
```

-	Layers:
	-	`sha256:17e6bf4b03c232f13acb280f35f3b04cad777afeab1156732f6d6e80ae08ac03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9673908047a020854098b5704b6ac719a43c3c5263868a007ef95e1dd656fe03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:1986b817125878c181d9add8424b112238bbcd915e03b3444b6e3b9962a71844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346124228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaf144d0210bf05141bac7875bc21c09171ace17f17693c306e46ee2347cc8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d24393939cc6c4eddc3a49c03d07080edb453591af15f5f40c3481b1c43289`  
		Last Modified: Fri, 27 Sep 2024 17:42:41 GMT  
		Size: 318.6 MB (318634204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:981dce7ac4cd7769d68270976ad41a566057debc664228639318ceeee2878c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb7573b7c4578171c99e4b1c475220bae80fd01a2abcc1ff7de0c789cee9993`

```dockerfile
```

-	Layers:
	-	`sha256:165fd9d1067cb2b20bc1127fb26bf62317d9ec727e17d418b73ad480975a460f`  
		Last Modified: Fri, 27 Sep 2024 17:42:37 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03aa2d5f9daee31ee7485507b38e1a42c341c49bd4f504117c96708fe84908d5`  
		Last Modified: Fri, 27 Sep 2024 17:42:36 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:5f54e4f0f25ffcb8493d73f38cbd7dd5f6b83ca78d6a33224fc326f6d654d16f
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
$ docker pull rust@sha256:45966c8f3e8348b7643bd40eb846b87015a6f1694ed2a13ca8475c5be35df8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284254306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b63b5bcc9542ec50795afee904fd719f71dbf5f3cd84e74de4c92f7808a727f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0607d7c68e964f9d197627ffe492db8c9ce40d39951ee73a3182e028b0be4e`  
		Last Modified: Thu, 17 Oct 2024 01:30:10 GMT  
		Size: 255.1 MB (255128017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f17aeca9415c8c8b3eec6d14b5a90f91bbe302ef815e6513d5763f9b1d2b645c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010e722839b0079d58e9aa6bcd3b6446f5bd6702bbfe47fc984b869d24c68e15`

```dockerfile
```

-	Layers:
	-	`sha256:e6e2cf59070156e4177eabcbb570b524e550d23ecba4082cc0876549b6a34458`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78cde42d64af02ec433aba2279aede7b5ce92746174556b598fd74de7abd9517`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 13.1 KB (13090 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:08dbf3d9d24bae232365620c62410ec5d83596ff380aad5f49e27cdec7317513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294070169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e6abf46c4d525890ed87fc173518b54a4bd6a1b01b96fe447fb1d17e08346a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4408bd841243a9a42a8e256c364029c480e1b0b2865b22e70a46bde0100c866`  
		Last Modified: Fri, 27 Sep 2024 18:42:06 GMT  
		Size: 269.4 MB (269352024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:df722b016f3cca3b94348d0bc6f597be00e94961777ca5cb428cf4cdd0af6f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e61fad66437481804743201bd550faf73c0e8846ddb64f6d8bf18e0dff7a4a3`

```dockerfile
```

-	Layers:
	-	`sha256:e090a867d43bfae1fb514bbb85985f7c87fff9bd5a411d0ec1cdcf062ed1c5f1`  
		Last Modified: Fri, 27 Sep 2024 18:42:01 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffb56d93014b97c2bf56f856a3b3c0c1c6de63989a9e8fca173c3abc901f156`  
		Last Modified: Fri, 27 Sep 2024 18:42:00 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3ba3fbf62527788a60c4908b3c389bab7f5ab6fb919ea3c771aeb9a278966253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343526226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233c27109e17c04665f9ed9ede09369aacd1865fc09fd1a6f5ac4863e32fc4a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995fd26d021eddb871651f81a432e2662de3c5b719d2248d4552105c40a67e47`  
		Last Modified: Fri, 27 Sep 2024 23:32:02 GMT  
		Size: 314.4 MB (314369857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e4a5a923d2e13d83eb71aa2cb933b273577721a70c5ff55a15af8cd5f4d21978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633019f2483a2e86da7ee1384084a836d087aab2347f626c8490a683b80397fc`

```dockerfile
```

-	Layers:
	-	`sha256:45375e55489ffbdb8bd47dbec3eee1f67a6679081f46e4dc1ac6c76ce18b1904`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f968eae71eae982a4adc164da8a72a293dd418f197ba71ede38a68bb18be6c05`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:ba4ee661bb466ab49f6ceb8c6d9e9f9784bba7c6e45225187cd3c7fb1fbc12ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295093589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e4df283163309e2fdaa8101fa73b670d133162155d4cd23424016dd87db8e4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a718584a1346679f83b1655ad2ac313c29bec26411eeb7c34dad2a91b6577448`  
		Last Modified: Thu, 17 Oct 2024 01:30:07 GMT  
		Size: 264.9 MB (264949322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4c72332e16899bfc022e891c90f0d93e00f555271f92b2e38817f8afa453c722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ca94475147e0318e9bad8ec073ef9dd87fef510c2eed0171a3f48a81c843a`

```dockerfile
```

-	Layers:
	-	`sha256:12434a1e188136de888271297f6eb4670c269905a0833cb0c26866ab817a1eac`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11e3392f42511d72755c775a9cd45fb9f2d612485058889a5a61cbb5dda587f`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 13.0 KB (13043 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:46bcce128e6ab5402c648739e95aa56eb2ed32d840ff42da0975ec8428034ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344618727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4f6cbc6fd8ecc671e77ece602998ab1fa543c11db83d5d64fa6bc051b111c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097a47a9153a9d3d44374a545c87a489f3842a16e291caf5a817ebaa5a0f1552`  
		Last Modified: Sat, 28 Sep 2024 04:15:09 GMT  
		Size: 311.5 MB (311496564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:fa335487319e81174f0920ee7efa014f25d5cdbbfdf8648c77cfeb1f771129bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f51b298cbeb650a1f7674e47e0ff5da39045f7a1c1b12678284013db4153e2`

```dockerfile
```

-	Layers:
	-	`sha256:17e6bf4b03c232f13acb280f35f3b04cad777afeab1156732f6d6e80ae08ac03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9673908047a020854098b5704b6ac719a43c3c5263868a007ef95e1dd656fe03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:1986b817125878c181d9add8424b112238bbcd915e03b3444b6e3b9962a71844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346124228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaf144d0210bf05141bac7875bc21c09171ace17f17693c306e46ee2347cc8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d24393939cc6c4eddc3a49c03d07080edb453591af15f5f40c3481b1c43289`  
		Last Modified: Fri, 27 Sep 2024 17:42:41 GMT  
		Size: 318.6 MB (318634204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:981dce7ac4cd7769d68270976ad41a566057debc664228639318ceeee2878c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb7573b7c4578171c99e4b1c475220bae80fd01a2abcc1ff7de0c789cee9993`

```dockerfile
```

-	Layers:
	-	`sha256:165fd9d1067cb2b20bc1127fb26bf62317d9ec727e17d418b73ad480975a460f`  
		Last Modified: Fri, 27 Sep 2024 17:42:37 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03aa2d5f9daee31ee7485507b38e1a42c341c49bd4f504117c96708fe84908d5`  
		Last Modified: Fri, 27 Sep 2024 17:42:36 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:915a4826b6111266e53e06f47c16cddebf36901623f0631f2cc10ce5c26022e5
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
$ docker pull rust@sha256:955e6b161e189ce9a70a3176d62bc853df1d45a8ff2c877bcc2639c1334e05da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275916178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72160f9a4acd420abe48f6f6d762750669ca08d8e16c3612f2aa8e48e6886df1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b38e595cdc330fbe56f1cc54e1fbb521c5c78b889fda1cb2553ec996eb7494`  
		Last Modified: Thu, 17 Oct 2024 01:28:56 GMT  
		Size: 244.5 MB (244487378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:913457ace1ef4de84bcd5852f75e36f52b6ec6cb0381db81b057670c1f7a64c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900b212c9018b48677c88ed0905ec79728757d918f45bb4e41c5f9ac0e6c8a10`

```dockerfile
```

-	Layers:
	-	`sha256:8347c9cf5193ed18506b7d4c96a1dd5a0451c1c9d4c0049fd6c1adaaefe4b7cb`  
		Last Modified: Thu, 17 Oct 2024 01:28:53 GMT  
		Size: 4.2 MB (4164416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee600185d29aecb0803b6cd08dc6117b7080dbec62c710fa35ae4dffc674e387`  
		Last Modified: Thu, 17 Oct 2024 01:28:53 GMT  
		Size: 11.2 KB (11176 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:649f33f2004e7cf32279d259133d1c887680c82371ca61040be0676de14478f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290373521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c1dea15d81a85919b55bae459fdf9865c474d6a3eeded3a426c223d45f15fe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:05 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
# Fri, 27 Sep 2024 05:14:07 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0961dc5030bdc38ffd749a496abefd5f5e3c43706db1ac4fbe6a89b425b6f565`  
		Last Modified: Mon, 07 Oct 2024 20:12:29 GMT  
		Size: 263.8 MB (263784209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0fdedd82265ee4abb67e00cb5ed763bb6b00b1e1a9cff139eb943b524eceddc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3984890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4338ea06da0c03a6090e3a6d0cdfbf4558bd2939605e26dcb73de43f3ae2445a`

```dockerfile
```

-	Layers:
	-	`sha256:ba5dd9365cb77053e5b690af6fb2194be4ea48e4cf45c38343e7917bf11ac2d6`  
		Last Modified: Mon, 07 Oct 2024 20:12:23 GMT  
		Size: 4.0 MB (3973677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71bcc530464af98ed85ff675234211982092c53f113700732ff05ba7b7063828`  
		Last Modified: Mon, 07 Oct 2024 20:12:22 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5a6a01ab245dd0f9c1c5289854e6bfbf41eda63717a403c2ec5715751e29df3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334323993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53157f2dc99d3da88944463c603f1435f567f3e51e835146526d5ddc3602023e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a5b36cf8f1de6f21df811fbf5e9fc34a4a885fdb4d55f5d99d5d38e9e10aa1`  
		Last Modified: Mon, 07 Oct 2024 20:29:36 GMT  
		Size: 304.2 MB (304248835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:117078f67d65fb1fb6692b2e819225b0028efe02b38e50d365a11fb8218ade4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4172348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7528c856c92358d9c7cab5571c3f927091bf38d06d14ae6832f0cdb6a0ea1f`

```dockerfile
```

-	Layers:
	-	`sha256:e585026bbab5521b31de85e6d76a91d424b33a11f16dfc4c480cb11110170e68`  
		Last Modified: Mon, 07 Oct 2024 20:29:28 GMT  
		Size: 4.2 MB (4161108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:115eecb4972db015834bb7865e3b2013bcb5784751739299b04ee1938b1efb82`  
		Last Modified: Mon, 07 Oct 2024 20:29:28 GMT  
		Size: 11.2 KB (11240 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b869a05737d767ce7fb7056cf77751bb5a8b8b577dfbc911a05c94b2d3754822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290535137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a880359cc690264cb0b553f18917849f5c945bc7ff9fea96ceea4696a15d345f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabfbb638063d13147d4f9a1a5694685c92adb5cf15ae94665eae2cd245e5f7a`  
		Last Modified: Thu, 17 Oct 2024 01:29:49 GMT  
		Size: 258.1 MB (258121307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e7bc0dd978b6918b697d54b2322bd89a8fc2364017dc1354c01927066ba886ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c222bd0ec93f4d3719cfa3e3ebd12b938ba155acbede32405b0b9551d71c0e27`

```dockerfile
```

-	Layers:
	-	`sha256:58a6810008287c12bb6320144c20f384550200c86b54ba7c87a2e079a24c5263`  
		Last Modified: Thu, 17 Oct 2024 01:29:43 GMT  
		Size: 4.2 MB (4156184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08b166a715fea1c9ef90fcc577433cc2762aea86d09168615d781dd8d5e38012`  
		Last Modified: Thu, 17 Oct 2024 01:29:43 GMT  
		Size: 11.1 KB (11146 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81`

```console
$ docker pull rust@sha256:0757ed8c0609498399dfde17ad6e5ac4adc5da04096fbd3d9c2301c62b93546b
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

### `rust:1.81` - linux; amd64

```console
$ docker pull rust@sha256:62afc139057dc9d3eda02e490677911b55a208ba22d6f7315f3c5c5851e31a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533623479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3b0145b0fabfa9f7bfc382e163449775329c6b95cb5704237a770a9e6e52a1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba0b3d08b81baa192d30dbb2257b8227f2a4eab719c79ef1c419e3a07b39dbc`  
		Last Modified: Thu, 17 Oct 2024 01:10:04 GMT  
		Size: 64.4 MB (64393080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bc85537ac7c401eea9ed38d4a75fddbe5d75d5570921f1c435a8342b3cef15`  
		Last Modified: Thu, 17 Oct 2024 01:10:40 GMT  
		Size: 211.3 MB (211281151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97b348fbebca67b25f027e550f95573ba6aff2f81f748dbf3e11e96d7fc6da6`  
		Last Modified: Thu, 17 Oct 2024 02:57:32 GMT  
		Size: 184.3 MB (184341137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81` - unknown; unknown

```console
$ docker pull rust@sha256:afd613e0c8388610680d95743ce6b0519e2e288ab2180009d03fdee5263cf66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ce36b1a51263afe43943de85c9d45999d4fd4b9197ac8e48278804e18c1582`

```dockerfile
```

-	Layers:
	-	`sha256:7b956ebc4fdf5bc354458d55f06403a6a7feff6dbe43975c601c444a5d70edc5`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde1eebb12461b3cf18799768782571274684aa61647d4c0e77a0b7d51d3c40`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 13.0 KB (13004 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81` - linux; arm variant v7

```console
$ docker pull rust@sha256:27b6e9bd919166bac1fb9211e9e52449d5fb725a70122e2280b3f235eef01f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.5 MB (523464584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd1ab1a770c8f7aa48d8b41c6152318ce574fb409b4620f8fea171c3ba763c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea668db82ddd31e7300e905d69bfbcc24fd0c70cd7c7212c915763a9e47f3e7`  
		Last Modified: Fri, 27 Sep 2024 07:39:33 GMT  
		Size: 175.2 MB (175207938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807abecaed8d4cffae0b7d1da027197029821fd16d2bbce8c0f8a1f90fd349f3`  
		Last Modified: Sat, 28 Sep 2024 04:08:11 GMT  
		Size: 221.5 MB (221511519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81` - unknown; unknown

```console
$ docker pull rust@sha256:ee2cbc5b0aa8369395392c722b55ad9ac0bd4916118b0cdf63d4d0f13269a299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15270591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa74c1d6fa4c9dda9c706f2706450a4b81da24d4559310f49de7e46773f9700`

```dockerfile
```

-	Layers:
	-	`sha256:45c0558bf77c60592fcc61666d1d55c2e8062c13eee2815becd8547e5fe62df5`  
		Last Modified: Sat, 28 Sep 2024 04:08:07 GMT  
		Size: 15.3 MB (15257523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab9e3cff7b672ef6b62a3eecbf1b9c661a226d91214cd3d7b68a9fd5b262ff05`  
		Last Modified: Sat, 28 Sep 2024 04:08:06 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f5fbbf475717a8e1fcfda24fc26c60200eb95e19b03291f3e43e60995a4d406e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.7 MB (588709463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d76e87cace62dbdc9c3a6c3fae1623de64a44b8b274d79b8e95bcd89b6f1e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71ace0e8bbdcfcf795b836e24a37a6ed0054100e14d6aa6e5a63f7e162ba729`  
		Last Modified: Fri, 27 Sep 2024 05:25:40 GMT  
		Size: 202.7 MB (202651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c70a9d34bb788145305c907ff9a5ed64690b67c5abbc4b676ff607611081e0`  
		Last Modified: Fri, 27 Sep 2024 23:30:32 GMT  
		Size: 248.5 MB (248529120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81` - unknown; unknown

```console
$ docker pull rust@sha256:be6c0d1bdd139e794a093f63bbdcf7c53acbacba5babbcf59b54af8fd37f7cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15494574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23350ebe95ee44b5c009236d86e0a9d13772ae5689fa9c3449fec0987bd7b81d`

```dockerfile
```

-	Layers:
	-	`sha256:7c227d855755631f9fc25b4280c874ce996590e6446ce7c7399e0c496bd31670`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 15.5 MB (15481248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a10530d2c00a615465f62c3a9b01ff478facbfb4d920cbbf7d0d386c559eb44`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81` - linux; 386

```console
$ docker pull rust@sha256:cae43437babe4a513bfaf1ebaed7b47e916e1a96bea4496ee763708f2a2b5bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549225958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af64455d7089be15c70fda713c93555e12afb877f65a7b29d2b3dddfab02d1f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9dd8137152c295fb3624be3ee13689c34dc13bc115d0032a5a2a581001f14f`  
		Last Modified: Thu, 17 Oct 2024 01:09:36 GMT  
		Size: 24.9 MB (24895435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbad5c607546fed7ceeb86b3cef161781f7cb90e39cb2c8da1b7774aa73975d4`  
		Last Modified: Thu, 17 Oct 2024 01:09:58 GMT  
		Size: 66.2 MB (66210908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c0ef7e16c4ea3f5643d06ea746c15f35cca787121e7078904f6a16114c48`  
		Last Modified: Thu, 17 Oct 2024 01:10:44 GMT  
		Size: 210.2 MB (210196330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f818dcff8930802b82fed8fbd3b89feef62a7b69bc64cebb8df64281a6dd9`  
		Last Modified: Thu, 17 Oct 2024 02:57:36 GMT  
		Size: 197.3 MB (197346451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81` - unknown; unknown

```console
$ docker pull rust@sha256:bc528a75faa20afa57e2c7e4b6f51d9b57b5485d2d379eea44c3bf52d6fbd4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808162f63c550251d4aaa7a5eee4f171d732b78e387b1137976a4a926ec4476c`

```dockerfile
```

-	Layers:
	-	`sha256:cecf68aacf4ab8230e1cd8e54fe8e2c4fe0ecb15f64b69df35db646913b7bdd2`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73cb9933a9869db1cc6fb4636124d96cbfd43111b4b05b820c4e12217bc5b56`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81` - linux; ppc64le

```console
$ docker pull rust@sha256:4d19fbcc0f0bb56e4a6b711398e5de3a634385319d0e8b2bbc0171c109260070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.1 MB (606115637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3374c6411cbaed1bfb06437a6e1edc6a41bd7b83e37ca5ecc6a1aaec09413300`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e2f2830e2003232ca51768518e8eb9e372430ea0c0445d3ec3c8d96672cb8c`  
		Last Modified: Fri, 27 Sep 2024 06:05:25 GMT  
		Size: 214.3 MB (214285718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83748e1ac06a3fcddae1dc3110de6342c4531f82f43779a5fabf89719505db6a`  
		Last Modified: Sat, 28 Sep 2024 05:54:49 GMT  
		Size: 242.7 MB (242735060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81` - unknown; unknown

```console
$ docker pull rust@sha256:606824019a2d5065cd43eaea75ffe3725a698dd0f28a75d3e050d7cccc157b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15440370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa45a38a900b92dbf585c0410238a0e5b5c4b9b926802c9c7acad6c298aeda8f`

```dockerfile
```

-	Layers:
	-	`sha256:9ab533a7bde3dae7d525cc723b7c2e2eeb5504de5e82bb10f2a6051c078f243c`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 15.4 MB (15427343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c830e1f96c43a12bb0b2d3f79e8307d9635fb3e3532b2762ab339dff8d8738fd`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 13.0 KB (13027 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81` - linux; s390x

```console
$ docker pull rust@sha256:0d9fc54c3ca5405db6f5892b2d90b374c38cab322301c88c164cb3d632dcacbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587261517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe66d1e8a70bea815ee500895b94596821696d893861c02b693a4f83ae31166c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1411196315040fbdc5fb36f5519fcdf47619046fa9476d4e7607333bcbd8131`  
		Last Modified: Fri, 27 Sep 2024 03:21:02 GMT  
		Size: 183.3 MB (183287662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35ddee15ec8c9e03e7f842b910c8fd17fe9bfef5ca8c21b7f32fbff8bbcc496`  
		Last Modified: Fri, 27 Sep 2024 17:40:49 GMT  
		Size: 268.5 MB (268487969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81` - unknown; unknown

```console
$ docker pull rust@sha256:03ac78767400c1d1b9c984acca6bd90df72cac0fb00e9100b2c5a8ee2438346e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15278999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1375e7d3522dd5c1a611790297f685c2fe0704944053af8e43e7d8a89930cc3`

```dockerfile
```

-	Layers:
	-	`sha256:f28e04508e5f7206d96f053f77275ef0c0bb7fa9f8a03c918a24d3fb10588e28`  
		Last Modified: Fri, 27 Sep 2024 17:40:44 GMT  
		Size: 15.3 MB (15266033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1a546a507332436c927687563a98866a316dbc8fab3ac46845bfa34cbe62b1`  
		Last Modified: Fri, 27 Sep 2024 17:40:43 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81-alpine`

```console
$ docker pull rust@sha256:d6e876ca5fe200f4ac60312b95606f0b042699c4cf6a19493b7d2a2ebbfb337b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.81-alpine` - linux; amd64

```console
$ docker pull rust@sha256:03b96a6b633cc6d3d1168e1afa2357ba5ccce128da909ba3b57487f0cc228428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283243467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c2a31537b2eac7656edddd62805b51abda9efb6f3761a92363fd35bac462ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7a6c0b92f840b647ad3fdd4fc8c1739f833da486d7e51793f4c1ebe411333`  
		Last Modified: Fri, 06 Sep 2024 23:25:12 GMT  
		Size: 55.3 MB (55309249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d299bec348b12e4baacefd5ece1f43bfb77ef3abe2e52f56ad4d5e67c263b056`  
		Last Modified: Fri, 06 Sep 2024 23:25:20 GMT  
		Size: 224.3 MB (224310411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:1d57ee624f00a8ce856aa31ba4730a87c91d9a11b9fd595f3d385f5bb44ece20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6497981077302a8c905b5e4e2dfffd9ac14137a0cfc7497d4dcafc806053e7`

```dockerfile
```

-	Layers:
	-	`sha256:da26bdf9689b6139ac3ee467c818e036ca25e103dae29ddb9f158f48efec517d`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2530f84e604ec82ab6979568cbfe879a3721c0a3adea3f06fb87cda5819f968e`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 11.7 KB (11678 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d577dfa9ebb3576ed0824cd4a6665ce2a1a37b908bf767ed0f96c10360f19e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291454748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193dfcd4e8418a0b3ab51d24dd2601d67cb5f6f7446bdcf55c7fc139421a0836`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dae75a7979f5c823e78faad77f0683f4120db209a14f80f65d35ffcfb6465c`  
		Last Modified: Sat, 07 Sep 2024 11:56:50 GMT  
		Size: 52.9 MB (52946235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d0ba6d79ddcc7adb2e073c295844423f77032e7b03bc7973c24f60d3d5ae3`  
		Last Modified: Sat, 07 Sep 2024 11:56:54 GMT  
		Size: 234.4 MB (234420867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:09413672bd07b597f07a8cc58f505f88e517959490527c39693b43a71c238377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f7960713521b5f6f4f75e0f419a67822c4ca3ac34eedb0753910785c0c3881`

```dockerfile
```

-	Layers:
	-	`sha256:b85be6b172df08e0e211efd0e6354594a97df69970d84ea800b01169be9286f4`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486ea238c8b03b69cfc3df4c2c5336edce93eb2ae87385c5b1b31951f59bdef2`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81-alpine3.19`

```console
$ docker pull rust@sha256:5b6bdc02ef966d208c7edc309d3cdf75725b3a0fe6535f4460f9d2d7fb88322b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.81-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:c45cc04288af707001a7a90382d16dc29309508b0d274a4c61282bad7ecd8345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283076960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e2a973eb4a9819fb599046858b1ccd486ae9157ed0d695bb65d7016cb83135`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b596d4da02c982671dbf6bed836470acee3a2fadc6863ba9e1cce5e388c93ab`  
		Last Modified: Fri, 06 Sep 2024 23:24:43 GMT  
		Size: 55.3 MB (55346883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872d9e0d3eae5459c9159c8cc624a3c35789017552614cda7063b19930cfda94`  
		Last Modified: Fri, 06 Sep 2024 23:24:47 GMT  
		Size: 224.3 MB (224310371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:e32690943c1038ed26065af835abea2eb061b1715bfd4330fe65d48ec1198103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdc2c73e311f0afde5234e3a30984507a7113be703884269be015f6a435cf5d`

```dockerfile
```

-	Layers:
	-	`sha256:612b4526cbae481700ab36cb68a6c9c0af9f27506d9f7dbe6867e3fb2e9a3ddd`  
		Last Modified: Fri, 06 Sep 2024 23:24:42 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e67ae8c135e6a6076ec3f5355c54c343cef04d8f379ed48c426f2dd6ba2622c9`  
		Last Modified: Fri, 06 Sep 2024 23:24:42 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2ad5d810439717463a3ad522bfe9c626490ca35176488b753a9e57d23f35d9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290775337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e25ee6035525a540920de98ffd4b96c964d2195252fb1dc32743828b84b0b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74da714a92090eec171b9fdcc6c89c6591ba432fdeeaa10d5c10538ede56c8a`  
		Last Modified: Sat, 07 Sep 2024 11:55:42 GMT  
		Size: 53.0 MB (52995429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b56e9f588d67bf61a8465ec612c0b1095ef03b2d5afe03498b7ad4fed2fd38f`  
		Last Modified: Sat, 07 Sep 2024 11:55:47 GMT  
		Size: 234.4 MB (234420805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:f9446358434100ac647f0d3dd9a0e1b2005a6f8910ede685cdc2e9e9c2ec5eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644500100d93dbb3715254eb9f6a6028976c644a3ea440840fa3de87e015593a`

```dockerfile
```

-	Layers:
	-	`sha256:5318473dfb1acaa5a3766971ec81932624e4e3e24520ff1226b8de3a4d1eabbc`  
		Last Modified: Sat, 07 Sep 2024 11:55:41 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5f4a984e365a0132171af9a5448f3da92750593f5660cb7358ca62cbe7b3b30`  
		Last Modified: Sat, 07 Sep 2024 11:55:40 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81-alpine3.20`

```console
$ docker pull rust@sha256:d6e876ca5fe200f4ac60312b95606f0b042699c4cf6a19493b7d2a2ebbfb337b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.81-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:03b96a6b633cc6d3d1168e1afa2357ba5ccce128da909ba3b57487f0cc228428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283243467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c2a31537b2eac7656edddd62805b51abda9efb6f3761a92363fd35bac462ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7a6c0b92f840b647ad3fdd4fc8c1739f833da486d7e51793f4c1ebe411333`  
		Last Modified: Fri, 06 Sep 2024 23:25:12 GMT  
		Size: 55.3 MB (55309249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d299bec348b12e4baacefd5ece1f43bfb77ef3abe2e52f56ad4d5e67c263b056`  
		Last Modified: Fri, 06 Sep 2024 23:25:20 GMT  
		Size: 224.3 MB (224310411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1d57ee624f00a8ce856aa31ba4730a87c91d9a11b9fd595f3d385f5bb44ece20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6497981077302a8c905b5e4e2dfffd9ac14137a0cfc7497d4dcafc806053e7`

```dockerfile
```

-	Layers:
	-	`sha256:da26bdf9689b6139ac3ee467c818e036ca25e103dae29ddb9f158f48efec517d`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2530f84e604ec82ab6979568cbfe879a3721c0a3adea3f06fb87cda5819f968e`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 11.7 KB (11678 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d577dfa9ebb3576ed0824cd4a6665ce2a1a37b908bf767ed0f96c10360f19e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291454748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193dfcd4e8418a0b3ab51d24dd2601d67cb5f6f7446bdcf55c7fc139421a0836`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dae75a7979f5c823e78faad77f0683f4120db209a14f80f65d35ffcfb6465c`  
		Last Modified: Sat, 07 Sep 2024 11:56:50 GMT  
		Size: 52.9 MB (52946235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d0ba6d79ddcc7adb2e073c295844423f77032e7b03bc7973c24f60d3d5ae3`  
		Last Modified: Sat, 07 Sep 2024 11:56:54 GMT  
		Size: 234.4 MB (234420867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:09413672bd07b597f07a8cc58f505f88e517959490527c39693b43a71c238377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f7960713521b5f6f4f75e0f419a67822c4ca3ac34eedb0753910785c0c3881`

```dockerfile
```

-	Layers:
	-	`sha256:b85be6b172df08e0e211efd0e6354594a97df69970d84ea800b01169be9286f4`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486ea238c8b03b69cfc3df4c2c5336edce93eb2ae87385c5b1b31951f59bdef2`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81-bookworm`

```console
$ docker pull rust@sha256:0757ed8c0609498399dfde17ad6e5ac4adc5da04096fbd3d9c2301c62b93546b
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

### `rust:1.81-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:62afc139057dc9d3eda02e490677911b55a208ba22d6f7315f3c5c5851e31a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533623479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3b0145b0fabfa9f7bfc382e163449775329c6b95cb5704237a770a9e6e52a1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba0b3d08b81baa192d30dbb2257b8227f2a4eab719c79ef1c419e3a07b39dbc`  
		Last Modified: Thu, 17 Oct 2024 01:10:04 GMT  
		Size: 64.4 MB (64393080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bc85537ac7c401eea9ed38d4a75fddbe5d75d5570921f1c435a8342b3cef15`  
		Last Modified: Thu, 17 Oct 2024 01:10:40 GMT  
		Size: 211.3 MB (211281151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97b348fbebca67b25f027e550f95573ba6aff2f81f748dbf3e11e96d7fc6da6`  
		Last Modified: Thu, 17 Oct 2024 02:57:32 GMT  
		Size: 184.3 MB (184341137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:afd613e0c8388610680d95743ce6b0519e2e288ab2180009d03fdee5263cf66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ce36b1a51263afe43943de85c9d45999d4fd4b9197ac8e48278804e18c1582`

```dockerfile
```

-	Layers:
	-	`sha256:7b956ebc4fdf5bc354458d55f06403a6a7feff6dbe43975c601c444a5d70edc5`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde1eebb12461b3cf18799768782571274684aa61647d4c0e77a0b7d51d3c40`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 13.0 KB (13004 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:27b6e9bd919166bac1fb9211e9e52449d5fb725a70122e2280b3f235eef01f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.5 MB (523464584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd1ab1a770c8f7aa48d8b41c6152318ce574fb409b4620f8fea171c3ba763c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea668db82ddd31e7300e905d69bfbcc24fd0c70cd7c7212c915763a9e47f3e7`  
		Last Modified: Fri, 27 Sep 2024 07:39:33 GMT  
		Size: 175.2 MB (175207938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807abecaed8d4cffae0b7d1da027197029821fd16d2bbce8c0f8a1f90fd349f3`  
		Last Modified: Sat, 28 Sep 2024 04:08:11 GMT  
		Size: 221.5 MB (221511519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ee2cbc5b0aa8369395392c722b55ad9ac0bd4916118b0cdf63d4d0f13269a299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15270591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa74c1d6fa4c9dda9c706f2706450a4b81da24d4559310f49de7e46773f9700`

```dockerfile
```

-	Layers:
	-	`sha256:45c0558bf77c60592fcc61666d1d55c2e8062c13eee2815becd8547e5fe62df5`  
		Last Modified: Sat, 28 Sep 2024 04:08:07 GMT  
		Size: 15.3 MB (15257523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab9e3cff7b672ef6b62a3eecbf1b9c661a226d91214cd3d7b68a9fd5b262ff05`  
		Last Modified: Sat, 28 Sep 2024 04:08:06 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f5fbbf475717a8e1fcfda24fc26c60200eb95e19b03291f3e43e60995a4d406e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.7 MB (588709463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d76e87cace62dbdc9c3a6c3fae1623de64a44b8b274d79b8e95bcd89b6f1e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71ace0e8bbdcfcf795b836e24a37a6ed0054100e14d6aa6e5a63f7e162ba729`  
		Last Modified: Fri, 27 Sep 2024 05:25:40 GMT  
		Size: 202.7 MB (202651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c70a9d34bb788145305c907ff9a5ed64690b67c5abbc4b676ff607611081e0`  
		Last Modified: Fri, 27 Sep 2024 23:30:32 GMT  
		Size: 248.5 MB (248529120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:be6c0d1bdd139e794a093f63bbdcf7c53acbacba5babbcf59b54af8fd37f7cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15494574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23350ebe95ee44b5c009236d86e0a9d13772ae5689fa9c3449fec0987bd7b81d`

```dockerfile
```

-	Layers:
	-	`sha256:7c227d855755631f9fc25b4280c874ce996590e6446ce7c7399e0c496bd31670`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 15.5 MB (15481248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a10530d2c00a615465f62c3a9b01ff478facbfb4d920cbbf7d0d386c559eb44`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-bookworm` - linux; 386

```console
$ docker pull rust@sha256:cae43437babe4a513bfaf1ebaed7b47e916e1a96bea4496ee763708f2a2b5bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549225958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af64455d7089be15c70fda713c93555e12afb877f65a7b29d2b3dddfab02d1f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9dd8137152c295fb3624be3ee13689c34dc13bc115d0032a5a2a581001f14f`  
		Last Modified: Thu, 17 Oct 2024 01:09:36 GMT  
		Size: 24.9 MB (24895435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbad5c607546fed7ceeb86b3cef161781f7cb90e39cb2c8da1b7774aa73975d4`  
		Last Modified: Thu, 17 Oct 2024 01:09:58 GMT  
		Size: 66.2 MB (66210908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c0ef7e16c4ea3f5643d06ea746c15f35cca787121e7078904f6a16114c48`  
		Last Modified: Thu, 17 Oct 2024 01:10:44 GMT  
		Size: 210.2 MB (210196330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f818dcff8930802b82fed8fbd3b89feef62a7b69bc64cebb8df64281a6dd9`  
		Last Modified: Thu, 17 Oct 2024 02:57:36 GMT  
		Size: 197.3 MB (197346451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bc528a75faa20afa57e2c7e4b6f51d9b57b5485d2d379eea44c3bf52d6fbd4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808162f63c550251d4aaa7a5eee4f171d732b78e387b1137976a4a926ec4476c`

```dockerfile
```

-	Layers:
	-	`sha256:cecf68aacf4ab8230e1cd8e54fe8e2c4fe0ecb15f64b69df35db646913b7bdd2`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73cb9933a9869db1cc6fb4636124d96cbfd43111b4b05b820c4e12217bc5b56`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:4d19fbcc0f0bb56e4a6b711398e5de3a634385319d0e8b2bbc0171c109260070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.1 MB (606115637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3374c6411cbaed1bfb06437a6e1edc6a41bd7b83e37ca5ecc6a1aaec09413300`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e2f2830e2003232ca51768518e8eb9e372430ea0c0445d3ec3c8d96672cb8c`  
		Last Modified: Fri, 27 Sep 2024 06:05:25 GMT  
		Size: 214.3 MB (214285718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83748e1ac06a3fcddae1dc3110de6342c4531f82f43779a5fabf89719505db6a`  
		Last Modified: Sat, 28 Sep 2024 05:54:49 GMT  
		Size: 242.7 MB (242735060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:606824019a2d5065cd43eaea75ffe3725a698dd0f28a75d3e050d7cccc157b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15440370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa45a38a900b92dbf585c0410238a0e5b5c4b9b926802c9c7acad6c298aeda8f`

```dockerfile
```

-	Layers:
	-	`sha256:9ab533a7bde3dae7d525cc723b7c2e2eeb5504de5e82bb10f2a6051c078f243c`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 15.4 MB (15427343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c830e1f96c43a12bb0b2d3f79e8307d9635fb3e3532b2762ab339dff8d8738fd`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 13.0 KB (13027 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:0d9fc54c3ca5405db6f5892b2d90b374c38cab322301c88c164cb3d632dcacbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587261517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe66d1e8a70bea815ee500895b94596821696d893861c02b693a4f83ae31166c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1411196315040fbdc5fb36f5519fcdf47619046fa9476d4e7607333bcbd8131`  
		Last Modified: Fri, 27 Sep 2024 03:21:02 GMT  
		Size: 183.3 MB (183287662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35ddee15ec8c9e03e7f842b910c8fd17fe9bfef5ca8c21b7f32fbff8bbcc496`  
		Last Modified: Fri, 27 Sep 2024 17:40:49 GMT  
		Size: 268.5 MB (268487969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:03ac78767400c1d1b9c984acca6bd90df72cac0fb00e9100b2c5a8ee2438346e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15278999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1375e7d3522dd5c1a611790297f685c2fe0704944053af8e43e7d8a89930cc3`

```dockerfile
```

-	Layers:
	-	`sha256:f28e04508e5f7206d96f053f77275ef0c0bb7fa9f8a03c918a24d3fb10588e28`  
		Last Modified: Fri, 27 Sep 2024 17:40:44 GMT  
		Size: 15.3 MB (15266033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1a546a507332436c927687563a98866a316dbc8fab3ac46845bfa34cbe62b1`  
		Last Modified: Fri, 27 Sep 2024 17:40:43 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81-bullseye`

```console
$ docker pull rust@sha256:8328d21407009f8a2d17b0327f32c63411a8c3d5590b71ab87ea993cd2ffd169
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

### `rust:1.81-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:c0c156a4887bdbf6abea8f98258d9d27cfe4c3f2794f674dfb6f5d237de67687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.0 MB (506995658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f511550e16ed987835311ad1d9c0da1b2b1d597b933aed15e44eb452187f9a9b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06817e07ed0f03c17ad0a7aa8ef22b2a6fcf2b939d6212ab0861571ef18a45b`  
		Last Modified: Thu, 17 Oct 2024 01:10:51 GMT  
		Size: 15.8 MB (15764889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173ffc78585eeabe33105e00a7be99b0cad17d5e6edebf7f760d7824fa76969`  
		Last Modified: Thu, 17 Oct 2024 01:11:06 GMT  
		Size: 54.7 MB (54723650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe335f0e34a87e4cbd05c121253490f0c293f8ff29540aa8cd3fc22d4519931`  
		Last Modified: Thu, 17 Oct 2024 01:11:36 GMT  
		Size: 197.1 MB (197085334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66586d4b6a786f40aa4eede68f290dbb5be4152d931746d9bbb17b4b085fcf7`  
		Last Modified: Thu, 17 Oct 2024 02:57:35 GMT  
		Size: 184.3 MB (184341174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7db843194e10c40a284a5f8742a0e692118d3bd1809aa01d16105ab7ec0823ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15063552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c6e3fd4ce8ce97591522bfaf2a495aa59ca89437e220dc586da3fde58d8f0e`

```dockerfile
```

-	Layers:
	-	`sha256:3e0db2ae8efc7a4b906bc15ffdce2bbda5f1c7cbea6015ea958b7c95523d700f`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 15.1 MB (15052438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2033b7ff7e29ef72ea44cc8fe20a94267d7ca6eaded58686e78d093bb6c8ed7f`  
		Last Modified: Thu, 17 Oct 2024 02:57:30 GMT  
		Size: 11.1 KB (11114 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:84331046d2e6bbfe4845d2ef8384cc8281fcbcf0e28fd1071709a3aa34eab212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.8 MB (504758766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d19257130fa88be44790843793cd4e706a1b61733f0e90388b767119ffb2bb`
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
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec523352a6e63a855ebebdbc8288b9cccf719fe4121211d5e0cae3f11e4f6b2`  
		Last Modified: Fri, 27 Sep 2024 07:39:46 GMT  
		Size: 14.9 MB (14879678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bfb8add2d4bda22b21df2a3eff38a6f4f66c2ef9fe110e7714a93f720a4f47`  
		Last Modified: Fri, 27 Sep 2024 07:40:06 GMT  
		Size: 50.6 MB (50618560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f69bcefdc97cf5fabaf3b01d416ce54278fa217058c4433beb68d39a6e1bc1`  
		Last Modified: Fri, 27 Sep 2024 07:40:47 GMT  
		Size: 167.5 MB (167508654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc16697bf56cf2fe7d356c600c48e8a13b2fb6f003a40aec403b77bf1e5a1777`  
		Last Modified: Mon, 07 Oct 2024 20:10:32 GMT  
		Size: 221.5 MB (221511494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3c9b6060fce57e62fb04164d07286dabb9431d2eb979eb665cf468a807fbe9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14864469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873edee47bb20240914debd5c61b9dd61ca27e7d1d73fc95f7657eb67d1419a4`

```dockerfile
```

-	Layers:
	-	`sha256:9e1a11645f7ce0d9026d44c1007e1f6ba2b3f0765e25fa435075743651016034`  
		Last Modified: Mon, 07 Oct 2024 20:10:28 GMT  
		Size: 14.9 MB (14853318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c5c9edc1a5a4d7481d377fa24e5662235f1ce8b366e78cd64a8bc412ee69cb7`  
		Last Modified: Mon, 07 Oct 2024 20:10:27 GMT  
		Size: 11.2 KB (11151 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:230f0887e9953ba599f30462d1601b3af95d1136cf8c1057b77533f0ea13993d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.8 MB (562811378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7fd17cd619497e8cf227bc8f6b6be5a4ceaf9020f09b88694555ccf79d7f65`
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
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4bba36b8add5e5ec5da6aa2c18637b64bce2d5f3f7d83723817e2139a11bcc`  
		Last Modified: Fri, 27 Sep 2024 05:25:50 GMT  
		Size: 15.7 MB (15749698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f212bcfdd3a473cde2991df3e1cf5373d8f097a630557a35fa77d891acce93d6`  
		Last Modified: Fri, 27 Sep 2024 05:26:04 GMT  
		Size: 54.8 MB (54834694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09310330a122777457e6d6b3094e1d1391aa246ba1b028adeb03cd353d0d29`  
		Last Modified: Fri, 27 Sep 2024 05:26:28 GMT  
		Size: 190.0 MB (189964252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da761adc8113e8e908061d91c6af387f04a41e668d2f111540d11a9ef01e5f0`  
		Last Modified: Mon, 07 Oct 2024 20:28:00 GMT  
		Size: 248.5 MB (248528870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f7218307ed60ee81340e8a569d237e241c8e97cac632dc78555ab6083d40909e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15065824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fecd41b23cc4f020e9f319dbf75f1613baa97e283f738646f4a549d49a0a29`

```dockerfile
```

-	Layers:
	-	`sha256:fecaccd039897250aae8a94b1523d4955c0726ff860d9f3a605565fd7b63d201`  
		Last Modified: Mon, 07 Oct 2024 20:27:55 GMT  
		Size: 15.1 MB (15054645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:357925a5449c30f481550c08a6e83d080b7faa1982dfdb43af76649057e41280`  
		Last Modified: Mon, 07 Oct 2024 20:27:54 GMT  
		Size: 11.2 KB (11179 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-bullseye` - linux; 386

```console
$ docker pull rust@sha256:0b74763c0c9110dc9342754e733f284101a3090b083abd7c9eb73f9e9162fee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.7 MB (525706874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01cf6a6c0b6626ce6748e3de2ff0182d8febe57f7c55eac503d91d6f9a3e1c7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000ce4e381f50a8f76ae5a1d4bcd9702f5146bac4fb30afc4e12c284ee68ca9`  
		Last Modified: Thu, 17 Oct 2024 01:10:55 GMT  
		Size: 16.3 MB (16268542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d0b1f51e6e34773cde9f3b41201942ff88384d907912b25ff3349f296f69b8`  
		Last Modified: Thu, 17 Oct 2024 01:11:14 GMT  
		Size: 56.0 MB (56032019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b257135cb04b7c9d5ceaf0572a0941a80b7eb3f7dd31444289a12b792e314e8`  
		Last Modified: Thu, 17 Oct 2024 01:12:01 GMT  
		Size: 200.0 MB (199982090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3420ca7067654974fc0f1971890285287aef101e8c0ad81c1d01689969ded4ec`  
		Last Modified: Thu, 17 Oct 2024 02:57:46 GMT  
		Size: 197.3 MB (197346400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f58b08210121da703d98863e10d84097f158a04b4f053e9f579b47a0ecd6819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b309ca17610165025ded60cffba70e585bf2294d8a81fe1ff260572e71d460d`

```dockerfile
```

-	Layers:
	-	`sha256:c660bef212dab636443f1060b4e1e7ca7a48a89cdf8c12a8d6298cf1ed6616f6`  
		Last Modified: Thu, 17 Oct 2024 02:57:42 GMT  
		Size: 15.0 MB (15040975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f6ca99ad4fa67ac8b5d8bd3b23ad2542d63b6634953bb2057d5c3e1a4443b8`  
		Last Modified: Thu, 17 Oct 2024 02:57:42 GMT  
		Size: 11.1 KB (11085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81-slim`

```console
$ docker pull rust@sha256:5f54e4f0f25ffcb8493d73f38cbd7dd5f6b83ca78d6a33224fc326f6d654d16f
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

### `rust:1.81-slim` - linux; amd64

```console
$ docker pull rust@sha256:45966c8f3e8348b7643bd40eb846b87015a6f1694ed2a13ca8475c5be35df8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284254306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b63b5bcc9542ec50795afee904fd719f71dbf5f3cd84e74de4c92f7808a727f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0607d7c68e964f9d197627ffe492db8c9ce40d39951ee73a3182e028b0be4e`  
		Last Modified: Thu, 17 Oct 2024 01:30:10 GMT  
		Size: 255.1 MB (255128017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim` - unknown; unknown

```console
$ docker pull rust@sha256:f17aeca9415c8c8b3eec6d14b5a90f91bbe302ef815e6513d5763f9b1d2b645c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010e722839b0079d58e9aa6bcd3b6446f5bd6702bbfe47fc984b869d24c68e15`

```dockerfile
```

-	Layers:
	-	`sha256:e6e2cf59070156e4177eabcbb570b524e550d23ecba4082cc0876549b6a34458`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78cde42d64af02ec433aba2279aede7b5ce92746174556b598fd74de7abd9517`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 13.1 KB (13090 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:08dbf3d9d24bae232365620c62410ec5d83596ff380aad5f49e27cdec7317513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294070169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e6abf46c4d525890ed87fc173518b54a4bd6a1b01b96fe447fb1d17e08346a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4408bd841243a9a42a8e256c364029c480e1b0b2865b22e70a46bde0100c866`  
		Last Modified: Fri, 27 Sep 2024 18:42:06 GMT  
		Size: 269.4 MB (269352024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim` - unknown; unknown

```console
$ docker pull rust@sha256:df722b016f3cca3b94348d0bc6f597be00e94961777ca5cb428cf4cdd0af6f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e61fad66437481804743201bd550faf73c0e8846ddb64f6d8bf18e0dff7a4a3`

```dockerfile
```

-	Layers:
	-	`sha256:e090a867d43bfae1fb514bbb85985f7c87fff9bd5a411d0ec1cdcf062ed1c5f1`  
		Last Modified: Fri, 27 Sep 2024 18:42:01 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffb56d93014b97c2bf56f856a3b3c0c1c6de63989a9e8fca173c3abc901f156`  
		Last Modified: Fri, 27 Sep 2024 18:42:00 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3ba3fbf62527788a60c4908b3c389bab7f5ab6fb919ea3c771aeb9a278966253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343526226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233c27109e17c04665f9ed9ede09369aacd1865fc09fd1a6f5ac4863e32fc4a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995fd26d021eddb871651f81a432e2662de3c5b719d2248d4552105c40a67e47`  
		Last Modified: Fri, 27 Sep 2024 23:32:02 GMT  
		Size: 314.4 MB (314369857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim` - unknown; unknown

```console
$ docker pull rust@sha256:e4a5a923d2e13d83eb71aa2cb933b273577721a70c5ff55a15af8cd5f4d21978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633019f2483a2e86da7ee1384084a836d087aab2347f626c8490a683b80397fc`

```dockerfile
```

-	Layers:
	-	`sha256:45375e55489ffbdb8bd47dbec3eee1f67a6679081f46e4dc1ac6c76ce18b1904`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f968eae71eae982a4adc164da8a72a293dd418f197ba71ede38a68bb18be6c05`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim` - linux; 386

```console
$ docker pull rust@sha256:ba4ee661bb466ab49f6ceb8c6d9e9f9784bba7c6e45225187cd3c7fb1fbc12ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295093589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e4df283163309e2fdaa8101fa73b670d133162155d4cd23424016dd87db8e4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a718584a1346679f83b1655ad2ac313c29bec26411eeb7c34dad2a91b6577448`  
		Last Modified: Thu, 17 Oct 2024 01:30:07 GMT  
		Size: 264.9 MB (264949322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4c72332e16899bfc022e891c90f0d93e00f555271f92b2e38817f8afa453c722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ca94475147e0318e9bad8ec073ef9dd87fef510c2eed0171a3f48a81c843a`

```dockerfile
```

-	Layers:
	-	`sha256:12434a1e188136de888271297f6eb4670c269905a0833cb0c26866ab817a1eac`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11e3392f42511d72755c775a9cd45fb9f2d612485058889a5a61cbb5dda587f`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 13.0 KB (13043 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:46bcce128e6ab5402c648739e95aa56eb2ed32d840ff42da0975ec8428034ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344618727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4f6cbc6fd8ecc671e77ece602998ab1fa543c11db83d5d64fa6bc051b111c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097a47a9153a9d3d44374a545c87a489f3842a16e291caf5a817ebaa5a0f1552`  
		Last Modified: Sat, 28 Sep 2024 04:15:09 GMT  
		Size: 311.5 MB (311496564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim` - unknown; unknown

```console
$ docker pull rust@sha256:fa335487319e81174f0920ee7efa014f25d5cdbbfdf8648c77cfeb1f771129bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f51b298cbeb650a1f7674e47e0ff5da39045f7a1c1b12678284013db4153e2`

```dockerfile
```

-	Layers:
	-	`sha256:17e6bf4b03c232f13acb280f35f3b04cad777afeab1156732f6d6e80ae08ac03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9673908047a020854098b5704b6ac719a43c3c5263868a007ef95e1dd656fe03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim` - linux; s390x

```console
$ docker pull rust@sha256:1986b817125878c181d9add8424b112238bbcd915e03b3444b6e3b9962a71844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346124228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaf144d0210bf05141bac7875bc21c09171ace17f17693c306e46ee2347cc8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d24393939cc6c4eddc3a49c03d07080edb453591af15f5f40c3481b1c43289`  
		Last Modified: Fri, 27 Sep 2024 17:42:41 GMT  
		Size: 318.6 MB (318634204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim` - unknown; unknown

```console
$ docker pull rust@sha256:981dce7ac4cd7769d68270976ad41a566057debc664228639318ceeee2878c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb7573b7c4578171c99e4b1c475220bae80fd01a2abcc1ff7de0c789cee9993`

```dockerfile
```

-	Layers:
	-	`sha256:165fd9d1067cb2b20bc1127fb26bf62317d9ec727e17d418b73ad480975a460f`  
		Last Modified: Fri, 27 Sep 2024 17:42:37 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03aa2d5f9daee31ee7485507b38e1a42c341c49bd4f504117c96708fe84908d5`  
		Last Modified: Fri, 27 Sep 2024 17:42:36 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81-slim-bookworm`

```console
$ docker pull rust@sha256:5f54e4f0f25ffcb8493d73f38cbd7dd5f6b83ca78d6a33224fc326f6d654d16f
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

### `rust:1.81-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:45966c8f3e8348b7643bd40eb846b87015a6f1694ed2a13ca8475c5be35df8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284254306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b63b5bcc9542ec50795afee904fd719f71dbf5f3cd84e74de4c92f7808a727f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0607d7c68e964f9d197627ffe492db8c9ce40d39951ee73a3182e028b0be4e`  
		Last Modified: Thu, 17 Oct 2024 01:30:10 GMT  
		Size: 255.1 MB (255128017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f17aeca9415c8c8b3eec6d14b5a90f91bbe302ef815e6513d5763f9b1d2b645c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010e722839b0079d58e9aa6bcd3b6446f5bd6702bbfe47fc984b869d24c68e15`

```dockerfile
```

-	Layers:
	-	`sha256:e6e2cf59070156e4177eabcbb570b524e550d23ecba4082cc0876549b6a34458`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78cde42d64af02ec433aba2279aede7b5ce92746174556b598fd74de7abd9517`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 13.1 KB (13090 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:08dbf3d9d24bae232365620c62410ec5d83596ff380aad5f49e27cdec7317513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294070169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e6abf46c4d525890ed87fc173518b54a4bd6a1b01b96fe447fb1d17e08346a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4408bd841243a9a42a8e256c364029c480e1b0b2865b22e70a46bde0100c866`  
		Last Modified: Fri, 27 Sep 2024 18:42:06 GMT  
		Size: 269.4 MB (269352024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:df722b016f3cca3b94348d0bc6f597be00e94961777ca5cb428cf4cdd0af6f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e61fad66437481804743201bd550faf73c0e8846ddb64f6d8bf18e0dff7a4a3`

```dockerfile
```

-	Layers:
	-	`sha256:e090a867d43bfae1fb514bbb85985f7c87fff9bd5a411d0ec1cdcf062ed1c5f1`  
		Last Modified: Fri, 27 Sep 2024 18:42:01 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffb56d93014b97c2bf56f856a3b3c0c1c6de63989a9e8fca173c3abc901f156`  
		Last Modified: Fri, 27 Sep 2024 18:42:00 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3ba3fbf62527788a60c4908b3c389bab7f5ab6fb919ea3c771aeb9a278966253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343526226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233c27109e17c04665f9ed9ede09369aacd1865fc09fd1a6f5ac4863e32fc4a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995fd26d021eddb871651f81a432e2662de3c5b719d2248d4552105c40a67e47`  
		Last Modified: Fri, 27 Sep 2024 23:32:02 GMT  
		Size: 314.4 MB (314369857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e4a5a923d2e13d83eb71aa2cb933b273577721a70c5ff55a15af8cd5f4d21978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633019f2483a2e86da7ee1384084a836d087aab2347f626c8490a683b80397fc`

```dockerfile
```

-	Layers:
	-	`sha256:45375e55489ffbdb8bd47dbec3eee1f67a6679081f46e4dc1ac6c76ce18b1904`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f968eae71eae982a4adc164da8a72a293dd418f197ba71ede38a68bb18be6c05`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:ba4ee661bb466ab49f6ceb8c6d9e9f9784bba7c6e45225187cd3c7fb1fbc12ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295093589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e4df283163309e2fdaa8101fa73b670d133162155d4cd23424016dd87db8e4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a718584a1346679f83b1655ad2ac313c29bec26411eeb7c34dad2a91b6577448`  
		Last Modified: Thu, 17 Oct 2024 01:30:07 GMT  
		Size: 264.9 MB (264949322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4c72332e16899bfc022e891c90f0d93e00f555271f92b2e38817f8afa453c722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ca94475147e0318e9bad8ec073ef9dd87fef510c2eed0171a3f48a81c843a`

```dockerfile
```

-	Layers:
	-	`sha256:12434a1e188136de888271297f6eb4670c269905a0833cb0c26866ab817a1eac`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11e3392f42511d72755c775a9cd45fb9f2d612485058889a5a61cbb5dda587f`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 13.0 KB (13043 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:46bcce128e6ab5402c648739e95aa56eb2ed32d840ff42da0975ec8428034ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344618727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4f6cbc6fd8ecc671e77ece602998ab1fa543c11db83d5d64fa6bc051b111c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097a47a9153a9d3d44374a545c87a489f3842a16e291caf5a817ebaa5a0f1552`  
		Last Modified: Sat, 28 Sep 2024 04:15:09 GMT  
		Size: 311.5 MB (311496564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:fa335487319e81174f0920ee7efa014f25d5cdbbfdf8648c77cfeb1f771129bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f51b298cbeb650a1f7674e47e0ff5da39045f7a1c1b12678284013db4153e2`

```dockerfile
```

-	Layers:
	-	`sha256:17e6bf4b03c232f13acb280f35f3b04cad777afeab1156732f6d6e80ae08ac03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9673908047a020854098b5704b6ac719a43c3c5263868a007ef95e1dd656fe03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:1986b817125878c181d9add8424b112238bbcd915e03b3444b6e3b9962a71844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346124228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaf144d0210bf05141bac7875bc21c09171ace17f17693c306e46ee2347cc8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d24393939cc6c4eddc3a49c03d07080edb453591af15f5f40c3481b1c43289`  
		Last Modified: Fri, 27 Sep 2024 17:42:41 GMT  
		Size: 318.6 MB (318634204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:981dce7ac4cd7769d68270976ad41a566057debc664228639318ceeee2878c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb7573b7c4578171c99e4b1c475220bae80fd01a2abcc1ff7de0c789cee9993`

```dockerfile
```

-	Layers:
	-	`sha256:165fd9d1067cb2b20bc1127fb26bf62317d9ec727e17d418b73ad480975a460f`  
		Last Modified: Fri, 27 Sep 2024 17:42:37 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03aa2d5f9daee31ee7485507b38e1a42c341c49bd4f504117c96708fe84908d5`  
		Last Modified: Fri, 27 Sep 2024 17:42:36 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81-slim-bullseye`

```console
$ docker pull rust@sha256:915a4826b6111266e53e06f47c16cddebf36901623f0631f2cc10ce5c26022e5
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

### `rust:1.81-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:955e6b161e189ce9a70a3176d62bc853df1d45a8ff2c877bcc2639c1334e05da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275916178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72160f9a4acd420abe48f6f6d762750669ca08d8e16c3612f2aa8e48e6886df1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b38e595cdc330fbe56f1cc54e1fbb521c5c78b889fda1cb2553ec996eb7494`  
		Last Modified: Thu, 17 Oct 2024 01:28:56 GMT  
		Size: 244.5 MB (244487378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:913457ace1ef4de84bcd5852f75e36f52b6ec6cb0381db81b057670c1f7a64c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900b212c9018b48677c88ed0905ec79728757d918f45bb4e41c5f9ac0e6c8a10`

```dockerfile
```

-	Layers:
	-	`sha256:8347c9cf5193ed18506b7d4c96a1dd5a0451c1c9d4c0049fd6c1adaaefe4b7cb`  
		Last Modified: Thu, 17 Oct 2024 01:28:53 GMT  
		Size: 4.2 MB (4164416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee600185d29aecb0803b6cd08dc6117b7080dbec62c710fa35ae4dffc674e387`  
		Last Modified: Thu, 17 Oct 2024 01:28:53 GMT  
		Size: 11.2 KB (11176 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:649f33f2004e7cf32279d259133d1c887680c82371ca61040be0676de14478f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290373521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c1dea15d81a85919b55bae459fdf9865c474d6a3eeded3a426c223d45f15fe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:05 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
# Fri, 27 Sep 2024 05:14:07 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0961dc5030bdc38ffd749a496abefd5f5e3c43706db1ac4fbe6a89b425b6f565`  
		Last Modified: Mon, 07 Oct 2024 20:12:29 GMT  
		Size: 263.8 MB (263784209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0fdedd82265ee4abb67e00cb5ed763bb6b00b1e1a9cff139eb943b524eceddc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3984890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4338ea06da0c03a6090e3a6d0cdfbf4558bd2939605e26dcb73de43f3ae2445a`

```dockerfile
```

-	Layers:
	-	`sha256:ba5dd9365cb77053e5b690af6fb2194be4ea48e4cf45c38343e7917bf11ac2d6`  
		Last Modified: Mon, 07 Oct 2024 20:12:23 GMT  
		Size: 4.0 MB (3973677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71bcc530464af98ed85ff675234211982092c53f113700732ff05ba7b7063828`  
		Last Modified: Mon, 07 Oct 2024 20:12:22 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5a6a01ab245dd0f9c1c5289854e6bfbf41eda63717a403c2ec5715751e29df3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334323993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53157f2dc99d3da88944463c603f1435f567f3e51e835146526d5ddc3602023e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a5b36cf8f1de6f21df811fbf5e9fc34a4a885fdb4d55f5d99d5d38e9e10aa1`  
		Last Modified: Mon, 07 Oct 2024 20:29:36 GMT  
		Size: 304.2 MB (304248835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:117078f67d65fb1fb6692b2e819225b0028efe02b38e50d365a11fb8218ade4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4172348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7528c856c92358d9c7cab5571c3f927091bf38d06d14ae6832f0cdb6a0ea1f`

```dockerfile
```

-	Layers:
	-	`sha256:e585026bbab5521b31de85e6d76a91d424b33a11f16dfc4c480cb11110170e68`  
		Last Modified: Mon, 07 Oct 2024 20:29:28 GMT  
		Size: 4.2 MB (4161108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:115eecb4972db015834bb7865e3b2013bcb5784751739299b04ee1938b1efb82`  
		Last Modified: Mon, 07 Oct 2024 20:29:28 GMT  
		Size: 11.2 KB (11240 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b869a05737d767ce7fb7056cf77751bb5a8b8b577dfbc911a05c94b2d3754822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290535137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a880359cc690264cb0b553f18917849f5c945bc7ff9fea96ceea4696a15d345f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabfbb638063d13147d4f9a1a5694685c92adb5cf15ae94665eae2cd245e5f7a`  
		Last Modified: Thu, 17 Oct 2024 01:29:49 GMT  
		Size: 258.1 MB (258121307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e7bc0dd978b6918b697d54b2322bd89a8fc2364017dc1354c01927066ba886ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c222bd0ec93f4d3719cfa3e3ebd12b938ba155acbede32405b0b9551d71c0e27`

```dockerfile
```

-	Layers:
	-	`sha256:58a6810008287c12bb6320144c20f384550200c86b54ba7c87a2e079a24c5263`  
		Last Modified: Thu, 17 Oct 2024 01:29:43 GMT  
		Size: 4.2 MB (4156184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08b166a715fea1c9ef90fcc577433cc2762aea86d09168615d781dd8d5e38012`  
		Last Modified: Thu, 17 Oct 2024 01:29:43 GMT  
		Size: 11.1 KB (11146 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81.0`

```console
$ docker pull rust@sha256:0757ed8c0609498399dfde17ad6e5ac4adc5da04096fbd3d9c2301c62b93546b
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

### `rust:1.81.0` - linux; amd64

```console
$ docker pull rust@sha256:62afc139057dc9d3eda02e490677911b55a208ba22d6f7315f3c5c5851e31a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533623479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3b0145b0fabfa9f7bfc382e163449775329c6b95cb5704237a770a9e6e52a1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba0b3d08b81baa192d30dbb2257b8227f2a4eab719c79ef1c419e3a07b39dbc`  
		Last Modified: Thu, 17 Oct 2024 01:10:04 GMT  
		Size: 64.4 MB (64393080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bc85537ac7c401eea9ed38d4a75fddbe5d75d5570921f1c435a8342b3cef15`  
		Last Modified: Thu, 17 Oct 2024 01:10:40 GMT  
		Size: 211.3 MB (211281151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97b348fbebca67b25f027e550f95573ba6aff2f81f748dbf3e11e96d7fc6da6`  
		Last Modified: Thu, 17 Oct 2024 02:57:32 GMT  
		Size: 184.3 MB (184341137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0` - unknown; unknown

```console
$ docker pull rust@sha256:afd613e0c8388610680d95743ce6b0519e2e288ab2180009d03fdee5263cf66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ce36b1a51263afe43943de85c9d45999d4fd4b9197ac8e48278804e18c1582`

```dockerfile
```

-	Layers:
	-	`sha256:7b956ebc4fdf5bc354458d55f06403a6a7feff6dbe43975c601c444a5d70edc5`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde1eebb12461b3cf18799768782571274684aa61647d4c0e77a0b7d51d3c40`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 13.0 KB (13004 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0` - linux; arm variant v7

```console
$ docker pull rust@sha256:27b6e9bd919166bac1fb9211e9e52449d5fb725a70122e2280b3f235eef01f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.5 MB (523464584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd1ab1a770c8f7aa48d8b41c6152318ce574fb409b4620f8fea171c3ba763c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea668db82ddd31e7300e905d69bfbcc24fd0c70cd7c7212c915763a9e47f3e7`  
		Last Modified: Fri, 27 Sep 2024 07:39:33 GMT  
		Size: 175.2 MB (175207938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807abecaed8d4cffae0b7d1da027197029821fd16d2bbce8c0f8a1f90fd349f3`  
		Last Modified: Sat, 28 Sep 2024 04:08:11 GMT  
		Size: 221.5 MB (221511519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0` - unknown; unknown

```console
$ docker pull rust@sha256:ee2cbc5b0aa8369395392c722b55ad9ac0bd4916118b0cdf63d4d0f13269a299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15270591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa74c1d6fa4c9dda9c706f2706450a4b81da24d4559310f49de7e46773f9700`

```dockerfile
```

-	Layers:
	-	`sha256:45c0558bf77c60592fcc61666d1d55c2e8062c13eee2815becd8547e5fe62df5`  
		Last Modified: Sat, 28 Sep 2024 04:08:07 GMT  
		Size: 15.3 MB (15257523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab9e3cff7b672ef6b62a3eecbf1b9c661a226d91214cd3d7b68a9fd5b262ff05`  
		Last Modified: Sat, 28 Sep 2024 04:08:06 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f5fbbf475717a8e1fcfda24fc26c60200eb95e19b03291f3e43e60995a4d406e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.7 MB (588709463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d76e87cace62dbdc9c3a6c3fae1623de64a44b8b274d79b8e95bcd89b6f1e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71ace0e8bbdcfcf795b836e24a37a6ed0054100e14d6aa6e5a63f7e162ba729`  
		Last Modified: Fri, 27 Sep 2024 05:25:40 GMT  
		Size: 202.7 MB (202651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c70a9d34bb788145305c907ff9a5ed64690b67c5abbc4b676ff607611081e0`  
		Last Modified: Fri, 27 Sep 2024 23:30:32 GMT  
		Size: 248.5 MB (248529120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0` - unknown; unknown

```console
$ docker pull rust@sha256:be6c0d1bdd139e794a093f63bbdcf7c53acbacba5babbcf59b54af8fd37f7cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15494574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23350ebe95ee44b5c009236d86e0a9d13772ae5689fa9c3449fec0987bd7b81d`

```dockerfile
```

-	Layers:
	-	`sha256:7c227d855755631f9fc25b4280c874ce996590e6446ce7c7399e0c496bd31670`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 15.5 MB (15481248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a10530d2c00a615465f62c3a9b01ff478facbfb4d920cbbf7d0d386c559eb44`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0` - linux; 386

```console
$ docker pull rust@sha256:cae43437babe4a513bfaf1ebaed7b47e916e1a96bea4496ee763708f2a2b5bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549225958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af64455d7089be15c70fda713c93555e12afb877f65a7b29d2b3dddfab02d1f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9dd8137152c295fb3624be3ee13689c34dc13bc115d0032a5a2a581001f14f`  
		Last Modified: Thu, 17 Oct 2024 01:09:36 GMT  
		Size: 24.9 MB (24895435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbad5c607546fed7ceeb86b3cef161781f7cb90e39cb2c8da1b7774aa73975d4`  
		Last Modified: Thu, 17 Oct 2024 01:09:58 GMT  
		Size: 66.2 MB (66210908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c0ef7e16c4ea3f5643d06ea746c15f35cca787121e7078904f6a16114c48`  
		Last Modified: Thu, 17 Oct 2024 01:10:44 GMT  
		Size: 210.2 MB (210196330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f818dcff8930802b82fed8fbd3b89feef62a7b69bc64cebb8df64281a6dd9`  
		Last Modified: Thu, 17 Oct 2024 02:57:36 GMT  
		Size: 197.3 MB (197346451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0` - unknown; unknown

```console
$ docker pull rust@sha256:bc528a75faa20afa57e2c7e4b6f51d9b57b5485d2d379eea44c3bf52d6fbd4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808162f63c550251d4aaa7a5eee4f171d732b78e387b1137976a4a926ec4476c`

```dockerfile
```

-	Layers:
	-	`sha256:cecf68aacf4ab8230e1cd8e54fe8e2c4fe0ecb15f64b69df35db646913b7bdd2`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73cb9933a9869db1cc6fb4636124d96cbfd43111b4b05b820c4e12217bc5b56`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0` - linux; ppc64le

```console
$ docker pull rust@sha256:4d19fbcc0f0bb56e4a6b711398e5de3a634385319d0e8b2bbc0171c109260070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.1 MB (606115637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3374c6411cbaed1bfb06437a6e1edc6a41bd7b83e37ca5ecc6a1aaec09413300`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e2f2830e2003232ca51768518e8eb9e372430ea0c0445d3ec3c8d96672cb8c`  
		Last Modified: Fri, 27 Sep 2024 06:05:25 GMT  
		Size: 214.3 MB (214285718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83748e1ac06a3fcddae1dc3110de6342c4531f82f43779a5fabf89719505db6a`  
		Last Modified: Sat, 28 Sep 2024 05:54:49 GMT  
		Size: 242.7 MB (242735060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0` - unknown; unknown

```console
$ docker pull rust@sha256:606824019a2d5065cd43eaea75ffe3725a698dd0f28a75d3e050d7cccc157b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15440370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa45a38a900b92dbf585c0410238a0e5b5c4b9b926802c9c7acad6c298aeda8f`

```dockerfile
```

-	Layers:
	-	`sha256:9ab533a7bde3dae7d525cc723b7c2e2eeb5504de5e82bb10f2a6051c078f243c`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 15.4 MB (15427343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c830e1f96c43a12bb0b2d3f79e8307d9635fb3e3532b2762ab339dff8d8738fd`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 13.0 KB (13027 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0` - linux; s390x

```console
$ docker pull rust@sha256:0d9fc54c3ca5405db6f5892b2d90b374c38cab322301c88c164cb3d632dcacbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587261517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe66d1e8a70bea815ee500895b94596821696d893861c02b693a4f83ae31166c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1411196315040fbdc5fb36f5519fcdf47619046fa9476d4e7607333bcbd8131`  
		Last Modified: Fri, 27 Sep 2024 03:21:02 GMT  
		Size: 183.3 MB (183287662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35ddee15ec8c9e03e7f842b910c8fd17fe9bfef5ca8c21b7f32fbff8bbcc496`  
		Last Modified: Fri, 27 Sep 2024 17:40:49 GMT  
		Size: 268.5 MB (268487969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0` - unknown; unknown

```console
$ docker pull rust@sha256:03ac78767400c1d1b9c984acca6bd90df72cac0fb00e9100b2c5a8ee2438346e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15278999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1375e7d3522dd5c1a611790297f685c2fe0704944053af8e43e7d8a89930cc3`

```dockerfile
```

-	Layers:
	-	`sha256:f28e04508e5f7206d96f053f77275ef0c0bb7fa9f8a03c918a24d3fb10588e28`  
		Last Modified: Fri, 27 Sep 2024 17:40:44 GMT  
		Size: 15.3 MB (15266033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1a546a507332436c927687563a98866a316dbc8fab3ac46845bfa34cbe62b1`  
		Last Modified: Fri, 27 Sep 2024 17:40:43 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81.0-alpine`

```console
$ docker pull rust@sha256:d6e876ca5fe200f4ac60312b95606f0b042699c4cf6a19493b7d2a2ebbfb337b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.81.0-alpine` - linux; amd64

```console
$ docker pull rust@sha256:03b96a6b633cc6d3d1168e1afa2357ba5ccce128da909ba3b57487f0cc228428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283243467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c2a31537b2eac7656edddd62805b51abda9efb6f3761a92363fd35bac462ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7a6c0b92f840b647ad3fdd4fc8c1739f833da486d7e51793f4c1ebe411333`  
		Last Modified: Fri, 06 Sep 2024 23:25:12 GMT  
		Size: 55.3 MB (55309249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d299bec348b12e4baacefd5ece1f43bfb77ef3abe2e52f56ad4d5e67c263b056`  
		Last Modified: Fri, 06 Sep 2024 23:25:20 GMT  
		Size: 224.3 MB (224310411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:1d57ee624f00a8ce856aa31ba4730a87c91d9a11b9fd595f3d385f5bb44ece20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6497981077302a8c905b5e4e2dfffd9ac14137a0cfc7497d4dcafc806053e7`

```dockerfile
```

-	Layers:
	-	`sha256:da26bdf9689b6139ac3ee467c818e036ca25e103dae29ddb9f158f48efec517d`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2530f84e604ec82ab6979568cbfe879a3721c0a3adea3f06fb87cda5819f968e`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 11.7 KB (11678 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d577dfa9ebb3576ed0824cd4a6665ce2a1a37b908bf767ed0f96c10360f19e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291454748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193dfcd4e8418a0b3ab51d24dd2601d67cb5f6f7446bdcf55c7fc139421a0836`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dae75a7979f5c823e78faad77f0683f4120db209a14f80f65d35ffcfb6465c`  
		Last Modified: Sat, 07 Sep 2024 11:56:50 GMT  
		Size: 52.9 MB (52946235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d0ba6d79ddcc7adb2e073c295844423f77032e7b03bc7973c24f60d3d5ae3`  
		Last Modified: Sat, 07 Sep 2024 11:56:54 GMT  
		Size: 234.4 MB (234420867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:09413672bd07b597f07a8cc58f505f88e517959490527c39693b43a71c238377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f7960713521b5f6f4f75e0f419a67822c4ca3ac34eedb0753910785c0c3881`

```dockerfile
```

-	Layers:
	-	`sha256:b85be6b172df08e0e211efd0e6354594a97df69970d84ea800b01169be9286f4`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486ea238c8b03b69cfc3df4c2c5336edce93eb2ae87385c5b1b31951f59bdef2`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81.0-alpine3.19`

```console
$ docker pull rust@sha256:5b6bdc02ef966d208c7edc309d3cdf75725b3a0fe6535f4460f9d2d7fb88322b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.81.0-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:c45cc04288af707001a7a90382d16dc29309508b0d274a4c61282bad7ecd8345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283076960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e2a973eb4a9819fb599046858b1ccd486ae9157ed0d695bb65d7016cb83135`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b596d4da02c982671dbf6bed836470acee3a2fadc6863ba9e1cce5e388c93ab`  
		Last Modified: Fri, 06 Sep 2024 23:24:43 GMT  
		Size: 55.3 MB (55346883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872d9e0d3eae5459c9159c8cc624a3c35789017552614cda7063b19930cfda94`  
		Last Modified: Fri, 06 Sep 2024 23:24:47 GMT  
		Size: 224.3 MB (224310371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:e32690943c1038ed26065af835abea2eb061b1715bfd4330fe65d48ec1198103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdc2c73e311f0afde5234e3a30984507a7113be703884269be015f6a435cf5d`

```dockerfile
```

-	Layers:
	-	`sha256:612b4526cbae481700ab36cb68a6c9c0af9f27506d9f7dbe6867e3fb2e9a3ddd`  
		Last Modified: Fri, 06 Sep 2024 23:24:42 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e67ae8c135e6a6076ec3f5355c54c343cef04d8f379ed48c426f2dd6ba2622c9`  
		Last Modified: Fri, 06 Sep 2024 23:24:42 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2ad5d810439717463a3ad522bfe9c626490ca35176488b753a9e57d23f35d9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290775337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e25ee6035525a540920de98ffd4b96c964d2195252fb1dc32743828b84b0b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74da714a92090eec171b9fdcc6c89c6591ba432fdeeaa10d5c10538ede56c8a`  
		Last Modified: Sat, 07 Sep 2024 11:55:42 GMT  
		Size: 53.0 MB (52995429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b56e9f588d67bf61a8465ec612c0b1095ef03b2d5afe03498b7ad4fed2fd38f`  
		Last Modified: Sat, 07 Sep 2024 11:55:47 GMT  
		Size: 234.4 MB (234420805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:f9446358434100ac647f0d3dd9a0e1b2005a6f8910ede685cdc2e9e9c2ec5eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644500100d93dbb3715254eb9f6a6028976c644a3ea440840fa3de87e015593a`

```dockerfile
```

-	Layers:
	-	`sha256:5318473dfb1acaa5a3766971ec81932624e4e3e24520ff1226b8de3a4d1eabbc`  
		Last Modified: Sat, 07 Sep 2024 11:55:41 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5f4a984e365a0132171af9a5448f3da92750593f5660cb7358ca62cbe7b3b30`  
		Last Modified: Sat, 07 Sep 2024 11:55:40 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81.0-alpine3.20`

```console
$ docker pull rust@sha256:d6e876ca5fe200f4ac60312b95606f0b042699c4cf6a19493b7d2a2ebbfb337b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.81.0-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:03b96a6b633cc6d3d1168e1afa2357ba5ccce128da909ba3b57487f0cc228428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283243467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c2a31537b2eac7656edddd62805b51abda9efb6f3761a92363fd35bac462ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7a6c0b92f840b647ad3fdd4fc8c1739f833da486d7e51793f4c1ebe411333`  
		Last Modified: Fri, 06 Sep 2024 23:25:12 GMT  
		Size: 55.3 MB (55309249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d299bec348b12e4baacefd5ece1f43bfb77ef3abe2e52f56ad4d5e67c263b056`  
		Last Modified: Fri, 06 Sep 2024 23:25:20 GMT  
		Size: 224.3 MB (224310411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1d57ee624f00a8ce856aa31ba4730a87c91d9a11b9fd595f3d385f5bb44ece20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6497981077302a8c905b5e4e2dfffd9ac14137a0cfc7497d4dcafc806053e7`

```dockerfile
```

-	Layers:
	-	`sha256:da26bdf9689b6139ac3ee467c818e036ca25e103dae29ddb9f158f48efec517d`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2530f84e604ec82ab6979568cbfe879a3721c0a3adea3f06fb87cda5819f968e`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 11.7 KB (11678 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d577dfa9ebb3576ed0824cd4a6665ce2a1a37b908bf767ed0f96c10360f19e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291454748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193dfcd4e8418a0b3ab51d24dd2601d67cb5f6f7446bdcf55c7fc139421a0836`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dae75a7979f5c823e78faad77f0683f4120db209a14f80f65d35ffcfb6465c`  
		Last Modified: Sat, 07 Sep 2024 11:56:50 GMT  
		Size: 52.9 MB (52946235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d0ba6d79ddcc7adb2e073c295844423f77032e7b03bc7973c24f60d3d5ae3`  
		Last Modified: Sat, 07 Sep 2024 11:56:54 GMT  
		Size: 234.4 MB (234420867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:09413672bd07b597f07a8cc58f505f88e517959490527c39693b43a71c238377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f7960713521b5f6f4f75e0f419a67822c4ca3ac34eedb0753910785c0c3881`

```dockerfile
```

-	Layers:
	-	`sha256:b85be6b172df08e0e211efd0e6354594a97df69970d84ea800b01169be9286f4`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486ea238c8b03b69cfc3df4c2c5336edce93eb2ae87385c5b1b31951f59bdef2`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81.0-bookworm`

```console
$ docker pull rust@sha256:0757ed8c0609498399dfde17ad6e5ac4adc5da04096fbd3d9c2301c62b93546b
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

### `rust:1.81.0-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:62afc139057dc9d3eda02e490677911b55a208ba22d6f7315f3c5c5851e31a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533623479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3b0145b0fabfa9f7bfc382e163449775329c6b95cb5704237a770a9e6e52a1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba0b3d08b81baa192d30dbb2257b8227f2a4eab719c79ef1c419e3a07b39dbc`  
		Last Modified: Thu, 17 Oct 2024 01:10:04 GMT  
		Size: 64.4 MB (64393080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bc85537ac7c401eea9ed38d4a75fddbe5d75d5570921f1c435a8342b3cef15`  
		Last Modified: Thu, 17 Oct 2024 01:10:40 GMT  
		Size: 211.3 MB (211281151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97b348fbebca67b25f027e550f95573ba6aff2f81f748dbf3e11e96d7fc6da6`  
		Last Modified: Thu, 17 Oct 2024 02:57:32 GMT  
		Size: 184.3 MB (184341137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:afd613e0c8388610680d95743ce6b0519e2e288ab2180009d03fdee5263cf66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ce36b1a51263afe43943de85c9d45999d4fd4b9197ac8e48278804e18c1582`

```dockerfile
```

-	Layers:
	-	`sha256:7b956ebc4fdf5bc354458d55f06403a6a7feff6dbe43975c601c444a5d70edc5`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde1eebb12461b3cf18799768782571274684aa61647d4c0e77a0b7d51d3c40`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 13.0 KB (13004 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:27b6e9bd919166bac1fb9211e9e52449d5fb725a70122e2280b3f235eef01f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.5 MB (523464584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd1ab1a770c8f7aa48d8b41c6152318ce574fb409b4620f8fea171c3ba763c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea668db82ddd31e7300e905d69bfbcc24fd0c70cd7c7212c915763a9e47f3e7`  
		Last Modified: Fri, 27 Sep 2024 07:39:33 GMT  
		Size: 175.2 MB (175207938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807abecaed8d4cffae0b7d1da027197029821fd16d2bbce8c0f8a1f90fd349f3`  
		Last Modified: Sat, 28 Sep 2024 04:08:11 GMT  
		Size: 221.5 MB (221511519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ee2cbc5b0aa8369395392c722b55ad9ac0bd4916118b0cdf63d4d0f13269a299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15270591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa74c1d6fa4c9dda9c706f2706450a4b81da24d4559310f49de7e46773f9700`

```dockerfile
```

-	Layers:
	-	`sha256:45c0558bf77c60592fcc61666d1d55c2e8062c13eee2815becd8547e5fe62df5`  
		Last Modified: Sat, 28 Sep 2024 04:08:07 GMT  
		Size: 15.3 MB (15257523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab9e3cff7b672ef6b62a3eecbf1b9c661a226d91214cd3d7b68a9fd5b262ff05`  
		Last Modified: Sat, 28 Sep 2024 04:08:06 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f5fbbf475717a8e1fcfda24fc26c60200eb95e19b03291f3e43e60995a4d406e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.7 MB (588709463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d76e87cace62dbdc9c3a6c3fae1623de64a44b8b274d79b8e95bcd89b6f1e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71ace0e8bbdcfcf795b836e24a37a6ed0054100e14d6aa6e5a63f7e162ba729`  
		Last Modified: Fri, 27 Sep 2024 05:25:40 GMT  
		Size: 202.7 MB (202651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c70a9d34bb788145305c907ff9a5ed64690b67c5abbc4b676ff607611081e0`  
		Last Modified: Fri, 27 Sep 2024 23:30:32 GMT  
		Size: 248.5 MB (248529120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:be6c0d1bdd139e794a093f63bbdcf7c53acbacba5babbcf59b54af8fd37f7cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15494574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23350ebe95ee44b5c009236d86e0a9d13772ae5689fa9c3449fec0987bd7b81d`

```dockerfile
```

-	Layers:
	-	`sha256:7c227d855755631f9fc25b4280c874ce996590e6446ce7c7399e0c496bd31670`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 15.5 MB (15481248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a10530d2c00a615465f62c3a9b01ff478facbfb4d920cbbf7d0d386c559eb44`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-bookworm` - linux; 386

```console
$ docker pull rust@sha256:cae43437babe4a513bfaf1ebaed7b47e916e1a96bea4496ee763708f2a2b5bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549225958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af64455d7089be15c70fda713c93555e12afb877f65a7b29d2b3dddfab02d1f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9dd8137152c295fb3624be3ee13689c34dc13bc115d0032a5a2a581001f14f`  
		Last Modified: Thu, 17 Oct 2024 01:09:36 GMT  
		Size: 24.9 MB (24895435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbad5c607546fed7ceeb86b3cef161781f7cb90e39cb2c8da1b7774aa73975d4`  
		Last Modified: Thu, 17 Oct 2024 01:09:58 GMT  
		Size: 66.2 MB (66210908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c0ef7e16c4ea3f5643d06ea746c15f35cca787121e7078904f6a16114c48`  
		Last Modified: Thu, 17 Oct 2024 01:10:44 GMT  
		Size: 210.2 MB (210196330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f818dcff8930802b82fed8fbd3b89feef62a7b69bc64cebb8df64281a6dd9`  
		Last Modified: Thu, 17 Oct 2024 02:57:36 GMT  
		Size: 197.3 MB (197346451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bc528a75faa20afa57e2c7e4b6f51d9b57b5485d2d379eea44c3bf52d6fbd4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808162f63c550251d4aaa7a5eee4f171d732b78e387b1137976a4a926ec4476c`

```dockerfile
```

-	Layers:
	-	`sha256:cecf68aacf4ab8230e1cd8e54fe8e2c4fe0ecb15f64b69df35db646913b7bdd2`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73cb9933a9869db1cc6fb4636124d96cbfd43111b4b05b820c4e12217bc5b56`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:4d19fbcc0f0bb56e4a6b711398e5de3a634385319d0e8b2bbc0171c109260070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.1 MB (606115637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3374c6411cbaed1bfb06437a6e1edc6a41bd7b83e37ca5ecc6a1aaec09413300`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e2f2830e2003232ca51768518e8eb9e372430ea0c0445d3ec3c8d96672cb8c`  
		Last Modified: Fri, 27 Sep 2024 06:05:25 GMT  
		Size: 214.3 MB (214285718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83748e1ac06a3fcddae1dc3110de6342c4531f82f43779a5fabf89719505db6a`  
		Last Modified: Sat, 28 Sep 2024 05:54:49 GMT  
		Size: 242.7 MB (242735060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:606824019a2d5065cd43eaea75ffe3725a698dd0f28a75d3e050d7cccc157b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15440370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa45a38a900b92dbf585c0410238a0e5b5c4b9b926802c9c7acad6c298aeda8f`

```dockerfile
```

-	Layers:
	-	`sha256:9ab533a7bde3dae7d525cc723b7c2e2eeb5504de5e82bb10f2a6051c078f243c`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 15.4 MB (15427343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c830e1f96c43a12bb0b2d3f79e8307d9635fb3e3532b2762ab339dff8d8738fd`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 13.0 KB (13027 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:0d9fc54c3ca5405db6f5892b2d90b374c38cab322301c88c164cb3d632dcacbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587261517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe66d1e8a70bea815ee500895b94596821696d893861c02b693a4f83ae31166c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1411196315040fbdc5fb36f5519fcdf47619046fa9476d4e7607333bcbd8131`  
		Last Modified: Fri, 27 Sep 2024 03:21:02 GMT  
		Size: 183.3 MB (183287662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35ddee15ec8c9e03e7f842b910c8fd17fe9bfef5ca8c21b7f32fbff8bbcc496`  
		Last Modified: Fri, 27 Sep 2024 17:40:49 GMT  
		Size: 268.5 MB (268487969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:03ac78767400c1d1b9c984acca6bd90df72cac0fb00e9100b2c5a8ee2438346e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15278999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1375e7d3522dd5c1a611790297f685c2fe0704944053af8e43e7d8a89930cc3`

```dockerfile
```

-	Layers:
	-	`sha256:f28e04508e5f7206d96f053f77275ef0c0bb7fa9f8a03c918a24d3fb10588e28`  
		Last Modified: Fri, 27 Sep 2024 17:40:44 GMT  
		Size: 15.3 MB (15266033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1a546a507332436c927687563a98866a316dbc8fab3ac46845bfa34cbe62b1`  
		Last Modified: Fri, 27 Sep 2024 17:40:43 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81.0-bullseye`

```console
$ docker pull rust@sha256:8328d21407009f8a2d17b0327f32c63411a8c3d5590b71ab87ea993cd2ffd169
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

### `rust:1.81.0-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:c0c156a4887bdbf6abea8f98258d9d27cfe4c3f2794f674dfb6f5d237de67687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.0 MB (506995658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f511550e16ed987835311ad1d9c0da1b2b1d597b933aed15e44eb452187f9a9b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06817e07ed0f03c17ad0a7aa8ef22b2a6fcf2b939d6212ab0861571ef18a45b`  
		Last Modified: Thu, 17 Oct 2024 01:10:51 GMT  
		Size: 15.8 MB (15764889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173ffc78585eeabe33105e00a7be99b0cad17d5e6edebf7f760d7824fa76969`  
		Last Modified: Thu, 17 Oct 2024 01:11:06 GMT  
		Size: 54.7 MB (54723650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe335f0e34a87e4cbd05c121253490f0c293f8ff29540aa8cd3fc22d4519931`  
		Last Modified: Thu, 17 Oct 2024 01:11:36 GMT  
		Size: 197.1 MB (197085334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66586d4b6a786f40aa4eede68f290dbb5be4152d931746d9bbb17b4b085fcf7`  
		Last Modified: Thu, 17 Oct 2024 02:57:35 GMT  
		Size: 184.3 MB (184341174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7db843194e10c40a284a5f8742a0e692118d3bd1809aa01d16105ab7ec0823ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15063552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c6e3fd4ce8ce97591522bfaf2a495aa59ca89437e220dc586da3fde58d8f0e`

```dockerfile
```

-	Layers:
	-	`sha256:3e0db2ae8efc7a4b906bc15ffdce2bbda5f1c7cbea6015ea958b7c95523d700f`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 15.1 MB (15052438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2033b7ff7e29ef72ea44cc8fe20a94267d7ca6eaded58686e78d093bb6c8ed7f`  
		Last Modified: Thu, 17 Oct 2024 02:57:30 GMT  
		Size: 11.1 KB (11114 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:84331046d2e6bbfe4845d2ef8384cc8281fcbcf0e28fd1071709a3aa34eab212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.8 MB (504758766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d19257130fa88be44790843793cd4e706a1b61733f0e90388b767119ffb2bb`
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
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec523352a6e63a855ebebdbc8288b9cccf719fe4121211d5e0cae3f11e4f6b2`  
		Last Modified: Fri, 27 Sep 2024 07:39:46 GMT  
		Size: 14.9 MB (14879678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bfb8add2d4bda22b21df2a3eff38a6f4f66c2ef9fe110e7714a93f720a4f47`  
		Last Modified: Fri, 27 Sep 2024 07:40:06 GMT  
		Size: 50.6 MB (50618560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f69bcefdc97cf5fabaf3b01d416ce54278fa217058c4433beb68d39a6e1bc1`  
		Last Modified: Fri, 27 Sep 2024 07:40:47 GMT  
		Size: 167.5 MB (167508654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc16697bf56cf2fe7d356c600c48e8a13b2fb6f003a40aec403b77bf1e5a1777`  
		Last Modified: Mon, 07 Oct 2024 20:10:32 GMT  
		Size: 221.5 MB (221511494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3c9b6060fce57e62fb04164d07286dabb9431d2eb979eb665cf468a807fbe9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14864469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873edee47bb20240914debd5c61b9dd61ca27e7d1d73fc95f7657eb67d1419a4`

```dockerfile
```

-	Layers:
	-	`sha256:9e1a11645f7ce0d9026d44c1007e1f6ba2b3f0765e25fa435075743651016034`  
		Last Modified: Mon, 07 Oct 2024 20:10:28 GMT  
		Size: 14.9 MB (14853318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c5c9edc1a5a4d7481d377fa24e5662235f1ce8b366e78cd64a8bc412ee69cb7`  
		Last Modified: Mon, 07 Oct 2024 20:10:27 GMT  
		Size: 11.2 KB (11151 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:230f0887e9953ba599f30462d1601b3af95d1136cf8c1057b77533f0ea13993d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.8 MB (562811378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7fd17cd619497e8cf227bc8f6b6be5a4ceaf9020f09b88694555ccf79d7f65`
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
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4bba36b8add5e5ec5da6aa2c18637b64bce2d5f3f7d83723817e2139a11bcc`  
		Last Modified: Fri, 27 Sep 2024 05:25:50 GMT  
		Size: 15.7 MB (15749698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f212bcfdd3a473cde2991df3e1cf5373d8f097a630557a35fa77d891acce93d6`  
		Last Modified: Fri, 27 Sep 2024 05:26:04 GMT  
		Size: 54.8 MB (54834694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09310330a122777457e6d6b3094e1d1391aa246ba1b028adeb03cd353d0d29`  
		Last Modified: Fri, 27 Sep 2024 05:26:28 GMT  
		Size: 190.0 MB (189964252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da761adc8113e8e908061d91c6af387f04a41e668d2f111540d11a9ef01e5f0`  
		Last Modified: Mon, 07 Oct 2024 20:28:00 GMT  
		Size: 248.5 MB (248528870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f7218307ed60ee81340e8a569d237e241c8e97cac632dc78555ab6083d40909e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15065824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fecd41b23cc4f020e9f319dbf75f1613baa97e283f738646f4a549d49a0a29`

```dockerfile
```

-	Layers:
	-	`sha256:fecaccd039897250aae8a94b1523d4955c0726ff860d9f3a605565fd7b63d201`  
		Last Modified: Mon, 07 Oct 2024 20:27:55 GMT  
		Size: 15.1 MB (15054645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:357925a5449c30f481550c08a6e83d080b7faa1982dfdb43af76649057e41280`  
		Last Modified: Mon, 07 Oct 2024 20:27:54 GMT  
		Size: 11.2 KB (11179 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-bullseye` - linux; 386

```console
$ docker pull rust@sha256:0b74763c0c9110dc9342754e733f284101a3090b083abd7c9eb73f9e9162fee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.7 MB (525706874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01cf6a6c0b6626ce6748e3de2ff0182d8febe57f7c55eac503d91d6f9a3e1c7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000ce4e381f50a8f76ae5a1d4bcd9702f5146bac4fb30afc4e12c284ee68ca9`  
		Last Modified: Thu, 17 Oct 2024 01:10:55 GMT  
		Size: 16.3 MB (16268542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d0b1f51e6e34773cde9f3b41201942ff88384d907912b25ff3349f296f69b8`  
		Last Modified: Thu, 17 Oct 2024 01:11:14 GMT  
		Size: 56.0 MB (56032019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b257135cb04b7c9d5ceaf0572a0941a80b7eb3f7dd31444289a12b792e314e8`  
		Last Modified: Thu, 17 Oct 2024 01:12:01 GMT  
		Size: 200.0 MB (199982090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3420ca7067654974fc0f1971890285287aef101e8c0ad81c1d01689969ded4ec`  
		Last Modified: Thu, 17 Oct 2024 02:57:46 GMT  
		Size: 197.3 MB (197346400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f58b08210121da703d98863e10d84097f158a04b4f053e9f579b47a0ecd6819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b309ca17610165025ded60cffba70e585bf2294d8a81fe1ff260572e71d460d`

```dockerfile
```

-	Layers:
	-	`sha256:c660bef212dab636443f1060b4e1e7ca7a48a89cdf8c12a8d6298cf1ed6616f6`  
		Last Modified: Thu, 17 Oct 2024 02:57:42 GMT  
		Size: 15.0 MB (15040975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f6ca99ad4fa67ac8b5d8bd3b23ad2542d63b6634953bb2057d5c3e1a4443b8`  
		Last Modified: Thu, 17 Oct 2024 02:57:42 GMT  
		Size: 11.1 KB (11085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81.0-slim`

```console
$ docker pull rust@sha256:5f54e4f0f25ffcb8493d73f38cbd7dd5f6b83ca78d6a33224fc326f6d654d16f
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

### `rust:1.81.0-slim` - linux; amd64

```console
$ docker pull rust@sha256:45966c8f3e8348b7643bd40eb846b87015a6f1694ed2a13ca8475c5be35df8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284254306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b63b5bcc9542ec50795afee904fd719f71dbf5f3cd84e74de4c92f7808a727f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0607d7c68e964f9d197627ffe492db8c9ce40d39951ee73a3182e028b0be4e`  
		Last Modified: Thu, 17 Oct 2024 01:30:10 GMT  
		Size: 255.1 MB (255128017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:f17aeca9415c8c8b3eec6d14b5a90f91bbe302ef815e6513d5763f9b1d2b645c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010e722839b0079d58e9aa6bcd3b6446f5bd6702bbfe47fc984b869d24c68e15`

```dockerfile
```

-	Layers:
	-	`sha256:e6e2cf59070156e4177eabcbb570b524e550d23ecba4082cc0876549b6a34458`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78cde42d64af02ec433aba2279aede7b5ce92746174556b598fd74de7abd9517`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 13.1 KB (13090 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:08dbf3d9d24bae232365620c62410ec5d83596ff380aad5f49e27cdec7317513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294070169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e6abf46c4d525890ed87fc173518b54a4bd6a1b01b96fe447fb1d17e08346a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4408bd841243a9a42a8e256c364029c480e1b0b2865b22e70a46bde0100c866`  
		Last Modified: Fri, 27 Sep 2024 18:42:06 GMT  
		Size: 269.4 MB (269352024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:df722b016f3cca3b94348d0bc6f597be00e94961777ca5cb428cf4cdd0af6f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e61fad66437481804743201bd550faf73c0e8846ddb64f6d8bf18e0dff7a4a3`

```dockerfile
```

-	Layers:
	-	`sha256:e090a867d43bfae1fb514bbb85985f7c87fff9bd5a411d0ec1cdcf062ed1c5f1`  
		Last Modified: Fri, 27 Sep 2024 18:42:01 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffb56d93014b97c2bf56f856a3b3c0c1c6de63989a9e8fca173c3abc901f156`  
		Last Modified: Fri, 27 Sep 2024 18:42:00 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3ba3fbf62527788a60c4908b3c389bab7f5ab6fb919ea3c771aeb9a278966253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343526226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233c27109e17c04665f9ed9ede09369aacd1865fc09fd1a6f5ac4863e32fc4a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995fd26d021eddb871651f81a432e2662de3c5b719d2248d4552105c40a67e47`  
		Last Modified: Fri, 27 Sep 2024 23:32:02 GMT  
		Size: 314.4 MB (314369857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:e4a5a923d2e13d83eb71aa2cb933b273577721a70c5ff55a15af8cd5f4d21978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633019f2483a2e86da7ee1384084a836d087aab2347f626c8490a683b80397fc`

```dockerfile
```

-	Layers:
	-	`sha256:45375e55489ffbdb8bd47dbec3eee1f67a6679081f46e4dc1ac6c76ce18b1904`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f968eae71eae982a4adc164da8a72a293dd418f197ba71ede38a68bb18be6c05`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim` - linux; 386

```console
$ docker pull rust@sha256:ba4ee661bb466ab49f6ceb8c6d9e9f9784bba7c6e45225187cd3c7fb1fbc12ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295093589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e4df283163309e2fdaa8101fa73b670d133162155d4cd23424016dd87db8e4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a718584a1346679f83b1655ad2ac313c29bec26411eeb7c34dad2a91b6577448`  
		Last Modified: Thu, 17 Oct 2024 01:30:07 GMT  
		Size: 264.9 MB (264949322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4c72332e16899bfc022e891c90f0d93e00f555271f92b2e38817f8afa453c722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ca94475147e0318e9bad8ec073ef9dd87fef510c2eed0171a3f48a81c843a`

```dockerfile
```

-	Layers:
	-	`sha256:12434a1e188136de888271297f6eb4670c269905a0833cb0c26866ab817a1eac`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11e3392f42511d72755c775a9cd45fb9f2d612485058889a5a61cbb5dda587f`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 13.0 KB (13043 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:46bcce128e6ab5402c648739e95aa56eb2ed32d840ff42da0975ec8428034ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344618727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4f6cbc6fd8ecc671e77ece602998ab1fa543c11db83d5d64fa6bc051b111c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097a47a9153a9d3d44374a545c87a489f3842a16e291caf5a817ebaa5a0f1552`  
		Last Modified: Sat, 28 Sep 2024 04:15:09 GMT  
		Size: 311.5 MB (311496564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:fa335487319e81174f0920ee7efa014f25d5cdbbfdf8648c77cfeb1f771129bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f51b298cbeb650a1f7674e47e0ff5da39045f7a1c1b12678284013db4153e2`

```dockerfile
```

-	Layers:
	-	`sha256:17e6bf4b03c232f13acb280f35f3b04cad777afeab1156732f6d6e80ae08ac03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9673908047a020854098b5704b6ac719a43c3c5263868a007ef95e1dd656fe03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim` - linux; s390x

```console
$ docker pull rust@sha256:1986b817125878c181d9add8424b112238bbcd915e03b3444b6e3b9962a71844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346124228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaf144d0210bf05141bac7875bc21c09171ace17f17693c306e46ee2347cc8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d24393939cc6c4eddc3a49c03d07080edb453591af15f5f40c3481b1c43289`  
		Last Modified: Fri, 27 Sep 2024 17:42:41 GMT  
		Size: 318.6 MB (318634204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:981dce7ac4cd7769d68270976ad41a566057debc664228639318ceeee2878c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb7573b7c4578171c99e4b1c475220bae80fd01a2abcc1ff7de0c789cee9993`

```dockerfile
```

-	Layers:
	-	`sha256:165fd9d1067cb2b20bc1127fb26bf62317d9ec727e17d418b73ad480975a460f`  
		Last Modified: Fri, 27 Sep 2024 17:42:37 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03aa2d5f9daee31ee7485507b38e1a42c341c49bd4f504117c96708fe84908d5`  
		Last Modified: Fri, 27 Sep 2024 17:42:36 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81.0-slim-bookworm`

```console
$ docker pull rust@sha256:5f54e4f0f25ffcb8493d73f38cbd7dd5f6b83ca78d6a33224fc326f6d654d16f
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

### `rust:1.81.0-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:45966c8f3e8348b7643bd40eb846b87015a6f1694ed2a13ca8475c5be35df8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284254306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b63b5bcc9542ec50795afee904fd719f71dbf5f3cd84e74de4c92f7808a727f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0607d7c68e964f9d197627ffe492db8c9ce40d39951ee73a3182e028b0be4e`  
		Last Modified: Thu, 17 Oct 2024 01:30:10 GMT  
		Size: 255.1 MB (255128017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f17aeca9415c8c8b3eec6d14b5a90f91bbe302ef815e6513d5763f9b1d2b645c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010e722839b0079d58e9aa6bcd3b6446f5bd6702bbfe47fc984b869d24c68e15`

```dockerfile
```

-	Layers:
	-	`sha256:e6e2cf59070156e4177eabcbb570b524e550d23ecba4082cc0876549b6a34458`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78cde42d64af02ec433aba2279aede7b5ce92746174556b598fd74de7abd9517`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 13.1 KB (13090 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:08dbf3d9d24bae232365620c62410ec5d83596ff380aad5f49e27cdec7317513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294070169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e6abf46c4d525890ed87fc173518b54a4bd6a1b01b96fe447fb1d17e08346a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4408bd841243a9a42a8e256c364029c480e1b0b2865b22e70a46bde0100c866`  
		Last Modified: Fri, 27 Sep 2024 18:42:06 GMT  
		Size: 269.4 MB (269352024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:df722b016f3cca3b94348d0bc6f597be00e94961777ca5cb428cf4cdd0af6f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e61fad66437481804743201bd550faf73c0e8846ddb64f6d8bf18e0dff7a4a3`

```dockerfile
```

-	Layers:
	-	`sha256:e090a867d43bfae1fb514bbb85985f7c87fff9bd5a411d0ec1cdcf062ed1c5f1`  
		Last Modified: Fri, 27 Sep 2024 18:42:01 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffb56d93014b97c2bf56f856a3b3c0c1c6de63989a9e8fca173c3abc901f156`  
		Last Modified: Fri, 27 Sep 2024 18:42:00 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3ba3fbf62527788a60c4908b3c389bab7f5ab6fb919ea3c771aeb9a278966253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343526226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233c27109e17c04665f9ed9ede09369aacd1865fc09fd1a6f5ac4863e32fc4a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995fd26d021eddb871651f81a432e2662de3c5b719d2248d4552105c40a67e47`  
		Last Modified: Fri, 27 Sep 2024 23:32:02 GMT  
		Size: 314.4 MB (314369857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e4a5a923d2e13d83eb71aa2cb933b273577721a70c5ff55a15af8cd5f4d21978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633019f2483a2e86da7ee1384084a836d087aab2347f626c8490a683b80397fc`

```dockerfile
```

-	Layers:
	-	`sha256:45375e55489ffbdb8bd47dbec3eee1f67a6679081f46e4dc1ac6c76ce18b1904`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f968eae71eae982a4adc164da8a72a293dd418f197ba71ede38a68bb18be6c05`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:ba4ee661bb466ab49f6ceb8c6d9e9f9784bba7c6e45225187cd3c7fb1fbc12ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295093589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e4df283163309e2fdaa8101fa73b670d133162155d4cd23424016dd87db8e4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a718584a1346679f83b1655ad2ac313c29bec26411eeb7c34dad2a91b6577448`  
		Last Modified: Thu, 17 Oct 2024 01:30:07 GMT  
		Size: 264.9 MB (264949322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4c72332e16899bfc022e891c90f0d93e00f555271f92b2e38817f8afa453c722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ca94475147e0318e9bad8ec073ef9dd87fef510c2eed0171a3f48a81c843a`

```dockerfile
```

-	Layers:
	-	`sha256:12434a1e188136de888271297f6eb4670c269905a0833cb0c26866ab817a1eac`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11e3392f42511d72755c775a9cd45fb9f2d612485058889a5a61cbb5dda587f`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 13.0 KB (13043 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:46bcce128e6ab5402c648739e95aa56eb2ed32d840ff42da0975ec8428034ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344618727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4f6cbc6fd8ecc671e77ece602998ab1fa543c11db83d5d64fa6bc051b111c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097a47a9153a9d3d44374a545c87a489f3842a16e291caf5a817ebaa5a0f1552`  
		Last Modified: Sat, 28 Sep 2024 04:15:09 GMT  
		Size: 311.5 MB (311496564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:fa335487319e81174f0920ee7efa014f25d5cdbbfdf8648c77cfeb1f771129bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f51b298cbeb650a1f7674e47e0ff5da39045f7a1c1b12678284013db4153e2`

```dockerfile
```

-	Layers:
	-	`sha256:17e6bf4b03c232f13acb280f35f3b04cad777afeab1156732f6d6e80ae08ac03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9673908047a020854098b5704b6ac719a43c3c5263868a007ef95e1dd656fe03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:1986b817125878c181d9add8424b112238bbcd915e03b3444b6e3b9962a71844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346124228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaf144d0210bf05141bac7875bc21c09171ace17f17693c306e46ee2347cc8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d24393939cc6c4eddc3a49c03d07080edb453591af15f5f40c3481b1c43289`  
		Last Modified: Fri, 27 Sep 2024 17:42:41 GMT  
		Size: 318.6 MB (318634204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:981dce7ac4cd7769d68270976ad41a566057debc664228639318ceeee2878c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb7573b7c4578171c99e4b1c475220bae80fd01a2abcc1ff7de0c789cee9993`

```dockerfile
```

-	Layers:
	-	`sha256:165fd9d1067cb2b20bc1127fb26bf62317d9ec727e17d418b73ad480975a460f`  
		Last Modified: Fri, 27 Sep 2024 17:42:37 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03aa2d5f9daee31ee7485507b38e1a42c341c49bd4f504117c96708fe84908d5`  
		Last Modified: Fri, 27 Sep 2024 17:42:36 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81.0-slim-bullseye`

```console
$ docker pull rust@sha256:915a4826b6111266e53e06f47c16cddebf36901623f0631f2cc10ce5c26022e5
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

### `rust:1.81.0-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:955e6b161e189ce9a70a3176d62bc853df1d45a8ff2c877bcc2639c1334e05da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275916178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72160f9a4acd420abe48f6f6d762750669ca08d8e16c3612f2aa8e48e6886df1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b38e595cdc330fbe56f1cc54e1fbb521c5c78b889fda1cb2553ec996eb7494`  
		Last Modified: Thu, 17 Oct 2024 01:28:56 GMT  
		Size: 244.5 MB (244487378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:913457ace1ef4de84bcd5852f75e36f52b6ec6cb0381db81b057670c1f7a64c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900b212c9018b48677c88ed0905ec79728757d918f45bb4e41c5f9ac0e6c8a10`

```dockerfile
```

-	Layers:
	-	`sha256:8347c9cf5193ed18506b7d4c96a1dd5a0451c1c9d4c0049fd6c1adaaefe4b7cb`  
		Last Modified: Thu, 17 Oct 2024 01:28:53 GMT  
		Size: 4.2 MB (4164416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee600185d29aecb0803b6cd08dc6117b7080dbec62c710fa35ae4dffc674e387`  
		Last Modified: Thu, 17 Oct 2024 01:28:53 GMT  
		Size: 11.2 KB (11176 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:649f33f2004e7cf32279d259133d1c887680c82371ca61040be0676de14478f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290373521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c1dea15d81a85919b55bae459fdf9865c474d6a3eeded3a426c223d45f15fe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:05 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
# Fri, 27 Sep 2024 05:14:07 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0961dc5030bdc38ffd749a496abefd5f5e3c43706db1ac4fbe6a89b425b6f565`  
		Last Modified: Mon, 07 Oct 2024 20:12:29 GMT  
		Size: 263.8 MB (263784209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0fdedd82265ee4abb67e00cb5ed763bb6b00b1e1a9cff139eb943b524eceddc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3984890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4338ea06da0c03a6090e3a6d0cdfbf4558bd2939605e26dcb73de43f3ae2445a`

```dockerfile
```

-	Layers:
	-	`sha256:ba5dd9365cb77053e5b690af6fb2194be4ea48e4cf45c38343e7917bf11ac2d6`  
		Last Modified: Mon, 07 Oct 2024 20:12:23 GMT  
		Size: 4.0 MB (3973677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71bcc530464af98ed85ff675234211982092c53f113700732ff05ba7b7063828`  
		Last Modified: Mon, 07 Oct 2024 20:12:22 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5a6a01ab245dd0f9c1c5289854e6bfbf41eda63717a403c2ec5715751e29df3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334323993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53157f2dc99d3da88944463c603f1435f567f3e51e835146526d5ddc3602023e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a5b36cf8f1de6f21df811fbf5e9fc34a4a885fdb4d55f5d99d5d38e9e10aa1`  
		Last Modified: Mon, 07 Oct 2024 20:29:36 GMT  
		Size: 304.2 MB (304248835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:117078f67d65fb1fb6692b2e819225b0028efe02b38e50d365a11fb8218ade4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4172348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7528c856c92358d9c7cab5571c3f927091bf38d06d14ae6832f0cdb6a0ea1f`

```dockerfile
```

-	Layers:
	-	`sha256:e585026bbab5521b31de85e6d76a91d424b33a11f16dfc4c480cb11110170e68`  
		Last Modified: Mon, 07 Oct 2024 20:29:28 GMT  
		Size: 4.2 MB (4161108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:115eecb4972db015834bb7865e3b2013bcb5784751739299b04ee1938b1efb82`  
		Last Modified: Mon, 07 Oct 2024 20:29:28 GMT  
		Size: 11.2 KB (11240 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b869a05737d767ce7fb7056cf77751bb5a8b8b577dfbc911a05c94b2d3754822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290535137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a880359cc690264cb0b553f18917849f5c945bc7ff9fea96ceea4696a15d345f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabfbb638063d13147d4f9a1a5694685c92adb5cf15ae94665eae2cd245e5f7a`  
		Last Modified: Thu, 17 Oct 2024 01:29:49 GMT  
		Size: 258.1 MB (258121307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e7bc0dd978b6918b697d54b2322bd89a8fc2364017dc1354c01927066ba886ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c222bd0ec93f4d3719cfa3e3ebd12b938ba155acbede32405b0b9551d71c0e27`

```dockerfile
```

-	Layers:
	-	`sha256:58a6810008287c12bb6320144c20f384550200c86b54ba7c87a2e079a24c5263`  
		Last Modified: Thu, 17 Oct 2024 01:29:43 GMT  
		Size: 4.2 MB (4156184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08b166a715fea1c9ef90fcc577433cc2762aea86d09168615d781dd8d5e38012`  
		Last Modified: Thu, 17 Oct 2024 01:29:43 GMT  
		Size: 11.1 KB (11146 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:d6e876ca5fe200f4ac60312b95606f0b042699c4cf6a19493b7d2a2ebbfb337b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:03b96a6b633cc6d3d1168e1afa2357ba5ccce128da909ba3b57487f0cc228428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283243467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c2a31537b2eac7656edddd62805b51abda9efb6f3761a92363fd35bac462ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7a6c0b92f840b647ad3fdd4fc8c1739f833da486d7e51793f4c1ebe411333`  
		Last Modified: Fri, 06 Sep 2024 23:25:12 GMT  
		Size: 55.3 MB (55309249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d299bec348b12e4baacefd5ece1f43bfb77ef3abe2e52f56ad4d5e67c263b056`  
		Last Modified: Fri, 06 Sep 2024 23:25:20 GMT  
		Size: 224.3 MB (224310411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:1d57ee624f00a8ce856aa31ba4730a87c91d9a11b9fd595f3d385f5bb44ece20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6497981077302a8c905b5e4e2dfffd9ac14137a0cfc7497d4dcafc806053e7`

```dockerfile
```

-	Layers:
	-	`sha256:da26bdf9689b6139ac3ee467c818e036ca25e103dae29ddb9f158f48efec517d`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2530f84e604ec82ab6979568cbfe879a3721c0a3adea3f06fb87cda5819f968e`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 11.7 KB (11678 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d577dfa9ebb3576ed0824cd4a6665ce2a1a37b908bf767ed0f96c10360f19e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291454748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193dfcd4e8418a0b3ab51d24dd2601d67cb5f6f7446bdcf55c7fc139421a0836`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dae75a7979f5c823e78faad77f0683f4120db209a14f80f65d35ffcfb6465c`  
		Last Modified: Sat, 07 Sep 2024 11:56:50 GMT  
		Size: 52.9 MB (52946235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d0ba6d79ddcc7adb2e073c295844423f77032e7b03bc7973c24f60d3d5ae3`  
		Last Modified: Sat, 07 Sep 2024 11:56:54 GMT  
		Size: 234.4 MB (234420867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:09413672bd07b597f07a8cc58f505f88e517959490527c39693b43a71c238377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f7960713521b5f6f4f75e0f419a67822c4ca3ac34eedb0753910785c0c3881`

```dockerfile
```

-	Layers:
	-	`sha256:b85be6b172df08e0e211efd0e6354594a97df69970d84ea800b01169be9286f4`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486ea238c8b03b69cfc3df4c2c5336edce93eb2ae87385c5b1b31951f59bdef2`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.19`

```console
$ docker pull rust@sha256:5b6bdc02ef966d208c7edc309d3cdf75725b3a0fe6535f4460f9d2d7fb88322b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:c45cc04288af707001a7a90382d16dc29309508b0d274a4c61282bad7ecd8345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283076960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e2a973eb4a9819fb599046858b1ccd486ae9157ed0d695bb65d7016cb83135`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b596d4da02c982671dbf6bed836470acee3a2fadc6863ba9e1cce5e388c93ab`  
		Last Modified: Fri, 06 Sep 2024 23:24:43 GMT  
		Size: 55.3 MB (55346883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872d9e0d3eae5459c9159c8cc624a3c35789017552614cda7063b19930cfda94`  
		Last Modified: Fri, 06 Sep 2024 23:24:47 GMT  
		Size: 224.3 MB (224310371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:e32690943c1038ed26065af835abea2eb061b1715bfd4330fe65d48ec1198103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdc2c73e311f0afde5234e3a30984507a7113be703884269be015f6a435cf5d`

```dockerfile
```

-	Layers:
	-	`sha256:612b4526cbae481700ab36cb68a6c9c0af9f27506d9f7dbe6867e3fb2e9a3ddd`  
		Last Modified: Fri, 06 Sep 2024 23:24:42 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e67ae8c135e6a6076ec3f5355c54c343cef04d8f379ed48c426f2dd6ba2622c9`  
		Last Modified: Fri, 06 Sep 2024 23:24:42 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2ad5d810439717463a3ad522bfe9c626490ca35176488b753a9e57d23f35d9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290775337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e25ee6035525a540920de98ffd4b96c964d2195252fb1dc32743828b84b0b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74da714a92090eec171b9fdcc6c89c6591ba432fdeeaa10d5c10538ede56c8a`  
		Last Modified: Sat, 07 Sep 2024 11:55:42 GMT  
		Size: 53.0 MB (52995429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b56e9f588d67bf61a8465ec612c0b1095ef03b2d5afe03498b7ad4fed2fd38f`  
		Last Modified: Sat, 07 Sep 2024 11:55:47 GMT  
		Size: 234.4 MB (234420805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:f9446358434100ac647f0d3dd9a0e1b2005a6f8910ede685cdc2e9e9c2ec5eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644500100d93dbb3715254eb9f6a6028976c644a3ea440840fa3de87e015593a`

```dockerfile
```

-	Layers:
	-	`sha256:5318473dfb1acaa5a3766971ec81932624e4e3e24520ff1226b8de3a4d1eabbc`  
		Last Modified: Sat, 07 Sep 2024 11:55:41 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5f4a984e365a0132171af9a5448f3da92750593f5660cb7358ca62cbe7b3b30`  
		Last Modified: Sat, 07 Sep 2024 11:55:40 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.20`

```console
$ docker pull rust@sha256:d6e876ca5fe200f4ac60312b95606f0b042699c4cf6a19493b7d2a2ebbfb337b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:03b96a6b633cc6d3d1168e1afa2357ba5ccce128da909ba3b57487f0cc228428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283243467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c2a31537b2eac7656edddd62805b51abda9efb6f3761a92363fd35bac462ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7a6c0b92f840b647ad3fdd4fc8c1739f833da486d7e51793f4c1ebe411333`  
		Last Modified: Fri, 06 Sep 2024 23:25:12 GMT  
		Size: 55.3 MB (55309249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d299bec348b12e4baacefd5ece1f43bfb77ef3abe2e52f56ad4d5e67c263b056`  
		Last Modified: Fri, 06 Sep 2024 23:25:20 GMT  
		Size: 224.3 MB (224310411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1d57ee624f00a8ce856aa31ba4730a87c91d9a11b9fd595f3d385f5bb44ece20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6497981077302a8c905b5e4e2dfffd9ac14137a0cfc7497d4dcafc806053e7`

```dockerfile
```

-	Layers:
	-	`sha256:da26bdf9689b6139ac3ee467c818e036ca25e103dae29ddb9f158f48efec517d`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2530f84e604ec82ab6979568cbfe879a3721c0a3adea3f06fb87cda5819f968e`  
		Last Modified: Fri, 06 Sep 2024 23:25:11 GMT  
		Size: 11.7 KB (11678 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d577dfa9ebb3576ed0824cd4a6665ce2a1a37b908bf767ed0f96c10360f19e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291454748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193dfcd4e8418a0b3ab51d24dd2601d67cb5f6f7446bdcf55c7fc139421a0836`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["/bin/sh"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dae75a7979f5c823e78faad77f0683f4120db209a14f80f65d35ffcfb6465c`  
		Last Modified: Sat, 07 Sep 2024 11:56:50 GMT  
		Size: 52.9 MB (52946235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d0ba6d79ddcc7adb2e073c295844423f77032e7b03bc7973c24f60d3d5ae3`  
		Last Modified: Sat, 07 Sep 2024 11:56:54 GMT  
		Size: 234.4 MB (234420867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:09413672bd07b597f07a8cc58f505f88e517959490527c39693b43a71c238377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f7960713521b5f6f4f75e0f419a67822c4ca3ac34eedb0753910785c0c3881`

```dockerfile
```

-	Layers:
	-	`sha256:b85be6b172df08e0e211efd0e6354594a97df69970d84ea800b01169be9286f4`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486ea238c8b03b69cfc3df4c2c5336edce93eb2ae87385c5b1b31951f59bdef2`  
		Last Modified: Sat, 07 Sep 2024 11:56:48 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:0757ed8c0609498399dfde17ad6e5ac4adc5da04096fbd3d9c2301c62b93546b
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
$ docker pull rust@sha256:62afc139057dc9d3eda02e490677911b55a208ba22d6f7315f3c5c5851e31a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533623479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3b0145b0fabfa9f7bfc382e163449775329c6b95cb5704237a770a9e6e52a1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba0b3d08b81baa192d30dbb2257b8227f2a4eab719c79ef1c419e3a07b39dbc`  
		Last Modified: Thu, 17 Oct 2024 01:10:04 GMT  
		Size: 64.4 MB (64393080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bc85537ac7c401eea9ed38d4a75fddbe5d75d5570921f1c435a8342b3cef15`  
		Last Modified: Thu, 17 Oct 2024 01:10:40 GMT  
		Size: 211.3 MB (211281151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97b348fbebca67b25f027e550f95573ba6aff2f81f748dbf3e11e96d7fc6da6`  
		Last Modified: Thu, 17 Oct 2024 02:57:32 GMT  
		Size: 184.3 MB (184341137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:afd613e0c8388610680d95743ce6b0519e2e288ab2180009d03fdee5263cf66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ce36b1a51263afe43943de85c9d45999d4fd4b9197ac8e48278804e18c1582`

```dockerfile
```

-	Layers:
	-	`sha256:7b956ebc4fdf5bc354458d55f06403a6a7feff6dbe43975c601c444a5d70edc5`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde1eebb12461b3cf18799768782571274684aa61647d4c0e77a0b7d51d3c40`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 13.0 KB (13004 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:27b6e9bd919166bac1fb9211e9e52449d5fb725a70122e2280b3f235eef01f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.5 MB (523464584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd1ab1a770c8f7aa48d8b41c6152318ce574fb409b4620f8fea171c3ba763c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea668db82ddd31e7300e905d69bfbcc24fd0c70cd7c7212c915763a9e47f3e7`  
		Last Modified: Fri, 27 Sep 2024 07:39:33 GMT  
		Size: 175.2 MB (175207938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807abecaed8d4cffae0b7d1da027197029821fd16d2bbce8c0f8a1f90fd349f3`  
		Last Modified: Sat, 28 Sep 2024 04:08:11 GMT  
		Size: 221.5 MB (221511519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ee2cbc5b0aa8369395392c722b55ad9ac0bd4916118b0cdf63d4d0f13269a299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15270591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa74c1d6fa4c9dda9c706f2706450a4b81da24d4559310f49de7e46773f9700`

```dockerfile
```

-	Layers:
	-	`sha256:45c0558bf77c60592fcc61666d1d55c2e8062c13eee2815becd8547e5fe62df5`  
		Last Modified: Sat, 28 Sep 2024 04:08:07 GMT  
		Size: 15.3 MB (15257523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab9e3cff7b672ef6b62a3eecbf1b9c661a226d91214cd3d7b68a9fd5b262ff05`  
		Last Modified: Sat, 28 Sep 2024 04:08:06 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f5fbbf475717a8e1fcfda24fc26c60200eb95e19b03291f3e43e60995a4d406e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.7 MB (588709463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d76e87cace62dbdc9c3a6c3fae1623de64a44b8b274d79b8e95bcd89b6f1e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71ace0e8bbdcfcf795b836e24a37a6ed0054100e14d6aa6e5a63f7e162ba729`  
		Last Modified: Fri, 27 Sep 2024 05:25:40 GMT  
		Size: 202.7 MB (202651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c70a9d34bb788145305c907ff9a5ed64690b67c5abbc4b676ff607611081e0`  
		Last Modified: Fri, 27 Sep 2024 23:30:32 GMT  
		Size: 248.5 MB (248529120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:be6c0d1bdd139e794a093f63bbdcf7c53acbacba5babbcf59b54af8fd37f7cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15494574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23350ebe95ee44b5c009236d86e0a9d13772ae5689fa9c3449fec0987bd7b81d`

```dockerfile
```

-	Layers:
	-	`sha256:7c227d855755631f9fc25b4280c874ce996590e6446ce7c7399e0c496bd31670`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 15.5 MB (15481248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a10530d2c00a615465f62c3a9b01ff478facbfb4d920cbbf7d0d386c559eb44`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:cae43437babe4a513bfaf1ebaed7b47e916e1a96bea4496ee763708f2a2b5bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549225958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af64455d7089be15c70fda713c93555e12afb877f65a7b29d2b3dddfab02d1f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9dd8137152c295fb3624be3ee13689c34dc13bc115d0032a5a2a581001f14f`  
		Last Modified: Thu, 17 Oct 2024 01:09:36 GMT  
		Size: 24.9 MB (24895435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbad5c607546fed7ceeb86b3cef161781f7cb90e39cb2c8da1b7774aa73975d4`  
		Last Modified: Thu, 17 Oct 2024 01:09:58 GMT  
		Size: 66.2 MB (66210908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c0ef7e16c4ea3f5643d06ea746c15f35cca787121e7078904f6a16114c48`  
		Last Modified: Thu, 17 Oct 2024 01:10:44 GMT  
		Size: 210.2 MB (210196330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f818dcff8930802b82fed8fbd3b89feef62a7b69bc64cebb8df64281a6dd9`  
		Last Modified: Thu, 17 Oct 2024 02:57:36 GMT  
		Size: 197.3 MB (197346451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bc528a75faa20afa57e2c7e4b6f51d9b57b5485d2d379eea44c3bf52d6fbd4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808162f63c550251d4aaa7a5eee4f171d732b78e387b1137976a4a926ec4476c`

```dockerfile
```

-	Layers:
	-	`sha256:cecf68aacf4ab8230e1cd8e54fe8e2c4fe0ecb15f64b69df35db646913b7bdd2`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73cb9933a9869db1cc6fb4636124d96cbfd43111b4b05b820c4e12217bc5b56`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:4d19fbcc0f0bb56e4a6b711398e5de3a634385319d0e8b2bbc0171c109260070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.1 MB (606115637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3374c6411cbaed1bfb06437a6e1edc6a41bd7b83e37ca5ecc6a1aaec09413300`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e2f2830e2003232ca51768518e8eb9e372430ea0c0445d3ec3c8d96672cb8c`  
		Last Modified: Fri, 27 Sep 2024 06:05:25 GMT  
		Size: 214.3 MB (214285718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83748e1ac06a3fcddae1dc3110de6342c4531f82f43779a5fabf89719505db6a`  
		Last Modified: Sat, 28 Sep 2024 05:54:49 GMT  
		Size: 242.7 MB (242735060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:606824019a2d5065cd43eaea75ffe3725a698dd0f28a75d3e050d7cccc157b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15440370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa45a38a900b92dbf585c0410238a0e5b5c4b9b926802c9c7acad6c298aeda8f`

```dockerfile
```

-	Layers:
	-	`sha256:9ab533a7bde3dae7d525cc723b7c2e2eeb5504de5e82bb10f2a6051c078f243c`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 15.4 MB (15427343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c830e1f96c43a12bb0b2d3f79e8307d9635fb3e3532b2762ab339dff8d8738fd`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 13.0 KB (13027 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:0d9fc54c3ca5405db6f5892b2d90b374c38cab322301c88c164cb3d632dcacbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587261517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe66d1e8a70bea815ee500895b94596821696d893861c02b693a4f83ae31166c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1411196315040fbdc5fb36f5519fcdf47619046fa9476d4e7607333bcbd8131`  
		Last Modified: Fri, 27 Sep 2024 03:21:02 GMT  
		Size: 183.3 MB (183287662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35ddee15ec8c9e03e7f842b910c8fd17fe9bfef5ca8c21b7f32fbff8bbcc496`  
		Last Modified: Fri, 27 Sep 2024 17:40:49 GMT  
		Size: 268.5 MB (268487969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:03ac78767400c1d1b9c984acca6bd90df72cac0fb00e9100b2c5a8ee2438346e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15278999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1375e7d3522dd5c1a611790297f685c2fe0704944053af8e43e7d8a89930cc3`

```dockerfile
```

-	Layers:
	-	`sha256:f28e04508e5f7206d96f053f77275ef0c0bb7fa9f8a03c918a24d3fb10588e28`  
		Last Modified: Fri, 27 Sep 2024 17:40:44 GMT  
		Size: 15.3 MB (15266033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1a546a507332436c927687563a98866a316dbc8fab3ac46845bfa34cbe62b1`  
		Last Modified: Fri, 27 Sep 2024 17:40:43 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:8328d21407009f8a2d17b0327f32c63411a8c3d5590b71ab87ea993cd2ffd169
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
$ docker pull rust@sha256:c0c156a4887bdbf6abea8f98258d9d27cfe4c3f2794f674dfb6f5d237de67687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.0 MB (506995658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f511550e16ed987835311ad1d9c0da1b2b1d597b933aed15e44eb452187f9a9b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06817e07ed0f03c17ad0a7aa8ef22b2a6fcf2b939d6212ab0861571ef18a45b`  
		Last Modified: Thu, 17 Oct 2024 01:10:51 GMT  
		Size: 15.8 MB (15764889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173ffc78585eeabe33105e00a7be99b0cad17d5e6edebf7f760d7824fa76969`  
		Last Modified: Thu, 17 Oct 2024 01:11:06 GMT  
		Size: 54.7 MB (54723650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe335f0e34a87e4cbd05c121253490f0c293f8ff29540aa8cd3fc22d4519931`  
		Last Modified: Thu, 17 Oct 2024 01:11:36 GMT  
		Size: 197.1 MB (197085334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66586d4b6a786f40aa4eede68f290dbb5be4152d931746d9bbb17b4b085fcf7`  
		Last Modified: Thu, 17 Oct 2024 02:57:35 GMT  
		Size: 184.3 MB (184341174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7db843194e10c40a284a5f8742a0e692118d3bd1809aa01d16105ab7ec0823ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15063552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c6e3fd4ce8ce97591522bfaf2a495aa59ca89437e220dc586da3fde58d8f0e`

```dockerfile
```

-	Layers:
	-	`sha256:3e0db2ae8efc7a4b906bc15ffdce2bbda5f1c7cbea6015ea958b7c95523d700f`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 15.1 MB (15052438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2033b7ff7e29ef72ea44cc8fe20a94267d7ca6eaded58686e78d093bb6c8ed7f`  
		Last Modified: Thu, 17 Oct 2024 02:57:30 GMT  
		Size: 11.1 KB (11114 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:84331046d2e6bbfe4845d2ef8384cc8281fcbcf0e28fd1071709a3aa34eab212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.8 MB (504758766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d19257130fa88be44790843793cd4e706a1b61733f0e90388b767119ffb2bb`
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
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec523352a6e63a855ebebdbc8288b9cccf719fe4121211d5e0cae3f11e4f6b2`  
		Last Modified: Fri, 27 Sep 2024 07:39:46 GMT  
		Size: 14.9 MB (14879678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bfb8add2d4bda22b21df2a3eff38a6f4f66c2ef9fe110e7714a93f720a4f47`  
		Last Modified: Fri, 27 Sep 2024 07:40:06 GMT  
		Size: 50.6 MB (50618560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f69bcefdc97cf5fabaf3b01d416ce54278fa217058c4433beb68d39a6e1bc1`  
		Last Modified: Fri, 27 Sep 2024 07:40:47 GMT  
		Size: 167.5 MB (167508654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc16697bf56cf2fe7d356c600c48e8a13b2fb6f003a40aec403b77bf1e5a1777`  
		Last Modified: Mon, 07 Oct 2024 20:10:32 GMT  
		Size: 221.5 MB (221511494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3c9b6060fce57e62fb04164d07286dabb9431d2eb979eb665cf468a807fbe9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14864469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873edee47bb20240914debd5c61b9dd61ca27e7d1d73fc95f7657eb67d1419a4`

```dockerfile
```

-	Layers:
	-	`sha256:9e1a11645f7ce0d9026d44c1007e1f6ba2b3f0765e25fa435075743651016034`  
		Last Modified: Mon, 07 Oct 2024 20:10:28 GMT  
		Size: 14.9 MB (14853318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c5c9edc1a5a4d7481d377fa24e5662235f1ce8b366e78cd64a8bc412ee69cb7`  
		Last Modified: Mon, 07 Oct 2024 20:10:27 GMT  
		Size: 11.2 KB (11151 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:230f0887e9953ba599f30462d1601b3af95d1136cf8c1057b77533f0ea13993d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.8 MB (562811378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7fd17cd619497e8cf227bc8f6b6be5a4ceaf9020f09b88694555ccf79d7f65`
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
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4bba36b8add5e5ec5da6aa2c18637b64bce2d5f3f7d83723817e2139a11bcc`  
		Last Modified: Fri, 27 Sep 2024 05:25:50 GMT  
		Size: 15.7 MB (15749698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f212bcfdd3a473cde2991df3e1cf5373d8f097a630557a35fa77d891acce93d6`  
		Last Modified: Fri, 27 Sep 2024 05:26:04 GMT  
		Size: 54.8 MB (54834694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09310330a122777457e6d6b3094e1d1391aa246ba1b028adeb03cd353d0d29`  
		Last Modified: Fri, 27 Sep 2024 05:26:28 GMT  
		Size: 190.0 MB (189964252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da761adc8113e8e908061d91c6af387f04a41e668d2f111540d11a9ef01e5f0`  
		Last Modified: Mon, 07 Oct 2024 20:28:00 GMT  
		Size: 248.5 MB (248528870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f7218307ed60ee81340e8a569d237e241c8e97cac632dc78555ab6083d40909e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15065824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fecd41b23cc4f020e9f319dbf75f1613baa97e283f738646f4a549d49a0a29`

```dockerfile
```

-	Layers:
	-	`sha256:fecaccd039897250aae8a94b1523d4955c0726ff860d9f3a605565fd7b63d201`  
		Last Modified: Mon, 07 Oct 2024 20:27:55 GMT  
		Size: 15.1 MB (15054645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:357925a5449c30f481550c08a6e83d080b7faa1982dfdb43af76649057e41280`  
		Last Modified: Mon, 07 Oct 2024 20:27:54 GMT  
		Size: 11.2 KB (11179 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:0b74763c0c9110dc9342754e733f284101a3090b083abd7c9eb73f9e9162fee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.7 MB (525706874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01cf6a6c0b6626ce6748e3de2ff0182d8febe57f7c55eac503d91d6f9a3e1c7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000ce4e381f50a8f76ae5a1d4bcd9702f5146bac4fb30afc4e12c284ee68ca9`  
		Last Modified: Thu, 17 Oct 2024 01:10:55 GMT  
		Size: 16.3 MB (16268542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d0b1f51e6e34773cde9f3b41201942ff88384d907912b25ff3349f296f69b8`  
		Last Modified: Thu, 17 Oct 2024 01:11:14 GMT  
		Size: 56.0 MB (56032019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b257135cb04b7c9d5ceaf0572a0941a80b7eb3f7dd31444289a12b792e314e8`  
		Last Modified: Thu, 17 Oct 2024 01:12:01 GMT  
		Size: 200.0 MB (199982090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3420ca7067654974fc0f1971890285287aef101e8c0ad81c1d01689969ded4ec`  
		Last Modified: Thu, 17 Oct 2024 02:57:46 GMT  
		Size: 197.3 MB (197346400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f58b08210121da703d98863e10d84097f158a04b4f053e9f579b47a0ecd6819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b309ca17610165025ded60cffba70e585bf2294d8a81fe1ff260572e71d460d`

```dockerfile
```

-	Layers:
	-	`sha256:c660bef212dab636443f1060b4e1e7ca7a48a89cdf8c12a8d6298cf1ed6616f6`  
		Last Modified: Thu, 17 Oct 2024 02:57:42 GMT  
		Size: 15.0 MB (15040975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f6ca99ad4fa67ac8b5d8bd3b23ad2542d63b6634953bb2057d5c3e1a4443b8`  
		Last Modified: Thu, 17 Oct 2024 02:57:42 GMT  
		Size: 11.1 KB (11085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:0757ed8c0609498399dfde17ad6e5ac4adc5da04096fbd3d9c2301c62b93546b
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
$ docker pull rust@sha256:62afc139057dc9d3eda02e490677911b55a208ba22d6f7315f3c5c5851e31a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533623479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3b0145b0fabfa9f7bfc382e163449775329c6b95cb5704237a770a9e6e52a1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5f3b3f727e71a2c8e2d282f958aa488342e7a0edc7c26d994f1dbbb88c88d`  
		Last Modified: Thu, 17 Oct 2024 01:09:47 GMT  
		Size: 24.1 MB (24053088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba0b3d08b81baa192d30dbb2257b8227f2a4eab719c79ef1c419e3a07b39dbc`  
		Last Modified: Thu, 17 Oct 2024 01:10:04 GMT  
		Size: 64.4 MB (64393080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bc85537ac7c401eea9ed38d4a75fddbe5d75d5570921f1c435a8342b3cef15`  
		Last Modified: Thu, 17 Oct 2024 01:10:40 GMT  
		Size: 211.3 MB (211281151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97b348fbebca67b25f027e550f95573ba6aff2f81f748dbf3e11e96d7fc6da6`  
		Last Modified: Thu, 17 Oct 2024 02:57:32 GMT  
		Size: 184.3 MB (184341137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:afd613e0c8388610680d95743ce6b0519e2e288ab2180009d03fdee5263cf66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ce36b1a51263afe43943de85c9d45999d4fd4b9197ac8e48278804e18c1582`

```dockerfile
```

-	Layers:
	-	`sha256:7b956ebc4fdf5bc354458d55f06403a6a7feff6dbe43975c601c444a5d70edc5`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acde1eebb12461b3cf18799768782571274684aa61647d4c0e77a0b7d51d3c40`  
		Last Modified: Thu, 17 Oct 2024 02:57:29 GMT  
		Size: 13.0 KB (13004 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:27b6e9bd919166bac1fb9211e9e52449d5fb725a70122e2280b3f235eef01f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.5 MB (523464584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd1ab1a770c8f7aa48d8b41c6152318ce574fb409b4620f8fea171c3ba763c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea668db82ddd31e7300e905d69bfbcc24fd0c70cd7c7212c915763a9e47f3e7`  
		Last Modified: Fri, 27 Sep 2024 07:39:33 GMT  
		Size: 175.2 MB (175207938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807abecaed8d4cffae0b7d1da027197029821fd16d2bbce8c0f8a1f90fd349f3`  
		Last Modified: Sat, 28 Sep 2024 04:08:11 GMT  
		Size: 221.5 MB (221511519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:ee2cbc5b0aa8369395392c722b55ad9ac0bd4916118b0cdf63d4d0f13269a299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15270591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa74c1d6fa4c9dda9c706f2706450a4b81da24d4559310f49de7e46773f9700`

```dockerfile
```

-	Layers:
	-	`sha256:45c0558bf77c60592fcc61666d1d55c2e8062c13eee2815becd8547e5fe62df5`  
		Last Modified: Sat, 28 Sep 2024 04:08:07 GMT  
		Size: 15.3 MB (15257523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab9e3cff7b672ef6b62a3eecbf1b9c661a226d91214cd3d7b68a9fd5b262ff05`  
		Last Modified: Sat, 28 Sep 2024 04:08:06 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f5fbbf475717a8e1fcfda24fc26c60200eb95e19b03291f3e43e60995a4d406e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.7 MB (588709463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d76e87cace62dbdc9c3a6c3fae1623de64a44b8b274d79b8e95bcd89b6f1e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71ace0e8bbdcfcf795b836e24a37a6ed0054100e14d6aa6e5a63f7e162ba729`  
		Last Modified: Fri, 27 Sep 2024 05:25:40 GMT  
		Size: 202.7 MB (202651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c70a9d34bb788145305c907ff9a5ed64690b67c5abbc4b676ff607611081e0`  
		Last Modified: Fri, 27 Sep 2024 23:30:32 GMT  
		Size: 248.5 MB (248529120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:be6c0d1bdd139e794a093f63bbdcf7c53acbacba5babbcf59b54af8fd37f7cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15494574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23350ebe95ee44b5c009236d86e0a9d13772ae5689fa9c3449fec0987bd7b81d`

```dockerfile
```

-	Layers:
	-	`sha256:7c227d855755631f9fc25b4280c874ce996590e6446ce7c7399e0c496bd31670`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 15.5 MB (15481248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a10530d2c00a615465f62c3a9b01ff478facbfb4d920cbbf7d0d386c559eb44`  
		Last Modified: Fri, 27 Sep 2024 23:30:27 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:cae43437babe4a513bfaf1ebaed7b47e916e1a96bea4496ee763708f2a2b5bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549225958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af64455d7089be15c70fda713c93555e12afb877f65a7b29d2b3dddfab02d1f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9dd8137152c295fb3624be3ee13689c34dc13bc115d0032a5a2a581001f14f`  
		Last Modified: Thu, 17 Oct 2024 01:09:36 GMT  
		Size: 24.9 MB (24895435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbad5c607546fed7ceeb86b3cef161781f7cb90e39cb2c8da1b7774aa73975d4`  
		Last Modified: Thu, 17 Oct 2024 01:09:58 GMT  
		Size: 66.2 MB (66210908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2c0ef7e16c4ea3f5643d06ea746c15f35cca787121e7078904f6a16114c48`  
		Last Modified: Thu, 17 Oct 2024 01:10:44 GMT  
		Size: 210.2 MB (210196330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f818dcff8930802b82fed8fbd3b89feef62a7b69bc64cebb8df64281a6dd9`  
		Last Modified: Thu, 17 Oct 2024 02:57:36 GMT  
		Size: 197.3 MB (197346451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:bc528a75faa20afa57e2c7e4b6f51d9b57b5485d2d379eea44c3bf52d6fbd4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808162f63c550251d4aaa7a5eee4f171d732b78e387b1137976a4a926ec4476c`

```dockerfile
```

-	Layers:
	-	`sha256:cecf68aacf4ab8230e1cd8e54fe8e2c4fe0ecb15f64b69df35db646913b7bdd2`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73cb9933a9869db1cc6fb4636124d96cbfd43111b4b05b820c4e12217bc5b56`  
		Last Modified: Thu, 17 Oct 2024 02:57:31 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:4d19fbcc0f0bb56e4a6b711398e5de3a634385319d0e8b2bbc0171c109260070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.1 MB (606115637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3374c6411cbaed1bfb06437a6e1edc6a41bd7b83e37ca5ecc6a1aaec09413300`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e2f2830e2003232ca51768518e8eb9e372430ea0c0445d3ec3c8d96672cb8c`  
		Last Modified: Fri, 27 Sep 2024 06:05:25 GMT  
		Size: 214.3 MB (214285718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83748e1ac06a3fcddae1dc3110de6342c4531f82f43779a5fabf89719505db6a`  
		Last Modified: Sat, 28 Sep 2024 05:54:49 GMT  
		Size: 242.7 MB (242735060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:606824019a2d5065cd43eaea75ffe3725a698dd0f28a75d3e050d7cccc157b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15440370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa45a38a900b92dbf585c0410238a0e5b5c4b9b926802c9c7acad6c298aeda8f`

```dockerfile
```

-	Layers:
	-	`sha256:9ab533a7bde3dae7d525cc723b7c2e2eeb5504de5e82bb10f2a6051c078f243c`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 15.4 MB (15427343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c830e1f96c43a12bb0b2d3f79e8307d9635fb3e3532b2762ab339dff8d8738fd`  
		Last Modified: Sat, 28 Sep 2024 05:54:43 GMT  
		Size: 13.0 KB (13027 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:0d9fc54c3ca5405db6f5892b2d90b374c38cab322301c88c164cb3d632dcacbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587261517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe66d1e8a70bea815ee500895b94596821696d893861c02b693a4f83ae31166c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1411196315040fbdc5fb36f5519fcdf47619046fa9476d4e7607333bcbd8131`  
		Last Modified: Fri, 27 Sep 2024 03:21:02 GMT  
		Size: 183.3 MB (183287662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35ddee15ec8c9e03e7f842b910c8fd17fe9bfef5ca8c21b7f32fbff8bbcc496`  
		Last Modified: Fri, 27 Sep 2024 17:40:49 GMT  
		Size: 268.5 MB (268487969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:03ac78767400c1d1b9c984acca6bd90df72cac0fb00e9100b2c5a8ee2438346e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15278999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1375e7d3522dd5c1a611790297f685c2fe0704944053af8e43e7d8a89930cc3`

```dockerfile
```

-	Layers:
	-	`sha256:f28e04508e5f7206d96f053f77275ef0c0bb7fa9f8a03c918a24d3fb10588e28`  
		Last Modified: Fri, 27 Sep 2024 17:40:44 GMT  
		Size: 15.3 MB (15266033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1a546a507332436c927687563a98866a316dbc8fab3ac46845bfa34cbe62b1`  
		Last Modified: Fri, 27 Sep 2024 17:40:43 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:5f54e4f0f25ffcb8493d73f38cbd7dd5f6b83ca78d6a33224fc326f6d654d16f
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
$ docker pull rust@sha256:45966c8f3e8348b7643bd40eb846b87015a6f1694ed2a13ca8475c5be35df8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284254306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b63b5bcc9542ec50795afee904fd719f71dbf5f3cd84e74de4c92f7808a727f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0607d7c68e964f9d197627ffe492db8c9ce40d39951ee73a3182e028b0be4e`  
		Last Modified: Thu, 17 Oct 2024 01:30:10 GMT  
		Size: 255.1 MB (255128017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:f17aeca9415c8c8b3eec6d14b5a90f91bbe302ef815e6513d5763f9b1d2b645c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010e722839b0079d58e9aa6bcd3b6446f5bd6702bbfe47fc984b869d24c68e15`

```dockerfile
```

-	Layers:
	-	`sha256:e6e2cf59070156e4177eabcbb570b524e550d23ecba4082cc0876549b6a34458`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78cde42d64af02ec433aba2279aede7b5ce92746174556b598fd74de7abd9517`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 13.1 KB (13090 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:08dbf3d9d24bae232365620c62410ec5d83596ff380aad5f49e27cdec7317513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294070169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e6abf46c4d525890ed87fc173518b54a4bd6a1b01b96fe447fb1d17e08346a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4408bd841243a9a42a8e256c364029c480e1b0b2865b22e70a46bde0100c866`  
		Last Modified: Fri, 27 Sep 2024 18:42:06 GMT  
		Size: 269.4 MB (269352024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:df722b016f3cca3b94348d0bc6f597be00e94961777ca5cb428cf4cdd0af6f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e61fad66437481804743201bd550faf73c0e8846ddb64f6d8bf18e0dff7a4a3`

```dockerfile
```

-	Layers:
	-	`sha256:e090a867d43bfae1fb514bbb85985f7c87fff9bd5a411d0ec1cdcf062ed1c5f1`  
		Last Modified: Fri, 27 Sep 2024 18:42:01 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffb56d93014b97c2bf56f856a3b3c0c1c6de63989a9e8fca173c3abc901f156`  
		Last Modified: Fri, 27 Sep 2024 18:42:00 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3ba3fbf62527788a60c4908b3c389bab7f5ab6fb919ea3c771aeb9a278966253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343526226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233c27109e17c04665f9ed9ede09369aacd1865fc09fd1a6f5ac4863e32fc4a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995fd26d021eddb871651f81a432e2662de3c5b719d2248d4552105c40a67e47`  
		Last Modified: Fri, 27 Sep 2024 23:32:02 GMT  
		Size: 314.4 MB (314369857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:e4a5a923d2e13d83eb71aa2cb933b273577721a70c5ff55a15af8cd5f4d21978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633019f2483a2e86da7ee1384084a836d087aab2347f626c8490a683b80397fc`

```dockerfile
```

-	Layers:
	-	`sha256:45375e55489ffbdb8bd47dbec3eee1f67a6679081f46e4dc1ac6c76ce18b1904`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f968eae71eae982a4adc164da8a72a293dd418f197ba71ede38a68bb18be6c05`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:ba4ee661bb466ab49f6ceb8c6d9e9f9784bba7c6e45225187cd3c7fb1fbc12ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295093589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e4df283163309e2fdaa8101fa73b670d133162155d4cd23424016dd87db8e4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a718584a1346679f83b1655ad2ac313c29bec26411eeb7c34dad2a91b6577448`  
		Last Modified: Thu, 17 Oct 2024 01:30:07 GMT  
		Size: 264.9 MB (264949322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:4c72332e16899bfc022e891c90f0d93e00f555271f92b2e38817f8afa453c722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ca94475147e0318e9bad8ec073ef9dd87fef510c2eed0171a3f48a81c843a`

```dockerfile
```

-	Layers:
	-	`sha256:12434a1e188136de888271297f6eb4670c269905a0833cb0c26866ab817a1eac`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11e3392f42511d72755c775a9cd45fb9f2d612485058889a5a61cbb5dda587f`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 13.0 KB (13043 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:46bcce128e6ab5402c648739e95aa56eb2ed32d840ff42da0975ec8428034ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344618727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4f6cbc6fd8ecc671e77ece602998ab1fa543c11db83d5d64fa6bc051b111c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097a47a9153a9d3d44374a545c87a489f3842a16e291caf5a817ebaa5a0f1552`  
		Last Modified: Sat, 28 Sep 2024 04:15:09 GMT  
		Size: 311.5 MB (311496564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:fa335487319e81174f0920ee7efa014f25d5cdbbfdf8648c77cfeb1f771129bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f51b298cbeb650a1f7674e47e0ff5da39045f7a1c1b12678284013db4153e2`

```dockerfile
```

-	Layers:
	-	`sha256:17e6bf4b03c232f13acb280f35f3b04cad777afeab1156732f6d6e80ae08ac03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9673908047a020854098b5704b6ac719a43c3c5263868a007ef95e1dd656fe03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:1986b817125878c181d9add8424b112238bbcd915e03b3444b6e3b9962a71844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346124228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaf144d0210bf05141bac7875bc21c09171ace17f17693c306e46ee2347cc8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d24393939cc6c4eddc3a49c03d07080edb453591af15f5f40c3481b1c43289`  
		Last Modified: Fri, 27 Sep 2024 17:42:41 GMT  
		Size: 318.6 MB (318634204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:981dce7ac4cd7769d68270976ad41a566057debc664228639318ceeee2878c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb7573b7c4578171c99e4b1c475220bae80fd01a2abcc1ff7de0c789cee9993`

```dockerfile
```

-	Layers:
	-	`sha256:165fd9d1067cb2b20bc1127fb26bf62317d9ec727e17d418b73ad480975a460f`  
		Last Modified: Fri, 27 Sep 2024 17:42:37 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03aa2d5f9daee31ee7485507b38e1a42c341c49bd4f504117c96708fe84908d5`  
		Last Modified: Fri, 27 Sep 2024 17:42:36 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:5f54e4f0f25ffcb8493d73f38cbd7dd5f6b83ca78d6a33224fc326f6d654d16f
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
$ docker pull rust@sha256:45966c8f3e8348b7643bd40eb846b87015a6f1694ed2a13ca8475c5be35df8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284254306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b63b5bcc9542ec50795afee904fd719f71dbf5f3cd84e74de4c92f7808a727f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0607d7c68e964f9d197627ffe492db8c9ce40d39951ee73a3182e028b0be4e`  
		Last Modified: Thu, 17 Oct 2024 01:30:10 GMT  
		Size: 255.1 MB (255128017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f17aeca9415c8c8b3eec6d14b5a90f91bbe302ef815e6513d5763f9b1d2b645c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010e722839b0079d58e9aa6bcd3b6446f5bd6702bbfe47fc984b869d24c68e15`

```dockerfile
```

-	Layers:
	-	`sha256:e6e2cf59070156e4177eabcbb570b524e550d23ecba4082cc0876549b6a34458`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78cde42d64af02ec433aba2279aede7b5ce92746174556b598fd74de7abd9517`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 13.1 KB (13090 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:08dbf3d9d24bae232365620c62410ec5d83596ff380aad5f49e27cdec7317513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294070169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e6abf46c4d525890ed87fc173518b54a4bd6a1b01b96fe447fb1d17e08346a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4408bd841243a9a42a8e256c364029c480e1b0b2865b22e70a46bde0100c866`  
		Last Modified: Fri, 27 Sep 2024 18:42:06 GMT  
		Size: 269.4 MB (269352024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:df722b016f3cca3b94348d0bc6f597be00e94961777ca5cb428cf4cdd0af6f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e61fad66437481804743201bd550faf73c0e8846ddb64f6d8bf18e0dff7a4a3`

```dockerfile
```

-	Layers:
	-	`sha256:e090a867d43bfae1fb514bbb85985f7c87fff9bd5a411d0ec1cdcf062ed1c5f1`  
		Last Modified: Fri, 27 Sep 2024 18:42:01 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffb56d93014b97c2bf56f856a3b3c0c1c6de63989a9e8fca173c3abc901f156`  
		Last Modified: Fri, 27 Sep 2024 18:42:00 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3ba3fbf62527788a60c4908b3c389bab7f5ab6fb919ea3c771aeb9a278966253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343526226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233c27109e17c04665f9ed9ede09369aacd1865fc09fd1a6f5ac4863e32fc4a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995fd26d021eddb871651f81a432e2662de3c5b719d2248d4552105c40a67e47`  
		Last Modified: Fri, 27 Sep 2024 23:32:02 GMT  
		Size: 314.4 MB (314369857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e4a5a923d2e13d83eb71aa2cb933b273577721a70c5ff55a15af8cd5f4d21978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633019f2483a2e86da7ee1384084a836d087aab2347f626c8490a683b80397fc`

```dockerfile
```

-	Layers:
	-	`sha256:45375e55489ffbdb8bd47dbec3eee1f67a6679081f46e4dc1ac6c76ce18b1904`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f968eae71eae982a4adc164da8a72a293dd418f197ba71ede38a68bb18be6c05`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:ba4ee661bb466ab49f6ceb8c6d9e9f9784bba7c6e45225187cd3c7fb1fbc12ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295093589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e4df283163309e2fdaa8101fa73b670d133162155d4cd23424016dd87db8e4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a718584a1346679f83b1655ad2ac313c29bec26411eeb7c34dad2a91b6577448`  
		Last Modified: Thu, 17 Oct 2024 01:30:07 GMT  
		Size: 264.9 MB (264949322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4c72332e16899bfc022e891c90f0d93e00f555271f92b2e38817f8afa453c722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ca94475147e0318e9bad8ec073ef9dd87fef510c2eed0171a3f48a81c843a`

```dockerfile
```

-	Layers:
	-	`sha256:12434a1e188136de888271297f6eb4670c269905a0833cb0c26866ab817a1eac`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11e3392f42511d72755c775a9cd45fb9f2d612485058889a5a61cbb5dda587f`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 13.0 KB (13043 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:46bcce128e6ab5402c648739e95aa56eb2ed32d840ff42da0975ec8428034ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344618727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4f6cbc6fd8ecc671e77ece602998ab1fa543c11db83d5d64fa6bc051b111c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097a47a9153a9d3d44374a545c87a489f3842a16e291caf5a817ebaa5a0f1552`  
		Last Modified: Sat, 28 Sep 2024 04:15:09 GMT  
		Size: 311.5 MB (311496564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:fa335487319e81174f0920ee7efa014f25d5cdbbfdf8648c77cfeb1f771129bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f51b298cbeb650a1f7674e47e0ff5da39045f7a1c1b12678284013db4153e2`

```dockerfile
```

-	Layers:
	-	`sha256:17e6bf4b03c232f13acb280f35f3b04cad777afeab1156732f6d6e80ae08ac03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9673908047a020854098b5704b6ac719a43c3c5263868a007ef95e1dd656fe03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:1986b817125878c181d9add8424b112238bbcd915e03b3444b6e3b9962a71844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346124228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaf144d0210bf05141bac7875bc21c09171ace17f17693c306e46ee2347cc8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d24393939cc6c4eddc3a49c03d07080edb453591af15f5f40c3481b1c43289`  
		Last Modified: Fri, 27 Sep 2024 17:42:41 GMT  
		Size: 318.6 MB (318634204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:981dce7ac4cd7769d68270976ad41a566057debc664228639318ceeee2878c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb7573b7c4578171c99e4b1c475220bae80fd01a2abcc1ff7de0c789cee9993`

```dockerfile
```

-	Layers:
	-	`sha256:165fd9d1067cb2b20bc1127fb26bf62317d9ec727e17d418b73ad480975a460f`  
		Last Modified: Fri, 27 Sep 2024 17:42:37 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03aa2d5f9daee31ee7485507b38e1a42c341c49bd4f504117c96708fe84908d5`  
		Last Modified: Fri, 27 Sep 2024 17:42:36 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:915a4826b6111266e53e06f47c16cddebf36901623f0631f2cc10ce5c26022e5
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
$ docker pull rust@sha256:955e6b161e189ce9a70a3176d62bc853df1d45a8ff2c877bcc2639c1334e05da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275916178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72160f9a4acd420abe48f6f6d762750669ca08d8e16c3612f2aa8e48e6886df1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b38e595cdc330fbe56f1cc54e1fbb521c5c78b889fda1cb2553ec996eb7494`  
		Last Modified: Thu, 17 Oct 2024 01:28:56 GMT  
		Size: 244.5 MB (244487378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:913457ace1ef4de84bcd5852f75e36f52b6ec6cb0381db81b057670c1f7a64c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900b212c9018b48677c88ed0905ec79728757d918f45bb4e41c5f9ac0e6c8a10`

```dockerfile
```

-	Layers:
	-	`sha256:8347c9cf5193ed18506b7d4c96a1dd5a0451c1c9d4c0049fd6c1adaaefe4b7cb`  
		Last Modified: Thu, 17 Oct 2024 01:28:53 GMT  
		Size: 4.2 MB (4164416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee600185d29aecb0803b6cd08dc6117b7080dbec62c710fa35ae4dffc674e387`  
		Last Modified: Thu, 17 Oct 2024 01:28:53 GMT  
		Size: 11.2 KB (11176 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:649f33f2004e7cf32279d259133d1c887680c82371ca61040be0676de14478f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290373521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c1dea15d81a85919b55bae459fdf9865c474d6a3eeded3a426c223d45f15fe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:05 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
# Fri, 27 Sep 2024 05:14:07 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0961dc5030bdc38ffd749a496abefd5f5e3c43706db1ac4fbe6a89b425b6f565`  
		Last Modified: Mon, 07 Oct 2024 20:12:29 GMT  
		Size: 263.8 MB (263784209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0fdedd82265ee4abb67e00cb5ed763bb6b00b1e1a9cff139eb943b524eceddc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3984890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4338ea06da0c03a6090e3a6d0cdfbf4558bd2939605e26dcb73de43f3ae2445a`

```dockerfile
```

-	Layers:
	-	`sha256:ba5dd9365cb77053e5b690af6fb2194be4ea48e4cf45c38343e7917bf11ac2d6`  
		Last Modified: Mon, 07 Oct 2024 20:12:23 GMT  
		Size: 4.0 MB (3973677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71bcc530464af98ed85ff675234211982092c53f113700732ff05ba7b7063828`  
		Last Modified: Mon, 07 Oct 2024 20:12:22 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5a6a01ab245dd0f9c1c5289854e6bfbf41eda63717a403c2ec5715751e29df3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334323993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53157f2dc99d3da88944463c603f1435f567f3e51e835146526d5ddc3602023e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a5b36cf8f1de6f21df811fbf5e9fc34a4a885fdb4d55f5d99d5d38e9e10aa1`  
		Last Modified: Mon, 07 Oct 2024 20:29:36 GMT  
		Size: 304.2 MB (304248835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:117078f67d65fb1fb6692b2e819225b0028efe02b38e50d365a11fb8218ade4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4172348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7528c856c92358d9c7cab5571c3f927091bf38d06d14ae6832f0cdb6a0ea1f`

```dockerfile
```

-	Layers:
	-	`sha256:e585026bbab5521b31de85e6d76a91d424b33a11f16dfc4c480cb11110170e68`  
		Last Modified: Mon, 07 Oct 2024 20:29:28 GMT  
		Size: 4.2 MB (4161108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:115eecb4972db015834bb7865e3b2013bcb5784751739299b04ee1938b1efb82`  
		Last Modified: Mon, 07 Oct 2024 20:29:28 GMT  
		Size: 11.2 KB (11240 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b869a05737d767ce7fb7056cf77751bb5a8b8b577dfbc911a05c94b2d3754822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290535137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a880359cc690264cb0b553f18917849f5c945bc7ff9fea96ceea4696a15d345f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabfbb638063d13147d4f9a1a5694685c92adb5cf15ae94665eae2cd245e5f7a`  
		Last Modified: Thu, 17 Oct 2024 01:29:49 GMT  
		Size: 258.1 MB (258121307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e7bc0dd978b6918b697d54b2322bd89a8fc2364017dc1354c01927066ba886ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c222bd0ec93f4d3719cfa3e3ebd12b938ba155acbede32405b0b9551d71c0e27`

```dockerfile
```

-	Layers:
	-	`sha256:58a6810008287c12bb6320144c20f384550200c86b54ba7c87a2e079a24c5263`  
		Last Modified: Thu, 17 Oct 2024 01:29:43 GMT  
		Size: 4.2 MB (4156184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08b166a715fea1c9ef90fcc577433cc2762aea86d09168615d781dd8d5e38012`  
		Last Modified: Thu, 17 Oct 2024 01:29:43 GMT  
		Size: 11.1 KB (11146 bytes)  
		MIME: application/vnd.in-toto+json
