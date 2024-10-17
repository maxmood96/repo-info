## `rust:1-bookworm`

```console
$ docker pull rust@sha256:4c1240ec53638d49bdc7e3e83dc05bc5705a75244db57bbc4634c0b84f67fea9
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
$ docker pull rust@sha256:9ec5f3c59961026a8b3e925736ed81575e23902138c7acb40a1de84dbdaacaae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.1 MB (606131321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e07219e2f7c36bddd76f5b3639eb0cec17b5335ee110a5b322ddc8192eaa3f7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
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
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a4688a74de76e26de6977ef8438b7e0161edaee4d986ee61e62bc0b84b1163`  
		Last Modified: Thu, 17 Oct 2024 01:51:23 GMT  
		Size: 25.7 MB (25709972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8022c20c080be7d80dd6512a4c9fed59039e755de95495c76a32f7c2baebf1`  
		Last Modified: Thu, 17 Oct 2024 01:51:43 GMT  
		Size: 69.8 MB (69829835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d27751f2c723de9cfb2cbb2775f1c16c1f3653cdff74eae652ff9cc1633eda6`  
		Last Modified: Thu, 17 Oct 2024 01:52:21 GMT  
		Size: 214.3 MB (214300830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c611a152413c976ff7ccb00877f76a6e0180e8de568f2e09d4b18f50c87dd38b`  
		Last Modified: Thu, 17 Oct 2024 13:52:47 GMT  
		Size: 242.7 MB (242735087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5aaa8b6d2b17c21f4ece284e4466bdb2bc14006f1d4fdee4d81c3b339005b3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15440408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97285688499d35118669ab9d834b3122eb457b1d4aadebe573fad79809ccce60`

```dockerfile
```

-	Layers:
	-	`sha256:2796700f6210389f2a34c61bea01c8a44c3a68b071d0dd6937d62839afa0e88b`  
		Last Modified: Thu, 17 Oct 2024 13:52:38 GMT  
		Size: 15.4 MB (15427343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98393b45ff7893dba079e6573f7fbff507288c94dd921c7fcc68acb40ccd0df3`  
		Last Modified: Thu, 17 Oct 2024 13:52:36 GMT  
		Size: 13.1 KB (13065 bytes)  
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
