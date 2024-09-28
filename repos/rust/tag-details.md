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
$ docker pull rust@sha256:a21d54019c66e3a1e7512651e9a7de99b08f28d49b023ed7220b7fe4d3b9f24e
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
$ docker pull rust@sha256:c9c623bcf8dd793e818cb5ee959b1eb431ebb39c044456e265de8e9815923cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533607280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3217a6680ad94a88c6ac0a3f8ce547b5040f8424fdee8578a1a5dfa669ea0c5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01272fe8adbacc44afd2b92994b31c40a151f4324ca392050d9e8d580927dd32`  
		Last Modified: Fri, 27 Sep 2024 05:15:17 GMT  
		Size: 211.3 MB (211265642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6baa1c7db3cf519424e08f89770f4a4f540d4d3effc5816374b37bbea6088f4`  
		Last Modified: Fri, 27 Sep 2024 06:15:59 GMT  
		Size: 184.3 MB (184341215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:1076083cde596f3ad1dadf81b432bd06f0aab7a6a9b26f231ce84664fec63184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3aefab207ffb59f652b7ea32af56dad0ff1cfbe09ac3421b174ea96d620e94`

```dockerfile
```

-	Layers:
	-	`sha256:29234bd63dfb587f9bc295fa626e6ef6b5719b1d8bb8f223aa30280100b48046`  
		Last Modified: Fri, 27 Sep 2024 06:15:57 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93886528e31b3e4bfe0c65731d32a765629c7df70835e6af89927539798d860b`  
		Last Modified: Fri, 27 Sep 2024 06:15:56 GMT  
		Size: 13.0 KB (12966 bytes)  
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
$ docker pull rust@sha256:6a81c71d5a7280b60a2cbdb73f5d4ecec2204329a5825bb0539d2531744f9d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549211767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014da5081bccc9f0142d0399541b0e671db7053e9157944b8538149ea5968c2b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
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
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ace8e3922a39d6cc6947b43fd1d677f246da4946ec81260c978cfd65f84ff1`  
		Last Modified: Fri, 27 Sep 2024 08:07:54 GMT  
		Size: 210.2 MB (210182340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9886795186c272f9016eb0f3875d40d863577d8f0092d46a03e6a4d68f4c4e57`  
		Last Modified: Fri, 27 Sep 2024 09:13:12 GMT  
		Size: 197.3 MB (197346422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:7275a253b7308d840d78872942bf9871c364592b63646148fb770dbb72769473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b73a609b6ed023d27dd5d4919c87729c1a143d1056eea3a8fad7a233443d0`

```dockerfile
```

-	Layers:
	-	`sha256:c71d848a6edb3cf9dec7a47303590462918ae83774d8d334c5d96e745526a5cd`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c9e4a4a6ebdb0fd79ab7fc79a335f0360c02f060e61a2f8436cc9941c6ce824`  
		Last Modified: Fri, 27 Sep 2024 09:13:07 GMT  
		Size: 12.9 KB (12917 bytes)  
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
$ docker pull rust@sha256:a21d54019c66e3a1e7512651e9a7de99b08f28d49b023ed7220b7fe4d3b9f24e
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
$ docker pull rust@sha256:c9c623bcf8dd793e818cb5ee959b1eb431ebb39c044456e265de8e9815923cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533607280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3217a6680ad94a88c6ac0a3f8ce547b5040f8424fdee8578a1a5dfa669ea0c5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01272fe8adbacc44afd2b92994b31c40a151f4324ca392050d9e8d580927dd32`  
		Last Modified: Fri, 27 Sep 2024 05:15:17 GMT  
		Size: 211.3 MB (211265642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6baa1c7db3cf519424e08f89770f4a4f540d4d3effc5816374b37bbea6088f4`  
		Last Modified: Fri, 27 Sep 2024 06:15:59 GMT  
		Size: 184.3 MB (184341215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1076083cde596f3ad1dadf81b432bd06f0aab7a6a9b26f231ce84664fec63184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3aefab207ffb59f652b7ea32af56dad0ff1cfbe09ac3421b174ea96d620e94`

```dockerfile
```

-	Layers:
	-	`sha256:29234bd63dfb587f9bc295fa626e6ef6b5719b1d8bb8f223aa30280100b48046`  
		Last Modified: Fri, 27 Sep 2024 06:15:57 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93886528e31b3e4bfe0c65731d32a765629c7df70835e6af89927539798d860b`  
		Last Modified: Fri, 27 Sep 2024 06:15:56 GMT  
		Size: 13.0 KB (12966 bytes)  
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
$ docker pull rust@sha256:6a81c71d5a7280b60a2cbdb73f5d4ecec2204329a5825bb0539d2531744f9d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549211767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014da5081bccc9f0142d0399541b0e671db7053e9157944b8538149ea5968c2b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
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
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ace8e3922a39d6cc6947b43fd1d677f246da4946ec81260c978cfd65f84ff1`  
		Last Modified: Fri, 27 Sep 2024 08:07:54 GMT  
		Size: 210.2 MB (210182340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9886795186c272f9016eb0f3875d40d863577d8f0092d46a03e6a4d68f4c4e57`  
		Last Modified: Fri, 27 Sep 2024 09:13:12 GMT  
		Size: 197.3 MB (197346422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7275a253b7308d840d78872942bf9871c364592b63646148fb770dbb72769473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b73a609b6ed023d27dd5d4919c87729c1a143d1056eea3a8fad7a233443d0`

```dockerfile
```

-	Layers:
	-	`sha256:c71d848a6edb3cf9dec7a47303590462918ae83774d8d334c5d96e745526a5cd`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c9e4a4a6ebdb0fd79ab7fc79a335f0360c02f060e61a2f8436cc9941c6ce824`  
		Last Modified: Fri, 27 Sep 2024 09:13:07 GMT  
		Size: 12.9 KB (12917 bytes)  
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
$ docker pull rust@sha256:0deb626fc05b074fc9b1453b007f92f0bec72c219e42a4a89b9b0d17201acb76
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

### `rust:1-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:f3c124d37b50b9c2b925843e96853ddc5b271046f32e1a4585aaedb6d106fdfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.0 MB (506979504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2ad98c9cf3eb39c4e66e283d192af97be03939340aca6181ad4c5c3daf8407`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21912b76607d1849ada521d53cc1be42bcc38d6583bd385a1bbd91babc6745f8`  
		Last Modified: Fri, 27 Sep 2024 05:15:27 GMT  
		Size: 15.8 MB (15764314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee27f1f94c19451b787e3a7d81f5eefbd7aed799349b4208bb04c1ce8880ccb2`  
		Last Modified: Fri, 27 Sep 2024 05:15:42 GMT  
		Size: 54.7 MB (54723654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a7fe5b36fbd67e153a5a6e8ec36c41c1fb931871662835b9abdd59e785fdb`  
		Last Modified: Fri, 27 Sep 2024 05:16:13 GMT  
		Size: 197.1 MB (197069002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c01ccb0aa52be675b92db0d8d0a7427b19445393029774c3c0fd52a324ff7ef`  
		Last Modified: Fri, 27 Sep 2024 06:16:04 GMT  
		Size: 184.3 MB (184341143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1972d424605b6c782ff0125e35c9eb029fb848de01dd4c5491dac5f38c06b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15064079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9a516196d12bb4d8d59608d0c44eb8b81491de22e6677a8dffbfe111bc3b08`

```dockerfile
```

-	Layers:
	-	`sha256:08741ee5e60d3fb87158bf15775e81b86ad4e06d851901d96b8493d3a1fe3ae0`  
		Last Modified: Fri, 27 Sep 2024 06:15:59 GMT  
		Size: 15.1 MB (15052276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:284b3427a93dbccf350467e9bf85c30cc857b3577a89a2b74dbbd2f0365830dd`  
		Last Modified: Fri, 27 Sep 2024 06:15:58 GMT  
		Size: 11.8 KB (11803 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:b276289647ff0aa629a2242b7f79691c5d9bc03ce73b687bb1440c28ad758bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.8 MB (504758546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b591737dedb5f1f7a1a7897835fbabfb6f387d7a0a233ace06964c8d2147b6bc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:c11b754156d52a292b4c2c82c7274bcdf02e2227709cc1a95025ac1512f5606f`  
		Last Modified: Sat, 28 Sep 2024 04:05:55 GMT  
		Size: 221.5 MB (221511274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d5eefeb3cf62dbd2e0294249ea58b6561ddcace71024582033bec2dced6cbba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14865192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5655e29fc00720432f5d238188a9c05e32a8c376d4803f4a0936c499ee3c91`

```dockerfile
```

-	Layers:
	-	`sha256:72c0500bc9617296f733c1557727b920ed9eed4fb7299ab1ce45b6d5ac424300`  
		Last Modified: Sat, 28 Sep 2024 04:05:50 GMT  
		Size: 14.9 MB (14853318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd4e6e657b9a9c6c5284dfec262fe343ce34100fc6be3d583217a9ccd52152ba`  
		Last Modified: Sat, 28 Sep 2024 04:05:49 GMT  
		Size: 11.9 KB (11874 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c3220040b0838a88b6b883a9bf4e252f6fe1aebba16a7189f08f45dbbee2487e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.8 MB (562811651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b925555db69a651d8e0f86e0f3b61195002c8eff0f5273dc4f50a5d43259dbab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:28c55e14a5fe2e5b9ec4f6f52d2b18f6cdda1baaa40243032acd71cbec4885e4`  
		Last Modified: Fri, 27 Sep 2024 23:27:39 GMT  
		Size: 248.5 MB (248529143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5c0c3ffcbae775ac2c9d7d87ac40bed3435a9bf507954fc22eb497d1c738fff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15066760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe42b10da972265beb8d1ea0da742b211a1298b6594a326081dbace555b12f27`

```dockerfile
```

-	Layers:
	-	`sha256:e2ea1e6cdae9a39aa1649c64168862704ec2af8be6988eb21f25b2a6dd212b85`  
		Last Modified: Fri, 27 Sep 2024 23:27:34 GMT  
		Size: 15.1 MB (15054645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d615fae986037c7de77864eb2b29aa110afaf379cd1264a912b02e7108bcf6d`  
		Last Modified: Fri, 27 Sep 2024 23:27:33 GMT  
		Size: 12.1 KB (12115 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:60c4afbe289a62aad63648c47790392011269f3ae812a7d03bc400333a68d836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.7 MB (525690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29ab444f2a7d9d62e8c0f1a19211d1d5fab3bbb9fe96cf8180b506d9aacb447`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614d8f32e100154b6cafdcf65ece0dbebfe80d8db1ef99ba3702f31f7e7492e8`  
		Last Modified: Fri, 27 Sep 2024 08:08:06 GMT  
		Size: 16.3 MB (16268079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59b47d19029f8522ed8e76f9d6f0e20d6e64ca4b0ec6b83c92cf0dcf4da57d4`  
		Last Modified: Fri, 27 Sep 2024 08:08:26 GMT  
		Size: 56.0 MB (56032289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93938e3248ca49e16485c4e39a8c601801fe32600e913ea08b6a71a42acd7759`  
		Last Modified: Fri, 27 Sep 2024 08:09:12 GMT  
		Size: 200.0 MB (199967470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6391bdc2b9692c19124977c7fb363bad97af929c403e77ac057e11aabc39ef7b`  
		Last Modified: Fri, 27 Sep 2024 09:12:45 GMT  
		Size: 197.3 MB (197346342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f07059339d02bf5f5deb1c3c9a9a678263144cadab6849d30ce7c1cb4b5c7bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a0a3e870e2c059fa54a70bf5c42e7f7da0289a021318006532ec5983512963`

```dockerfile
```

-	Layers:
	-	`sha256:ef0c21cfe2c931dc8fca5bc73db3fd7ddde0af5bc3c73c116a05f8ecb6a42c09`  
		Last Modified: Fri, 27 Sep 2024 09:12:40 GMT  
		Size: 15.0 MB (15040813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caeb82e791023136ba0d5372d24967e5b37b91950f985476225f277413ce379d`  
		Last Modified: Fri, 27 Sep 2024 09:12:40 GMT  
		Size: 11.8 KB (11775 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:6986d4ab9271f5504e3b561e66e2db6e40fb8dde4c8262994604db3acd937db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.7 MB (573737346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d444768bce4ae6afc8b0de2725d811c5c35d512be053c6036e77a60f78a7230`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:af2c25052aab46bab5ee70bf1b7f7c8d0339d147a2bd4daeb04ec25bd34e4799 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a8e5e0425eb7845f41056f6e5fe36c228a23a602de31f39d88868def2b2bf980`  
		Last Modified: Wed, 04 Sep 2024 22:30:31 GMT  
		Size: 59.0 MB (58950090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e76b45808a7b15592738cc59f261bb4109d1d280c5fa410f157dd270ddbf8c9`  
		Last Modified: Wed, 04 Sep 2024 23:14:50 GMT  
		Size: 16.8 MB (16766250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb7a5e65d3cbab78e31accfce79b09855b78c5b547ef6a738d98e4678a2af87`  
		Last Modified: Wed, 04 Sep 2024 23:15:06 GMT  
		Size: 58.9 MB (58872541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49975637c562cd117e86d9b35bd61ab045430938723115feadf0b276d917f54`  
		Last Modified: Wed, 04 Sep 2024 23:15:41 GMT  
		Size: 196.4 MB (196413350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4e72548af0663df3a67047671a227ceb818fd743ec005c3e0c26dba1196fa7`  
		Last Modified: Thu, 05 Sep 2024 23:37:33 GMT  
		Size: 242.7 MB (242735115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:18d2607644bfca8d172785ef824024a2587bbcd7e039c160e48e95881e76d361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15031565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3addc400c2a717f18c43ccd08b90ace573132a4d8be14ccabd100f3b5e3e79e3`

```dockerfile
```

-	Layers:
	-	`sha256:f7e53895621c513771d001c28dbc076ad0911acfcf791f76b496be0d3c03c00a`  
		Last Modified: Thu, 05 Sep 2024 23:37:26 GMT  
		Size: 15.0 MB (15019723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee700960b0d4111e9120391d7ac3ff153661a00f521840d83e2ded13f2ee5cb`  
		Last Modified: Thu, 05 Sep 2024 23:37:23 GMT  
		Size: 11.8 KB (11842 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:e994862cc3338753c10e48a809a5727a3e1766320405aad3b6bc6b2b99588710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564570515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597e9c037660824a854cb08d0af1ebfb2e150b6f43e618bd8f45cdbf4ed44fa2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:855e3f68f57762c16941f4426d4c9911e4dcaf77abfb6d1993bd8c8f0d7e83b5 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:52560ec7a98b7f8127e927ecee98fe2d97be23a6a2ec8ffbbb0b71455e06dc54`  
		Last Modified: Wed, 04 Sep 2024 21:47:54 GMT  
		Size: 53.3 MB (53317200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deb07fb0f47d9daa6d0bf809dee66d9c90207821b4a8f6c849f8287efdda0fd`  
		Last Modified: Thu, 05 Sep 2024 00:00:53 GMT  
		Size: 15.6 MB (15642390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed93d5f01b376419cd54d2ce3b7abf1bb4ab16f8c188ed6e0bca4959d860c9e`  
		Last Modified: Thu, 05 Sep 2024 00:01:05 GMT  
		Size: 54.1 MB (54075084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819f8402428b6e76aa2474a2ad7b60bda05d2333b58c0ce2e044e6474eb477b3`  
		Last Modified: Thu, 05 Sep 2024 00:01:31 GMT  
		Size: 173.0 MB (173047915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928cd4be8f5c53da1abdc68e27bdc267586b2236cb685b7ac9411f8178a4e9c9`  
		Last Modified: Fri, 06 Sep 2024 03:48:36 GMT  
		Size: 268.5 MB (268487926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:060a7d7485d2b2136c69bad068f873973ca97c522af1da4d6a695691c830ed1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4aff1b5e2666120285959b2a32028ace5129a7c6ff9db899af0b68480eae04`

```dockerfile
```

-	Layers:
	-	`sha256:46ebae515231e7a0d42d05c17b4a42e37ca8587225e58ba27697967fb36bce99`  
		Last Modified: Fri, 06 Sep 2024 03:48:31 GMT  
		Size: 14.9 MB (14873217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58aff1056b597cab684a0715c700502ce479d4df587d8a5f4cd6c7de0d2ff53`  
		Last Modified: Fri, 06 Sep 2024 03:48:31 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:948b2b7413d0c9797581db9dc847e8ef49ff30f9edad108058f35f2829094892
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
$ docker pull rust@sha256:e1a7feeb1ede7988cd98bf29fe12658840962a6698fe7648b1d963911c3652f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284251390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb403fd1b9b464461b4572eb4f7b18b2b6881e31158e7b81255da64a67163b56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fbc8922a73fa72fbbbda7d3faf1d5d10a8eff36091c5173e584d9a215891bf`  
		Last Modified: Fri, 27 Sep 2024 06:15:51 GMT  
		Size: 255.1 MB (255125114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:ac727fe37fea34e145bfff9e75b51e85a802c0d063767fa3e6df994ea1da8e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eead885a9da4703238deeb48abba86d35cdcc283f04146b1c9f6111cbab3ae`

```dockerfile
```

-	Layers:
	-	`sha256:5b300e89b5db1b6f79b8095863c2a61a2cb3f710fb2261c2eed2be59b4e48e67`  
		Last Modified: Fri, 27 Sep 2024 06:15:48 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c85b7e53d6fadcbec1e983cf20f845447156dd1164dbe7c43f291d3dd90d52`  
		Last Modified: Fri, 27 Sep 2024 06:15:47 GMT  
		Size: 13.1 KB (13054 bytes)  
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
$ docker pull rust@sha256:ee4a58c7b9ba278c5e9dc04d77c9581a695f1e0ffe81bb13096f2fad7ef43351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295092776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0734af6dfbf06fc900b5026c3e972c1d3611cb78cfe967484986f62297ee84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7597026bf36d7da868af0b6530f3e00d5c1d9f0facf729ac27ef8c053adf3e1`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 264.9 MB (264948560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:8e14a2c4857d8c4ad5a32a3614385588fdb73ad679e464988be2f9c259d07197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de2d55084645c72d82f718d0dfe3ffba574c2a849e89f88ab2760fe6bdf995c`

```dockerfile
```

-	Layers:
	-	`sha256:25fd4c3a5d5a7e1153c978571285a580167caf9ad7360d57fbb518357e01f516`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb37db2d7c06eba4dc179767f03593cae639be850cf9e9fb8dfad5d91cc796b0`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 13.0 KB (13005 bytes)  
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
$ docker pull rust@sha256:948b2b7413d0c9797581db9dc847e8ef49ff30f9edad108058f35f2829094892
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
$ docker pull rust@sha256:e1a7feeb1ede7988cd98bf29fe12658840962a6698fe7648b1d963911c3652f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284251390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb403fd1b9b464461b4572eb4f7b18b2b6881e31158e7b81255da64a67163b56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fbc8922a73fa72fbbbda7d3faf1d5d10a8eff36091c5173e584d9a215891bf`  
		Last Modified: Fri, 27 Sep 2024 06:15:51 GMT  
		Size: 255.1 MB (255125114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ac727fe37fea34e145bfff9e75b51e85a802c0d063767fa3e6df994ea1da8e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eead885a9da4703238deeb48abba86d35cdcc283f04146b1c9f6111cbab3ae`

```dockerfile
```

-	Layers:
	-	`sha256:5b300e89b5db1b6f79b8095863c2a61a2cb3f710fb2261c2eed2be59b4e48e67`  
		Last Modified: Fri, 27 Sep 2024 06:15:48 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c85b7e53d6fadcbec1e983cf20f845447156dd1164dbe7c43f291d3dd90d52`  
		Last Modified: Fri, 27 Sep 2024 06:15:47 GMT  
		Size: 13.1 KB (13054 bytes)  
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
$ docker pull rust@sha256:ee4a58c7b9ba278c5e9dc04d77c9581a695f1e0ffe81bb13096f2fad7ef43351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295092776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0734af6dfbf06fc900b5026c3e972c1d3611cb78cfe967484986f62297ee84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7597026bf36d7da868af0b6530f3e00d5c1d9f0facf729ac27ef8c053adf3e1`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 264.9 MB (264948560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8e14a2c4857d8c4ad5a32a3614385588fdb73ad679e464988be2f9c259d07197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de2d55084645c72d82f718d0dfe3ffba574c2a849e89f88ab2760fe6bdf995c`

```dockerfile
```

-	Layers:
	-	`sha256:25fd4c3a5d5a7e1153c978571285a580167caf9ad7360d57fbb518357e01f516`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb37db2d7c06eba4dc179767f03593cae639be850cf9e9fb8dfad5d91cc796b0`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 13.0 KB (13005 bytes)  
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
$ docker pull rust@sha256:60fd98e4f6b0cc14964d74edf0dc884e101945b4a1e2eaa7112daeb1d84619ff
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

### `rust:1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:c867715387d7363cf3c30c26381179f4f1e804b0d1b9969a7f852492baee90af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275916206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346d4256eb653e635cafc15d8f7282998e29ebc76b694c88da73dfe837097889`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbabb339956394a4d1fb91746cbf4761db1e54d54c9c5e487b98fcf4c45cbcd4`  
		Last Modified: Fri, 27 Sep 2024 06:16:02 GMT  
		Size: 244.5 MB (244487607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7eef46d1dcd0e823fe875b24a70e9c1355467596a38ef031ad7e418154f6eadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77a7207310f10b7ec7217d47abd395d9718820083b43ce51cb4041c02a16bf3`

```dockerfile
```

-	Layers:
	-	`sha256:85b3a79d5c46bef73c9bf9973e5ea4e1e6aaf43fb04f7e447dd70d19e6c88e7d`  
		Last Modified: Fri, 27 Sep 2024 06:15:56 GMT  
		Size: 4.2 MB (4164326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:279917aa77c9e1c40758a70e6573a49f3034cc50f5fc41b515a40385f1474e14`  
		Last Modified: Fri, 27 Sep 2024 06:15:55 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:3864eae3b065e3d81344c823dac118246b84efe418da96c127369a00cabda4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290373786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9b68951fcca1c7239656abb516436a845f49303a3f76720ba86529f4354960`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
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
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d8db63bffbb27f6b6ed74cd77d5b4f7ec42191a0b2475d68e5ed27105e592`  
		Last Modified: Fri, 27 Sep 2024 18:40:15 GMT  
		Size: 263.8 MB (263784474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:22f04e7c807cb8bdfe6269815eea5164f572c016ffda5eff59c755f41b9e068a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db454d62ef28a3c82390e251029f25d9893fea65a0925e74c81ea8c398f57d6c`

```dockerfile
```

-	Layers:
	-	`sha256:b3e4a96099f809c0ddb915f77a34b6f9fdd86737ab496c9ab79c156985b041ca`  
		Last Modified: Fri, 27 Sep 2024 18:40:09 GMT  
		Size: 4.0 MB (3973677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b966f43de96afeec4ba17d293fdc44b0a83a5a9968b85b27ec70e25a553a7eb9`  
		Last Modified: Fri, 27 Sep 2024 18:40:09 GMT  
		Size: 11.9 KB (11935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:480535d160c76a5e638040c70225a8e4d121ea028634b5d263620b58ec413a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334323357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45f260f195927f8cd55d4504b96e3434ec5bd092287a3c5868e42073e53450c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3631b207c7c399be644b042eeb8fbb3ac0c51b3397c2168d0161b1553ad076`  
		Last Modified: Fri, 27 Sep 2024 23:29:07 GMT  
		Size: 304.2 MB (304248199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e3b945e7be780f647d3eb32426bba0ba0f2add9a1bf28958cd7e4eb58155bb39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae3f54d0f5b7eb56a28900316f0b957c0b9576eb1a7024048541ca4b22d7792`

```dockerfile
```

-	Layers:
	-	`sha256:7a476c013b6e8b15084c2821b389d6d1231c10bcddfae752cdf10e7dc4554fe6`  
		Last Modified: Fri, 27 Sep 2024 23:29:01 GMT  
		Size: 4.2 MB (4161108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd5a81733b89782f55f77276aef546505e1ee78ab6888343370f870cf595bbc`  
		Last Modified: Fri, 27 Sep 2024 23:29:00 GMT  
		Size: 12.2 KB (12174 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:370149bebadd4b8a584b3d980b8a5ad01ea5406d2a144002c1866061a08fb2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290534147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c84b20cb0ea15828268c7aad29217666b9d53c3b8919c0e2439fcc40278e47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:176ca55c782e88e529d56f56999487b261e37eaa9b59fcfdf2b400ed60a31a55 in / 
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
	-	`sha256:5306a3a8e6d3817e237e681e3f75f332f8a6ba35c1f365dcff9af549d9f45234`  
		Last Modified: Fri, 27 Sep 2024 07:27:50 GMT  
		Size: 32.4 MB (32413499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e12102af9e460ec4e1bebb62ca4f08dc362023b60123469c376da657d9b6f6a`  
		Last Modified: Fri, 27 Sep 2024 09:12:29 GMT  
		Size: 258.1 MB (258120648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6a2abce60a26598af546287b011c7faabf8c4d7431dd39bf5384c1f6933c1592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd5f9c55110a73c479ef96a72e9ed6c4006bfb5cfd0a4c6c9c07e46bf125967`

```dockerfile
```

-	Layers:
	-	`sha256:f8d0de040f64ccaa948a96733126b0c90c2aa3dff35fcbb9cc21778cd3492d31`  
		Last Modified: Fri, 27 Sep 2024 09:12:22 GMT  
		Size: 4.2 MB (4156094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f87ed75714693f89afb0d8ec96eef215d07388367b7b45eb91149f838bb01e9`  
		Last Modified: Fri, 27 Sep 2024 09:12:22 GMT  
		Size: 11.8 KB (11835 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:8decec112addbd13695a85c3e36cfb3cb2234d665990d6f69a9bebfb0bbc1cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.0 MB (333036407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0333435dde12c12f5b045e83da42c26356268ad32349b2de967ad73018c3f85a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
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
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef013636d6b4779de60a6daee7eb6d85444109ea750ff43367edc3b44048045`  
		Last Modified: Thu, 05 Sep 2024 23:39:59 GMT  
		Size: 297.7 MB (297737133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:656e87dfd5b323b3534529ebb6d0988156203604648266168165a837d1ef6dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5059fbdba445f288b2849f55639287d8333cc7655e843b9fbe7c85020c224d`

```dockerfile
```

-	Layers:
	-	`sha256:d25bcba9a065f355cde74f818a97e486db851e80f67a0a407d235d79d3ade18f`  
		Last Modified: Thu, 05 Sep 2024 23:39:43 GMT  
		Size: 4.1 MB (4125251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d6c5709ca112dc1e234b9723a7a09ca1019d006a2afcc4412640d98e4fea32`  
		Last Modified: Thu, 05 Sep 2024 23:39:42 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:f1a0949c9448b312796a4aec2d6154e999eb2f96afe929b603a213508841435c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340544165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de8960b7a01ddb04ba5bfd4bfb32db85f2897b897dd86ec4323b2621f22f4f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
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
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306069be260e0429366a2595212c3875058050805ba1b96aeea8dab379bb2415`  
		Last Modified: Fri, 06 Sep 2024 03:50:36 GMT  
		Size: 310.9 MB (310880718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f155f0ff66d7853629c893ae2d504e8682516a9b70a7cd93d5a8908014def30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c44c2520b53671c6568b4dd36d9c48258d46aa1996934dc922e3db2e6f40e4`

```dockerfile
```

-	Layers:
	-	`sha256:5f3a48f9f2e94610235d8c5b94113c04789bc2d5645daf17048ffe8910ba4b8f`  
		Last Modified: Fri, 06 Sep 2024 03:50:33 GMT  
		Size: 4.0 MB (3996088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69bbabadfe35e88452c9b6e7c9598c0207c7f8a45727e3d37f9cadf57d18f76c`  
		Last Modified: Fri, 06 Sep 2024 03:50:32 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81`

```console
$ docker pull rust@sha256:a21d54019c66e3a1e7512651e9a7de99b08f28d49b023ed7220b7fe4d3b9f24e
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
$ docker pull rust@sha256:c9c623bcf8dd793e818cb5ee959b1eb431ebb39c044456e265de8e9815923cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533607280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3217a6680ad94a88c6ac0a3f8ce547b5040f8424fdee8578a1a5dfa669ea0c5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01272fe8adbacc44afd2b92994b31c40a151f4324ca392050d9e8d580927dd32`  
		Last Modified: Fri, 27 Sep 2024 05:15:17 GMT  
		Size: 211.3 MB (211265642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6baa1c7db3cf519424e08f89770f4a4f540d4d3effc5816374b37bbea6088f4`  
		Last Modified: Fri, 27 Sep 2024 06:15:59 GMT  
		Size: 184.3 MB (184341215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81` - unknown; unknown

```console
$ docker pull rust@sha256:1076083cde596f3ad1dadf81b432bd06f0aab7a6a9b26f231ce84664fec63184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3aefab207ffb59f652b7ea32af56dad0ff1cfbe09ac3421b174ea96d620e94`

```dockerfile
```

-	Layers:
	-	`sha256:29234bd63dfb587f9bc295fa626e6ef6b5719b1d8bb8f223aa30280100b48046`  
		Last Modified: Fri, 27 Sep 2024 06:15:57 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93886528e31b3e4bfe0c65731d32a765629c7df70835e6af89927539798d860b`  
		Last Modified: Fri, 27 Sep 2024 06:15:56 GMT  
		Size: 13.0 KB (12966 bytes)  
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
$ docker pull rust@sha256:6a81c71d5a7280b60a2cbdb73f5d4ecec2204329a5825bb0539d2531744f9d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549211767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014da5081bccc9f0142d0399541b0e671db7053e9157944b8538149ea5968c2b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
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
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ace8e3922a39d6cc6947b43fd1d677f246da4946ec81260c978cfd65f84ff1`  
		Last Modified: Fri, 27 Sep 2024 08:07:54 GMT  
		Size: 210.2 MB (210182340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9886795186c272f9016eb0f3875d40d863577d8f0092d46a03e6a4d68f4c4e57`  
		Last Modified: Fri, 27 Sep 2024 09:13:12 GMT  
		Size: 197.3 MB (197346422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81` - unknown; unknown

```console
$ docker pull rust@sha256:7275a253b7308d840d78872942bf9871c364592b63646148fb770dbb72769473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b73a609b6ed023d27dd5d4919c87729c1a143d1056eea3a8fad7a233443d0`

```dockerfile
```

-	Layers:
	-	`sha256:c71d848a6edb3cf9dec7a47303590462918ae83774d8d334c5d96e745526a5cd`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c9e4a4a6ebdb0fd79ab7fc79a335f0360c02f060e61a2f8436cc9941c6ce824`  
		Last Modified: Fri, 27 Sep 2024 09:13:07 GMT  
		Size: 12.9 KB (12917 bytes)  
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
$ docker pull rust@sha256:a21d54019c66e3a1e7512651e9a7de99b08f28d49b023ed7220b7fe4d3b9f24e
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
$ docker pull rust@sha256:c9c623bcf8dd793e818cb5ee959b1eb431ebb39c044456e265de8e9815923cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533607280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3217a6680ad94a88c6ac0a3f8ce547b5040f8424fdee8578a1a5dfa669ea0c5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01272fe8adbacc44afd2b92994b31c40a151f4324ca392050d9e8d580927dd32`  
		Last Modified: Fri, 27 Sep 2024 05:15:17 GMT  
		Size: 211.3 MB (211265642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6baa1c7db3cf519424e08f89770f4a4f540d4d3effc5816374b37bbea6088f4`  
		Last Modified: Fri, 27 Sep 2024 06:15:59 GMT  
		Size: 184.3 MB (184341215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1076083cde596f3ad1dadf81b432bd06f0aab7a6a9b26f231ce84664fec63184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3aefab207ffb59f652b7ea32af56dad0ff1cfbe09ac3421b174ea96d620e94`

```dockerfile
```

-	Layers:
	-	`sha256:29234bd63dfb587f9bc295fa626e6ef6b5719b1d8bb8f223aa30280100b48046`  
		Last Modified: Fri, 27 Sep 2024 06:15:57 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93886528e31b3e4bfe0c65731d32a765629c7df70835e6af89927539798d860b`  
		Last Modified: Fri, 27 Sep 2024 06:15:56 GMT  
		Size: 13.0 KB (12966 bytes)  
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
$ docker pull rust@sha256:6a81c71d5a7280b60a2cbdb73f5d4ecec2204329a5825bb0539d2531744f9d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549211767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014da5081bccc9f0142d0399541b0e671db7053e9157944b8538149ea5968c2b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
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
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ace8e3922a39d6cc6947b43fd1d677f246da4946ec81260c978cfd65f84ff1`  
		Last Modified: Fri, 27 Sep 2024 08:07:54 GMT  
		Size: 210.2 MB (210182340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9886795186c272f9016eb0f3875d40d863577d8f0092d46a03e6a4d68f4c4e57`  
		Last Modified: Fri, 27 Sep 2024 09:13:12 GMT  
		Size: 197.3 MB (197346422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7275a253b7308d840d78872942bf9871c364592b63646148fb770dbb72769473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b73a609b6ed023d27dd5d4919c87729c1a143d1056eea3a8fad7a233443d0`

```dockerfile
```

-	Layers:
	-	`sha256:c71d848a6edb3cf9dec7a47303590462918ae83774d8d334c5d96e745526a5cd`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c9e4a4a6ebdb0fd79ab7fc79a335f0360c02f060e61a2f8436cc9941c6ce824`  
		Last Modified: Fri, 27 Sep 2024 09:13:07 GMT  
		Size: 12.9 KB (12917 bytes)  
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
$ docker pull rust@sha256:0deb626fc05b074fc9b1453b007f92f0bec72c219e42a4a89b9b0d17201acb76
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

### `rust:1.81-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:f3c124d37b50b9c2b925843e96853ddc5b271046f32e1a4585aaedb6d106fdfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.0 MB (506979504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2ad98c9cf3eb39c4e66e283d192af97be03939340aca6181ad4c5c3daf8407`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21912b76607d1849ada521d53cc1be42bcc38d6583bd385a1bbd91babc6745f8`  
		Last Modified: Fri, 27 Sep 2024 05:15:27 GMT  
		Size: 15.8 MB (15764314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee27f1f94c19451b787e3a7d81f5eefbd7aed799349b4208bb04c1ce8880ccb2`  
		Last Modified: Fri, 27 Sep 2024 05:15:42 GMT  
		Size: 54.7 MB (54723654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a7fe5b36fbd67e153a5a6e8ec36c41c1fb931871662835b9abdd59e785fdb`  
		Last Modified: Fri, 27 Sep 2024 05:16:13 GMT  
		Size: 197.1 MB (197069002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c01ccb0aa52be675b92db0d8d0a7427b19445393029774c3c0fd52a324ff7ef`  
		Last Modified: Fri, 27 Sep 2024 06:16:04 GMT  
		Size: 184.3 MB (184341143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1972d424605b6c782ff0125e35c9eb029fb848de01dd4c5491dac5f38c06b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15064079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9a516196d12bb4d8d59608d0c44eb8b81491de22e6677a8dffbfe111bc3b08`

```dockerfile
```

-	Layers:
	-	`sha256:08741ee5e60d3fb87158bf15775e81b86ad4e06d851901d96b8493d3a1fe3ae0`  
		Last Modified: Fri, 27 Sep 2024 06:15:59 GMT  
		Size: 15.1 MB (15052276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:284b3427a93dbccf350467e9bf85c30cc857b3577a89a2b74dbbd2f0365830dd`  
		Last Modified: Fri, 27 Sep 2024 06:15:58 GMT  
		Size: 11.8 KB (11803 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:b276289647ff0aa629a2242b7f79691c5d9bc03ce73b687bb1440c28ad758bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.8 MB (504758546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b591737dedb5f1f7a1a7897835fbabfb6f387d7a0a233ace06964c8d2147b6bc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:c11b754156d52a292b4c2c82c7274bcdf02e2227709cc1a95025ac1512f5606f`  
		Last Modified: Sat, 28 Sep 2024 04:05:55 GMT  
		Size: 221.5 MB (221511274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d5eefeb3cf62dbd2e0294249ea58b6561ddcace71024582033bec2dced6cbba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14865192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5655e29fc00720432f5d238188a9c05e32a8c376d4803f4a0936c499ee3c91`

```dockerfile
```

-	Layers:
	-	`sha256:72c0500bc9617296f733c1557727b920ed9eed4fb7299ab1ce45b6d5ac424300`  
		Last Modified: Sat, 28 Sep 2024 04:05:50 GMT  
		Size: 14.9 MB (14853318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd4e6e657b9a9c6c5284dfec262fe343ce34100fc6be3d583217a9ccd52152ba`  
		Last Modified: Sat, 28 Sep 2024 04:05:49 GMT  
		Size: 11.9 KB (11874 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c3220040b0838a88b6b883a9bf4e252f6fe1aebba16a7189f08f45dbbee2487e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.8 MB (562811651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b925555db69a651d8e0f86e0f3b61195002c8eff0f5273dc4f50a5d43259dbab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:28c55e14a5fe2e5b9ec4f6f52d2b18f6cdda1baaa40243032acd71cbec4885e4`  
		Last Modified: Fri, 27 Sep 2024 23:27:39 GMT  
		Size: 248.5 MB (248529143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5c0c3ffcbae775ac2c9d7d87ac40bed3435a9bf507954fc22eb497d1c738fff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15066760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe42b10da972265beb8d1ea0da742b211a1298b6594a326081dbace555b12f27`

```dockerfile
```

-	Layers:
	-	`sha256:e2ea1e6cdae9a39aa1649c64168862704ec2af8be6988eb21f25b2a6dd212b85`  
		Last Modified: Fri, 27 Sep 2024 23:27:34 GMT  
		Size: 15.1 MB (15054645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d615fae986037c7de77864eb2b29aa110afaf379cd1264a912b02e7108bcf6d`  
		Last Modified: Fri, 27 Sep 2024 23:27:33 GMT  
		Size: 12.1 KB (12115 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-bullseye` - linux; 386

```console
$ docker pull rust@sha256:60c4afbe289a62aad63648c47790392011269f3ae812a7d03bc400333a68d836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.7 MB (525690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29ab444f2a7d9d62e8c0f1a19211d1d5fab3bbb9fe96cf8180b506d9aacb447`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614d8f32e100154b6cafdcf65ece0dbebfe80d8db1ef99ba3702f31f7e7492e8`  
		Last Modified: Fri, 27 Sep 2024 08:08:06 GMT  
		Size: 16.3 MB (16268079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59b47d19029f8522ed8e76f9d6f0e20d6e64ca4b0ec6b83c92cf0dcf4da57d4`  
		Last Modified: Fri, 27 Sep 2024 08:08:26 GMT  
		Size: 56.0 MB (56032289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93938e3248ca49e16485c4e39a8c601801fe32600e913ea08b6a71a42acd7759`  
		Last Modified: Fri, 27 Sep 2024 08:09:12 GMT  
		Size: 200.0 MB (199967470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6391bdc2b9692c19124977c7fb363bad97af929c403e77ac057e11aabc39ef7b`  
		Last Modified: Fri, 27 Sep 2024 09:12:45 GMT  
		Size: 197.3 MB (197346342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f07059339d02bf5f5deb1c3c9a9a678263144cadab6849d30ce7c1cb4b5c7bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a0a3e870e2c059fa54a70bf5c42e7f7da0289a021318006532ec5983512963`

```dockerfile
```

-	Layers:
	-	`sha256:ef0c21cfe2c931dc8fca5bc73db3fd7ddde0af5bc3c73c116a05f8ecb6a42c09`  
		Last Modified: Fri, 27 Sep 2024 09:12:40 GMT  
		Size: 15.0 MB (15040813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caeb82e791023136ba0d5372d24967e5b37b91950f985476225f277413ce379d`  
		Last Modified: Fri, 27 Sep 2024 09:12:40 GMT  
		Size: 11.8 KB (11775 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:6986d4ab9271f5504e3b561e66e2db6e40fb8dde4c8262994604db3acd937db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.7 MB (573737346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d444768bce4ae6afc8b0de2725d811c5c35d512be053c6036e77a60f78a7230`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:af2c25052aab46bab5ee70bf1b7f7c8d0339d147a2bd4daeb04ec25bd34e4799 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a8e5e0425eb7845f41056f6e5fe36c228a23a602de31f39d88868def2b2bf980`  
		Last Modified: Wed, 04 Sep 2024 22:30:31 GMT  
		Size: 59.0 MB (58950090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e76b45808a7b15592738cc59f261bb4109d1d280c5fa410f157dd270ddbf8c9`  
		Last Modified: Wed, 04 Sep 2024 23:14:50 GMT  
		Size: 16.8 MB (16766250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb7a5e65d3cbab78e31accfce79b09855b78c5b547ef6a738d98e4678a2af87`  
		Last Modified: Wed, 04 Sep 2024 23:15:06 GMT  
		Size: 58.9 MB (58872541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49975637c562cd117e86d9b35bd61ab045430938723115feadf0b276d917f54`  
		Last Modified: Wed, 04 Sep 2024 23:15:41 GMT  
		Size: 196.4 MB (196413350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4e72548af0663df3a67047671a227ceb818fd743ec005c3e0c26dba1196fa7`  
		Last Modified: Thu, 05 Sep 2024 23:37:33 GMT  
		Size: 242.7 MB (242735115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:18d2607644bfca8d172785ef824024a2587bbcd7e039c160e48e95881e76d361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15031565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3addc400c2a717f18c43ccd08b90ace573132a4d8be14ccabd100f3b5e3e79e3`

```dockerfile
```

-	Layers:
	-	`sha256:f7e53895621c513771d001c28dbc076ad0911acfcf791f76b496be0d3c03c00a`  
		Last Modified: Thu, 05 Sep 2024 23:37:26 GMT  
		Size: 15.0 MB (15019723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee700960b0d4111e9120391d7ac3ff153661a00f521840d83e2ded13f2ee5cb`  
		Last Modified: Thu, 05 Sep 2024 23:37:23 GMT  
		Size: 11.8 KB (11842 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:e994862cc3338753c10e48a809a5727a3e1766320405aad3b6bc6b2b99588710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564570515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597e9c037660824a854cb08d0af1ebfb2e150b6f43e618bd8f45cdbf4ed44fa2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:855e3f68f57762c16941f4426d4c9911e4dcaf77abfb6d1993bd8c8f0d7e83b5 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:52560ec7a98b7f8127e927ecee98fe2d97be23a6a2ec8ffbbb0b71455e06dc54`  
		Last Modified: Wed, 04 Sep 2024 21:47:54 GMT  
		Size: 53.3 MB (53317200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deb07fb0f47d9daa6d0bf809dee66d9c90207821b4a8f6c849f8287efdda0fd`  
		Last Modified: Thu, 05 Sep 2024 00:00:53 GMT  
		Size: 15.6 MB (15642390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed93d5f01b376419cd54d2ce3b7abf1bb4ab16f8c188ed6e0bca4959d860c9e`  
		Last Modified: Thu, 05 Sep 2024 00:01:05 GMT  
		Size: 54.1 MB (54075084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819f8402428b6e76aa2474a2ad7b60bda05d2333b58c0ce2e044e6474eb477b3`  
		Last Modified: Thu, 05 Sep 2024 00:01:31 GMT  
		Size: 173.0 MB (173047915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928cd4be8f5c53da1abdc68e27bdc267586b2236cb685b7ac9411f8178a4e9c9`  
		Last Modified: Fri, 06 Sep 2024 03:48:36 GMT  
		Size: 268.5 MB (268487926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:060a7d7485d2b2136c69bad068f873973ca97c522af1da4d6a695691c830ed1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4aff1b5e2666120285959b2a32028ace5129a7c6ff9db899af0b68480eae04`

```dockerfile
```

-	Layers:
	-	`sha256:46ebae515231e7a0d42d05c17b4a42e37ca8587225e58ba27697967fb36bce99`  
		Last Modified: Fri, 06 Sep 2024 03:48:31 GMT  
		Size: 14.9 MB (14873217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58aff1056b597cab684a0715c700502ce479d4df587d8a5f4cd6c7de0d2ff53`  
		Last Modified: Fri, 06 Sep 2024 03:48:31 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81-slim`

```console
$ docker pull rust@sha256:948b2b7413d0c9797581db9dc847e8ef49ff30f9edad108058f35f2829094892
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
$ docker pull rust@sha256:e1a7feeb1ede7988cd98bf29fe12658840962a6698fe7648b1d963911c3652f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284251390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb403fd1b9b464461b4572eb4f7b18b2b6881e31158e7b81255da64a67163b56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fbc8922a73fa72fbbbda7d3faf1d5d10a8eff36091c5173e584d9a215891bf`  
		Last Modified: Fri, 27 Sep 2024 06:15:51 GMT  
		Size: 255.1 MB (255125114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim` - unknown; unknown

```console
$ docker pull rust@sha256:ac727fe37fea34e145bfff9e75b51e85a802c0d063767fa3e6df994ea1da8e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eead885a9da4703238deeb48abba86d35cdcc283f04146b1c9f6111cbab3ae`

```dockerfile
```

-	Layers:
	-	`sha256:5b300e89b5db1b6f79b8095863c2a61a2cb3f710fb2261c2eed2be59b4e48e67`  
		Last Modified: Fri, 27 Sep 2024 06:15:48 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c85b7e53d6fadcbec1e983cf20f845447156dd1164dbe7c43f291d3dd90d52`  
		Last Modified: Fri, 27 Sep 2024 06:15:47 GMT  
		Size: 13.1 KB (13054 bytes)  
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
$ docker pull rust@sha256:ee4a58c7b9ba278c5e9dc04d77c9581a695f1e0ffe81bb13096f2fad7ef43351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295092776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0734af6dfbf06fc900b5026c3e972c1d3611cb78cfe967484986f62297ee84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7597026bf36d7da868af0b6530f3e00d5c1d9f0facf729ac27ef8c053adf3e1`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 264.9 MB (264948560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim` - unknown; unknown

```console
$ docker pull rust@sha256:8e14a2c4857d8c4ad5a32a3614385588fdb73ad679e464988be2f9c259d07197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de2d55084645c72d82f718d0dfe3ffba574c2a849e89f88ab2760fe6bdf995c`

```dockerfile
```

-	Layers:
	-	`sha256:25fd4c3a5d5a7e1153c978571285a580167caf9ad7360d57fbb518357e01f516`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb37db2d7c06eba4dc179767f03593cae639be850cf9e9fb8dfad5d91cc796b0`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 13.0 KB (13005 bytes)  
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
$ docker pull rust@sha256:948b2b7413d0c9797581db9dc847e8ef49ff30f9edad108058f35f2829094892
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
$ docker pull rust@sha256:e1a7feeb1ede7988cd98bf29fe12658840962a6698fe7648b1d963911c3652f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284251390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb403fd1b9b464461b4572eb4f7b18b2b6881e31158e7b81255da64a67163b56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fbc8922a73fa72fbbbda7d3faf1d5d10a8eff36091c5173e584d9a215891bf`  
		Last Modified: Fri, 27 Sep 2024 06:15:51 GMT  
		Size: 255.1 MB (255125114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ac727fe37fea34e145bfff9e75b51e85a802c0d063767fa3e6df994ea1da8e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eead885a9da4703238deeb48abba86d35cdcc283f04146b1c9f6111cbab3ae`

```dockerfile
```

-	Layers:
	-	`sha256:5b300e89b5db1b6f79b8095863c2a61a2cb3f710fb2261c2eed2be59b4e48e67`  
		Last Modified: Fri, 27 Sep 2024 06:15:48 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c85b7e53d6fadcbec1e983cf20f845447156dd1164dbe7c43f291d3dd90d52`  
		Last Modified: Fri, 27 Sep 2024 06:15:47 GMT  
		Size: 13.1 KB (13054 bytes)  
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
$ docker pull rust@sha256:ee4a58c7b9ba278c5e9dc04d77c9581a695f1e0ffe81bb13096f2fad7ef43351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295092776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0734af6dfbf06fc900b5026c3e972c1d3611cb78cfe967484986f62297ee84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7597026bf36d7da868af0b6530f3e00d5c1d9f0facf729ac27ef8c053adf3e1`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 264.9 MB (264948560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8e14a2c4857d8c4ad5a32a3614385588fdb73ad679e464988be2f9c259d07197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de2d55084645c72d82f718d0dfe3ffba574c2a849e89f88ab2760fe6bdf995c`

```dockerfile
```

-	Layers:
	-	`sha256:25fd4c3a5d5a7e1153c978571285a580167caf9ad7360d57fbb518357e01f516`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb37db2d7c06eba4dc179767f03593cae639be850cf9e9fb8dfad5d91cc796b0`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 13.0 KB (13005 bytes)  
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
$ docker pull rust@sha256:60fd98e4f6b0cc14964d74edf0dc884e101945b4a1e2eaa7112daeb1d84619ff
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

### `rust:1.81-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:c867715387d7363cf3c30c26381179f4f1e804b0d1b9969a7f852492baee90af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275916206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346d4256eb653e635cafc15d8f7282998e29ebc76b694c88da73dfe837097889`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbabb339956394a4d1fb91746cbf4761db1e54d54c9c5e487b98fcf4c45cbcd4`  
		Last Modified: Fri, 27 Sep 2024 06:16:02 GMT  
		Size: 244.5 MB (244487607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7eef46d1dcd0e823fe875b24a70e9c1355467596a38ef031ad7e418154f6eadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77a7207310f10b7ec7217d47abd395d9718820083b43ce51cb4041c02a16bf3`

```dockerfile
```

-	Layers:
	-	`sha256:85b3a79d5c46bef73c9bf9973e5ea4e1e6aaf43fb04f7e447dd70d19e6c88e7d`  
		Last Modified: Fri, 27 Sep 2024 06:15:56 GMT  
		Size: 4.2 MB (4164326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:279917aa77c9e1c40758a70e6573a49f3034cc50f5fc41b515a40385f1474e14`  
		Last Modified: Fri, 27 Sep 2024 06:15:55 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:3864eae3b065e3d81344c823dac118246b84efe418da96c127369a00cabda4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290373786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9b68951fcca1c7239656abb516436a845f49303a3f76720ba86529f4354960`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
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
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d8db63bffbb27f6b6ed74cd77d5b4f7ec42191a0b2475d68e5ed27105e592`  
		Last Modified: Fri, 27 Sep 2024 18:40:15 GMT  
		Size: 263.8 MB (263784474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:22f04e7c807cb8bdfe6269815eea5164f572c016ffda5eff59c755f41b9e068a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db454d62ef28a3c82390e251029f25d9893fea65a0925e74c81ea8c398f57d6c`

```dockerfile
```

-	Layers:
	-	`sha256:b3e4a96099f809c0ddb915f77a34b6f9fdd86737ab496c9ab79c156985b041ca`  
		Last Modified: Fri, 27 Sep 2024 18:40:09 GMT  
		Size: 4.0 MB (3973677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b966f43de96afeec4ba17d293fdc44b0a83a5a9968b85b27ec70e25a553a7eb9`  
		Last Modified: Fri, 27 Sep 2024 18:40:09 GMT  
		Size: 11.9 KB (11935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:480535d160c76a5e638040c70225a8e4d121ea028634b5d263620b58ec413a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334323357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45f260f195927f8cd55d4504b96e3434ec5bd092287a3c5868e42073e53450c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3631b207c7c399be644b042eeb8fbb3ac0c51b3397c2168d0161b1553ad076`  
		Last Modified: Fri, 27 Sep 2024 23:29:07 GMT  
		Size: 304.2 MB (304248199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e3b945e7be780f647d3eb32426bba0ba0f2add9a1bf28958cd7e4eb58155bb39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae3f54d0f5b7eb56a28900316f0b957c0b9576eb1a7024048541ca4b22d7792`

```dockerfile
```

-	Layers:
	-	`sha256:7a476c013b6e8b15084c2821b389d6d1231c10bcddfae752cdf10e7dc4554fe6`  
		Last Modified: Fri, 27 Sep 2024 23:29:01 GMT  
		Size: 4.2 MB (4161108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd5a81733b89782f55f77276aef546505e1ee78ab6888343370f870cf595bbc`  
		Last Modified: Fri, 27 Sep 2024 23:29:00 GMT  
		Size: 12.2 KB (12174 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:370149bebadd4b8a584b3d980b8a5ad01ea5406d2a144002c1866061a08fb2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290534147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c84b20cb0ea15828268c7aad29217666b9d53c3b8919c0e2439fcc40278e47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:176ca55c782e88e529d56f56999487b261e37eaa9b59fcfdf2b400ed60a31a55 in / 
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
	-	`sha256:5306a3a8e6d3817e237e681e3f75f332f8a6ba35c1f365dcff9af549d9f45234`  
		Last Modified: Fri, 27 Sep 2024 07:27:50 GMT  
		Size: 32.4 MB (32413499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e12102af9e460ec4e1bebb62ca4f08dc362023b60123469c376da657d9b6f6a`  
		Last Modified: Fri, 27 Sep 2024 09:12:29 GMT  
		Size: 258.1 MB (258120648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6a2abce60a26598af546287b011c7faabf8c4d7431dd39bf5384c1f6933c1592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd5f9c55110a73c479ef96a72e9ed6c4006bfb5cfd0a4c6c9c07e46bf125967`

```dockerfile
```

-	Layers:
	-	`sha256:f8d0de040f64ccaa948a96733126b0c90c2aa3dff35fcbb9cc21778cd3492d31`  
		Last Modified: Fri, 27 Sep 2024 09:12:22 GMT  
		Size: 4.2 MB (4156094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f87ed75714693f89afb0d8ec96eef215d07388367b7b45eb91149f838bb01e9`  
		Last Modified: Fri, 27 Sep 2024 09:12:22 GMT  
		Size: 11.8 KB (11835 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:8decec112addbd13695a85c3e36cfb3cb2234d665990d6f69a9bebfb0bbc1cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.0 MB (333036407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0333435dde12c12f5b045e83da42c26356268ad32349b2de967ad73018c3f85a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
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
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef013636d6b4779de60a6daee7eb6d85444109ea750ff43367edc3b44048045`  
		Last Modified: Thu, 05 Sep 2024 23:39:59 GMT  
		Size: 297.7 MB (297737133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:656e87dfd5b323b3534529ebb6d0988156203604648266168165a837d1ef6dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5059fbdba445f288b2849f55639287d8333cc7655e843b9fbe7c85020c224d`

```dockerfile
```

-	Layers:
	-	`sha256:d25bcba9a065f355cde74f818a97e486db851e80f67a0a407d235d79d3ade18f`  
		Last Modified: Thu, 05 Sep 2024 23:39:43 GMT  
		Size: 4.1 MB (4125251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d6c5709ca112dc1e234b9723a7a09ca1019d006a2afcc4412640d98e4fea32`  
		Last Modified: Thu, 05 Sep 2024 23:39:42 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81-slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:f1a0949c9448b312796a4aec2d6154e999eb2f96afe929b603a213508841435c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340544165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de8960b7a01ddb04ba5bfd4bfb32db85f2897b897dd86ec4323b2621f22f4f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
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
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306069be260e0429366a2595212c3875058050805ba1b96aeea8dab379bb2415`  
		Last Modified: Fri, 06 Sep 2024 03:50:36 GMT  
		Size: 310.9 MB (310880718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f155f0ff66d7853629c893ae2d504e8682516a9b70a7cd93d5a8908014def30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c44c2520b53671c6568b4dd36d9c48258d46aa1996934dc922e3db2e6f40e4`

```dockerfile
```

-	Layers:
	-	`sha256:5f3a48f9f2e94610235d8c5b94113c04789bc2d5645daf17048ffe8910ba4b8f`  
		Last Modified: Fri, 06 Sep 2024 03:50:33 GMT  
		Size: 4.0 MB (3996088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69bbabadfe35e88452c9b6e7c9598c0207c7f8a45727e3d37f9cadf57d18f76c`  
		Last Modified: Fri, 06 Sep 2024 03:50:32 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81.0`

```console
$ docker pull rust@sha256:a21d54019c66e3a1e7512651e9a7de99b08f28d49b023ed7220b7fe4d3b9f24e
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
$ docker pull rust@sha256:c9c623bcf8dd793e818cb5ee959b1eb431ebb39c044456e265de8e9815923cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533607280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3217a6680ad94a88c6ac0a3f8ce547b5040f8424fdee8578a1a5dfa669ea0c5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01272fe8adbacc44afd2b92994b31c40a151f4324ca392050d9e8d580927dd32`  
		Last Modified: Fri, 27 Sep 2024 05:15:17 GMT  
		Size: 211.3 MB (211265642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6baa1c7db3cf519424e08f89770f4a4f540d4d3effc5816374b37bbea6088f4`  
		Last Modified: Fri, 27 Sep 2024 06:15:59 GMT  
		Size: 184.3 MB (184341215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0` - unknown; unknown

```console
$ docker pull rust@sha256:1076083cde596f3ad1dadf81b432bd06f0aab7a6a9b26f231ce84664fec63184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3aefab207ffb59f652b7ea32af56dad0ff1cfbe09ac3421b174ea96d620e94`

```dockerfile
```

-	Layers:
	-	`sha256:29234bd63dfb587f9bc295fa626e6ef6b5719b1d8bb8f223aa30280100b48046`  
		Last Modified: Fri, 27 Sep 2024 06:15:57 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93886528e31b3e4bfe0c65731d32a765629c7df70835e6af89927539798d860b`  
		Last Modified: Fri, 27 Sep 2024 06:15:56 GMT  
		Size: 13.0 KB (12966 bytes)  
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
$ docker pull rust@sha256:6a81c71d5a7280b60a2cbdb73f5d4ecec2204329a5825bb0539d2531744f9d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549211767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014da5081bccc9f0142d0399541b0e671db7053e9157944b8538149ea5968c2b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
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
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ace8e3922a39d6cc6947b43fd1d677f246da4946ec81260c978cfd65f84ff1`  
		Last Modified: Fri, 27 Sep 2024 08:07:54 GMT  
		Size: 210.2 MB (210182340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9886795186c272f9016eb0f3875d40d863577d8f0092d46a03e6a4d68f4c4e57`  
		Last Modified: Fri, 27 Sep 2024 09:13:12 GMT  
		Size: 197.3 MB (197346422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0` - unknown; unknown

```console
$ docker pull rust@sha256:7275a253b7308d840d78872942bf9871c364592b63646148fb770dbb72769473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b73a609b6ed023d27dd5d4919c87729c1a143d1056eea3a8fad7a233443d0`

```dockerfile
```

-	Layers:
	-	`sha256:c71d848a6edb3cf9dec7a47303590462918ae83774d8d334c5d96e745526a5cd`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c9e4a4a6ebdb0fd79ab7fc79a335f0360c02f060e61a2f8436cc9941c6ce824`  
		Last Modified: Fri, 27 Sep 2024 09:13:07 GMT  
		Size: 12.9 KB (12917 bytes)  
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
$ docker pull rust@sha256:a21d54019c66e3a1e7512651e9a7de99b08f28d49b023ed7220b7fe4d3b9f24e
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
$ docker pull rust@sha256:c9c623bcf8dd793e818cb5ee959b1eb431ebb39c044456e265de8e9815923cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533607280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3217a6680ad94a88c6ac0a3f8ce547b5040f8424fdee8578a1a5dfa669ea0c5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01272fe8adbacc44afd2b92994b31c40a151f4324ca392050d9e8d580927dd32`  
		Last Modified: Fri, 27 Sep 2024 05:15:17 GMT  
		Size: 211.3 MB (211265642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6baa1c7db3cf519424e08f89770f4a4f540d4d3effc5816374b37bbea6088f4`  
		Last Modified: Fri, 27 Sep 2024 06:15:59 GMT  
		Size: 184.3 MB (184341215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1076083cde596f3ad1dadf81b432bd06f0aab7a6a9b26f231ce84664fec63184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3aefab207ffb59f652b7ea32af56dad0ff1cfbe09ac3421b174ea96d620e94`

```dockerfile
```

-	Layers:
	-	`sha256:29234bd63dfb587f9bc295fa626e6ef6b5719b1d8bb8f223aa30280100b48046`  
		Last Modified: Fri, 27 Sep 2024 06:15:57 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93886528e31b3e4bfe0c65731d32a765629c7df70835e6af89927539798d860b`  
		Last Modified: Fri, 27 Sep 2024 06:15:56 GMT  
		Size: 13.0 KB (12966 bytes)  
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
$ docker pull rust@sha256:6a81c71d5a7280b60a2cbdb73f5d4ecec2204329a5825bb0539d2531744f9d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549211767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014da5081bccc9f0142d0399541b0e671db7053e9157944b8538149ea5968c2b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
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
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ace8e3922a39d6cc6947b43fd1d677f246da4946ec81260c978cfd65f84ff1`  
		Last Modified: Fri, 27 Sep 2024 08:07:54 GMT  
		Size: 210.2 MB (210182340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9886795186c272f9016eb0f3875d40d863577d8f0092d46a03e6a4d68f4c4e57`  
		Last Modified: Fri, 27 Sep 2024 09:13:12 GMT  
		Size: 197.3 MB (197346422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7275a253b7308d840d78872942bf9871c364592b63646148fb770dbb72769473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b73a609b6ed023d27dd5d4919c87729c1a143d1056eea3a8fad7a233443d0`

```dockerfile
```

-	Layers:
	-	`sha256:c71d848a6edb3cf9dec7a47303590462918ae83774d8d334c5d96e745526a5cd`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c9e4a4a6ebdb0fd79ab7fc79a335f0360c02f060e61a2f8436cc9941c6ce824`  
		Last Modified: Fri, 27 Sep 2024 09:13:07 GMT  
		Size: 12.9 KB (12917 bytes)  
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
$ docker pull rust@sha256:0deb626fc05b074fc9b1453b007f92f0bec72c219e42a4a89b9b0d17201acb76
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

### `rust:1.81.0-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:f3c124d37b50b9c2b925843e96853ddc5b271046f32e1a4585aaedb6d106fdfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.0 MB (506979504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2ad98c9cf3eb39c4e66e283d192af97be03939340aca6181ad4c5c3daf8407`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21912b76607d1849ada521d53cc1be42bcc38d6583bd385a1bbd91babc6745f8`  
		Last Modified: Fri, 27 Sep 2024 05:15:27 GMT  
		Size: 15.8 MB (15764314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee27f1f94c19451b787e3a7d81f5eefbd7aed799349b4208bb04c1ce8880ccb2`  
		Last Modified: Fri, 27 Sep 2024 05:15:42 GMT  
		Size: 54.7 MB (54723654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a7fe5b36fbd67e153a5a6e8ec36c41c1fb931871662835b9abdd59e785fdb`  
		Last Modified: Fri, 27 Sep 2024 05:16:13 GMT  
		Size: 197.1 MB (197069002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c01ccb0aa52be675b92db0d8d0a7427b19445393029774c3c0fd52a324ff7ef`  
		Last Modified: Fri, 27 Sep 2024 06:16:04 GMT  
		Size: 184.3 MB (184341143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1972d424605b6c782ff0125e35c9eb029fb848de01dd4c5491dac5f38c06b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15064079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9a516196d12bb4d8d59608d0c44eb8b81491de22e6677a8dffbfe111bc3b08`

```dockerfile
```

-	Layers:
	-	`sha256:08741ee5e60d3fb87158bf15775e81b86ad4e06d851901d96b8493d3a1fe3ae0`  
		Last Modified: Fri, 27 Sep 2024 06:15:59 GMT  
		Size: 15.1 MB (15052276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:284b3427a93dbccf350467e9bf85c30cc857b3577a89a2b74dbbd2f0365830dd`  
		Last Modified: Fri, 27 Sep 2024 06:15:58 GMT  
		Size: 11.8 KB (11803 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:b276289647ff0aa629a2242b7f79691c5d9bc03ce73b687bb1440c28ad758bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.8 MB (504758546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b591737dedb5f1f7a1a7897835fbabfb6f387d7a0a233ace06964c8d2147b6bc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:c11b754156d52a292b4c2c82c7274bcdf02e2227709cc1a95025ac1512f5606f`  
		Last Modified: Sat, 28 Sep 2024 04:05:55 GMT  
		Size: 221.5 MB (221511274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d5eefeb3cf62dbd2e0294249ea58b6561ddcace71024582033bec2dced6cbba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14865192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5655e29fc00720432f5d238188a9c05e32a8c376d4803f4a0936c499ee3c91`

```dockerfile
```

-	Layers:
	-	`sha256:72c0500bc9617296f733c1557727b920ed9eed4fb7299ab1ce45b6d5ac424300`  
		Last Modified: Sat, 28 Sep 2024 04:05:50 GMT  
		Size: 14.9 MB (14853318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd4e6e657b9a9c6c5284dfec262fe343ce34100fc6be3d583217a9ccd52152ba`  
		Last Modified: Sat, 28 Sep 2024 04:05:49 GMT  
		Size: 11.9 KB (11874 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c3220040b0838a88b6b883a9bf4e252f6fe1aebba16a7189f08f45dbbee2487e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.8 MB (562811651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b925555db69a651d8e0f86e0f3b61195002c8eff0f5273dc4f50a5d43259dbab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:28c55e14a5fe2e5b9ec4f6f52d2b18f6cdda1baaa40243032acd71cbec4885e4`  
		Last Modified: Fri, 27 Sep 2024 23:27:39 GMT  
		Size: 248.5 MB (248529143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5c0c3ffcbae775ac2c9d7d87ac40bed3435a9bf507954fc22eb497d1c738fff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15066760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe42b10da972265beb8d1ea0da742b211a1298b6594a326081dbace555b12f27`

```dockerfile
```

-	Layers:
	-	`sha256:e2ea1e6cdae9a39aa1649c64168862704ec2af8be6988eb21f25b2a6dd212b85`  
		Last Modified: Fri, 27 Sep 2024 23:27:34 GMT  
		Size: 15.1 MB (15054645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d615fae986037c7de77864eb2b29aa110afaf379cd1264a912b02e7108bcf6d`  
		Last Modified: Fri, 27 Sep 2024 23:27:33 GMT  
		Size: 12.1 KB (12115 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-bullseye` - linux; 386

```console
$ docker pull rust@sha256:60c4afbe289a62aad63648c47790392011269f3ae812a7d03bc400333a68d836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.7 MB (525690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29ab444f2a7d9d62e8c0f1a19211d1d5fab3bbb9fe96cf8180b506d9aacb447`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614d8f32e100154b6cafdcf65ece0dbebfe80d8db1ef99ba3702f31f7e7492e8`  
		Last Modified: Fri, 27 Sep 2024 08:08:06 GMT  
		Size: 16.3 MB (16268079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59b47d19029f8522ed8e76f9d6f0e20d6e64ca4b0ec6b83c92cf0dcf4da57d4`  
		Last Modified: Fri, 27 Sep 2024 08:08:26 GMT  
		Size: 56.0 MB (56032289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93938e3248ca49e16485c4e39a8c601801fe32600e913ea08b6a71a42acd7759`  
		Last Modified: Fri, 27 Sep 2024 08:09:12 GMT  
		Size: 200.0 MB (199967470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6391bdc2b9692c19124977c7fb363bad97af929c403e77ac057e11aabc39ef7b`  
		Last Modified: Fri, 27 Sep 2024 09:12:45 GMT  
		Size: 197.3 MB (197346342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f07059339d02bf5f5deb1c3c9a9a678263144cadab6849d30ce7c1cb4b5c7bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a0a3e870e2c059fa54a70bf5c42e7f7da0289a021318006532ec5983512963`

```dockerfile
```

-	Layers:
	-	`sha256:ef0c21cfe2c931dc8fca5bc73db3fd7ddde0af5bc3c73c116a05f8ecb6a42c09`  
		Last Modified: Fri, 27 Sep 2024 09:12:40 GMT  
		Size: 15.0 MB (15040813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caeb82e791023136ba0d5372d24967e5b37b91950f985476225f277413ce379d`  
		Last Modified: Fri, 27 Sep 2024 09:12:40 GMT  
		Size: 11.8 KB (11775 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:6986d4ab9271f5504e3b561e66e2db6e40fb8dde4c8262994604db3acd937db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.7 MB (573737346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d444768bce4ae6afc8b0de2725d811c5c35d512be053c6036e77a60f78a7230`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:af2c25052aab46bab5ee70bf1b7f7c8d0339d147a2bd4daeb04ec25bd34e4799 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a8e5e0425eb7845f41056f6e5fe36c228a23a602de31f39d88868def2b2bf980`  
		Last Modified: Wed, 04 Sep 2024 22:30:31 GMT  
		Size: 59.0 MB (58950090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e76b45808a7b15592738cc59f261bb4109d1d280c5fa410f157dd270ddbf8c9`  
		Last Modified: Wed, 04 Sep 2024 23:14:50 GMT  
		Size: 16.8 MB (16766250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb7a5e65d3cbab78e31accfce79b09855b78c5b547ef6a738d98e4678a2af87`  
		Last Modified: Wed, 04 Sep 2024 23:15:06 GMT  
		Size: 58.9 MB (58872541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49975637c562cd117e86d9b35bd61ab045430938723115feadf0b276d917f54`  
		Last Modified: Wed, 04 Sep 2024 23:15:41 GMT  
		Size: 196.4 MB (196413350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4e72548af0663df3a67047671a227ceb818fd743ec005c3e0c26dba1196fa7`  
		Last Modified: Thu, 05 Sep 2024 23:37:33 GMT  
		Size: 242.7 MB (242735115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:18d2607644bfca8d172785ef824024a2587bbcd7e039c160e48e95881e76d361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15031565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3addc400c2a717f18c43ccd08b90ace573132a4d8be14ccabd100f3b5e3e79e3`

```dockerfile
```

-	Layers:
	-	`sha256:f7e53895621c513771d001c28dbc076ad0911acfcf791f76b496be0d3c03c00a`  
		Last Modified: Thu, 05 Sep 2024 23:37:26 GMT  
		Size: 15.0 MB (15019723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee700960b0d4111e9120391d7ac3ff153661a00f521840d83e2ded13f2ee5cb`  
		Last Modified: Thu, 05 Sep 2024 23:37:23 GMT  
		Size: 11.8 KB (11842 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:e994862cc3338753c10e48a809a5727a3e1766320405aad3b6bc6b2b99588710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564570515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597e9c037660824a854cb08d0af1ebfb2e150b6f43e618bd8f45cdbf4ed44fa2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:855e3f68f57762c16941f4426d4c9911e4dcaf77abfb6d1993bd8c8f0d7e83b5 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:52560ec7a98b7f8127e927ecee98fe2d97be23a6a2ec8ffbbb0b71455e06dc54`  
		Last Modified: Wed, 04 Sep 2024 21:47:54 GMT  
		Size: 53.3 MB (53317200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deb07fb0f47d9daa6d0bf809dee66d9c90207821b4a8f6c849f8287efdda0fd`  
		Last Modified: Thu, 05 Sep 2024 00:00:53 GMT  
		Size: 15.6 MB (15642390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed93d5f01b376419cd54d2ce3b7abf1bb4ab16f8c188ed6e0bca4959d860c9e`  
		Last Modified: Thu, 05 Sep 2024 00:01:05 GMT  
		Size: 54.1 MB (54075084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819f8402428b6e76aa2474a2ad7b60bda05d2333b58c0ce2e044e6474eb477b3`  
		Last Modified: Thu, 05 Sep 2024 00:01:31 GMT  
		Size: 173.0 MB (173047915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928cd4be8f5c53da1abdc68e27bdc267586b2236cb685b7ac9411f8178a4e9c9`  
		Last Modified: Fri, 06 Sep 2024 03:48:36 GMT  
		Size: 268.5 MB (268487926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:060a7d7485d2b2136c69bad068f873973ca97c522af1da4d6a695691c830ed1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4aff1b5e2666120285959b2a32028ace5129a7c6ff9db899af0b68480eae04`

```dockerfile
```

-	Layers:
	-	`sha256:46ebae515231e7a0d42d05c17b4a42e37ca8587225e58ba27697967fb36bce99`  
		Last Modified: Fri, 06 Sep 2024 03:48:31 GMT  
		Size: 14.9 MB (14873217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58aff1056b597cab684a0715c700502ce479d4df587d8a5f4cd6c7de0d2ff53`  
		Last Modified: Fri, 06 Sep 2024 03:48:31 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.81.0-slim`

```console
$ docker pull rust@sha256:948b2b7413d0c9797581db9dc847e8ef49ff30f9edad108058f35f2829094892
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
$ docker pull rust@sha256:e1a7feeb1ede7988cd98bf29fe12658840962a6698fe7648b1d963911c3652f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284251390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb403fd1b9b464461b4572eb4f7b18b2b6881e31158e7b81255da64a67163b56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fbc8922a73fa72fbbbda7d3faf1d5d10a8eff36091c5173e584d9a215891bf`  
		Last Modified: Fri, 27 Sep 2024 06:15:51 GMT  
		Size: 255.1 MB (255125114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:ac727fe37fea34e145bfff9e75b51e85a802c0d063767fa3e6df994ea1da8e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eead885a9da4703238deeb48abba86d35cdcc283f04146b1c9f6111cbab3ae`

```dockerfile
```

-	Layers:
	-	`sha256:5b300e89b5db1b6f79b8095863c2a61a2cb3f710fb2261c2eed2be59b4e48e67`  
		Last Modified: Fri, 27 Sep 2024 06:15:48 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c85b7e53d6fadcbec1e983cf20f845447156dd1164dbe7c43f291d3dd90d52`  
		Last Modified: Fri, 27 Sep 2024 06:15:47 GMT  
		Size: 13.1 KB (13054 bytes)  
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
$ docker pull rust@sha256:ee4a58c7b9ba278c5e9dc04d77c9581a695f1e0ffe81bb13096f2fad7ef43351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295092776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0734af6dfbf06fc900b5026c3e972c1d3611cb78cfe967484986f62297ee84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7597026bf36d7da868af0b6530f3e00d5c1d9f0facf729ac27ef8c053adf3e1`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 264.9 MB (264948560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:8e14a2c4857d8c4ad5a32a3614385588fdb73ad679e464988be2f9c259d07197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de2d55084645c72d82f718d0dfe3ffba574c2a849e89f88ab2760fe6bdf995c`

```dockerfile
```

-	Layers:
	-	`sha256:25fd4c3a5d5a7e1153c978571285a580167caf9ad7360d57fbb518357e01f516`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb37db2d7c06eba4dc179767f03593cae639be850cf9e9fb8dfad5d91cc796b0`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 13.0 KB (13005 bytes)  
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
$ docker pull rust@sha256:948b2b7413d0c9797581db9dc847e8ef49ff30f9edad108058f35f2829094892
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
$ docker pull rust@sha256:e1a7feeb1ede7988cd98bf29fe12658840962a6698fe7648b1d963911c3652f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284251390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb403fd1b9b464461b4572eb4f7b18b2b6881e31158e7b81255da64a67163b56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fbc8922a73fa72fbbbda7d3faf1d5d10a8eff36091c5173e584d9a215891bf`  
		Last Modified: Fri, 27 Sep 2024 06:15:51 GMT  
		Size: 255.1 MB (255125114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ac727fe37fea34e145bfff9e75b51e85a802c0d063767fa3e6df994ea1da8e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eead885a9da4703238deeb48abba86d35cdcc283f04146b1c9f6111cbab3ae`

```dockerfile
```

-	Layers:
	-	`sha256:5b300e89b5db1b6f79b8095863c2a61a2cb3f710fb2261c2eed2be59b4e48e67`  
		Last Modified: Fri, 27 Sep 2024 06:15:48 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c85b7e53d6fadcbec1e983cf20f845447156dd1164dbe7c43f291d3dd90d52`  
		Last Modified: Fri, 27 Sep 2024 06:15:47 GMT  
		Size: 13.1 KB (13054 bytes)  
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
$ docker pull rust@sha256:ee4a58c7b9ba278c5e9dc04d77c9581a695f1e0ffe81bb13096f2fad7ef43351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295092776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0734af6dfbf06fc900b5026c3e972c1d3611cb78cfe967484986f62297ee84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7597026bf36d7da868af0b6530f3e00d5c1d9f0facf729ac27ef8c053adf3e1`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 264.9 MB (264948560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8e14a2c4857d8c4ad5a32a3614385588fdb73ad679e464988be2f9c259d07197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de2d55084645c72d82f718d0dfe3ffba574c2a849e89f88ab2760fe6bdf995c`

```dockerfile
```

-	Layers:
	-	`sha256:25fd4c3a5d5a7e1153c978571285a580167caf9ad7360d57fbb518357e01f516`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb37db2d7c06eba4dc179767f03593cae639be850cf9e9fb8dfad5d91cc796b0`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 13.0 KB (13005 bytes)  
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
$ docker pull rust@sha256:60fd98e4f6b0cc14964d74edf0dc884e101945b4a1e2eaa7112daeb1d84619ff
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

### `rust:1.81.0-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:c867715387d7363cf3c30c26381179f4f1e804b0d1b9969a7f852492baee90af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275916206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346d4256eb653e635cafc15d8f7282998e29ebc76b694c88da73dfe837097889`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbabb339956394a4d1fb91746cbf4761db1e54d54c9c5e487b98fcf4c45cbcd4`  
		Last Modified: Fri, 27 Sep 2024 06:16:02 GMT  
		Size: 244.5 MB (244487607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7eef46d1dcd0e823fe875b24a70e9c1355467596a38ef031ad7e418154f6eadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77a7207310f10b7ec7217d47abd395d9718820083b43ce51cb4041c02a16bf3`

```dockerfile
```

-	Layers:
	-	`sha256:85b3a79d5c46bef73c9bf9973e5ea4e1e6aaf43fb04f7e447dd70d19e6c88e7d`  
		Last Modified: Fri, 27 Sep 2024 06:15:56 GMT  
		Size: 4.2 MB (4164326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:279917aa77c9e1c40758a70e6573a49f3034cc50f5fc41b515a40385f1474e14`  
		Last Modified: Fri, 27 Sep 2024 06:15:55 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:3864eae3b065e3d81344c823dac118246b84efe418da96c127369a00cabda4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290373786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9b68951fcca1c7239656abb516436a845f49303a3f76720ba86529f4354960`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
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
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d8db63bffbb27f6b6ed74cd77d5b4f7ec42191a0b2475d68e5ed27105e592`  
		Last Modified: Fri, 27 Sep 2024 18:40:15 GMT  
		Size: 263.8 MB (263784474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:22f04e7c807cb8bdfe6269815eea5164f572c016ffda5eff59c755f41b9e068a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db454d62ef28a3c82390e251029f25d9893fea65a0925e74c81ea8c398f57d6c`

```dockerfile
```

-	Layers:
	-	`sha256:b3e4a96099f809c0ddb915f77a34b6f9fdd86737ab496c9ab79c156985b041ca`  
		Last Modified: Fri, 27 Sep 2024 18:40:09 GMT  
		Size: 4.0 MB (3973677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b966f43de96afeec4ba17d293fdc44b0a83a5a9968b85b27ec70e25a553a7eb9`  
		Last Modified: Fri, 27 Sep 2024 18:40:09 GMT  
		Size: 11.9 KB (11935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:480535d160c76a5e638040c70225a8e4d121ea028634b5d263620b58ec413a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334323357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45f260f195927f8cd55d4504b96e3434ec5bd092287a3c5868e42073e53450c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3631b207c7c399be644b042eeb8fbb3ac0c51b3397c2168d0161b1553ad076`  
		Last Modified: Fri, 27 Sep 2024 23:29:07 GMT  
		Size: 304.2 MB (304248199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e3b945e7be780f647d3eb32426bba0ba0f2add9a1bf28958cd7e4eb58155bb39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae3f54d0f5b7eb56a28900316f0b957c0b9576eb1a7024048541ca4b22d7792`

```dockerfile
```

-	Layers:
	-	`sha256:7a476c013b6e8b15084c2821b389d6d1231c10bcddfae752cdf10e7dc4554fe6`  
		Last Modified: Fri, 27 Sep 2024 23:29:01 GMT  
		Size: 4.2 MB (4161108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd5a81733b89782f55f77276aef546505e1ee78ab6888343370f870cf595bbc`  
		Last Modified: Fri, 27 Sep 2024 23:29:00 GMT  
		Size: 12.2 KB (12174 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:370149bebadd4b8a584b3d980b8a5ad01ea5406d2a144002c1866061a08fb2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290534147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c84b20cb0ea15828268c7aad29217666b9d53c3b8919c0e2439fcc40278e47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:176ca55c782e88e529d56f56999487b261e37eaa9b59fcfdf2b400ed60a31a55 in / 
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
	-	`sha256:5306a3a8e6d3817e237e681e3f75f332f8a6ba35c1f365dcff9af549d9f45234`  
		Last Modified: Fri, 27 Sep 2024 07:27:50 GMT  
		Size: 32.4 MB (32413499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e12102af9e460ec4e1bebb62ca4f08dc362023b60123469c376da657d9b6f6a`  
		Last Modified: Fri, 27 Sep 2024 09:12:29 GMT  
		Size: 258.1 MB (258120648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6a2abce60a26598af546287b011c7faabf8c4d7431dd39bf5384c1f6933c1592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd5f9c55110a73c479ef96a72e9ed6c4006bfb5cfd0a4c6c9c07e46bf125967`

```dockerfile
```

-	Layers:
	-	`sha256:f8d0de040f64ccaa948a96733126b0c90c2aa3dff35fcbb9cc21778cd3492d31`  
		Last Modified: Fri, 27 Sep 2024 09:12:22 GMT  
		Size: 4.2 MB (4156094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f87ed75714693f89afb0d8ec96eef215d07388367b7b45eb91149f838bb01e9`  
		Last Modified: Fri, 27 Sep 2024 09:12:22 GMT  
		Size: 11.8 KB (11835 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:8decec112addbd13695a85c3e36cfb3cb2234d665990d6f69a9bebfb0bbc1cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.0 MB (333036407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0333435dde12c12f5b045e83da42c26356268ad32349b2de967ad73018c3f85a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
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
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef013636d6b4779de60a6daee7eb6d85444109ea750ff43367edc3b44048045`  
		Last Modified: Thu, 05 Sep 2024 23:39:59 GMT  
		Size: 297.7 MB (297737133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:656e87dfd5b323b3534529ebb6d0988156203604648266168165a837d1ef6dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5059fbdba445f288b2849f55639287d8333cc7655e843b9fbe7c85020c224d`

```dockerfile
```

-	Layers:
	-	`sha256:d25bcba9a065f355cde74f818a97e486db851e80f67a0a407d235d79d3ade18f`  
		Last Modified: Thu, 05 Sep 2024 23:39:43 GMT  
		Size: 4.1 MB (4125251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d6c5709ca112dc1e234b9723a7a09ca1019d006a2afcc4412640d98e4fea32`  
		Last Modified: Thu, 05 Sep 2024 23:39:42 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.81.0-slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:f1a0949c9448b312796a4aec2d6154e999eb2f96afe929b603a213508841435c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340544165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de8960b7a01ddb04ba5bfd4bfb32db85f2897b897dd86ec4323b2621f22f4f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
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
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306069be260e0429366a2595212c3875058050805ba1b96aeea8dab379bb2415`  
		Last Modified: Fri, 06 Sep 2024 03:50:36 GMT  
		Size: 310.9 MB (310880718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.81.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f155f0ff66d7853629c893ae2d504e8682516a9b70a7cd93d5a8908014def30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c44c2520b53671c6568b4dd36d9c48258d46aa1996934dc922e3db2e6f40e4`

```dockerfile
```

-	Layers:
	-	`sha256:5f3a48f9f2e94610235d8c5b94113c04789bc2d5645daf17048ffe8910ba4b8f`  
		Last Modified: Fri, 06 Sep 2024 03:50:33 GMT  
		Size: 4.0 MB (3996088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69bbabadfe35e88452c9b6e7c9598c0207c7f8a45727e3d37f9cadf57d18f76c`  
		Last Modified: Fri, 06 Sep 2024 03:50:32 GMT  
		Size: 11.9 KB (11866 bytes)  
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
$ docker pull rust@sha256:a21d54019c66e3a1e7512651e9a7de99b08f28d49b023ed7220b7fe4d3b9f24e
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
$ docker pull rust@sha256:c9c623bcf8dd793e818cb5ee959b1eb431ebb39c044456e265de8e9815923cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533607280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3217a6680ad94a88c6ac0a3f8ce547b5040f8424fdee8578a1a5dfa669ea0c5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01272fe8adbacc44afd2b92994b31c40a151f4324ca392050d9e8d580927dd32`  
		Last Modified: Fri, 27 Sep 2024 05:15:17 GMT  
		Size: 211.3 MB (211265642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6baa1c7db3cf519424e08f89770f4a4f540d4d3effc5816374b37bbea6088f4`  
		Last Modified: Fri, 27 Sep 2024 06:15:59 GMT  
		Size: 184.3 MB (184341215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1076083cde596f3ad1dadf81b432bd06f0aab7a6a9b26f231ce84664fec63184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3aefab207ffb59f652b7ea32af56dad0ff1cfbe09ac3421b174ea96d620e94`

```dockerfile
```

-	Layers:
	-	`sha256:29234bd63dfb587f9bc295fa626e6ef6b5719b1d8bb8f223aa30280100b48046`  
		Last Modified: Fri, 27 Sep 2024 06:15:57 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93886528e31b3e4bfe0c65731d32a765629c7df70835e6af89927539798d860b`  
		Last Modified: Fri, 27 Sep 2024 06:15:56 GMT  
		Size: 13.0 KB (12966 bytes)  
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
$ docker pull rust@sha256:6a81c71d5a7280b60a2cbdb73f5d4ecec2204329a5825bb0539d2531744f9d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549211767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014da5081bccc9f0142d0399541b0e671db7053e9157944b8538149ea5968c2b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
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
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ace8e3922a39d6cc6947b43fd1d677f246da4946ec81260c978cfd65f84ff1`  
		Last Modified: Fri, 27 Sep 2024 08:07:54 GMT  
		Size: 210.2 MB (210182340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9886795186c272f9016eb0f3875d40d863577d8f0092d46a03e6a4d68f4c4e57`  
		Last Modified: Fri, 27 Sep 2024 09:13:12 GMT  
		Size: 197.3 MB (197346422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7275a253b7308d840d78872942bf9871c364592b63646148fb770dbb72769473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b73a609b6ed023d27dd5d4919c87729c1a143d1056eea3a8fad7a233443d0`

```dockerfile
```

-	Layers:
	-	`sha256:c71d848a6edb3cf9dec7a47303590462918ae83774d8d334c5d96e745526a5cd`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c9e4a4a6ebdb0fd79ab7fc79a335f0360c02f060e61a2f8436cc9941c6ce824`  
		Last Modified: Fri, 27 Sep 2024 09:13:07 GMT  
		Size: 12.9 KB (12917 bytes)  
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
$ docker pull rust@sha256:0deb626fc05b074fc9b1453b007f92f0bec72c219e42a4a89b9b0d17201acb76
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

### `rust:bullseye` - linux; amd64

```console
$ docker pull rust@sha256:f3c124d37b50b9c2b925843e96853ddc5b271046f32e1a4585aaedb6d106fdfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.0 MB (506979504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2ad98c9cf3eb39c4e66e283d192af97be03939340aca6181ad4c5c3daf8407`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21912b76607d1849ada521d53cc1be42bcc38d6583bd385a1bbd91babc6745f8`  
		Last Modified: Fri, 27 Sep 2024 05:15:27 GMT  
		Size: 15.8 MB (15764314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee27f1f94c19451b787e3a7d81f5eefbd7aed799349b4208bb04c1ce8880ccb2`  
		Last Modified: Fri, 27 Sep 2024 05:15:42 GMT  
		Size: 54.7 MB (54723654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a7fe5b36fbd67e153a5a6e8ec36c41c1fb931871662835b9abdd59e785fdb`  
		Last Modified: Fri, 27 Sep 2024 05:16:13 GMT  
		Size: 197.1 MB (197069002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c01ccb0aa52be675b92db0d8d0a7427b19445393029774c3c0fd52a324ff7ef`  
		Last Modified: Fri, 27 Sep 2024 06:16:04 GMT  
		Size: 184.3 MB (184341143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1972d424605b6c782ff0125e35c9eb029fb848de01dd4c5491dac5f38c06b4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15064079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9a516196d12bb4d8d59608d0c44eb8b81491de22e6677a8dffbfe111bc3b08`

```dockerfile
```

-	Layers:
	-	`sha256:08741ee5e60d3fb87158bf15775e81b86ad4e06d851901d96b8493d3a1fe3ae0`  
		Last Modified: Fri, 27 Sep 2024 06:15:59 GMT  
		Size: 15.1 MB (15052276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:284b3427a93dbccf350467e9bf85c30cc857b3577a89a2b74dbbd2f0365830dd`  
		Last Modified: Fri, 27 Sep 2024 06:15:58 GMT  
		Size: 11.8 KB (11803 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:b276289647ff0aa629a2242b7f79691c5d9bc03ce73b687bb1440c28ad758bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.8 MB (504758546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b591737dedb5f1f7a1a7897835fbabfb6f387d7a0a233ace06964c8d2147b6bc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:c11b754156d52a292b4c2c82c7274bcdf02e2227709cc1a95025ac1512f5606f`  
		Last Modified: Sat, 28 Sep 2024 04:05:55 GMT  
		Size: 221.5 MB (221511274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d5eefeb3cf62dbd2e0294249ea58b6561ddcace71024582033bec2dced6cbba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14865192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5655e29fc00720432f5d238188a9c05e32a8c376d4803f4a0936c499ee3c91`

```dockerfile
```

-	Layers:
	-	`sha256:72c0500bc9617296f733c1557727b920ed9eed4fb7299ab1ce45b6d5ac424300`  
		Last Modified: Sat, 28 Sep 2024 04:05:50 GMT  
		Size: 14.9 MB (14853318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd4e6e657b9a9c6c5284dfec262fe343ce34100fc6be3d583217a9ccd52152ba`  
		Last Modified: Sat, 28 Sep 2024 04:05:49 GMT  
		Size: 11.9 KB (11874 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c3220040b0838a88b6b883a9bf4e252f6fe1aebba16a7189f08f45dbbee2487e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.8 MB (562811651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b925555db69a651d8e0f86e0f3b61195002c8eff0f5273dc4f50a5d43259dbab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:28c55e14a5fe2e5b9ec4f6f52d2b18f6cdda1baaa40243032acd71cbec4885e4`  
		Last Modified: Fri, 27 Sep 2024 23:27:39 GMT  
		Size: 248.5 MB (248529143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5c0c3ffcbae775ac2c9d7d87ac40bed3435a9bf507954fc22eb497d1c738fff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15066760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe42b10da972265beb8d1ea0da742b211a1298b6594a326081dbace555b12f27`

```dockerfile
```

-	Layers:
	-	`sha256:e2ea1e6cdae9a39aa1649c64168862704ec2af8be6988eb21f25b2a6dd212b85`  
		Last Modified: Fri, 27 Sep 2024 23:27:34 GMT  
		Size: 15.1 MB (15054645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d615fae986037c7de77864eb2b29aa110afaf379cd1264a912b02e7108bcf6d`  
		Last Modified: Fri, 27 Sep 2024 23:27:33 GMT  
		Size: 12.1 KB (12115 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:60c4afbe289a62aad63648c47790392011269f3ae812a7d03bc400333a68d836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.7 MB (525690683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29ab444f2a7d9d62e8c0f1a19211d1d5fab3bbb9fe96cf8180b506d9aacb447`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614d8f32e100154b6cafdcf65ece0dbebfe80d8db1ef99ba3702f31f7e7492e8`  
		Last Modified: Fri, 27 Sep 2024 08:08:06 GMT  
		Size: 16.3 MB (16268079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59b47d19029f8522ed8e76f9d6f0e20d6e64ca4b0ec6b83c92cf0dcf4da57d4`  
		Last Modified: Fri, 27 Sep 2024 08:08:26 GMT  
		Size: 56.0 MB (56032289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93938e3248ca49e16485c4e39a8c601801fe32600e913ea08b6a71a42acd7759`  
		Last Modified: Fri, 27 Sep 2024 08:09:12 GMT  
		Size: 200.0 MB (199967470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6391bdc2b9692c19124977c7fb363bad97af929c403e77ac057e11aabc39ef7b`  
		Last Modified: Fri, 27 Sep 2024 09:12:45 GMT  
		Size: 197.3 MB (197346342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f07059339d02bf5f5deb1c3c9a9a678263144cadab6849d30ce7c1cb4b5c7bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a0a3e870e2c059fa54a70bf5c42e7f7da0289a021318006532ec5983512963`

```dockerfile
```

-	Layers:
	-	`sha256:ef0c21cfe2c931dc8fca5bc73db3fd7ddde0af5bc3c73c116a05f8ecb6a42c09`  
		Last Modified: Fri, 27 Sep 2024 09:12:40 GMT  
		Size: 15.0 MB (15040813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caeb82e791023136ba0d5372d24967e5b37b91950f985476225f277413ce379d`  
		Last Modified: Fri, 27 Sep 2024 09:12:40 GMT  
		Size: 11.8 KB (11775 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:6986d4ab9271f5504e3b561e66e2db6e40fb8dde4c8262994604db3acd937db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.7 MB (573737346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d444768bce4ae6afc8b0de2725d811c5c35d512be053c6036e77a60f78a7230`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:af2c25052aab46bab5ee70bf1b7f7c8d0339d147a2bd4daeb04ec25bd34e4799 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a8e5e0425eb7845f41056f6e5fe36c228a23a602de31f39d88868def2b2bf980`  
		Last Modified: Wed, 04 Sep 2024 22:30:31 GMT  
		Size: 59.0 MB (58950090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e76b45808a7b15592738cc59f261bb4109d1d280c5fa410f157dd270ddbf8c9`  
		Last Modified: Wed, 04 Sep 2024 23:14:50 GMT  
		Size: 16.8 MB (16766250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb7a5e65d3cbab78e31accfce79b09855b78c5b547ef6a738d98e4678a2af87`  
		Last Modified: Wed, 04 Sep 2024 23:15:06 GMT  
		Size: 58.9 MB (58872541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49975637c562cd117e86d9b35bd61ab045430938723115feadf0b276d917f54`  
		Last Modified: Wed, 04 Sep 2024 23:15:41 GMT  
		Size: 196.4 MB (196413350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4e72548af0663df3a67047671a227ceb818fd743ec005c3e0c26dba1196fa7`  
		Last Modified: Thu, 05 Sep 2024 23:37:33 GMT  
		Size: 242.7 MB (242735115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:18d2607644bfca8d172785ef824024a2587bbcd7e039c160e48e95881e76d361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15031565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3addc400c2a717f18c43ccd08b90ace573132a4d8be14ccabd100f3b5e3e79e3`

```dockerfile
```

-	Layers:
	-	`sha256:f7e53895621c513771d001c28dbc076ad0911acfcf791f76b496be0d3c03c00a`  
		Last Modified: Thu, 05 Sep 2024 23:37:26 GMT  
		Size: 15.0 MB (15019723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee700960b0d4111e9120391d7ac3ff153661a00f521840d83e2ded13f2ee5cb`  
		Last Modified: Thu, 05 Sep 2024 23:37:23 GMT  
		Size: 11.8 KB (11842 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; s390x

```console
$ docker pull rust@sha256:e994862cc3338753c10e48a809a5727a3e1766320405aad3b6bc6b2b99588710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564570515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597e9c037660824a854cb08d0af1ebfb2e150b6f43e618bd8f45cdbf4ed44fa2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:855e3f68f57762c16941f4426d4c9911e4dcaf77abfb6d1993bd8c8f0d7e83b5 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:52560ec7a98b7f8127e927ecee98fe2d97be23a6a2ec8ffbbb0b71455e06dc54`  
		Last Modified: Wed, 04 Sep 2024 21:47:54 GMT  
		Size: 53.3 MB (53317200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deb07fb0f47d9daa6d0bf809dee66d9c90207821b4a8f6c849f8287efdda0fd`  
		Last Modified: Thu, 05 Sep 2024 00:00:53 GMT  
		Size: 15.6 MB (15642390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed93d5f01b376419cd54d2ce3b7abf1bb4ab16f8c188ed6e0bca4959d860c9e`  
		Last Modified: Thu, 05 Sep 2024 00:01:05 GMT  
		Size: 54.1 MB (54075084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819f8402428b6e76aa2474a2ad7b60bda05d2333b58c0ce2e044e6474eb477b3`  
		Last Modified: Thu, 05 Sep 2024 00:01:31 GMT  
		Size: 173.0 MB (173047915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928cd4be8f5c53da1abdc68e27bdc267586b2236cb685b7ac9411f8178a4e9c9`  
		Last Modified: Fri, 06 Sep 2024 03:48:36 GMT  
		Size: 268.5 MB (268487926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:060a7d7485d2b2136c69bad068f873973ca97c522af1da4d6a695691c830ed1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4aff1b5e2666120285959b2a32028ace5129a7c6ff9db899af0b68480eae04`

```dockerfile
```

-	Layers:
	-	`sha256:46ebae515231e7a0d42d05c17b4a42e37ca8587225e58ba27697967fb36bce99`  
		Last Modified: Fri, 06 Sep 2024 03:48:31 GMT  
		Size: 14.9 MB (14873217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58aff1056b597cab684a0715c700502ce479d4df587d8a5f4cd6c7de0d2ff53`  
		Last Modified: Fri, 06 Sep 2024 03:48:31 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:a21d54019c66e3a1e7512651e9a7de99b08f28d49b023ed7220b7fe4d3b9f24e
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
$ docker pull rust@sha256:c9c623bcf8dd793e818cb5ee959b1eb431ebb39c044456e265de8e9815923cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.6 MB (533607280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3217a6680ad94a88c6ac0a3f8ce547b5040f8424fdee8578a1a5dfa669ea0c5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01272fe8adbacc44afd2b92994b31c40a151f4324ca392050d9e8d580927dd32`  
		Last Modified: Fri, 27 Sep 2024 05:15:17 GMT  
		Size: 211.3 MB (211265642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6baa1c7db3cf519424e08f89770f4a4f540d4d3effc5816374b37bbea6088f4`  
		Last Modified: Fri, 27 Sep 2024 06:15:59 GMT  
		Size: 184.3 MB (184341215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:1076083cde596f3ad1dadf81b432bd06f0aab7a6a9b26f231ce84664fec63184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3aefab207ffb59f652b7ea32af56dad0ff1cfbe09ac3421b174ea96d620e94`

```dockerfile
```

-	Layers:
	-	`sha256:29234bd63dfb587f9bc295fa626e6ef6b5719b1d8bb8f223aa30280100b48046`  
		Last Modified: Fri, 27 Sep 2024 06:15:57 GMT  
		Size: 15.5 MB (15452641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93886528e31b3e4bfe0c65731d32a765629c7df70835e6af89927539798d860b`  
		Last Modified: Fri, 27 Sep 2024 06:15:56 GMT  
		Size: 13.0 KB (12966 bytes)  
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
$ docker pull rust@sha256:6a81c71d5a7280b60a2cbdb73f5d4ecec2204329a5825bb0539d2531744f9d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549211767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014da5081bccc9f0142d0399541b0e671db7053e9157944b8538149ea5968c2b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
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
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc024f7d9bdaf927d56f9baf9b1ddee069ce2f784ce99bf5967c93bafc57fec`  
		Last Modified: Fri, 27 Sep 2024 08:06:44 GMT  
		Size: 24.9 MB (24895422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173ceeebced8e0220c3a89ff17a261e20756481c2ad65c5a4388bd4cfc63c575`  
		Last Modified: Fri, 27 Sep 2024 08:07:07 GMT  
		Size: 66.2 MB (66210942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ace8e3922a39d6cc6947b43fd1d677f246da4946ec81260c978cfd65f84ff1`  
		Last Modified: Fri, 27 Sep 2024 08:07:54 GMT  
		Size: 210.2 MB (210182340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9886795186c272f9016eb0f3875d40d863577d8f0092d46a03e6a4d68f4c4e57`  
		Last Modified: Fri, 27 Sep 2024 09:13:12 GMT  
		Size: 197.3 MB (197346422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:7275a253b7308d840d78872942bf9871c364592b63646148fb770dbb72769473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15444318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94b73a609b6ed023d27dd5d4919c87729c1a143d1056eea3a8fad7a233443d0`

```dockerfile
```

-	Layers:
	-	`sha256:c71d848a6edb3cf9dec7a47303590462918ae83774d8d334c5d96e745526a5cd`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 15.4 MB (15431401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c9e4a4a6ebdb0fd79ab7fc79a335f0360c02f060e61a2f8436cc9941c6ce824`  
		Last Modified: Fri, 27 Sep 2024 09:13:07 GMT  
		Size: 12.9 KB (12917 bytes)  
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
$ docker pull rust@sha256:948b2b7413d0c9797581db9dc847e8ef49ff30f9edad108058f35f2829094892
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
$ docker pull rust@sha256:e1a7feeb1ede7988cd98bf29fe12658840962a6698fe7648b1d963911c3652f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284251390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb403fd1b9b464461b4572eb4f7b18b2b6881e31158e7b81255da64a67163b56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fbc8922a73fa72fbbbda7d3faf1d5d10a8eff36091c5173e584d9a215891bf`  
		Last Modified: Fri, 27 Sep 2024 06:15:51 GMT  
		Size: 255.1 MB (255125114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:ac727fe37fea34e145bfff9e75b51e85a802c0d063767fa3e6df994ea1da8e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eead885a9da4703238deeb48abba86d35cdcc283f04146b1c9f6111cbab3ae`

```dockerfile
```

-	Layers:
	-	`sha256:5b300e89b5db1b6f79b8095863c2a61a2cb3f710fb2261c2eed2be59b4e48e67`  
		Last Modified: Fri, 27 Sep 2024 06:15:48 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c85b7e53d6fadcbec1e983cf20f845447156dd1164dbe7c43f291d3dd90d52`  
		Last Modified: Fri, 27 Sep 2024 06:15:47 GMT  
		Size: 13.1 KB (13054 bytes)  
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
$ docker pull rust@sha256:ee4a58c7b9ba278c5e9dc04d77c9581a695f1e0ffe81bb13096f2fad7ef43351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295092776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0734af6dfbf06fc900b5026c3e972c1d3611cb78cfe967484986f62297ee84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7597026bf36d7da868af0b6530f3e00d5c1d9f0facf729ac27ef8c053adf3e1`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 264.9 MB (264948560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:8e14a2c4857d8c4ad5a32a3614385588fdb73ad679e464988be2f9c259d07197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de2d55084645c72d82f718d0dfe3ffba574c2a849e89f88ab2760fe6bdf995c`

```dockerfile
```

-	Layers:
	-	`sha256:25fd4c3a5d5a7e1153c978571285a580167caf9ad7360d57fbb518357e01f516`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb37db2d7c06eba4dc179767f03593cae639be850cf9e9fb8dfad5d91cc796b0`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 13.0 KB (13005 bytes)  
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
$ docker pull rust@sha256:948b2b7413d0c9797581db9dc847e8ef49ff30f9edad108058f35f2829094892
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
$ docker pull rust@sha256:e1a7feeb1ede7988cd98bf29fe12658840962a6698fe7648b1d963911c3652f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284251390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb403fd1b9b464461b4572eb4f7b18b2b6881e31158e7b81255da64a67163b56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fbc8922a73fa72fbbbda7d3faf1d5d10a8eff36091c5173e584d9a215891bf`  
		Last Modified: Fri, 27 Sep 2024 06:15:51 GMT  
		Size: 255.1 MB (255125114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ac727fe37fea34e145bfff9e75b51e85a802c0d063767fa3e6df994ea1da8e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eead885a9da4703238deeb48abba86d35cdcc283f04146b1c9f6111cbab3ae`

```dockerfile
```

-	Layers:
	-	`sha256:5b300e89b5db1b6f79b8095863c2a61a2cb3f710fb2261c2eed2be59b4e48e67`  
		Last Modified: Fri, 27 Sep 2024 06:15:48 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c85b7e53d6fadcbec1e983cf20f845447156dd1164dbe7c43f291d3dd90d52`  
		Last Modified: Fri, 27 Sep 2024 06:15:47 GMT  
		Size: 13.1 KB (13054 bytes)  
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
$ docker pull rust@sha256:ee4a58c7b9ba278c5e9dc04d77c9581a695f1e0ffe81bb13096f2fad7ef43351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295092776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0734af6dfbf06fc900b5026c3e972c1d3611cb78cfe967484986f62297ee84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7597026bf36d7da868af0b6530f3e00d5c1d9f0facf729ac27ef8c053adf3e1`  
		Last Modified: Fri, 27 Sep 2024 09:13:08 GMT  
		Size: 264.9 MB (264948560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8e14a2c4857d8c4ad5a32a3614385588fdb73ad679e464988be2f9c259d07197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de2d55084645c72d82f718d0dfe3ffba574c2a849e89f88ab2760fe6bdf995c`

```dockerfile
```

-	Layers:
	-	`sha256:25fd4c3a5d5a7e1153c978571285a580167caf9ad7360d57fbb518357e01f516`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb37db2d7c06eba4dc179767f03593cae639be850cf9e9fb8dfad5d91cc796b0`  
		Last Modified: Fri, 27 Sep 2024 09:13:02 GMT  
		Size: 13.0 KB (13005 bytes)  
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
$ docker pull rust@sha256:60fd98e4f6b0cc14964d74edf0dc884e101945b4a1e2eaa7112daeb1d84619ff
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

### `rust:slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:c867715387d7363cf3c30c26381179f4f1e804b0d1b9969a7f852492baee90af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275916206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346d4256eb653e635cafc15d8f7282998e29ebc76b694c88da73dfe837097889`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbabb339956394a4d1fb91746cbf4761db1e54d54c9c5e487b98fcf4c45cbcd4`  
		Last Modified: Fri, 27 Sep 2024 06:16:02 GMT  
		Size: 244.5 MB (244487607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7eef46d1dcd0e823fe875b24a70e9c1355467596a38ef031ad7e418154f6eadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77a7207310f10b7ec7217d47abd395d9718820083b43ce51cb4041c02a16bf3`

```dockerfile
```

-	Layers:
	-	`sha256:85b3a79d5c46bef73c9bf9973e5ea4e1e6aaf43fb04f7e447dd70d19e6c88e7d`  
		Last Modified: Fri, 27 Sep 2024 06:15:56 GMT  
		Size: 4.2 MB (4164326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:279917aa77c9e1c40758a70e6573a49f3034cc50f5fc41b515a40385f1474e14`  
		Last Modified: Fri, 27 Sep 2024 06:15:55 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:3864eae3b065e3d81344c823dac118246b84efe418da96c127369a00cabda4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290373786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9b68951fcca1c7239656abb516436a845f49303a3f76720ba86529f4354960`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
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
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d8db63bffbb27f6b6ed74cd77d5b4f7ec42191a0b2475d68e5ed27105e592`  
		Last Modified: Fri, 27 Sep 2024 18:40:15 GMT  
		Size: 263.8 MB (263784474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:22f04e7c807cb8bdfe6269815eea5164f572c016ffda5eff59c755f41b9e068a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db454d62ef28a3c82390e251029f25d9893fea65a0925e74c81ea8c398f57d6c`

```dockerfile
```

-	Layers:
	-	`sha256:b3e4a96099f809c0ddb915f77a34b6f9fdd86737ab496c9ab79c156985b041ca`  
		Last Modified: Fri, 27 Sep 2024 18:40:09 GMT  
		Size: 4.0 MB (3973677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b966f43de96afeec4ba17d293fdc44b0a83a5a9968b85b27ec70e25a553a7eb9`  
		Last Modified: Fri, 27 Sep 2024 18:40:09 GMT  
		Size: 11.9 KB (11935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:480535d160c76a5e638040c70225a8e4d121ea028634b5d263620b58ec413a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334323357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45f260f195927f8cd55d4504b96e3434ec5bd092287a3c5868e42073e53450c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3631b207c7c399be644b042eeb8fbb3ac0c51b3397c2168d0161b1553ad076`  
		Last Modified: Fri, 27 Sep 2024 23:29:07 GMT  
		Size: 304.2 MB (304248199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e3b945e7be780f647d3eb32426bba0ba0f2add9a1bf28958cd7e4eb58155bb39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae3f54d0f5b7eb56a28900316f0b957c0b9576eb1a7024048541ca4b22d7792`

```dockerfile
```

-	Layers:
	-	`sha256:7a476c013b6e8b15084c2821b389d6d1231c10bcddfae752cdf10e7dc4554fe6`  
		Last Modified: Fri, 27 Sep 2024 23:29:01 GMT  
		Size: 4.2 MB (4161108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd5a81733b89782f55f77276aef546505e1ee78ab6888343370f870cf595bbc`  
		Last Modified: Fri, 27 Sep 2024 23:29:00 GMT  
		Size: 12.2 KB (12174 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:370149bebadd4b8a584b3d980b8a5ad01ea5406d2a144002c1866061a08fb2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290534147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c84b20cb0ea15828268c7aad29217666b9d53c3b8919c0e2439fcc40278e47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:176ca55c782e88e529d56f56999487b261e37eaa9b59fcfdf2b400ed60a31a55 in / 
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
	-	`sha256:5306a3a8e6d3817e237e681e3f75f332f8a6ba35c1f365dcff9af549d9f45234`  
		Last Modified: Fri, 27 Sep 2024 07:27:50 GMT  
		Size: 32.4 MB (32413499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e12102af9e460ec4e1bebb62ca4f08dc362023b60123469c376da657d9b6f6a`  
		Last Modified: Fri, 27 Sep 2024 09:12:29 GMT  
		Size: 258.1 MB (258120648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6a2abce60a26598af546287b011c7faabf8c4d7431dd39bf5384c1f6933c1592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd5f9c55110a73c479ef96a72e9ed6c4006bfb5cfd0a4c6c9c07e46bf125967`

```dockerfile
```

-	Layers:
	-	`sha256:f8d0de040f64ccaa948a96733126b0c90c2aa3dff35fcbb9cc21778cd3492d31`  
		Last Modified: Fri, 27 Sep 2024 09:12:22 GMT  
		Size: 4.2 MB (4156094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f87ed75714693f89afb0d8ec96eef215d07388367b7b45eb91149f838bb01e9`  
		Last Modified: Fri, 27 Sep 2024 09:12:22 GMT  
		Size: 11.8 KB (11835 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:8decec112addbd13695a85c3e36cfb3cb2234d665990d6f69a9bebfb0bbc1cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.0 MB (333036407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0333435dde12c12f5b045e83da42c26356268ad32349b2de967ad73018c3f85a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
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
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef013636d6b4779de60a6daee7eb6d85444109ea750ff43367edc3b44048045`  
		Last Modified: Thu, 05 Sep 2024 23:39:59 GMT  
		Size: 297.7 MB (297737133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:656e87dfd5b323b3534529ebb6d0988156203604648266168165a837d1ef6dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5059fbdba445f288b2849f55639287d8333cc7655e843b9fbe7c85020c224d`

```dockerfile
```

-	Layers:
	-	`sha256:d25bcba9a065f355cde74f818a97e486db851e80f67a0a407d235d79d3ade18f`  
		Last Modified: Thu, 05 Sep 2024 23:39:43 GMT  
		Size: 4.1 MB (4125251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d6c5709ca112dc1e234b9723a7a09ca1019d006a2afcc4412640d98e4fea32`  
		Last Modified: Thu, 05 Sep 2024 23:39:42 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:f1a0949c9448b312796a4aec2d6154e999eb2f96afe929b603a213508841435c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340544165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de8960b7a01ddb04ba5bfd4bfb32db85f2897b897dd86ec4323b2621f22f4f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
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
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306069be260e0429366a2595212c3875058050805ba1b96aeea8dab379bb2415`  
		Last Modified: Fri, 06 Sep 2024 03:50:36 GMT  
		Size: 310.9 MB (310880718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f155f0ff66d7853629c893ae2d504e8682516a9b70a7cd93d5a8908014def30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c44c2520b53671c6568b4dd36d9c48258d46aa1996934dc922e3db2e6f40e4`

```dockerfile
```

-	Layers:
	-	`sha256:5f3a48f9f2e94610235d8c5b94113c04789bc2d5645daf17048ffe8910ba4b8f`  
		Last Modified: Fri, 06 Sep 2024 03:50:33 GMT  
		Size: 4.0 MB (3996088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69bbabadfe35e88452c9b6e7c9598c0207c7f8a45727e3d37f9cadf57d18f76c`  
		Last Modified: Fri, 06 Sep 2024 03:50:32 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json
