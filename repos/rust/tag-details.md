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
-	[`rust:1.80`](#rust180)
-	[`rust:1.80-alpine`](#rust180-alpine)
-	[`rust:1.80-alpine3.19`](#rust180-alpine319)
-	[`rust:1.80-alpine3.20`](#rust180-alpine320)
-	[`rust:1.80-bookworm`](#rust180-bookworm)
-	[`rust:1.80-bullseye`](#rust180-bullseye)
-	[`rust:1.80-slim`](#rust180-slim)
-	[`rust:1.80-slim-bookworm`](#rust180-slim-bookworm)
-	[`rust:1.80-slim-bullseye`](#rust180-slim-bullseye)
-	[`rust:1.80.1`](#rust1801)
-	[`rust:1.80.1-alpine`](#rust1801-alpine)
-	[`rust:1.80.1-alpine3.19`](#rust1801-alpine319)
-	[`rust:1.80.1-alpine3.20`](#rust1801-alpine320)
-	[`rust:1.80.1-bookworm`](#rust1801-bookworm)
-	[`rust:1.80.1-bullseye`](#rust1801-bullseye)
-	[`rust:1.80.1-slim`](#rust1801-slim)
-	[`rust:1.80.1-slim-bookworm`](#rust1801-slim-bookworm)
-	[`rust:1.80.1-slim-bullseye`](#rust1801-slim-bullseye)
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
$ docker pull rust@sha256:536c1a47d86bcfcd08b00dc234c44db1f809d4d82e86bc27fac1bf93c5da4d4a
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
$ docker pull rust@sha256:06ccb5e3932bd75a2da9ff2baf4c4f19d03ad5486e634c340bffef9db8b50064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529281659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026a817e4bea1b6b749a75bc85d5ef64738daeecc409d9e869b7f9ef888452d2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed93aa58a52c9abc1ee472f1ac74b73d3adcccc2c30744498fd5f14f3f5d22c`  
		Last Modified: Tue, 13 Aug 2024 00:50:05 GMT  
		Size: 64.1 MB (64143347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c78da43830be6d988d34c7ee091f98d828516ce5478ca10a4933d655191bf`  
		Last Modified: Tue, 13 Aug 2024 00:50:40 GMT  
		Size: 211.2 MB (211241362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab98c54729822ef968838854f81888aefb579f47b191ad4a4d785cf5b971d523`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 180.3 MB (180292173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:477d7cc2994739a0c23215ad3f1b83d1ecefb0bfb50aed4dc5bcb8d34a8318a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64aa0734bc1145b915f5daf8c924a2fad004de7d0aa084c2538aee193839a0ba`

```dockerfile
```

-	Layers:
	-	`sha256:7d7901d0a1b95ff2f3e59aa16259137ba55255568135f630079010abda348131`  
		Last Modified: Tue, 13 Aug 2024 02:07:09 GMT  
		Size: 15.4 MB (15445633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0539b21bb7c1437f95afce8e66fadbc940a7d0f5c069da6b6cfc37b172a78d7d`  
		Last Modified: Tue, 13 Aug 2024 02:07:08 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:52635e3d536e65aabeda6035aebf16cfefa52222c80f2b7c89ba2aef49344566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997788d628f3ed7e3e69e5b548f993d57216a6d67d2a674cf1db410cd051f487`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:36:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdaec64288ad5c82e3a7f27432ae79c4867ba6c8f1a77e1dc0389e784b1c6dc`  
		Last Modified: Tue, 23 Jul 2024 03:48:08 GMT  
		Size: 175.2 MB (175182891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330aae2c516b379cdc6ab2ea46fe6022ca5abb5dd81f6ceb22b5dd684739dd6f`  
		Last Modified: Thu, 08 Aug 2024 23:11:40 GMT  
		Size: 216.6 MB (216645477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:777c64ed0d880c972519d3fc0915ff77029381f1998295b1cbf1ef488c1c2e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b185492ed5df011c125b1753979c70f76f8382d95f37e98be9e7571377ba3a5`

```dockerfile
```

-	Layers:
	-	`sha256:2a12347c74112b0705e33b5abeb4386ce4db740d9f6d70491c0ba2ae5d87a7b3`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc72b06301f35f899cd2a895a63bc1c3182667593d5a711266a98120479c2d6`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3718c2d7cb8ca07e18af18e39ad9d47978f5d6293ea08cf93388519b0bdeb69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cef39470d2a61e25ea969945765cd04d4a6812b36183f5649c80d93a2c4fb85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:04:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e903e4e709d192e5547602a5978c79692063228a98585f33fb02d343bc15719`  
		Last Modified: Tue, 23 Jul 2024 08:10:20 GMT  
		Size: 64.0 MB (63994288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adacb995432c92df6de0b5690abdd064e095988fac45631ba8fc0a0ffa9be5cc`  
		Last Modified: Tue, 23 Jul 2024 08:10:47 GMT  
		Size: 202.6 MB (202624227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005a0fa88074d27ab23eb9476d21dda069a977b29a14805ef8b69c9ee9de6f83`  
		Last Modified: Thu, 08 Aug 2024 20:19:32 GMT  
		Size: 249.9 MB (249924631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:bb0e18e62c512b219c4030e85aed77e21492e6c209f41c2bd97b4c6e419d75e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbad8ceff217f49198a0154e749dca9eed27634d53533f72d7b78371522c6b9f`

```dockerfile
```

-	Layers:
	-	`sha256:0164b6a3e90b84a2be124ea2398ab19c15b61667b9c8903e8bf0138f97c9ca12`  
		Last Modified: Thu, 08 Aug 2024 20:19:27 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc9866d976cc2a34ff099e2ebaa0e2da6cd1653a0fc3b9089324f3d72569970`  
		Last Modified: Thu, 08 Aug 2024 20:19:26 GMT  
		Size: 13.3 KB (13325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:6dbb08dc9881b5c188fd943932c6d7745f00ab49d037dafc08a2a25e431ddbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544805103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a7544afeb84426d1c9251a1a7fe8f5c9a00bf544f4392b8cc4e05997281ebc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e075b040ebfb55bbbc37499ceb62cce7e1b159d4e84ac39d21c750496a79bb79`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 210.2 MB (210154881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917938cdbf5dc24e60575067e6e20b28a79f6d94e7edd13a98999aca51d10f76`  
		Last Modified: Tue, 13 Aug 2024 02:07:27 GMT  
		Size: 193.2 MB (193190447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:76077e463500664db2b6e17edd6b8937466fc72fb68683e00a40c2640408e394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15437310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b5422b0a384f3899ccf52cde5aa27a1865208b4b4527d8687f5fd1b9ce517e`

```dockerfile
```

-	Layers:
	-	`sha256:4f164ab8d63ed169dfd8be585a981ebbbc797a2188b6bc3b480f38ad7d5d6b96`  
		Last Modified: Tue, 13 Aug 2024 02:07:23 GMT  
		Size: 15.4 MB (15424393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850c5335cc3ea66d6a561ea86473df5e0a4500b715b808ad7771431463e92f16`  
		Last Modified: Tue, 13 Aug 2024 02:07:22 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:aabfcd7267b18899c0d5687bd04d90055d1c6a2bc5a6d00cfa25aeb095fd6c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554125432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfe1f9849979c55071de76ee36905890d5c20b129365588e8c37cb5baf3538c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:31:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98b19c7a350c0cd13610a34d9ca7ecb2491895327b24e7a8aa6c8e93c31678e`  
		Last Modified: Tue, 23 Jul 2024 02:42:57 GMT  
		Size: 214.3 MB (214264729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ecd62c101caf569db6b7baed93da3c1e32df39c40bfb200fe82ca215ba179c`  
		Last Modified: Thu, 08 Aug 2024 20:43:56 GMT  
		Size: 191.0 MB (191025895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:c6f065ccb862957415aa7d5700202f44c9742dbc678ec693544d019f39f58a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbe446c7d1251461e8a12f11a46b74a3f5bd0fa32c4f19972219fbef82b5642`

```dockerfile
```

-	Layers:
	-	`sha256:24c795cc9a6fd5df327f65e1543048107eeaa32312581d7c6fff3c56e1a915dd`  
		Last Modified: Thu, 08 Aug 2024 20:43:51 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02454961c6c66b24fb9862d190622f2fe224a0e61697c87bd092af1e82f5ebe0`  
		Last Modified: Thu, 08 Aug 2024 20:43:49 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:a041f87038dd5aa50a7edb19a9a22b0e63f2114761c4c2c0909cc34c017d7f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581465886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ecfc031bdc4da9adb677c5ca252c80e59830349950b36490e5b4d73a8610db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:06:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f11437a649236e2e47148907f7f8038ee2ae1c54cb67398c9bab566828b04`  
		Last Modified: Tue, 23 Jul 2024 03:15:09 GMT  
		Size: 183.3 MB (183265308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85cf1eebdb2d2ebd65ba1cc5fe22e8faf7e89da74096c3782bd59753a6738ac`  
		Last Modified: Thu, 08 Aug 2024 21:07:20 GMT  
		Size: 263.1 MB (263095152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:2f6db1ed28cd7cef16c31848f4a3223802bdd4cae172692c376ee2060a23cf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf974f24f2e88f8e59aa1d28cd69bdd82f21f64f4ceb54498f33ee166751d4a`

```dockerfile
```

-	Layers:
	-	`sha256:671441fa02a185b806c430e150049dac27e7e423084c0808cc8953a1afe27b45`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4353db07ec2b290c585bf32df750773716984ed21a6c04397779e82aaa038b1`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:b3ac1f65cf33390407c9b90558eb41e7a8311c47d836fca5800960f1aa2d11d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:25c79c9854cd4bedc797a88e2d4dc1b4502d22a540867fa66257e6e03c4c1d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279155377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204c24ee400cc1a13c13b275cb04657bc5e47150ce5a4e77d3a7671021b9a32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061bdf3a42c6c4489e9e78047cdaa3af6f7b63e5d255e0ab9e6660d180836f4`  
		Last Modified: Thu, 08 Aug 2024 20:02:39 GMT  
		Size: 55.3 MB (55346819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acee9c63bebda8ae8f027b6e99deee99e570d38430b1f5de3f271f853c530cc`  
		Last Modified: Thu, 08 Aug 2024 20:02:41 GMT  
		Size: 220.4 MB (220389518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:d7f847716cae21dc55ac84add1dab418798ef33b8624854fb6b8c65f17169302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b861f59014e11471235b45ca58fe55e1bce20e2d3235649938ddd8e10ac83b`

```dockerfile
```

-	Layers:
	-	`sha256:cda40d4b828cdfea673ac423a0571622627c241817509f9ba745a38be1560b4f`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e221181fdb20703a089d816b169375986ae47adf4002808cc72821fdf9b9e942`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1c9472feed43f2708eaa2821cf5f0a646160cee7be9d584bf730e755eedbee94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286589138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040de42a611e54d884e5a00d1765df3de096fba714c4defafc0750e79bcb340e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1b276de5f8a8a2fd3e6b931c4e180f78458c812dda2346f21361c13108618d`  
		Last Modified: Fri, 26 Jul 2024 00:29:37 GMT  
		Size: 53.0 MB (52995484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2abe5cb54c2cfbfce48a309498337e7a126ab4ea86b6df2ef36f1613354c5c4`  
		Last Modified: Thu, 08 Aug 2024 20:22:15 GMT  
		Size: 230.2 MB (230235196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:c808914252afc74e4ba729fb24e0bb95b91c9a2f8608b2a35bd39fc92b7d5a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27a7713ca3e5389a8f63774d2f2029f10a884a7ef5258c5a110ac3cc5fa9642`

```dockerfile
```

-	Layers:
	-	`sha256:dab1ad55931d3701c8a9c82cd1652b524d00f22c57bd6fc291789059b83165e3`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a90f930d575ecabd7599845ca4411c5bf521f8695acca03fbc6142619add3f7`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:536c1a47d86bcfcd08b00dc234c44db1f809d4d82e86bc27fac1bf93c5da4d4a
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
$ docker pull rust@sha256:06ccb5e3932bd75a2da9ff2baf4c4f19d03ad5486e634c340bffef9db8b50064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529281659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026a817e4bea1b6b749a75bc85d5ef64738daeecc409d9e869b7f9ef888452d2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed93aa58a52c9abc1ee472f1ac74b73d3adcccc2c30744498fd5f14f3f5d22c`  
		Last Modified: Tue, 13 Aug 2024 00:50:05 GMT  
		Size: 64.1 MB (64143347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c78da43830be6d988d34c7ee091f98d828516ce5478ca10a4933d655191bf`  
		Last Modified: Tue, 13 Aug 2024 00:50:40 GMT  
		Size: 211.2 MB (211241362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab98c54729822ef968838854f81888aefb579f47b191ad4a4d785cf5b971d523`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 180.3 MB (180292173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:477d7cc2994739a0c23215ad3f1b83d1ecefb0bfb50aed4dc5bcb8d34a8318a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64aa0734bc1145b915f5daf8c924a2fad004de7d0aa084c2538aee193839a0ba`

```dockerfile
```

-	Layers:
	-	`sha256:7d7901d0a1b95ff2f3e59aa16259137ba55255568135f630079010abda348131`  
		Last Modified: Tue, 13 Aug 2024 02:07:09 GMT  
		Size: 15.4 MB (15445633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0539b21bb7c1437f95afce8e66fadbc940a7d0f5c069da6b6cfc37b172a78d7d`  
		Last Modified: Tue, 13 Aug 2024 02:07:08 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:52635e3d536e65aabeda6035aebf16cfefa52222c80f2b7c89ba2aef49344566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997788d628f3ed7e3e69e5b548f993d57216a6d67d2a674cf1db410cd051f487`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:36:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdaec64288ad5c82e3a7f27432ae79c4867ba6c8f1a77e1dc0389e784b1c6dc`  
		Last Modified: Tue, 23 Jul 2024 03:48:08 GMT  
		Size: 175.2 MB (175182891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330aae2c516b379cdc6ab2ea46fe6022ca5abb5dd81f6ceb22b5dd684739dd6f`  
		Last Modified: Thu, 08 Aug 2024 23:11:40 GMT  
		Size: 216.6 MB (216645477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:777c64ed0d880c972519d3fc0915ff77029381f1998295b1cbf1ef488c1c2e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b185492ed5df011c125b1753979c70f76f8382d95f37e98be9e7571377ba3a5`

```dockerfile
```

-	Layers:
	-	`sha256:2a12347c74112b0705e33b5abeb4386ce4db740d9f6d70491c0ba2ae5d87a7b3`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc72b06301f35f899cd2a895a63bc1c3182667593d5a711266a98120479c2d6`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3718c2d7cb8ca07e18af18e39ad9d47978f5d6293ea08cf93388519b0bdeb69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cef39470d2a61e25ea969945765cd04d4a6812b36183f5649c80d93a2c4fb85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:04:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e903e4e709d192e5547602a5978c79692063228a98585f33fb02d343bc15719`  
		Last Modified: Tue, 23 Jul 2024 08:10:20 GMT  
		Size: 64.0 MB (63994288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adacb995432c92df6de0b5690abdd064e095988fac45631ba8fc0a0ffa9be5cc`  
		Last Modified: Tue, 23 Jul 2024 08:10:47 GMT  
		Size: 202.6 MB (202624227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005a0fa88074d27ab23eb9476d21dda069a977b29a14805ef8b69c9ee9de6f83`  
		Last Modified: Thu, 08 Aug 2024 20:19:32 GMT  
		Size: 249.9 MB (249924631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bb0e18e62c512b219c4030e85aed77e21492e6c209f41c2bd97b4c6e419d75e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbad8ceff217f49198a0154e749dca9eed27634d53533f72d7b78371522c6b9f`

```dockerfile
```

-	Layers:
	-	`sha256:0164b6a3e90b84a2be124ea2398ab19c15b61667b9c8903e8bf0138f97c9ca12`  
		Last Modified: Thu, 08 Aug 2024 20:19:27 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc9866d976cc2a34ff099e2ebaa0e2da6cd1653a0fc3b9089324f3d72569970`  
		Last Modified: Thu, 08 Aug 2024 20:19:26 GMT  
		Size: 13.3 KB (13325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:6dbb08dc9881b5c188fd943932c6d7745f00ab49d037dafc08a2a25e431ddbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544805103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a7544afeb84426d1c9251a1a7fe8f5c9a00bf544f4392b8cc4e05997281ebc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e075b040ebfb55bbbc37499ceb62cce7e1b159d4e84ac39d21c750496a79bb79`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 210.2 MB (210154881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917938cdbf5dc24e60575067e6e20b28a79f6d94e7edd13a98999aca51d10f76`  
		Last Modified: Tue, 13 Aug 2024 02:07:27 GMT  
		Size: 193.2 MB (193190447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:76077e463500664db2b6e17edd6b8937466fc72fb68683e00a40c2640408e394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15437310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b5422b0a384f3899ccf52cde5aa27a1865208b4b4527d8687f5fd1b9ce517e`

```dockerfile
```

-	Layers:
	-	`sha256:4f164ab8d63ed169dfd8be585a981ebbbc797a2188b6bc3b480f38ad7d5d6b96`  
		Last Modified: Tue, 13 Aug 2024 02:07:23 GMT  
		Size: 15.4 MB (15424393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850c5335cc3ea66d6a561ea86473df5e0a4500b715b808ad7771431463e92f16`  
		Last Modified: Tue, 13 Aug 2024 02:07:22 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:aabfcd7267b18899c0d5687bd04d90055d1c6a2bc5a6d00cfa25aeb095fd6c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554125432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfe1f9849979c55071de76ee36905890d5c20b129365588e8c37cb5baf3538c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:31:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98b19c7a350c0cd13610a34d9ca7ecb2491895327b24e7a8aa6c8e93c31678e`  
		Last Modified: Tue, 23 Jul 2024 02:42:57 GMT  
		Size: 214.3 MB (214264729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ecd62c101caf569db6b7baed93da3c1e32df39c40bfb200fe82ca215ba179c`  
		Last Modified: Thu, 08 Aug 2024 20:43:56 GMT  
		Size: 191.0 MB (191025895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c6f065ccb862957415aa7d5700202f44c9742dbc678ec693544d019f39f58a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbe446c7d1251461e8a12f11a46b74a3f5bd0fa32c4f19972219fbef82b5642`

```dockerfile
```

-	Layers:
	-	`sha256:24c795cc9a6fd5df327f65e1543048107eeaa32312581d7c6fff3c56e1a915dd`  
		Last Modified: Thu, 08 Aug 2024 20:43:51 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02454961c6c66b24fb9862d190622f2fe224a0e61697c87bd092af1e82f5ebe0`  
		Last Modified: Thu, 08 Aug 2024 20:43:49 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:a041f87038dd5aa50a7edb19a9a22b0e63f2114761c4c2c0909cc34c017d7f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581465886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ecfc031bdc4da9adb677c5ca252c80e59830349950b36490e5b4d73a8610db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:06:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f11437a649236e2e47148907f7f8038ee2ae1c54cb67398c9bab566828b04`  
		Last Modified: Tue, 23 Jul 2024 03:15:09 GMT  
		Size: 183.3 MB (183265308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85cf1eebdb2d2ebd65ba1cc5fe22e8faf7e89da74096c3782bd59753a6738ac`  
		Last Modified: Thu, 08 Aug 2024 21:07:20 GMT  
		Size: 263.1 MB (263095152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2f6db1ed28cd7cef16c31848f4a3223802bdd4cae172692c376ee2060a23cf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf974f24f2e88f8e59aa1d28cd69bdd82f21f64f4ceb54498f33ee166751d4a`

```dockerfile
```

-	Layers:
	-	`sha256:671441fa02a185b806c430e150049dac27e7e423084c0808cc8953a1afe27b45`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4353db07ec2b290c585bf32df750773716984ed21a6c04397779e82aaa038b1`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:de1606afadf25c846e6b430df25a9392e198afef8424f5164a3c397629bdf6f5
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
$ docker pull rust@sha256:8a01cbb1d1a0b0f20d0e85ac69474ca840d7e34dd1f3762d22ce624c13c417d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.8 MB (502777238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cf4e5177929d237aea9ee13011db71d6f4393b12bf0823f867c081979cfe68`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6665b6f4bd774e6a4c9738f0532ee622cf3bc07679e5a4449ba05c1f395e4f75`  
		Last Modified: Tue, 13 Aug 2024 00:51:07 GMT  
		Size: 54.6 MB (54588802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6864ced29689ec8b202ccbf73c58c0e8dc0b33400b46042d3cf659b11bbeb0`  
		Last Modified: Tue, 13 Aug 2024 00:51:37 GMT  
		Size: 197.0 MB (197047386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9332bfc0250a021ae7365e49946d877a2802c54970be6301f98a6377f3167b`  
		Last Modified: Tue, 13 Aug 2024 02:07:19 GMT  
		Size: 180.3 MB (180292122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:45c6625dc4c571c6e065eacd2c290d3b52e78721431672ef8f1aae6017189ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15064066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee08aba60fcfb9871b851fb9438503f2c42fd7ec55e838035d91709961fd4e6`

```dockerfile
```

-	Layers:
	-	`sha256:6178f196ed0702f5c1082757335355ef367c059eeb1a5c8a2eb4eff5841a0531`  
		Last Modified: Tue, 13 Aug 2024 02:07:15 GMT  
		Size: 15.1 MB (15052263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8725f5279633844314eff90b2dde2df13d1b317f50774f092d72fe4500515d5`  
		Last Modified: Tue, 13 Aug 2024 02:07:14 GMT  
		Size: 11.8 KB (11803 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:fc1c2ba8dbdab427e658f6e1072b478d8a2c7f044a23c2a71c044e1c28473be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.6 MB (499627303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d292f506565814f43ade875846ff70334e5d5ae1b0fc048cc5f736d62ec66b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:37:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:39:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a61d577d5393ca0b5e52e6cbd75569b7d9e9b50cb27f783d5482f5f97240ba0`  
		Last Modified: Tue, 23 Jul 2024 03:48:23 GMT  
		Size: 14.9 MB (14879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6354534da26fdc193140968c5b8a059bd98e1fc05e33deacad3b97f257fd35f`  
		Last Modified: Tue, 23 Jul 2024 03:48:44 GMT  
		Size: 50.4 MB (50357798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82623cfc0dda8411ed87ecde5f4fe0993f1ef9fe052103e7d162351520e9b5a`  
		Last Modified: Tue, 23 Jul 2024 03:49:26 GMT  
		Size: 167.5 MB (167501970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37b8df02c4399a603b03b4f34b372704cd35a452576506606d22fcae445377f`  
		Last Modified: Thu, 08 Aug 2024 23:07:33 GMT  
		Size: 216.6 MB (216645515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:462eebeecdde3963e3063b2490e1b6e0782c734d0dcf1048a0e33ac768815c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14865179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0932916c3084993fbcdc712e131a3e0bf6e66eaa0c6eb1d821a716d879d4cf`

```dockerfile
```

-	Layers:
	-	`sha256:1ceb9766ffc3c996f4eaebf55fe07450dd5e94eeea1a5b89b36c5fba53d689f6`  
		Last Modified: Thu, 08 Aug 2024 23:07:28 GMT  
		Size: 14.9 MB (14853305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfdb28ad04244bef9011ba332ec2910156e53b81f745250e98ccb568ad1c3c14`  
		Last Modified: Thu, 08 Aug 2024 23:07:28 GMT  
		Size: 11.9 KB (11874 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:0af877d93f5ad15b273900b5718fa54e9543053d6b60fdaf7d3933d324dd0e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564064898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e308a60ea5d4fc6acf5860b8590f8a62068a836d81ccfbff21d32e1554a0623b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:05:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c27a83c76abd51a72277b6a74eb7f88e560054e0d04383f64e2886877a20dd5`  
		Last Modified: Tue, 23 Jul 2024 08:11:04 GMT  
		Size: 15.7 MB (15749501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac540a55631c4cba93c7e4e4bf634300076d45e71db5f34f3c0d770eb826303`  
		Last Modified: Tue, 23 Jul 2024 08:11:17 GMT  
		Size: 54.7 MB (54694822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df233b2a5328fe9ae508771678b5a4faaefca18e64196b4ac65584baa5c8aa9f`  
		Last Modified: Tue, 23 Jul 2024 08:11:41 GMT  
		Size: 190.0 MB (189965935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293bb9bde419e7ff2bd1d11b0be5e624bbb4da022a57306810e8bf93edacae7`  
		Last Modified: Thu, 08 Aug 2024 20:16:15 GMT  
		Size: 249.9 MB (249924653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a81c950759245fe6bf71dc9a44290967120f9cf196ac6f9c3ec26cc9b9066cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15066748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1f155c7f42861ae71ae977b5327605eb7c0b08fd25d933a70fcabdfc74f7d3`

```dockerfile
```

-	Layers:
	-	`sha256:63e419ed617ca1448cb4e3de395d6c7eaa34a1e3863d78000db038b0dd28e597`  
		Last Modified: Thu, 08 Aug 2024 20:16:10 GMT  
		Size: 15.1 MB (15054632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c5431487765e54121cd0aa3eae0f911e3b5a461276e16d995252ff8bf1f0dd`  
		Last Modified: Thu, 08 Aug 2024 20:16:09 GMT  
		Size: 12.1 KB (12116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:738a3b16b04454270fc63b75e2a047da0e48b231aeceb616b7cc940f37555e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.4 MB (521413626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e90b11ef61715850ea288d0327fe4f6c66a3e58b76b713dcced59e1c160537a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d740897ef0cfebeecea08cfc67998814e44c45164f9dc7c044e9e2a0507541f4`  
		Last Modified: Tue, 13 Aug 2024 01:15:00 GMT  
		Size: 16.3 MB (16267943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dab982039e3c0ad98af0fa361fb64e7b9635b80923dca6744c230e0994f2bf3`  
		Last Modified: Tue, 13 Aug 2024 01:15:21 GMT  
		Size: 55.9 MB (55927707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29843169a9c8306d94c89194ed26f3e75a8d2afa2d64a020ecbfd7f77998e397`  
		Last Modified: Tue, 13 Aug 2024 01:16:03 GMT  
		Size: 200.0 MB (199953236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8aa7cdb2f4805ec070e522b08fb8df2daca6950383c02a67b5e53717344597`  
		Last Modified: Tue, 13 Aug 2024 02:07:17 GMT  
		Size: 193.2 MB (193190636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fdbf1d6b7f1e2e1b294e0f58085485d95dfab14af98d6b7e6be79004e5b974c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e2502e1e8009aa3dd9aa0e3e514e2377c2697e88143834ce72c62919176441`

```dockerfile
```

-	Layers:
	-	`sha256:d4ade476a4648ad687d599130798cfadeb31acd52e0a469ac39034d98da1d119`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 15.0 MB (15040800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b418326de281e7cea6502c3eaa68cef047f7645101d4f0e73ab3d714712e8f46`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 11.8 KB (11775 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:5d169b000fa22c36500111459fa54598015d9b9a58036c4fde316ea970715080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.0 MB (522015479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6628ed239b45a3bac424f61944be13339f4ff8a69b1ecaa56a2b0f910cfd9ce0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:34:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89f3ec0749e802be2768d4d8d990f300a55cd418831db42ee374e4bb81ab0a3`  
		Last Modified: Tue, 23 Jul 2024 02:43:09 GMT  
		Size: 16.8 MB (16765814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3543cad9c41f9c9127d1adde535bc13ac5b446330727c5083aafa4b8d005c62`  
		Last Modified: Tue, 23 Jul 2024 02:43:26 GMT  
		Size: 58.9 MB (58872667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8d0e14af4e3c68b0eae63b664f02cecf25bea995af2d28db767811530400f5`  
		Last Modified: Tue, 23 Jul 2024 02:44:02 GMT  
		Size: 196.4 MB (196396379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa1e7e00fb7dcb267da537ea7773b70fc23ef4911517cd47ca57e16f1737d39`  
		Last Modified: Thu, 08 Aug 2024 20:39:03 GMT  
		Size: 191.0 MB (191025932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6365a77354226047cb669dcd86f2834239435f66fc9b0006e2932140785087b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15031565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deab1a4e30e869095efe93fd7115bb6c4822d7adb53a741dd444ddfcc9962ed0`

```dockerfile
```

-	Layers:
	-	`sha256:920b9708e3e8034a1e85c6cd3eb284b4de4807a2573fc3cb3fcb14e7dec8c365`  
		Last Modified: Thu, 08 Aug 2024 20:38:41 GMT  
		Size: 15.0 MB (15019723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0df8b6335988c60b5f64fecffadff01292c331c5018206853c0a32330939873f`  
		Last Modified: Thu, 08 Aug 2024 20:38:40 GMT  
		Size: 11.8 KB (11842 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:921ebae07fbeba23dc69a361a9b0b36c8622aea3d650324d8be26f29f2435ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 MB (559194472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc3aa1912d381708f43b8a60cf18a4b8990c7ef65126c25b34133979bcd4eef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:07:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:08:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e924418f310f18ad368886d6df84cac76659f51225b0784a1e53ff07318533`  
		Last Modified: Tue, 23 Jul 2024 03:15:16 GMT  
		Size: 15.6 MB (15641720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af67dae0133d3a5f116411c20eed624558ce4a187db4fd8eb9a8d622a827e5f`  
		Last Modified: Tue, 23 Jul 2024 03:15:29 GMT  
		Size: 54.1 MB (54075295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d2fba31676a932e41fb57a433c1ba42080bc1e363d7a190b9c73795d53b569`  
		Last Modified: Tue, 23 Jul 2024 03:15:55 GMT  
		Size: 173.1 MB (173058357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01182cd8b35aac0f952d57ea2856b1cff0705e5fedb6acbe5036a8421dfa51c2`  
		Last Modified: Thu, 08 Aug 2024 21:02:30 GMT  
		Size: 263.1 MB (263095008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b1a3b3790ec214331ca9d1cde91e1b7dd7f754f5b4b8b22208eb03a9b0da7cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289c25562f9db8f60cc67dbe26ff26919bf469e2255ce9cfe5e7d316b1019cbe`

```dockerfile
```

-	Layers:
	-	`sha256:11856feef6838c72b7e993143fa557388e2eba83880de951658906e2eb4d308e`  
		Last Modified: Thu, 08 Aug 2024 21:02:26 GMT  
		Size: 14.9 MB (14873217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76bab5070fee4c9b12687acf21124bf4ab302cf66783848bd3a68de2e8d76da5`  
		Last Modified: Thu, 08 Aug 2024 21:02:26 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:24a6f218b9812adadf974ec395972383c309082abaa1934a71366fe72f5520ee
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
$ docker pull rust@sha256:c843545c3459df49f242e5f65abfaefab8daf6762fd02c9e7cc7d61ab0231f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280199925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aad58829b68dd23972cf2fce1aff495d6acfa7a892b4f6c1559aba9bc3c91c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f892dead4dc7447d193bf1eee68dee3497b9aacd74640651a96a4361e0247a`  
		Last Modified: Tue, 13 Aug 2024 01:24:04 GMT  
		Size: 251.1 MB (251073693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:1116ce021e26ccb4836af6a2a2a1cb7b01897da0f16b0acd3399dda83f4119ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9084ce95a43595419649c640801fee62d71f4680fcb3c826faf482dbe2dea8f`

```dockerfile
```

-	Layers:
	-	`sha256:8430a84b3cd2e32e3552a659255ca153d6e1270686be4e1eba1b91f41e4d86a7`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 3.9 MB (3945031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd8e5703942249a8168a5ab26c53e4bd1aec67480b9f77fef010c375be43429`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:ce61929bbf18fe2f71f3baf22ff0d922a23184b7a363659c4a89f061b592e620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289207527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21f40a92b064aab4ee6ffd996bc602bf2792f21275c7b9cdc43d00de4740e5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:06 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Tue, 23 Jul 2024 03:03:07 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce921058f79778f084b125986b13bbbc385e2af4323a43e8ba3619b56c4f9958`  
		Last Modified: Thu, 08 Aug 2024 23:13:34 GMT  
		Size: 264.5 MB (264489327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:c6158e3d52946464ea2a084549b57e9b5a7a316d4d5c8687ab55759dce5a1b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c38b348c9f5b9bc8beed607cad78c1693495c300cdc56085d09c4c7185f357`

```dockerfile
```

-	Layers:
	-	`sha256:d9b2fa0740b793cb1f22595581639ae59968ced32677bac7867b15035147130a`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 3.8 MB (3761488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8627724826143f20c71410a776275bf988fc9b607322f492cf1b8b257db26806`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:8a838c35cdd6830f0c38cad489c6c61bb175e743b780e073e32325fda2030c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290939264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0711696e0f062a8fb4b8c457f1c655fa9fad0526477a4f4d1667c274350f8270`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c971093bb3eb1663f53feb24b7ec49c5c9d286fba9596e358485ba6c1df7ed98`  
		Last Modified: Tue, 13 Aug 2024 01:24:20 GMT  
		Size: 260.8 MB (260794983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:c4b3f242d70526b2339549f2604d7eba5a09f1de1186638c21daef66c3ba4b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b39d8c066404d4bc719b8cd01f0d98568d81fec2b83a3fefc3e35779e95f96c`

```dockerfile
```

-	Layers:
	-	`sha256:f9143b5f37e30ff289509b5218f09b93034d2d775abd7b8b6d86df7e022a6448`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 3.9 MB (3926444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778dc71a73defbef6ddf88850ce25d585cce872fcdf0d89813f8c98e9f83f889`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:d6e98cbd14d47879216d00da246bc59421df36932dc01b1487ebfc231096ba57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292898154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872774294942018a3bd21ad695b897a5b10b030cdae2cbfe7f9d19d3482a84b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df685a4d1a2a8bd237a5de9d5ddcec381181a53967e15a25c69a7d0bd6a6c47`  
		Last Modified: Tue, 13 Aug 2024 12:47:08 GMT  
		Size: 259.8 MB (259775854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:d6e0eb2b2891ffb94f956f0ba3c7355c065c7819f5cdab82ce2b7e84b4f97b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87410e542a7a1f5e4786ef0c08d3c8e777220a50b2d36be9ece3713441efe5d`

```dockerfile
```

-	Layers:
	-	`sha256:bcd74365e2bfd97dee5ee0949156a9b2ae95479d7fb80b76ebfa4879fcbf541a`  
		Last Modified: Tue, 13 Aug 2024 12:47:02 GMT  
		Size: 3.9 MB (3917193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e101befb9e09ce3290dc45010a760b1d168781e5168d7a7b0188f9a00d3847`  
		Last Modified: Tue, 13 Aug 2024 12:47:01 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:eed01104c2dff5d47cad9cde6259fe152acdbffee61a32ccde4bf0df37e56f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340723676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec325392296c2da7203a1653034f9eb71d67c5e7da3a999fb2e08517d5794a58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e46961b207b826f317f9ddb2a562a2d81899099ed73257d6da8457c24e45e0c`  
		Last Modified: Tue, 13 Aug 2024 10:26:32 GMT  
		Size: 313.2 MB (313233579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:21c53034f7aa6da4784a46d7576ef1148a2f3dc58095a4bfd2fc98e624f3bf08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0090555459333f4a328dd0853b7ad2dbae4eb2d6c022b03a387ab0d1b97ea6e`

```dockerfile
```

-	Layers:
	-	`sha256:b71e18ae5a72712b53981379eeb88d9dc9c733fde3f2ba3bd3a1600f45aa4e5b`  
		Last Modified: Tue, 13 Aug 2024 10:26:28 GMT  
		Size: 3.8 MB (3787356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03cbdb302244d21da4fdf43fdfb2872c28958607938c6e753ef13ec9f4f5662d`  
		Last Modified: Tue, 13 Aug 2024 10:26:27 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:24a6f218b9812adadf974ec395972383c309082abaa1934a71366fe72f5520ee
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
$ docker pull rust@sha256:c843545c3459df49f242e5f65abfaefab8daf6762fd02c9e7cc7d61ab0231f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280199925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aad58829b68dd23972cf2fce1aff495d6acfa7a892b4f6c1559aba9bc3c91c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f892dead4dc7447d193bf1eee68dee3497b9aacd74640651a96a4361e0247a`  
		Last Modified: Tue, 13 Aug 2024 01:24:04 GMT  
		Size: 251.1 MB (251073693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1116ce021e26ccb4836af6a2a2a1cb7b01897da0f16b0acd3399dda83f4119ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9084ce95a43595419649c640801fee62d71f4680fcb3c826faf482dbe2dea8f`

```dockerfile
```

-	Layers:
	-	`sha256:8430a84b3cd2e32e3552a659255ca153d6e1270686be4e1eba1b91f41e4d86a7`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 3.9 MB (3945031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd8e5703942249a8168a5ab26c53e4bd1aec67480b9f77fef010c375be43429`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ce61929bbf18fe2f71f3baf22ff0d922a23184b7a363659c4a89f061b592e620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289207527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21f40a92b064aab4ee6ffd996bc602bf2792f21275c7b9cdc43d00de4740e5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:06 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Tue, 23 Jul 2024 03:03:07 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce921058f79778f084b125986b13bbbc385e2af4323a43e8ba3619b56c4f9958`  
		Last Modified: Thu, 08 Aug 2024 23:13:34 GMT  
		Size: 264.5 MB (264489327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c6158e3d52946464ea2a084549b57e9b5a7a316d4d5c8687ab55759dce5a1b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c38b348c9f5b9bc8beed607cad78c1693495c300cdc56085d09c4c7185f357`

```dockerfile
```

-	Layers:
	-	`sha256:d9b2fa0740b793cb1f22595581639ae59968ced32677bac7867b15035147130a`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 3.8 MB (3761488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8627724826143f20c71410a776275bf988fc9b607322f492cf1b8b257db26806`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:8a838c35cdd6830f0c38cad489c6c61bb175e743b780e073e32325fda2030c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290939264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0711696e0f062a8fb4b8c457f1c655fa9fad0526477a4f4d1667c274350f8270`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c971093bb3eb1663f53feb24b7ec49c5c9d286fba9596e358485ba6c1df7ed98`  
		Last Modified: Tue, 13 Aug 2024 01:24:20 GMT  
		Size: 260.8 MB (260794983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c4b3f242d70526b2339549f2604d7eba5a09f1de1186638c21daef66c3ba4b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b39d8c066404d4bc719b8cd01f0d98568d81fec2b83a3fefc3e35779e95f96c`

```dockerfile
```

-	Layers:
	-	`sha256:f9143b5f37e30ff289509b5218f09b93034d2d775abd7b8b6d86df7e022a6448`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 3.9 MB (3926444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778dc71a73defbef6ddf88850ce25d585cce872fcdf0d89813f8c98e9f83f889`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d6e98cbd14d47879216d00da246bc59421df36932dc01b1487ebfc231096ba57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292898154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872774294942018a3bd21ad695b897a5b10b030cdae2cbfe7f9d19d3482a84b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df685a4d1a2a8bd237a5de9d5ddcec381181a53967e15a25c69a7d0bd6a6c47`  
		Last Modified: Tue, 13 Aug 2024 12:47:08 GMT  
		Size: 259.8 MB (259775854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d6e0eb2b2891ffb94f956f0ba3c7355c065c7819f5cdab82ce2b7e84b4f97b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87410e542a7a1f5e4786ef0c08d3c8e777220a50b2d36be9ece3713441efe5d`

```dockerfile
```

-	Layers:
	-	`sha256:bcd74365e2bfd97dee5ee0949156a9b2ae95479d7fb80b76ebfa4879fcbf541a`  
		Last Modified: Tue, 13 Aug 2024 12:47:02 GMT  
		Size: 3.9 MB (3917193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e101befb9e09ce3290dc45010a760b1d168781e5168d7a7b0188f9a00d3847`  
		Last Modified: Tue, 13 Aug 2024 12:47:01 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:eed01104c2dff5d47cad9cde6259fe152acdbffee61a32ccde4bf0df37e56f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340723676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec325392296c2da7203a1653034f9eb71d67c5e7da3a999fb2e08517d5794a58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e46961b207b826f317f9ddb2a562a2d81899099ed73257d6da8457c24e45e0c`  
		Last Modified: Tue, 13 Aug 2024 10:26:32 GMT  
		Size: 313.2 MB (313233579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:21c53034f7aa6da4784a46d7576ef1148a2f3dc58095a4bfd2fc98e624f3bf08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0090555459333f4a328dd0853b7ad2dbae4eb2d6c022b03a387ab0d1b97ea6e`

```dockerfile
```

-	Layers:
	-	`sha256:b71e18ae5a72712b53981379eeb88d9dc9c733fde3f2ba3bd3a1600f45aa4e5b`  
		Last Modified: Tue, 13 Aug 2024 10:26:28 GMT  
		Size: 3.8 MB (3787356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03cbdb302244d21da4fdf43fdfb2872c28958607938c6e753ef13ec9f4f5662d`  
		Last Modified: Tue, 13 Aug 2024 10:26:27 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:2e03809b8850da918e5e3cf51d72f56fa89c50a0fd6043ba746b32b0eba325f2
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
$ docker pull rust@sha256:d6f66b9a8a080c54c17b7193ff57dd8c3160430b45db053d03f2721abd743a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271859645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c003508b7a8f691ad62a0eed4fa69e0d54ec27655f65d990a81d24994b64c61f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addb778fc66febdc6f1c2108c2c9d5ace21494739f320298cb4ff8c12241e592`  
		Last Modified: Tue, 13 Aug 2024 01:24:03 GMT  
		Size: 240.4 MB (240431358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:261ba66ea47b4f291dce74dfe5a0d5f2e68805f23ce59b0e5d23cf9a89254fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe7e7eb7b0f76624b32e911f5e554d351784720dbb382c7d1c1734cc7b8f532`

```dockerfile
```

-	Layers:
	-	`sha256:5b733f3cf156538fccc1809d173deaca4cb1c82de082355b20850a6e7c5da1e2`  
		Last Modified: Tue, 13 Aug 2024 01:23:59 GMT  
		Size: 4.2 MB (4164313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7acec69afed99d3c5670a73b375dbccdd8be76d552522b6ac93356fdc0debf7`  
		Last Modified: Tue, 13 Aug 2024 01:23:59 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:986d5f2381b37436bb8e34f8496af720c959d2b7c15b845b441e75b369b4b5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285517740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e696c058b2d5d16db2fe655314f747c1de6972798354d2a3936ebb13c5abb1d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:30 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Tue, 23 Jul 2024 03:03:30 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177377f17a0886d5eb4f3376f0b3abae7d0d7d4e4ac4caffea0a934ec2f7fca0`  
		Last Modified: Thu, 08 Aug 2024 23:09:20 GMT  
		Size: 258.9 MB (258928610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:36cfe3d0cd7c956d981d68f14407ba2857af81c06d1346e2544fb10e7f1b3ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d71ec4ba0a2208ed398f79b0ab349e1f079ca9b23beb584a4c2fe52b390b70`

```dockerfile
```

-	Layers:
	-	`sha256:150ddd50558ebecc4ce1407b5055277b0630ab26f76acbf0b3039e8bd670b66b`  
		Last Modified: Thu, 08 Aug 2024 23:09:14 GMT  
		Size: 4.0 MB (3973664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e54223131a68b8ea3b674333ffa6107f1eec517f9d9ef4af5e90347eca661016`  
		Last Modified: Thu, 08 Aug 2024 23:09:14 GMT  
		Size: 11.9 KB (11935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea400ae221974016cf01cfc99716046022430cc14de5608db498729f7618f668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.7 MB (335717687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290fe501a9234536387b5b30c99f27e439d23d64536b7815fe2de01d3682d07f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cb6cdc1948b06794974ff2e98a7005fb4728291f972fd9fe6890a51b35589`  
		Last Modified: Tue, 13 Aug 2024 11:45:59 GMT  
		Size: 305.6 MB (305641600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a3676673a581a4a22ae35dba326c5d9ccd2bdbde7ba9cfab0820cb96773f78ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621cc11386fc3351be6a2c44213e137c509b73cbc571f6de7541e04cbe8a4ac1`

```dockerfile
```

-	Layers:
	-	`sha256:25d0ce1b84cd190aa843a54b2f062344d99aacfdeb1f4215da7fc975e859651e`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 4.2 MB (4161095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66c9bde30e15c9a5a38892f97be33009492c2633b0fd4b560fb3907e93ecf62`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 12.2 KB (12175 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:ad0355bc000ca4ba51bbc0807b462d54262b6b5b62e73b32f506b869fc76d66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286389179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989eec17b76f290937e7bc846e971364efe1c2a25e1cc1b29fabac7b76f86a25`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:3c28079e98aa5b4ba96d948760be5fa7d7f99c878e193a63fab4f18eda2ee67e in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:1fff23531e74037071ba9be4ee63db5ccfd9c3823dceddfee08bed3fdeb6dea1`  
		Last Modified: Tue, 13 Aug 2024 00:43:17 GMT  
		Size: 32.4 MB (32413784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dad33f80b46deb53b484c36c78eb11195dd0235f166a822ec675fc08927191`  
		Last Modified: Tue, 13 Aug 2024 01:24:15 GMT  
		Size: 254.0 MB (253975395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7d5e3fc8fd195a69d23e3198c99399f9e930c4e5cd0fd5d152d7a1ada796c893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8ae1e1cb0895f077b29c9f421a61a78c4959247033e056c4da366f75634f97`

```dockerfile
```

-	Layers:
	-	`sha256:07625b7fe58e23a8c55b7286c8f8040a637b03a7c5809e152a08a580b900715e`  
		Last Modified: Tue, 13 Aug 2024 01:24:09 GMT  
		Size: 4.2 MB (4156081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8b284fa8fdb67251562fd31e46d6b1da860b97a19470f5d5063657bde4a63c9`  
		Last Modified: Tue, 13 Aug 2024 01:24:09 GMT  
		Size: 11.8 KB (11837 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:2e124406e413d8776b1b453199881fed5e310cccd6ff2cf89bbcd55e7779392c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281307733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b552eb51c1b8f762dd4d377b80e2d4c5efb0a328a7768155ed2af074d6e4698`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c654362147788e613020c1dfd3dbc701742f0f382576a6c8fc04270fa6971adc`  
		Last Modified: Tue, 13 Aug 2024 12:45:01 GMT  
		Size: 246.0 MB (246002600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fc1a61e4a6294cd56939edaacaf3806c8e09c8e0e819ec2ac682f79ff0652860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebc27d4fcc986991e662e4d513125eb2853de84f71c955ea5d8f365fe9347e3`

```dockerfile
```

-	Layers:
	-	`sha256:59027fbc6d8061aadd55edc122501d1f113062f9cf7e1bd2f47fff9b1adc0f2c`  
		Last Modified: Tue, 13 Aug 2024 12:44:55 GMT  
		Size: 4.1 MB (4125251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:508fdbef0798fce2e62a675348e13da7fd33785a7c7feefa1d4b6f8b722e159f`  
		Last Modified: Tue, 13 Aug 2024 12:44:55 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:f32b2cc38bf331c2dcff9a2576c73c3d99fcf712e8a0f950317fa9c5ed02761e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.2 MB (335152308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1a9f2b11e7d42b0db2c2f3775690e72d71b3a4f2b25b1f594542899c8a1de0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:a473fc09ddb0d1045f7f330f3a48b9cfe65ff9ea65cfa5c8262a8a5be9d4db75 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:83ea1b2f9d26c88827c9a658387c782a21fca528fbf7418f1a4eaea9a9818bdf`  
		Last Modified: Tue, 13 Aug 2024 00:47:58 GMT  
		Size: 29.7 MB (29668965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa1b7e0935282d5dc2e3ed32b65580c9c1c5de92e62d38b3a2733171400637a`  
		Last Modified: Tue, 13 Aug 2024 10:24:34 GMT  
		Size: 305.5 MB (305483343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d8e5509f37d18a1f09701710bca8d2f20d240c92f2ec7abbb27584f74a3bf65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088f2652d425afff66fa5c06441c9176a550540b0c3acf473f72b0f7f2679f63`

```dockerfile
```

-	Layers:
	-	`sha256:bdde162d496d13b73574bc4ebaf1594707c06da7ff0e2d1a126f3398c45b4896`  
		Last Modified: Tue, 13 Aug 2024 10:24:29 GMT  
		Size: 4.0 MB (3996088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63d2e6e316929c4003d9bac6b86c2fe1f7aa69ffc3070585e949f434945961b8`  
		Last Modified: Tue, 13 Aug 2024 10:24:29 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80`

```console
$ docker pull rust@sha256:536c1a47d86bcfcd08b00dc234c44db1f809d4d82e86bc27fac1bf93c5da4d4a
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

### `rust:1.80` - linux; amd64

```console
$ docker pull rust@sha256:06ccb5e3932bd75a2da9ff2baf4c4f19d03ad5486e634c340bffef9db8b50064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529281659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026a817e4bea1b6b749a75bc85d5ef64738daeecc409d9e869b7f9ef888452d2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed93aa58a52c9abc1ee472f1ac74b73d3adcccc2c30744498fd5f14f3f5d22c`  
		Last Modified: Tue, 13 Aug 2024 00:50:05 GMT  
		Size: 64.1 MB (64143347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c78da43830be6d988d34c7ee091f98d828516ce5478ca10a4933d655191bf`  
		Last Modified: Tue, 13 Aug 2024 00:50:40 GMT  
		Size: 211.2 MB (211241362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab98c54729822ef968838854f81888aefb579f47b191ad4a4d785cf5b971d523`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 180.3 MB (180292173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80` - unknown; unknown

```console
$ docker pull rust@sha256:477d7cc2994739a0c23215ad3f1b83d1ecefb0bfb50aed4dc5bcb8d34a8318a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64aa0734bc1145b915f5daf8c924a2fad004de7d0aa084c2538aee193839a0ba`

```dockerfile
```

-	Layers:
	-	`sha256:7d7901d0a1b95ff2f3e59aa16259137ba55255568135f630079010abda348131`  
		Last Modified: Tue, 13 Aug 2024 02:07:09 GMT  
		Size: 15.4 MB (15445633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0539b21bb7c1437f95afce8e66fadbc940a7d0f5c069da6b6cfc37b172a78d7d`  
		Last Modified: Tue, 13 Aug 2024 02:07:08 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80` - linux; arm variant v7

```console
$ docker pull rust@sha256:52635e3d536e65aabeda6035aebf16cfefa52222c80f2b7c89ba2aef49344566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997788d628f3ed7e3e69e5b548f993d57216a6d67d2a674cf1db410cd051f487`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:36:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdaec64288ad5c82e3a7f27432ae79c4867ba6c8f1a77e1dc0389e784b1c6dc`  
		Last Modified: Tue, 23 Jul 2024 03:48:08 GMT  
		Size: 175.2 MB (175182891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330aae2c516b379cdc6ab2ea46fe6022ca5abb5dd81f6ceb22b5dd684739dd6f`  
		Last Modified: Thu, 08 Aug 2024 23:11:40 GMT  
		Size: 216.6 MB (216645477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80` - unknown; unknown

```console
$ docker pull rust@sha256:777c64ed0d880c972519d3fc0915ff77029381f1998295b1cbf1ef488c1c2e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b185492ed5df011c125b1753979c70f76f8382d95f37e98be9e7571377ba3a5`

```dockerfile
```

-	Layers:
	-	`sha256:2a12347c74112b0705e33b5abeb4386ce4db740d9f6d70491c0ba2ae5d87a7b3`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc72b06301f35f899cd2a895a63bc1c3182667593d5a711266a98120479c2d6`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3718c2d7cb8ca07e18af18e39ad9d47978f5d6293ea08cf93388519b0bdeb69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cef39470d2a61e25ea969945765cd04d4a6812b36183f5649c80d93a2c4fb85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:04:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e903e4e709d192e5547602a5978c79692063228a98585f33fb02d343bc15719`  
		Last Modified: Tue, 23 Jul 2024 08:10:20 GMT  
		Size: 64.0 MB (63994288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adacb995432c92df6de0b5690abdd064e095988fac45631ba8fc0a0ffa9be5cc`  
		Last Modified: Tue, 23 Jul 2024 08:10:47 GMT  
		Size: 202.6 MB (202624227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005a0fa88074d27ab23eb9476d21dda069a977b29a14805ef8b69c9ee9de6f83`  
		Last Modified: Thu, 08 Aug 2024 20:19:32 GMT  
		Size: 249.9 MB (249924631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80` - unknown; unknown

```console
$ docker pull rust@sha256:bb0e18e62c512b219c4030e85aed77e21492e6c209f41c2bd97b4c6e419d75e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbad8ceff217f49198a0154e749dca9eed27634d53533f72d7b78371522c6b9f`

```dockerfile
```

-	Layers:
	-	`sha256:0164b6a3e90b84a2be124ea2398ab19c15b61667b9c8903e8bf0138f97c9ca12`  
		Last Modified: Thu, 08 Aug 2024 20:19:27 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc9866d976cc2a34ff099e2ebaa0e2da6cd1653a0fc3b9089324f3d72569970`  
		Last Modified: Thu, 08 Aug 2024 20:19:26 GMT  
		Size: 13.3 KB (13325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80` - linux; 386

```console
$ docker pull rust@sha256:6dbb08dc9881b5c188fd943932c6d7745f00ab49d037dafc08a2a25e431ddbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544805103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a7544afeb84426d1c9251a1a7fe8f5c9a00bf544f4392b8cc4e05997281ebc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e075b040ebfb55bbbc37499ceb62cce7e1b159d4e84ac39d21c750496a79bb79`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 210.2 MB (210154881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917938cdbf5dc24e60575067e6e20b28a79f6d94e7edd13a98999aca51d10f76`  
		Last Modified: Tue, 13 Aug 2024 02:07:27 GMT  
		Size: 193.2 MB (193190447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80` - unknown; unknown

```console
$ docker pull rust@sha256:76077e463500664db2b6e17edd6b8937466fc72fb68683e00a40c2640408e394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15437310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b5422b0a384f3899ccf52cde5aa27a1865208b4b4527d8687f5fd1b9ce517e`

```dockerfile
```

-	Layers:
	-	`sha256:4f164ab8d63ed169dfd8be585a981ebbbc797a2188b6bc3b480f38ad7d5d6b96`  
		Last Modified: Tue, 13 Aug 2024 02:07:23 GMT  
		Size: 15.4 MB (15424393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850c5335cc3ea66d6a561ea86473df5e0a4500b715b808ad7771431463e92f16`  
		Last Modified: Tue, 13 Aug 2024 02:07:22 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80` - linux; ppc64le

```console
$ docker pull rust@sha256:aabfcd7267b18899c0d5687bd04d90055d1c6a2bc5a6d00cfa25aeb095fd6c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554125432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfe1f9849979c55071de76ee36905890d5c20b129365588e8c37cb5baf3538c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:31:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98b19c7a350c0cd13610a34d9ca7ecb2491895327b24e7a8aa6c8e93c31678e`  
		Last Modified: Tue, 23 Jul 2024 02:42:57 GMT  
		Size: 214.3 MB (214264729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ecd62c101caf569db6b7baed93da3c1e32df39c40bfb200fe82ca215ba179c`  
		Last Modified: Thu, 08 Aug 2024 20:43:56 GMT  
		Size: 191.0 MB (191025895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80` - unknown; unknown

```console
$ docker pull rust@sha256:c6f065ccb862957415aa7d5700202f44c9742dbc678ec693544d019f39f58a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbe446c7d1251461e8a12f11a46b74a3f5bd0fa32c4f19972219fbef82b5642`

```dockerfile
```

-	Layers:
	-	`sha256:24c795cc9a6fd5df327f65e1543048107eeaa32312581d7c6fff3c56e1a915dd`  
		Last Modified: Thu, 08 Aug 2024 20:43:51 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02454961c6c66b24fb9862d190622f2fe224a0e61697c87bd092af1e82f5ebe0`  
		Last Modified: Thu, 08 Aug 2024 20:43:49 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80` - linux; s390x

```console
$ docker pull rust@sha256:a041f87038dd5aa50a7edb19a9a22b0e63f2114761c4c2c0909cc34c017d7f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581465886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ecfc031bdc4da9adb677c5ca252c80e59830349950b36490e5b4d73a8610db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:06:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f11437a649236e2e47148907f7f8038ee2ae1c54cb67398c9bab566828b04`  
		Last Modified: Tue, 23 Jul 2024 03:15:09 GMT  
		Size: 183.3 MB (183265308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85cf1eebdb2d2ebd65ba1cc5fe22e8faf7e89da74096c3782bd59753a6738ac`  
		Last Modified: Thu, 08 Aug 2024 21:07:20 GMT  
		Size: 263.1 MB (263095152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80` - unknown; unknown

```console
$ docker pull rust@sha256:2f6db1ed28cd7cef16c31848f4a3223802bdd4cae172692c376ee2060a23cf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf974f24f2e88f8e59aa1d28cd69bdd82f21f64f4ceb54498f33ee166751d4a`

```dockerfile
```

-	Layers:
	-	`sha256:671441fa02a185b806c430e150049dac27e7e423084c0808cc8953a1afe27b45`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4353db07ec2b290c585bf32df750773716984ed21a6c04397779e82aaa038b1`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-alpine`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.80-alpine` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-alpine3.19`

```console
$ docker pull rust@sha256:b3ac1f65cf33390407c9b90558eb41e7a8311c47d836fca5800960f1aa2d11d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.80-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:25c79c9854cd4bedc797a88e2d4dc1b4502d22a540867fa66257e6e03c4c1d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279155377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204c24ee400cc1a13c13b275cb04657bc5e47150ce5a4e77d3a7671021b9a32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061bdf3a42c6c4489e9e78047cdaa3af6f7b63e5d255e0ab9e6660d180836f4`  
		Last Modified: Thu, 08 Aug 2024 20:02:39 GMT  
		Size: 55.3 MB (55346819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acee9c63bebda8ae8f027b6e99deee99e570d38430b1f5de3f271f853c530cc`  
		Last Modified: Thu, 08 Aug 2024 20:02:41 GMT  
		Size: 220.4 MB (220389518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:d7f847716cae21dc55ac84add1dab418798ef33b8624854fb6b8c65f17169302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b861f59014e11471235b45ca58fe55e1bce20e2d3235649938ddd8e10ac83b`

```dockerfile
```

-	Layers:
	-	`sha256:cda40d4b828cdfea673ac423a0571622627c241817509f9ba745a38be1560b4f`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e221181fdb20703a089d816b169375986ae47adf4002808cc72821fdf9b9e942`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1c9472feed43f2708eaa2821cf5f0a646160cee7be9d584bf730e755eedbee94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286589138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040de42a611e54d884e5a00d1765df3de096fba714c4defafc0750e79bcb340e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1b276de5f8a8a2fd3e6b931c4e180f78458c812dda2346f21361c13108618d`  
		Last Modified: Fri, 26 Jul 2024 00:29:37 GMT  
		Size: 53.0 MB (52995484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2abe5cb54c2cfbfce48a309498337e7a126ab4ea86b6df2ef36f1613354c5c4`  
		Last Modified: Thu, 08 Aug 2024 20:22:15 GMT  
		Size: 230.2 MB (230235196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:c808914252afc74e4ba729fb24e0bb95b91c9a2f8608b2a35bd39fc92b7d5a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27a7713ca3e5389a8f63774d2f2029f10a884a7ef5258c5a110ac3cc5fa9642`

```dockerfile
```

-	Layers:
	-	`sha256:dab1ad55931d3701c8a9c82cd1652b524d00f22c57bd6fc291789059b83165e3`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a90f930d575ecabd7599845ca4411c5bf521f8695acca03fbc6142619add3f7`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-alpine3.20`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.80-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-bookworm`

```console
$ docker pull rust@sha256:536c1a47d86bcfcd08b00dc234c44db1f809d4d82e86bc27fac1bf93c5da4d4a
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

### `rust:1.80-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:06ccb5e3932bd75a2da9ff2baf4c4f19d03ad5486e634c340bffef9db8b50064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529281659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026a817e4bea1b6b749a75bc85d5ef64738daeecc409d9e869b7f9ef888452d2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed93aa58a52c9abc1ee472f1ac74b73d3adcccc2c30744498fd5f14f3f5d22c`  
		Last Modified: Tue, 13 Aug 2024 00:50:05 GMT  
		Size: 64.1 MB (64143347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c78da43830be6d988d34c7ee091f98d828516ce5478ca10a4933d655191bf`  
		Last Modified: Tue, 13 Aug 2024 00:50:40 GMT  
		Size: 211.2 MB (211241362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab98c54729822ef968838854f81888aefb579f47b191ad4a4d785cf5b971d523`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 180.3 MB (180292173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:477d7cc2994739a0c23215ad3f1b83d1ecefb0bfb50aed4dc5bcb8d34a8318a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64aa0734bc1145b915f5daf8c924a2fad004de7d0aa084c2538aee193839a0ba`

```dockerfile
```

-	Layers:
	-	`sha256:7d7901d0a1b95ff2f3e59aa16259137ba55255568135f630079010abda348131`  
		Last Modified: Tue, 13 Aug 2024 02:07:09 GMT  
		Size: 15.4 MB (15445633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0539b21bb7c1437f95afce8e66fadbc940a7d0f5c069da6b6cfc37b172a78d7d`  
		Last Modified: Tue, 13 Aug 2024 02:07:08 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:52635e3d536e65aabeda6035aebf16cfefa52222c80f2b7c89ba2aef49344566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997788d628f3ed7e3e69e5b548f993d57216a6d67d2a674cf1db410cd051f487`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:36:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdaec64288ad5c82e3a7f27432ae79c4867ba6c8f1a77e1dc0389e784b1c6dc`  
		Last Modified: Tue, 23 Jul 2024 03:48:08 GMT  
		Size: 175.2 MB (175182891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330aae2c516b379cdc6ab2ea46fe6022ca5abb5dd81f6ceb22b5dd684739dd6f`  
		Last Modified: Thu, 08 Aug 2024 23:11:40 GMT  
		Size: 216.6 MB (216645477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:777c64ed0d880c972519d3fc0915ff77029381f1998295b1cbf1ef488c1c2e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b185492ed5df011c125b1753979c70f76f8382d95f37e98be9e7571377ba3a5`

```dockerfile
```

-	Layers:
	-	`sha256:2a12347c74112b0705e33b5abeb4386ce4db740d9f6d70491c0ba2ae5d87a7b3`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc72b06301f35f899cd2a895a63bc1c3182667593d5a711266a98120479c2d6`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3718c2d7cb8ca07e18af18e39ad9d47978f5d6293ea08cf93388519b0bdeb69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cef39470d2a61e25ea969945765cd04d4a6812b36183f5649c80d93a2c4fb85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:04:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e903e4e709d192e5547602a5978c79692063228a98585f33fb02d343bc15719`  
		Last Modified: Tue, 23 Jul 2024 08:10:20 GMT  
		Size: 64.0 MB (63994288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adacb995432c92df6de0b5690abdd064e095988fac45631ba8fc0a0ffa9be5cc`  
		Last Modified: Tue, 23 Jul 2024 08:10:47 GMT  
		Size: 202.6 MB (202624227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005a0fa88074d27ab23eb9476d21dda069a977b29a14805ef8b69c9ee9de6f83`  
		Last Modified: Thu, 08 Aug 2024 20:19:32 GMT  
		Size: 249.9 MB (249924631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bb0e18e62c512b219c4030e85aed77e21492e6c209f41c2bd97b4c6e419d75e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbad8ceff217f49198a0154e749dca9eed27634d53533f72d7b78371522c6b9f`

```dockerfile
```

-	Layers:
	-	`sha256:0164b6a3e90b84a2be124ea2398ab19c15b61667b9c8903e8bf0138f97c9ca12`  
		Last Modified: Thu, 08 Aug 2024 20:19:27 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc9866d976cc2a34ff099e2ebaa0e2da6cd1653a0fc3b9089324f3d72569970`  
		Last Modified: Thu, 08 Aug 2024 20:19:26 GMT  
		Size: 13.3 KB (13325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bookworm` - linux; 386

```console
$ docker pull rust@sha256:6dbb08dc9881b5c188fd943932c6d7745f00ab49d037dafc08a2a25e431ddbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544805103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a7544afeb84426d1c9251a1a7fe8f5c9a00bf544f4392b8cc4e05997281ebc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e075b040ebfb55bbbc37499ceb62cce7e1b159d4e84ac39d21c750496a79bb79`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 210.2 MB (210154881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917938cdbf5dc24e60575067e6e20b28a79f6d94e7edd13a98999aca51d10f76`  
		Last Modified: Tue, 13 Aug 2024 02:07:27 GMT  
		Size: 193.2 MB (193190447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:76077e463500664db2b6e17edd6b8937466fc72fb68683e00a40c2640408e394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15437310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b5422b0a384f3899ccf52cde5aa27a1865208b4b4527d8687f5fd1b9ce517e`

```dockerfile
```

-	Layers:
	-	`sha256:4f164ab8d63ed169dfd8be585a981ebbbc797a2188b6bc3b480f38ad7d5d6b96`  
		Last Modified: Tue, 13 Aug 2024 02:07:23 GMT  
		Size: 15.4 MB (15424393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850c5335cc3ea66d6a561ea86473df5e0a4500b715b808ad7771431463e92f16`  
		Last Modified: Tue, 13 Aug 2024 02:07:22 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:aabfcd7267b18899c0d5687bd04d90055d1c6a2bc5a6d00cfa25aeb095fd6c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554125432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfe1f9849979c55071de76ee36905890d5c20b129365588e8c37cb5baf3538c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:31:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98b19c7a350c0cd13610a34d9ca7ecb2491895327b24e7a8aa6c8e93c31678e`  
		Last Modified: Tue, 23 Jul 2024 02:42:57 GMT  
		Size: 214.3 MB (214264729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ecd62c101caf569db6b7baed93da3c1e32df39c40bfb200fe82ca215ba179c`  
		Last Modified: Thu, 08 Aug 2024 20:43:56 GMT  
		Size: 191.0 MB (191025895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c6f065ccb862957415aa7d5700202f44c9742dbc678ec693544d019f39f58a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbe446c7d1251461e8a12f11a46b74a3f5bd0fa32c4f19972219fbef82b5642`

```dockerfile
```

-	Layers:
	-	`sha256:24c795cc9a6fd5df327f65e1543048107eeaa32312581d7c6fff3c56e1a915dd`  
		Last Modified: Thu, 08 Aug 2024 20:43:51 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02454961c6c66b24fb9862d190622f2fe224a0e61697c87bd092af1e82f5ebe0`  
		Last Modified: Thu, 08 Aug 2024 20:43:49 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:a041f87038dd5aa50a7edb19a9a22b0e63f2114761c4c2c0909cc34c017d7f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581465886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ecfc031bdc4da9adb677c5ca252c80e59830349950b36490e5b4d73a8610db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:06:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f11437a649236e2e47148907f7f8038ee2ae1c54cb67398c9bab566828b04`  
		Last Modified: Tue, 23 Jul 2024 03:15:09 GMT  
		Size: 183.3 MB (183265308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85cf1eebdb2d2ebd65ba1cc5fe22e8faf7e89da74096c3782bd59753a6738ac`  
		Last Modified: Thu, 08 Aug 2024 21:07:20 GMT  
		Size: 263.1 MB (263095152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2f6db1ed28cd7cef16c31848f4a3223802bdd4cae172692c376ee2060a23cf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf974f24f2e88f8e59aa1d28cd69bdd82f21f64f4ceb54498f33ee166751d4a`

```dockerfile
```

-	Layers:
	-	`sha256:671441fa02a185b806c430e150049dac27e7e423084c0808cc8953a1afe27b45`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4353db07ec2b290c585bf32df750773716984ed21a6c04397779e82aaa038b1`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-bullseye`

```console
$ docker pull rust@sha256:de1606afadf25c846e6b430df25a9392e198afef8424f5164a3c397629bdf6f5
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

### `rust:1.80-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:8a01cbb1d1a0b0f20d0e85ac69474ca840d7e34dd1f3762d22ce624c13c417d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.8 MB (502777238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cf4e5177929d237aea9ee13011db71d6f4393b12bf0823f867c081979cfe68`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6665b6f4bd774e6a4c9738f0532ee622cf3bc07679e5a4449ba05c1f395e4f75`  
		Last Modified: Tue, 13 Aug 2024 00:51:07 GMT  
		Size: 54.6 MB (54588802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6864ced29689ec8b202ccbf73c58c0e8dc0b33400b46042d3cf659b11bbeb0`  
		Last Modified: Tue, 13 Aug 2024 00:51:37 GMT  
		Size: 197.0 MB (197047386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9332bfc0250a021ae7365e49946d877a2802c54970be6301f98a6377f3167b`  
		Last Modified: Tue, 13 Aug 2024 02:07:19 GMT  
		Size: 180.3 MB (180292122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:45c6625dc4c571c6e065eacd2c290d3b52e78721431672ef8f1aae6017189ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15064066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee08aba60fcfb9871b851fb9438503f2c42fd7ec55e838035d91709961fd4e6`

```dockerfile
```

-	Layers:
	-	`sha256:6178f196ed0702f5c1082757335355ef367c059eeb1a5c8a2eb4eff5841a0531`  
		Last Modified: Tue, 13 Aug 2024 02:07:15 GMT  
		Size: 15.1 MB (15052263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8725f5279633844314eff90b2dde2df13d1b317f50774f092d72fe4500515d5`  
		Last Modified: Tue, 13 Aug 2024 02:07:14 GMT  
		Size: 11.8 KB (11803 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:fc1c2ba8dbdab427e658f6e1072b478d8a2c7f044a23c2a71c044e1c28473be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.6 MB (499627303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d292f506565814f43ade875846ff70334e5d5ae1b0fc048cc5f736d62ec66b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:37:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:39:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a61d577d5393ca0b5e52e6cbd75569b7d9e9b50cb27f783d5482f5f97240ba0`  
		Last Modified: Tue, 23 Jul 2024 03:48:23 GMT  
		Size: 14.9 MB (14879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6354534da26fdc193140968c5b8a059bd98e1fc05e33deacad3b97f257fd35f`  
		Last Modified: Tue, 23 Jul 2024 03:48:44 GMT  
		Size: 50.4 MB (50357798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82623cfc0dda8411ed87ecde5f4fe0993f1ef9fe052103e7d162351520e9b5a`  
		Last Modified: Tue, 23 Jul 2024 03:49:26 GMT  
		Size: 167.5 MB (167501970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37b8df02c4399a603b03b4f34b372704cd35a452576506606d22fcae445377f`  
		Last Modified: Thu, 08 Aug 2024 23:07:33 GMT  
		Size: 216.6 MB (216645515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:462eebeecdde3963e3063b2490e1b6e0782c734d0dcf1048a0e33ac768815c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14865179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0932916c3084993fbcdc712e131a3e0bf6e66eaa0c6eb1d821a716d879d4cf`

```dockerfile
```

-	Layers:
	-	`sha256:1ceb9766ffc3c996f4eaebf55fe07450dd5e94eeea1a5b89b36c5fba53d689f6`  
		Last Modified: Thu, 08 Aug 2024 23:07:28 GMT  
		Size: 14.9 MB (14853305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfdb28ad04244bef9011ba332ec2910156e53b81f745250e98ccb568ad1c3c14`  
		Last Modified: Thu, 08 Aug 2024 23:07:28 GMT  
		Size: 11.9 KB (11874 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:0af877d93f5ad15b273900b5718fa54e9543053d6b60fdaf7d3933d324dd0e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564064898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e308a60ea5d4fc6acf5860b8590f8a62068a836d81ccfbff21d32e1554a0623b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:05:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c27a83c76abd51a72277b6a74eb7f88e560054e0d04383f64e2886877a20dd5`  
		Last Modified: Tue, 23 Jul 2024 08:11:04 GMT  
		Size: 15.7 MB (15749501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac540a55631c4cba93c7e4e4bf634300076d45e71db5f34f3c0d770eb826303`  
		Last Modified: Tue, 23 Jul 2024 08:11:17 GMT  
		Size: 54.7 MB (54694822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df233b2a5328fe9ae508771678b5a4faaefca18e64196b4ac65584baa5c8aa9f`  
		Last Modified: Tue, 23 Jul 2024 08:11:41 GMT  
		Size: 190.0 MB (189965935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293bb9bde419e7ff2bd1d11b0be5e624bbb4da022a57306810e8bf93edacae7`  
		Last Modified: Thu, 08 Aug 2024 20:16:15 GMT  
		Size: 249.9 MB (249924653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a81c950759245fe6bf71dc9a44290967120f9cf196ac6f9c3ec26cc9b9066cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15066748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1f155c7f42861ae71ae977b5327605eb7c0b08fd25d933a70fcabdfc74f7d3`

```dockerfile
```

-	Layers:
	-	`sha256:63e419ed617ca1448cb4e3de395d6c7eaa34a1e3863d78000db038b0dd28e597`  
		Last Modified: Thu, 08 Aug 2024 20:16:10 GMT  
		Size: 15.1 MB (15054632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c5431487765e54121cd0aa3eae0f911e3b5a461276e16d995252ff8bf1f0dd`  
		Last Modified: Thu, 08 Aug 2024 20:16:09 GMT  
		Size: 12.1 KB (12116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bullseye` - linux; 386

```console
$ docker pull rust@sha256:738a3b16b04454270fc63b75e2a047da0e48b231aeceb616b7cc940f37555e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.4 MB (521413626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e90b11ef61715850ea288d0327fe4f6c66a3e58b76b713dcced59e1c160537a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d740897ef0cfebeecea08cfc67998814e44c45164f9dc7c044e9e2a0507541f4`  
		Last Modified: Tue, 13 Aug 2024 01:15:00 GMT  
		Size: 16.3 MB (16267943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dab982039e3c0ad98af0fa361fb64e7b9635b80923dca6744c230e0994f2bf3`  
		Last Modified: Tue, 13 Aug 2024 01:15:21 GMT  
		Size: 55.9 MB (55927707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29843169a9c8306d94c89194ed26f3e75a8d2afa2d64a020ecbfd7f77998e397`  
		Last Modified: Tue, 13 Aug 2024 01:16:03 GMT  
		Size: 200.0 MB (199953236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8aa7cdb2f4805ec070e522b08fb8df2daca6950383c02a67b5e53717344597`  
		Last Modified: Tue, 13 Aug 2024 02:07:17 GMT  
		Size: 193.2 MB (193190636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fdbf1d6b7f1e2e1b294e0f58085485d95dfab14af98d6b7e6be79004e5b974c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e2502e1e8009aa3dd9aa0e3e514e2377c2697e88143834ce72c62919176441`

```dockerfile
```

-	Layers:
	-	`sha256:d4ade476a4648ad687d599130798cfadeb31acd52e0a469ac39034d98da1d119`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 15.0 MB (15040800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b418326de281e7cea6502c3eaa68cef047f7645101d4f0e73ab3d714712e8f46`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 11.8 KB (11775 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:5d169b000fa22c36500111459fa54598015d9b9a58036c4fde316ea970715080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.0 MB (522015479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6628ed239b45a3bac424f61944be13339f4ff8a69b1ecaa56a2b0f910cfd9ce0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:34:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89f3ec0749e802be2768d4d8d990f300a55cd418831db42ee374e4bb81ab0a3`  
		Last Modified: Tue, 23 Jul 2024 02:43:09 GMT  
		Size: 16.8 MB (16765814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3543cad9c41f9c9127d1adde535bc13ac5b446330727c5083aafa4b8d005c62`  
		Last Modified: Tue, 23 Jul 2024 02:43:26 GMT  
		Size: 58.9 MB (58872667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8d0e14af4e3c68b0eae63b664f02cecf25bea995af2d28db767811530400f5`  
		Last Modified: Tue, 23 Jul 2024 02:44:02 GMT  
		Size: 196.4 MB (196396379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa1e7e00fb7dcb267da537ea7773b70fc23ef4911517cd47ca57e16f1737d39`  
		Last Modified: Thu, 08 Aug 2024 20:39:03 GMT  
		Size: 191.0 MB (191025932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6365a77354226047cb669dcd86f2834239435f66fc9b0006e2932140785087b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15031565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deab1a4e30e869095efe93fd7115bb6c4822d7adb53a741dd444ddfcc9962ed0`

```dockerfile
```

-	Layers:
	-	`sha256:920b9708e3e8034a1e85c6cd3eb284b4de4807a2573fc3cb3fcb14e7dec8c365`  
		Last Modified: Thu, 08 Aug 2024 20:38:41 GMT  
		Size: 15.0 MB (15019723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0df8b6335988c60b5f64fecffadff01292c331c5018206853c0a32330939873f`  
		Last Modified: Thu, 08 Aug 2024 20:38:40 GMT  
		Size: 11.8 KB (11842 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:921ebae07fbeba23dc69a361a9b0b36c8622aea3d650324d8be26f29f2435ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 MB (559194472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc3aa1912d381708f43b8a60cf18a4b8990c7ef65126c25b34133979bcd4eef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:07:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:08:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e924418f310f18ad368886d6df84cac76659f51225b0784a1e53ff07318533`  
		Last Modified: Tue, 23 Jul 2024 03:15:16 GMT  
		Size: 15.6 MB (15641720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af67dae0133d3a5f116411c20eed624558ce4a187db4fd8eb9a8d622a827e5f`  
		Last Modified: Tue, 23 Jul 2024 03:15:29 GMT  
		Size: 54.1 MB (54075295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d2fba31676a932e41fb57a433c1ba42080bc1e363d7a190b9c73795d53b569`  
		Last Modified: Tue, 23 Jul 2024 03:15:55 GMT  
		Size: 173.1 MB (173058357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01182cd8b35aac0f952d57ea2856b1cff0705e5fedb6acbe5036a8421dfa51c2`  
		Last Modified: Thu, 08 Aug 2024 21:02:30 GMT  
		Size: 263.1 MB (263095008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b1a3b3790ec214331ca9d1cde91e1b7dd7f754f5b4b8b22208eb03a9b0da7cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289c25562f9db8f60cc67dbe26ff26919bf469e2255ce9cfe5e7d316b1019cbe`

```dockerfile
```

-	Layers:
	-	`sha256:11856feef6838c72b7e993143fa557388e2eba83880de951658906e2eb4d308e`  
		Last Modified: Thu, 08 Aug 2024 21:02:26 GMT  
		Size: 14.9 MB (14873217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76bab5070fee4c9b12687acf21124bf4ab302cf66783848bd3a68de2e8d76da5`  
		Last Modified: Thu, 08 Aug 2024 21:02:26 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-slim`

```console
$ docker pull rust@sha256:24a6f218b9812adadf974ec395972383c309082abaa1934a71366fe72f5520ee
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

### `rust:1.80-slim` - linux; amd64

```console
$ docker pull rust@sha256:c843545c3459df49f242e5f65abfaefab8daf6762fd02c9e7cc7d61ab0231f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280199925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aad58829b68dd23972cf2fce1aff495d6acfa7a892b4f6c1559aba9bc3c91c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f892dead4dc7447d193bf1eee68dee3497b9aacd74640651a96a4361e0247a`  
		Last Modified: Tue, 13 Aug 2024 01:24:04 GMT  
		Size: 251.1 MB (251073693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim` - unknown; unknown

```console
$ docker pull rust@sha256:1116ce021e26ccb4836af6a2a2a1cb7b01897da0f16b0acd3399dda83f4119ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9084ce95a43595419649c640801fee62d71f4680fcb3c826faf482dbe2dea8f`

```dockerfile
```

-	Layers:
	-	`sha256:8430a84b3cd2e32e3552a659255ca153d6e1270686be4e1eba1b91f41e4d86a7`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 3.9 MB (3945031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd8e5703942249a8168a5ab26c53e4bd1aec67480b9f77fef010c375be43429`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:ce61929bbf18fe2f71f3baf22ff0d922a23184b7a363659c4a89f061b592e620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289207527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21f40a92b064aab4ee6ffd996bc602bf2792f21275c7b9cdc43d00de4740e5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:06 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Tue, 23 Jul 2024 03:03:07 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce921058f79778f084b125986b13bbbc385e2af4323a43e8ba3619b56c4f9958`  
		Last Modified: Thu, 08 Aug 2024 23:13:34 GMT  
		Size: 264.5 MB (264489327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim` - unknown; unknown

```console
$ docker pull rust@sha256:c6158e3d52946464ea2a084549b57e9b5a7a316d4d5c8687ab55759dce5a1b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c38b348c9f5b9bc8beed607cad78c1693495c300cdc56085d09c4c7185f357`

```dockerfile
```

-	Layers:
	-	`sha256:d9b2fa0740b793cb1f22595581639ae59968ced32677bac7867b15035147130a`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 3.8 MB (3761488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8627724826143f20c71410a776275bf988fc9b607322f492cf1b8b257db26806`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim` - linux; 386

```console
$ docker pull rust@sha256:8a838c35cdd6830f0c38cad489c6c61bb175e743b780e073e32325fda2030c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290939264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0711696e0f062a8fb4b8c457f1c655fa9fad0526477a4f4d1667c274350f8270`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c971093bb3eb1663f53feb24b7ec49c5c9d286fba9596e358485ba6c1df7ed98`  
		Last Modified: Tue, 13 Aug 2024 01:24:20 GMT  
		Size: 260.8 MB (260794983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim` - unknown; unknown

```console
$ docker pull rust@sha256:c4b3f242d70526b2339549f2604d7eba5a09f1de1186638c21daef66c3ba4b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b39d8c066404d4bc719b8cd01f0d98568d81fec2b83a3fefc3e35779e95f96c`

```dockerfile
```

-	Layers:
	-	`sha256:f9143b5f37e30ff289509b5218f09b93034d2d775abd7b8b6d86df7e022a6448`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 3.9 MB (3926444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778dc71a73defbef6ddf88850ce25d585cce872fcdf0d89813f8c98e9f83f889`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:d6e98cbd14d47879216d00da246bc59421df36932dc01b1487ebfc231096ba57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292898154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872774294942018a3bd21ad695b897a5b10b030cdae2cbfe7f9d19d3482a84b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df685a4d1a2a8bd237a5de9d5ddcec381181a53967e15a25c69a7d0bd6a6c47`  
		Last Modified: Tue, 13 Aug 2024 12:47:08 GMT  
		Size: 259.8 MB (259775854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim` - unknown; unknown

```console
$ docker pull rust@sha256:d6e0eb2b2891ffb94f956f0ba3c7355c065c7819f5cdab82ce2b7e84b4f97b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87410e542a7a1f5e4786ef0c08d3c8e777220a50b2d36be9ece3713441efe5d`

```dockerfile
```

-	Layers:
	-	`sha256:bcd74365e2bfd97dee5ee0949156a9b2ae95479d7fb80b76ebfa4879fcbf541a`  
		Last Modified: Tue, 13 Aug 2024 12:47:02 GMT  
		Size: 3.9 MB (3917193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e101befb9e09ce3290dc45010a760b1d168781e5168d7a7b0188f9a00d3847`  
		Last Modified: Tue, 13 Aug 2024 12:47:01 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim` - linux; s390x

```console
$ docker pull rust@sha256:eed01104c2dff5d47cad9cde6259fe152acdbffee61a32ccde4bf0df37e56f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340723676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec325392296c2da7203a1653034f9eb71d67c5e7da3a999fb2e08517d5794a58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e46961b207b826f317f9ddb2a562a2d81899099ed73257d6da8457c24e45e0c`  
		Last Modified: Tue, 13 Aug 2024 10:26:32 GMT  
		Size: 313.2 MB (313233579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim` - unknown; unknown

```console
$ docker pull rust@sha256:21c53034f7aa6da4784a46d7576ef1148a2f3dc58095a4bfd2fc98e624f3bf08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0090555459333f4a328dd0853b7ad2dbae4eb2d6c022b03a387ab0d1b97ea6e`

```dockerfile
```

-	Layers:
	-	`sha256:b71e18ae5a72712b53981379eeb88d9dc9c733fde3f2ba3bd3a1600f45aa4e5b`  
		Last Modified: Tue, 13 Aug 2024 10:26:28 GMT  
		Size: 3.8 MB (3787356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03cbdb302244d21da4fdf43fdfb2872c28958607938c6e753ef13ec9f4f5662d`  
		Last Modified: Tue, 13 Aug 2024 10:26:27 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-slim-bookworm`

```console
$ docker pull rust@sha256:24a6f218b9812adadf974ec395972383c309082abaa1934a71366fe72f5520ee
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

### `rust:1.80-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:c843545c3459df49f242e5f65abfaefab8daf6762fd02c9e7cc7d61ab0231f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280199925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aad58829b68dd23972cf2fce1aff495d6acfa7a892b4f6c1559aba9bc3c91c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f892dead4dc7447d193bf1eee68dee3497b9aacd74640651a96a4361e0247a`  
		Last Modified: Tue, 13 Aug 2024 01:24:04 GMT  
		Size: 251.1 MB (251073693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1116ce021e26ccb4836af6a2a2a1cb7b01897da0f16b0acd3399dda83f4119ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9084ce95a43595419649c640801fee62d71f4680fcb3c826faf482dbe2dea8f`

```dockerfile
```

-	Layers:
	-	`sha256:8430a84b3cd2e32e3552a659255ca153d6e1270686be4e1eba1b91f41e4d86a7`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 3.9 MB (3945031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd8e5703942249a8168a5ab26c53e4bd1aec67480b9f77fef010c375be43429`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ce61929bbf18fe2f71f3baf22ff0d922a23184b7a363659c4a89f061b592e620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289207527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21f40a92b064aab4ee6ffd996bc602bf2792f21275c7b9cdc43d00de4740e5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:06 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Tue, 23 Jul 2024 03:03:07 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce921058f79778f084b125986b13bbbc385e2af4323a43e8ba3619b56c4f9958`  
		Last Modified: Thu, 08 Aug 2024 23:13:34 GMT  
		Size: 264.5 MB (264489327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c6158e3d52946464ea2a084549b57e9b5a7a316d4d5c8687ab55759dce5a1b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c38b348c9f5b9bc8beed607cad78c1693495c300cdc56085d09c4c7185f357`

```dockerfile
```

-	Layers:
	-	`sha256:d9b2fa0740b793cb1f22595581639ae59968ced32677bac7867b15035147130a`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 3.8 MB (3761488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8627724826143f20c71410a776275bf988fc9b607322f492cf1b8b257db26806`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:8a838c35cdd6830f0c38cad489c6c61bb175e743b780e073e32325fda2030c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290939264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0711696e0f062a8fb4b8c457f1c655fa9fad0526477a4f4d1667c274350f8270`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c971093bb3eb1663f53feb24b7ec49c5c9d286fba9596e358485ba6c1df7ed98`  
		Last Modified: Tue, 13 Aug 2024 01:24:20 GMT  
		Size: 260.8 MB (260794983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c4b3f242d70526b2339549f2604d7eba5a09f1de1186638c21daef66c3ba4b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b39d8c066404d4bc719b8cd01f0d98568d81fec2b83a3fefc3e35779e95f96c`

```dockerfile
```

-	Layers:
	-	`sha256:f9143b5f37e30ff289509b5218f09b93034d2d775abd7b8b6d86df7e022a6448`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 3.9 MB (3926444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778dc71a73defbef6ddf88850ce25d585cce872fcdf0d89813f8c98e9f83f889`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d6e98cbd14d47879216d00da246bc59421df36932dc01b1487ebfc231096ba57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292898154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872774294942018a3bd21ad695b897a5b10b030cdae2cbfe7f9d19d3482a84b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df685a4d1a2a8bd237a5de9d5ddcec381181a53967e15a25c69a7d0bd6a6c47`  
		Last Modified: Tue, 13 Aug 2024 12:47:08 GMT  
		Size: 259.8 MB (259775854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d6e0eb2b2891ffb94f956f0ba3c7355c065c7819f5cdab82ce2b7e84b4f97b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87410e542a7a1f5e4786ef0c08d3c8e777220a50b2d36be9ece3713441efe5d`

```dockerfile
```

-	Layers:
	-	`sha256:bcd74365e2bfd97dee5ee0949156a9b2ae95479d7fb80b76ebfa4879fcbf541a`  
		Last Modified: Tue, 13 Aug 2024 12:47:02 GMT  
		Size: 3.9 MB (3917193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e101befb9e09ce3290dc45010a760b1d168781e5168d7a7b0188f9a00d3847`  
		Last Modified: Tue, 13 Aug 2024 12:47:01 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:eed01104c2dff5d47cad9cde6259fe152acdbffee61a32ccde4bf0df37e56f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340723676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec325392296c2da7203a1653034f9eb71d67c5e7da3a999fb2e08517d5794a58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e46961b207b826f317f9ddb2a562a2d81899099ed73257d6da8457c24e45e0c`  
		Last Modified: Tue, 13 Aug 2024 10:26:32 GMT  
		Size: 313.2 MB (313233579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:21c53034f7aa6da4784a46d7576ef1148a2f3dc58095a4bfd2fc98e624f3bf08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0090555459333f4a328dd0853b7ad2dbae4eb2d6c022b03a387ab0d1b97ea6e`

```dockerfile
```

-	Layers:
	-	`sha256:b71e18ae5a72712b53981379eeb88d9dc9c733fde3f2ba3bd3a1600f45aa4e5b`  
		Last Modified: Tue, 13 Aug 2024 10:26:28 GMT  
		Size: 3.8 MB (3787356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03cbdb302244d21da4fdf43fdfb2872c28958607938c6e753ef13ec9f4f5662d`  
		Last Modified: Tue, 13 Aug 2024 10:26:27 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-slim-bullseye`

```console
$ docker pull rust@sha256:2e03809b8850da918e5e3cf51d72f56fa89c50a0fd6043ba746b32b0eba325f2
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

### `rust:1.80-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:d6f66b9a8a080c54c17b7193ff57dd8c3160430b45db053d03f2721abd743a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271859645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c003508b7a8f691ad62a0eed4fa69e0d54ec27655f65d990a81d24994b64c61f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addb778fc66febdc6f1c2108c2c9d5ace21494739f320298cb4ff8c12241e592`  
		Last Modified: Tue, 13 Aug 2024 01:24:03 GMT  
		Size: 240.4 MB (240431358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:261ba66ea47b4f291dce74dfe5a0d5f2e68805f23ce59b0e5d23cf9a89254fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe7e7eb7b0f76624b32e911f5e554d351784720dbb382c7d1c1734cc7b8f532`

```dockerfile
```

-	Layers:
	-	`sha256:5b733f3cf156538fccc1809d173deaca4cb1c82de082355b20850a6e7c5da1e2`  
		Last Modified: Tue, 13 Aug 2024 01:23:59 GMT  
		Size: 4.2 MB (4164313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7acec69afed99d3c5670a73b375dbccdd8be76d552522b6ac93356fdc0debf7`  
		Last Modified: Tue, 13 Aug 2024 01:23:59 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:986d5f2381b37436bb8e34f8496af720c959d2b7c15b845b441e75b369b4b5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285517740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e696c058b2d5d16db2fe655314f747c1de6972798354d2a3936ebb13c5abb1d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:30 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Tue, 23 Jul 2024 03:03:30 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177377f17a0886d5eb4f3376f0b3abae7d0d7d4e4ac4caffea0a934ec2f7fca0`  
		Last Modified: Thu, 08 Aug 2024 23:09:20 GMT  
		Size: 258.9 MB (258928610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:36cfe3d0cd7c956d981d68f14407ba2857af81c06d1346e2544fb10e7f1b3ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d71ec4ba0a2208ed398f79b0ab349e1f079ca9b23beb584a4c2fe52b390b70`

```dockerfile
```

-	Layers:
	-	`sha256:150ddd50558ebecc4ce1407b5055277b0630ab26f76acbf0b3039e8bd670b66b`  
		Last Modified: Thu, 08 Aug 2024 23:09:14 GMT  
		Size: 4.0 MB (3973664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e54223131a68b8ea3b674333ffa6107f1eec517f9d9ef4af5e90347eca661016`  
		Last Modified: Thu, 08 Aug 2024 23:09:14 GMT  
		Size: 11.9 KB (11935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea400ae221974016cf01cfc99716046022430cc14de5608db498729f7618f668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.7 MB (335717687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290fe501a9234536387b5b30c99f27e439d23d64536b7815fe2de01d3682d07f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cb6cdc1948b06794974ff2e98a7005fb4728291f972fd9fe6890a51b35589`  
		Last Modified: Tue, 13 Aug 2024 11:45:59 GMT  
		Size: 305.6 MB (305641600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a3676673a581a4a22ae35dba326c5d9ccd2bdbde7ba9cfab0820cb96773f78ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621cc11386fc3351be6a2c44213e137c509b73cbc571f6de7541e04cbe8a4ac1`

```dockerfile
```

-	Layers:
	-	`sha256:25d0ce1b84cd190aa843a54b2f062344d99aacfdeb1f4215da7fc975e859651e`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 4.2 MB (4161095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66c9bde30e15c9a5a38892f97be33009492c2633b0fd4b560fb3907e93ecf62`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 12.2 KB (12175 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:ad0355bc000ca4ba51bbc0807b462d54262b6b5b62e73b32f506b869fc76d66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286389179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989eec17b76f290937e7bc846e971364efe1c2a25e1cc1b29fabac7b76f86a25`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:3c28079e98aa5b4ba96d948760be5fa7d7f99c878e193a63fab4f18eda2ee67e in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:1fff23531e74037071ba9be4ee63db5ccfd9c3823dceddfee08bed3fdeb6dea1`  
		Last Modified: Tue, 13 Aug 2024 00:43:17 GMT  
		Size: 32.4 MB (32413784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dad33f80b46deb53b484c36c78eb11195dd0235f166a822ec675fc08927191`  
		Last Modified: Tue, 13 Aug 2024 01:24:15 GMT  
		Size: 254.0 MB (253975395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7d5e3fc8fd195a69d23e3198c99399f9e930c4e5cd0fd5d152d7a1ada796c893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8ae1e1cb0895f077b29c9f421a61a78c4959247033e056c4da366f75634f97`

```dockerfile
```

-	Layers:
	-	`sha256:07625b7fe58e23a8c55b7286c8f8040a637b03a7c5809e152a08a580b900715e`  
		Last Modified: Tue, 13 Aug 2024 01:24:09 GMT  
		Size: 4.2 MB (4156081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8b284fa8fdb67251562fd31e46d6b1da860b97a19470f5d5063657bde4a63c9`  
		Last Modified: Tue, 13 Aug 2024 01:24:09 GMT  
		Size: 11.8 KB (11837 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:2e124406e413d8776b1b453199881fed5e310cccd6ff2cf89bbcd55e7779392c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281307733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b552eb51c1b8f762dd4d377b80e2d4c5efb0a328a7768155ed2af074d6e4698`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c654362147788e613020c1dfd3dbc701742f0f382576a6c8fc04270fa6971adc`  
		Last Modified: Tue, 13 Aug 2024 12:45:01 GMT  
		Size: 246.0 MB (246002600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fc1a61e4a6294cd56939edaacaf3806c8e09c8e0e819ec2ac682f79ff0652860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebc27d4fcc986991e662e4d513125eb2853de84f71c955ea5d8f365fe9347e3`

```dockerfile
```

-	Layers:
	-	`sha256:59027fbc6d8061aadd55edc122501d1f113062f9cf7e1bd2f47fff9b1adc0f2c`  
		Last Modified: Tue, 13 Aug 2024 12:44:55 GMT  
		Size: 4.1 MB (4125251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:508fdbef0798fce2e62a675348e13da7fd33785a7c7feefa1d4b6f8b722e159f`  
		Last Modified: Tue, 13 Aug 2024 12:44:55 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:f32b2cc38bf331c2dcff9a2576c73c3d99fcf712e8a0f950317fa9c5ed02761e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.2 MB (335152308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1a9f2b11e7d42b0db2c2f3775690e72d71b3a4f2b25b1f594542899c8a1de0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:a473fc09ddb0d1045f7f330f3a48b9cfe65ff9ea65cfa5c8262a8a5be9d4db75 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:83ea1b2f9d26c88827c9a658387c782a21fca528fbf7418f1a4eaea9a9818bdf`  
		Last Modified: Tue, 13 Aug 2024 00:47:58 GMT  
		Size: 29.7 MB (29668965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa1b7e0935282d5dc2e3ed32b65580c9c1c5de92e62d38b3a2733171400637a`  
		Last Modified: Tue, 13 Aug 2024 10:24:34 GMT  
		Size: 305.5 MB (305483343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d8e5509f37d18a1f09701710bca8d2f20d240c92f2ec7abbb27584f74a3bf65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088f2652d425afff66fa5c06441c9176a550540b0c3acf473f72b0f7f2679f63`

```dockerfile
```

-	Layers:
	-	`sha256:bdde162d496d13b73574bc4ebaf1594707c06da7ff0e2d1a126f3398c45b4896`  
		Last Modified: Tue, 13 Aug 2024 10:24:29 GMT  
		Size: 4.0 MB (3996088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63d2e6e316929c4003d9bac6b86c2fe1f7aa69ffc3070585e949f434945961b8`  
		Last Modified: Tue, 13 Aug 2024 10:24:29 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1`

```console
$ docker pull rust@sha256:536c1a47d86bcfcd08b00dc234c44db1f809d4d82e86bc27fac1bf93c5da4d4a
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

### `rust:1.80.1` - linux; amd64

```console
$ docker pull rust@sha256:06ccb5e3932bd75a2da9ff2baf4c4f19d03ad5486e634c340bffef9db8b50064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529281659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026a817e4bea1b6b749a75bc85d5ef64738daeecc409d9e869b7f9ef888452d2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed93aa58a52c9abc1ee472f1ac74b73d3adcccc2c30744498fd5f14f3f5d22c`  
		Last Modified: Tue, 13 Aug 2024 00:50:05 GMT  
		Size: 64.1 MB (64143347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c78da43830be6d988d34c7ee091f98d828516ce5478ca10a4933d655191bf`  
		Last Modified: Tue, 13 Aug 2024 00:50:40 GMT  
		Size: 211.2 MB (211241362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab98c54729822ef968838854f81888aefb579f47b191ad4a4d785cf5b971d523`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 180.3 MB (180292173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1` - unknown; unknown

```console
$ docker pull rust@sha256:477d7cc2994739a0c23215ad3f1b83d1ecefb0bfb50aed4dc5bcb8d34a8318a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64aa0734bc1145b915f5daf8c924a2fad004de7d0aa084c2538aee193839a0ba`

```dockerfile
```

-	Layers:
	-	`sha256:7d7901d0a1b95ff2f3e59aa16259137ba55255568135f630079010abda348131`  
		Last Modified: Tue, 13 Aug 2024 02:07:09 GMT  
		Size: 15.4 MB (15445633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0539b21bb7c1437f95afce8e66fadbc940a7d0f5c069da6b6cfc37b172a78d7d`  
		Last Modified: Tue, 13 Aug 2024 02:07:08 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1` - linux; arm variant v7

```console
$ docker pull rust@sha256:52635e3d536e65aabeda6035aebf16cfefa52222c80f2b7c89ba2aef49344566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997788d628f3ed7e3e69e5b548f993d57216a6d67d2a674cf1db410cd051f487`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:36:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdaec64288ad5c82e3a7f27432ae79c4867ba6c8f1a77e1dc0389e784b1c6dc`  
		Last Modified: Tue, 23 Jul 2024 03:48:08 GMT  
		Size: 175.2 MB (175182891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330aae2c516b379cdc6ab2ea46fe6022ca5abb5dd81f6ceb22b5dd684739dd6f`  
		Last Modified: Thu, 08 Aug 2024 23:11:40 GMT  
		Size: 216.6 MB (216645477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1` - unknown; unknown

```console
$ docker pull rust@sha256:777c64ed0d880c972519d3fc0915ff77029381f1998295b1cbf1ef488c1c2e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b185492ed5df011c125b1753979c70f76f8382d95f37e98be9e7571377ba3a5`

```dockerfile
```

-	Layers:
	-	`sha256:2a12347c74112b0705e33b5abeb4386ce4db740d9f6d70491c0ba2ae5d87a7b3`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc72b06301f35f899cd2a895a63bc1c3182667593d5a711266a98120479c2d6`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3718c2d7cb8ca07e18af18e39ad9d47978f5d6293ea08cf93388519b0bdeb69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cef39470d2a61e25ea969945765cd04d4a6812b36183f5649c80d93a2c4fb85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:04:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e903e4e709d192e5547602a5978c79692063228a98585f33fb02d343bc15719`  
		Last Modified: Tue, 23 Jul 2024 08:10:20 GMT  
		Size: 64.0 MB (63994288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adacb995432c92df6de0b5690abdd064e095988fac45631ba8fc0a0ffa9be5cc`  
		Last Modified: Tue, 23 Jul 2024 08:10:47 GMT  
		Size: 202.6 MB (202624227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005a0fa88074d27ab23eb9476d21dda069a977b29a14805ef8b69c9ee9de6f83`  
		Last Modified: Thu, 08 Aug 2024 20:19:32 GMT  
		Size: 249.9 MB (249924631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1` - unknown; unknown

```console
$ docker pull rust@sha256:bb0e18e62c512b219c4030e85aed77e21492e6c209f41c2bd97b4c6e419d75e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbad8ceff217f49198a0154e749dca9eed27634d53533f72d7b78371522c6b9f`

```dockerfile
```

-	Layers:
	-	`sha256:0164b6a3e90b84a2be124ea2398ab19c15b61667b9c8903e8bf0138f97c9ca12`  
		Last Modified: Thu, 08 Aug 2024 20:19:27 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc9866d976cc2a34ff099e2ebaa0e2da6cd1653a0fc3b9089324f3d72569970`  
		Last Modified: Thu, 08 Aug 2024 20:19:26 GMT  
		Size: 13.3 KB (13325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1` - linux; 386

```console
$ docker pull rust@sha256:6dbb08dc9881b5c188fd943932c6d7745f00ab49d037dafc08a2a25e431ddbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544805103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a7544afeb84426d1c9251a1a7fe8f5c9a00bf544f4392b8cc4e05997281ebc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e075b040ebfb55bbbc37499ceb62cce7e1b159d4e84ac39d21c750496a79bb79`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 210.2 MB (210154881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917938cdbf5dc24e60575067e6e20b28a79f6d94e7edd13a98999aca51d10f76`  
		Last Modified: Tue, 13 Aug 2024 02:07:27 GMT  
		Size: 193.2 MB (193190447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1` - unknown; unknown

```console
$ docker pull rust@sha256:76077e463500664db2b6e17edd6b8937466fc72fb68683e00a40c2640408e394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15437310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b5422b0a384f3899ccf52cde5aa27a1865208b4b4527d8687f5fd1b9ce517e`

```dockerfile
```

-	Layers:
	-	`sha256:4f164ab8d63ed169dfd8be585a981ebbbc797a2188b6bc3b480f38ad7d5d6b96`  
		Last Modified: Tue, 13 Aug 2024 02:07:23 GMT  
		Size: 15.4 MB (15424393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850c5335cc3ea66d6a561ea86473df5e0a4500b715b808ad7771431463e92f16`  
		Last Modified: Tue, 13 Aug 2024 02:07:22 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1` - linux; ppc64le

```console
$ docker pull rust@sha256:aabfcd7267b18899c0d5687bd04d90055d1c6a2bc5a6d00cfa25aeb095fd6c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554125432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfe1f9849979c55071de76ee36905890d5c20b129365588e8c37cb5baf3538c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:31:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98b19c7a350c0cd13610a34d9ca7ecb2491895327b24e7a8aa6c8e93c31678e`  
		Last Modified: Tue, 23 Jul 2024 02:42:57 GMT  
		Size: 214.3 MB (214264729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ecd62c101caf569db6b7baed93da3c1e32df39c40bfb200fe82ca215ba179c`  
		Last Modified: Thu, 08 Aug 2024 20:43:56 GMT  
		Size: 191.0 MB (191025895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1` - unknown; unknown

```console
$ docker pull rust@sha256:c6f065ccb862957415aa7d5700202f44c9742dbc678ec693544d019f39f58a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbe446c7d1251461e8a12f11a46b74a3f5bd0fa32c4f19972219fbef82b5642`

```dockerfile
```

-	Layers:
	-	`sha256:24c795cc9a6fd5df327f65e1543048107eeaa32312581d7c6fff3c56e1a915dd`  
		Last Modified: Thu, 08 Aug 2024 20:43:51 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02454961c6c66b24fb9862d190622f2fe224a0e61697c87bd092af1e82f5ebe0`  
		Last Modified: Thu, 08 Aug 2024 20:43:49 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1` - linux; s390x

```console
$ docker pull rust@sha256:a041f87038dd5aa50a7edb19a9a22b0e63f2114761c4c2c0909cc34c017d7f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581465886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ecfc031bdc4da9adb677c5ca252c80e59830349950b36490e5b4d73a8610db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:06:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f11437a649236e2e47148907f7f8038ee2ae1c54cb67398c9bab566828b04`  
		Last Modified: Tue, 23 Jul 2024 03:15:09 GMT  
		Size: 183.3 MB (183265308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85cf1eebdb2d2ebd65ba1cc5fe22e8faf7e89da74096c3782bd59753a6738ac`  
		Last Modified: Thu, 08 Aug 2024 21:07:20 GMT  
		Size: 263.1 MB (263095152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1` - unknown; unknown

```console
$ docker pull rust@sha256:2f6db1ed28cd7cef16c31848f4a3223802bdd4cae172692c376ee2060a23cf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf974f24f2e88f8e59aa1d28cd69bdd82f21f64f4ceb54498f33ee166751d4a`

```dockerfile
```

-	Layers:
	-	`sha256:671441fa02a185b806c430e150049dac27e7e423084c0808cc8953a1afe27b45`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4353db07ec2b290c585bf32df750773716984ed21a6c04397779e82aaa038b1`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-alpine`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.80.1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-alpine3.19`

```console
$ docker pull rust@sha256:b3ac1f65cf33390407c9b90558eb41e7a8311c47d836fca5800960f1aa2d11d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.80.1-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:25c79c9854cd4bedc797a88e2d4dc1b4502d22a540867fa66257e6e03c4c1d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279155377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204c24ee400cc1a13c13b275cb04657bc5e47150ce5a4e77d3a7671021b9a32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061bdf3a42c6c4489e9e78047cdaa3af6f7b63e5d255e0ab9e6660d180836f4`  
		Last Modified: Thu, 08 Aug 2024 20:02:39 GMT  
		Size: 55.3 MB (55346819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acee9c63bebda8ae8f027b6e99deee99e570d38430b1f5de3f271f853c530cc`  
		Last Modified: Thu, 08 Aug 2024 20:02:41 GMT  
		Size: 220.4 MB (220389518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:d7f847716cae21dc55ac84add1dab418798ef33b8624854fb6b8c65f17169302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b861f59014e11471235b45ca58fe55e1bce20e2d3235649938ddd8e10ac83b`

```dockerfile
```

-	Layers:
	-	`sha256:cda40d4b828cdfea673ac423a0571622627c241817509f9ba745a38be1560b4f`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e221181fdb20703a089d816b169375986ae47adf4002808cc72821fdf9b9e942`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1c9472feed43f2708eaa2821cf5f0a646160cee7be9d584bf730e755eedbee94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286589138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040de42a611e54d884e5a00d1765df3de096fba714c4defafc0750e79bcb340e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1b276de5f8a8a2fd3e6b931c4e180f78458c812dda2346f21361c13108618d`  
		Last Modified: Fri, 26 Jul 2024 00:29:37 GMT  
		Size: 53.0 MB (52995484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2abe5cb54c2cfbfce48a309498337e7a126ab4ea86b6df2ef36f1613354c5c4`  
		Last Modified: Thu, 08 Aug 2024 20:22:15 GMT  
		Size: 230.2 MB (230235196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:c808914252afc74e4ba729fb24e0bb95b91c9a2f8608b2a35bd39fc92b7d5a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27a7713ca3e5389a8f63774d2f2029f10a884a7ef5258c5a110ac3cc5fa9642`

```dockerfile
```

-	Layers:
	-	`sha256:dab1ad55931d3701c8a9c82cd1652b524d00f22c57bd6fc291789059b83165e3`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a90f930d575ecabd7599845ca4411c5bf521f8695acca03fbc6142619add3f7`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-alpine3.20`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.80.1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-bookworm`

```console
$ docker pull rust@sha256:536c1a47d86bcfcd08b00dc234c44db1f809d4d82e86bc27fac1bf93c5da4d4a
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

### `rust:1.80.1-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:06ccb5e3932bd75a2da9ff2baf4c4f19d03ad5486e634c340bffef9db8b50064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529281659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026a817e4bea1b6b749a75bc85d5ef64738daeecc409d9e869b7f9ef888452d2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed93aa58a52c9abc1ee472f1ac74b73d3adcccc2c30744498fd5f14f3f5d22c`  
		Last Modified: Tue, 13 Aug 2024 00:50:05 GMT  
		Size: 64.1 MB (64143347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c78da43830be6d988d34c7ee091f98d828516ce5478ca10a4933d655191bf`  
		Last Modified: Tue, 13 Aug 2024 00:50:40 GMT  
		Size: 211.2 MB (211241362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab98c54729822ef968838854f81888aefb579f47b191ad4a4d785cf5b971d523`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 180.3 MB (180292173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:477d7cc2994739a0c23215ad3f1b83d1ecefb0bfb50aed4dc5bcb8d34a8318a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64aa0734bc1145b915f5daf8c924a2fad004de7d0aa084c2538aee193839a0ba`

```dockerfile
```

-	Layers:
	-	`sha256:7d7901d0a1b95ff2f3e59aa16259137ba55255568135f630079010abda348131`  
		Last Modified: Tue, 13 Aug 2024 02:07:09 GMT  
		Size: 15.4 MB (15445633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0539b21bb7c1437f95afce8e66fadbc940a7d0f5c069da6b6cfc37b172a78d7d`  
		Last Modified: Tue, 13 Aug 2024 02:07:08 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:52635e3d536e65aabeda6035aebf16cfefa52222c80f2b7c89ba2aef49344566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997788d628f3ed7e3e69e5b548f993d57216a6d67d2a674cf1db410cd051f487`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:36:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdaec64288ad5c82e3a7f27432ae79c4867ba6c8f1a77e1dc0389e784b1c6dc`  
		Last Modified: Tue, 23 Jul 2024 03:48:08 GMT  
		Size: 175.2 MB (175182891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330aae2c516b379cdc6ab2ea46fe6022ca5abb5dd81f6ceb22b5dd684739dd6f`  
		Last Modified: Thu, 08 Aug 2024 23:11:40 GMT  
		Size: 216.6 MB (216645477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:777c64ed0d880c972519d3fc0915ff77029381f1998295b1cbf1ef488c1c2e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b185492ed5df011c125b1753979c70f76f8382d95f37e98be9e7571377ba3a5`

```dockerfile
```

-	Layers:
	-	`sha256:2a12347c74112b0705e33b5abeb4386ce4db740d9f6d70491c0ba2ae5d87a7b3`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc72b06301f35f899cd2a895a63bc1c3182667593d5a711266a98120479c2d6`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3718c2d7cb8ca07e18af18e39ad9d47978f5d6293ea08cf93388519b0bdeb69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cef39470d2a61e25ea969945765cd04d4a6812b36183f5649c80d93a2c4fb85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:04:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e903e4e709d192e5547602a5978c79692063228a98585f33fb02d343bc15719`  
		Last Modified: Tue, 23 Jul 2024 08:10:20 GMT  
		Size: 64.0 MB (63994288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adacb995432c92df6de0b5690abdd064e095988fac45631ba8fc0a0ffa9be5cc`  
		Last Modified: Tue, 23 Jul 2024 08:10:47 GMT  
		Size: 202.6 MB (202624227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005a0fa88074d27ab23eb9476d21dda069a977b29a14805ef8b69c9ee9de6f83`  
		Last Modified: Thu, 08 Aug 2024 20:19:32 GMT  
		Size: 249.9 MB (249924631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bb0e18e62c512b219c4030e85aed77e21492e6c209f41c2bd97b4c6e419d75e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbad8ceff217f49198a0154e749dca9eed27634d53533f72d7b78371522c6b9f`

```dockerfile
```

-	Layers:
	-	`sha256:0164b6a3e90b84a2be124ea2398ab19c15b61667b9c8903e8bf0138f97c9ca12`  
		Last Modified: Thu, 08 Aug 2024 20:19:27 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc9866d976cc2a34ff099e2ebaa0e2da6cd1653a0fc3b9089324f3d72569970`  
		Last Modified: Thu, 08 Aug 2024 20:19:26 GMT  
		Size: 13.3 KB (13325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:6dbb08dc9881b5c188fd943932c6d7745f00ab49d037dafc08a2a25e431ddbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544805103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a7544afeb84426d1c9251a1a7fe8f5c9a00bf544f4392b8cc4e05997281ebc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e075b040ebfb55bbbc37499ceb62cce7e1b159d4e84ac39d21c750496a79bb79`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 210.2 MB (210154881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917938cdbf5dc24e60575067e6e20b28a79f6d94e7edd13a98999aca51d10f76`  
		Last Modified: Tue, 13 Aug 2024 02:07:27 GMT  
		Size: 193.2 MB (193190447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:76077e463500664db2b6e17edd6b8937466fc72fb68683e00a40c2640408e394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15437310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b5422b0a384f3899ccf52cde5aa27a1865208b4b4527d8687f5fd1b9ce517e`

```dockerfile
```

-	Layers:
	-	`sha256:4f164ab8d63ed169dfd8be585a981ebbbc797a2188b6bc3b480f38ad7d5d6b96`  
		Last Modified: Tue, 13 Aug 2024 02:07:23 GMT  
		Size: 15.4 MB (15424393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850c5335cc3ea66d6a561ea86473df5e0a4500b715b808ad7771431463e92f16`  
		Last Modified: Tue, 13 Aug 2024 02:07:22 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:aabfcd7267b18899c0d5687bd04d90055d1c6a2bc5a6d00cfa25aeb095fd6c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554125432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfe1f9849979c55071de76ee36905890d5c20b129365588e8c37cb5baf3538c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:31:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98b19c7a350c0cd13610a34d9ca7ecb2491895327b24e7a8aa6c8e93c31678e`  
		Last Modified: Tue, 23 Jul 2024 02:42:57 GMT  
		Size: 214.3 MB (214264729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ecd62c101caf569db6b7baed93da3c1e32df39c40bfb200fe82ca215ba179c`  
		Last Modified: Thu, 08 Aug 2024 20:43:56 GMT  
		Size: 191.0 MB (191025895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c6f065ccb862957415aa7d5700202f44c9742dbc678ec693544d019f39f58a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbe446c7d1251461e8a12f11a46b74a3f5bd0fa32c4f19972219fbef82b5642`

```dockerfile
```

-	Layers:
	-	`sha256:24c795cc9a6fd5df327f65e1543048107eeaa32312581d7c6fff3c56e1a915dd`  
		Last Modified: Thu, 08 Aug 2024 20:43:51 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02454961c6c66b24fb9862d190622f2fe224a0e61697c87bd092af1e82f5ebe0`  
		Last Modified: Thu, 08 Aug 2024 20:43:49 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:a041f87038dd5aa50a7edb19a9a22b0e63f2114761c4c2c0909cc34c017d7f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581465886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ecfc031bdc4da9adb677c5ca252c80e59830349950b36490e5b4d73a8610db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:06:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f11437a649236e2e47148907f7f8038ee2ae1c54cb67398c9bab566828b04`  
		Last Modified: Tue, 23 Jul 2024 03:15:09 GMT  
		Size: 183.3 MB (183265308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85cf1eebdb2d2ebd65ba1cc5fe22e8faf7e89da74096c3782bd59753a6738ac`  
		Last Modified: Thu, 08 Aug 2024 21:07:20 GMT  
		Size: 263.1 MB (263095152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2f6db1ed28cd7cef16c31848f4a3223802bdd4cae172692c376ee2060a23cf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf974f24f2e88f8e59aa1d28cd69bdd82f21f64f4ceb54498f33ee166751d4a`

```dockerfile
```

-	Layers:
	-	`sha256:671441fa02a185b806c430e150049dac27e7e423084c0808cc8953a1afe27b45`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4353db07ec2b290c585bf32df750773716984ed21a6c04397779e82aaa038b1`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-bullseye`

```console
$ docker pull rust@sha256:de1606afadf25c846e6b430df25a9392e198afef8424f5164a3c397629bdf6f5
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

### `rust:1.80.1-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:8a01cbb1d1a0b0f20d0e85ac69474ca840d7e34dd1f3762d22ce624c13c417d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.8 MB (502777238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cf4e5177929d237aea9ee13011db71d6f4393b12bf0823f867c081979cfe68`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6665b6f4bd774e6a4c9738f0532ee622cf3bc07679e5a4449ba05c1f395e4f75`  
		Last Modified: Tue, 13 Aug 2024 00:51:07 GMT  
		Size: 54.6 MB (54588802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6864ced29689ec8b202ccbf73c58c0e8dc0b33400b46042d3cf659b11bbeb0`  
		Last Modified: Tue, 13 Aug 2024 00:51:37 GMT  
		Size: 197.0 MB (197047386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9332bfc0250a021ae7365e49946d877a2802c54970be6301f98a6377f3167b`  
		Last Modified: Tue, 13 Aug 2024 02:07:19 GMT  
		Size: 180.3 MB (180292122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:45c6625dc4c571c6e065eacd2c290d3b52e78721431672ef8f1aae6017189ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15064066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee08aba60fcfb9871b851fb9438503f2c42fd7ec55e838035d91709961fd4e6`

```dockerfile
```

-	Layers:
	-	`sha256:6178f196ed0702f5c1082757335355ef367c059eeb1a5c8a2eb4eff5841a0531`  
		Last Modified: Tue, 13 Aug 2024 02:07:15 GMT  
		Size: 15.1 MB (15052263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8725f5279633844314eff90b2dde2df13d1b317f50774f092d72fe4500515d5`  
		Last Modified: Tue, 13 Aug 2024 02:07:14 GMT  
		Size: 11.8 KB (11803 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:fc1c2ba8dbdab427e658f6e1072b478d8a2c7f044a23c2a71c044e1c28473be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.6 MB (499627303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d292f506565814f43ade875846ff70334e5d5ae1b0fc048cc5f736d62ec66b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:37:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:39:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a61d577d5393ca0b5e52e6cbd75569b7d9e9b50cb27f783d5482f5f97240ba0`  
		Last Modified: Tue, 23 Jul 2024 03:48:23 GMT  
		Size: 14.9 MB (14879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6354534da26fdc193140968c5b8a059bd98e1fc05e33deacad3b97f257fd35f`  
		Last Modified: Tue, 23 Jul 2024 03:48:44 GMT  
		Size: 50.4 MB (50357798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82623cfc0dda8411ed87ecde5f4fe0993f1ef9fe052103e7d162351520e9b5a`  
		Last Modified: Tue, 23 Jul 2024 03:49:26 GMT  
		Size: 167.5 MB (167501970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37b8df02c4399a603b03b4f34b372704cd35a452576506606d22fcae445377f`  
		Last Modified: Thu, 08 Aug 2024 23:07:33 GMT  
		Size: 216.6 MB (216645515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:462eebeecdde3963e3063b2490e1b6e0782c734d0dcf1048a0e33ac768815c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14865179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0932916c3084993fbcdc712e131a3e0bf6e66eaa0c6eb1d821a716d879d4cf`

```dockerfile
```

-	Layers:
	-	`sha256:1ceb9766ffc3c996f4eaebf55fe07450dd5e94eeea1a5b89b36c5fba53d689f6`  
		Last Modified: Thu, 08 Aug 2024 23:07:28 GMT  
		Size: 14.9 MB (14853305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfdb28ad04244bef9011ba332ec2910156e53b81f745250e98ccb568ad1c3c14`  
		Last Modified: Thu, 08 Aug 2024 23:07:28 GMT  
		Size: 11.9 KB (11874 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:0af877d93f5ad15b273900b5718fa54e9543053d6b60fdaf7d3933d324dd0e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564064898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e308a60ea5d4fc6acf5860b8590f8a62068a836d81ccfbff21d32e1554a0623b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:05:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c27a83c76abd51a72277b6a74eb7f88e560054e0d04383f64e2886877a20dd5`  
		Last Modified: Tue, 23 Jul 2024 08:11:04 GMT  
		Size: 15.7 MB (15749501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac540a55631c4cba93c7e4e4bf634300076d45e71db5f34f3c0d770eb826303`  
		Last Modified: Tue, 23 Jul 2024 08:11:17 GMT  
		Size: 54.7 MB (54694822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df233b2a5328fe9ae508771678b5a4faaefca18e64196b4ac65584baa5c8aa9f`  
		Last Modified: Tue, 23 Jul 2024 08:11:41 GMT  
		Size: 190.0 MB (189965935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293bb9bde419e7ff2bd1d11b0be5e624bbb4da022a57306810e8bf93edacae7`  
		Last Modified: Thu, 08 Aug 2024 20:16:15 GMT  
		Size: 249.9 MB (249924653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a81c950759245fe6bf71dc9a44290967120f9cf196ac6f9c3ec26cc9b9066cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15066748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1f155c7f42861ae71ae977b5327605eb7c0b08fd25d933a70fcabdfc74f7d3`

```dockerfile
```

-	Layers:
	-	`sha256:63e419ed617ca1448cb4e3de395d6c7eaa34a1e3863d78000db038b0dd28e597`  
		Last Modified: Thu, 08 Aug 2024 20:16:10 GMT  
		Size: 15.1 MB (15054632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c5431487765e54121cd0aa3eae0f911e3b5a461276e16d995252ff8bf1f0dd`  
		Last Modified: Thu, 08 Aug 2024 20:16:09 GMT  
		Size: 12.1 KB (12116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:738a3b16b04454270fc63b75e2a047da0e48b231aeceb616b7cc940f37555e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.4 MB (521413626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e90b11ef61715850ea288d0327fe4f6c66a3e58b76b713dcced59e1c160537a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d740897ef0cfebeecea08cfc67998814e44c45164f9dc7c044e9e2a0507541f4`  
		Last Modified: Tue, 13 Aug 2024 01:15:00 GMT  
		Size: 16.3 MB (16267943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dab982039e3c0ad98af0fa361fb64e7b9635b80923dca6744c230e0994f2bf3`  
		Last Modified: Tue, 13 Aug 2024 01:15:21 GMT  
		Size: 55.9 MB (55927707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29843169a9c8306d94c89194ed26f3e75a8d2afa2d64a020ecbfd7f77998e397`  
		Last Modified: Tue, 13 Aug 2024 01:16:03 GMT  
		Size: 200.0 MB (199953236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8aa7cdb2f4805ec070e522b08fb8df2daca6950383c02a67b5e53717344597`  
		Last Modified: Tue, 13 Aug 2024 02:07:17 GMT  
		Size: 193.2 MB (193190636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fdbf1d6b7f1e2e1b294e0f58085485d95dfab14af98d6b7e6be79004e5b974c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e2502e1e8009aa3dd9aa0e3e514e2377c2697e88143834ce72c62919176441`

```dockerfile
```

-	Layers:
	-	`sha256:d4ade476a4648ad687d599130798cfadeb31acd52e0a469ac39034d98da1d119`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 15.0 MB (15040800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b418326de281e7cea6502c3eaa68cef047f7645101d4f0e73ab3d714712e8f46`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 11.8 KB (11775 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:5d169b000fa22c36500111459fa54598015d9b9a58036c4fde316ea970715080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.0 MB (522015479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6628ed239b45a3bac424f61944be13339f4ff8a69b1ecaa56a2b0f910cfd9ce0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:34:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89f3ec0749e802be2768d4d8d990f300a55cd418831db42ee374e4bb81ab0a3`  
		Last Modified: Tue, 23 Jul 2024 02:43:09 GMT  
		Size: 16.8 MB (16765814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3543cad9c41f9c9127d1adde535bc13ac5b446330727c5083aafa4b8d005c62`  
		Last Modified: Tue, 23 Jul 2024 02:43:26 GMT  
		Size: 58.9 MB (58872667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8d0e14af4e3c68b0eae63b664f02cecf25bea995af2d28db767811530400f5`  
		Last Modified: Tue, 23 Jul 2024 02:44:02 GMT  
		Size: 196.4 MB (196396379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa1e7e00fb7dcb267da537ea7773b70fc23ef4911517cd47ca57e16f1737d39`  
		Last Modified: Thu, 08 Aug 2024 20:39:03 GMT  
		Size: 191.0 MB (191025932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6365a77354226047cb669dcd86f2834239435f66fc9b0006e2932140785087b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15031565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deab1a4e30e869095efe93fd7115bb6c4822d7adb53a741dd444ddfcc9962ed0`

```dockerfile
```

-	Layers:
	-	`sha256:920b9708e3e8034a1e85c6cd3eb284b4de4807a2573fc3cb3fcb14e7dec8c365`  
		Last Modified: Thu, 08 Aug 2024 20:38:41 GMT  
		Size: 15.0 MB (15019723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0df8b6335988c60b5f64fecffadff01292c331c5018206853c0a32330939873f`  
		Last Modified: Thu, 08 Aug 2024 20:38:40 GMT  
		Size: 11.8 KB (11842 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:921ebae07fbeba23dc69a361a9b0b36c8622aea3d650324d8be26f29f2435ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 MB (559194472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc3aa1912d381708f43b8a60cf18a4b8990c7ef65126c25b34133979bcd4eef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:07:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:08:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e924418f310f18ad368886d6df84cac76659f51225b0784a1e53ff07318533`  
		Last Modified: Tue, 23 Jul 2024 03:15:16 GMT  
		Size: 15.6 MB (15641720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af67dae0133d3a5f116411c20eed624558ce4a187db4fd8eb9a8d622a827e5f`  
		Last Modified: Tue, 23 Jul 2024 03:15:29 GMT  
		Size: 54.1 MB (54075295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d2fba31676a932e41fb57a433c1ba42080bc1e363d7a190b9c73795d53b569`  
		Last Modified: Tue, 23 Jul 2024 03:15:55 GMT  
		Size: 173.1 MB (173058357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01182cd8b35aac0f952d57ea2856b1cff0705e5fedb6acbe5036a8421dfa51c2`  
		Last Modified: Thu, 08 Aug 2024 21:02:30 GMT  
		Size: 263.1 MB (263095008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b1a3b3790ec214331ca9d1cde91e1b7dd7f754f5b4b8b22208eb03a9b0da7cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289c25562f9db8f60cc67dbe26ff26919bf469e2255ce9cfe5e7d316b1019cbe`

```dockerfile
```

-	Layers:
	-	`sha256:11856feef6838c72b7e993143fa557388e2eba83880de951658906e2eb4d308e`  
		Last Modified: Thu, 08 Aug 2024 21:02:26 GMT  
		Size: 14.9 MB (14873217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76bab5070fee4c9b12687acf21124bf4ab302cf66783848bd3a68de2e8d76da5`  
		Last Modified: Thu, 08 Aug 2024 21:02:26 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-slim`

```console
$ docker pull rust@sha256:24a6f218b9812adadf974ec395972383c309082abaa1934a71366fe72f5520ee
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

### `rust:1.80.1-slim` - linux; amd64

```console
$ docker pull rust@sha256:c843545c3459df49f242e5f65abfaefab8daf6762fd02c9e7cc7d61ab0231f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280199925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aad58829b68dd23972cf2fce1aff495d6acfa7a892b4f6c1559aba9bc3c91c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f892dead4dc7447d193bf1eee68dee3497b9aacd74640651a96a4361e0247a`  
		Last Modified: Tue, 13 Aug 2024 01:24:04 GMT  
		Size: 251.1 MB (251073693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:1116ce021e26ccb4836af6a2a2a1cb7b01897da0f16b0acd3399dda83f4119ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9084ce95a43595419649c640801fee62d71f4680fcb3c826faf482dbe2dea8f`

```dockerfile
```

-	Layers:
	-	`sha256:8430a84b3cd2e32e3552a659255ca153d6e1270686be4e1eba1b91f41e4d86a7`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 3.9 MB (3945031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd8e5703942249a8168a5ab26c53e4bd1aec67480b9f77fef010c375be43429`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:ce61929bbf18fe2f71f3baf22ff0d922a23184b7a363659c4a89f061b592e620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289207527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21f40a92b064aab4ee6ffd996bc602bf2792f21275c7b9cdc43d00de4740e5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:06 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Tue, 23 Jul 2024 03:03:07 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce921058f79778f084b125986b13bbbc385e2af4323a43e8ba3619b56c4f9958`  
		Last Modified: Thu, 08 Aug 2024 23:13:34 GMT  
		Size: 264.5 MB (264489327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:c6158e3d52946464ea2a084549b57e9b5a7a316d4d5c8687ab55759dce5a1b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c38b348c9f5b9bc8beed607cad78c1693495c300cdc56085d09c4c7185f357`

```dockerfile
```

-	Layers:
	-	`sha256:d9b2fa0740b793cb1f22595581639ae59968ced32677bac7867b15035147130a`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 3.8 MB (3761488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8627724826143f20c71410a776275bf988fc9b607322f492cf1b8b257db26806`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim` - linux; 386

```console
$ docker pull rust@sha256:8a838c35cdd6830f0c38cad489c6c61bb175e743b780e073e32325fda2030c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290939264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0711696e0f062a8fb4b8c457f1c655fa9fad0526477a4f4d1667c274350f8270`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c971093bb3eb1663f53feb24b7ec49c5c9d286fba9596e358485ba6c1df7ed98`  
		Last Modified: Tue, 13 Aug 2024 01:24:20 GMT  
		Size: 260.8 MB (260794983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:c4b3f242d70526b2339549f2604d7eba5a09f1de1186638c21daef66c3ba4b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b39d8c066404d4bc719b8cd01f0d98568d81fec2b83a3fefc3e35779e95f96c`

```dockerfile
```

-	Layers:
	-	`sha256:f9143b5f37e30ff289509b5218f09b93034d2d775abd7b8b6d86df7e022a6448`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 3.9 MB (3926444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778dc71a73defbef6ddf88850ce25d585cce872fcdf0d89813f8c98e9f83f889`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:d6e98cbd14d47879216d00da246bc59421df36932dc01b1487ebfc231096ba57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292898154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872774294942018a3bd21ad695b897a5b10b030cdae2cbfe7f9d19d3482a84b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df685a4d1a2a8bd237a5de9d5ddcec381181a53967e15a25c69a7d0bd6a6c47`  
		Last Modified: Tue, 13 Aug 2024 12:47:08 GMT  
		Size: 259.8 MB (259775854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:d6e0eb2b2891ffb94f956f0ba3c7355c065c7819f5cdab82ce2b7e84b4f97b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87410e542a7a1f5e4786ef0c08d3c8e777220a50b2d36be9ece3713441efe5d`

```dockerfile
```

-	Layers:
	-	`sha256:bcd74365e2bfd97dee5ee0949156a9b2ae95479d7fb80b76ebfa4879fcbf541a`  
		Last Modified: Tue, 13 Aug 2024 12:47:02 GMT  
		Size: 3.9 MB (3917193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e101befb9e09ce3290dc45010a760b1d168781e5168d7a7b0188f9a00d3847`  
		Last Modified: Tue, 13 Aug 2024 12:47:01 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim` - linux; s390x

```console
$ docker pull rust@sha256:eed01104c2dff5d47cad9cde6259fe152acdbffee61a32ccde4bf0df37e56f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340723676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec325392296c2da7203a1653034f9eb71d67c5e7da3a999fb2e08517d5794a58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e46961b207b826f317f9ddb2a562a2d81899099ed73257d6da8457c24e45e0c`  
		Last Modified: Tue, 13 Aug 2024 10:26:32 GMT  
		Size: 313.2 MB (313233579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:21c53034f7aa6da4784a46d7576ef1148a2f3dc58095a4bfd2fc98e624f3bf08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0090555459333f4a328dd0853b7ad2dbae4eb2d6c022b03a387ab0d1b97ea6e`

```dockerfile
```

-	Layers:
	-	`sha256:b71e18ae5a72712b53981379eeb88d9dc9c733fde3f2ba3bd3a1600f45aa4e5b`  
		Last Modified: Tue, 13 Aug 2024 10:26:28 GMT  
		Size: 3.8 MB (3787356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03cbdb302244d21da4fdf43fdfb2872c28958607938c6e753ef13ec9f4f5662d`  
		Last Modified: Tue, 13 Aug 2024 10:26:27 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-slim-bookworm`

```console
$ docker pull rust@sha256:24a6f218b9812adadf974ec395972383c309082abaa1934a71366fe72f5520ee
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

### `rust:1.80.1-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:c843545c3459df49f242e5f65abfaefab8daf6762fd02c9e7cc7d61ab0231f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280199925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aad58829b68dd23972cf2fce1aff495d6acfa7a892b4f6c1559aba9bc3c91c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f892dead4dc7447d193bf1eee68dee3497b9aacd74640651a96a4361e0247a`  
		Last Modified: Tue, 13 Aug 2024 01:24:04 GMT  
		Size: 251.1 MB (251073693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1116ce021e26ccb4836af6a2a2a1cb7b01897da0f16b0acd3399dda83f4119ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9084ce95a43595419649c640801fee62d71f4680fcb3c826faf482dbe2dea8f`

```dockerfile
```

-	Layers:
	-	`sha256:8430a84b3cd2e32e3552a659255ca153d6e1270686be4e1eba1b91f41e4d86a7`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 3.9 MB (3945031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd8e5703942249a8168a5ab26c53e4bd1aec67480b9f77fef010c375be43429`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ce61929bbf18fe2f71f3baf22ff0d922a23184b7a363659c4a89f061b592e620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289207527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21f40a92b064aab4ee6ffd996bc602bf2792f21275c7b9cdc43d00de4740e5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:06 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Tue, 23 Jul 2024 03:03:07 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce921058f79778f084b125986b13bbbc385e2af4323a43e8ba3619b56c4f9958`  
		Last Modified: Thu, 08 Aug 2024 23:13:34 GMT  
		Size: 264.5 MB (264489327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c6158e3d52946464ea2a084549b57e9b5a7a316d4d5c8687ab55759dce5a1b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c38b348c9f5b9bc8beed607cad78c1693495c300cdc56085d09c4c7185f357`

```dockerfile
```

-	Layers:
	-	`sha256:d9b2fa0740b793cb1f22595581639ae59968ced32677bac7867b15035147130a`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 3.8 MB (3761488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8627724826143f20c71410a776275bf988fc9b607322f492cf1b8b257db26806`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:8a838c35cdd6830f0c38cad489c6c61bb175e743b780e073e32325fda2030c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290939264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0711696e0f062a8fb4b8c457f1c655fa9fad0526477a4f4d1667c274350f8270`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c971093bb3eb1663f53feb24b7ec49c5c9d286fba9596e358485ba6c1df7ed98`  
		Last Modified: Tue, 13 Aug 2024 01:24:20 GMT  
		Size: 260.8 MB (260794983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c4b3f242d70526b2339549f2604d7eba5a09f1de1186638c21daef66c3ba4b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b39d8c066404d4bc719b8cd01f0d98568d81fec2b83a3fefc3e35779e95f96c`

```dockerfile
```

-	Layers:
	-	`sha256:f9143b5f37e30ff289509b5218f09b93034d2d775abd7b8b6d86df7e022a6448`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 3.9 MB (3926444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778dc71a73defbef6ddf88850ce25d585cce872fcdf0d89813f8c98e9f83f889`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d6e98cbd14d47879216d00da246bc59421df36932dc01b1487ebfc231096ba57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292898154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872774294942018a3bd21ad695b897a5b10b030cdae2cbfe7f9d19d3482a84b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df685a4d1a2a8bd237a5de9d5ddcec381181a53967e15a25c69a7d0bd6a6c47`  
		Last Modified: Tue, 13 Aug 2024 12:47:08 GMT  
		Size: 259.8 MB (259775854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d6e0eb2b2891ffb94f956f0ba3c7355c065c7819f5cdab82ce2b7e84b4f97b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87410e542a7a1f5e4786ef0c08d3c8e777220a50b2d36be9ece3713441efe5d`

```dockerfile
```

-	Layers:
	-	`sha256:bcd74365e2bfd97dee5ee0949156a9b2ae95479d7fb80b76ebfa4879fcbf541a`  
		Last Modified: Tue, 13 Aug 2024 12:47:02 GMT  
		Size: 3.9 MB (3917193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e101befb9e09ce3290dc45010a760b1d168781e5168d7a7b0188f9a00d3847`  
		Last Modified: Tue, 13 Aug 2024 12:47:01 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:eed01104c2dff5d47cad9cde6259fe152acdbffee61a32ccde4bf0df37e56f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340723676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec325392296c2da7203a1653034f9eb71d67c5e7da3a999fb2e08517d5794a58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e46961b207b826f317f9ddb2a562a2d81899099ed73257d6da8457c24e45e0c`  
		Last Modified: Tue, 13 Aug 2024 10:26:32 GMT  
		Size: 313.2 MB (313233579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:21c53034f7aa6da4784a46d7576ef1148a2f3dc58095a4bfd2fc98e624f3bf08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0090555459333f4a328dd0853b7ad2dbae4eb2d6c022b03a387ab0d1b97ea6e`

```dockerfile
```

-	Layers:
	-	`sha256:b71e18ae5a72712b53981379eeb88d9dc9c733fde3f2ba3bd3a1600f45aa4e5b`  
		Last Modified: Tue, 13 Aug 2024 10:26:28 GMT  
		Size: 3.8 MB (3787356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03cbdb302244d21da4fdf43fdfb2872c28958607938c6e753ef13ec9f4f5662d`  
		Last Modified: Tue, 13 Aug 2024 10:26:27 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-slim-bullseye`

```console
$ docker pull rust@sha256:2e03809b8850da918e5e3cf51d72f56fa89c50a0fd6043ba746b32b0eba325f2
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

### `rust:1.80.1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:d6f66b9a8a080c54c17b7193ff57dd8c3160430b45db053d03f2721abd743a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271859645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c003508b7a8f691ad62a0eed4fa69e0d54ec27655f65d990a81d24994b64c61f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addb778fc66febdc6f1c2108c2c9d5ace21494739f320298cb4ff8c12241e592`  
		Last Modified: Tue, 13 Aug 2024 01:24:03 GMT  
		Size: 240.4 MB (240431358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:261ba66ea47b4f291dce74dfe5a0d5f2e68805f23ce59b0e5d23cf9a89254fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe7e7eb7b0f76624b32e911f5e554d351784720dbb382c7d1c1734cc7b8f532`

```dockerfile
```

-	Layers:
	-	`sha256:5b733f3cf156538fccc1809d173deaca4cb1c82de082355b20850a6e7c5da1e2`  
		Last Modified: Tue, 13 Aug 2024 01:23:59 GMT  
		Size: 4.2 MB (4164313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7acec69afed99d3c5670a73b375dbccdd8be76d552522b6ac93356fdc0debf7`  
		Last Modified: Tue, 13 Aug 2024 01:23:59 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:986d5f2381b37436bb8e34f8496af720c959d2b7c15b845b441e75b369b4b5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285517740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e696c058b2d5d16db2fe655314f747c1de6972798354d2a3936ebb13c5abb1d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:30 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Tue, 23 Jul 2024 03:03:30 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177377f17a0886d5eb4f3376f0b3abae7d0d7d4e4ac4caffea0a934ec2f7fca0`  
		Last Modified: Thu, 08 Aug 2024 23:09:20 GMT  
		Size: 258.9 MB (258928610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:36cfe3d0cd7c956d981d68f14407ba2857af81c06d1346e2544fb10e7f1b3ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d71ec4ba0a2208ed398f79b0ab349e1f079ca9b23beb584a4c2fe52b390b70`

```dockerfile
```

-	Layers:
	-	`sha256:150ddd50558ebecc4ce1407b5055277b0630ab26f76acbf0b3039e8bd670b66b`  
		Last Modified: Thu, 08 Aug 2024 23:09:14 GMT  
		Size: 4.0 MB (3973664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e54223131a68b8ea3b674333ffa6107f1eec517f9d9ef4af5e90347eca661016`  
		Last Modified: Thu, 08 Aug 2024 23:09:14 GMT  
		Size: 11.9 KB (11935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea400ae221974016cf01cfc99716046022430cc14de5608db498729f7618f668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.7 MB (335717687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290fe501a9234536387b5b30c99f27e439d23d64536b7815fe2de01d3682d07f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cb6cdc1948b06794974ff2e98a7005fb4728291f972fd9fe6890a51b35589`  
		Last Modified: Tue, 13 Aug 2024 11:45:59 GMT  
		Size: 305.6 MB (305641600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a3676673a581a4a22ae35dba326c5d9ccd2bdbde7ba9cfab0820cb96773f78ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621cc11386fc3351be6a2c44213e137c509b73cbc571f6de7541e04cbe8a4ac1`

```dockerfile
```

-	Layers:
	-	`sha256:25d0ce1b84cd190aa843a54b2f062344d99aacfdeb1f4215da7fc975e859651e`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 4.2 MB (4161095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66c9bde30e15c9a5a38892f97be33009492c2633b0fd4b560fb3907e93ecf62`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 12.2 KB (12175 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:ad0355bc000ca4ba51bbc0807b462d54262b6b5b62e73b32f506b869fc76d66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286389179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989eec17b76f290937e7bc846e971364efe1c2a25e1cc1b29fabac7b76f86a25`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:3c28079e98aa5b4ba96d948760be5fa7d7f99c878e193a63fab4f18eda2ee67e in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:1fff23531e74037071ba9be4ee63db5ccfd9c3823dceddfee08bed3fdeb6dea1`  
		Last Modified: Tue, 13 Aug 2024 00:43:17 GMT  
		Size: 32.4 MB (32413784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dad33f80b46deb53b484c36c78eb11195dd0235f166a822ec675fc08927191`  
		Last Modified: Tue, 13 Aug 2024 01:24:15 GMT  
		Size: 254.0 MB (253975395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7d5e3fc8fd195a69d23e3198c99399f9e930c4e5cd0fd5d152d7a1ada796c893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8ae1e1cb0895f077b29c9f421a61a78c4959247033e056c4da366f75634f97`

```dockerfile
```

-	Layers:
	-	`sha256:07625b7fe58e23a8c55b7286c8f8040a637b03a7c5809e152a08a580b900715e`  
		Last Modified: Tue, 13 Aug 2024 01:24:09 GMT  
		Size: 4.2 MB (4156081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8b284fa8fdb67251562fd31e46d6b1da860b97a19470f5d5063657bde4a63c9`  
		Last Modified: Tue, 13 Aug 2024 01:24:09 GMT  
		Size: 11.8 KB (11837 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:2e124406e413d8776b1b453199881fed5e310cccd6ff2cf89bbcd55e7779392c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281307733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b552eb51c1b8f762dd4d377b80e2d4c5efb0a328a7768155ed2af074d6e4698`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c654362147788e613020c1dfd3dbc701742f0f382576a6c8fc04270fa6971adc`  
		Last Modified: Tue, 13 Aug 2024 12:45:01 GMT  
		Size: 246.0 MB (246002600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fc1a61e4a6294cd56939edaacaf3806c8e09c8e0e819ec2ac682f79ff0652860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebc27d4fcc986991e662e4d513125eb2853de84f71c955ea5d8f365fe9347e3`

```dockerfile
```

-	Layers:
	-	`sha256:59027fbc6d8061aadd55edc122501d1f113062f9cf7e1bd2f47fff9b1adc0f2c`  
		Last Modified: Tue, 13 Aug 2024 12:44:55 GMT  
		Size: 4.1 MB (4125251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:508fdbef0798fce2e62a675348e13da7fd33785a7c7feefa1d4b6f8b722e159f`  
		Last Modified: Tue, 13 Aug 2024 12:44:55 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:f32b2cc38bf331c2dcff9a2576c73c3d99fcf712e8a0f950317fa9c5ed02761e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.2 MB (335152308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1a9f2b11e7d42b0db2c2f3775690e72d71b3a4f2b25b1f594542899c8a1de0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:a473fc09ddb0d1045f7f330f3a48b9cfe65ff9ea65cfa5c8262a8a5be9d4db75 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:83ea1b2f9d26c88827c9a658387c782a21fca528fbf7418f1a4eaea9a9818bdf`  
		Last Modified: Tue, 13 Aug 2024 00:47:58 GMT  
		Size: 29.7 MB (29668965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa1b7e0935282d5dc2e3ed32b65580c9c1c5de92e62d38b3a2733171400637a`  
		Last Modified: Tue, 13 Aug 2024 10:24:34 GMT  
		Size: 305.5 MB (305483343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d8e5509f37d18a1f09701710bca8d2f20d240c92f2ec7abbb27584f74a3bf65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088f2652d425afff66fa5c06441c9176a550540b0c3acf473f72b0f7f2679f63`

```dockerfile
```

-	Layers:
	-	`sha256:bdde162d496d13b73574bc4ebaf1594707c06da7ff0e2d1a126f3398c45b4896`  
		Last Modified: Tue, 13 Aug 2024 10:24:29 GMT  
		Size: 4.0 MB (3996088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63d2e6e316929c4003d9bac6b86c2fe1f7aa69ffc3070585e949f434945961b8`  
		Last Modified: Tue, 13 Aug 2024 10:24:29 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.19`

```console
$ docker pull rust@sha256:b3ac1f65cf33390407c9b90558eb41e7a8311c47d836fca5800960f1aa2d11d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:25c79c9854cd4bedc797a88e2d4dc1b4502d22a540867fa66257e6e03c4c1d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279155377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204c24ee400cc1a13c13b275cb04657bc5e47150ce5a4e77d3a7671021b9a32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061bdf3a42c6c4489e9e78047cdaa3af6f7b63e5d255e0ab9e6660d180836f4`  
		Last Modified: Thu, 08 Aug 2024 20:02:39 GMT  
		Size: 55.3 MB (55346819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acee9c63bebda8ae8f027b6e99deee99e570d38430b1f5de3f271f853c530cc`  
		Last Modified: Thu, 08 Aug 2024 20:02:41 GMT  
		Size: 220.4 MB (220389518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:d7f847716cae21dc55ac84add1dab418798ef33b8624854fb6b8c65f17169302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b861f59014e11471235b45ca58fe55e1bce20e2d3235649938ddd8e10ac83b`

```dockerfile
```

-	Layers:
	-	`sha256:cda40d4b828cdfea673ac423a0571622627c241817509f9ba745a38be1560b4f`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e221181fdb20703a089d816b169375986ae47adf4002808cc72821fdf9b9e942`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1c9472feed43f2708eaa2821cf5f0a646160cee7be9d584bf730e755eedbee94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286589138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040de42a611e54d884e5a00d1765df3de096fba714c4defafc0750e79bcb340e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1b276de5f8a8a2fd3e6b931c4e180f78458c812dda2346f21361c13108618d`  
		Last Modified: Fri, 26 Jul 2024 00:29:37 GMT  
		Size: 53.0 MB (52995484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2abe5cb54c2cfbfce48a309498337e7a126ab4ea86b6df2ef36f1613354c5c4`  
		Last Modified: Thu, 08 Aug 2024 20:22:15 GMT  
		Size: 230.2 MB (230235196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:c808914252afc74e4ba729fb24e0bb95b91c9a2f8608b2a35bd39fc92b7d5a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27a7713ca3e5389a8f63774d2f2029f10a884a7ef5258c5a110ac3cc5fa9642`

```dockerfile
```

-	Layers:
	-	`sha256:dab1ad55931d3701c8a9c82cd1652b524d00f22c57bd6fc291789059b83165e3`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a90f930d575ecabd7599845ca4411c5bf521f8695acca03fbc6142619add3f7`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.20`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:536c1a47d86bcfcd08b00dc234c44db1f809d4d82e86bc27fac1bf93c5da4d4a
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
$ docker pull rust@sha256:06ccb5e3932bd75a2da9ff2baf4c4f19d03ad5486e634c340bffef9db8b50064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529281659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026a817e4bea1b6b749a75bc85d5ef64738daeecc409d9e869b7f9ef888452d2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed93aa58a52c9abc1ee472f1ac74b73d3adcccc2c30744498fd5f14f3f5d22c`  
		Last Modified: Tue, 13 Aug 2024 00:50:05 GMT  
		Size: 64.1 MB (64143347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c78da43830be6d988d34c7ee091f98d828516ce5478ca10a4933d655191bf`  
		Last Modified: Tue, 13 Aug 2024 00:50:40 GMT  
		Size: 211.2 MB (211241362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab98c54729822ef968838854f81888aefb579f47b191ad4a4d785cf5b971d523`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 180.3 MB (180292173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:477d7cc2994739a0c23215ad3f1b83d1ecefb0bfb50aed4dc5bcb8d34a8318a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64aa0734bc1145b915f5daf8c924a2fad004de7d0aa084c2538aee193839a0ba`

```dockerfile
```

-	Layers:
	-	`sha256:7d7901d0a1b95ff2f3e59aa16259137ba55255568135f630079010abda348131`  
		Last Modified: Tue, 13 Aug 2024 02:07:09 GMT  
		Size: 15.4 MB (15445633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0539b21bb7c1437f95afce8e66fadbc940a7d0f5c069da6b6cfc37b172a78d7d`  
		Last Modified: Tue, 13 Aug 2024 02:07:08 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:52635e3d536e65aabeda6035aebf16cfefa52222c80f2b7c89ba2aef49344566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997788d628f3ed7e3e69e5b548f993d57216a6d67d2a674cf1db410cd051f487`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:36:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdaec64288ad5c82e3a7f27432ae79c4867ba6c8f1a77e1dc0389e784b1c6dc`  
		Last Modified: Tue, 23 Jul 2024 03:48:08 GMT  
		Size: 175.2 MB (175182891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330aae2c516b379cdc6ab2ea46fe6022ca5abb5dd81f6ceb22b5dd684739dd6f`  
		Last Modified: Thu, 08 Aug 2024 23:11:40 GMT  
		Size: 216.6 MB (216645477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:777c64ed0d880c972519d3fc0915ff77029381f1998295b1cbf1ef488c1c2e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b185492ed5df011c125b1753979c70f76f8382d95f37e98be9e7571377ba3a5`

```dockerfile
```

-	Layers:
	-	`sha256:2a12347c74112b0705e33b5abeb4386ce4db740d9f6d70491c0ba2ae5d87a7b3`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc72b06301f35f899cd2a895a63bc1c3182667593d5a711266a98120479c2d6`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3718c2d7cb8ca07e18af18e39ad9d47978f5d6293ea08cf93388519b0bdeb69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cef39470d2a61e25ea969945765cd04d4a6812b36183f5649c80d93a2c4fb85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:04:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e903e4e709d192e5547602a5978c79692063228a98585f33fb02d343bc15719`  
		Last Modified: Tue, 23 Jul 2024 08:10:20 GMT  
		Size: 64.0 MB (63994288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adacb995432c92df6de0b5690abdd064e095988fac45631ba8fc0a0ffa9be5cc`  
		Last Modified: Tue, 23 Jul 2024 08:10:47 GMT  
		Size: 202.6 MB (202624227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005a0fa88074d27ab23eb9476d21dda069a977b29a14805ef8b69c9ee9de6f83`  
		Last Modified: Thu, 08 Aug 2024 20:19:32 GMT  
		Size: 249.9 MB (249924631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bb0e18e62c512b219c4030e85aed77e21492e6c209f41c2bd97b4c6e419d75e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbad8ceff217f49198a0154e749dca9eed27634d53533f72d7b78371522c6b9f`

```dockerfile
```

-	Layers:
	-	`sha256:0164b6a3e90b84a2be124ea2398ab19c15b61667b9c8903e8bf0138f97c9ca12`  
		Last Modified: Thu, 08 Aug 2024 20:19:27 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc9866d976cc2a34ff099e2ebaa0e2da6cd1653a0fc3b9089324f3d72569970`  
		Last Modified: Thu, 08 Aug 2024 20:19:26 GMT  
		Size: 13.3 KB (13325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:6dbb08dc9881b5c188fd943932c6d7745f00ab49d037dafc08a2a25e431ddbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544805103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a7544afeb84426d1c9251a1a7fe8f5c9a00bf544f4392b8cc4e05997281ebc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e075b040ebfb55bbbc37499ceb62cce7e1b159d4e84ac39d21c750496a79bb79`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 210.2 MB (210154881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917938cdbf5dc24e60575067e6e20b28a79f6d94e7edd13a98999aca51d10f76`  
		Last Modified: Tue, 13 Aug 2024 02:07:27 GMT  
		Size: 193.2 MB (193190447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:76077e463500664db2b6e17edd6b8937466fc72fb68683e00a40c2640408e394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15437310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b5422b0a384f3899ccf52cde5aa27a1865208b4b4527d8687f5fd1b9ce517e`

```dockerfile
```

-	Layers:
	-	`sha256:4f164ab8d63ed169dfd8be585a981ebbbc797a2188b6bc3b480f38ad7d5d6b96`  
		Last Modified: Tue, 13 Aug 2024 02:07:23 GMT  
		Size: 15.4 MB (15424393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850c5335cc3ea66d6a561ea86473df5e0a4500b715b808ad7771431463e92f16`  
		Last Modified: Tue, 13 Aug 2024 02:07:22 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:aabfcd7267b18899c0d5687bd04d90055d1c6a2bc5a6d00cfa25aeb095fd6c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554125432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfe1f9849979c55071de76ee36905890d5c20b129365588e8c37cb5baf3538c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:31:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98b19c7a350c0cd13610a34d9ca7ecb2491895327b24e7a8aa6c8e93c31678e`  
		Last Modified: Tue, 23 Jul 2024 02:42:57 GMT  
		Size: 214.3 MB (214264729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ecd62c101caf569db6b7baed93da3c1e32df39c40bfb200fe82ca215ba179c`  
		Last Modified: Thu, 08 Aug 2024 20:43:56 GMT  
		Size: 191.0 MB (191025895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c6f065ccb862957415aa7d5700202f44c9742dbc678ec693544d019f39f58a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbe446c7d1251461e8a12f11a46b74a3f5bd0fa32c4f19972219fbef82b5642`

```dockerfile
```

-	Layers:
	-	`sha256:24c795cc9a6fd5df327f65e1543048107eeaa32312581d7c6fff3c56e1a915dd`  
		Last Modified: Thu, 08 Aug 2024 20:43:51 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02454961c6c66b24fb9862d190622f2fe224a0e61697c87bd092af1e82f5ebe0`  
		Last Modified: Thu, 08 Aug 2024 20:43:49 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:a041f87038dd5aa50a7edb19a9a22b0e63f2114761c4c2c0909cc34c017d7f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581465886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ecfc031bdc4da9adb677c5ca252c80e59830349950b36490e5b4d73a8610db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:06:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f11437a649236e2e47148907f7f8038ee2ae1c54cb67398c9bab566828b04`  
		Last Modified: Tue, 23 Jul 2024 03:15:09 GMT  
		Size: 183.3 MB (183265308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85cf1eebdb2d2ebd65ba1cc5fe22e8faf7e89da74096c3782bd59753a6738ac`  
		Last Modified: Thu, 08 Aug 2024 21:07:20 GMT  
		Size: 263.1 MB (263095152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2f6db1ed28cd7cef16c31848f4a3223802bdd4cae172692c376ee2060a23cf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf974f24f2e88f8e59aa1d28cd69bdd82f21f64f4ceb54498f33ee166751d4a`

```dockerfile
```

-	Layers:
	-	`sha256:671441fa02a185b806c430e150049dac27e7e423084c0808cc8953a1afe27b45`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4353db07ec2b290c585bf32df750773716984ed21a6c04397779e82aaa038b1`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:de1606afadf25c846e6b430df25a9392e198afef8424f5164a3c397629bdf6f5
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
$ docker pull rust@sha256:8a01cbb1d1a0b0f20d0e85ac69474ca840d7e34dd1f3762d22ce624c13c417d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.8 MB (502777238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cf4e5177929d237aea9ee13011db71d6f4393b12bf0823f867c081979cfe68`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6665b6f4bd774e6a4c9738f0532ee622cf3bc07679e5a4449ba05c1f395e4f75`  
		Last Modified: Tue, 13 Aug 2024 00:51:07 GMT  
		Size: 54.6 MB (54588802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6864ced29689ec8b202ccbf73c58c0e8dc0b33400b46042d3cf659b11bbeb0`  
		Last Modified: Tue, 13 Aug 2024 00:51:37 GMT  
		Size: 197.0 MB (197047386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9332bfc0250a021ae7365e49946d877a2802c54970be6301f98a6377f3167b`  
		Last Modified: Tue, 13 Aug 2024 02:07:19 GMT  
		Size: 180.3 MB (180292122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:45c6625dc4c571c6e065eacd2c290d3b52e78721431672ef8f1aae6017189ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15064066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee08aba60fcfb9871b851fb9438503f2c42fd7ec55e838035d91709961fd4e6`

```dockerfile
```

-	Layers:
	-	`sha256:6178f196ed0702f5c1082757335355ef367c059eeb1a5c8a2eb4eff5841a0531`  
		Last Modified: Tue, 13 Aug 2024 02:07:15 GMT  
		Size: 15.1 MB (15052263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8725f5279633844314eff90b2dde2df13d1b317f50774f092d72fe4500515d5`  
		Last Modified: Tue, 13 Aug 2024 02:07:14 GMT  
		Size: 11.8 KB (11803 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:fc1c2ba8dbdab427e658f6e1072b478d8a2c7f044a23c2a71c044e1c28473be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.6 MB (499627303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d292f506565814f43ade875846ff70334e5d5ae1b0fc048cc5f736d62ec66b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:37:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:39:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a61d577d5393ca0b5e52e6cbd75569b7d9e9b50cb27f783d5482f5f97240ba0`  
		Last Modified: Tue, 23 Jul 2024 03:48:23 GMT  
		Size: 14.9 MB (14879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6354534da26fdc193140968c5b8a059bd98e1fc05e33deacad3b97f257fd35f`  
		Last Modified: Tue, 23 Jul 2024 03:48:44 GMT  
		Size: 50.4 MB (50357798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82623cfc0dda8411ed87ecde5f4fe0993f1ef9fe052103e7d162351520e9b5a`  
		Last Modified: Tue, 23 Jul 2024 03:49:26 GMT  
		Size: 167.5 MB (167501970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37b8df02c4399a603b03b4f34b372704cd35a452576506606d22fcae445377f`  
		Last Modified: Thu, 08 Aug 2024 23:07:33 GMT  
		Size: 216.6 MB (216645515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:462eebeecdde3963e3063b2490e1b6e0782c734d0dcf1048a0e33ac768815c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14865179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0932916c3084993fbcdc712e131a3e0bf6e66eaa0c6eb1d821a716d879d4cf`

```dockerfile
```

-	Layers:
	-	`sha256:1ceb9766ffc3c996f4eaebf55fe07450dd5e94eeea1a5b89b36c5fba53d689f6`  
		Last Modified: Thu, 08 Aug 2024 23:07:28 GMT  
		Size: 14.9 MB (14853305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfdb28ad04244bef9011ba332ec2910156e53b81f745250e98ccb568ad1c3c14`  
		Last Modified: Thu, 08 Aug 2024 23:07:28 GMT  
		Size: 11.9 KB (11874 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:0af877d93f5ad15b273900b5718fa54e9543053d6b60fdaf7d3933d324dd0e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564064898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e308a60ea5d4fc6acf5860b8590f8a62068a836d81ccfbff21d32e1554a0623b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:05:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c27a83c76abd51a72277b6a74eb7f88e560054e0d04383f64e2886877a20dd5`  
		Last Modified: Tue, 23 Jul 2024 08:11:04 GMT  
		Size: 15.7 MB (15749501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac540a55631c4cba93c7e4e4bf634300076d45e71db5f34f3c0d770eb826303`  
		Last Modified: Tue, 23 Jul 2024 08:11:17 GMT  
		Size: 54.7 MB (54694822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df233b2a5328fe9ae508771678b5a4faaefca18e64196b4ac65584baa5c8aa9f`  
		Last Modified: Tue, 23 Jul 2024 08:11:41 GMT  
		Size: 190.0 MB (189965935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293bb9bde419e7ff2bd1d11b0be5e624bbb4da022a57306810e8bf93edacae7`  
		Last Modified: Thu, 08 Aug 2024 20:16:15 GMT  
		Size: 249.9 MB (249924653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a81c950759245fe6bf71dc9a44290967120f9cf196ac6f9c3ec26cc9b9066cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15066748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1f155c7f42861ae71ae977b5327605eb7c0b08fd25d933a70fcabdfc74f7d3`

```dockerfile
```

-	Layers:
	-	`sha256:63e419ed617ca1448cb4e3de395d6c7eaa34a1e3863d78000db038b0dd28e597`  
		Last Modified: Thu, 08 Aug 2024 20:16:10 GMT  
		Size: 15.1 MB (15054632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c5431487765e54121cd0aa3eae0f911e3b5a461276e16d995252ff8bf1f0dd`  
		Last Modified: Thu, 08 Aug 2024 20:16:09 GMT  
		Size: 12.1 KB (12116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:738a3b16b04454270fc63b75e2a047da0e48b231aeceb616b7cc940f37555e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.4 MB (521413626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e90b11ef61715850ea288d0327fe4f6c66a3e58b76b713dcced59e1c160537a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d740897ef0cfebeecea08cfc67998814e44c45164f9dc7c044e9e2a0507541f4`  
		Last Modified: Tue, 13 Aug 2024 01:15:00 GMT  
		Size: 16.3 MB (16267943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dab982039e3c0ad98af0fa361fb64e7b9635b80923dca6744c230e0994f2bf3`  
		Last Modified: Tue, 13 Aug 2024 01:15:21 GMT  
		Size: 55.9 MB (55927707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29843169a9c8306d94c89194ed26f3e75a8d2afa2d64a020ecbfd7f77998e397`  
		Last Modified: Tue, 13 Aug 2024 01:16:03 GMT  
		Size: 200.0 MB (199953236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8aa7cdb2f4805ec070e522b08fb8df2daca6950383c02a67b5e53717344597`  
		Last Modified: Tue, 13 Aug 2024 02:07:17 GMT  
		Size: 193.2 MB (193190636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fdbf1d6b7f1e2e1b294e0f58085485d95dfab14af98d6b7e6be79004e5b974c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e2502e1e8009aa3dd9aa0e3e514e2377c2697e88143834ce72c62919176441`

```dockerfile
```

-	Layers:
	-	`sha256:d4ade476a4648ad687d599130798cfadeb31acd52e0a469ac39034d98da1d119`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 15.0 MB (15040800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b418326de281e7cea6502c3eaa68cef047f7645101d4f0e73ab3d714712e8f46`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 11.8 KB (11775 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:5d169b000fa22c36500111459fa54598015d9b9a58036c4fde316ea970715080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.0 MB (522015479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6628ed239b45a3bac424f61944be13339f4ff8a69b1ecaa56a2b0f910cfd9ce0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:34:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89f3ec0749e802be2768d4d8d990f300a55cd418831db42ee374e4bb81ab0a3`  
		Last Modified: Tue, 23 Jul 2024 02:43:09 GMT  
		Size: 16.8 MB (16765814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3543cad9c41f9c9127d1adde535bc13ac5b446330727c5083aafa4b8d005c62`  
		Last Modified: Tue, 23 Jul 2024 02:43:26 GMT  
		Size: 58.9 MB (58872667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8d0e14af4e3c68b0eae63b664f02cecf25bea995af2d28db767811530400f5`  
		Last Modified: Tue, 23 Jul 2024 02:44:02 GMT  
		Size: 196.4 MB (196396379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa1e7e00fb7dcb267da537ea7773b70fc23ef4911517cd47ca57e16f1737d39`  
		Last Modified: Thu, 08 Aug 2024 20:39:03 GMT  
		Size: 191.0 MB (191025932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6365a77354226047cb669dcd86f2834239435f66fc9b0006e2932140785087b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15031565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deab1a4e30e869095efe93fd7115bb6c4822d7adb53a741dd444ddfcc9962ed0`

```dockerfile
```

-	Layers:
	-	`sha256:920b9708e3e8034a1e85c6cd3eb284b4de4807a2573fc3cb3fcb14e7dec8c365`  
		Last Modified: Thu, 08 Aug 2024 20:38:41 GMT  
		Size: 15.0 MB (15019723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0df8b6335988c60b5f64fecffadff01292c331c5018206853c0a32330939873f`  
		Last Modified: Thu, 08 Aug 2024 20:38:40 GMT  
		Size: 11.8 KB (11842 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; s390x

```console
$ docker pull rust@sha256:921ebae07fbeba23dc69a361a9b0b36c8622aea3d650324d8be26f29f2435ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 MB (559194472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc3aa1912d381708f43b8a60cf18a4b8990c7ef65126c25b34133979bcd4eef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:07:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:08:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e924418f310f18ad368886d6df84cac76659f51225b0784a1e53ff07318533`  
		Last Modified: Tue, 23 Jul 2024 03:15:16 GMT  
		Size: 15.6 MB (15641720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af67dae0133d3a5f116411c20eed624558ce4a187db4fd8eb9a8d622a827e5f`  
		Last Modified: Tue, 23 Jul 2024 03:15:29 GMT  
		Size: 54.1 MB (54075295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d2fba31676a932e41fb57a433c1ba42080bc1e363d7a190b9c73795d53b569`  
		Last Modified: Tue, 23 Jul 2024 03:15:55 GMT  
		Size: 173.1 MB (173058357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01182cd8b35aac0f952d57ea2856b1cff0705e5fedb6acbe5036a8421dfa51c2`  
		Last Modified: Thu, 08 Aug 2024 21:02:30 GMT  
		Size: 263.1 MB (263095008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b1a3b3790ec214331ca9d1cde91e1b7dd7f754f5b4b8b22208eb03a9b0da7cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289c25562f9db8f60cc67dbe26ff26919bf469e2255ce9cfe5e7d316b1019cbe`

```dockerfile
```

-	Layers:
	-	`sha256:11856feef6838c72b7e993143fa557388e2eba83880de951658906e2eb4d308e`  
		Last Modified: Thu, 08 Aug 2024 21:02:26 GMT  
		Size: 14.9 MB (14873217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76bab5070fee4c9b12687acf21124bf4ab302cf66783848bd3a68de2e8d76da5`  
		Last Modified: Thu, 08 Aug 2024 21:02:26 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:536c1a47d86bcfcd08b00dc234c44db1f809d4d82e86bc27fac1bf93c5da4d4a
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
$ docker pull rust@sha256:06ccb5e3932bd75a2da9ff2baf4c4f19d03ad5486e634c340bffef9db8b50064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529281659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026a817e4bea1b6b749a75bc85d5ef64738daeecc409d9e869b7f9ef888452d2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed93aa58a52c9abc1ee472f1ac74b73d3adcccc2c30744498fd5f14f3f5d22c`  
		Last Modified: Tue, 13 Aug 2024 00:50:05 GMT  
		Size: 64.1 MB (64143347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c78da43830be6d988d34c7ee091f98d828516ce5478ca10a4933d655191bf`  
		Last Modified: Tue, 13 Aug 2024 00:50:40 GMT  
		Size: 211.2 MB (211241362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab98c54729822ef968838854f81888aefb579f47b191ad4a4d785cf5b971d523`  
		Last Modified: Tue, 13 Aug 2024 02:07:11 GMT  
		Size: 180.3 MB (180292173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:477d7cc2994739a0c23215ad3f1b83d1ecefb0bfb50aed4dc5bcb8d34a8318a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64aa0734bc1145b915f5daf8c924a2fad004de7d0aa084c2538aee193839a0ba`

```dockerfile
```

-	Layers:
	-	`sha256:7d7901d0a1b95ff2f3e59aa16259137ba55255568135f630079010abda348131`  
		Last Modified: Tue, 13 Aug 2024 02:07:09 GMT  
		Size: 15.4 MB (15445633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0539b21bb7c1437f95afce8e66fadbc940a7d0f5c069da6b6cfc37b172a78d7d`  
		Last Modified: Tue, 13 Aug 2024 02:07:08 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:52635e3d536e65aabeda6035aebf16cfefa52222c80f2b7c89ba2aef49344566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997788d628f3ed7e3e69e5b548f993d57216a6d67d2a674cf1db410cd051f487`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:36:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdaec64288ad5c82e3a7f27432ae79c4867ba6c8f1a77e1dc0389e784b1c6dc`  
		Last Modified: Tue, 23 Jul 2024 03:48:08 GMT  
		Size: 175.2 MB (175182891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330aae2c516b379cdc6ab2ea46fe6022ca5abb5dd81f6ceb22b5dd684739dd6f`  
		Last Modified: Thu, 08 Aug 2024 23:11:40 GMT  
		Size: 216.6 MB (216645477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:777c64ed0d880c972519d3fc0915ff77029381f1998295b1cbf1ef488c1c2e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b185492ed5df011c125b1753979c70f76f8382d95f37e98be9e7571377ba3a5`

```dockerfile
```

-	Layers:
	-	`sha256:2a12347c74112b0705e33b5abeb4386ce4db740d9f6d70491c0ba2ae5d87a7b3`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc72b06301f35f899cd2a895a63bc1c3182667593d5a711266a98120479c2d6`  
		Last Modified: Thu, 08 Aug 2024 23:11:35 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3718c2d7cb8ca07e18af18e39ad9d47978f5d6293ea08cf93388519b0bdeb69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cef39470d2a61e25ea969945765cd04d4a6812b36183f5649c80d93a2c4fb85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:04:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e903e4e709d192e5547602a5978c79692063228a98585f33fb02d343bc15719`  
		Last Modified: Tue, 23 Jul 2024 08:10:20 GMT  
		Size: 64.0 MB (63994288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adacb995432c92df6de0b5690abdd064e095988fac45631ba8fc0a0ffa9be5cc`  
		Last Modified: Tue, 23 Jul 2024 08:10:47 GMT  
		Size: 202.6 MB (202624227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005a0fa88074d27ab23eb9476d21dda069a977b29a14805ef8b69c9ee9de6f83`  
		Last Modified: Thu, 08 Aug 2024 20:19:32 GMT  
		Size: 249.9 MB (249924631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:bb0e18e62c512b219c4030e85aed77e21492e6c209f41c2bd97b4c6e419d75e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbad8ceff217f49198a0154e749dca9eed27634d53533f72d7b78371522c6b9f`

```dockerfile
```

-	Layers:
	-	`sha256:0164b6a3e90b84a2be124ea2398ab19c15b61667b9c8903e8bf0138f97c9ca12`  
		Last Modified: Thu, 08 Aug 2024 20:19:27 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc9866d976cc2a34ff099e2ebaa0e2da6cd1653a0fc3b9089324f3d72569970`  
		Last Modified: Thu, 08 Aug 2024 20:19:26 GMT  
		Size: 13.3 KB (13325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:6dbb08dc9881b5c188fd943932c6d7745f00ab49d037dafc08a2a25e431ddbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544805103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a7544afeb84426d1c9251a1a7fe8f5c9a00bf544f4392b8cc4e05997281ebc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e075b040ebfb55bbbc37499ceb62cce7e1b159d4e84ac39d21c750496a79bb79`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 210.2 MB (210154881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917938cdbf5dc24e60575067e6e20b28a79f6d94e7edd13a98999aca51d10f76`  
		Last Modified: Tue, 13 Aug 2024 02:07:27 GMT  
		Size: 193.2 MB (193190447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:76077e463500664db2b6e17edd6b8937466fc72fb68683e00a40c2640408e394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15437310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b5422b0a384f3899ccf52cde5aa27a1865208b4b4527d8687f5fd1b9ce517e`

```dockerfile
```

-	Layers:
	-	`sha256:4f164ab8d63ed169dfd8be585a981ebbbc797a2188b6bc3b480f38ad7d5d6b96`  
		Last Modified: Tue, 13 Aug 2024 02:07:23 GMT  
		Size: 15.4 MB (15424393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850c5335cc3ea66d6a561ea86473df5e0a4500b715b808ad7771431463e92f16`  
		Last Modified: Tue, 13 Aug 2024 02:07:22 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:aabfcd7267b18899c0d5687bd04d90055d1c6a2bc5a6d00cfa25aeb095fd6c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554125432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfe1f9849979c55071de76ee36905890d5c20b129365588e8c37cb5baf3538c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:31:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98b19c7a350c0cd13610a34d9ca7ecb2491895327b24e7a8aa6c8e93c31678e`  
		Last Modified: Tue, 23 Jul 2024 02:42:57 GMT  
		Size: 214.3 MB (214264729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ecd62c101caf569db6b7baed93da3c1e32df39c40bfb200fe82ca215ba179c`  
		Last Modified: Thu, 08 Aug 2024 20:43:56 GMT  
		Size: 191.0 MB (191025895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:c6f065ccb862957415aa7d5700202f44c9742dbc678ec693544d019f39f58a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbe446c7d1251461e8a12f11a46b74a3f5bd0fa32c4f19972219fbef82b5642`

```dockerfile
```

-	Layers:
	-	`sha256:24c795cc9a6fd5df327f65e1543048107eeaa32312581d7c6fff3c56e1a915dd`  
		Last Modified: Thu, 08 Aug 2024 20:43:51 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02454961c6c66b24fb9862d190622f2fe224a0e61697c87bd092af1e82f5ebe0`  
		Last Modified: Thu, 08 Aug 2024 20:43:49 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:a041f87038dd5aa50a7edb19a9a22b0e63f2114761c4c2c0909cc34c017d7f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581465886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ecfc031bdc4da9adb677c5ca252c80e59830349950b36490e5b4d73a8610db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:06:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f11437a649236e2e47148907f7f8038ee2ae1c54cb67398c9bab566828b04`  
		Last Modified: Tue, 23 Jul 2024 03:15:09 GMT  
		Size: 183.3 MB (183265308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85cf1eebdb2d2ebd65ba1cc5fe22e8faf7e89da74096c3782bd59753a6738ac`  
		Last Modified: Thu, 08 Aug 2024 21:07:20 GMT  
		Size: 263.1 MB (263095152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:2f6db1ed28cd7cef16c31848f4a3223802bdd4cae172692c376ee2060a23cf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf974f24f2e88f8e59aa1d28cd69bdd82f21f64f4ceb54498f33ee166751d4a`

```dockerfile
```

-	Layers:
	-	`sha256:671441fa02a185b806c430e150049dac27e7e423084c0808cc8953a1afe27b45`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4353db07ec2b290c585bf32df750773716984ed21a6c04397779e82aaa038b1`  
		Last Modified: Thu, 08 Aug 2024 21:07:16 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:24a6f218b9812adadf974ec395972383c309082abaa1934a71366fe72f5520ee
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
$ docker pull rust@sha256:c843545c3459df49f242e5f65abfaefab8daf6762fd02c9e7cc7d61ab0231f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280199925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aad58829b68dd23972cf2fce1aff495d6acfa7a892b4f6c1559aba9bc3c91c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f892dead4dc7447d193bf1eee68dee3497b9aacd74640651a96a4361e0247a`  
		Last Modified: Tue, 13 Aug 2024 01:24:04 GMT  
		Size: 251.1 MB (251073693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:1116ce021e26ccb4836af6a2a2a1cb7b01897da0f16b0acd3399dda83f4119ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9084ce95a43595419649c640801fee62d71f4680fcb3c826faf482dbe2dea8f`

```dockerfile
```

-	Layers:
	-	`sha256:8430a84b3cd2e32e3552a659255ca153d6e1270686be4e1eba1b91f41e4d86a7`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 3.9 MB (3945031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd8e5703942249a8168a5ab26c53e4bd1aec67480b9f77fef010c375be43429`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:ce61929bbf18fe2f71f3baf22ff0d922a23184b7a363659c4a89f061b592e620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289207527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21f40a92b064aab4ee6ffd996bc602bf2792f21275c7b9cdc43d00de4740e5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:06 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Tue, 23 Jul 2024 03:03:07 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce921058f79778f084b125986b13bbbc385e2af4323a43e8ba3619b56c4f9958`  
		Last Modified: Thu, 08 Aug 2024 23:13:34 GMT  
		Size: 264.5 MB (264489327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:c6158e3d52946464ea2a084549b57e9b5a7a316d4d5c8687ab55759dce5a1b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c38b348c9f5b9bc8beed607cad78c1693495c300cdc56085d09c4c7185f357`

```dockerfile
```

-	Layers:
	-	`sha256:d9b2fa0740b793cb1f22595581639ae59968ced32677bac7867b15035147130a`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 3.8 MB (3761488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8627724826143f20c71410a776275bf988fc9b607322f492cf1b8b257db26806`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:8a838c35cdd6830f0c38cad489c6c61bb175e743b780e073e32325fda2030c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290939264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0711696e0f062a8fb4b8c457f1c655fa9fad0526477a4f4d1667c274350f8270`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c971093bb3eb1663f53feb24b7ec49c5c9d286fba9596e358485ba6c1df7ed98`  
		Last Modified: Tue, 13 Aug 2024 01:24:20 GMT  
		Size: 260.8 MB (260794983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:c4b3f242d70526b2339549f2604d7eba5a09f1de1186638c21daef66c3ba4b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b39d8c066404d4bc719b8cd01f0d98568d81fec2b83a3fefc3e35779e95f96c`

```dockerfile
```

-	Layers:
	-	`sha256:f9143b5f37e30ff289509b5218f09b93034d2d775abd7b8b6d86df7e022a6448`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 3.9 MB (3926444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778dc71a73defbef6ddf88850ce25d585cce872fcdf0d89813f8c98e9f83f889`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:d6e98cbd14d47879216d00da246bc59421df36932dc01b1487ebfc231096ba57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292898154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872774294942018a3bd21ad695b897a5b10b030cdae2cbfe7f9d19d3482a84b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df685a4d1a2a8bd237a5de9d5ddcec381181a53967e15a25c69a7d0bd6a6c47`  
		Last Modified: Tue, 13 Aug 2024 12:47:08 GMT  
		Size: 259.8 MB (259775854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:d6e0eb2b2891ffb94f956f0ba3c7355c065c7819f5cdab82ce2b7e84b4f97b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87410e542a7a1f5e4786ef0c08d3c8e777220a50b2d36be9ece3713441efe5d`

```dockerfile
```

-	Layers:
	-	`sha256:bcd74365e2bfd97dee5ee0949156a9b2ae95479d7fb80b76ebfa4879fcbf541a`  
		Last Modified: Tue, 13 Aug 2024 12:47:02 GMT  
		Size: 3.9 MB (3917193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e101befb9e09ce3290dc45010a760b1d168781e5168d7a7b0188f9a00d3847`  
		Last Modified: Tue, 13 Aug 2024 12:47:01 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:eed01104c2dff5d47cad9cde6259fe152acdbffee61a32ccde4bf0df37e56f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340723676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec325392296c2da7203a1653034f9eb71d67c5e7da3a999fb2e08517d5794a58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e46961b207b826f317f9ddb2a562a2d81899099ed73257d6da8457c24e45e0c`  
		Last Modified: Tue, 13 Aug 2024 10:26:32 GMT  
		Size: 313.2 MB (313233579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:21c53034f7aa6da4784a46d7576ef1148a2f3dc58095a4bfd2fc98e624f3bf08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0090555459333f4a328dd0853b7ad2dbae4eb2d6c022b03a387ab0d1b97ea6e`

```dockerfile
```

-	Layers:
	-	`sha256:b71e18ae5a72712b53981379eeb88d9dc9c733fde3f2ba3bd3a1600f45aa4e5b`  
		Last Modified: Tue, 13 Aug 2024 10:26:28 GMT  
		Size: 3.8 MB (3787356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03cbdb302244d21da4fdf43fdfb2872c28958607938c6e753ef13ec9f4f5662d`  
		Last Modified: Tue, 13 Aug 2024 10:26:27 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:24a6f218b9812adadf974ec395972383c309082abaa1934a71366fe72f5520ee
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
$ docker pull rust@sha256:c843545c3459df49f242e5f65abfaefab8daf6762fd02c9e7cc7d61ab0231f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280199925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aad58829b68dd23972cf2fce1aff495d6acfa7a892b4f6c1559aba9bc3c91c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f892dead4dc7447d193bf1eee68dee3497b9aacd74640651a96a4361e0247a`  
		Last Modified: Tue, 13 Aug 2024 01:24:04 GMT  
		Size: 251.1 MB (251073693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1116ce021e26ccb4836af6a2a2a1cb7b01897da0f16b0acd3399dda83f4119ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9084ce95a43595419649c640801fee62d71f4680fcb3c826faf482dbe2dea8f`

```dockerfile
```

-	Layers:
	-	`sha256:8430a84b3cd2e32e3552a659255ca153d6e1270686be4e1eba1b91f41e4d86a7`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 3.9 MB (3945031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd8e5703942249a8168a5ab26c53e4bd1aec67480b9f77fef010c375be43429`  
		Last Modified: Tue, 13 Aug 2024 01:24:01 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ce61929bbf18fe2f71f3baf22ff0d922a23184b7a363659c4a89f061b592e620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289207527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21f40a92b064aab4ee6ffd996bc602bf2792f21275c7b9cdc43d00de4740e5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:06 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Tue, 23 Jul 2024 03:03:07 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce921058f79778f084b125986b13bbbc385e2af4323a43e8ba3619b56c4f9958`  
		Last Modified: Thu, 08 Aug 2024 23:13:34 GMT  
		Size: 264.5 MB (264489327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c6158e3d52946464ea2a084549b57e9b5a7a316d4d5c8687ab55759dce5a1b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c38b348c9f5b9bc8beed607cad78c1693495c300cdc56085d09c4c7185f357`

```dockerfile
```

-	Layers:
	-	`sha256:d9b2fa0740b793cb1f22595581639ae59968ced32677bac7867b15035147130a`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 3.8 MB (3761488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8627724826143f20c71410a776275bf988fc9b607322f492cf1b8b257db26806`  
		Last Modified: Thu, 08 Aug 2024 23:13:28 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:8a838c35cdd6830f0c38cad489c6c61bb175e743b780e073e32325fda2030c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290939264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0711696e0f062a8fb4b8c457f1c655fa9fad0526477a4f4d1667c274350f8270`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c971093bb3eb1663f53feb24b7ec49c5c9d286fba9596e358485ba6c1df7ed98`  
		Last Modified: Tue, 13 Aug 2024 01:24:20 GMT  
		Size: 260.8 MB (260794983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c4b3f242d70526b2339549f2604d7eba5a09f1de1186638c21daef66c3ba4b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b39d8c066404d4bc719b8cd01f0d98568d81fec2b83a3fefc3e35779e95f96c`

```dockerfile
```

-	Layers:
	-	`sha256:f9143b5f37e30ff289509b5218f09b93034d2d775abd7b8b6d86df7e022a6448`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 3.9 MB (3926444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778dc71a73defbef6ddf88850ce25d585cce872fcdf0d89813f8c98e9f83f889`  
		Last Modified: Tue, 13 Aug 2024 01:24:14 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d6e98cbd14d47879216d00da246bc59421df36932dc01b1487ebfc231096ba57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292898154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872774294942018a3bd21ad695b897a5b10b030cdae2cbfe7f9d19d3482a84b8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df685a4d1a2a8bd237a5de9d5ddcec381181a53967e15a25c69a7d0bd6a6c47`  
		Last Modified: Tue, 13 Aug 2024 12:47:08 GMT  
		Size: 259.8 MB (259775854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d6e0eb2b2891ffb94f956f0ba3c7355c065c7819f5cdab82ce2b7e84b4f97b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87410e542a7a1f5e4786ef0c08d3c8e777220a50b2d36be9ece3713441efe5d`

```dockerfile
```

-	Layers:
	-	`sha256:bcd74365e2bfd97dee5ee0949156a9b2ae95479d7fb80b76ebfa4879fcbf541a`  
		Last Modified: Tue, 13 Aug 2024 12:47:02 GMT  
		Size: 3.9 MB (3917193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e101befb9e09ce3290dc45010a760b1d168781e5168d7a7b0188f9a00d3847`  
		Last Modified: Tue, 13 Aug 2024 12:47:01 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:eed01104c2dff5d47cad9cde6259fe152acdbffee61a32ccde4bf0df37e56f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340723676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec325392296c2da7203a1653034f9eb71d67c5e7da3a999fb2e08517d5794a58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e46961b207b826f317f9ddb2a562a2d81899099ed73257d6da8457c24e45e0c`  
		Last Modified: Tue, 13 Aug 2024 10:26:32 GMT  
		Size: 313.2 MB (313233579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:21c53034f7aa6da4784a46d7576ef1148a2f3dc58095a4bfd2fc98e624f3bf08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0090555459333f4a328dd0853b7ad2dbae4eb2d6c022b03a387ab0d1b97ea6e`

```dockerfile
```

-	Layers:
	-	`sha256:b71e18ae5a72712b53981379eeb88d9dc9c733fde3f2ba3bd3a1600f45aa4e5b`  
		Last Modified: Tue, 13 Aug 2024 10:26:28 GMT  
		Size: 3.8 MB (3787356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03cbdb302244d21da4fdf43fdfb2872c28958607938c6e753ef13ec9f4f5662d`  
		Last Modified: Tue, 13 Aug 2024 10:26:27 GMT  
		Size: 13.1 KB (13053 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:2e03809b8850da918e5e3cf51d72f56fa89c50a0fd6043ba746b32b0eba325f2
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
$ docker pull rust@sha256:d6f66b9a8a080c54c17b7193ff57dd8c3160430b45db053d03f2721abd743a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271859645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c003508b7a8f691ad62a0eed4fa69e0d54ec27655f65d990a81d24994b64c61f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addb778fc66febdc6f1c2108c2c9d5ace21494739f320298cb4ff8c12241e592`  
		Last Modified: Tue, 13 Aug 2024 01:24:03 GMT  
		Size: 240.4 MB (240431358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:261ba66ea47b4f291dce74dfe5a0d5f2e68805f23ce59b0e5d23cf9a89254fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe7e7eb7b0f76624b32e911f5e554d351784720dbb382c7d1c1734cc7b8f532`

```dockerfile
```

-	Layers:
	-	`sha256:5b733f3cf156538fccc1809d173deaca4cb1c82de082355b20850a6e7c5da1e2`  
		Last Modified: Tue, 13 Aug 2024 01:23:59 GMT  
		Size: 4.2 MB (4164313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7acec69afed99d3c5670a73b375dbccdd8be76d552522b6ac93356fdc0debf7`  
		Last Modified: Tue, 13 Aug 2024 01:23:59 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:986d5f2381b37436bb8e34f8496af720c959d2b7c15b845b441e75b369b4b5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285517740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e696c058b2d5d16db2fe655314f747c1de6972798354d2a3936ebb13c5abb1d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:30 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Tue, 23 Jul 2024 03:03:30 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177377f17a0886d5eb4f3376f0b3abae7d0d7d4e4ac4caffea0a934ec2f7fca0`  
		Last Modified: Thu, 08 Aug 2024 23:09:20 GMT  
		Size: 258.9 MB (258928610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:36cfe3d0cd7c956d981d68f14407ba2857af81c06d1346e2544fb10e7f1b3ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d71ec4ba0a2208ed398f79b0ab349e1f079ca9b23beb584a4c2fe52b390b70`

```dockerfile
```

-	Layers:
	-	`sha256:150ddd50558ebecc4ce1407b5055277b0630ab26f76acbf0b3039e8bd670b66b`  
		Last Modified: Thu, 08 Aug 2024 23:09:14 GMT  
		Size: 4.0 MB (3973664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e54223131a68b8ea3b674333ffa6107f1eec517f9d9ef4af5e90347eca661016`  
		Last Modified: Thu, 08 Aug 2024 23:09:14 GMT  
		Size: 11.9 KB (11935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea400ae221974016cf01cfc99716046022430cc14de5608db498729f7618f668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.7 MB (335717687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290fe501a9234536387b5b30c99f27e439d23d64536b7815fe2de01d3682d07f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cb6cdc1948b06794974ff2e98a7005fb4728291f972fd9fe6890a51b35589`  
		Last Modified: Tue, 13 Aug 2024 11:45:59 GMT  
		Size: 305.6 MB (305641600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a3676673a581a4a22ae35dba326c5d9ccd2bdbde7ba9cfab0820cb96773f78ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621cc11386fc3351be6a2c44213e137c509b73cbc571f6de7541e04cbe8a4ac1`

```dockerfile
```

-	Layers:
	-	`sha256:25d0ce1b84cd190aa843a54b2f062344d99aacfdeb1f4215da7fc975e859651e`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 4.2 MB (4161095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66c9bde30e15c9a5a38892f97be33009492c2633b0fd4b560fb3907e93ecf62`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 12.2 KB (12175 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:ad0355bc000ca4ba51bbc0807b462d54262b6b5b62e73b32f506b869fc76d66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286389179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989eec17b76f290937e7bc846e971364efe1c2a25e1cc1b29fabac7b76f86a25`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:3c28079e98aa5b4ba96d948760be5fa7d7f99c878e193a63fab4f18eda2ee67e in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:1fff23531e74037071ba9be4ee63db5ccfd9c3823dceddfee08bed3fdeb6dea1`  
		Last Modified: Tue, 13 Aug 2024 00:43:17 GMT  
		Size: 32.4 MB (32413784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dad33f80b46deb53b484c36c78eb11195dd0235f166a822ec675fc08927191`  
		Last Modified: Tue, 13 Aug 2024 01:24:15 GMT  
		Size: 254.0 MB (253975395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7d5e3fc8fd195a69d23e3198c99399f9e930c4e5cd0fd5d152d7a1ada796c893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8ae1e1cb0895f077b29c9f421a61a78c4959247033e056c4da366f75634f97`

```dockerfile
```

-	Layers:
	-	`sha256:07625b7fe58e23a8c55b7286c8f8040a637b03a7c5809e152a08a580b900715e`  
		Last Modified: Tue, 13 Aug 2024 01:24:09 GMT  
		Size: 4.2 MB (4156081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8b284fa8fdb67251562fd31e46d6b1da860b97a19470f5d5063657bde4a63c9`  
		Last Modified: Tue, 13 Aug 2024 01:24:09 GMT  
		Size: 11.8 KB (11837 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:2e124406e413d8776b1b453199881fed5e310cccd6ff2cf89bbcd55e7779392c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281307733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b552eb51c1b8f762dd4d377b80e2d4c5efb0a328a7768155ed2af074d6e4698`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c654362147788e613020c1dfd3dbc701742f0f382576a6c8fc04270fa6971adc`  
		Last Modified: Tue, 13 Aug 2024 12:45:01 GMT  
		Size: 246.0 MB (246002600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fc1a61e4a6294cd56939edaacaf3806c8e09c8e0e819ec2ac682f79ff0652860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebc27d4fcc986991e662e4d513125eb2853de84f71c955ea5d8f365fe9347e3`

```dockerfile
```

-	Layers:
	-	`sha256:59027fbc6d8061aadd55edc122501d1f113062f9cf7e1bd2f47fff9b1adc0f2c`  
		Last Modified: Tue, 13 Aug 2024 12:44:55 GMT  
		Size: 4.1 MB (4125251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:508fdbef0798fce2e62a675348e13da7fd33785a7c7feefa1d4b6f8b722e159f`  
		Last Modified: Tue, 13 Aug 2024 12:44:55 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:f32b2cc38bf331c2dcff9a2576c73c3d99fcf712e8a0f950317fa9c5ed02761e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.2 MB (335152308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1a9f2b11e7d42b0db2c2f3775690e72d71b3a4f2b25b1f594542899c8a1de0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:a473fc09ddb0d1045f7f330f3a48b9cfe65ff9ea65cfa5c8262a8a5be9d4db75 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:83ea1b2f9d26c88827c9a658387c782a21fca528fbf7418f1a4eaea9a9818bdf`  
		Last Modified: Tue, 13 Aug 2024 00:47:58 GMT  
		Size: 29.7 MB (29668965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa1b7e0935282d5dc2e3ed32b65580c9c1c5de92e62d38b3a2733171400637a`  
		Last Modified: Tue, 13 Aug 2024 10:24:34 GMT  
		Size: 305.5 MB (305483343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d8e5509f37d18a1f09701710bca8d2f20d240c92f2ec7abbb27584f74a3bf65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088f2652d425afff66fa5c06441c9176a550540b0c3acf473f72b0f7f2679f63`

```dockerfile
```

-	Layers:
	-	`sha256:bdde162d496d13b73574bc4ebaf1594707c06da7ff0e2d1a126f3398c45b4896`  
		Last Modified: Tue, 13 Aug 2024 10:24:29 GMT  
		Size: 4.0 MB (3996088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63d2e6e316929c4003d9bac6b86c2fe1f7aa69ffc3070585e949f434945961b8`  
		Last Modified: Tue, 13 Aug 2024 10:24:29 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json
