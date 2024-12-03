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
-	[`rust:1.83`](#rust183)
-	[`rust:1.83-alpine`](#rust183-alpine)
-	[`rust:1.83-alpine3.19`](#rust183-alpine319)
-	[`rust:1.83-alpine3.20`](#rust183-alpine320)
-	[`rust:1.83-bookworm`](#rust183-bookworm)
-	[`rust:1.83-bullseye`](#rust183-bullseye)
-	[`rust:1.83-slim`](#rust183-slim)
-	[`rust:1.83-slim-bookworm`](#rust183-slim-bookworm)
-	[`rust:1.83-slim-bullseye`](#rust183-slim-bullseye)
-	[`rust:1.83.0`](#rust1830)
-	[`rust:1.83.0-alpine`](#rust1830-alpine)
-	[`rust:1.83.0-alpine3.19`](#rust1830-alpine319)
-	[`rust:1.83.0-alpine3.20`](#rust1830-alpine320)
-	[`rust:1.83.0-bookworm`](#rust1830-bookworm)
-	[`rust:1.83.0-bullseye`](#rust1830-bullseye)
-	[`rust:1.83.0-slim`](#rust1830-slim)
-	[`rust:1.83.0-slim-bookworm`](#rust1830-slim-bookworm)
-	[`rust:1.83.0-slim-bullseye`](#rust1830-slim-bullseye)
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
$ docker pull rust@sha256:d242a48452a5f6f490e1c13d3340d54ead1198948a4585dc42e326d6eacd07d1
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
$ docker pull rust@sha256:71aa4f8bdbfb924be55914e8910657aaf15420a87649ea1c64de6f3aef99b357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.7 MB (540737368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51381ded149a6148696b8fd088a50b9684925a0f5c26541db5d3a99db5aae059`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bc823accc52b76a805eb38c2d85f6916c18b62280e12ef86557cf7aae9f958b5`  
		Last Modified: Mon, 02 Dec 2024 20:24:37 GMT  
		Size: 191.4 MB (191418150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:6f2bd220e2f16cb7fe49a9b9ad87295829ed6ebf6b745b45163ccb5c6758e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2628cb17b709463f28662019efa1ac6f3499b61335860965970c347da12bc324`

```dockerfile
```

-	Layers:
	-	`sha256:286a3f2db2c8a6d92215bd0e79bef8cc02de285df8e4a1a45cf8e27b0ab0e625`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 15.5 MB (15500541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dea8927ea34a8749863f37f48d5c3386465f87be87fca83ebfb2da54e47f09`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:c4eab5718491261254547e9dee552013f246ffd187d3fe1c1427b2ca4b061ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526493619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b2f5c8fb2f32e205088f699538ac30a1f60f942ca99b46a7d63ee474294911`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:e64ed70b984c825bcf2c316778efdf694d1177f214c907b60097f528bbda5cf8`  
		Last Modified: Mon, 02 Dec 2024 20:29:54 GMT  
		Size: 224.5 MB (224498211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:be5458af59d7a9d4850ec727e792fe1ce39320e685eba63907c07a62c663a19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15317922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8513824646d633879f3b9c31a95e4313b646af70856500a177c618bb79ec94`

```dockerfile
```

-	Layers:
	-	`sha256:d5013ef9b8a7a070d15a1c43f9eb413d3814d5083868ad3477c7ca363e2629e8`  
		Last Modified: Mon, 02 Dec 2024 20:29:49 GMT  
		Size: 15.3 MB (15304676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a68401994195014fb21c06bdf19c124aea45e5bef8843f712d311bdfced543`  
		Last Modified: Mon, 02 Dec 2024 20:29:48 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f53e59e92e0aeabaf6660d225a107e99c545db88292aa0b26c622e74a040d965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 MB (592017331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c109228921d40f3351cd8c44731f364371c3d17735ca2a5e5f91c306a0dfbfa`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:73de18a65d13f2c8a09a8d948d31e3de3f45af2bead8f228a386915adb234c35`  
		Last Modified: Mon, 02 Dec 2024 20:35:51 GMT  
		Size: 251.8 MB (251804771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:c509b7be5dcd87df97728f5298103aa353944b0f8c8f7d25b5b4b7d797017c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15542437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6766be12848456f1e52235b69ad6e4a319291879e57f2a2238bef89da8f3f9e`

```dockerfile
```

-	Layers:
	-	`sha256:98ab1278bc14cd425e7f3eed1e29aae39b73c5f89b91ccc51caee870f35910be`  
		Last Modified: Mon, 02 Dec 2024 20:35:45 GMT  
		Size: 15.5 MB (15529147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9709d89560fe98a5ae0be73fdda845fa48e30c80363bbca1ff69fdb179217095`  
		Last Modified: Mon, 02 Dec 2024 20:35:44 GMT  
		Size: 13.3 KB (13290 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:2b7d61e0cace1004b172c4c485053c11bc9a0f8bb92c9af92b22ff6d35ea5ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (556034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fe164933a80fc8c7abf32c417a466d96db3609b6f1ee14d861525cfdd78fea`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:336b9aae3521ef72851abe97810af76d93937f45be24b0cb67340ff9444cb707`  
		Last Modified: Mon, 02 Dec 2024 20:24:45 GMT  
		Size: 204.1 MB (204137618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:2972bbfcb74add45006671eba779b040f9bf6bf4e3f7135555a34491df439bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b839cc63e7b08f07e283f08b415463fb2ab045791fdd19edf58fa0f210451796`

```dockerfile
```

-	Layers:
	-	`sha256:fd8c3f67164e288cb011c211b630adad3ad6454abdf247636e1be356b57369e7`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bde4a6f2185736694cd07ae59ade73bff87e8e8e38ea4758ae457fe22cf0bb7b`  
		Last Modified: Mon, 02 Dec 2024 20:24:39 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:1a3ec9464aaca3679e309b5a2d37d74b8ee5c1d49087f1580d6490b05dff4c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.7 MB (611728786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc406666b8bba58ebe80d82916ba809f85bc3d079aea65006a7189adc4fa98d`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bb1560f641778d2cb5455f2c6681cb70f74871be341fc94de016ad79eb2311af`  
		Last Modified: Mon, 02 Dec 2024 20:26:21 GMT  
		Size: 248.3 MB (248313252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:4afd1f4300f64430965f43299137ca75249e7c27fbf74de6f92b8393fa33afa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab512b7df0c02174eb212c06d747326403186f429de36c0a0613f77795a9463`

```dockerfile
```

-	Layers:
	-	`sha256:1014165fb7c18bc7f0f45b139b7defb3fdaac4819329563e7b9abfd971721ca9`  
		Last Modified: Mon, 02 Dec 2024 20:26:15 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:971d6fde5f27e47969a782345543d65c64c4609aa41146345e4a00de2400f898`  
		Last Modified: Mon, 02 Dec 2024 20:26:14 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:6fc1e9e942c9ad8d4445769678468782e33f232441a2107277aa9309c8171531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.4 MB (593416662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb95fc496432694f3664ec33ed661538c8d318eddb1848edd90df4e723030f4`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:c731e424a0e50fe1d61cdc956a2238603eb68c82b94428b992cdd8b46e4494ca`  
		Last Modified: Mon, 02 Dec 2024 20:26:44 GMT  
		Size: 274.6 MB (274619819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:a6f9b86026a3aa6e8f0f74e68331895240fe3be10c6d92205fb9e48ff2e3cc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d159b76c2f0dbfef842d8141ba3fb10cf86a429132d7f363f0b81aaf4d7cbd`

```dockerfile
```

-	Layers:
	-	`sha256:e33f6f4afffd15877fb13164def1212d1e66c7616414660e48f2ca508e1427c3`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 15.3 MB (15312980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158597ba495f8617e6dc77be65c0b5dcabe1b602984b6babf8551c0eba26c5d7`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:838d384a1138fe1f2e448e3901bb3d23683570ba3dca581160880ffad760332b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:88a66dc9c1ac1f281b82efafd2b33db603d1ce07f9e4e1bbbe9d3fceef0cdd72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290128622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e791fdca85c41d01da61496939bb1c3e40ef365c768e19e018ded15901356c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dcbc4b34b53bc9e532e413490c8f92a11e6a1682223532ea90597337ed5def`  
		Last Modified: Mon, 02 Dec 2024 20:24:27 GMT  
		Size: 55.3 MB (55309206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a818bb3055598f9d975638712fd88bcf5d9faea94cae98e3059ff8680f4a2cdb`  
		Last Modified: Mon, 02 Dec 2024 20:24:30 GMT  
		Size: 231.2 MB (231195512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:1f4b461f3a7aa6a1d4fbbb717befabe3f146ebbf6ca6f427fe69ce8aebbc3425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eae7f8256cd37b35f89f9fc66faa1f8cd9fb813cbb64c747f44f461117e133`

```dockerfile
```

-	Layers:
	-	`sha256:07d675aac3f963b3a7bcc70c8f78fe4d629b3b9a64ff5d9ca285bf702237511a`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 710.5 KB (710491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a813425ea6f27d41933a1b5e80e290317aa6794a3ea8d7899cdc65dc38852d6d`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14d4e74fdaa1be40a40d60c28718b50f5600e05c496a982f9f499c04d80f9e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294622464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfa952d58e30aa2711dbeb8abcc4e70f27e5ed3ebe16e63c1c12b8642016ec2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61267d89978ab3ab775d217fd01b9f59b054d41cb3b70b13746a2a62eca5677f`  
		Last Modified: Mon, 02 Dec 2024 20:39:22 GMT  
		Size: 52.9 MB (52946253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f5c65e82878a882751b85d69f1b5e1fef9e5a1e2b6e8c6fb91b5a9106f0035`  
		Last Modified: Mon, 02 Dec 2024 20:39:25 GMT  
		Size: 237.6 MB (237588485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:83e6d986399402cf4f87ea920e42c14d1a2b3c9042fd6228a3c8591086bb011d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5040baee093c81f9e4600e14249874276bb6b1011b669a6c4d5962dac288d7`

```dockerfile
```

-	Layers:
	-	`sha256:0607df65216df8538ba3def2f4c315296c5b0fe079a14242b9b8819fc0879ad4`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 746.5 KB (746526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1a8c49a90f68976a179692f548c3e83293af8f8637778ff9a85839ff9df4b8`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:c22e43db16b649a713eb39606c5054dd072eed35a7acffe05e295749c8a7eed3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:51158a1b5d1531f739f78b9ececd3c074e75bf5cc18b4c7b63b1a891c4216740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (289961960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47c29028d898cefa39de15d160ad8cc6cdb1d1dacf206c360c4b4d7d045eb10`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88faabca0966b648ec58d261009681663f60798257994a9281be6f9b359864d0`  
		Last Modified: Mon, 02 Dec 2024 20:24:21 GMT  
		Size: 55.3 MB (55346817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6927d0b73da7baf8ea757697b138a23dc5a1196a24f50ae7a26794aba2b17cd`  
		Last Modified: Mon, 02 Dec 2024 20:24:23 GMT  
		Size: 231.2 MB (231195415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:62a85d1b9963d7c5b3276c4f04bd4d2a32be81c6551a6a6cdb5cf11dd077d933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.7 KB (723693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232ac0ffe4a86028aaba1f2e862002fdd2b4ff1731bb1c90c21401078f6dbd42`

```dockerfile
```

-	Layers:
	-	`sha256:05cdb77f193f20e943f1f0d26b0bb06e83851c90af78776aa9399c35f9aa807b`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 713.0 KB (712979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6cf2aab24ba344de6369df5fa858a9401710c70dc1af99a87e867c019cfd3c4`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b0c30be9019c61d2b4530ec4a206cbf74cf620f9e664db3e2397e50a5dfac14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293943317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170301d6a34aefd5eef35c3fe64882a2094a92214a974fd5804f2656861f9d02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf14d9efd6e0969b2a6f4ce16e7e2e47ac742a9d6b368dd70438e47e0748902`  
		Last Modified: Mon, 02 Dec 2024 20:38:15 GMT  
		Size: 53.0 MB (52995484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27dc85633c060e9e44a987a0c01fdb11e356c8687a7f3f9e9ff64aba2dbceb5`  
		Last Modified: Mon, 02 Dec 2024 20:38:20 GMT  
		Size: 237.6 MB (237588587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:3f475980df113266726615ba78fd4785b4571a54434bb7dc2dd65dbb276e44e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.8 KB (759798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f2ed814e83bb291354abbb56196747dc117e79d9aabab9fa38add98041005f`

```dockerfile
```

-	Layers:
	-	`sha256:c81bbdf1ea267ee371e25e7d9afcd5a265141af67890a79e494bd6dc3c727908`  
		Last Modified: Mon, 02 Dec 2024 20:38:13 GMT  
		Size: 749.0 KB (748965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f261ba6d1390fd6a70a6e72bd1cd40a9d924c207931d67ef020f9481b294128c`  
		Last Modified: Mon, 02 Dec 2024 20:38:13 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:838d384a1138fe1f2e448e3901bb3d23683570ba3dca581160880ffad760332b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:88a66dc9c1ac1f281b82efafd2b33db603d1ce07f9e4e1bbbe9d3fceef0cdd72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290128622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e791fdca85c41d01da61496939bb1c3e40ef365c768e19e018ded15901356c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dcbc4b34b53bc9e532e413490c8f92a11e6a1682223532ea90597337ed5def`  
		Last Modified: Mon, 02 Dec 2024 20:24:27 GMT  
		Size: 55.3 MB (55309206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a818bb3055598f9d975638712fd88bcf5d9faea94cae98e3059ff8680f4a2cdb`  
		Last Modified: Mon, 02 Dec 2024 20:24:30 GMT  
		Size: 231.2 MB (231195512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1f4b461f3a7aa6a1d4fbbb717befabe3f146ebbf6ca6f427fe69ce8aebbc3425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eae7f8256cd37b35f89f9fc66faa1f8cd9fb813cbb64c747f44f461117e133`

```dockerfile
```

-	Layers:
	-	`sha256:07d675aac3f963b3a7bcc70c8f78fe4d629b3b9a64ff5d9ca285bf702237511a`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 710.5 KB (710491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a813425ea6f27d41933a1b5e80e290317aa6794a3ea8d7899cdc65dc38852d6d`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14d4e74fdaa1be40a40d60c28718b50f5600e05c496a982f9f499c04d80f9e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294622464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfa952d58e30aa2711dbeb8abcc4e70f27e5ed3ebe16e63c1c12b8642016ec2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61267d89978ab3ab775d217fd01b9f59b054d41cb3b70b13746a2a62eca5677f`  
		Last Modified: Mon, 02 Dec 2024 20:39:22 GMT  
		Size: 52.9 MB (52946253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f5c65e82878a882751b85d69f1b5e1fef9e5a1e2b6e8c6fb91b5a9106f0035`  
		Last Modified: Mon, 02 Dec 2024 20:39:25 GMT  
		Size: 237.6 MB (237588485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:83e6d986399402cf4f87ea920e42c14d1a2b3c9042fd6228a3c8591086bb011d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5040baee093c81f9e4600e14249874276bb6b1011b669a6c4d5962dac288d7`

```dockerfile
```

-	Layers:
	-	`sha256:0607df65216df8538ba3def2f4c315296c5b0fe079a14242b9b8819fc0879ad4`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 746.5 KB (746526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1a8c49a90f68976a179692f548c3e83293af8f8637778ff9a85839ff9df4b8`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:d242a48452a5f6f490e1c13d3340d54ead1198948a4585dc42e326d6eacd07d1
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
$ docker pull rust@sha256:71aa4f8bdbfb924be55914e8910657aaf15420a87649ea1c64de6f3aef99b357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.7 MB (540737368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51381ded149a6148696b8fd088a50b9684925a0f5c26541db5d3a99db5aae059`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bc823accc52b76a805eb38c2d85f6916c18b62280e12ef86557cf7aae9f958b5`  
		Last Modified: Mon, 02 Dec 2024 20:24:37 GMT  
		Size: 191.4 MB (191418150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:6f2bd220e2f16cb7fe49a9b9ad87295829ed6ebf6b745b45163ccb5c6758e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2628cb17b709463f28662019efa1ac6f3499b61335860965970c347da12bc324`

```dockerfile
```

-	Layers:
	-	`sha256:286a3f2db2c8a6d92215bd0e79bef8cc02de285df8e4a1a45cf8e27b0ab0e625`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 15.5 MB (15500541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dea8927ea34a8749863f37f48d5c3386465f87be87fca83ebfb2da54e47f09`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:c4eab5718491261254547e9dee552013f246ffd187d3fe1c1427b2ca4b061ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526493619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b2f5c8fb2f32e205088f699538ac30a1f60f942ca99b46a7d63ee474294911`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:e64ed70b984c825bcf2c316778efdf694d1177f214c907b60097f528bbda5cf8`  
		Last Modified: Mon, 02 Dec 2024 20:29:54 GMT  
		Size: 224.5 MB (224498211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:be5458af59d7a9d4850ec727e792fe1ce39320e685eba63907c07a62c663a19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15317922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8513824646d633879f3b9c31a95e4313b646af70856500a177c618bb79ec94`

```dockerfile
```

-	Layers:
	-	`sha256:d5013ef9b8a7a070d15a1c43f9eb413d3814d5083868ad3477c7ca363e2629e8`  
		Last Modified: Mon, 02 Dec 2024 20:29:49 GMT  
		Size: 15.3 MB (15304676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a68401994195014fb21c06bdf19c124aea45e5bef8843f712d311bdfced543`  
		Last Modified: Mon, 02 Dec 2024 20:29:48 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f53e59e92e0aeabaf6660d225a107e99c545db88292aa0b26c622e74a040d965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 MB (592017331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c109228921d40f3351cd8c44731f364371c3d17735ca2a5e5f91c306a0dfbfa`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:73de18a65d13f2c8a09a8d948d31e3de3f45af2bead8f228a386915adb234c35`  
		Last Modified: Mon, 02 Dec 2024 20:35:51 GMT  
		Size: 251.8 MB (251804771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c509b7be5dcd87df97728f5298103aa353944b0f8c8f7d25b5b4b7d797017c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15542437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6766be12848456f1e52235b69ad6e4a319291879e57f2a2238bef89da8f3f9e`

```dockerfile
```

-	Layers:
	-	`sha256:98ab1278bc14cd425e7f3eed1e29aae39b73c5f89b91ccc51caee870f35910be`  
		Last Modified: Mon, 02 Dec 2024 20:35:45 GMT  
		Size: 15.5 MB (15529147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9709d89560fe98a5ae0be73fdda845fa48e30c80363bbca1ff69fdb179217095`  
		Last Modified: Mon, 02 Dec 2024 20:35:44 GMT  
		Size: 13.3 KB (13290 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:2b7d61e0cace1004b172c4c485053c11bc9a0f8bb92c9af92b22ff6d35ea5ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (556034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fe164933a80fc8c7abf32c417a466d96db3609b6f1ee14d861525cfdd78fea`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:336b9aae3521ef72851abe97810af76d93937f45be24b0cb67340ff9444cb707`  
		Last Modified: Mon, 02 Dec 2024 20:24:45 GMT  
		Size: 204.1 MB (204137618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2972bbfcb74add45006671eba779b040f9bf6bf4e3f7135555a34491df439bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b839cc63e7b08f07e283f08b415463fb2ab045791fdd19edf58fa0f210451796`

```dockerfile
```

-	Layers:
	-	`sha256:fd8c3f67164e288cb011c211b630adad3ad6454abdf247636e1be356b57369e7`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bde4a6f2185736694cd07ae59ade73bff87e8e8e38ea4758ae457fe22cf0bb7b`  
		Last Modified: Mon, 02 Dec 2024 20:24:39 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:1a3ec9464aaca3679e309b5a2d37d74b8ee5c1d49087f1580d6490b05dff4c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.7 MB (611728786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc406666b8bba58ebe80d82916ba809f85bc3d079aea65006a7189adc4fa98d`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bb1560f641778d2cb5455f2c6681cb70f74871be341fc94de016ad79eb2311af`  
		Last Modified: Mon, 02 Dec 2024 20:26:21 GMT  
		Size: 248.3 MB (248313252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4afd1f4300f64430965f43299137ca75249e7c27fbf74de6f92b8393fa33afa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab512b7df0c02174eb212c06d747326403186f429de36c0a0613f77795a9463`

```dockerfile
```

-	Layers:
	-	`sha256:1014165fb7c18bc7f0f45b139b7defb3fdaac4819329563e7b9abfd971721ca9`  
		Last Modified: Mon, 02 Dec 2024 20:26:15 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:971d6fde5f27e47969a782345543d65c64c4609aa41146345e4a00de2400f898`  
		Last Modified: Mon, 02 Dec 2024 20:26:14 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:6fc1e9e942c9ad8d4445769678468782e33f232441a2107277aa9309c8171531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.4 MB (593416662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb95fc496432694f3664ec33ed661538c8d318eddb1848edd90df4e723030f4`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:c731e424a0e50fe1d61cdc956a2238603eb68c82b94428b992cdd8b46e4494ca`  
		Last Modified: Mon, 02 Dec 2024 20:26:44 GMT  
		Size: 274.6 MB (274619819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a6f9b86026a3aa6e8f0f74e68331895240fe3be10c6d92205fb9e48ff2e3cc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d159b76c2f0dbfef842d8141ba3fb10cf86a429132d7f363f0b81aaf4d7cbd`

```dockerfile
```

-	Layers:
	-	`sha256:e33f6f4afffd15877fb13164def1212d1e66c7616414660e48f2ca508e1427c3`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 15.3 MB (15312980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158597ba495f8617e6dc77be65c0b5dcabe1b602984b6babf8551c0eba26c5d7`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:48e32924c033e231995e5d604fc0bde746603529ab9c9525ed69551d1763722f
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
$ docker pull rust@sha256:3b69b1344468f45d6841e7d7eeddb646a6109c51ba6ad84867d40ce93bdb6507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.9 MB (513894985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1322104423ebd73df2358552ad57a4775ed183c222ff55d72233ce9c62b8e0c4`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:74d39ef915c9431d8814f436f6c5a05c033b7d061a908a761893aba712738dca`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 191.4 MB (191418226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:464848c0989553e6f5c696e1e8f488b2fd360b489a7c71bfc156c6c854921e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aed3439b87c35516bfcefed896ac0fbc064e92cdc1fc24c50cf3f4f82a470b8`

```dockerfile
```

-	Layers:
	-	`sha256:d5e8c58afb3cd8c33d2faf04883bb9f40a4d9ed6d20d0f401f4edc4b73f3f483`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 15.1 MB (15099560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7b47989b19887839396cc56566eed4407f3d0105f1bbb3dedb3ae59ecc329`  
		Last Modified: Mon, 02 Dec 2024 20:24:39 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:ef4925470bc527b51f98b8fd0e090015ba06289dce879ce02540c523a950492c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.6 MB (507587556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d219ef379dcd3a55ce17998421a285fdcae9d0e18e6dc6719f234d8ba6fdba2`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:460e72c81a8faf8a12fa4517b675bc73c5173407737e669feb3c5c0de5acdf15`  
		Last Modified: Mon, 02 Dec 2024 20:33:45 GMT  
		Size: 224.5 MB (224498199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8ffb613d6c04af1f4a4c9dad7c9046e06244f7a51eafe51ef0239aa93e16887b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5692a48de82943f6da6098bdb2f952d25c38b546e4aad806bba8904ea5c1086f`

```dockerfile
```

-	Layers:
	-	`sha256:0c4c1556ccde855c9606ac4814d71b557174cf8f2b9521f60c9cea5219852703`  
		Last Modified: Mon, 02 Dec 2024 20:33:40 GMT  
		Size: 14.9 MB (14900067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea7e331de6703885f45617be049222c6f6d6474c6b8b1e74d1493ea5482878c9`  
		Last Modified: Mon, 02 Dec 2024 20:33:39 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b92b53e23598b9accd960a82d00386d9c100495c88f77a4aac5b6983bfd24697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.9 MB (565925019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0b729695c79cc2b5ab22d9798c6a3c74ab86f10b3c7e147e82236a28cdac7`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:2d9513256f7bf83972d3d8a5644bef3b31913ac18f945e7bda5e1b67800b99ff`  
		Last Modified: Mon, 02 Dec 2024 20:32:52 GMT  
		Size: 251.8 MB (251804822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1c90a3d5572cdeb856d417ebbc90b19c0c4ad64b5ac8849d506106dea513ae57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15113175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53bdc544237eb3432d49c4682f0fe3627f7d36735a5cb1865033529582e0fe6`

```dockerfile
```

-	Layers:
	-	`sha256:58f3bb41e62e5e98de42e3be870f748aec12d2a62f8576bac1c8869337ee9e15`  
		Last Modified: Mon, 02 Dec 2024 20:32:47 GMT  
		Size: 15.1 MB (15101822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9d1ceb3d92c5f213ec0ca376ec575dd98f09f32d6d5430b2555d6c0b7562d1`  
		Last Modified: Mon, 02 Dec 2024 20:32:46 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:a534b238c9b99b740f1216486f77bf3c14cea88e3a9e1bbf070d86fbab5bb0fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.3 MB (532304484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18675ba81d558cf8f9ec3d367d8c3ec104bff1aab30160b88e8bc51d23329c49`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:8c0d713557008a8d69677c0aa162eedcab0ac7846ed90aee9c2d5788a51fad0f`  
		Last Modified: Mon, 02 Dec 2024 20:24:51 GMT  
		Size: 204.1 MB (204137636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:74c74e7676b304b2cb4c939116791d252bdd51e0bf9e358dcb40dad59a622617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15097814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c3da0659cf7eddc4df08832981dc114a0434eff8cff0f7e0a5318dcda2ea8d`

```dockerfile
```

-	Layers:
	-	`sha256:e179a67825d943f6221f1e2e7a9c60df8de969054fec98b3538bbf4a5682769b`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 15.1 MB (15086597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6b6fde063e7e47ab87f2ab98387725a5cbba86c1ba5665ba2280757cd267dd0`  
		Last Modified: Mon, 02 Dec 2024 20:24:46 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:2808c258e14c25a1277d7ba6e653093ef00ba088dc73d99402a900e8cc218d5c
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
$ docker pull rust@sha256:6a3be2a97d72a2d401807e494ff0b2d500bb241293db2f8d84e16b629f952366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291337423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae1dcbb4bdaada87c1f2a5397fb3e2534cd10a921d8b38ab8e032613d4bec82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbfe6cc0ca59f7757297ccc9049930ac7f37bccab06b5fb02b80eb1d37e4a48`  
		Last Modified: Mon, 02 Dec 2024 20:24:38 GMT  
		Size: 262.2 MB (262209428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:1a1e9a3dd7b8efd48e40f7a424dd24b8ba15de70d687a06656717edbb9048faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1ba3680f55e2998a08ff5c873a90a1249c120eba4a76d95874c78c7e755812`

```dockerfile
```

-	Layers:
	-	`sha256:190def7ed7dafd6d8ee1ba46e117570e708371dde8e290f4c757acd3f543a0da`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 4.0 MB (3960916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3749ab658f8ad4f8d17c77b275dd953cfdf9c2de24728be40fda41f514178b`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:6d7afc9f25f7a5cefc9b6f3fbf2304e89502533bf562b3d008f1d7e98e849723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297059662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302b6a008c606c7cd8b9263e55bcb04488d3fe948c1a45f2f7a6b2e9f6c11f23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defe357fcbe93d1e65d0570d021785ad676696d2d624262bdb0e214723689b36`  
		Last Modified: Mon, 02 Dec 2024 20:31:38 GMT  
		Size: 272.3 MB (272340753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3f2058fe6f54a997932102d8b6bc235e8d4666e331b9296243cf75c70990da78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7fc6c7b289d0a098a407027d015ead0708a0e04655389eae49e4155b848f52`

```dockerfile
```

-	Layers:
	-	`sha256:8928a87a6013ae9d938cea84efc86dfc5fb240cf83f931e727c7693adaa6da2c`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 3.8 MB (3776732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea6b01b234f1e08ebc59a4a02bda774ffe04cf102809435a132937896e535eaf`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:594e5e30e34cb3f1edfcf62b6c42ab7418bfbe4fd83057099fede39488edc7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.8 MB (346802313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3d008bad10df60f61201660a99f5d86423c1a1a546c0a1a1838123d75a27a1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0237173b80106fe0760a817d7e6d1c71f9e5e284c512b7d06074708c59aff7`  
		Last Modified: Mon, 02 Dec 2024 20:37:13 GMT  
		Size: 317.6 MB (317644957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:895f4818b23e10a7e1f1880f5e42eb988a221a3a0eb6f39134e09fa24dcf11ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e2f37d04cfed0d9e84101878c4064b4b8353ce7996f5587a68e63f1e717bd8`

```dockerfile
```

-	Layers:
	-	`sha256:05e0e8f9842371d47373dc72339abb01c46ebf232229e4810af7074cc8f68115`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 4.0 MB (3983284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b63a1b31beb1e3b516d716bd7530b21f5698318b664ff2c0808a3a6738dbc2`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:e3a12bd5e08f7ffd7c014c2820aa4bbb647a30f3617f59659136669d0765cde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301886447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3c3937265088583d6ea42714a975738f2bf863ef26ec51c0eceafa294d88e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ceb72ece1ea1e0fe9569779176af4568889e4706901654739657a99aa4700`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 271.7 MB (271740997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:ea30beb0ac18971c71310961164ae02c93873a3dee5e71820cb92ca5af9cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad0f3a1a05782cc497e5841bd1cba942630e16eb84acaf9a3809618df1ee6d`

```dockerfile
```

-	Layers:
	-	`sha256:bf795665c0773ee9ebba9af59adaf88084fc89e625ffd096983779a3322b9d98`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea300ff11941e5c8c9dca6dae2eaeb1b7aa9ff4ffacb336422e939217214bca`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:901e8fd72a554e505e9273538a8ad34c2bf33a02f62b634250d35e34bb2ded90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.2 MB (350198087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c2aef4eee77ed0f0829ba276a911bf8cd57b8afb28b00184b775c489a82bb4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a607df9bd35302bace9a6ad9223bd9a4b868b9c462a42e5cca65d5fd3d8a9b`  
		Last Modified: Mon, 02 Dec 2024 20:29:03 GMT  
		Size: 317.1 MB (317072734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:12a9974e9bd55d24e84c10e72f5170591f010651e62da1a001cce00b60a8b5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f48e8cf17275373c2886d5d424e13f54217678435465c09519f9d27932b9a4`

```dockerfile
```

-	Layers:
	-	`sha256:1969029d7112da6fdd40a3a936b1152b38032abb4d7bd1bc31411ed5fd021715`  
		Last Modified: Mon, 02 Dec 2024 20:28:53 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52df272aeab4c0542aa89ec9e6638cabd6465bf962ee7053c5eac2b05e53b44d`  
		Last Modified: Mon, 02 Dec 2024 20:28:52 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:59e72321724e973f7b278fe9cfdbc7916988c33529e4f16eaa3be7e72b4d7b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352217458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c145addc8a9384eb579adb69c9d9500d0a57a3690e0e396cdce0b24098684ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e04d7c8b55a5ef929486fce3eca63d3be7958f04b601f4f73a52e9591e4a16`  
		Last Modified: Mon, 02 Dec 2024 20:28:50 GMT  
		Size: 324.7 MB (324725830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:34d0adfbc6046e33a5307df483d7f0626cfbedc28bc7cb0fa092b40008a9d30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3815877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4d233def5b8a5cbdca87e1d70f4c0e5602f12e771f4e9c36399233edb2ef42`

```dockerfile
```

-	Layers:
	-	`sha256:a2bb7709243f1094bc9ed02cbe32492f025e7ba1b46404d9f64f3527d774ce68`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 3.8 MB (3802606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60ee2d606d582a3328f010baeb9968ac6e723667c4dac109be44717dae4d543`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:2808c258e14c25a1277d7ba6e653093ef00ba088dc73d99402a900e8cc218d5c
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
$ docker pull rust@sha256:6a3be2a97d72a2d401807e494ff0b2d500bb241293db2f8d84e16b629f952366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291337423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae1dcbb4bdaada87c1f2a5397fb3e2534cd10a921d8b38ab8e032613d4bec82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbfe6cc0ca59f7757297ccc9049930ac7f37bccab06b5fb02b80eb1d37e4a48`  
		Last Modified: Mon, 02 Dec 2024 20:24:38 GMT  
		Size: 262.2 MB (262209428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1a1e9a3dd7b8efd48e40f7a424dd24b8ba15de70d687a06656717edbb9048faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1ba3680f55e2998a08ff5c873a90a1249c120eba4a76d95874c78c7e755812`

```dockerfile
```

-	Layers:
	-	`sha256:190def7ed7dafd6d8ee1ba46e117570e708371dde8e290f4c757acd3f543a0da`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 4.0 MB (3960916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3749ab658f8ad4f8d17c77b275dd953cfdf9c2de24728be40fda41f514178b`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:6d7afc9f25f7a5cefc9b6f3fbf2304e89502533bf562b3d008f1d7e98e849723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297059662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302b6a008c606c7cd8b9263e55bcb04488d3fe948c1a45f2f7a6b2e9f6c11f23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defe357fcbe93d1e65d0570d021785ad676696d2d624262bdb0e214723689b36`  
		Last Modified: Mon, 02 Dec 2024 20:31:38 GMT  
		Size: 272.3 MB (272340753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3f2058fe6f54a997932102d8b6bc235e8d4666e331b9296243cf75c70990da78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7fc6c7b289d0a098a407027d015ead0708a0e04655389eae49e4155b848f52`

```dockerfile
```

-	Layers:
	-	`sha256:8928a87a6013ae9d938cea84efc86dfc5fb240cf83f931e727c7693adaa6da2c`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 3.8 MB (3776732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea6b01b234f1e08ebc59a4a02bda774ffe04cf102809435a132937896e535eaf`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:594e5e30e34cb3f1edfcf62b6c42ab7418bfbe4fd83057099fede39488edc7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.8 MB (346802313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3d008bad10df60f61201660a99f5d86423c1a1a546c0a1a1838123d75a27a1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0237173b80106fe0760a817d7e6d1c71f9e5e284c512b7d06074708c59aff7`  
		Last Modified: Mon, 02 Dec 2024 20:37:13 GMT  
		Size: 317.6 MB (317644957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:895f4818b23e10a7e1f1880f5e42eb988a221a3a0eb6f39134e09fa24dcf11ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e2f37d04cfed0d9e84101878c4064b4b8353ce7996f5587a68e63f1e717bd8`

```dockerfile
```

-	Layers:
	-	`sha256:05e0e8f9842371d47373dc72339abb01c46ebf232229e4810af7074cc8f68115`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 4.0 MB (3983284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b63a1b31beb1e3b516d716bd7530b21f5698318b664ff2c0808a3a6738dbc2`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:e3a12bd5e08f7ffd7c014c2820aa4bbb647a30f3617f59659136669d0765cde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301886447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3c3937265088583d6ea42714a975738f2bf863ef26ec51c0eceafa294d88e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ceb72ece1ea1e0fe9569779176af4568889e4706901654739657a99aa4700`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 271.7 MB (271740997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ea30beb0ac18971c71310961164ae02c93873a3dee5e71820cb92ca5af9cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad0f3a1a05782cc497e5841bd1cba942630e16eb84acaf9a3809618df1ee6d`

```dockerfile
```

-	Layers:
	-	`sha256:bf795665c0773ee9ebba9af59adaf88084fc89e625ffd096983779a3322b9d98`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea300ff11941e5c8c9dca6dae2eaeb1b7aa9ff4ffacb336422e939217214bca`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:901e8fd72a554e505e9273538a8ad34c2bf33a02f62b634250d35e34bb2ded90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.2 MB (350198087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c2aef4eee77ed0f0829ba276a911bf8cd57b8afb28b00184b775c489a82bb4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a607df9bd35302bace9a6ad9223bd9a4b868b9c462a42e5cca65d5fd3d8a9b`  
		Last Modified: Mon, 02 Dec 2024 20:29:03 GMT  
		Size: 317.1 MB (317072734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:12a9974e9bd55d24e84c10e72f5170591f010651e62da1a001cce00b60a8b5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f48e8cf17275373c2886d5d424e13f54217678435465c09519f9d27932b9a4`

```dockerfile
```

-	Layers:
	-	`sha256:1969029d7112da6fdd40a3a936b1152b38032abb4d7bd1bc31411ed5fd021715`  
		Last Modified: Mon, 02 Dec 2024 20:28:53 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52df272aeab4c0542aa89ec9e6638cabd6465bf962ee7053c5eac2b05e53b44d`  
		Last Modified: Mon, 02 Dec 2024 20:28:52 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:59e72321724e973f7b278fe9cfdbc7916988c33529e4f16eaa3be7e72b4d7b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352217458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c145addc8a9384eb579adb69c9d9500d0a57a3690e0e396cdce0b24098684ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e04d7c8b55a5ef929486fce3eca63d3be7958f04b601f4f73a52e9591e4a16`  
		Last Modified: Mon, 02 Dec 2024 20:28:50 GMT  
		Size: 324.7 MB (324725830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:34d0adfbc6046e33a5307df483d7f0626cfbedc28bc7cb0fa092b40008a9d30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3815877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4d233def5b8a5cbdca87e1d70f4c0e5602f12e771f4e9c36399233edb2ef42`

```dockerfile
```

-	Layers:
	-	`sha256:a2bb7709243f1094bc9ed02cbe32492f025e7ba1b46404d9f64f3527d774ce68`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 3.8 MB (3802606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60ee2d606d582a3328f010baeb9968ac6e723667c4dac109be44717dae4d543`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:cd64d55bf5d90faca3b5e69039e03cc8eaf4d0c531537cb08d20ee8ee87f438f
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
$ docker pull rust@sha256:693226f9da3b618f747e1d45901d1d6c27e591f5d3d17c92685a55f4983911ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.8 MB (282812182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecfd0a5420dc73cd925c46f1879d9c00df802531eccda112b2d406071cacca0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384329ccf6be51bb1ef6f2b07175dcdcebcf898a37bba183bfe10f903be995ce`  
		Last Modified: Mon, 02 Dec 2024 20:24:22 GMT  
		Size: 251.4 MB (251360621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ebc287a15a3e3cd43102b0e5b3df9aae5ae0a8cd284c6cd6845bc32e9e0b5903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4191040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8375006c14246df12ba094238c9468666ade0d799bb9d20f012e4f299847e56a`

```dockerfile
```

-	Layers:
	-	`sha256:74af93f126d4c06de89836c2cf05cebb553960e94e4ab55a74d46b28183ad983`  
		Last Modified: Mon, 02 Dec 2024 20:24:19 GMT  
		Size: 4.2 MB (4179684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c366dfc129927914c32fbdf3b3a7128249ed30666f407a63a7ff0f19be5aff8`  
		Last Modified: Mon, 02 Dec 2024 20:24:18 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:abf606a99416890d34310c1ed7c2dc863aa6a1ce4f8ab588c768b2511ffdaa5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.2 MB (293172521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4ff907c925646494aeeb07f6a9c015b9f209c836a858b44c751fffc645ed1b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fffe59376f64ffa8f62067ec6c177458ad560736ecb62f5a746b99a1213febb`  
		Last Modified: Mon, 02 Dec 2024 20:27:46 GMT  
		Size: 266.6 MB (266563264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6ec69ccb3c2df674b652af2bf87b9af3d1c186c907bacf211557fca6a0605d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d2e1fea37fd47ebcb90737269a9a15f43d09ff6e3a8ac409221ed3d6a3b8d3`

```dockerfile
```

-	Layers:
	-	`sha256:b11be9c55ffbd97983468ba6c80f6bfb1b6d2f881f28c132a972181a2f323cf1`  
		Last Modified: Mon, 02 Dec 2024 20:27:40 GMT  
		Size: 4.0 MB (3988606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9172172b88ef1546ba7e0d5edb4641fbb14bdf07ff13f0bb89ccbb6102cb8a32`  
		Last Modified: Mon, 02 Dec 2024 20:27:40 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a32ae5ae9cad532df229a1fef4ada9991409591a7ccf15c3856ba3ca21d7c26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.4 MB (337389995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504b549e7eafa02320debcac41241b24c3e628c6a7f2c4a085a0e8430d5fa44f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b17b8db729381225a8d73b8af06a440c8b3f44ba100df98709bb0b03c0a016`  
		Last Modified: Mon, 02 Dec 2024 20:34:10 GMT  
		Size: 307.3 MB (307298395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3b6d85ff4952c3db80e6f66474078bd4e09bc1b884e7978509e0cf8a7c4410ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4187819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2535b26d94240ff8a8243d5fcaf6cd4f3238cc6575f145c7055f3be7a7af6e18`

```dockerfile
```

-	Layers:
	-	`sha256:280d6fd398dd958493aa5d431829910d0726c625baf5513aa3477e64de936e0d`  
		Last Modified: Mon, 02 Dec 2024 20:34:04 GMT  
		Size: 4.2 MB (4176359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb393af559bdc07a24e80a9442f17ed5976eafc6cced8e26e7df0a3132f88ce7`  
		Last Modified: Mon, 02 Dec 2024 20:34:04 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:d5af146980a072b682d3ac22609ffed95252933df15d14690667925cf35a83bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297129117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182df1c816edafaeadc3362a748a39f671aa57bf19f6d7fafd20bcb2a4becdd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a29bf3a9090d3e58d845509836c32130197f51dc0eafb75e2102450607aa614`  
		Last Modified: Mon, 02 Dec 2024 20:24:48 GMT  
		Size: 264.7 MB (264705766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:de112da84d3f18bbad7559779bde4d938157704801863564aaae2a20e856f0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaa8827be2c8dbe784a39a4b999bb4842aa2514d900dbd211b897aabc55f32b`

```dockerfile
```

-	Layers:
	-	`sha256:1e6ab84278603cf43cd88053eb59875eea8a1a59d9a120bb129fdeff7482806d`  
		Last Modified: Mon, 02 Dec 2024 20:24:41 GMT  
		Size: 4.2 MB (4169952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67bd2e3b5300c4b614ff1c265cf9f027c92cb2fd18db1cac9fc58fb89c69ea17`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83`

```console
$ docker pull rust@sha256:d242a48452a5f6f490e1c13d3340d54ead1198948a4585dc42e326d6eacd07d1
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

### `rust:1.83` - linux; amd64

```console
$ docker pull rust@sha256:71aa4f8bdbfb924be55914e8910657aaf15420a87649ea1c64de6f3aef99b357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.7 MB (540737368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51381ded149a6148696b8fd088a50b9684925a0f5c26541db5d3a99db5aae059`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bc823accc52b76a805eb38c2d85f6916c18b62280e12ef86557cf7aae9f958b5`  
		Last Modified: Mon, 02 Dec 2024 20:24:37 GMT  
		Size: 191.4 MB (191418150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83` - unknown; unknown

```console
$ docker pull rust@sha256:6f2bd220e2f16cb7fe49a9b9ad87295829ed6ebf6b745b45163ccb5c6758e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2628cb17b709463f28662019efa1ac6f3499b61335860965970c347da12bc324`

```dockerfile
```

-	Layers:
	-	`sha256:286a3f2db2c8a6d92215bd0e79bef8cc02de285df8e4a1a45cf8e27b0ab0e625`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 15.5 MB (15500541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dea8927ea34a8749863f37f48d5c3386465f87be87fca83ebfb2da54e47f09`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83` - linux; arm variant v7

```console
$ docker pull rust@sha256:c4eab5718491261254547e9dee552013f246ffd187d3fe1c1427b2ca4b061ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526493619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b2f5c8fb2f32e205088f699538ac30a1f60f942ca99b46a7d63ee474294911`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:e64ed70b984c825bcf2c316778efdf694d1177f214c907b60097f528bbda5cf8`  
		Last Modified: Mon, 02 Dec 2024 20:29:54 GMT  
		Size: 224.5 MB (224498211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83` - unknown; unknown

```console
$ docker pull rust@sha256:be5458af59d7a9d4850ec727e792fe1ce39320e685eba63907c07a62c663a19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15317922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8513824646d633879f3b9c31a95e4313b646af70856500a177c618bb79ec94`

```dockerfile
```

-	Layers:
	-	`sha256:d5013ef9b8a7a070d15a1c43f9eb413d3814d5083868ad3477c7ca363e2629e8`  
		Last Modified: Mon, 02 Dec 2024 20:29:49 GMT  
		Size: 15.3 MB (15304676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a68401994195014fb21c06bdf19c124aea45e5bef8843f712d311bdfced543`  
		Last Modified: Mon, 02 Dec 2024 20:29:48 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f53e59e92e0aeabaf6660d225a107e99c545db88292aa0b26c622e74a040d965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 MB (592017331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c109228921d40f3351cd8c44731f364371c3d17735ca2a5e5f91c306a0dfbfa`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:73de18a65d13f2c8a09a8d948d31e3de3f45af2bead8f228a386915adb234c35`  
		Last Modified: Mon, 02 Dec 2024 20:35:51 GMT  
		Size: 251.8 MB (251804771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83` - unknown; unknown

```console
$ docker pull rust@sha256:c509b7be5dcd87df97728f5298103aa353944b0f8c8f7d25b5b4b7d797017c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15542437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6766be12848456f1e52235b69ad6e4a319291879e57f2a2238bef89da8f3f9e`

```dockerfile
```

-	Layers:
	-	`sha256:98ab1278bc14cd425e7f3eed1e29aae39b73c5f89b91ccc51caee870f35910be`  
		Last Modified: Mon, 02 Dec 2024 20:35:45 GMT  
		Size: 15.5 MB (15529147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9709d89560fe98a5ae0be73fdda845fa48e30c80363bbca1ff69fdb179217095`  
		Last Modified: Mon, 02 Dec 2024 20:35:44 GMT  
		Size: 13.3 KB (13290 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83` - linux; 386

```console
$ docker pull rust@sha256:2b7d61e0cace1004b172c4c485053c11bc9a0f8bb92c9af92b22ff6d35ea5ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (556034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fe164933a80fc8c7abf32c417a466d96db3609b6f1ee14d861525cfdd78fea`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:336b9aae3521ef72851abe97810af76d93937f45be24b0cb67340ff9444cb707`  
		Last Modified: Mon, 02 Dec 2024 20:24:45 GMT  
		Size: 204.1 MB (204137618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83` - unknown; unknown

```console
$ docker pull rust@sha256:2972bbfcb74add45006671eba779b040f9bf6bf4e3f7135555a34491df439bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b839cc63e7b08f07e283f08b415463fb2ab045791fdd19edf58fa0f210451796`

```dockerfile
```

-	Layers:
	-	`sha256:fd8c3f67164e288cb011c211b630adad3ad6454abdf247636e1be356b57369e7`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bde4a6f2185736694cd07ae59ade73bff87e8e8e38ea4758ae457fe22cf0bb7b`  
		Last Modified: Mon, 02 Dec 2024 20:24:39 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83` - linux; ppc64le

```console
$ docker pull rust@sha256:1a3ec9464aaca3679e309b5a2d37d74b8ee5c1d49087f1580d6490b05dff4c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.7 MB (611728786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc406666b8bba58ebe80d82916ba809f85bc3d079aea65006a7189adc4fa98d`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bb1560f641778d2cb5455f2c6681cb70f74871be341fc94de016ad79eb2311af`  
		Last Modified: Mon, 02 Dec 2024 20:26:21 GMT  
		Size: 248.3 MB (248313252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83` - unknown; unknown

```console
$ docker pull rust@sha256:4afd1f4300f64430965f43299137ca75249e7c27fbf74de6f92b8393fa33afa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab512b7df0c02174eb212c06d747326403186f429de36c0a0613f77795a9463`

```dockerfile
```

-	Layers:
	-	`sha256:1014165fb7c18bc7f0f45b139b7defb3fdaac4819329563e7b9abfd971721ca9`  
		Last Modified: Mon, 02 Dec 2024 20:26:15 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:971d6fde5f27e47969a782345543d65c64c4609aa41146345e4a00de2400f898`  
		Last Modified: Mon, 02 Dec 2024 20:26:14 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83` - linux; s390x

```console
$ docker pull rust@sha256:6fc1e9e942c9ad8d4445769678468782e33f232441a2107277aa9309c8171531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.4 MB (593416662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb95fc496432694f3664ec33ed661538c8d318eddb1848edd90df4e723030f4`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:c731e424a0e50fe1d61cdc956a2238603eb68c82b94428b992cdd8b46e4494ca`  
		Last Modified: Mon, 02 Dec 2024 20:26:44 GMT  
		Size: 274.6 MB (274619819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83` - unknown; unknown

```console
$ docker pull rust@sha256:a6f9b86026a3aa6e8f0f74e68331895240fe3be10c6d92205fb9e48ff2e3cc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d159b76c2f0dbfef842d8141ba3fb10cf86a429132d7f363f0b81aaf4d7cbd`

```dockerfile
```

-	Layers:
	-	`sha256:e33f6f4afffd15877fb13164def1212d1e66c7616414660e48f2ca508e1427c3`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 15.3 MB (15312980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158597ba495f8617e6dc77be65c0b5dcabe1b602984b6babf8551c0eba26c5d7`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83-alpine`

```console
$ docker pull rust@sha256:838d384a1138fe1f2e448e3901bb3d23683570ba3dca581160880ffad760332b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.83-alpine` - linux; amd64

```console
$ docker pull rust@sha256:88a66dc9c1ac1f281b82efafd2b33db603d1ce07f9e4e1bbbe9d3fceef0cdd72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290128622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e791fdca85c41d01da61496939bb1c3e40ef365c768e19e018ded15901356c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dcbc4b34b53bc9e532e413490c8f92a11e6a1682223532ea90597337ed5def`  
		Last Modified: Mon, 02 Dec 2024 20:24:27 GMT  
		Size: 55.3 MB (55309206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a818bb3055598f9d975638712fd88bcf5d9faea94cae98e3059ff8680f4a2cdb`  
		Last Modified: Mon, 02 Dec 2024 20:24:30 GMT  
		Size: 231.2 MB (231195512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:1f4b461f3a7aa6a1d4fbbb717befabe3f146ebbf6ca6f427fe69ce8aebbc3425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eae7f8256cd37b35f89f9fc66faa1f8cd9fb813cbb64c747f44f461117e133`

```dockerfile
```

-	Layers:
	-	`sha256:07d675aac3f963b3a7bcc70c8f78fe4d629b3b9a64ff5d9ca285bf702237511a`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 710.5 KB (710491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a813425ea6f27d41933a1b5e80e290317aa6794a3ea8d7899cdc65dc38852d6d`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14d4e74fdaa1be40a40d60c28718b50f5600e05c496a982f9f499c04d80f9e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294622464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfa952d58e30aa2711dbeb8abcc4e70f27e5ed3ebe16e63c1c12b8642016ec2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61267d89978ab3ab775d217fd01b9f59b054d41cb3b70b13746a2a62eca5677f`  
		Last Modified: Mon, 02 Dec 2024 20:39:22 GMT  
		Size: 52.9 MB (52946253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f5c65e82878a882751b85d69f1b5e1fef9e5a1e2b6e8c6fb91b5a9106f0035`  
		Last Modified: Mon, 02 Dec 2024 20:39:25 GMT  
		Size: 237.6 MB (237588485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:83e6d986399402cf4f87ea920e42c14d1a2b3c9042fd6228a3c8591086bb011d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5040baee093c81f9e4600e14249874276bb6b1011b669a6c4d5962dac288d7`

```dockerfile
```

-	Layers:
	-	`sha256:0607df65216df8538ba3def2f4c315296c5b0fe079a14242b9b8819fc0879ad4`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 746.5 KB (746526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1a8c49a90f68976a179692f548c3e83293af8f8637778ff9a85839ff9df4b8`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83-alpine3.19`

```console
$ docker pull rust@sha256:c22e43db16b649a713eb39606c5054dd072eed35a7acffe05e295749c8a7eed3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.83-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:51158a1b5d1531f739f78b9ececd3c074e75bf5cc18b4c7b63b1a891c4216740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (289961960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47c29028d898cefa39de15d160ad8cc6cdb1d1dacf206c360c4b4d7d045eb10`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88faabca0966b648ec58d261009681663f60798257994a9281be6f9b359864d0`  
		Last Modified: Mon, 02 Dec 2024 20:24:21 GMT  
		Size: 55.3 MB (55346817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6927d0b73da7baf8ea757697b138a23dc5a1196a24f50ae7a26794aba2b17cd`  
		Last Modified: Mon, 02 Dec 2024 20:24:23 GMT  
		Size: 231.2 MB (231195415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:62a85d1b9963d7c5b3276c4f04bd4d2a32be81c6551a6a6cdb5cf11dd077d933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.7 KB (723693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232ac0ffe4a86028aaba1f2e862002fdd2b4ff1731bb1c90c21401078f6dbd42`

```dockerfile
```

-	Layers:
	-	`sha256:05cdb77f193f20e943f1f0d26b0bb06e83851c90af78776aa9399c35f9aa807b`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 713.0 KB (712979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6cf2aab24ba344de6369df5fa858a9401710c70dc1af99a87e867c019cfd3c4`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b0c30be9019c61d2b4530ec4a206cbf74cf620f9e664db3e2397e50a5dfac14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293943317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170301d6a34aefd5eef35c3fe64882a2094a92214a974fd5804f2656861f9d02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf14d9efd6e0969b2a6f4ce16e7e2e47ac742a9d6b368dd70438e47e0748902`  
		Last Modified: Mon, 02 Dec 2024 20:38:15 GMT  
		Size: 53.0 MB (52995484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27dc85633c060e9e44a987a0c01fdb11e356c8687a7f3f9e9ff64aba2dbceb5`  
		Last Modified: Mon, 02 Dec 2024 20:38:20 GMT  
		Size: 237.6 MB (237588587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:3f475980df113266726615ba78fd4785b4571a54434bb7dc2dd65dbb276e44e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.8 KB (759798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f2ed814e83bb291354abbb56196747dc117e79d9aabab9fa38add98041005f`

```dockerfile
```

-	Layers:
	-	`sha256:c81bbdf1ea267ee371e25e7d9afcd5a265141af67890a79e494bd6dc3c727908`  
		Last Modified: Mon, 02 Dec 2024 20:38:13 GMT  
		Size: 749.0 KB (748965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f261ba6d1390fd6a70a6e72bd1cd40a9d924c207931d67ef020f9481b294128c`  
		Last Modified: Mon, 02 Dec 2024 20:38:13 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83-alpine3.20`

```console
$ docker pull rust@sha256:838d384a1138fe1f2e448e3901bb3d23683570ba3dca581160880ffad760332b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.83-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:88a66dc9c1ac1f281b82efafd2b33db603d1ce07f9e4e1bbbe9d3fceef0cdd72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290128622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e791fdca85c41d01da61496939bb1c3e40ef365c768e19e018ded15901356c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dcbc4b34b53bc9e532e413490c8f92a11e6a1682223532ea90597337ed5def`  
		Last Modified: Mon, 02 Dec 2024 20:24:27 GMT  
		Size: 55.3 MB (55309206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a818bb3055598f9d975638712fd88bcf5d9faea94cae98e3059ff8680f4a2cdb`  
		Last Modified: Mon, 02 Dec 2024 20:24:30 GMT  
		Size: 231.2 MB (231195512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1f4b461f3a7aa6a1d4fbbb717befabe3f146ebbf6ca6f427fe69ce8aebbc3425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eae7f8256cd37b35f89f9fc66faa1f8cd9fb813cbb64c747f44f461117e133`

```dockerfile
```

-	Layers:
	-	`sha256:07d675aac3f963b3a7bcc70c8f78fe4d629b3b9a64ff5d9ca285bf702237511a`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 710.5 KB (710491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a813425ea6f27d41933a1b5e80e290317aa6794a3ea8d7899cdc65dc38852d6d`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14d4e74fdaa1be40a40d60c28718b50f5600e05c496a982f9f499c04d80f9e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294622464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfa952d58e30aa2711dbeb8abcc4e70f27e5ed3ebe16e63c1c12b8642016ec2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61267d89978ab3ab775d217fd01b9f59b054d41cb3b70b13746a2a62eca5677f`  
		Last Modified: Mon, 02 Dec 2024 20:39:22 GMT  
		Size: 52.9 MB (52946253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f5c65e82878a882751b85d69f1b5e1fef9e5a1e2b6e8c6fb91b5a9106f0035`  
		Last Modified: Mon, 02 Dec 2024 20:39:25 GMT  
		Size: 237.6 MB (237588485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:83e6d986399402cf4f87ea920e42c14d1a2b3c9042fd6228a3c8591086bb011d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5040baee093c81f9e4600e14249874276bb6b1011b669a6c4d5962dac288d7`

```dockerfile
```

-	Layers:
	-	`sha256:0607df65216df8538ba3def2f4c315296c5b0fe079a14242b9b8819fc0879ad4`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 746.5 KB (746526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1a8c49a90f68976a179692f548c3e83293af8f8637778ff9a85839ff9df4b8`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83-bookworm`

```console
$ docker pull rust@sha256:d242a48452a5f6f490e1c13d3340d54ead1198948a4585dc42e326d6eacd07d1
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

### `rust:1.83-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:71aa4f8bdbfb924be55914e8910657aaf15420a87649ea1c64de6f3aef99b357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.7 MB (540737368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51381ded149a6148696b8fd088a50b9684925a0f5c26541db5d3a99db5aae059`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bc823accc52b76a805eb38c2d85f6916c18b62280e12ef86557cf7aae9f958b5`  
		Last Modified: Mon, 02 Dec 2024 20:24:37 GMT  
		Size: 191.4 MB (191418150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:6f2bd220e2f16cb7fe49a9b9ad87295829ed6ebf6b745b45163ccb5c6758e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2628cb17b709463f28662019efa1ac6f3499b61335860965970c347da12bc324`

```dockerfile
```

-	Layers:
	-	`sha256:286a3f2db2c8a6d92215bd0e79bef8cc02de285df8e4a1a45cf8e27b0ab0e625`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 15.5 MB (15500541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dea8927ea34a8749863f37f48d5c3386465f87be87fca83ebfb2da54e47f09`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:c4eab5718491261254547e9dee552013f246ffd187d3fe1c1427b2ca4b061ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526493619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b2f5c8fb2f32e205088f699538ac30a1f60f942ca99b46a7d63ee474294911`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:e64ed70b984c825bcf2c316778efdf694d1177f214c907b60097f528bbda5cf8`  
		Last Modified: Mon, 02 Dec 2024 20:29:54 GMT  
		Size: 224.5 MB (224498211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:be5458af59d7a9d4850ec727e792fe1ce39320e685eba63907c07a62c663a19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15317922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8513824646d633879f3b9c31a95e4313b646af70856500a177c618bb79ec94`

```dockerfile
```

-	Layers:
	-	`sha256:d5013ef9b8a7a070d15a1c43f9eb413d3814d5083868ad3477c7ca363e2629e8`  
		Last Modified: Mon, 02 Dec 2024 20:29:49 GMT  
		Size: 15.3 MB (15304676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a68401994195014fb21c06bdf19c124aea45e5bef8843f712d311bdfced543`  
		Last Modified: Mon, 02 Dec 2024 20:29:48 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f53e59e92e0aeabaf6660d225a107e99c545db88292aa0b26c622e74a040d965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 MB (592017331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c109228921d40f3351cd8c44731f364371c3d17735ca2a5e5f91c306a0dfbfa`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:73de18a65d13f2c8a09a8d948d31e3de3f45af2bead8f228a386915adb234c35`  
		Last Modified: Mon, 02 Dec 2024 20:35:51 GMT  
		Size: 251.8 MB (251804771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c509b7be5dcd87df97728f5298103aa353944b0f8c8f7d25b5b4b7d797017c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15542437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6766be12848456f1e52235b69ad6e4a319291879e57f2a2238bef89da8f3f9e`

```dockerfile
```

-	Layers:
	-	`sha256:98ab1278bc14cd425e7f3eed1e29aae39b73c5f89b91ccc51caee870f35910be`  
		Last Modified: Mon, 02 Dec 2024 20:35:45 GMT  
		Size: 15.5 MB (15529147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9709d89560fe98a5ae0be73fdda845fa48e30c80363bbca1ff69fdb179217095`  
		Last Modified: Mon, 02 Dec 2024 20:35:44 GMT  
		Size: 13.3 KB (13290 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-bookworm` - linux; 386

```console
$ docker pull rust@sha256:2b7d61e0cace1004b172c4c485053c11bc9a0f8bb92c9af92b22ff6d35ea5ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (556034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fe164933a80fc8c7abf32c417a466d96db3609b6f1ee14d861525cfdd78fea`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:336b9aae3521ef72851abe97810af76d93937f45be24b0cb67340ff9444cb707`  
		Last Modified: Mon, 02 Dec 2024 20:24:45 GMT  
		Size: 204.1 MB (204137618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2972bbfcb74add45006671eba779b040f9bf6bf4e3f7135555a34491df439bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b839cc63e7b08f07e283f08b415463fb2ab045791fdd19edf58fa0f210451796`

```dockerfile
```

-	Layers:
	-	`sha256:fd8c3f67164e288cb011c211b630adad3ad6454abdf247636e1be356b57369e7`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bde4a6f2185736694cd07ae59ade73bff87e8e8e38ea4758ae457fe22cf0bb7b`  
		Last Modified: Mon, 02 Dec 2024 20:24:39 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:1a3ec9464aaca3679e309b5a2d37d74b8ee5c1d49087f1580d6490b05dff4c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.7 MB (611728786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc406666b8bba58ebe80d82916ba809f85bc3d079aea65006a7189adc4fa98d`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bb1560f641778d2cb5455f2c6681cb70f74871be341fc94de016ad79eb2311af`  
		Last Modified: Mon, 02 Dec 2024 20:26:21 GMT  
		Size: 248.3 MB (248313252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4afd1f4300f64430965f43299137ca75249e7c27fbf74de6f92b8393fa33afa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab512b7df0c02174eb212c06d747326403186f429de36c0a0613f77795a9463`

```dockerfile
```

-	Layers:
	-	`sha256:1014165fb7c18bc7f0f45b139b7defb3fdaac4819329563e7b9abfd971721ca9`  
		Last Modified: Mon, 02 Dec 2024 20:26:15 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:971d6fde5f27e47969a782345543d65c64c4609aa41146345e4a00de2400f898`  
		Last Modified: Mon, 02 Dec 2024 20:26:14 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:6fc1e9e942c9ad8d4445769678468782e33f232441a2107277aa9309c8171531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.4 MB (593416662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb95fc496432694f3664ec33ed661538c8d318eddb1848edd90df4e723030f4`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:c731e424a0e50fe1d61cdc956a2238603eb68c82b94428b992cdd8b46e4494ca`  
		Last Modified: Mon, 02 Dec 2024 20:26:44 GMT  
		Size: 274.6 MB (274619819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a6f9b86026a3aa6e8f0f74e68331895240fe3be10c6d92205fb9e48ff2e3cc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d159b76c2f0dbfef842d8141ba3fb10cf86a429132d7f363f0b81aaf4d7cbd`

```dockerfile
```

-	Layers:
	-	`sha256:e33f6f4afffd15877fb13164def1212d1e66c7616414660e48f2ca508e1427c3`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 15.3 MB (15312980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158597ba495f8617e6dc77be65c0b5dcabe1b602984b6babf8551c0eba26c5d7`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83-bullseye`

```console
$ docker pull rust@sha256:48e32924c033e231995e5d604fc0bde746603529ab9c9525ed69551d1763722f
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

### `rust:1.83-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:3b69b1344468f45d6841e7d7eeddb646a6109c51ba6ad84867d40ce93bdb6507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.9 MB (513894985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1322104423ebd73df2358552ad57a4775ed183c222ff55d72233ce9c62b8e0c4`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:74d39ef915c9431d8814f436f6c5a05c033b7d061a908a761893aba712738dca`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 191.4 MB (191418226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:464848c0989553e6f5c696e1e8f488b2fd360b489a7c71bfc156c6c854921e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aed3439b87c35516bfcefed896ac0fbc064e92cdc1fc24c50cf3f4f82a470b8`

```dockerfile
```

-	Layers:
	-	`sha256:d5e8c58afb3cd8c33d2faf04883bb9f40a4d9ed6d20d0f401f4edc4b73f3f483`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 15.1 MB (15099560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7b47989b19887839396cc56566eed4407f3d0105f1bbb3dedb3ae59ecc329`  
		Last Modified: Mon, 02 Dec 2024 20:24:39 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:ef4925470bc527b51f98b8fd0e090015ba06289dce879ce02540c523a950492c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.6 MB (507587556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d219ef379dcd3a55ce17998421a285fdcae9d0e18e6dc6719f234d8ba6fdba2`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:460e72c81a8faf8a12fa4517b675bc73c5173407737e669feb3c5c0de5acdf15`  
		Last Modified: Mon, 02 Dec 2024 20:33:45 GMT  
		Size: 224.5 MB (224498199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8ffb613d6c04af1f4a4c9dad7c9046e06244f7a51eafe51ef0239aa93e16887b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5692a48de82943f6da6098bdb2f952d25c38b546e4aad806bba8904ea5c1086f`

```dockerfile
```

-	Layers:
	-	`sha256:0c4c1556ccde855c9606ac4814d71b557174cf8f2b9521f60c9cea5219852703`  
		Last Modified: Mon, 02 Dec 2024 20:33:40 GMT  
		Size: 14.9 MB (14900067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea7e331de6703885f45617be049222c6f6d6474c6b8b1e74d1493ea5482878c9`  
		Last Modified: Mon, 02 Dec 2024 20:33:39 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b92b53e23598b9accd960a82d00386d9c100495c88f77a4aac5b6983bfd24697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.9 MB (565925019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0b729695c79cc2b5ab22d9798c6a3c74ab86f10b3c7e147e82236a28cdac7`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:2d9513256f7bf83972d3d8a5644bef3b31913ac18f945e7bda5e1b67800b99ff`  
		Last Modified: Mon, 02 Dec 2024 20:32:52 GMT  
		Size: 251.8 MB (251804822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1c90a3d5572cdeb856d417ebbc90b19c0c4ad64b5ac8849d506106dea513ae57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15113175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53bdc544237eb3432d49c4682f0fe3627f7d36735a5cb1865033529582e0fe6`

```dockerfile
```

-	Layers:
	-	`sha256:58f3bb41e62e5e98de42e3be870f748aec12d2a62f8576bac1c8869337ee9e15`  
		Last Modified: Mon, 02 Dec 2024 20:32:47 GMT  
		Size: 15.1 MB (15101822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9d1ceb3d92c5f213ec0ca376ec575dd98f09f32d6d5430b2555d6c0b7562d1`  
		Last Modified: Mon, 02 Dec 2024 20:32:46 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-bullseye` - linux; 386

```console
$ docker pull rust@sha256:a534b238c9b99b740f1216486f77bf3c14cea88e3a9e1bbf070d86fbab5bb0fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.3 MB (532304484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18675ba81d558cf8f9ec3d367d8c3ec104bff1aab30160b88e8bc51d23329c49`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:8c0d713557008a8d69677c0aa162eedcab0ac7846ed90aee9c2d5788a51fad0f`  
		Last Modified: Mon, 02 Dec 2024 20:24:51 GMT  
		Size: 204.1 MB (204137636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:74c74e7676b304b2cb4c939116791d252bdd51e0bf9e358dcb40dad59a622617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15097814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c3da0659cf7eddc4df08832981dc114a0434eff8cff0f7e0a5318dcda2ea8d`

```dockerfile
```

-	Layers:
	-	`sha256:e179a67825d943f6221f1e2e7a9c60df8de969054fec98b3538bbf4a5682769b`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 15.1 MB (15086597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6b6fde063e7e47ab87f2ab98387725a5cbba86c1ba5665ba2280757cd267dd0`  
		Last Modified: Mon, 02 Dec 2024 20:24:46 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83-slim`

```console
$ docker pull rust@sha256:2808c258e14c25a1277d7ba6e653093ef00ba088dc73d99402a900e8cc218d5c
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

### `rust:1.83-slim` - linux; amd64

```console
$ docker pull rust@sha256:6a3be2a97d72a2d401807e494ff0b2d500bb241293db2f8d84e16b629f952366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291337423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae1dcbb4bdaada87c1f2a5397fb3e2534cd10a921d8b38ab8e032613d4bec82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbfe6cc0ca59f7757297ccc9049930ac7f37bccab06b5fb02b80eb1d37e4a48`  
		Last Modified: Mon, 02 Dec 2024 20:24:38 GMT  
		Size: 262.2 MB (262209428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim` - unknown; unknown

```console
$ docker pull rust@sha256:1a1e9a3dd7b8efd48e40f7a424dd24b8ba15de70d687a06656717edbb9048faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1ba3680f55e2998a08ff5c873a90a1249c120eba4a76d95874c78c7e755812`

```dockerfile
```

-	Layers:
	-	`sha256:190def7ed7dafd6d8ee1ba46e117570e708371dde8e290f4c757acd3f543a0da`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 4.0 MB (3960916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3749ab658f8ad4f8d17c77b275dd953cfdf9c2de24728be40fda41f514178b`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:6d7afc9f25f7a5cefc9b6f3fbf2304e89502533bf562b3d008f1d7e98e849723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297059662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302b6a008c606c7cd8b9263e55bcb04488d3fe948c1a45f2f7a6b2e9f6c11f23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defe357fcbe93d1e65d0570d021785ad676696d2d624262bdb0e214723689b36`  
		Last Modified: Mon, 02 Dec 2024 20:31:38 GMT  
		Size: 272.3 MB (272340753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3f2058fe6f54a997932102d8b6bc235e8d4666e331b9296243cf75c70990da78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7fc6c7b289d0a098a407027d015ead0708a0e04655389eae49e4155b848f52`

```dockerfile
```

-	Layers:
	-	`sha256:8928a87a6013ae9d938cea84efc86dfc5fb240cf83f931e727c7693adaa6da2c`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 3.8 MB (3776732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea6b01b234f1e08ebc59a4a02bda774ffe04cf102809435a132937896e535eaf`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:594e5e30e34cb3f1edfcf62b6c42ab7418bfbe4fd83057099fede39488edc7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.8 MB (346802313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3d008bad10df60f61201660a99f5d86423c1a1a546c0a1a1838123d75a27a1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0237173b80106fe0760a817d7e6d1c71f9e5e284c512b7d06074708c59aff7`  
		Last Modified: Mon, 02 Dec 2024 20:37:13 GMT  
		Size: 317.6 MB (317644957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim` - unknown; unknown

```console
$ docker pull rust@sha256:895f4818b23e10a7e1f1880f5e42eb988a221a3a0eb6f39134e09fa24dcf11ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e2f37d04cfed0d9e84101878c4064b4b8353ce7996f5587a68e63f1e717bd8`

```dockerfile
```

-	Layers:
	-	`sha256:05e0e8f9842371d47373dc72339abb01c46ebf232229e4810af7074cc8f68115`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 4.0 MB (3983284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b63a1b31beb1e3b516d716bd7530b21f5698318b664ff2c0808a3a6738dbc2`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-slim` - linux; 386

```console
$ docker pull rust@sha256:e3a12bd5e08f7ffd7c014c2820aa4bbb647a30f3617f59659136669d0765cde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301886447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3c3937265088583d6ea42714a975738f2bf863ef26ec51c0eceafa294d88e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ceb72ece1ea1e0fe9569779176af4568889e4706901654739657a99aa4700`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 271.7 MB (271740997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim` - unknown; unknown

```console
$ docker pull rust@sha256:ea30beb0ac18971c71310961164ae02c93873a3dee5e71820cb92ca5af9cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad0f3a1a05782cc497e5841bd1cba942630e16eb84acaf9a3809618df1ee6d`

```dockerfile
```

-	Layers:
	-	`sha256:bf795665c0773ee9ebba9af59adaf88084fc89e625ffd096983779a3322b9d98`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea300ff11941e5c8c9dca6dae2eaeb1b7aa9ff4ffacb336422e939217214bca`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:901e8fd72a554e505e9273538a8ad34c2bf33a02f62b634250d35e34bb2ded90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.2 MB (350198087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c2aef4eee77ed0f0829ba276a911bf8cd57b8afb28b00184b775c489a82bb4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a607df9bd35302bace9a6ad9223bd9a4b868b9c462a42e5cca65d5fd3d8a9b`  
		Last Modified: Mon, 02 Dec 2024 20:29:03 GMT  
		Size: 317.1 MB (317072734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim` - unknown; unknown

```console
$ docker pull rust@sha256:12a9974e9bd55d24e84c10e72f5170591f010651e62da1a001cce00b60a8b5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f48e8cf17275373c2886d5d424e13f54217678435465c09519f9d27932b9a4`

```dockerfile
```

-	Layers:
	-	`sha256:1969029d7112da6fdd40a3a936b1152b38032abb4d7bd1bc31411ed5fd021715`  
		Last Modified: Mon, 02 Dec 2024 20:28:53 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52df272aeab4c0542aa89ec9e6638cabd6465bf962ee7053c5eac2b05e53b44d`  
		Last Modified: Mon, 02 Dec 2024 20:28:52 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-slim` - linux; s390x

```console
$ docker pull rust@sha256:59e72321724e973f7b278fe9cfdbc7916988c33529e4f16eaa3be7e72b4d7b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352217458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c145addc8a9384eb579adb69c9d9500d0a57a3690e0e396cdce0b24098684ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e04d7c8b55a5ef929486fce3eca63d3be7958f04b601f4f73a52e9591e4a16`  
		Last Modified: Mon, 02 Dec 2024 20:28:50 GMT  
		Size: 324.7 MB (324725830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim` - unknown; unknown

```console
$ docker pull rust@sha256:34d0adfbc6046e33a5307df483d7f0626cfbedc28bc7cb0fa092b40008a9d30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3815877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4d233def5b8a5cbdca87e1d70f4c0e5602f12e771f4e9c36399233edb2ef42`

```dockerfile
```

-	Layers:
	-	`sha256:a2bb7709243f1094bc9ed02cbe32492f025e7ba1b46404d9f64f3527d774ce68`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 3.8 MB (3802606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60ee2d606d582a3328f010baeb9968ac6e723667c4dac109be44717dae4d543`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83-slim-bookworm`

```console
$ docker pull rust@sha256:2808c258e14c25a1277d7ba6e653093ef00ba088dc73d99402a900e8cc218d5c
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

### `rust:1.83-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:6a3be2a97d72a2d401807e494ff0b2d500bb241293db2f8d84e16b629f952366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291337423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae1dcbb4bdaada87c1f2a5397fb3e2534cd10a921d8b38ab8e032613d4bec82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbfe6cc0ca59f7757297ccc9049930ac7f37bccab06b5fb02b80eb1d37e4a48`  
		Last Modified: Mon, 02 Dec 2024 20:24:38 GMT  
		Size: 262.2 MB (262209428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1a1e9a3dd7b8efd48e40f7a424dd24b8ba15de70d687a06656717edbb9048faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1ba3680f55e2998a08ff5c873a90a1249c120eba4a76d95874c78c7e755812`

```dockerfile
```

-	Layers:
	-	`sha256:190def7ed7dafd6d8ee1ba46e117570e708371dde8e290f4c757acd3f543a0da`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 4.0 MB (3960916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3749ab658f8ad4f8d17c77b275dd953cfdf9c2de24728be40fda41f514178b`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:6d7afc9f25f7a5cefc9b6f3fbf2304e89502533bf562b3d008f1d7e98e849723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297059662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302b6a008c606c7cd8b9263e55bcb04488d3fe948c1a45f2f7a6b2e9f6c11f23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defe357fcbe93d1e65d0570d021785ad676696d2d624262bdb0e214723689b36`  
		Last Modified: Mon, 02 Dec 2024 20:31:38 GMT  
		Size: 272.3 MB (272340753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3f2058fe6f54a997932102d8b6bc235e8d4666e331b9296243cf75c70990da78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7fc6c7b289d0a098a407027d015ead0708a0e04655389eae49e4155b848f52`

```dockerfile
```

-	Layers:
	-	`sha256:8928a87a6013ae9d938cea84efc86dfc5fb240cf83f931e727c7693adaa6da2c`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 3.8 MB (3776732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea6b01b234f1e08ebc59a4a02bda774ffe04cf102809435a132937896e535eaf`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:594e5e30e34cb3f1edfcf62b6c42ab7418bfbe4fd83057099fede39488edc7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.8 MB (346802313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3d008bad10df60f61201660a99f5d86423c1a1a546c0a1a1838123d75a27a1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0237173b80106fe0760a817d7e6d1c71f9e5e284c512b7d06074708c59aff7`  
		Last Modified: Mon, 02 Dec 2024 20:37:13 GMT  
		Size: 317.6 MB (317644957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:895f4818b23e10a7e1f1880f5e42eb988a221a3a0eb6f39134e09fa24dcf11ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e2f37d04cfed0d9e84101878c4064b4b8353ce7996f5587a68e63f1e717bd8`

```dockerfile
```

-	Layers:
	-	`sha256:05e0e8f9842371d47373dc72339abb01c46ebf232229e4810af7074cc8f68115`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 4.0 MB (3983284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b63a1b31beb1e3b516d716bd7530b21f5698318b664ff2c0808a3a6738dbc2`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:e3a12bd5e08f7ffd7c014c2820aa4bbb647a30f3617f59659136669d0765cde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301886447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3c3937265088583d6ea42714a975738f2bf863ef26ec51c0eceafa294d88e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ceb72ece1ea1e0fe9569779176af4568889e4706901654739657a99aa4700`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 271.7 MB (271740997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ea30beb0ac18971c71310961164ae02c93873a3dee5e71820cb92ca5af9cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad0f3a1a05782cc497e5841bd1cba942630e16eb84acaf9a3809618df1ee6d`

```dockerfile
```

-	Layers:
	-	`sha256:bf795665c0773ee9ebba9af59adaf88084fc89e625ffd096983779a3322b9d98`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea300ff11941e5c8c9dca6dae2eaeb1b7aa9ff4ffacb336422e939217214bca`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:901e8fd72a554e505e9273538a8ad34c2bf33a02f62b634250d35e34bb2ded90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.2 MB (350198087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c2aef4eee77ed0f0829ba276a911bf8cd57b8afb28b00184b775c489a82bb4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a607df9bd35302bace9a6ad9223bd9a4b868b9c462a42e5cca65d5fd3d8a9b`  
		Last Modified: Mon, 02 Dec 2024 20:29:03 GMT  
		Size: 317.1 MB (317072734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:12a9974e9bd55d24e84c10e72f5170591f010651e62da1a001cce00b60a8b5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f48e8cf17275373c2886d5d424e13f54217678435465c09519f9d27932b9a4`

```dockerfile
```

-	Layers:
	-	`sha256:1969029d7112da6fdd40a3a936b1152b38032abb4d7bd1bc31411ed5fd021715`  
		Last Modified: Mon, 02 Dec 2024 20:28:53 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52df272aeab4c0542aa89ec9e6638cabd6465bf962ee7053c5eac2b05e53b44d`  
		Last Modified: Mon, 02 Dec 2024 20:28:52 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:59e72321724e973f7b278fe9cfdbc7916988c33529e4f16eaa3be7e72b4d7b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352217458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c145addc8a9384eb579adb69c9d9500d0a57a3690e0e396cdce0b24098684ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e04d7c8b55a5ef929486fce3eca63d3be7958f04b601f4f73a52e9591e4a16`  
		Last Modified: Mon, 02 Dec 2024 20:28:50 GMT  
		Size: 324.7 MB (324725830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:34d0adfbc6046e33a5307df483d7f0626cfbedc28bc7cb0fa092b40008a9d30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3815877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4d233def5b8a5cbdca87e1d70f4c0e5602f12e771f4e9c36399233edb2ef42`

```dockerfile
```

-	Layers:
	-	`sha256:a2bb7709243f1094bc9ed02cbe32492f025e7ba1b46404d9f64f3527d774ce68`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 3.8 MB (3802606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60ee2d606d582a3328f010baeb9968ac6e723667c4dac109be44717dae4d543`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83-slim-bullseye`

```console
$ docker pull rust@sha256:cd64d55bf5d90faca3b5e69039e03cc8eaf4d0c531537cb08d20ee8ee87f438f
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

### `rust:1.83-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:693226f9da3b618f747e1d45901d1d6c27e591f5d3d17c92685a55f4983911ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.8 MB (282812182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecfd0a5420dc73cd925c46f1879d9c00df802531eccda112b2d406071cacca0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384329ccf6be51bb1ef6f2b07175dcdcebcf898a37bba183bfe10f903be995ce`  
		Last Modified: Mon, 02 Dec 2024 20:24:22 GMT  
		Size: 251.4 MB (251360621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ebc287a15a3e3cd43102b0e5b3df9aae5ae0a8cd284c6cd6845bc32e9e0b5903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4191040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8375006c14246df12ba094238c9468666ade0d799bb9d20f012e4f299847e56a`

```dockerfile
```

-	Layers:
	-	`sha256:74af93f126d4c06de89836c2cf05cebb553960e94e4ab55a74d46b28183ad983`  
		Last Modified: Mon, 02 Dec 2024 20:24:19 GMT  
		Size: 4.2 MB (4179684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c366dfc129927914c32fbdf3b3a7128249ed30666f407a63a7ff0f19be5aff8`  
		Last Modified: Mon, 02 Dec 2024 20:24:18 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:abf606a99416890d34310c1ed7c2dc863aa6a1ce4f8ab588c768b2511ffdaa5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.2 MB (293172521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4ff907c925646494aeeb07f6a9c015b9f209c836a858b44c751fffc645ed1b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fffe59376f64ffa8f62067ec6c177458ad560736ecb62f5a746b99a1213febb`  
		Last Modified: Mon, 02 Dec 2024 20:27:46 GMT  
		Size: 266.6 MB (266563264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6ec69ccb3c2df674b652af2bf87b9af3d1c186c907bacf211557fca6a0605d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d2e1fea37fd47ebcb90737269a9a15f43d09ff6e3a8ac409221ed3d6a3b8d3`

```dockerfile
```

-	Layers:
	-	`sha256:b11be9c55ffbd97983468ba6c80f6bfb1b6d2f881f28c132a972181a2f323cf1`  
		Last Modified: Mon, 02 Dec 2024 20:27:40 GMT  
		Size: 4.0 MB (3988606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9172172b88ef1546ba7e0d5edb4641fbb14bdf07ff13f0bb89ccbb6102cb8a32`  
		Last Modified: Mon, 02 Dec 2024 20:27:40 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a32ae5ae9cad532df229a1fef4ada9991409591a7ccf15c3856ba3ca21d7c26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.4 MB (337389995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504b549e7eafa02320debcac41241b24c3e628c6a7f2c4a085a0e8430d5fa44f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b17b8db729381225a8d73b8af06a440c8b3f44ba100df98709bb0b03c0a016`  
		Last Modified: Mon, 02 Dec 2024 20:34:10 GMT  
		Size: 307.3 MB (307298395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3b6d85ff4952c3db80e6f66474078bd4e09bc1b884e7978509e0cf8a7c4410ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4187819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2535b26d94240ff8a8243d5fcaf6cd4f3238cc6575f145c7055f3be7a7af6e18`

```dockerfile
```

-	Layers:
	-	`sha256:280d6fd398dd958493aa5d431829910d0726c625baf5513aa3477e64de936e0d`  
		Last Modified: Mon, 02 Dec 2024 20:34:04 GMT  
		Size: 4.2 MB (4176359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb393af559bdc07a24e80a9442f17ed5976eafc6cced8e26e7df0a3132f88ce7`  
		Last Modified: Mon, 02 Dec 2024 20:34:04 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:d5af146980a072b682d3ac22609ffed95252933df15d14690667925cf35a83bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297129117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182df1c816edafaeadc3362a748a39f671aa57bf19f6d7fafd20bcb2a4becdd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a29bf3a9090d3e58d845509836c32130197f51dc0eafb75e2102450607aa614`  
		Last Modified: Mon, 02 Dec 2024 20:24:48 GMT  
		Size: 264.7 MB (264705766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:de112da84d3f18bbad7559779bde4d938157704801863564aaae2a20e856f0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaa8827be2c8dbe784a39a4b999bb4842aa2514d900dbd211b897aabc55f32b`

```dockerfile
```

-	Layers:
	-	`sha256:1e6ab84278603cf43cd88053eb59875eea8a1a59d9a120bb129fdeff7482806d`  
		Last Modified: Mon, 02 Dec 2024 20:24:41 GMT  
		Size: 4.2 MB (4169952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67bd2e3b5300c4b614ff1c265cf9f027c92cb2fd18db1cac9fc58fb89c69ea17`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83.0`

```console
$ docker pull rust@sha256:d242a48452a5f6f490e1c13d3340d54ead1198948a4585dc42e326d6eacd07d1
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

### `rust:1.83.0` - linux; amd64

```console
$ docker pull rust@sha256:71aa4f8bdbfb924be55914e8910657aaf15420a87649ea1c64de6f3aef99b357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.7 MB (540737368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51381ded149a6148696b8fd088a50b9684925a0f5c26541db5d3a99db5aae059`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bc823accc52b76a805eb38c2d85f6916c18b62280e12ef86557cf7aae9f958b5`  
		Last Modified: Mon, 02 Dec 2024 20:24:37 GMT  
		Size: 191.4 MB (191418150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0` - unknown; unknown

```console
$ docker pull rust@sha256:6f2bd220e2f16cb7fe49a9b9ad87295829ed6ebf6b745b45163ccb5c6758e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2628cb17b709463f28662019efa1ac6f3499b61335860965970c347da12bc324`

```dockerfile
```

-	Layers:
	-	`sha256:286a3f2db2c8a6d92215bd0e79bef8cc02de285df8e4a1a45cf8e27b0ab0e625`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 15.5 MB (15500541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dea8927ea34a8749863f37f48d5c3386465f87be87fca83ebfb2da54e47f09`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0` - linux; arm variant v7

```console
$ docker pull rust@sha256:c4eab5718491261254547e9dee552013f246ffd187d3fe1c1427b2ca4b061ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526493619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b2f5c8fb2f32e205088f699538ac30a1f60f942ca99b46a7d63ee474294911`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:e64ed70b984c825bcf2c316778efdf694d1177f214c907b60097f528bbda5cf8`  
		Last Modified: Mon, 02 Dec 2024 20:29:54 GMT  
		Size: 224.5 MB (224498211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0` - unknown; unknown

```console
$ docker pull rust@sha256:be5458af59d7a9d4850ec727e792fe1ce39320e685eba63907c07a62c663a19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15317922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8513824646d633879f3b9c31a95e4313b646af70856500a177c618bb79ec94`

```dockerfile
```

-	Layers:
	-	`sha256:d5013ef9b8a7a070d15a1c43f9eb413d3814d5083868ad3477c7ca363e2629e8`  
		Last Modified: Mon, 02 Dec 2024 20:29:49 GMT  
		Size: 15.3 MB (15304676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a68401994195014fb21c06bdf19c124aea45e5bef8843f712d311bdfced543`  
		Last Modified: Mon, 02 Dec 2024 20:29:48 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f53e59e92e0aeabaf6660d225a107e99c545db88292aa0b26c622e74a040d965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 MB (592017331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c109228921d40f3351cd8c44731f364371c3d17735ca2a5e5f91c306a0dfbfa`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:73de18a65d13f2c8a09a8d948d31e3de3f45af2bead8f228a386915adb234c35`  
		Last Modified: Mon, 02 Dec 2024 20:35:51 GMT  
		Size: 251.8 MB (251804771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0` - unknown; unknown

```console
$ docker pull rust@sha256:c509b7be5dcd87df97728f5298103aa353944b0f8c8f7d25b5b4b7d797017c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15542437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6766be12848456f1e52235b69ad6e4a319291879e57f2a2238bef89da8f3f9e`

```dockerfile
```

-	Layers:
	-	`sha256:98ab1278bc14cd425e7f3eed1e29aae39b73c5f89b91ccc51caee870f35910be`  
		Last Modified: Mon, 02 Dec 2024 20:35:45 GMT  
		Size: 15.5 MB (15529147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9709d89560fe98a5ae0be73fdda845fa48e30c80363bbca1ff69fdb179217095`  
		Last Modified: Mon, 02 Dec 2024 20:35:44 GMT  
		Size: 13.3 KB (13290 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0` - linux; 386

```console
$ docker pull rust@sha256:2b7d61e0cace1004b172c4c485053c11bc9a0f8bb92c9af92b22ff6d35ea5ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (556034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fe164933a80fc8c7abf32c417a466d96db3609b6f1ee14d861525cfdd78fea`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:336b9aae3521ef72851abe97810af76d93937f45be24b0cb67340ff9444cb707`  
		Last Modified: Mon, 02 Dec 2024 20:24:45 GMT  
		Size: 204.1 MB (204137618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0` - unknown; unknown

```console
$ docker pull rust@sha256:2972bbfcb74add45006671eba779b040f9bf6bf4e3f7135555a34491df439bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b839cc63e7b08f07e283f08b415463fb2ab045791fdd19edf58fa0f210451796`

```dockerfile
```

-	Layers:
	-	`sha256:fd8c3f67164e288cb011c211b630adad3ad6454abdf247636e1be356b57369e7`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bde4a6f2185736694cd07ae59ade73bff87e8e8e38ea4758ae457fe22cf0bb7b`  
		Last Modified: Mon, 02 Dec 2024 20:24:39 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0` - linux; ppc64le

```console
$ docker pull rust@sha256:1a3ec9464aaca3679e309b5a2d37d74b8ee5c1d49087f1580d6490b05dff4c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.7 MB (611728786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc406666b8bba58ebe80d82916ba809f85bc3d079aea65006a7189adc4fa98d`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bb1560f641778d2cb5455f2c6681cb70f74871be341fc94de016ad79eb2311af`  
		Last Modified: Mon, 02 Dec 2024 20:26:21 GMT  
		Size: 248.3 MB (248313252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0` - unknown; unknown

```console
$ docker pull rust@sha256:4afd1f4300f64430965f43299137ca75249e7c27fbf74de6f92b8393fa33afa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab512b7df0c02174eb212c06d747326403186f429de36c0a0613f77795a9463`

```dockerfile
```

-	Layers:
	-	`sha256:1014165fb7c18bc7f0f45b139b7defb3fdaac4819329563e7b9abfd971721ca9`  
		Last Modified: Mon, 02 Dec 2024 20:26:15 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:971d6fde5f27e47969a782345543d65c64c4609aa41146345e4a00de2400f898`  
		Last Modified: Mon, 02 Dec 2024 20:26:14 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0` - linux; s390x

```console
$ docker pull rust@sha256:6fc1e9e942c9ad8d4445769678468782e33f232441a2107277aa9309c8171531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.4 MB (593416662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb95fc496432694f3664ec33ed661538c8d318eddb1848edd90df4e723030f4`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:c731e424a0e50fe1d61cdc956a2238603eb68c82b94428b992cdd8b46e4494ca`  
		Last Modified: Mon, 02 Dec 2024 20:26:44 GMT  
		Size: 274.6 MB (274619819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0` - unknown; unknown

```console
$ docker pull rust@sha256:a6f9b86026a3aa6e8f0f74e68331895240fe3be10c6d92205fb9e48ff2e3cc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d159b76c2f0dbfef842d8141ba3fb10cf86a429132d7f363f0b81aaf4d7cbd`

```dockerfile
```

-	Layers:
	-	`sha256:e33f6f4afffd15877fb13164def1212d1e66c7616414660e48f2ca508e1427c3`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 15.3 MB (15312980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158597ba495f8617e6dc77be65c0b5dcabe1b602984b6babf8551c0eba26c5d7`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83.0-alpine`

```console
$ docker pull rust@sha256:838d384a1138fe1f2e448e3901bb3d23683570ba3dca581160880ffad760332b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.83.0-alpine` - linux; amd64

```console
$ docker pull rust@sha256:88a66dc9c1ac1f281b82efafd2b33db603d1ce07f9e4e1bbbe9d3fceef0cdd72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290128622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e791fdca85c41d01da61496939bb1c3e40ef365c768e19e018ded15901356c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dcbc4b34b53bc9e532e413490c8f92a11e6a1682223532ea90597337ed5def`  
		Last Modified: Mon, 02 Dec 2024 20:24:27 GMT  
		Size: 55.3 MB (55309206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a818bb3055598f9d975638712fd88bcf5d9faea94cae98e3059ff8680f4a2cdb`  
		Last Modified: Mon, 02 Dec 2024 20:24:30 GMT  
		Size: 231.2 MB (231195512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:1f4b461f3a7aa6a1d4fbbb717befabe3f146ebbf6ca6f427fe69ce8aebbc3425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eae7f8256cd37b35f89f9fc66faa1f8cd9fb813cbb64c747f44f461117e133`

```dockerfile
```

-	Layers:
	-	`sha256:07d675aac3f963b3a7bcc70c8f78fe4d629b3b9a64ff5d9ca285bf702237511a`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 710.5 KB (710491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a813425ea6f27d41933a1b5e80e290317aa6794a3ea8d7899cdc65dc38852d6d`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14d4e74fdaa1be40a40d60c28718b50f5600e05c496a982f9f499c04d80f9e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294622464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfa952d58e30aa2711dbeb8abcc4e70f27e5ed3ebe16e63c1c12b8642016ec2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61267d89978ab3ab775d217fd01b9f59b054d41cb3b70b13746a2a62eca5677f`  
		Last Modified: Mon, 02 Dec 2024 20:39:22 GMT  
		Size: 52.9 MB (52946253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f5c65e82878a882751b85d69f1b5e1fef9e5a1e2b6e8c6fb91b5a9106f0035`  
		Last Modified: Mon, 02 Dec 2024 20:39:25 GMT  
		Size: 237.6 MB (237588485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:83e6d986399402cf4f87ea920e42c14d1a2b3c9042fd6228a3c8591086bb011d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5040baee093c81f9e4600e14249874276bb6b1011b669a6c4d5962dac288d7`

```dockerfile
```

-	Layers:
	-	`sha256:0607df65216df8538ba3def2f4c315296c5b0fe079a14242b9b8819fc0879ad4`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 746.5 KB (746526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1a8c49a90f68976a179692f548c3e83293af8f8637778ff9a85839ff9df4b8`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83.0-alpine3.19`

```console
$ docker pull rust@sha256:c22e43db16b649a713eb39606c5054dd072eed35a7acffe05e295749c8a7eed3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.83.0-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:51158a1b5d1531f739f78b9ececd3c074e75bf5cc18b4c7b63b1a891c4216740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (289961960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47c29028d898cefa39de15d160ad8cc6cdb1d1dacf206c360c4b4d7d045eb10`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88faabca0966b648ec58d261009681663f60798257994a9281be6f9b359864d0`  
		Last Modified: Mon, 02 Dec 2024 20:24:21 GMT  
		Size: 55.3 MB (55346817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6927d0b73da7baf8ea757697b138a23dc5a1196a24f50ae7a26794aba2b17cd`  
		Last Modified: Mon, 02 Dec 2024 20:24:23 GMT  
		Size: 231.2 MB (231195415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:62a85d1b9963d7c5b3276c4f04bd4d2a32be81c6551a6a6cdb5cf11dd077d933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.7 KB (723693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232ac0ffe4a86028aaba1f2e862002fdd2b4ff1731bb1c90c21401078f6dbd42`

```dockerfile
```

-	Layers:
	-	`sha256:05cdb77f193f20e943f1f0d26b0bb06e83851c90af78776aa9399c35f9aa807b`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 713.0 KB (712979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6cf2aab24ba344de6369df5fa858a9401710c70dc1af99a87e867c019cfd3c4`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b0c30be9019c61d2b4530ec4a206cbf74cf620f9e664db3e2397e50a5dfac14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293943317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170301d6a34aefd5eef35c3fe64882a2094a92214a974fd5804f2656861f9d02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf14d9efd6e0969b2a6f4ce16e7e2e47ac742a9d6b368dd70438e47e0748902`  
		Last Modified: Mon, 02 Dec 2024 20:38:15 GMT  
		Size: 53.0 MB (52995484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27dc85633c060e9e44a987a0c01fdb11e356c8687a7f3f9e9ff64aba2dbceb5`  
		Last Modified: Mon, 02 Dec 2024 20:38:20 GMT  
		Size: 237.6 MB (237588587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:3f475980df113266726615ba78fd4785b4571a54434bb7dc2dd65dbb276e44e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.8 KB (759798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f2ed814e83bb291354abbb56196747dc117e79d9aabab9fa38add98041005f`

```dockerfile
```

-	Layers:
	-	`sha256:c81bbdf1ea267ee371e25e7d9afcd5a265141af67890a79e494bd6dc3c727908`  
		Last Modified: Mon, 02 Dec 2024 20:38:13 GMT  
		Size: 749.0 KB (748965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f261ba6d1390fd6a70a6e72bd1cd40a9d924c207931d67ef020f9481b294128c`  
		Last Modified: Mon, 02 Dec 2024 20:38:13 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83.0-alpine3.20`

```console
$ docker pull rust@sha256:838d384a1138fe1f2e448e3901bb3d23683570ba3dca581160880ffad760332b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.83.0-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:88a66dc9c1ac1f281b82efafd2b33db603d1ce07f9e4e1bbbe9d3fceef0cdd72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290128622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e791fdca85c41d01da61496939bb1c3e40ef365c768e19e018ded15901356c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dcbc4b34b53bc9e532e413490c8f92a11e6a1682223532ea90597337ed5def`  
		Last Modified: Mon, 02 Dec 2024 20:24:27 GMT  
		Size: 55.3 MB (55309206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a818bb3055598f9d975638712fd88bcf5d9faea94cae98e3059ff8680f4a2cdb`  
		Last Modified: Mon, 02 Dec 2024 20:24:30 GMT  
		Size: 231.2 MB (231195512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1f4b461f3a7aa6a1d4fbbb717befabe3f146ebbf6ca6f427fe69ce8aebbc3425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eae7f8256cd37b35f89f9fc66faa1f8cd9fb813cbb64c747f44f461117e133`

```dockerfile
```

-	Layers:
	-	`sha256:07d675aac3f963b3a7bcc70c8f78fe4d629b3b9a64ff5d9ca285bf702237511a`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 710.5 KB (710491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a813425ea6f27d41933a1b5e80e290317aa6794a3ea8d7899cdc65dc38852d6d`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14d4e74fdaa1be40a40d60c28718b50f5600e05c496a982f9f499c04d80f9e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294622464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfa952d58e30aa2711dbeb8abcc4e70f27e5ed3ebe16e63c1c12b8642016ec2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61267d89978ab3ab775d217fd01b9f59b054d41cb3b70b13746a2a62eca5677f`  
		Last Modified: Mon, 02 Dec 2024 20:39:22 GMT  
		Size: 52.9 MB (52946253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f5c65e82878a882751b85d69f1b5e1fef9e5a1e2b6e8c6fb91b5a9106f0035`  
		Last Modified: Mon, 02 Dec 2024 20:39:25 GMT  
		Size: 237.6 MB (237588485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:83e6d986399402cf4f87ea920e42c14d1a2b3c9042fd6228a3c8591086bb011d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5040baee093c81f9e4600e14249874276bb6b1011b669a6c4d5962dac288d7`

```dockerfile
```

-	Layers:
	-	`sha256:0607df65216df8538ba3def2f4c315296c5b0fe079a14242b9b8819fc0879ad4`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 746.5 KB (746526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1a8c49a90f68976a179692f548c3e83293af8f8637778ff9a85839ff9df4b8`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83.0-bookworm`

```console
$ docker pull rust@sha256:d242a48452a5f6f490e1c13d3340d54ead1198948a4585dc42e326d6eacd07d1
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

### `rust:1.83.0-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:71aa4f8bdbfb924be55914e8910657aaf15420a87649ea1c64de6f3aef99b357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.7 MB (540737368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51381ded149a6148696b8fd088a50b9684925a0f5c26541db5d3a99db5aae059`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bc823accc52b76a805eb38c2d85f6916c18b62280e12ef86557cf7aae9f958b5`  
		Last Modified: Mon, 02 Dec 2024 20:24:37 GMT  
		Size: 191.4 MB (191418150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:6f2bd220e2f16cb7fe49a9b9ad87295829ed6ebf6b745b45163ccb5c6758e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2628cb17b709463f28662019efa1ac6f3499b61335860965970c347da12bc324`

```dockerfile
```

-	Layers:
	-	`sha256:286a3f2db2c8a6d92215bd0e79bef8cc02de285df8e4a1a45cf8e27b0ab0e625`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 15.5 MB (15500541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dea8927ea34a8749863f37f48d5c3386465f87be87fca83ebfb2da54e47f09`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:c4eab5718491261254547e9dee552013f246ffd187d3fe1c1427b2ca4b061ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526493619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b2f5c8fb2f32e205088f699538ac30a1f60f942ca99b46a7d63ee474294911`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:e64ed70b984c825bcf2c316778efdf694d1177f214c907b60097f528bbda5cf8`  
		Last Modified: Mon, 02 Dec 2024 20:29:54 GMT  
		Size: 224.5 MB (224498211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:be5458af59d7a9d4850ec727e792fe1ce39320e685eba63907c07a62c663a19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15317922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8513824646d633879f3b9c31a95e4313b646af70856500a177c618bb79ec94`

```dockerfile
```

-	Layers:
	-	`sha256:d5013ef9b8a7a070d15a1c43f9eb413d3814d5083868ad3477c7ca363e2629e8`  
		Last Modified: Mon, 02 Dec 2024 20:29:49 GMT  
		Size: 15.3 MB (15304676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a68401994195014fb21c06bdf19c124aea45e5bef8843f712d311bdfced543`  
		Last Modified: Mon, 02 Dec 2024 20:29:48 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f53e59e92e0aeabaf6660d225a107e99c545db88292aa0b26c622e74a040d965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 MB (592017331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c109228921d40f3351cd8c44731f364371c3d17735ca2a5e5f91c306a0dfbfa`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:73de18a65d13f2c8a09a8d948d31e3de3f45af2bead8f228a386915adb234c35`  
		Last Modified: Mon, 02 Dec 2024 20:35:51 GMT  
		Size: 251.8 MB (251804771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c509b7be5dcd87df97728f5298103aa353944b0f8c8f7d25b5b4b7d797017c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15542437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6766be12848456f1e52235b69ad6e4a319291879e57f2a2238bef89da8f3f9e`

```dockerfile
```

-	Layers:
	-	`sha256:98ab1278bc14cd425e7f3eed1e29aae39b73c5f89b91ccc51caee870f35910be`  
		Last Modified: Mon, 02 Dec 2024 20:35:45 GMT  
		Size: 15.5 MB (15529147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9709d89560fe98a5ae0be73fdda845fa48e30c80363bbca1ff69fdb179217095`  
		Last Modified: Mon, 02 Dec 2024 20:35:44 GMT  
		Size: 13.3 KB (13290 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-bookworm` - linux; 386

```console
$ docker pull rust@sha256:2b7d61e0cace1004b172c4c485053c11bc9a0f8bb92c9af92b22ff6d35ea5ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (556034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fe164933a80fc8c7abf32c417a466d96db3609b6f1ee14d861525cfdd78fea`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:336b9aae3521ef72851abe97810af76d93937f45be24b0cb67340ff9444cb707`  
		Last Modified: Mon, 02 Dec 2024 20:24:45 GMT  
		Size: 204.1 MB (204137618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2972bbfcb74add45006671eba779b040f9bf6bf4e3f7135555a34491df439bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b839cc63e7b08f07e283f08b415463fb2ab045791fdd19edf58fa0f210451796`

```dockerfile
```

-	Layers:
	-	`sha256:fd8c3f67164e288cb011c211b630adad3ad6454abdf247636e1be356b57369e7`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bde4a6f2185736694cd07ae59ade73bff87e8e8e38ea4758ae457fe22cf0bb7b`  
		Last Modified: Mon, 02 Dec 2024 20:24:39 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:1a3ec9464aaca3679e309b5a2d37d74b8ee5c1d49087f1580d6490b05dff4c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.7 MB (611728786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc406666b8bba58ebe80d82916ba809f85bc3d079aea65006a7189adc4fa98d`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bb1560f641778d2cb5455f2c6681cb70f74871be341fc94de016ad79eb2311af`  
		Last Modified: Mon, 02 Dec 2024 20:26:21 GMT  
		Size: 248.3 MB (248313252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4afd1f4300f64430965f43299137ca75249e7c27fbf74de6f92b8393fa33afa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab512b7df0c02174eb212c06d747326403186f429de36c0a0613f77795a9463`

```dockerfile
```

-	Layers:
	-	`sha256:1014165fb7c18bc7f0f45b139b7defb3fdaac4819329563e7b9abfd971721ca9`  
		Last Modified: Mon, 02 Dec 2024 20:26:15 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:971d6fde5f27e47969a782345543d65c64c4609aa41146345e4a00de2400f898`  
		Last Modified: Mon, 02 Dec 2024 20:26:14 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:6fc1e9e942c9ad8d4445769678468782e33f232441a2107277aa9309c8171531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.4 MB (593416662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb95fc496432694f3664ec33ed661538c8d318eddb1848edd90df4e723030f4`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:c731e424a0e50fe1d61cdc956a2238603eb68c82b94428b992cdd8b46e4494ca`  
		Last Modified: Mon, 02 Dec 2024 20:26:44 GMT  
		Size: 274.6 MB (274619819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a6f9b86026a3aa6e8f0f74e68331895240fe3be10c6d92205fb9e48ff2e3cc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d159b76c2f0dbfef842d8141ba3fb10cf86a429132d7f363f0b81aaf4d7cbd`

```dockerfile
```

-	Layers:
	-	`sha256:e33f6f4afffd15877fb13164def1212d1e66c7616414660e48f2ca508e1427c3`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 15.3 MB (15312980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158597ba495f8617e6dc77be65c0b5dcabe1b602984b6babf8551c0eba26c5d7`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83.0-bullseye`

```console
$ docker pull rust@sha256:48e32924c033e231995e5d604fc0bde746603529ab9c9525ed69551d1763722f
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

### `rust:1.83.0-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:3b69b1344468f45d6841e7d7eeddb646a6109c51ba6ad84867d40ce93bdb6507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.9 MB (513894985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1322104423ebd73df2358552ad57a4775ed183c222ff55d72233ce9c62b8e0c4`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:74d39ef915c9431d8814f436f6c5a05c033b7d061a908a761893aba712738dca`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 191.4 MB (191418226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:464848c0989553e6f5c696e1e8f488b2fd360b489a7c71bfc156c6c854921e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aed3439b87c35516bfcefed896ac0fbc064e92cdc1fc24c50cf3f4f82a470b8`

```dockerfile
```

-	Layers:
	-	`sha256:d5e8c58afb3cd8c33d2faf04883bb9f40a4d9ed6d20d0f401f4edc4b73f3f483`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 15.1 MB (15099560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7b47989b19887839396cc56566eed4407f3d0105f1bbb3dedb3ae59ecc329`  
		Last Modified: Mon, 02 Dec 2024 20:24:39 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:ef4925470bc527b51f98b8fd0e090015ba06289dce879ce02540c523a950492c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.6 MB (507587556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d219ef379dcd3a55ce17998421a285fdcae9d0e18e6dc6719f234d8ba6fdba2`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:460e72c81a8faf8a12fa4517b675bc73c5173407737e669feb3c5c0de5acdf15`  
		Last Modified: Mon, 02 Dec 2024 20:33:45 GMT  
		Size: 224.5 MB (224498199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8ffb613d6c04af1f4a4c9dad7c9046e06244f7a51eafe51ef0239aa93e16887b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5692a48de82943f6da6098bdb2f952d25c38b546e4aad806bba8904ea5c1086f`

```dockerfile
```

-	Layers:
	-	`sha256:0c4c1556ccde855c9606ac4814d71b557174cf8f2b9521f60c9cea5219852703`  
		Last Modified: Mon, 02 Dec 2024 20:33:40 GMT  
		Size: 14.9 MB (14900067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea7e331de6703885f45617be049222c6f6d6474c6b8b1e74d1493ea5482878c9`  
		Last Modified: Mon, 02 Dec 2024 20:33:39 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b92b53e23598b9accd960a82d00386d9c100495c88f77a4aac5b6983bfd24697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.9 MB (565925019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0b729695c79cc2b5ab22d9798c6a3c74ab86f10b3c7e147e82236a28cdac7`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:2d9513256f7bf83972d3d8a5644bef3b31913ac18f945e7bda5e1b67800b99ff`  
		Last Modified: Mon, 02 Dec 2024 20:32:52 GMT  
		Size: 251.8 MB (251804822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1c90a3d5572cdeb856d417ebbc90b19c0c4ad64b5ac8849d506106dea513ae57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15113175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53bdc544237eb3432d49c4682f0fe3627f7d36735a5cb1865033529582e0fe6`

```dockerfile
```

-	Layers:
	-	`sha256:58f3bb41e62e5e98de42e3be870f748aec12d2a62f8576bac1c8869337ee9e15`  
		Last Modified: Mon, 02 Dec 2024 20:32:47 GMT  
		Size: 15.1 MB (15101822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9d1ceb3d92c5f213ec0ca376ec575dd98f09f32d6d5430b2555d6c0b7562d1`  
		Last Modified: Mon, 02 Dec 2024 20:32:46 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-bullseye` - linux; 386

```console
$ docker pull rust@sha256:a534b238c9b99b740f1216486f77bf3c14cea88e3a9e1bbf070d86fbab5bb0fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.3 MB (532304484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18675ba81d558cf8f9ec3d367d8c3ec104bff1aab30160b88e8bc51d23329c49`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:8c0d713557008a8d69677c0aa162eedcab0ac7846ed90aee9c2d5788a51fad0f`  
		Last Modified: Mon, 02 Dec 2024 20:24:51 GMT  
		Size: 204.1 MB (204137636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:74c74e7676b304b2cb4c939116791d252bdd51e0bf9e358dcb40dad59a622617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15097814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c3da0659cf7eddc4df08832981dc114a0434eff8cff0f7e0a5318dcda2ea8d`

```dockerfile
```

-	Layers:
	-	`sha256:e179a67825d943f6221f1e2e7a9c60df8de969054fec98b3538bbf4a5682769b`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 15.1 MB (15086597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6b6fde063e7e47ab87f2ab98387725a5cbba86c1ba5665ba2280757cd267dd0`  
		Last Modified: Mon, 02 Dec 2024 20:24:46 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83.0-slim`

```console
$ docker pull rust@sha256:2808c258e14c25a1277d7ba6e653093ef00ba088dc73d99402a900e8cc218d5c
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

### `rust:1.83.0-slim` - linux; amd64

```console
$ docker pull rust@sha256:6a3be2a97d72a2d401807e494ff0b2d500bb241293db2f8d84e16b629f952366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291337423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae1dcbb4bdaada87c1f2a5397fb3e2534cd10a921d8b38ab8e032613d4bec82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbfe6cc0ca59f7757297ccc9049930ac7f37bccab06b5fb02b80eb1d37e4a48`  
		Last Modified: Mon, 02 Dec 2024 20:24:38 GMT  
		Size: 262.2 MB (262209428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:1a1e9a3dd7b8efd48e40f7a424dd24b8ba15de70d687a06656717edbb9048faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1ba3680f55e2998a08ff5c873a90a1249c120eba4a76d95874c78c7e755812`

```dockerfile
```

-	Layers:
	-	`sha256:190def7ed7dafd6d8ee1ba46e117570e708371dde8e290f4c757acd3f543a0da`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 4.0 MB (3960916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3749ab658f8ad4f8d17c77b275dd953cfdf9c2de24728be40fda41f514178b`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:6d7afc9f25f7a5cefc9b6f3fbf2304e89502533bf562b3d008f1d7e98e849723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297059662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302b6a008c606c7cd8b9263e55bcb04488d3fe948c1a45f2f7a6b2e9f6c11f23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defe357fcbe93d1e65d0570d021785ad676696d2d624262bdb0e214723689b36`  
		Last Modified: Mon, 02 Dec 2024 20:31:38 GMT  
		Size: 272.3 MB (272340753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3f2058fe6f54a997932102d8b6bc235e8d4666e331b9296243cf75c70990da78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7fc6c7b289d0a098a407027d015ead0708a0e04655389eae49e4155b848f52`

```dockerfile
```

-	Layers:
	-	`sha256:8928a87a6013ae9d938cea84efc86dfc5fb240cf83f931e727c7693adaa6da2c`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 3.8 MB (3776732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea6b01b234f1e08ebc59a4a02bda774ffe04cf102809435a132937896e535eaf`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:594e5e30e34cb3f1edfcf62b6c42ab7418bfbe4fd83057099fede39488edc7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.8 MB (346802313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3d008bad10df60f61201660a99f5d86423c1a1a546c0a1a1838123d75a27a1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0237173b80106fe0760a817d7e6d1c71f9e5e284c512b7d06074708c59aff7`  
		Last Modified: Mon, 02 Dec 2024 20:37:13 GMT  
		Size: 317.6 MB (317644957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:895f4818b23e10a7e1f1880f5e42eb988a221a3a0eb6f39134e09fa24dcf11ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e2f37d04cfed0d9e84101878c4064b4b8353ce7996f5587a68e63f1e717bd8`

```dockerfile
```

-	Layers:
	-	`sha256:05e0e8f9842371d47373dc72339abb01c46ebf232229e4810af7074cc8f68115`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 4.0 MB (3983284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b63a1b31beb1e3b516d716bd7530b21f5698318b664ff2c0808a3a6738dbc2`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-slim` - linux; 386

```console
$ docker pull rust@sha256:e3a12bd5e08f7ffd7c014c2820aa4bbb647a30f3617f59659136669d0765cde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301886447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3c3937265088583d6ea42714a975738f2bf863ef26ec51c0eceafa294d88e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ceb72ece1ea1e0fe9569779176af4568889e4706901654739657a99aa4700`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 271.7 MB (271740997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:ea30beb0ac18971c71310961164ae02c93873a3dee5e71820cb92ca5af9cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad0f3a1a05782cc497e5841bd1cba942630e16eb84acaf9a3809618df1ee6d`

```dockerfile
```

-	Layers:
	-	`sha256:bf795665c0773ee9ebba9af59adaf88084fc89e625ffd096983779a3322b9d98`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea300ff11941e5c8c9dca6dae2eaeb1b7aa9ff4ffacb336422e939217214bca`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:901e8fd72a554e505e9273538a8ad34c2bf33a02f62b634250d35e34bb2ded90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.2 MB (350198087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c2aef4eee77ed0f0829ba276a911bf8cd57b8afb28b00184b775c489a82bb4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a607df9bd35302bace9a6ad9223bd9a4b868b9c462a42e5cca65d5fd3d8a9b`  
		Last Modified: Mon, 02 Dec 2024 20:29:03 GMT  
		Size: 317.1 MB (317072734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:12a9974e9bd55d24e84c10e72f5170591f010651e62da1a001cce00b60a8b5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f48e8cf17275373c2886d5d424e13f54217678435465c09519f9d27932b9a4`

```dockerfile
```

-	Layers:
	-	`sha256:1969029d7112da6fdd40a3a936b1152b38032abb4d7bd1bc31411ed5fd021715`  
		Last Modified: Mon, 02 Dec 2024 20:28:53 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52df272aeab4c0542aa89ec9e6638cabd6465bf962ee7053c5eac2b05e53b44d`  
		Last Modified: Mon, 02 Dec 2024 20:28:52 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-slim` - linux; s390x

```console
$ docker pull rust@sha256:59e72321724e973f7b278fe9cfdbc7916988c33529e4f16eaa3be7e72b4d7b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352217458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c145addc8a9384eb579adb69c9d9500d0a57a3690e0e396cdce0b24098684ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e04d7c8b55a5ef929486fce3eca63d3be7958f04b601f4f73a52e9591e4a16`  
		Last Modified: Mon, 02 Dec 2024 20:28:50 GMT  
		Size: 324.7 MB (324725830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:34d0adfbc6046e33a5307df483d7f0626cfbedc28bc7cb0fa092b40008a9d30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3815877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4d233def5b8a5cbdca87e1d70f4c0e5602f12e771f4e9c36399233edb2ef42`

```dockerfile
```

-	Layers:
	-	`sha256:a2bb7709243f1094bc9ed02cbe32492f025e7ba1b46404d9f64f3527d774ce68`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 3.8 MB (3802606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60ee2d606d582a3328f010baeb9968ac6e723667c4dac109be44717dae4d543`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83.0-slim-bookworm`

```console
$ docker pull rust@sha256:2808c258e14c25a1277d7ba6e653093ef00ba088dc73d99402a900e8cc218d5c
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

### `rust:1.83.0-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:6a3be2a97d72a2d401807e494ff0b2d500bb241293db2f8d84e16b629f952366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291337423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae1dcbb4bdaada87c1f2a5397fb3e2534cd10a921d8b38ab8e032613d4bec82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbfe6cc0ca59f7757297ccc9049930ac7f37bccab06b5fb02b80eb1d37e4a48`  
		Last Modified: Mon, 02 Dec 2024 20:24:38 GMT  
		Size: 262.2 MB (262209428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1a1e9a3dd7b8efd48e40f7a424dd24b8ba15de70d687a06656717edbb9048faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1ba3680f55e2998a08ff5c873a90a1249c120eba4a76d95874c78c7e755812`

```dockerfile
```

-	Layers:
	-	`sha256:190def7ed7dafd6d8ee1ba46e117570e708371dde8e290f4c757acd3f543a0da`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 4.0 MB (3960916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3749ab658f8ad4f8d17c77b275dd953cfdf9c2de24728be40fda41f514178b`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:6d7afc9f25f7a5cefc9b6f3fbf2304e89502533bf562b3d008f1d7e98e849723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297059662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302b6a008c606c7cd8b9263e55bcb04488d3fe948c1a45f2f7a6b2e9f6c11f23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defe357fcbe93d1e65d0570d021785ad676696d2d624262bdb0e214723689b36`  
		Last Modified: Mon, 02 Dec 2024 20:31:38 GMT  
		Size: 272.3 MB (272340753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3f2058fe6f54a997932102d8b6bc235e8d4666e331b9296243cf75c70990da78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7fc6c7b289d0a098a407027d015ead0708a0e04655389eae49e4155b848f52`

```dockerfile
```

-	Layers:
	-	`sha256:8928a87a6013ae9d938cea84efc86dfc5fb240cf83f931e727c7693adaa6da2c`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 3.8 MB (3776732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea6b01b234f1e08ebc59a4a02bda774ffe04cf102809435a132937896e535eaf`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:594e5e30e34cb3f1edfcf62b6c42ab7418bfbe4fd83057099fede39488edc7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.8 MB (346802313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3d008bad10df60f61201660a99f5d86423c1a1a546c0a1a1838123d75a27a1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0237173b80106fe0760a817d7e6d1c71f9e5e284c512b7d06074708c59aff7`  
		Last Modified: Mon, 02 Dec 2024 20:37:13 GMT  
		Size: 317.6 MB (317644957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:895f4818b23e10a7e1f1880f5e42eb988a221a3a0eb6f39134e09fa24dcf11ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e2f37d04cfed0d9e84101878c4064b4b8353ce7996f5587a68e63f1e717bd8`

```dockerfile
```

-	Layers:
	-	`sha256:05e0e8f9842371d47373dc72339abb01c46ebf232229e4810af7074cc8f68115`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 4.0 MB (3983284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b63a1b31beb1e3b516d716bd7530b21f5698318b664ff2c0808a3a6738dbc2`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:e3a12bd5e08f7ffd7c014c2820aa4bbb647a30f3617f59659136669d0765cde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301886447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3c3937265088583d6ea42714a975738f2bf863ef26ec51c0eceafa294d88e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ceb72ece1ea1e0fe9569779176af4568889e4706901654739657a99aa4700`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 271.7 MB (271740997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ea30beb0ac18971c71310961164ae02c93873a3dee5e71820cb92ca5af9cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad0f3a1a05782cc497e5841bd1cba942630e16eb84acaf9a3809618df1ee6d`

```dockerfile
```

-	Layers:
	-	`sha256:bf795665c0773ee9ebba9af59adaf88084fc89e625ffd096983779a3322b9d98`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea300ff11941e5c8c9dca6dae2eaeb1b7aa9ff4ffacb336422e939217214bca`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:901e8fd72a554e505e9273538a8ad34c2bf33a02f62b634250d35e34bb2ded90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.2 MB (350198087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c2aef4eee77ed0f0829ba276a911bf8cd57b8afb28b00184b775c489a82bb4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a607df9bd35302bace9a6ad9223bd9a4b868b9c462a42e5cca65d5fd3d8a9b`  
		Last Modified: Mon, 02 Dec 2024 20:29:03 GMT  
		Size: 317.1 MB (317072734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:12a9974e9bd55d24e84c10e72f5170591f010651e62da1a001cce00b60a8b5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f48e8cf17275373c2886d5d424e13f54217678435465c09519f9d27932b9a4`

```dockerfile
```

-	Layers:
	-	`sha256:1969029d7112da6fdd40a3a936b1152b38032abb4d7bd1bc31411ed5fd021715`  
		Last Modified: Mon, 02 Dec 2024 20:28:53 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52df272aeab4c0542aa89ec9e6638cabd6465bf962ee7053c5eac2b05e53b44d`  
		Last Modified: Mon, 02 Dec 2024 20:28:52 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:59e72321724e973f7b278fe9cfdbc7916988c33529e4f16eaa3be7e72b4d7b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352217458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c145addc8a9384eb579adb69c9d9500d0a57a3690e0e396cdce0b24098684ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e04d7c8b55a5ef929486fce3eca63d3be7958f04b601f4f73a52e9591e4a16`  
		Last Modified: Mon, 02 Dec 2024 20:28:50 GMT  
		Size: 324.7 MB (324725830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:34d0adfbc6046e33a5307df483d7f0626cfbedc28bc7cb0fa092b40008a9d30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3815877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4d233def5b8a5cbdca87e1d70f4c0e5602f12e771f4e9c36399233edb2ef42`

```dockerfile
```

-	Layers:
	-	`sha256:a2bb7709243f1094bc9ed02cbe32492f025e7ba1b46404d9f64f3527d774ce68`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 3.8 MB (3802606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60ee2d606d582a3328f010baeb9968ac6e723667c4dac109be44717dae4d543`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.83.0-slim-bullseye`

```console
$ docker pull rust@sha256:cd64d55bf5d90faca3b5e69039e03cc8eaf4d0c531537cb08d20ee8ee87f438f
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

### `rust:1.83.0-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:693226f9da3b618f747e1d45901d1d6c27e591f5d3d17c92685a55f4983911ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.8 MB (282812182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecfd0a5420dc73cd925c46f1879d9c00df802531eccda112b2d406071cacca0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384329ccf6be51bb1ef6f2b07175dcdcebcf898a37bba183bfe10f903be995ce`  
		Last Modified: Mon, 02 Dec 2024 20:24:22 GMT  
		Size: 251.4 MB (251360621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ebc287a15a3e3cd43102b0e5b3df9aae5ae0a8cd284c6cd6845bc32e9e0b5903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4191040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8375006c14246df12ba094238c9468666ade0d799bb9d20f012e4f299847e56a`

```dockerfile
```

-	Layers:
	-	`sha256:74af93f126d4c06de89836c2cf05cebb553960e94e4ab55a74d46b28183ad983`  
		Last Modified: Mon, 02 Dec 2024 20:24:19 GMT  
		Size: 4.2 MB (4179684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c366dfc129927914c32fbdf3b3a7128249ed30666f407a63a7ff0f19be5aff8`  
		Last Modified: Mon, 02 Dec 2024 20:24:18 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:abf606a99416890d34310c1ed7c2dc863aa6a1ce4f8ab588c768b2511ffdaa5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.2 MB (293172521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4ff907c925646494aeeb07f6a9c015b9f209c836a858b44c751fffc645ed1b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fffe59376f64ffa8f62067ec6c177458ad560736ecb62f5a746b99a1213febb`  
		Last Modified: Mon, 02 Dec 2024 20:27:46 GMT  
		Size: 266.6 MB (266563264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6ec69ccb3c2df674b652af2bf87b9af3d1c186c907bacf211557fca6a0605d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d2e1fea37fd47ebcb90737269a9a15f43d09ff6e3a8ac409221ed3d6a3b8d3`

```dockerfile
```

-	Layers:
	-	`sha256:b11be9c55ffbd97983468ba6c80f6bfb1b6d2f881f28c132a972181a2f323cf1`  
		Last Modified: Mon, 02 Dec 2024 20:27:40 GMT  
		Size: 4.0 MB (3988606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9172172b88ef1546ba7e0d5edb4641fbb14bdf07ff13f0bb89ccbb6102cb8a32`  
		Last Modified: Mon, 02 Dec 2024 20:27:40 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a32ae5ae9cad532df229a1fef4ada9991409591a7ccf15c3856ba3ca21d7c26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.4 MB (337389995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504b549e7eafa02320debcac41241b24c3e628c6a7f2c4a085a0e8430d5fa44f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b17b8db729381225a8d73b8af06a440c8b3f44ba100df98709bb0b03c0a016`  
		Last Modified: Mon, 02 Dec 2024 20:34:10 GMT  
		Size: 307.3 MB (307298395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3b6d85ff4952c3db80e6f66474078bd4e09bc1b884e7978509e0cf8a7c4410ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4187819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2535b26d94240ff8a8243d5fcaf6cd4f3238cc6575f145c7055f3be7a7af6e18`

```dockerfile
```

-	Layers:
	-	`sha256:280d6fd398dd958493aa5d431829910d0726c625baf5513aa3477e64de936e0d`  
		Last Modified: Mon, 02 Dec 2024 20:34:04 GMT  
		Size: 4.2 MB (4176359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb393af559bdc07a24e80a9442f17ed5976eafc6cced8e26e7df0a3132f88ce7`  
		Last Modified: Mon, 02 Dec 2024 20:34:04 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.83.0-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:d5af146980a072b682d3ac22609ffed95252933df15d14690667925cf35a83bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297129117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182df1c816edafaeadc3362a748a39f671aa57bf19f6d7fafd20bcb2a4becdd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a29bf3a9090d3e58d845509836c32130197f51dc0eafb75e2102450607aa614`  
		Last Modified: Mon, 02 Dec 2024 20:24:48 GMT  
		Size: 264.7 MB (264705766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.83.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:de112da84d3f18bbad7559779bde4d938157704801863564aaae2a20e856f0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaa8827be2c8dbe784a39a4b999bb4842aa2514d900dbd211b897aabc55f32b`

```dockerfile
```

-	Layers:
	-	`sha256:1e6ab84278603cf43cd88053eb59875eea8a1a59d9a120bb129fdeff7482806d`  
		Last Modified: Mon, 02 Dec 2024 20:24:41 GMT  
		Size: 4.2 MB (4169952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67bd2e3b5300c4b614ff1c265cf9f027c92cb2fd18db1cac9fc58fb89c69ea17`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:838d384a1138fe1f2e448e3901bb3d23683570ba3dca581160880ffad760332b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:88a66dc9c1ac1f281b82efafd2b33db603d1ce07f9e4e1bbbe9d3fceef0cdd72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290128622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e791fdca85c41d01da61496939bb1c3e40ef365c768e19e018ded15901356c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dcbc4b34b53bc9e532e413490c8f92a11e6a1682223532ea90597337ed5def`  
		Last Modified: Mon, 02 Dec 2024 20:24:27 GMT  
		Size: 55.3 MB (55309206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a818bb3055598f9d975638712fd88bcf5d9faea94cae98e3059ff8680f4a2cdb`  
		Last Modified: Mon, 02 Dec 2024 20:24:30 GMT  
		Size: 231.2 MB (231195512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:1f4b461f3a7aa6a1d4fbbb717befabe3f146ebbf6ca6f427fe69ce8aebbc3425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eae7f8256cd37b35f89f9fc66faa1f8cd9fb813cbb64c747f44f461117e133`

```dockerfile
```

-	Layers:
	-	`sha256:07d675aac3f963b3a7bcc70c8f78fe4d629b3b9a64ff5d9ca285bf702237511a`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 710.5 KB (710491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a813425ea6f27d41933a1b5e80e290317aa6794a3ea8d7899cdc65dc38852d6d`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14d4e74fdaa1be40a40d60c28718b50f5600e05c496a982f9f499c04d80f9e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294622464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfa952d58e30aa2711dbeb8abcc4e70f27e5ed3ebe16e63c1c12b8642016ec2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61267d89978ab3ab775d217fd01b9f59b054d41cb3b70b13746a2a62eca5677f`  
		Last Modified: Mon, 02 Dec 2024 20:39:22 GMT  
		Size: 52.9 MB (52946253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f5c65e82878a882751b85d69f1b5e1fef9e5a1e2b6e8c6fb91b5a9106f0035`  
		Last Modified: Mon, 02 Dec 2024 20:39:25 GMT  
		Size: 237.6 MB (237588485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:83e6d986399402cf4f87ea920e42c14d1a2b3c9042fd6228a3c8591086bb011d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5040baee093c81f9e4600e14249874276bb6b1011b669a6c4d5962dac288d7`

```dockerfile
```

-	Layers:
	-	`sha256:0607df65216df8538ba3def2f4c315296c5b0fe079a14242b9b8819fc0879ad4`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 746.5 KB (746526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1a8c49a90f68976a179692f548c3e83293af8f8637778ff9a85839ff9df4b8`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.19`

```console
$ docker pull rust@sha256:c22e43db16b649a713eb39606c5054dd072eed35a7acffe05e295749c8a7eed3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:51158a1b5d1531f739f78b9ececd3c074e75bf5cc18b4c7b63b1a891c4216740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (289961960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47c29028d898cefa39de15d160ad8cc6cdb1d1dacf206c360c4b4d7d045eb10`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88faabca0966b648ec58d261009681663f60798257994a9281be6f9b359864d0`  
		Last Modified: Mon, 02 Dec 2024 20:24:21 GMT  
		Size: 55.3 MB (55346817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6927d0b73da7baf8ea757697b138a23dc5a1196a24f50ae7a26794aba2b17cd`  
		Last Modified: Mon, 02 Dec 2024 20:24:23 GMT  
		Size: 231.2 MB (231195415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:62a85d1b9963d7c5b3276c4f04bd4d2a32be81c6551a6a6cdb5cf11dd077d933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.7 KB (723693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232ac0ffe4a86028aaba1f2e862002fdd2b4ff1731bb1c90c21401078f6dbd42`

```dockerfile
```

-	Layers:
	-	`sha256:05cdb77f193f20e943f1f0d26b0bb06e83851c90af78776aa9399c35f9aa807b`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 713.0 KB (712979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6cf2aab24ba344de6369df5fa858a9401710c70dc1af99a87e867c019cfd3c4`  
		Last Modified: Mon, 02 Dec 2024 20:24:20 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b0c30be9019c61d2b4530ec4a206cbf74cf620f9e664db3e2397e50a5dfac14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293943317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170301d6a34aefd5eef35c3fe64882a2094a92214a974fd5804f2656861f9d02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf14d9efd6e0969b2a6f4ce16e7e2e47ac742a9d6b368dd70438e47e0748902`  
		Last Modified: Mon, 02 Dec 2024 20:38:15 GMT  
		Size: 53.0 MB (52995484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27dc85633c060e9e44a987a0c01fdb11e356c8687a7f3f9e9ff64aba2dbceb5`  
		Last Modified: Mon, 02 Dec 2024 20:38:20 GMT  
		Size: 237.6 MB (237588587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:3f475980df113266726615ba78fd4785b4571a54434bb7dc2dd65dbb276e44e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.8 KB (759798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f2ed814e83bb291354abbb56196747dc117e79d9aabab9fa38add98041005f`

```dockerfile
```

-	Layers:
	-	`sha256:c81bbdf1ea267ee371e25e7d9afcd5a265141af67890a79e494bd6dc3c727908`  
		Last Modified: Mon, 02 Dec 2024 20:38:13 GMT  
		Size: 749.0 KB (748965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f261ba6d1390fd6a70a6e72bd1cd40a9d924c207931d67ef020f9481b294128c`  
		Last Modified: Mon, 02 Dec 2024 20:38:13 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.20`

```console
$ docker pull rust@sha256:838d384a1138fe1f2e448e3901bb3d23683570ba3dca581160880ffad760332b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:88a66dc9c1ac1f281b82efafd2b33db603d1ce07f9e4e1bbbe9d3fceef0cdd72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290128622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e791fdca85c41d01da61496939bb1c3e40ef365c768e19e018ded15901356c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dcbc4b34b53bc9e532e413490c8f92a11e6a1682223532ea90597337ed5def`  
		Last Modified: Mon, 02 Dec 2024 20:24:27 GMT  
		Size: 55.3 MB (55309206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a818bb3055598f9d975638712fd88bcf5d9faea94cae98e3059ff8680f4a2cdb`  
		Last Modified: Mon, 02 Dec 2024 20:24:30 GMT  
		Size: 231.2 MB (231195512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1f4b461f3a7aa6a1d4fbbb717befabe3f146ebbf6ca6f427fe69ce8aebbc3425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99eae7f8256cd37b35f89f9fc66faa1f8cd9fb813cbb64c747f44f461117e133`

```dockerfile
```

-	Layers:
	-	`sha256:07d675aac3f963b3a7bcc70c8f78fe4d629b3b9a64ff5d9ca285bf702237511a`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 710.5 KB (710491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a813425ea6f27d41933a1b5e80e290317aa6794a3ea8d7899cdc65dc38852d6d`  
		Last Modified: Mon, 02 Dec 2024 20:24:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14d4e74fdaa1be40a40d60c28718b50f5600e05c496a982f9f499c04d80f9e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294622464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfa952d58e30aa2711dbeb8abcc4e70f27e5ed3ebe16e63c1c12b8642016ec2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61267d89978ab3ab775d217fd01b9f59b054d41cb3b70b13746a2a62eca5677f`  
		Last Modified: Mon, 02 Dec 2024 20:39:22 GMT  
		Size: 52.9 MB (52946253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f5c65e82878a882751b85d69f1b5e1fef9e5a1e2b6e8c6fb91b5a9106f0035`  
		Last Modified: Mon, 02 Dec 2024 20:39:25 GMT  
		Size: 237.6 MB (237588485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:83e6d986399402cf4f87ea920e42c14d1a2b3c9042fd6228a3c8591086bb011d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5040baee093c81f9e4600e14249874276bb6b1011b669a6c4d5962dac288d7`

```dockerfile
```

-	Layers:
	-	`sha256:0607df65216df8538ba3def2f4c315296c5b0fe079a14242b9b8819fc0879ad4`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 746.5 KB (746526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1a8c49a90f68976a179692f548c3e83293af8f8637778ff9a85839ff9df4b8`  
		Last Modified: Mon, 02 Dec 2024 20:39:20 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:d242a48452a5f6f490e1c13d3340d54ead1198948a4585dc42e326d6eacd07d1
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
$ docker pull rust@sha256:71aa4f8bdbfb924be55914e8910657aaf15420a87649ea1c64de6f3aef99b357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.7 MB (540737368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51381ded149a6148696b8fd088a50b9684925a0f5c26541db5d3a99db5aae059`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bc823accc52b76a805eb38c2d85f6916c18b62280e12ef86557cf7aae9f958b5`  
		Last Modified: Mon, 02 Dec 2024 20:24:37 GMT  
		Size: 191.4 MB (191418150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:6f2bd220e2f16cb7fe49a9b9ad87295829ed6ebf6b745b45163ccb5c6758e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2628cb17b709463f28662019efa1ac6f3499b61335860965970c347da12bc324`

```dockerfile
```

-	Layers:
	-	`sha256:286a3f2db2c8a6d92215bd0e79bef8cc02de285df8e4a1a45cf8e27b0ab0e625`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 15.5 MB (15500541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dea8927ea34a8749863f37f48d5c3386465f87be87fca83ebfb2da54e47f09`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:c4eab5718491261254547e9dee552013f246ffd187d3fe1c1427b2ca4b061ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526493619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b2f5c8fb2f32e205088f699538ac30a1f60f942ca99b46a7d63ee474294911`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:e64ed70b984c825bcf2c316778efdf694d1177f214c907b60097f528bbda5cf8`  
		Last Modified: Mon, 02 Dec 2024 20:29:54 GMT  
		Size: 224.5 MB (224498211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:be5458af59d7a9d4850ec727e792fe1ce39320e685eba63907c07a62c663a19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15317922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8513824646d633879f3b9c31a95e4313b646af70856500a177c618bb79ec94`

```dockerfile
```

-	Layers:
	-	`sha256:d5013ef9b8a7a070d15a1c43f9eb413d3814d5083868ad3477c7ca363e2629e8`  
		Last Modified: Mon, 02 Dec 2024 20:29:49 GMT  
		Size: 15.3 MB (15304676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a68401994195014fb21c06bdf19c124aea45e5bef8843f712d311bdfced543`  
		Last Modified: Mon, 02 Dec 2024 20:29:48 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f53e59e92e0aeabaf6660d225a107e99c545db88292aa0b26c622e74a040d965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 MB (592017331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c109228921d40f3351cd8c44731f364371c3d17735ca2a5e5f91c306a0dfbfa`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:73de18a65d13f2c8a09a8d948d31e3de3f45af2bead8f228a386915adb234c35`  
		Last Modified: Mon, 02 Dec 2024 20:35:51 GMT  
		Size: 251.8 MB (251804771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c509b7be5dcd87df97728f5298103aa353944b0f8c8f7d25b5b4b7d797017c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15542437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6766be12848456f1e52235b69ad6e4a319291879e57f2a2238bef89da8f3f9e`

```dockerfile
```

-	Layers:
	-	`sha256:98ab1278bc14cd425e7f3eed1e29aae39b73c5f89b91ccc51caee870f35910be`  
		Last Modified: Mon, 02 Dec 2024 20:35:45 GMT  
		Size: 15.5 MB (15529147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9709d89560fe98a5ae0be73fdda845fa48e30c80363bbca1ff69fdb179217095`  
		Last Modified: Mon, 02 Dec 2024 20:35:44 GMT  
		Size: 13.3 KB (13290 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:2b7d61e0cace1004b172c4c485053c11bc9a0f8bb92c9af92b22ff6d35ea5ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (556034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fe164933a80fc8c7abf32c417a466d96db3609b6f1ee14d861525cfdd78fea`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:336b9aae3521ef72851abe97810af76d93937f45be24b0cb67340ff9444cb707`  
		Last Modified: Mon, 02 Dec 2024 20:24:45 GMT  
		Size: 204.1 MB (204137618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2972bbfcb74add45006671eba779b040f9bf6bf4e3f7135555a34491df439bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b839cc63e7b08f07e283f08b415463fb2ab045791fdd19edf58fa0f210451796`

```dockerfile
```

-	Layers:
	-	`sha256:fd8c3f67164e288cb011c211b630adad3ad6454abdf247636e1be356b57369e7`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bde4a6f2185736694cd07ae59ade73bff87e8e8e38ea4758ae457fe22cf0bb7b`  
		Last Modified: Mon, 02 Dec 2024 20:24:39 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:1a3ec9464aaca3679e309b5a2d37d74b8ee5c1d49087f1580d6490b05dff4c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.7 MB (611728786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc406666b8bba58ebe80d82916ba809f85bc3d079aea65006a7189adc4fa98d`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bb1560f641778d2cb5455f2c6681cb70f74871be341fc94de016ad79eb2311af`  
		Last Modified: Mon, 02 Dec 2024 20:26:21 GMT  
		Size: 248.3 MB (248313252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4afd1f4300f64430965f43299137ca75249e7c27fbf74de6f92b8393fa33afa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab512b7df0c02174eb212c06d747326403186f429de36c0a0613f77795a9463`

```dockerfile
```

-	Layers:
	-	`sha256:1014165fb7c18bc7f0f45b139b7defb3fdaac4819329563e7b9abfd971721ca9`  
		Last Modified: Mon, 02 Dec 2024 20:26:15 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:971d6fde5f27e47969a782345543d65c64c4609aa41146345e4a00de2400f898`  
		Last Modified: Mon, 02 Dec 2024 20:26:14 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:6fc1e9e942c9ad8d4445769678468782e33f232441a2107277aa9309c8171531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.4 MB (593416662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb95fc496432694f3664ec33ed661538c8d318eddb1848edd90df4e723030f4`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:c731e424a0e50fe1d61cdc956a2238603eb68c82b94428b992cdd8b46e4494ca`  
		Last Modified: Mon, 02 Dec 2024 20:26:44 GMT  
		Size: 274.6 MB (274619819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a6f9b86026a3aa6e8f0f74e68331895240fe3be10c6d92205fb9e48ff2e3cc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d159b76c2f0dbfef842d8141ba3fb10cf86a429132d7f363f0b81aaf4d7cbd`

```dockerfile
```

-	Layers:
	-	`sha256:e33f6f4afffd15877fb13164def1212d1e66c7616414660e48f2ca508e1427c3`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 15.3 MB (15312980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158597ba495f8617e6dc77be65c0b5dcabe1b602984b6babf8551c0eba26c5d7`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:48e32924c033e231995e5d604fc0bde746603529ab9c9525ed69551d1763722f
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
$ docker pull rust@sha256:3b69b1344468f45d6841e7d7eeddb646a6109c51ba6ad84867d40ce93bdb6507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.9 MB (513894985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1322104423ebd73df2358552ad57a4775ed183c222ff55d72233ce9c62b8e0c4`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:74d39ef915c9431d8814f436f6c5a05c033b7d061a908a761893aba712738dca`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 191.4 MB (191418226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:464848c0989553e6f5c696e1e8f488b2fd360b489a7c71bfc156c6c854921e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aed3439b87c35516bfcefed896ac0fbc064e92cdc1fc24c50cf3f4f82a470b8`

```dockerfile
```

-	Layers:
	-	`sha256:d5e8c58afb3cd8c33d2faf04883bb9f40a4d9ed6d20d0f401f4edc4b73f3f483`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 15.1 MB (15099560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7b47989b19887839396cc56566eed4407f3d0105f1bbb3dedb3ae59ecc329`  
		Last Modified: Mon, 02 Dec 2024 20:24:39 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:ef4925470bc527b51f98b8fd0e090015ba06289dce879ce02540c523a950492c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.6 MB (507587556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d219ef379dcd3a55ce17998421a285fdcae9d0e18e6dc6719f234d8ba6fdba2`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:460e72c81a8faf8a12fa4517b675bc73c5173407737e669feb3c5c0de5acdf15`  
		Last Modified: Mon, 02 Dec 2024 20:33:45 GMT  
		Size: 224.5 MB (224498199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8ffb613d6c04af1f4a4c9dad7c9046e06244f7a51eafe51ef0239aa93e16887b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5692a48de82943f6da6098bdb2f952d25c38b546e4aad806bba8904ea5c1086f`

```dockerfile
```

-	Layers:
	-	`sha256:0c4c1556ccde855c9606ac4814d71b557174cf8f2b9521f60c9cea5219852703`  
		Last Modified: Mon, 02 Dec 2024 20:33:40 GMT  
		Size: 14.9 MB (14900067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea7e331de6703885f45617be049222c6f6d6474c6b8b1e74d1493ea5482878c9`  
		Last Modified: Mon, 02 Dec 2024 20:33:39 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b92b53e23598b9accd960a82d00386d9c100495c88f77a4aac5b6983bfd24697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.9 MB (565925019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b0b729695c79cc2b5ab22d9798c6a3c74ab86f10b3c7e147e82236a28cdac7`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:2d9513256f7bf83972d3d8a5644bef3b31913ac18f945e7bda5e1b67800b99ff`  
		Last Modified: Mon, 02 Dec 2024 20:32:52 GMT  
		Size: 251.8 MB (251804822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1c90a3d5572cdeb856d417ebbc90b19c0c4ad64b5ac8849d506106dea513ae57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15113175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53bdc544237eb3432d49c4682f0fe3627f7d36735a5cb1865033529582e0fe6`

```dockerfile
```

-	Layers:
	-	`sha256:58f3bb41e62e5e98de42e3be870f748aec12d2a62f8576bac1c8869337ee9e15`  
		Last Modified: Mon, 02 Dec 2024 20:32:47 GMT  
		Size: 15.1 MB (15101822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9d1ceb3d92c5f213ec0ca376ec575dd98f09f32d6d5430b2555d6c0b7562d1`  
		Last Modified: Mon, 02 Dec 2024 20:32:46 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:a534b238c9b99b740f1216486f77bf3c14cea88e3a9e1bbf070d86fbab5bb0fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.3 MB (532304484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18675ba81d558cf8f9ec3d367d8c3ec104bff1aab30160b88e8bc51d23329c49`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:8c0d713557008a8d69677c0aa162eedcab0ac7846ed90aee9c2d5788a51fad0f`  
		Last Modified: Mon, 02 Dec 2024 20:24:51 GMT  
		Size: 204.1 MB (204137636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:74c74e7676b304b2cb4c939116791d252bdd51e0bf9e358dcb40dad59a622617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15097814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c3da0659cf7eddc4df08832981dc114a0434eff8cff0f7e0a5318dcda2ea8d`

```dockerfile
```

-	Layers:
	-	`sha256:e179a67825d943f6221f1e2e7a9c60df8de969054fec98b3538bbf4a5682769b`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 15.1 MB (15086597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6b6fde063e7e47ab87f2ab98387725a5cbba86c1ba5665ba2280757cd267dd0`  
		Last Modified: Mon, 02 Dec 2024 20:24:46 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:d242a48452a5f6f490e1c13d3340d54ead1198948a4585dc42e326d6eacd07d1
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
$ docker pull rust@sha256:71aa4f8bdbfb924be55914e8910657aaf15420a87649ea1c64de6f3aef99b357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.7 MB (540737368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51381ded149a6148696b8fd088a50b9684925a0f5c26541db5d3a99db5aae059`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bc823accc52b76a805eb38c2d85f6916c18b62280e12ef86557cf7aae9f958b5`  
		Last Modified: Mon, 02 Dec 2024 20:24:37 GMT  
		Size: 191.4 MB (191418150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:6f2bd220e2f16cb7fe49a9b9ad87295829ed6ebf6b745b45163ccb5c6758e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2628cb17b709463f28662019efa1ac6f3499b61335860965970c347da12bc324`

```dockerfile
```

-	Layers:
	-	`sha256:286a3f2db2c8a6d92215bd0e79bef8cc02de285df8e4a1a45cf8e27b0ab0e625`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 15.5 MB (15500541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dea8927ea34a8749863f37f48d5c3386465f87be87fca83ebfb2da54e47f09`  
		Last Modified: Mon, 02 Dec 2024 20:24:34 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:c4eab5718491261254547e9dee552013f246ffd187d3fe1c1427b2ca4b061ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526493619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b2f5c8fb2f32e205088f699538ac30a1f60f942ca99b46a7d63ee474294911`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:e64ed70b984c825bcf2c316778efdf694d1177f214c907b60097f528bbda5cf8`  
		Last Modified: Mon, 02 Dec 2024 20:29:54 GMT  
		Size: 224.5 MB (224498211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:be5458af59d7a9d4850ec727e792fe1ce39320e685eba63907c07a62c663a19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15317922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8513824646d633879f3b9c31a95e4313b646af70856500a177c618bb79ec94`

```dockerfile
```

-	Layers:
	-	`sha256:d5013ef9b8a7a070d15a1c43f9eb413d3814d5083868ad3477c7ca363e2629e8`  
		Last Modified: Mon, 02 Dec 2024 20:29:49 GMT  
		Size: 15.3 MB (15304676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86a68401994195014fb21c06bdf19c124aea45e5bef8843f712d311bdfced543`  
		Last Modified: Mon, 02 Dec 2024 20:29:48 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f53e59e92e0aeabaf6660d225a107e99c545db88292aa0b26c622e74a040d965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 MB (592017331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c109228921d40f3351cd8c44731f364371c3d17735ca2a5e5f91c306a0dfbfa`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:73de18a65d13f2c8a09a8d948d31e3de3f45af2bead8f228a386915adb234c35`  
		Last Modified: Mon, 02 Dec 2024 20:35:51 GMT  
		Size: 251.8 MB (251804771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:c509b7be5dcd87df97728f5298103aa353944b0f8c8f7d25b5b4b7d797017c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15542437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6766be12848456f1e52235b69ad6e4a319291879e57f2a2238bef89da8f3f9e`

```dockerfile
```

-	Layers:
	-	`sha256:98ab1278bc14cd425e7f3eed1e29aae39b73c5f89b91ccc51caee870f35910be`  
		Last Modified: Mon, 02 Dec 2024 20:35:45 GMT  
		Size: 15.5 MB (15529147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9709d89560fe98a5ae0be73fdda845fa48e30c80363bbca1ff69fdb179217095`  
		Last Modified: Mon, 02 Dec 2024 20:35:44 GMT  
		Size: 13.3 KB (13290 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:2b7d61e0cace1004b172c4c485053c11bc9a0f8bb92c9af92b22ff6d35ea5ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (556034990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fe164933a80fc8c7abf32c417a466d96db3609b6f1ee14d861525cfdd78fea`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:336b9aae3521ef72851abe97810af76d93937f45be24b0cb67340ff9444cb707`  
		Last Modified: Mon, 02 Dec 2024 20:24:45 GMT  
		Size: 204.1 MB (204137618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:2972bbfcb74add45006671eba779b040f9bf6bf4e3f7135555a34491df439bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b839cc63e7b08f07e283f08b415463fb2ab045791fdd19edf58fa0f210451796`

```dockerfile
```

-	Layers:
	-	`sha256:fd8c3f67164e288cb011c211b630adad3ad6454abdf247636e1be356b57369e7`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 15.5 MB (15477801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bde4a6f2185736694cd07ae59ade73bff87e8e8e38ea4758ae457fe22cf0bb7b`  
		Last Modified: Mon, 02 Dec 2024 20:24:39 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:1a3ec9464aaca3679e309b5a2d37d74b8ee5c1d49087f1580d6490b05dff4c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.7 MB (611728786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc406666b8bba58ebe80d82916ba809f85bc3d079aea65006a7189adc4fa98d`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:bb1560f641778d2cb5455f2c6681cb70f74871be341fc94de016ad79eb2311af`  
		Last Modified: Mon, 02 Dec 2024 20:26:21 GMT  
		Size: 248.3 MB (248313252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:4afd1f4300f64430965f43299137ca75249e7c27fbf74de6f92b8393fa33afa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab512b7df0c02174eb212c06d747326403186f429de36c0a0613f77795a9463`

```dockerfile
```

-	Layers:
	-	`sha256:1014165fb7c18bc7f0f45b139b7defb3fdaac4819329563e7b9abfd971721ca9`  
		Last Modified: Mon, 02 Dec 2024 20:26:15 GMT  
		Size: 15.5 MB (15475580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:971d6fde5f27e47969a782345543d65c64c4609aa41146345e4a00de2400f898`  
		Last Modified: Mon, 02 Dec 2024 20:26:14 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:6fc1e9e942c9ad8d4445769678468782e33f232441a2107277aa9309c8171531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.4 MB (593416662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb95fc496432694f3664ec33ed661538c8d318eddb1848edd90df4e723030f4`
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
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
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
	-	`sha256:c731e424a0e50fe1d61cdc956a2238603eb68c82b94428b992cdd8b46e4494ca`  
		Last Modified: Mon, 02 Dec 2024 20:26:44 GMT  
		Size: 274.6 MB (274619819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:a6f9b86026a3aa6e8f0f74e68331895240fe3be10c6d92205fb9e48ff2e3cc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d159b76c2f0dbfef842d8141ba3fb10cf86a429132d7f363f0b81aaf4d7cbd`

```dockerfile
```

-	Layers:
	-	`sha256:e33f6f4afffd15877fb13164def1212d1e66c7616414660e48f2ca508e1427c3`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 15.3 MB (15312980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158597ba495f8617e6dc77be65c0b5dcabe1b602984b6babf8551c0eba26c5d7`  
		Last Modified: Mon, 02 Dec 2024 20:26:39 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:2808c258e14c25a1277d7ba6e653093ef00ba088dc73d99402a900e8cc218d5c
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
$ docker pull rust@sha256:6a3be2a97d72a2d401807e494ff0b2d500bb241293db2f8d84e16b629f952366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291337423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae1dcbb4bdaada87c1f2a5397fb3e2534cd10a921d8b38ab8e032613d4bec82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbfe6cc0ca59f7757297ccc9049930ac7f37bccab06b5fb02b80eb1d37e4a48`  
		Last Modified: Mon, 02 Dec 2024 20:24:38 GMT  
		Size: 262.2 MB (262209428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:1a1e9a3dd7b8efd48e40f7a424dd24b8ba15de70d687a06656717edbb9048faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1ba3680f55e2998a08ff5c873a90a1249c120eba4a76d95874c78c7e755812`

```dockerfile
```

-	Layers:
	-	`sha256:190def7ed7dafd6d8ee1ba46e117570e708371dde8e290f4c757acd3f543a0da`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 4.0 MB (3960916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3749ab658f8ad4f8d17c77b275dd953cfdf9c2de24728be40fda41f514178b`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:6d7afc9f25f7a5cefc9b6f3fbf2304e89502533bf562b3d008f1d7e98e849723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297059662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302b6a008c606c7cd8b9263e55bcb04488d3fe948c1a45f2f7a6b2e9f6c11f23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defe357fcbe93d1e65d0570d021785ad676696d2d624262bdb0e214723689b36`  
		Last Modified: Mon, 02 Dec 2024 20:31:38 GMT  
		Size: 272.3 MB (272340753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:3f2058fe6f54a997932102d8b6bc235e8d4666e331b9296243cf75c70990da78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7fc6c7b289d0a098a407027d015ead0708a0e04655389eae49e4155b848f52`

```dockerfile
```

-	Layers:
	-	`sha256:8928a87a6013ae9d938cea84efc86dfc5fb240cf83f931e727c7693adaa6da2c`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 3.8 MB (3776732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea6b01b234f1e08ebc59a4a02bda774ffe04cf102809435a132937896e535eaf`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:594e5e30e34cb3f1edfcf62b6c42ab7418bfbe4fd83057099fede39488edc7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.8 MB (346802313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3d008bad10df60f61201660a99f5d86423c1a1a546c0a1a1838123d75a27a1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0237173b80106fe0760a817d7e6d1c71f9e5e284c512b7d06074708c59aff7`  
		Last Modified: Mon, 02 Dec 2024 20:37:13 GMT  
		Size: 317.6 MB (317644957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:895f4818b23e10a7e1f1880f5e42eb988a221a3a0eb6f39134e09fa24dcf11ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e2f37d04cfed0d9e84101878c4064b4b8353ce7996f5587a68e63f1e717bd8`

```dockerfile
```

-	Layers:
	-	`sha256:05e0e8f9842371d47373dc72339abb01c46ebf232229e4810af7074cc8f68115`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 4.0 MB (3983284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b63a1b31beb1e3b516d716bd7530b21f5698318b664ff2c0808a3a6738dbc2`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:e3a12bd5e08f7ffd7c014c2820aa4bbb647a30f3617f59659136669d0765cde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301886447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3c3937265088583d6ea42714a975738f2bf863ef26ec51c0eceafa294d88e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ceb72ece1ea1e0fe9569779176af4568889e4706901654739657a99aa4700`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 271.7 MB (271740997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:ea30beb0ac18971c71310961164ae02c93873a3dee5e71820cb92ca5af9cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad0f3a1a05782cc497e5841bd1cba942630e16eb84acaf9a3809618df1ee6d`

```dockerfile
```

-	Layers:
	-	`sha256:bf795665c0773ee9ebba9af59adaf88084fc89e625ffd096983779a3322b9d98`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea300ff11941e5c8c9dca6dae2eaeb1b7aa9ff4ffacb336422e939217214bca`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:901e8fd72a554e505e9273538a8ad34c2bf33a02f62b634250d35e34bb2ded90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.2 MB (350198087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c2aef4eee77ed0f0829ba276a911bf8cd57b8afb28b00184b775c489a82bb4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a607df9bd35302bace9a6ad9223bd9a4b868b9c462a42e5cca65d5fd3d8a9b`  
		Last Modified: Mon, 02 Dec 2024 20:29:03 GMT  
		Size: 317.1 MB (317072734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:12a9974e9bd55d24e84c10e72f5170591f010651e62da1a001cce00b60a8b5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f48e8cf17275373c2886d5d424e13f54217678435465c09519f9d27932b9a4`

```dockerfile
```

-	Layers:
	-	`sha256:1969029d7112da6fdd40a3a936b1152b38032abb4d7bd1bc31411ed5fd021715`  
		Last Modified: Mon, 02 Dec 2024 20:28:53 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52df272aeab4c0542aa89ec9e6638cabd6465bf962ee7053c5eac2b05e53b44d`  
		Last Modified: Mon, 02 Dec 2024 20:28:52 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:59e72321724e973f7b278fe9cfdbc7916988c33529e4f16eaa3be7e72b4d7b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352217458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c145addc8a9384eb579adb69c9d9500d0a57a3690e0e396cdce0b24098684ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e04d7c8b55a5ef929486fce3eca63d3be7958f04b601f4f73a52e9591e4a16`  
		Last Modified: Mon, 02 Dec 2024 20:28:50 GMT  
		Size: 324.7 MB (324725830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:34d0adfbc6046e33a5307df483d7f0626cfbedc28bc7cb0fa092b40008a9d30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3815877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4d233def5b8a5cbdca87e1d70f4c0e5602f12e771f4e9c36399233edb2ef42`

```dockerfile
```

-	Layers:
	-	`sha256:a2bb7709243f1094bc9ed02cbe32492f025e7ba1b46404d9f64f3527d774ce68`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 3.8 MB (3802606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60ee2d606d582a3328f010baeb9968ac6e723667c4dac109be44717dae4d543`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:2808c258e14c25a1277d7ba6e653093ef00ba088dc73d99402a900e8cc218d5c
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
$ docker pull rust@sha256:6a3be2a97d72a2d401807e494ff0b2d500bb241293db2f8d84e16b629f952366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291337423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae1dcbb4bdaada87c1f2a5397fb3e2534cd10a921d8b38ab8e032613d4bec82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbfe6cc0ca59f7757297ccc9049930ac7f37bccab06b5fb02b80eb1d37e4a48`  
		Last Modified: Mon, 02 Dec 2024 20:24:38 GMT  
		Size: 262.2 MB (262209428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1a1e9a3dd7b8efd48e40f7a424dd24b8ba15de70d687a06656717edbb9048faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1ba3680f55e2998a08ff5c873a90a1249c120eba4a76d95874c78c7e755812`

```dockerfile
```

-	Layers:
	-	`sha256:190def7ed7dafd6d8ee1ba46e117570e708371dde8e290f4c757acd3f543a0da`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 4.0 MB (3960916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3749ab658f8ad4f8d17c77b275dd953cfdf9c2de24728be40fda41f514178b`  
		Last Modified: Mon, 02 Dec 2024 20:24:31 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:6d7afc9f25f7a5cefc9b6f3fbf2304e89502533bf562b3d008f1d7e98e849723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297059662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302b6a008c606c7cd8b9263e55bcb04488d3fe948c1a45f2f7a6b2e9f6c11f23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defe357fcbe93d1e65d0570d021785ad676696d2d624262bdb0e214723689b36`  
		Last Modified: Mon, 02 Dec 2024 20:31:38 GMT  
		Size: 272.3 MB (272340753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3f2058fe6f54a997932102d8b6bc235e8d4666e331b9296243cf75c70990da78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3790112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7fc6c7b289d0a098a407027d015ead0708a0e04655389eae49e4155b848f52`

```dockerfile
```

-	Layers:
	-	`sha256:8928a87a6013ae9d938cea84efc86dfc5fb240cf83f931e727c7693adaa6da2c`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 3.8 MB (3776732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea6b01b234f1e08ebc59a4a02bda774ffe04cf102809435a132937896e535eaf`  
		Last Modified: Mon, 02 Dec 2024 20:31:32 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:594e5e30e34cb3f1edfcf62b6c42ab7418bfbe4fd83057099fede39488edc7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.8 MB (346802313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3d008bad10df60f61201660a99f5d86423c1a1a546c0a1a1838123d75a27a1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0237173b80106fe0760a817d7e6d1c71f9e5e284c512b7d06074708c59aff7`  
		Last Modified: Mon, 02 Dec 2024 20:37:13 GMT  
		Size: 317.6 MB (317644957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:895f4818b23e10a7e1f1880f5e42eb988a221a3a0eb6f39134e09fa24dcf11ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e2f37d04cfed0d9e84101878c4064b4b8353ce7996f5587a68e63f1e717bd8`

```dockerfile
```

-	Layers:
	-	`sha256:05e0e8f9842371d47373dc72339abb01c46ebf232229e4810af7074cc8f68115`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 4.0 MB (3983284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b63a1b31beb1e3b516d716bd7530b21f5698318b664ff2c0808a3a6738dbc2`  
		Last Modified: Mon, 02 Dec 2024 20:37:06 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:e3a12bd5e08f7ffd7c014c2820aa4bbb647a30f3617f59659136669d0765cde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301886447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3c3937265088583d6ea42714a975738f2bf863ef26ec51c0eceafa294d88e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ceb72ece1ea1e0fe9569779176af4568889e4706901654739657a99aa4700`  
		Last Modified: Mon, 02 Dec 2024 20:24:47 GMT  
		Size: 271.7 MB (271740997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ea30beb0ac18971c71310961164ae02c93873a3dee5e71820cb92ca5af9cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bad0f3a1a05782cc497e5841bd1cba942630e16eb84acaf9a3809618df1ee6d`

```dockerfile
```

-	Layers:
	-	`sha256:bf795665c0773ee9ebba9af59adaf88084fc89e625ffd096983779a3322b9d98`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 3.9 MB (3940829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea300ff11941e5c8c9dca6dae2eaeb1b7aa9ff4ffacb336422e939217214bca`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:901e8fd72a554e505e9273538a8ad34c2bf33a02f62b634250d35e34bb2ded90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.2 MB (350198087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c2aef4eee77ed0f0829ba276a911bf8cd57b8afb28b00184b775c489a82bb4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a607df9bd35302bace9a6ad9223bd9a4b868b9c462a42e5cca65d5fd3d8a9b`  
		Last Modified: Mon, 02 Dec 2024 20:29:03 GMT  
		Size: 317.1 MB (317072734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:12a9974e9bd55d24e84c10e72f5170591f010651e62da1a001cce00b60a8b5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f48e8cf17275373c2886d5d424e13f54217678435465c09519f9d27932b9a4`

```dockerfile
```

-	Layers:
	-	`sha256:1969029d7112da6fdd40a3a936b1152b38032abb4d7bd1bc31411ed5fd021715`  
		Last Modified: Mon, 02 Dec 2024 20:28:53 GMT  
		Size: 3.9 MB (3933415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52df272aeab4c0542aa89ec9e6638cabd6465bf962ee7053c5eac2b05e53b44d`  
		Last Modified: Mon, 02 Dec 2024 20:28:52 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:59e72321724e973f7b278fe9cfdbc7916988c33529e4f16eaa3be7e72b4d7b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352217458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c145addc8a9384eb579adb69c9d9500d0a57a3690e0e396cdce0b24098684ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e04d7c8b55a5ef929486fce3eca63d3be7958f04b601f4f73a52e9591e4a16`  
		Last Modified: Mon, 02 Dec 2024 20:28:50 GMT  
		Size: 324.7 MB (324725830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:34d0adfbc6046e33a5307df483d7f0626cfbedc28bc7cb0fa092b40008a9d30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3815877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4d233def5b8a5cbdca87e1d70f4c0e5602f12e771f4e9c36399233edb2ef42`

```dockerfile
```

-	Layers:
	-	`sha256:a2bb7709243f1094bc9ed02cbe32492f025e7ba1b46404d9f64f3527d774ce68`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 3.8 MB (3802606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60ee2d606d582a3328f010baeb9968ac6e723667c4dac109be44717dae4d543`  
		Last Modified: Mon, 02 Dec 2024 20:28:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:cd64d55bf5d90faca3b5e69039e03cc8eaf4d0c531537cb08d20ee8ee87f438f
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
$ docker pull rust@sha256:693226f9da3b618f747e1d45901d1d6c27e591f5d3d17c92685a55f4983911ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.8 MB (282812182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecfd0a5420dc73cd925c46f1879d9c00df802531eccda112b2d406071cacca0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384329ccf6be51bb1ef6f2b07175dcdcebcf898a37bba183bfe10f903be995ce`  
		Last Modified: Mon, 02 Dec 2024 20:24:22 GMT  
		Size: 251.4 MB (251360621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ebc287a15a3e3cd43102b0e5b3df9aae5ae0a8cd284c6cd6845bc32e9e0b5903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4191040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8375006c14246df12ba094238c9468666ade0d799bb9d20f012e4f299847e56a`

```dockerfile
```

-	Layers:
	-	`sha256:74af93f126d4c06de89836c2cf05cebb553960e94e4ab55a74d46b28183ad983`  
		Last Modified: Mon, 02 Dec 2024 20:24:19 GMT  
		Size: 4.2 MB (4179684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c366dfc129927914c32fbdf3b3a7128249ed30666f407a63a7ff0f19be5aff8`  
		Last Modified: Mon, 02 Dec 2024 20:24:18 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:abf606a99416890d34310c1ed7c2dc863aa6a1ce4f8ab588c768b2511ffdaa5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.2 MB (293172521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4ff907c925646494aeeb07f6a9c015b9f209c836a858b44c751fffc645ed1b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fffe59376f64ffa8f62067ec6c177458ad560736ecb62f5a746b99a1213febb`  
		Last Modified: Mon, 02 Dec 2024 20:27:46 GMT  
		Size: 266.6 MB (266563264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6ec69ccb3c2df674b652af2bf87b9af3d1c186c907bacf211557fca6a0605d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d2e1fea37fd47ebcb90737269a9a15f43d09ff6e3a8ac409221ed3d6a3b8d3`

```dockerfile
```

-	Layers:
	-	`sha256:b11be9c55ffbd97983468ba6c80f6bfb1b6d2f881f28c132a972181a2f323cf1`  
		Last Modified: Mon, 02 Dec 2024 20:27:40 GMT  
		Size: 4.0 MB (3988606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9172172b88ef1546ba7e0d5edb4641fbb14bdf07ff13f0bb89ccbb6102cb8a32`  
		Last Modified: Mon, 02 Dec 2024 20:27:40 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a32ae5ae9cad532df229a1fef4ada9991409591a7ccf15c3856ba3ca21d7c26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.4 MB (337389995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504b549e7eafa02320debcac41241b24c3e628c6a7f2c4a085a0e8430d5fa44f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b17b8db729381225a8d73b8af06a440c8b3f44ba100df98709bb0b03c0a016`  
		Last Modified: Mon, 02 Dec 2024 20:34:10 GMT  
		Size: 307.3 MB (307298395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3b6d85ff4952c3db80e6f66474078bd4e09bc1b884e7978509e0cf8a7c4410ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4187819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2535b26d94240ff8a8243d5fcaf6cd4f3238cc6575f145c7055f3be7a7af6e18`

```dockerfile
```

-	Layers:
	-	`sha256:280d6fd398dd958493aa5d431829910d0726c625baf5513aa3477e64de936e0d`  
		Last Modified: Mon, 02 Dec 2024 20:34:04 GMT  
		Size: 4.2 MB (4176359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb393af559bdc07a24e80a9442f17ed5976eafc6cced8e26e7df0a3132f88ce7`  
		Last Modified: Mon, 02 Dec 2024 20:34:04 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:d5af146980a072b682d3ac22609ffed95252933df15d14690667925cf35a83bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297129117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182df1c816edafaeadc3362a748a39f671aa57bf19f6d7fafd20bcb2a4becdd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 28 Nov 2024 14:36:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 28 Nov 2024 14:36:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 28 Nov 2024 14:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a29bf3a9090d3e58d845509836c32130197f51dc0eafb75e2102450607aa614`  
		Last Modified: Mon, 02 Dec 2024 20:24:48 GMT  
		Size: 264.7 MB (264705766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:de112da84d3f18bbad7559779bde4d938157704801863564aaae2a20e856f0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaa8827be2c8dbe784a39a4b999bb4842aa2514d900dbd211b897aabc55f32b`

```dockerfile
```

-	Layers:
	-	`sha256:1e6ab84278603cf43cd88053eb59875eea8a1a59d9a120bb129fdeff7482806d`  
		Last Modified: Mon, 02 Dec 2024 20:24:41 GMT  
		Size: 4.2 MB (4169952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67bd2e3b5300c4b614ff1c265cf9f027c92cb2fd18db1cac9fc58fb89c69ea17`  
		Last Modified: Mon, 02 Dec 2024 20:24:40 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json
