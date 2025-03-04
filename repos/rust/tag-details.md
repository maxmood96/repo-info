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
-	[`rust:1.85`](#rust185)
-	[`rust:1.85-alpine`](#rust185-alpine)
-	[`rust:1.85-alpine3.20`](#rust185-alpine320)
-	[`rust:1.85-alpine3.21`](#rust185-alpine321)
-	[`rust:1.85-bookworm`](#rust185-bookworm)
-	[`rust:1.85-bullseye`](#rust185-bullseye)
-	[`rust:1.85-slim`](#rust185-slim)
-	[`rust:1.85-slim-bookworm`](#rust185-slim-bookworm)
-	[`rust:1.85-slim-bullseye`](#rust185-slim-bullseye)
-	[`rust:1.85.0`](#rust1850)
-	[`rust:1.85.0-alpine`](#rust1850-alpine)
-	[`rust:1.85.0-alpine3.20`](#rust1850-alpine320)
-	[`rust:1.85.0-alpine3.21`](#rust1850-alpine321)
-	[`rust:1.85.0-bookworm`](#rust1850-bookworm)
-	[`rust:1.85.0-bullseye`](#rust1850-bullseye)
-	[`rust:1.85.0-slim`](#rust1850-slim)
-	[`rust:1.85.0-slim-bookworm`](#rust1850-slim-bookworm)
-	[`rust:1.85.0-slim-bullseye`](#rust1850-slim-bullseye)
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
$ docker pull rust@sha256:e15c642b487dd013b2e425d001d32927391aca787ac582b98cca72234d466b60
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
$ docker pull rust@sha256:f6fc45b5a8d3b72dcff6442b5311f0b1f854a3480797f91ecbfb16c0fd5d4527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.0 MB (541963415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aac1c9ca934dcc8a2f93033651d5f86fb3b99783c81428ecce40198d4abc0af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c03d5625da4fd65f189b350dab8fda9ce3054bdd41f9a509973b3cd0cd571e`  
		Last Modified: Mon, 03 Mar 2025 21:14:28 GMT  
		Size: 193.7 MB (193695926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:4d1be75651ae6516c73cd01fb804f023e4d53bdf2b9d5cb9e5a78381266818c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca03f69ea0d5d937b5bf2bba4b75d5a4cb308e7460975b526f3138436e1a7f7b`

```dockerfile
```

-	Layers:
	-	`sha256:f2aa5e71de5c6e138f09eb61c0c64219101f7290d0719c4e4f2763b9cbbcafa9`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 15.5 MB (15474256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bfe55c7c856b4e205d1086d7f00a0c16d9544ceb0316ec5f5368e8f86a5a815`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:cb81fdf6321d7de7b04a0978a0f1af3d2ce2e9b5302a619b7d538132a0d783bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531318143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cba7271ee5cf51b3565fbb44d531aa336955fdf97d4159e8544e9e1ede35187`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70e25650a3be5d12fed3dfd4069f605d42d17b86fa4c689b69aa636aee22155`  
		Last Modified: Mon, 03 Mar 2025 21:18:08 GMT  
		Size: 230.3 MB (230264903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:c6712addcc809b8eb0fe21d81f7f7eba0637e2838086b119dcbbc41e4187a6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e9006d373cfef0bc4e89bb17079c2f22f1ae42ed8a2b7dcd57d4b3c67b04c9`

```dockerfile
```

-	Layers:
	-	`sha256:fab2c1c1f543fac09d7660a2054a25708a28b23b14e1f1c9a3a6e1644e54b678`  
		Last Modified: Mon, 03 Mar 2025 21:18:02 GMT  
		Size: 15.3 MB (15278698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f349b53969dfbfa675b8173f92a74dbd59458f6214685c9dd2c7318179f6cc32`  
		Last Modified: Mon, 03 Mar 2025 21:18:01 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be252dc02478902ea4c4a6e1e2b49181f1fa3aaeb96a47e40dc248b2598cf243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.8 MB (597772744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192cc1afeb41abe7df5d2c3f94eb7e40a991156c86412ad4cab156f754d7f291`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b5a4332d3d01f663d9e0b5d8a153c25ca20c2d7e94ce224b627a88380da001`  
		Last Modified: Mon, 03 Mar 2025 21:31:31 GMT  
		Size: 258.8 MB (258797571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:0cea832fdaaa30a9c04e35a4d5de0ede3f8723564efacebd2cae817dba8af26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef22842e59d31eab71173da3ae37fbcabd9b445839c9e49ffa7b0d93c64a8f51`

```dockerfile
```

-	Layers:
	-	`sha256:463dc9b45f12289d11de3d7eaffa14e7641471dd399b68728748be80a572fea3`  
		Last Modified: Mon, 03 Mar 2025 21:31:25 GMT  
		Size: 15.5 MB (15502831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:479aac264bc9d5563cda8973c1adf5fcc9d667f916488c189c512d2bb1d18d12`  
		Last Modified: Mon, 03 Mar 2025 21:31:24 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:c3ba8ba76e08440fcff73d04693fef720530890076f46b8761da0dddcedadb78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.7 MB (561694245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676197b0baccfd7dd45db61469de196ac15950aa10debfbcd2b0583af2dafed4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca163299b0e606d2916a03bd0f60c5903c6e5abeab65da3a8c490174697c929`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 24.9 MB (24899353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c3400be327e90dc9e848a16d4b0fcd191708de152e68c6b4888d83c61f441`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 66.2 MB (66237814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3ca8ca718f538c2871c3deeec438c611f0f26a3b97976b89d6d6abcca894dd`  
		Last Modified: Tue, 25 Feb 2025 05:12:06 GMT  
		Size: 210.3 MB (210255482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c5735fe88e109ded1d53e0e079c60705e16af5652ea6c119760594e52d6fb`  
		Last Modified: Mon, 03 Mar 2025 21:14:43 GMT  
		Size: 210.8 MB (210843144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:8c10ae28c24f12a5b3e3598c4abb8a26206a7edef522211dc27667c598621f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5c3c563ea6d86b133dd81fc4d8eaecefc99bc076f1c075059797e8116f36d3`

```dockerfile
```

-	Layers:
	-	`sha256:0ab28f08ca6a412da7f3016c8c2eb5dc331d3000a50c38114eb87924f817b53a`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 15.5 MB (15451518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd3c3e28ee8144d301f821eb5b432e99ec8f8776af706e07ba3a04d48e6f7ac`  
		Last Modified: Mon, 03 Mar 2025 21:14:37 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:0fe5e17dc44d5fdbd2560266262d98e813b49ca1e9b0ba23d9b3675fe2adacb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.6 MB (616586281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d35305b8c7077eb68baa8b585fec750d11f2afc7094e64b59f8e368246879`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad13c90d099a380a8fc2ec9ef74de7ad957b1496d75b8d1c4617069765510053`  
		Last Modified: Mon, 03 Mar 2025 21:24:43 GMT  
		Size: 254.3 MB (254345476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:0676ad8c84ebbb134f5e3c3aab74a661c1ac924ee0fa1a042d90d7fbadfc4585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ad946c6e11f49c09021728047cc0f3fa4a83f0101fa1031085c8f8e0d2ca1c`

```dockerfile
```

-	Layers:
	-	`sha256:14a5009de22d0268d16a06051e63b1bd4e5a83615d08555e021663ada543f0e2`  
		Last Modified: Mon, 03 Mar 2025 21:24:31 GMT  
		Size: 15.4 MB (15449362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e237236a91844fef1f239951791ab5549d6226f7a182592fa6867fc48d952279`  
		Last Modified: Mon, 03 Mar 2025 21:24:28 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:70fe5668b3762d8a81b5059f9c4bad31ac92bf152d57195193c433368ec36f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599864262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b0dc30045f5d2e53b0a2a92cd31f6f8e3bdeca4ccb1165d6d2ac3cdcf807a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f679165548785dd187eaea9af4ee69db5b37630f35ce564d064cd7512fcfb9`  
		Last Modified: Mon, 03 Mar 2025 21:31:35 GMT  
		Size: 281.8 MB (281820436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:dbf40b3fd37699736f3445354654c43b50a382b3ef92f0ea8de4366bcc1af9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d288575d5989682a9df5b6cb7dc314ca8e3380685956acf21030572b2fe26d2e`

```dockerfile
```

-	Layers:
	-	`sha256:83fad1cb4c19e71cbc100ba5c079f7fda458db61bafa47c1cc48e228ce18802f`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 15.3 MB (15286944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4d7f0c7c0907b0c5b392d225150310f20e92d9173b7a16ce384cd7507427f6`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:1030547bd568497d69e41771ada279179f0613369dc54779e46a3f6f376b3020
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:84b5e9c7c2f9437f62769913b419cc02a1e310bf40fd86720cd2b3b64bffb452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304368783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec94ecf18f99333d5bd8f2a15427ba1b4736299f4d5f4a35660f5fe75b6291a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b95e11be61c0eea8aadf788692bf0fcec5f9c75738d3f5713dfbcc016f337f4`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 61.6 MB (61565003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6fc4d476520099dcd8ba0f71c1e15bb2d762c9977506070eea6cb78a2a4c6`  
		Last Modified: Mon, 03 Mar 2025 21:14:31 GMT  
		Size: 239.2 MB (239161533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:d8cff90939ad06ca11df0fc881253dc5d1d768c2221f8466415334d2739cbfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4955895d71a1f61c0886f29ea5b6a23986cda0a9910e8ba13ff472aff21cac1f`

```dockerfile
```

-	Layers:
	-	`sha256:fd7a8c7ea021f7804add54b5f5efd33149b2e2c7d915f1622744e64dbbe08c7c`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457f860b4e4d19a0674d0ca4f6ec06ff6958c351407559ee9c974d2b3bbca63f`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bda9e5682eeb0013c19b06e469812ae54cbe76cf0128796def8eb9bfe30a5c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307415047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72195abfac34db128f0c99e35ad0a1a98210b81274e98b65ac2973dae8aeb0dd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b46568d489c620031542c16213dea9e63b74c664a11f85b1bb86a8e526e5a16`  
		Last Modified: Mon, 03 Mar 2025 21:23:23 GMT  
		Size: 59.1 MB (59101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51de9687e383104ad782ecb8afe38b4c33220f4e646112f07f0e47d399d0a9fd`  
		Last Modified: Mon, 03 Mar 2025 21:23:28 GMT  
		Size: 244.3 MB (244320886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:429bfdee3cf71b49563ad904faf2875e578ae734980bd44b1c38b27f5855fd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d07c59fd4b9553baf3c76bd773969e82fed14c0dcfa7ca467660406d07156`

```dockerfile
```

-	Layers:
	-	`sha256:fbed74b3e0b30a9432fe2ba4b82f04cb881dd5c6f374c1aff1f3d2f2018fb7f3`  
		Last Modified: Mon, 03 Mar 2025 21:23:22 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81eca9cb1582aed143c4d744ce7a925b1e10e4678aaf0916e76d40846bb2d61`  
		Last Modified: Mon, 03 Mar 2025 21:23:21 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:f0cef6c65992995b1c7816cb667de95799852e3fbed9d06f95855cbc512a0fd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:6d824fef86a8532aecead5889d49d432d19e0dd58b958266c994cca9eb7a3357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298102813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c38e59fb99c1014ea6d250d396bb9bf55981f1d69fe17ed05047b90cd119ca9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0430b4a2b30329b0c06034d1df61c2f3533c436834a54b76def8756d804d888`  
		Last Modified: Mon, 03 Mar 2025 21:17:28 GMT  
		Size: 55.3 MB (55315558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fda7dd06f6e434e3727cd86155430a51568846533e3824548334e20f1078e28`  
		Last Modified: Mon, 03 Mar 2025 21:17:31 GMT  
		Size: 239.2 MB (239160358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:ab2a41c3a86b0e8de97e1cff7ca3624a6e69e478c7c29615df5979d5655d03c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e987a7ec625942a721de02dcd92bf4ea3f7481ee651c6aef639e3a2f3f16ba`

```dockerfile
```

-	Layers:
	-	`sha256:4100e90a822ec6152c54ec22e8ce0b4cfb24694b82b0d9252e191958ce4d59cf`  
		Last Modified: Mon, 03 Mar 2025 21:17:28 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca3c1b9b1144fd4038e19dea5e9afef77e4732804442cc1813ffcbd1c7289e4`  
		Last Modified: Mon, 03 Mar 2025 21:17:27 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f91c5c68a69111314bb721b7bb75aaa4b310b9ef676f2591e88769bbbb3bd933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301363171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61566cb96efc54b3ee29f6409c0e76059ca7b3c261b99a2940c188c54c3a66c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c8bee9c91c68545cb9604a6baaf13f4c921f1a8a851437cc7ce63f942e113d`  
		Last Modified: Mon, 03 Mar 2025 21:26:24 GMT  
		Size: 53.0 MB (52950488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998e7300919f154807a1ce8bdaa868228719c39a95b4c276a758f1bf480b361`  
		Last Modified: Mon, 03 Mar 2025 21:26:28 GMT  
		Size: 244.3 MB (244321518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1e4651facc4a66b01c40f8bec063469f936cbf603daf477c1003e794040d3e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beeb6c0426bb32cbdd133d31ad5ed10820561b72d66e1d95f332bfb42d012779`

```dockerfile
```

-	Layers:
	-	`sha256:183ceb0143fb3784d416af0d9e6e49059191e33606b5db6d715b5666f0fd139b`  
		Last Modified: Mon, 03 Mar 2025 21:26:22 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe75a1adc68e5615e04f2ea23b7e198a996bb1378319d115d5ca7b6fbef7602`  
		Last Modified: Mon, 03 Mar 2025 21:26:22 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.21`

```console
$ docker pull rust@sha256:1030547bd568497d69e41771ada279179f0613369dc54779e46a3f6f376b3020
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:84b5e9c7c2f9437f62769913b419cc02a1e310bf40fd86720cd2b3b64bffb452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304368783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec94ecf18f99333d5bd8f2a15427ba1b4736299f4d5f4a35660f5fe75b6291a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b95e11be61c0eea8aadf788692bf0fcec5f9c75738d3f5713dfbcc016f337f4`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 61.6 MB (61565003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6fc4d476520099dcd8ba0f71c1e15bb2d762c9977506070eea6cb78a2a4c6`  
		Last Modified: Mon, 03 Mar 2025 21:14:31 GMT  
		Size: 239.2 MB (239161533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:d8cff90939ad06ca11df0fc881253dc5d1d768c2221f8466415334d2739cbfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4955895d71a1f61c0886f29ea5b6a23986cda0a9910e8ba13ff472aff21cac1f`

```dockerfile
```

-	Layers:
	-	`sha256:fd7a8c7ea021f7804add54b5f5efd33149b2e2c7d915f1622744e64dbbe08c7c`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457f860b4e4d19a0674d0ca4f6ec06ff6958c351407559ee9c974d2b3bbca63f`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bda9e5682eeb0013c19b06e469812ae54cbe76cf0128796def8eb9bfe30a5c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307415047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72195abfac34db128f0c99e35ad0a1a98210b81274e98b65ac2973dae8aeb0dd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b46568d489c620031542c16213dea9e63b74c664a11f85b1bb86a8e526e5a16`  
		Last Modified: Mon, 03 Mar 2025 21:23:23 GMT  
		Size: 59.1 MB (59101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51de9687e383104ad782ecb8afe38b4c33220f4e646112f07f0e47d399d0a9fd`  
		Last Modified: Mon, 03 Mar 2025 21:23:28 GMT  
		Size: 244.3 MB (244320886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:429bfdee3cf71b49563ad904faf2875e578ae734980bd44b1c38b27f5855fd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d07c59fd4b9553baf3c76bd773969e82fed14c0dcfa7ca467660406d07156`

```dockerfile
```

-	Layers:
	-	`sha256:fbed74b3e0b30a9432fe2ba4b82f04cb881dd5c6f374c1aff1f3d2f2018fb7f3`  
		Last Modified: Mon, 03 Mar 2025 21:23:22 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81eca9cb1582aed143c4d744ce7a925b1e10e4678aaf0916e76d40846bb2d61`  
		Last Modified: Mon, 03 Mar 2025 21:23:21 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:e15c642b487dd013b2e425d001d32927391aca787ac582b98cca72234d466b60
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
$ docker pull rust@sha256:f6fc45b5a8d3b72dcff6442b5311f0b1f854a3480797f91ecbfb16c0fd5d4527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.0 MB (541963415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aac1c9ca934dcc8a2f93033651d5f86fb3b99783c81428ecce40198d4abc0af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c03d5625da4fd65f189b350dab8fda9ce3054bdd41f9a509973b3cd0cd571e`  
		Last Modified: Mon, 03 Mar 2025 21:14:28 GMT  
		Size: 193.7 MB (193695926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4d1be75651ae6516c73cd01fb804f023e4d53bdf2b9d5cb9e5a78381266818c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca03f69ea0d5d937b5bf2bba4b75d5a4cb308e7460975b526f3138436e1a7f7b`

```dockerfile
```

-	Layers:
	-	`sha256:f2aa5e71de5c6e138f09eb61c0c64219101f7290d0719c4e4f2763b9cbbcafa9`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 15.5 MB (15474256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bfe55c7c856b4e205d1086d7f00a0c16d9544ceb0316ec5f5368e8f86a5a815`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:cb81fdf6321d7de7b04a0978a0f1af3d2ce2e9b5302a619b7d538132a0d783bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531318143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cba7271ee5cf51b3565fbb44d531aa336955fdf97d4159e8544e9e1ede35187`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70e25650a3be5d12fed3dfd4069f605d42d17b86fa4c689b69aa636aee22155`  
		Last Modified: Mon, 03 Mar 2025 21:18:08 GMT  
		Size: 230.3 MB (230264903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c6712addcc809b8eb0fe21d81f7f7eba0637e2838086b119dcbbc41e4187a6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e9006d373cfef0bc4e89bb17079c2f22f1ae42ed8a2b7dcd57d4b3c67b04c9`

```dockerfile
```

-	Layers:
	-	`sha256:fab2c1c1f543fac09d7660a2054a25708a28b23b14e1f1c9a3a6e1644e54b678`  
		Last Modified: Mon, 03 Mar 2025 21:18:02 GMT  
		Size: 15.3 MB (15278698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f349b53969dfbfa675b8173f92a74dbd59458f6214685c9dd2c7318179f6cc32`  
		Last Modified: Mon, 03 Mar 2025 21:18:01 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be252dc02478902ea4c4a6e1e2b49181f1fa3aaeb96a47e40dc248b2598cf243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.8 MB (597772744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192cc1afeb41abe7df5d2c3f94eb7e40a991156c86412ad4cab156f754d7f291`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b5a4332d3d01f663d9e0b5d8a153c25ca20c2d7e94ce224b627a88380da001`  
		Last Modified: Mon, 03 Mar 2025 21:31:31 GMT  
		Size: 258.8 MB (258797571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0cea832fdaaa30a9c04e35a4d5de0ede3f8723564efacebd2cae817dba8af26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef22842e59d31eab71173da3ae37fbcabd9b445839c9e49ffa7b0d93c64a8f51`

```dockerfile
```

-	Layers:
	-	`sha256:463dc9b45f12289d11de3d7eaffa14e7641471dd399b68728748be80a572fea3`  
		Last Modified: Mon, 03 Mar 2025 21:31:25 GMT  
		Size: 15.5 MB (15502831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:479aac264bc9d5563cda8973c1adf5fcc9d667f916488c189c512d2bb1d18d12`  
		Last Modified: Mon, 03 Mar 2025 21:31:24 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:c3ba8ba76e08440fcff73d04693fef720530890076f46b8761da0dddcedadb78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.7 MB (561694245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676197b0baccfd7dd45db61469de196ac15950aa10debfbcd2b0583af2dafed4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca163299b0e606d2916a03bd0f60c5903c6e5abeab65da3a8c490174697c929`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 24.9 MB (24899353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c3400be327e90dc9e848a16d4b0fcd191708de152e68c6b4888d83c61f441`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 66.2 MB (66237814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3ca8ca718f538c2871c3deeec438c611f0f26a3b97976b89d6d6abcca894dd`  
		Last Modified: Tue, 25 Feb 2025 05:12:06 GMT  
		Size: 210.3 MB (210255482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c5735fe88e109ded1d53e0e079c60705e16af5652ea6c119760594e52d6fb`  
		Last Modified: Mon, 03 Mar 2025 21:14:43 GMT  
		Size: 210.8 MB (210843144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8c10ae28c24f12a5b3e3598c4abb8a26206a7edef522211dc27667c598621f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5c3c563ea6d86b133dd81fc4d8eaecefc99bc076f1c075059797e8116f36d3`

```dockerfile
```

-	Layers:
	-	`sha256:0ab28f08ca6a412da7f3016c8c2eb5dc331d3000a50c38114eb87924f817b53a`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 15.5 MB (15451518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd3c3e28ee8144d301f821eb5b432e99ec8f8776af706e07ba3a04d48e6f7ac`  
		Last Modified: Mon, 03 Mar 2025 21:14:37 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:0fe5e17dc44d5fdbd2560266262d98e813b49ca1e9b0ba23d9b3675fe2adacb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.6 MB (616586281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d35305b8c7077eb68baa8b585fec750d11f2afc7094e64b59f8e368246879`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad13c90d099a380a8fc2ec9ef74de7ad957b1496d75b8d1c4617069765510053`  
		Last Modified: Mon, 03 Mar 2025 21:24:43 GMT  
		Size: 254.3 MB (254345476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0676ad8c84ebbb134f5e3c3aab74a661c1ac924ee0fa1a042d90d7fbadfc4585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ad946c6e11f49c09021728047cc0f3fa4a83f0101fa1031085c8f8e0d2ca1c`

```dockerfile
```

-	Layers:
	-	`sha256:14a5009de22d0268d16a06051e63b1bd4e5a83615d08555e021663ada543f0e2`  
		Last Modified: Mon, 03 Mar 2025 21:24:31 GMT  
		Size: 15.4 MB (15449362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e237236a91844fef1f239951791ab5549d6226f7a182592fa6867fc48d952279`  
		Last Modified: Mon, 03 Mar 2025 21:24:28 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:70fe5668b3762d8a81b5059f9c4bad31ac92bf152d57195193c433368ec36f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599864262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b0dc30045f5d2e53b0a2a92cd31f6f8e3bdeca4ccb1165d6d2ac3cdcf807a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f679165548785dd187eaea9af4ee69db5b37630f35ce564d064cd7512fcfb9`  
		Last Modified: Mon, 03 Mar 2025 21:31:35 GMT  
		Size: 281.8 MB (281820436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:dbf40b3fd37699736f3445354654c43b50a382b3ef92f0ea8de4366bcc1af9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d288575d5989682a9df5b6cb7dc314ca8e3380685956acf21030572b2fe26d2e`

```dockerfile
```

-	Layers:
	-	`sha256:83fad1cb4c19e71cbc100ba5c079f7fda458db61bafa47c1cc48e228ce18802f`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 15.3 MB (15286944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4d7f0c7c0907b0c5b392d225150310f20e92d9173b7a16ce384cd7507427f6`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:6cb2cf341137cabc58d05942ca17e31c2c973ee50e2dac8bef4c0edc4e9e21ac
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
$ docker pull rust@sha256:4774472306a1c334734103f7bf6231ad1370d4f71c2ae394fe8978afac5b2e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.8 MB (514821415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63309be2c0345cac77307aa173b9782aa5a84f553951abd498d16f5c04a4fa8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bcbc2151ce4be9aa40b26468719dafd6528d7d11d6f6cb60e3a58a3447305`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 15.6 MB (15558424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36295709cc3855d0f98f8a6b939053cc43efcf3092756703c1fc518d73fe77`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 54.8 MB (54752085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e451f55144f64f697f2945598b3a000bbac10e699d6068b7d6e63f9aa2b7f3b5`  
		Last Modified: Tue, 25 Feb 2025 04:17:48 GMT  
		Size: 197.1 MB (197074397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c39801b95216b4260c69cafb56f78679aec6c847d1e3d1afc1de560c4cd5e9`  
		Last Modified: Mon, 03 Mar 2025 21:14:42 GMT  
		Size: 193.7 MB (193695108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:2ee0d74ac110bd1a17d8332af3912202fbe343a4a38370a9db6bc9fa364b9d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd28e732df28539d58b7d7f26dacd50370d93acc3d43ba5ae570174138f6aec`

```dockerfile
```

-	Layers:
	-	`sha256:b0537ca4f5998de091de7aadced2002bc586c005466354e27181079037c37733`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 15.1 MB (15073413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:323b971a0322980ccb6d5b56d28083ac175e1bd00757315708f1421f1797d01f`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:2ac2d9029c9950551413e86bd26d8ad86f61590dd45bb4cd2da0a4b001432ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.1 MB (512134009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5029ae4b22101f3709c37ae1b0f1483b2f9ff3209787eb6e49ad590cad55da6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b371c05b17ddc4521fa62e27633ef500c9e18d0922c933dc30ad692d163a6adb`  
		Last Modified: Tue, 25 Feb 2025 01:31:01 GMT  
		Size: 49.0 MB (49026733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce7f37fed942ce7eb6947b63b02cebac1a836c49ae19b59c3dfd4d0dafde5e9`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 14.7 MB (14673973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3908d2a88cdaeb59d430f53cffe54008e1006a05c4aa7a391f2dce9c9b9aff8`  
		Last Modified: Tue, 25 Feb 2025 14:18:51 GMT  
		Size: 50.6 MB (50640099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a931f277cb7dadd19c4ea31b7570c91e754bb6d034542896c14a613c77034a3e`  
		Last Modified: Tue, 25 Feb 2025 16:54:04 GMT  
		Size: 167.5 MB (167527903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8016ff31b139f4cc1ac2b37027c3a5c553771198a19e3563f9ebcc51e15f4999`  
		Last Modified: Mon, 03 Mar 2025 21:23:09 GMT  
		Size: 230.3 MB (230265301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0bd6feae8faa96fd3e378eaa561081d1edabb91e202219f3fa32d7468381c067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c7808076946af42d45e2924dc9a57c449d7f6c9539ed7801a920d87def0c75`

```dockerfile
```

-	Layers:
	-	`sha256:afaa1ab536f6764953fbf3d43692672f51fc56aa085586bfb78431ead85f5d36`  
		Last Modified: Mon, 03 Mar 2025 21:23:04 GMT  
		Size: 14.9 MB (14874204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d11f72eaf746d2a6aa73bdc233abd05555878019f6832b3a21234f539567442`  
		Last Modified: Mon, 03 Mar 2025 21:23:03 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5d6e25360f6d028455c8b643f8f53d7c4efbc0064b23759608b61ad6a3adc223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.4 MB (571431917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1371eb80ca3e9f7fe5098765803837081bef8ff5751aecccc695e544f321dec2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364a649b3acc0e2c47a31825e92a687c9eae217b5c8c062f3efaabe7bec06f7`  
		Last Modified: Tue, 25 Feb 2025 05:42:11 GMT  
		Size: 15.5 MB (15544146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8a227b92685cb13561fe06ec9cfa79231e26157c7e163ab5b9af993e63bd10`  
		Last Modified: Tue, 25 Feb 2025 11:54:42 GMT  
		Size: 54.9 MB (54855421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bd61bef017e8e3b4e6f403c074fa47f738d2ac56d92eb50f50fff5dc8bd03`  
		Last Modified: Tue, 25 Feb 2025 15:23:19 GMT  
		Size: 190.0 MB (189986146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0073060607bc719b0aa94e147a0b6b03b6aefcd068fff7a78b8f947eecf9d5`  
		Last Modified: Mon, 03 Mar 2025 21:36:29 GMT  
		Size: 258.8 MB (258797560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7c24d055c4c4a49c2b849357293da9e9e2988140bdd4d982de7271f0e3143c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ebf36916e6fb93d90caf00958262c0c8b9c86735cb8958a061bbc281f3fd85`

```dockerfile
```

-	Layers:
	-	`sha256:493bc9dc75ddde0e35de2091d2eac442ce52714aa89a6f684f07608dbbcc2dea`  
		Last Modified: Mon, 03 Mar 2025 21:36:24 GMT  
		Size: 15.1 MB (15075673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44037f8c5cd51ccebdbaed303063aa1b879764d15ae47c490d35c0fe101c959f`  
		Last Modified: Mon, 03 Mar 2025 21:36:24 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:d96bbc13b6e3f5741b38e2d39e57c378073d01c5cf0f2e18023d0bf7c730098a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.6 MB (537592438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fb3dfd29980bf4e4cf1a785df10f73d2a9093d02a06e3fb1789e2e0670f645`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1763bdfcd7e692c8f35c71602a5206ff9e4716856edf6ae712febb4cc579d3`  
		Last Modified: Tue, 25 Feb 2025 02:24:11 GMT  
		Size: 16.1 MB (16062177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820de11811e966e41fc39b6790cf28a33ce0645127033d9f041fa3707235430e`  
		Last Modified: Tue, 25 Feb 2025 03:13:43 GMT  
		Size: 56.0 MB (56030023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa00228844a300b416d3473480cea8953822058ab89fc86d0c3c4056d2fe123`  
		Last Modified: Tue, 25 Feb 2025 04:18:06 GMT  
		Size: 200.0 MB (199978138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883849d920b1b05e06838787b545a094134ce0719a6b7b9f208333a79ce9a242`  
		Last Modified: Mon, 03 Mar 2025 21:14:43 GMT  
		Size: 210.8 MB (210843237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:16c416c5f5c143b8d3d0444b211b06b0f4ce71c2d44bab44374d6c8e196621f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5baa792f584e43afed942f1cb227670cfbb389df99f48d8914c3676ae81592e`

```dockerfile
```

-	Layers:
	-	`sha256:6a66d8cce735ea8c5513f850111cf3a06be5855d644d3836537665c230246349`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 15.1 MB (15060440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4f74ec7a17331b1624aac92a9d8ebad6de4e7c0902f293d6a7495e63d14e456`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:215987920101ed15967e9ab4bab3a20e1b71ab3c0551b5088b380e0d4e1758b1
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
$ docker pull rust@sha256:d3d93642ae6fd2cd84c7912184bb459b7b0db7e8faac0426bd6dca3940a8e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292709649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f34a203a3c381506722cf3c29ff282ee2a7a6c3ea5f9122a253e5db711f00a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387149dce16056dbdb4b06942bebd598293454f04bcf825305789d3fbd03ccc2`  
		Last Modified: Mon, 03 Mar 2025 21:14:29 GMT  
		Size: 264.5 MB (264490348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:2cadfef9494fded06cb45ac7dd21cf8be95bbc29d29843982b1136d37965399b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b31992db534d2f4beea704cd6f87a532756c8285f835090e85c8f923d989e`

```dockerfile
```

-	Layers:
	-	`sha256:12dde0feb1e98f9767c8a92f79c123cbb093c4e7ae6e7eada09ffdbaa4d28854`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 4.0 MB (3955305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc39115291e4d274b7e0282badf83b093f4dbfb6c01e6213fb4ee57cc1166dc9`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:9b012a9e771ea654d5d5ca13df9b16d30c582cbd91b239a6fac4d1261df41dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302041787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84120db8ea77fcfa8688c3eff9973638aa867fa532f1e31f8c14ab72b3a64581`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d5d06d813118d1b82098ef607f6a62da0ee850225501b423d07dfd2711d755`  
		Last Modified: Mon, 03 Mar 2025 21:15:00 GMT  
		Size: 278.1 MB (278122053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:c9bd5c78945d857d38fe8fa1ac884fe625c77e20599616076ad6721182c2f9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e04d921f393c225935b32033dca57f0e95c593bc7adb10b09f97d690f21a8e4`

```dockerfile
```

-	Layers:
	-	`sha256:6814569f1e5d4ef57f4bea7482e085eb9fb50e1857c3855319e7648690f598ae`  
		Last Modified: Mon, 03 Mar 2025 21:14:54 GMT  
		Size: 3.8 MB (3771368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86dd27a840b3d8ec5e099dd6964b60024cf9d327bb8bc7ecae0b35a82d999080`  
		Last Modified: Mon, 03 Mar 2025 21:14:53 GMT  
		Size: 13.4 KB (13378 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2592404bc1c86ee8445a2102a9a6927ac6f91aaa8821a4ff764884ac7984094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352689188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379c3debf1acbd8228d0dac86005b4fe2aa9dae005b2e1d825e5c1462322dd7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51868c8eb2680ac4209dae1f73861b9c082564efc6f5a6b39e39ac0d7d6ff6b5`  
		Last Modified: Mon, 03 Mar 2025 21:29:50 GMT  
		Size: 324.6 MB (324640763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:1e31d6a2695c5af40509bfd2eb1d961a0fb7988b0c1f26bff5d8f6e61c418412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52299a9631b27c74dd842e31aa7e0da8e26a849b4a815ba25015741e88c0ae46`

```dockerfile
```

-	Layers:
	-	`sha256:f273ab084a2e7575d05d06fa8ba8cf7e2d8f8da05b88269989a9ddde03493037`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 4.0 MB (3977648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b19592b0bba92266591738d7b34e3def4520d60096b6a10a024f01b3bedd90e`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:88ba2b4761e6d4257c7060aae566853aca592df9e026d748f161b37fb1c2764b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307630505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35b195ee846be85652a54550356ce979af10471acbd66a58ac492de03315688`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a89d68e962de64b429c772557a0e0a429dc425b2a14dcb31802e63de2e4e6bd`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 278.4 MB (278435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b3a7a9e30f6b551540715acbe44f408f539191ad77cc92d3276a74e91dfe0fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed2d74491588bf1f3886ac5c1ba7ef38f7f513a0298f405327e9be21f7af5da`

```dockerfile
```

-	Layers:
	-	`sha256:f2761352b9bb345b81ef703154b559b8e013093b8599a35ed94fdefb3c7327aa`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 3.9 MB (3935220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bacf9a7e03faf1ff9bf9fbd5138346c494c6f27d2ca9c99b3e3b0f5e79c2fe71`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:d17f48a04c1c202eb18025d892fddf578cedbdc537fa56a041db85189882ab6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355168893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8c917d31b3a645483187dd86afa887442274f948403c6ba0cb7530982f308f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a5a9edf391ebe6e786c0c06eb206b9f00800b0262e795ed3ae7f7a0618588f`  
		Last Modified: Mon, 03 Mar 2025 21:16:50 GMT  
		Size: 323.1 MB (323116579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:77418e4a89328c9c95965a089ff40eb2c4ae1bf5bece9a92578f48b38d198a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce5ae98dec6ba000aab82460ddc24921096bc35a28c42968b20cbe7a9b19d05`

```dockerfile
```

-	Layers:
	-	`sha256:9fc9db7381e23b41c20dcc2dea87608b0cf0c9091ea543bafb588a1cbb532d21`  
		Last Modified: Mon, 03 Mar 2025 21:16:33 GMT  
		Size: 3.9 MB (3927866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6eb443440c8ecf14e727b7761eed1b229ee61670c0190619f7a21685eb501b`  
		Last Modified: Mon, 03 Mar 2025 21:16:32 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:5703e183e49c0e1dc763e6bdbe2c9bac4d8b652267f0bb85718f9e1c359f1b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358827701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d0faf0f8207be9497615f4b7573829e4fc8b2977f1a06d02e4b28d030c1d41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078929da424ac5687fa6c367c58665828a7d802e10e816e2ae05060d62a114e9`  
		Last Modified: Mon, 03 Mar 2025 21:15:44 GMT  
		Size: 332.0 MB (331962863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:22316782835c59c254cf08a9f94d0fbf9c7d97933beeca3f7be35411f06e5640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40c95061e80226561af8a4a6448bc3128287baf27bd094ecbb1af08b0ca6d00`

```dockerfile
```

-	Layers:
	-	`sha256:db5d3a28f1d73244b43980f7869840e4d6b6a7e6815101a9c53f1f060eb04089`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 3.8 MB (3797205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f1036a2309ba1a573101a8d36570d74e90b4a1095fdd22f30435cae8bfa61e`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:215987920101ed15967e9ab4bab3a20e1b71ab3c0551b5088b380e0d4e1758b1
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
$ docker pull rust@sha256:d3d93642ae6fd2cd84c7912184bb459b7b0db7e8faac0426bd6dca3940a8e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292709649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f34a203a3c381506722cf3c29ff282ee2a7a6c3ea5f9122a253e5db711f00a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387149dce16056dbdb4b06942bebd598293454f04bcf825305789d3fbd03ccc2`  
		Last Modified: Mon, 03 Mar 2025 21:14:29 GMT  
		Size: 264.5 MB (264490348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2cadfef9494fded06cb45ac7dd21cf8be95bbc29d29843982b1136d37965399b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b31992db534d2f4beea704cd6f87a532756c8285f835090e85c8f923d989e`

```dockerfile
```

-	Layers:
	-	`sha256:12dde0feb1e98f9767c8a92f79c123cbb093c4e7ae6e7eada09ffdbaa4d28854`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 4.0 MB (3955305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc39115291e4d274b7e0282badf83b093f4dbfb6c01e6213fb4ee57cc1166dc9`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:9b012a9e771ea654d5d5ca13df9b16d30c582cbd91b239a6fac4d1261df41dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302041787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84120db8ea77fcfa8688c3eff9973638aa867fa532f1e31f8c14ab72b3a64581`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d5d06d813118d1b82098ef607f6a62da0ee850225501b423d07dfd2711d755`  
		Last Modified: Mon, 03 Mar 2025 21:15:00 GMT  
		Size: 278.1 MB (278122053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c9bd5c78945d857d38fe8fa1ac884fe625c77e20599616076ad6721182c2f9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e04d921f393c225935b32033dca57f0e95c593bc7adb10b09f97d690f21a8e4`

```dockerfile
```

-	Layers:
	-	`sha256:6814569f1e5d4ef57f4bea7482e085eb9fb50e1857c3855319e7648690f598ae`  
		Last Modified: Mon, 03 Mar 2025 21:14:54 GMT  
		Size: 3.8 MB (3771368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86dd27a840b3d8ec5e099dd6964b60024cf9d327bb8bc7ecae0b35a82d999080`  
		Last Modified: Mon, 03 Mar 2025 21:14:53 GMT  
		Size: 13.4 KB (13378 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2592404bc1c86ee8445a2102a9a6927ac6f91aaa8821a4ff764884ac7984094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352689188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379c3debf1acbd8228d0dac86005b4fe2aa9dae005b2e1d825e5c1462322dd7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51868c8eb2680ac4209dae1f73861b9c082564efc6f5a6b39e39ac0d7d6ff6b5`  
		Last Modified: Mon, 03 Mar 2025 21:29:50 GMT  
		Size: 324.6 MB (324640763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1e31d6a2695c5af40509bfd2eb1d961a0fb7988b0c1f26bff5d8f6e61c418412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52299a9631b27c74dd842e31aa7e0da8e26a849b4a815ba25015741e88c0ae46`

```dockerfile
```

-	Layers:
	-	`sha256:f273ab084a2e7575d05d06fa8ba8cf7e2d8f8da05b88269989a9ddde03493037`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 4.0 MB (3977648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b19592b0bba92266591738d7b34e3def4520d60096b6a10a024f01b3bedd90e`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:88ba2b4761e6d4257c7060aae566853aca592df9e026d748f161b37fb1c2764b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307630505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35b195ee846be85652a54550356ce979af10471acbd66a58ac492de03315688`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a89d68e962de64b429c772557a0e0a429dc425b2a14dcb31802e63de2e4e6bd`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 278.4 MB (278435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b3a7a9e30f6b551540715acbe44f408f539191ad77cc92d3276a74e91dfe0fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed2d74491588bf1f3886ac5c1ba7ef38f7f513a0298f405327e9be21f7af5da`

```dockerfile
```

-	Layers:
	-	`sha256:f2761352b9bb345b81ef703154b559b8e013093b8599a35ed94fdefb3c7327aa`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 3.9 MB (3935220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bacf9a7e03faf1ff9bf9fbd5138346c494c6f27d2ca9c99b3e3b0f5e79c2fe71`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d17f48a04c1c202eb18025d892fddf578cedbdc537fa56a041db85189882ab6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355168893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8c917d31b3a645483187dd86afa887442274f948403c6ba0cb7530982f308f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a5a9edf391ebe6e786c0c06eb206b9f00800b0262e795ed3ae7f7a0618588f`  
		Last Modified: Mon, 03 Mar 2025 21:16:50 GMT  
		Size: 323.1 MB (323116579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:77418e4a89328c9c95965a089ff40eb2c4ae1bf5bece9a92578f48b38d198a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce5ae98dec6ba000aab82460ddc24921096bc35a28c42968b20cbe7a9b19d05`

```dockerfile
```

-	Layers:
	-	`sha256:9fc9db7381e23b41c20dcc2dea87608b0cf0c9091ea543bafb588a1cbb532d21`  
		Last Modified: Mon, 03 Mar 2025 21:16:33 GMT  
		Size: 3.9 MB (3927866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6eb443440c8ecf14e727b7761eed1b229ee61670c0190619f7a21685eb501b`  
		Last Modified: Mon, 03 Mar 2025 21:16:32 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:5703e183e49c0e1dc763e6bdbe2c9bac4d8b652267f0bb85718f9e1c359f1b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358827701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d0faf0f8207be9497615f4b7573829e4fc8b2977f1a06d02e4b28d030c1d41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078929da424ac5687fa6c367c58665828a7d802e10e816e2ae05060d62a114e9`  
		Last Modified: Mon, 03 Mar 2025 21:15:44 GMT  
		Size: 332.0 MB (331962863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:22316782835c59c254cf08a9f94d0fbf9c7d97933beeca3f7be35411f06e5640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40c95061e80226561af8a4a6448bc3128287baf27bd094ecbb1af08b0ca6d00`

```dockerfile
```

-	Layers:
	-	`sha256:db5d3a28f1d73244b43980f7869840e4d6b6a7e6815101a9c53f1f060eb04089`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 3.8 MB (3797205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f1036a2309ba1a573101a8d36570d74e90b4a1095fdd22f30435cae8bfa61e`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:e94e2d2e0a9df48fdfcacb47d8b60d036abe60b7c6fa3ac3de1dd16a3d18f19a
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
$ docker pull rust@sha256:dccdc77b5b046c078e76f4ca452308e213f4b7ba3e8a6c215393381d36d5b280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283883304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35d2ada2c353b98b46aff96c86cc0c21d362da854c48fcd0aa754b13b83eb20`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e0052749e7f2c9ab3a91aad47ad13df4c7c8911c162e2bdb7d08f691e99aac`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 253.6 MB (253629374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:19d324bd0c298ad1b3f5e6df1ce1df18225864b216efbb6c90ddce0a8ce24642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c80060630492f3b3f74f9d388000b5067bc23694bacc999541e6da57bf59ff`

```dockerfile
```

-	Layers:
	-	`sha256:df56ae19c38d79a9c6b3901f1921d9c3833a93218a082679bdb0a12883f3905e`  
		Last Modified: Mon, 03 Mar 2025 21:14:22 GMT  
		Size: 4.2 MB (4173204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9fc1edc1c95e2a303e127182409fafb9fc9e2d3f3ad0da80b896cad7720daaa`  
		Last Modified: Mon, 03 Mar 2025 21:14:21 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:1c291529dbe66cd22592a3d8ecc5cead222cb64a3d43b8aaadfa065746e28570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297882666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e350660ab01bd40fd4abffb3fd8ba3d377659d12c689daca3b6779053172617`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0ca501b624d9dae81049df15e1024733ee21141b25f8ca123d98e0d13df5d12`  
		Last Modified: Tue, 25 Feb 2025 01:31:18 GMT  
		Size: 25.5 MB (25535432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6d72cafe6043b15f5dabf082f52f18a84a9ac04dfbfe5fc6bba3fcbe37edd0`  
		Last Modified: Mon, 03 Mar 2025 21:20:57 GMT  
		Size: 272.3 MB (272347234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:07cd7090e5192facfdd11a8b0ed54d90c6c4f804c8c9a9059c3d3e7ba657c970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612130ff6bdfd39ede8255ddb232e9327ffb825112e6bb1017c80060be9e9c7d`

```dockerfile
```

-	Layers:
	-	`sha256:73bc2806f7ecf2f20576c7878e9d5e9b7dfc3b25b6132689e08490bce610f038`  
		Last Modified: Mon, 03 Mar 2025 21:20:39 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f927f926449a4f38eeebab517940bd75ca9acef94ae1a163391730411486b20`  
		Last Modified: Mon, 03 Mar 2025 21:20:38 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:de9c5b13bcc43221f1603fb03089d27e59603e8087525be9302e30fa4a75e3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343069561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e422222ab9bba42554ec25e8f7656f35c48de3d1930f29223b4c40648547e500`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ae7537677409c7e96b2e534829fe706743a9e1c1fc79c0e6c3a6ae631021d1`  
		Last Modified: Mon, 03 Mar 2025 21:34:48 GMT  
		Size: 314.3 MB (314323574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:cb9b665a79ff9d7407b5196e20d85e27ec9c2216b78c66b5a1dfa4a438542750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b594182c132405732dc65dec31b847e10c0314703f603d9728caf021dd2f8c3`

```dockerfile
```

-	Layers:
	-	`sha256:f87a9a1c38fe1dae028e9162ed79be83deebf92138b807780b636247a977d593`  
		Last Modified: Mon, 03 Mar 2025 21:34:40 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0c9191b26a4828e5bd697af4e870ad8de930043587eddf2407e36a5f19df4ea`  
		Last Modified: Mon, 03 Mar 2025 21:34:40 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:8ce46ac85186e75d85f9912eaea882d8fab038755ad48d921a2974b006f800a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302583357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66df80913375cbd40ebb9b025095b1856d1454a6206427f78c4846d5b5771158`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc6ac53dd3c2cb0c6fd992e5925fc15a335691c21c9dc26765ed22ae0d20371`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 271.4 MB (271402930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e925605333c9a3842c68db47ba3d21c3ba0539ccbf18a0231b3a8cfacca912b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55c2e9da4484fa31efbf5cc3c8d14b787bc24da1ef1871ff26f4e0ac811f26d`

```dockerfile
```

-	Layers:
	-	`sha256:d0d87fc423e5c2445348c3696ac9ef20a4fae6bfa1ceebb2a4a2a6b7af161b60`  
		Last Modified: Mon, 03 Mar 2025 21:14:33 GMT  
		Size: 4.2 MB (4163461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714de8d934c25f3276ae4b994be3302532085a4c69860853de35ef86540dd876`  
		Last Modified: Mon, 03 Mar 2025 21:14:33 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85`

```console
$ docker pull rust@sha256:e15c642b487dd013b2e425d001d32927391aca787ac582b98cca72234d466b60
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

### `rust:1.85` - linux; amd64

```console
$ docker pull rust@sha256:f6fc45b5a8d3b72dcff6442b5311f0b1f854a3480797f91ecbfb16c0fd5d4527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.0 MB (541963415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aac1c9ca934dcc8a2f93033651d5f86fb3b99783c81428ecce40198d4abc0af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c03d5625da4fd65f189b350dab8fda9ce3054bdd41f9a509973b3cd0cd571e`  
		Last Modified: Mon, 03 Mar 2025 21:14:28 GMT  
		Size: 193.7 MB (193695926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85` - unknown; unknown

```console
$ docker pull rust@sha256:4d1be75651ae6516c73cd01fb804f023e4d53bdf2b9d5cb9e5a78381266818c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca03f69ea0d5d937b5bf2bba4b75d5a4cb308e7460975b526f3138436e1a7f7b`

```dockerfile
```

-	Layers:
	-	`sha256:f2aa5e71de5c6e138f09eb61c0c64219101f7290d0719c4e4f2763b9cbbcafa9`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 15.5 MB (15474256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bfe55c7c856b4e205d1086d7f00a0c16d9544ceb0316ec5f5368e8f86a5a815`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85` - linux; arm variant v7

```console
$ docker pull rust@sha256:cb81fdf6321d7de7b04a0978a0f1af3d2ce2e9b5302a619b7d538132a0d783bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531318143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cba7271ee5cf51b3565fbb44d531aa336955fdf97d4159e8544e9e1ede35187`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70e25650a3be5d12fed3dfd4069f605d42d17b86fa4c689b69aa636aee22155`  
		Last Modified: Mon, 03 Mar 2025 21:18:08 GMT  
		Size: 230.3 MB (230264903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85` - unknown; unknown

```console
$ docker pull rust@sha256:c6712addcc809b8eb0fe21d81f7f7eba0637e2838086b119dcbbc41e4187a6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e9006d373cfef0bc4e89bb17079c2f22f1ae42ed8a2b7dcd57d4b3c67b04c9`

```dockerfile
```

-	Layers:
	-	`sha256:fab2c1c1f543fac09d7660a2054a25708a28b23b14e1f1c9a3a6e1644e54b678`  
		Last Modified: Mon, 03 Mar 2025 21:18:02 GMT  
		Size: 15.3 MB (15278698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f349b53969dfbfa675b8173f92a74dbd59458f6214685c9dd2c7318179f6cc32`  
		Last Modified: Mon, 03 Mar 2025 21:18:01 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be252dc02478902ea4c4a6e1e2b49181f1fa3aaeb96a47e40dc248b2598cf243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.8 MB (597772744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192cc1afeb41abe7df5d2c3f94eb7e40a991156c86412ad4cab156f754d7f291`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b5a4332d3d01f663d9e0b5d8a153c25ca20c2d7e94ce224b627a88380da001`  
		Last Modified: Mon, 03 Mar 2025 21:31:31 GMT  
		Size: 258.8 MB (258797571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85` - unknown; unknown

```console
$ docker pull rust@sha256:0cea832fdaaa30a9c04e35a4d5de0ede3f8723564efacebd2cae817dba8af26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef22842e59d31eab71173da3ae37fbcabd9b445839c9e49ffa7b0d93c64a8f51`

```dockerfile
```

-	Layers:
	-	`sha256:463dc9b45f12289d11de3d7eaffa14e7641471dd399b68728748be80a572fea3`  
		Last Modified: Mon, 03 Mar 2025 21:31:25 GMT  
		Size: 15.5 MB (15502831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:479aac264bc9d5563cda8973c1adf5fcc9d667f916488c189c512d2bb1d18d12`  
		Last Modified: Mon, 03 Mar 2025 21:31:24 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85` - linux; 386

```console
$ docker pull rust@sha256:c3ba8ba76e08440fcff73d04693fef720530890076f46b8761da0dddcedadb78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.7 MB (561694245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676197b0baccfd7dd45db61469de196ac15950aa10debfbcd2b0583af2dafed4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca163299b0e606d2916a03bd0f60c5903c6e5abeab65da3a8c490174697c929`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 24.9 MB (24899353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c3400be327e90dc9e848a16d4b0fcd191708de152e68c6b4888d83c61f441`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 66.2 MB (66237814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3ca8ca718f538c2871c3deeec438c611f0f26a3b97976b89d6d6abcca894dd`  
		Last Modified: Tue, 25 Feb 2025 05:12:06 GMT  
		Size: 210.3 MB (210255482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c5735fe88e109ded1d53e0e079c60705e16af5652ea6c119760594e52d6fb`  
		Last Modified: Mon, 03 Mar 2025 21:14:43 GMT  
		Size: 210.8 MB (210843144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85` - unknown; unknown

```console
$ docker pull rust@sha256:8c10ae28c24f12a5b3e3598c4abb8a26206a7edef522211dc27667c598621f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5c3c563ea6d86b133dd81fc4d8eaecefc99bc076f1c075059797e8116f36d3`

```dockerfile
```

-	Layers:
	-	`sha256:0ab28f08ca6a412da7f3016c8c2eb5dc331d3000a50c38114eb87924f817b53a`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 15.5 MB (15451518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd3c3e28ee8144d301f821eb5b432e99ec8f8776af706e07ba3a04d48e6f7ac`  
		Last Modified: Mon, 03 Mar 2025 21:14:37 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85` - linux; ppc64le

```console
$ docker pull rust@sha256:0fe5e17dc44d5fdbd2560266262d98e813b49ca1e9b0ba23d9b3675fe2adacb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.6 MB (616586281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d35305b8c7077eb68baa8b585fec750d11f2afc7094e64b59f8e368246879`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad13c90d099a380a8fc2ec9ef74de7ad957b1496d75b8d1c4617069765510053`  
		Last Modified: Mon, 03 Mar 2025 21:24:43 GMT  
		Size: 254.3 MB (254345476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85` - unknown; unknown

```console
$ docker pull rust@sha256:0676ad8c84ebbb134f5e3c3aab74a661c1ac924ee0fa1a042d90d7fbadfc4585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ad946c6e11f49c09021728047cc0f3fa4a83f0101fa1031085c8f8e0d2ca1c`

```dockerfile
```

-	Layers:
	-	`sha256:14a5009de22d0268d16a06051e63b1bd4e5a83615d08555e021663ada543f0e2`  
		Last Modified: Mon, 03 Mar 2025 21:24:31 GMT  
		Size: 15.4 MB (15449362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e237236a91844fef1f239951791ab5549d6226f7a182592fa6867fc48d952279`  
		Last Modified: Mon, 03 Mar 2025 21:24:28 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85` - linux; s390x

```console
$ docker pull rust@sha256:70fe5668b3762d8a81b5059f9c4bad31ac92bf152d57195193c433368ec36f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599864262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b0dc30045f5d2e53b0a2a92cd31f6f8e3bdeca4ccb1165d6d2ac3cdcf807a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f679165548785dd187eaea9af4ee69db5b37630f35ce564d064cd7512fcfb9`  
		Last Modified: Mon, 03 Mar 2025 21:31:35 GMT  
		Size: 281.8 MB (281820436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85` - unknown; unknown

```console
$ docker pull rust@sha256:dbf40b3fd37699736f3445354654c43b50a382b3ef92f0ea8de4366bcc1af9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d288575d5989682a9df5b6cb7dc314ca8e3380685956acf21030572b2fe26d2e`

```dockerfile
```

-	Layers:
	-	`sha256:83fad1cb4c19e71cbc100ba5c079f7fda458db61bafa47c1cc48e228ce18802f`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 15.3 MB (15286944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4d7f0c7c0907b0c5b392d225150310f20e92d9173b7a16ce384cd7507427f6`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85-alpine`

```console
$ docker pull rust@sha256:1030547bd568497d69e41771ada279179f0613369dc54779e46a3f6f376b3020
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.85-alpine` - linux; amd64

```console
$ docker pull rust@sha256:84b5e9c7c2f9437f62769913b419cc02a1e310bf40fd86720cd2b3b64bffb452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304368783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec94ecf18f99333d5bd8f2a15427ba1b4736299f4d5f4a35660f5fe75b6291a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b95e11be61c0eea8aadf788692bf0fcec5f9c75738d3f5713dfbcc016f337f4`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 61.6 MB (61565003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6fc4d476520099dcd8ba0f71c1e15bb2d762c9977506070eea6cb78a2a4c6`  
		Last Modified: Mon, 03 Mar 2025 21:14:31 GMT  
		Size: 239.2 MB (239161533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:d8cff90939ad06ca11df0fc881253dc5d1d768c2221f8466415334d2739cbfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4955895d71a1f61c0886f29ea5b6a23986cda0a9910e8ba13ff472aff21cac1f`

```dockerfile
```

-	Layers:
	-	`sha256:fd7a8c7ea021f7804add54b5f5efd33149b2e2c7d915f1622744e64dbbe08c7c`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457f860b4e4d19a0674d0ca4f6ec06ff6958c351407559ee9c974d2b3bbca63f`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bda9e5682eeb0013c19b06e469812ae54cbe76cf0128796def8eb9bfe30a5c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307415047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72195abfac34db128f0c99e35ad0a1a98210b81274e98b65ac2973dae8aeb0dd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b46568d489c620031542c16213dea9e63b74c664a11f85b1bb86a8e526e5a16`  
		Last Modified: Mon, 03 Mar 2025 21:23:23 GMT  
		Size: 59.1 MB (59101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51de9687e383104ad782ecb8afe38b4c33220f4e646112f07f0e47d399d0a9fd`  
		Last Modified: Mon, 03 Mar 2025 21:23:28 GMT  
		Size: 244.3 MB (244320886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:429bfdee3cf71b49563ad904faf2875e578ae734980bd44b1c38b27f5855fd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d07c59fd4b9553baf3c76bd773969e82fed14c0dcfa7ca467660406d07156`

```dockerfile
```

-	Layers:
	-	`sha256:fbed74b3e0b30a9432fe2ba4b82f04cb881dd5c6f374c1aff1f3d2f2018fb7f3`  
		Last Modified: Mon, 03 Mar 2025 21:23:22 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81eca9cb1582aed143c4d744ce7a925b1e10e4678aaf0916e76d40846bb2d61`  
		Last Modified: Mon, 03 Mar 2025 21:23:21 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85-alpine3.20`

```console
$ docker pull rust@sha256:f0cef6c65992995b1c7816cb667de95799852e3fbed9d06f95855cbc512a0fd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.85-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:6d824fef86a8532aecead5889d49d432d19e0dd58b958266c994cca9eb7a3357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298102813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c38e59fb99c1014ea6d250d396bb9bf55981f1d69fe17ed05047b90cd119ca9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0430b4a2b30329b0c06034d1df61c2f3533c436834a54b76def8756d804d888`  
		Last Modified: Mon, 03 Mar 2025 21:17:28 GMT  
		Size: 55.3 MB (55315558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fda7dd06f6e434e3727cd86155430a51568846533e3824548334e20f1078e28`  
		Last Modified: Mon, 03 Mar 2025 21:17:31 GMT  
		Size: 239.2 MB (239160358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:ab2a41c3a86b0e8de97e1cff7ca3624a6e69e478c7c29615df5979d5655d03c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e987a7ec625942a721de02dcd92bf4ea3f7481ee651c6aef639e3a2f3f16ba`

```dockerfile
```

-	Layers:
	-	`sha256:4100e90a822ec6152c54ec22e8ce0b4cfb24694b82b0d9252e191958ce4d59cf`  
		Last Modified: Mon, 03 Mar 2025 21:17:28 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca3c1b9b1144fd4038e19dea5e9afef77e4732804442cc1813ffcbd1c7289e4`  
		Last Modified: Mon, 03 Mar 2025 21:17:27 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f91c5c68a69111314bb721b7bb75aaa4b310b9ef676f2591e88769bbbb3bd933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301363171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61566cb96efc54b3ee29f6409c0e76059ca7b3c261b99a2940c188c54c3a66c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c8bee9c91c68545cb9604a6baaf13f4c921f1a8a851437cc7ce63f942e113d`  
		Last Modified: Mon, 03 Mar 2025 21:26:24 GMT  
		Size: 53.0 MB (52950488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998e7300919f154807a1ce8bdaa868228719c39a95b4c276a758f1bf480b361`  
		Last Modified: Mon, 03 Mar 2025 21:26:28 GMT  
		Size: 244.3 MB (244321518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1e4651facc4a66b01c40f8bec063469f936cbf603daf477c1003e794040d3e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beeb6c0426bb32cbdd133d31ad5ed10820561b72d66e1d95f332bfb42d012779`

```dockerfile
```

-	Layers:
	-	`sha256:183ceb0143fb3784d416af0d9e6e49059191e33606b5db6d715b5666f0fd139b`  
		Last Modified: Mon, 03 Mar 2025 21:26:22 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe75a1adc68e5615e04f2ea23b7e198a996bb1378319d115d5ca7b6fbef7602`  
		Last Modified: Mon, 03 Mar 2025 21:26:22 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85-alpine3.21`

```console
$ docker pull rust@sha256:1030547bd568497d69e41771ada279179f0613369dc54779e46a3f6f376b3020
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.85-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:84b5e9c7c2f9437f62769913b419cc02a1e310bf40fd86720cd2b3b64bffb452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304368783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec94ecf18f99333d5bd8f2a15427ba1b4736299f4d5f4a35660f5fe75b6291a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b95e11be61c0eea8aadf788692bf0fcec5f9c75738d3f5713dfbcc016f337f4`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 61.6 MB (61565003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6fc4d476520099dcd8ba0f71c1e15bb2d762c9977506070eea6cb78a2a4c6`  
		Last Modified: Mon, 03 Mar 2025 21:14:31 GMT  
		Size: 239.2 MB (239161533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:d8cff90939ad06ca11df0fc881253dc5d1d768c2221f8466415334d2739cbfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4955895d71a1f61c0886f29ea5b6a23986cda0a9910e8ba13ff472aff21cac1f`

```dockerfile
```

-	Layers:
	-	`sha256:fd7a8c7ea021f7804add54b5f5efd33149b2e2c7d915f1622744e64dbbe08c7c`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457f860b4e4d19a0674d0ca4f6ec06ff6958c351407559ee9c974d2b3bbca63f`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bda9e5682eeb0013c19b06e469812ae54cbe76cf0128796def8eb9bfe30a5c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307415047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72195abfac34db128f0c99e35ad0a1a98210b81274e98b65ac2973dae8aeb0dd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b46568d489c620031542c16213dea9e63b74c664a11f85b1bb86a8e526e5a16`  
		Last Modified: Mon, 03 Mar 2025 21:23:23 GMT  
		Size: 59.1 MB (59101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51de9687e383104ad782ecb8afe38b4c33220f4e646112f07f0e47d399d0a9fd`  
		Last Modified: Mon, 03 Mar 2025 21:23:28 GMT  
		Size: 244.3 MB (244320886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:429bfdee3cf71b49563ad904faf2875e578ae734980bd44b1c38b27f5855fd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d07c59fd4b9553baf3c76bd773969e82fed14c0dcfa7ca467660406d07156`

```dockerfile
```

-	Layers:
	-	`sha256:fbed74b3e0b30a9432fe2ba4b82f04cb881dd5c6f374c1aff1f3d2f2018fb7f3`  
		Last Modified: Mon, 03 Mar 2025 21:23:22 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81eca9cb1582aed143c4d744ce7a925b1e10e4678aaf0916e76d40846bb2d61`  
		Last Modified: Mon, 03 Mar 2025 21:23:21 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85-bookworm`

```console
$ docker pull rust@sha256:e15c642b487dd013b2e425d001d32927391aca787ac582b98cca72234d466b60
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

### `rust:1.85-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:f6fc45b5a8d3b72dcff6442b5311f0b1f854a3480797f91ecbfb16c0fd5d4527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.0 MB (541963415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aac1c9ca934dcc8a2f93033651d5f86fb3b99783c81428ecce40198d4abc0af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c03d5625da4fd65f189b350dab8fda9ce3054bdd41f9a509973b3cd0cd571e`  
		Last Modified: Mon, 03 Mar 2025 21:14:28 GMT  
		Size: 193.7 MB (193695926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4d1be75651ae6516c73cd01fb804f023e4d53bdf2b9d5cb9e5a78381266818c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca03f69ea0d5d937b5bf2bba4b75d5a4cb308e7460975b526f3138436e1a7f7b`

```dockerfile
```

-	Layers:
	-	`sha256:f2aa5e71de5c6e138f09eb61c0c64219101f7290d0719c4e4f2763b9cbbcafa9`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 15.5 MB (15474256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bfe55c7c856b4e205d1086d7f00a0c16d9544ceb0316ec5f5368e8f86a5a815`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:cb81fdf6321d7de7b04a0978a0f1af3d2ce2e9b5302a619b7d538132a0d783bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531318143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cba7271ee5cf51b3565fbb44d531aa336955fdf97d4159e8544e9e1ede35187`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70e25650a3be5d12fed3dfd4069f605d42d17b86fa4c689b69aa636aee22155`  
		Last Modified: Mon, 03 Mar 2025 21:18:08 GMT  
		Size: 230.3 MB (230264903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c6712addcc809b8eb0fe21d81f7f7eba0637e2838086b119dcbbc41e4187a6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e9006d373cfef0bc4e89bb17079c2f22f1ae42ed8a2b7dcd57d4b3c67b04c9`

```dockerfile
```

-	Layers:
	-	`sha256:fab2c1c1f543fac09d7660a2054a25708a28b23b14e1f1c9a3a6e1644e54b678`  
		Last Modified: Mon, 03 Mar 2025 21:18:02 GMT  
		Size: 15.3 MB (15278698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f349b53969dfbfa675b8173f92a74dbd59458f6214685c9dd2c7318179f6cc32`  
		Last Modified: Mon, 03 Mar 2025 21:18:01 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be252dc02478902ea4c4a6e1e2b49181f1fa3aaeb96a47e40dc248b2598cf243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.8 MB (597772744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192cc1afeb41abe7df5d2c3f94eb7e40a991156c86412ad4cab156f754d7f291`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b5a4332d3d01f663d9e0b5d8a153c25ca20c2d7e94ce224b627a88380da001`  
		Last Modified: Mon, 03 Mar 2025 21:31:31 GMT  
		Size: 258.8 MB (258797571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0cea832fdaaa30a9c04e35a4d5de0ede3f8723564efacebd2cae817dba8af26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef22842e59d31eab71173da3ae37fbcabd9b445839c9e49ffa7b0d93c64a8f51`

```dockerfile
```

-	Layers:
	-	`sha256:463dc9b45f12289d11de3d7eaffa14e7641471dd399b68728748be80a572fea3`  
		Last Modified: Mon, 03 Mar 2025 21:31:25 GMT  
		Size: 15.5 MB (15502831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:479aac264bc9d5563cda8973c1adf5fcc9d667f916488c189c512d2bb1d18d12`  
		Last Modified: Mon, 03 Mar 2025 21:31:24 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-bookworm` - linux; 386

```console
$ docker pull rust@sha256:c3ba8ba76e08440fcff73d04693fef720530890076f46b8761da0dddcedadb78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.7 MB (561694245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676197b0baccfd7dd45db61469de196ac15950aa10debfbcd2b0583af2dafed4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca163299b0e606d2916a03bd0f60c5903c6e5abeab65da3a8c490174697c929`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 24.9 MB (24899353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c3400be327e90dc9e848a16d4b0fcd191708de152e68c6b4888d83c61f441`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 66.2 MB (66237814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3ca8ca718f538c2871c3deeec438c611f0f26a3b97976b89d6d6abcca894dd`  
		Last Modified: Tue, 25 Feb 2025 05:12:06 GMT  
		Size: 210.3 MB (210255482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c5735fe88e109ded1d53e0e079c60705e16af5652ea6c119760594e52d6fb`  
		Last Modified: Mon, 03 Mar 2025 21:14:43 GMT  
		Size: 210.8 MB (210843144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8c10ae28c24f12a5b3e3598c4abb8a26206a7edef522211dc27667c598621f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5c3c563ea6d86b133dd81fc4d8eaecefc99bc076f1c075059797e8116f36d3`

```dockerfile
```

-	Layers:
	-	`sha256:0ab28f08ca6a412da7f3016c8c2eb5dc331d3000a50c38114eb87924f817b53a`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 15.5 MB (15451518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd3c3e28ee8144d301f821eb5b432e99ec8f8776af706e07ba3a04d48e6f7ac`  
		Last Modified: Mon, 03 Mar 2025 21:14:37 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:0fe5e17dc44d5fdbd2560266262d98e813b49ca1e9b0ba23d9b3675fe2adacb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.6 MB (616586281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d35305b8c7077eb68baa8b585fec750d11f2afc7094e64b59f8e368246879`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad13c90d099a380a8fc2ec9ef74de7ad957b1496d75b8d1c4617069765510053`  
		Last Modified: Mon, 03 Mar 2025 21:24:43 GMT  
		Size: 254.3 MB (254345476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0676ad8c84ebbb134f5e3c3aab74a661c1ac924ee0fa1a042d90d7fbadfc4585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ad946c6e11f49c09021728047cc0f3fa4a83f0101fa1031085c8f8e0d2ca1c`

```dockerfile
```

-	Layers:
	-	`sha256:14a5009de22d0268d16a06051e63b1bd4e5a83615d08555e021663ada543f0e2`  
		Last Modified: Mon, 03 Mar 2025 21:24:31 GMT  
		Size: 15.4 MB (15449362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e237236a91844fef1f239951791ab5549d6226f7a182592fa6867fc48d952279`  
		Last Modified: Mon, 03 Mar 2025 21:24:28 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:70fe5668b3762d8a81b5059f9c4bad31ac92bf152d57195193c433368ec36f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599864262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b0dc30045f5d2e53b0a2a92cd31f6f8e3bdeca4ccb1165d6d2ac3cdcf807a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f679165548785dd187eaea9af4ee69db5b37630f35ce564d064cd7512fcfb9`  
		Last Modified: Mon, 03 Mar 2025 21:31:35 GMT  
		Size: 281.8 MB (281820436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:dbf40b3fd37699736f3445354654c43b50a382b3ef92f0ea8de4366bcc1af9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d288575d5989682a9df5b6cb7dc314ca8e3380685956acf21030572b2fe26d2e`

```dockerfile
```

-	Layers:
	-	`sha256:83fad1cb4c19e71cbc100ba5c079f7fda458db61bafa47c1cc48e228ce18802f`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 15.3 MB (15286944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4d7f0c7c0907b0c5b392d225150310f20e92d9173b7a16ce384cd7507427f6`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85-bullseye`

```console
$ docker pull rust@sha256:6cb2cf341137cabc58d05942ca17e31c2c973ee50e2dac8bef4c0edc4e9e21ac
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

### `rust:1.85-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:4774472306a1c334734103f7bf6231ad1370d4f71c2ae394fe8978afac5b2e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.8 MB (514821415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63309be2c0345cac77307aa173b9782aa5a84f553951abd498d16f5c04a4fa8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bcbc2151ce4be9aa40b26468719dafd6528d7d11d6f6cb60e3a58a3447305`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 15.6 MB (15558424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36295709cc3855d0f98f8a6b939053cc43efcf3092756703c1fc518d73fe77`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 54.8 MB (54752085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e451f55144f64f697f2945598b3a000bbac10e699d6068b7d6e63f9aa2b7f3b5`  
		Last Modified: Tue, 25 Feb 2025 04:17:48 GMT  
		Size: 197.1 MB (197074397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c39801b95216b4260c69cafb56f78679aec6c847d1e3d1afc1de560c4cd5e9`  
		Last Modified: Mon, 03 Mar 2025 21:14:42 GMT  
		Size: 193.7 MB (193695108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:2ee0d74ac110bd1a17d8332af3912202fbe343a4a38370a9db6bc9fa364b9d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd28e732df28539d58b7d7f26dacd50370d93acc3d43ba5ae570174138f6aec`

```dockerfile
```

-	Layers:
	-	`sha256:b0537ca4f5998de091de7aadced2002bc586c005466354e27181079037c37733`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 15.1 MB (15073413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:323b971a0322980ccb6d5b56d28083ac175e1bd00757315708f1421f1797d01f`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:2ac2d9029c9950551413e86bd26d8ad86f61590dd45bb4cd2da0a4b001432ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.1 MB (512134009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5029ae4b22101f3709c37ae1b0f1483b2f9ff3209787eb6e49ad590cad55da6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b371c05b17ddc4521fa62e27633ef500c9e18d0922c933dc30ad692d163a6adb`  
		Last Modified: Tue, 25 Feb 2025 01:31:01 GMT  
		Size: 49.0 MB (49026733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce7f37fed942ce7eb6947b63b02cebac1a836c49ae19b59c3dfd4d0dafde5e9`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 14.7 MB (14673973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3908d2a88cdaeb59d430f53cffe54008e1006a05c4aa7a391f2dce9c9b9aff8`  
		Last Modified: Tue, 25 Feb 2025 14:18:51 GMT  
		Size: 50.6 MB (50640099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a931f277cb7dadd19c4ea31b7570c91e754bb6d034542896c14a613c77034a3e`  
		Last Modified: Tue, 25 Feb 2025 16:54:04 GMT  
		Size: 167.5 MB (167527903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8016ff31b139f4cc1ac2b37027c3a5c553771198a19e3563f9ebcc51e15f4999`  
		Last Modified: Mon, 03 Mar 2025 21:23:09 GMT  
		Size: 230.3 MB (230265301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0bd6feae8faa96fd3e378eaa561081d1edabb91e202219f3fa32d7468381c067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c7808076946af42d45e2924dc9a57c449d7f6c9539ed7801a920d87def0c75`

```dockerfile
```

-	Layers:
	-	`sha256:afaa1ab536f6764953fbf3d43692672f51fc56aa085586bfb78431ead85f5d36`  
		Last Modified: Mon, 03 Mar 2025 21:23:04 GMT  
		Size: 14.9 MB (14874204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d11f72eaf746d2a6aa73bdc233abd05555878019f6832b3a21234f539567442`  
		Last Modified: Mon, 03 Mar 2025 21:23:03 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5d6e25360f6d028455c8b643f8f53d7c4efbc0064b23759608b61ad6a3adc223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.4 MB (571431917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1371eb80ca3e9f7fe5098765803837081bef8ff5751aecccc695e544f321dec2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364a649b3acc0e2c47a31825e92a687c9eae217b5c8c062f3efaabe7bec06f7`  
		Last Modified: Tue, 25 Feb 2025 05:42:11 GMT  
		Size: 15.5 MB (15544146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8a227b92685cb13561fe06ec9cfa79231e26157c7e163ab5b9af993e63bd10`  
		Last Modified: Tue, 25 Feb 2025 11:54:42 GMT  
		Size: 54.9 MB (54855421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bd61bef017e8e3b4e6f403c074fa47f738d2ac56d92eb50f50fff5dc8bd03`  
		Last Modified: Tue, 25 Feb 2025 15:23:19 GMT  
		Size: 190.0 MB (189986146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0073060607bc719b0aa94e147a0b6b03b6aefcd068fff7a78b8f947eecf9d5`  
		Last Modified: Mon, 03 Mar 2025 21:36:29 GMT  
		Size: 258.8 MB (258797560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7c24d055c4c4a49c2b849357293da9e9e2988140bdd4d982de7271f0e3143c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ebf36916e6fb93d90caf00958262c0c8b9c86735cb8958a061bbc281f3fd85`

```dockerfile
```

-	Layers:
	-	`sha256:493bc9dc75ddde0e35de2091d2eac442ce52714aa89a6f684f07608dbbcc2dea`  
		Last Modified: Mon, 03 Mar 2025 21:36:24 GMT  
		Size: 15.1 MB (15075673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44037f8c5cd51ccebdbaed303063aa1b879764d15ae47c490d35c0fe101c959f`  
		Last Modified: Mon, 03 Mar 2025 21:36:24 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-bullseye` - linux; 386

```console
$ docker pull rust@sha256:d96bbc13b6e3f5741b38e2d39e57c378073d01c5cf0f2e18023d0bf7c730098a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.6 MB (537592438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fb3dfd29980bf4e4cf1a785df10f73d2a9093d02a06e3fb1789e2e0670f645`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1763bdfcd7e692c8f35c71602a5206ff9e4716856edf6ae712febb4cc579d3`  
		Last Modified: Tue, 25 Feb 2025 02:24:11 GMT  
		Size: 16.1 MB (16062177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820de11811e966e41fc39b6790cf28a33ce0645127033d9f041fa3707235430e`  
		Last Modified: Tue, 25 Feb 2025 03:13:43 GMT  
		Size: 56.0 MB (56030023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa00228844a300b416d3473480cea8953822058ab89fc86d0c3c4056d2fe123`  
		Last Modified: Tue, 25 Feb 2025 04:18:06 GMT  
		Size: 200.0 MB (199978138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883849d920b1b05e06838787b545a094134ce0719a6b7b9f208333a79ce9a242`  
		Last Modified: Mon, 03 Mar 2025 21:14:43 GMT  
		Size: 210.8 MB (210843237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:16c416c5f5c143b8d3d0444b211b06b0f4ce71c2d44bab44374d6c8e196621f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5baa792f584e43afed942f1cb227670cfbb389df99f48d8914c3676ae81592e`

```dockerfile
```

-	Layers:
	-	`sha256:6a66d8cce735ea8c5513f850111cf3a06be5855d644d3836537665c230246349`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 15.1 MB (15060440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4f74ec7a17331b1624aac92a9d8ebad6de4e7c0902f293d6a7495e63d14e456`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85-slim`

```console
$ docker pull rust@sha256:215987920101ed15967e9ab4bab3a20e1b71ab3c0551b5088b380e0d4e1758b1
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

### `rust:1.85-slim` - linux; amd64

```console
$ docker pull rust@sha256:d3d93642ae6fd2cd84c7912184bb459b7b0db7e8faac0426bd6dca3940a8e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292709649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f34a203a3c381506722cf3c29ff282ee2a7a6c3ea5f9122a253e5db711f00a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387149dce16056dbdb4b06942bebd598293454f04bcf825305789d3fbd03ccc2`  
		Last Modified: Mon, 03 Mar 2025 21:14:29 GMT  
		Size: 264.5 MB (264490348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim` - unknown; unknown

```console
$ docker pull rust@sha256:2cadfef9494fded06cb45ac7dd21cf8be95bbc29d29843982b1136d37965399b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b31992db534d2f4beea704cd6f87a532756c8285f835090e85c8f923d989e`

```dockerfile
```

-	Layers:
	-	`sha256:12dde0feb1e98f9767c8a92f79c123cbb093c4e7ae6e7eada09ffdbaa4d28854`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 4.0 MB (3955305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc39115291e4d274b7e0282badf83b093f4dbfb6c01e6213fb4ee57cc1166dc9`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:9b012a9e771ea654d5d5ca13df9b16d30c582cbd91b239a6fac4d1261df41dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302041787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84120db8ea77fcfa8688c3eff9973638aa867fa532f1e31f8c14ab72b3a64581`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d5d06d813118d1b82098ef607f6a62da0ee850225501b423d07dfd2711d755`  
		Last Modified: Mon, 03 Mar 2025 21:15:00 GMT  
		Size: 278.1 MB (278122053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim` - unknown; unknown

```console
$ docker pull rust@sha256:c9bd5c78945d857d38fe8fa1ac884fe625c77e20599616076ad6721182c2f9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e04d921f393c225935b32033dca57f0e95c593bc7adb10b09f97d690f21a8e4`

```dockerfile
```

-	Layers:
	-	`sha256:6814569f1e5d4ef57f4bea7482e085eb9fb50e1857c3855319e7648690f598ae`  
		Last Modified: Mon, 03 Mar 2025 21:14:54 GMT  
		Size: 3.8 MB (3771368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86dd27a840b3d8ec5e099dd6964b60024cf9d327bb8bc7ecae0b35a82d999080`  
		Last Modified: Mon, 03 Mar 2025 21:14:53 GMT  
		Size: 13.4 KB (13378 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2592404bc1c86ee8445a2102a9a6927ac6f91aaa8821a4ff764884ac7984094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352689188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379c3debf1acbd8228d0dac86005b4fe2aa9dae005b2e1d825e5c1462322dd7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51868c8eb2680ac4209dae1f73861b9c082564efc6f5a6b39e39ac0d7d6ff6b5`  
		Last Modified: Mon, 03 Mar 2025 21:29:50 GMT  
		Size: 324.6 MB (324640763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim` - unknown; unknown

```console
$ docker pull rust@sha256:1e31d6a2695c5af40509bfd2eb1d961a0fb7988b0c1f26bff5d8f6e61c418412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52299a9631b27c74dd842e31aa7e0da8e26a849b4a815ba25015741e88c0ae46`

```dockerfile
```

-	Layers:
	-	`sha256:f273ab084a2e7575d05d06fa8ba8cf7e2d8f8da05b88269989a9ddde03493037`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 4.0 MB (3977648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b19592b0bba92266591738d7b34e3def4520d60096b6a10a024f01b3bedd90e`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-slim` - linux; 386

```console
$ docker pull rust@sha256:88ba2b4761e6d4257c7060aae566853aca592df9e026d748f161b37fb1c2764b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307630505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35b195ee846be85652a54550356ce979af10471acbd66a58ac492de03315688`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a89d68e962de64b429c772557a0e0a429dc425b2a14dcb31802e63de2e4e6bd`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 278.4 MB (278435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b3a7a9e30f6b551540715acbe44f408f539191ad77cc92d3276a74e91dfe0fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed2d74491588bf1f3886ac5c1ba7ef38f7f513a0298f405327e9be21f7af5da`

```dockerfile
```

-	Layers:
	-	`sha256:f2761352b9bb345b81ef703154b559b8e013093b8599a35ed94fdefb3c7327aa`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 3.9 MB (3935220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bacf9a7e03faf1ff9bf9fbd5138346c494c6f27d2ca9c99b3e3b0f5e79c2fe71`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:d17f48a04c1c202eb18025d892fddf578cedbdc537fa56a041db85189882ab6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355168893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8c917d31b3a645483187dd86afa887442274f948403c6ba0cb7530982f308f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a5a9edf391ebe6e786c0c06eb206b9f00800b0262e795ed3ae7f7a0618588f`  
		Last Modified: Mon, 03 Mar 2025 21:16:50 GMT  
		Size: 323.1 MB (323116579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim` - unknown; unknown

```console
$ docker pull rust@sha256:77418e4a89328c9c95965a089ff40eb2c4ae1bf5bece9a92578f48b38d198a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce5ae98dec6ba000aab82460ddc24921096bc35a28c42968b20cbe7a9b19d05`

```dockerfile
```

-	Layers:
	-	`sha256:9fc9db7381e23b41c20dcc2dea87608b0cf0c9091ea543bafb588a1cbb532d21`  
		Last Modified: Mon, 03 Mar 2025 21:16:33 GMT  
		Size: 3.9 MB (3927866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6eb443440c8ecf14e727b7761eed1b229ee61670c0190619f7a21685eb501b`  
		Last Modified: Mon, 03 Mar 2025 21:16:32 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-slim` - linux; s390x

```console
$ docker pull rust@sha256:5703e183e49c0e1dc763e6bdbe2c9bac4d8b652267f0bb85718f9e1c359f1b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358827701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d0faf0f8207be9497615f4b7573829e4fc8b2977f1a06d02e4b28d030c1d41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078929da424ac5687fa6c367c58665828a7d802e10e816e2ae05060d62a114e9`  
		Last Modified: Mon, 03 Mar 2025 21:15:44 GMT  
		Size: 332.0 MB (331962863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim` - unknown; unknown

```console
$ docker pull rust@sha256:22316782835c59c254cf08a9f94d0fbf9c7d97933beeca3f7be35411f06e5640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40c95061e80226561af8a4a6448bc3128287baf27bd094ecbb1af08b0ca6d00`

```dockerfile
```

-	Layers:
	-	`sha256:db5d3a28f1d73244b43980f7869840e4d6b6a7e6815101a9c53f1f060eb04089`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 3.8 MB (3797205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f1036a2309ba1a573101a8d36570d74e90b4a1095fdd22f30435cae8bfa61e`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85-slim-bookworm`

```console
$ docker pull rust@sha256:215987920101ed15967e9ab4bab3a20e1b71ab3c0551b5088b380e0d4e1758b1
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

### `rust:1.85-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:d3d93642ae6fd2cd84c7912184bb459b7b0db7e8faac0426bd6dca3940a8e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292709649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f34a203a3c381506722cf3c29ff282ee2a7a6c3ea5f9122a253e5db711f00a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387149dce16056dbdb4b06942bebd598293454f04bcf825305789d3fbd03ccc2`  
		Last Modified: Mon, 03 Mar 2025 21:14:29 GMT  
		Size: 264.5 MB (264490348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2cadfef9494fded06cb45ac7dd21cf8be95bbc29d29843982b1136d37965399b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b31992db534d2f4beea704cd6f87a532756c8285f835090e85c8f923d989e`

```dockerfile
```

-	Layers:
	-	`sha256:12dde0feb1e98f9767c8a92f79c123cbb093c4e7ae6e7eada09ffdbaa4d28854`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 4.0 MB (3955305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc39115291e4d274b7e0282badf83b093f4dbfb6c01e6213fb4ee57cc1166dc9`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:9b012a9e771ea654d5d5ca13df9b16d30c582cbd91b239a6fac4d1261df41dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302041787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84120db8ea77fcfa8688c3eff9973638aa867fa532f1e31f8c14ab72b3a64581`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d5d06d813118d1b82098ef607f6a62da0ee850225501b423d07dfd2711d755`  
		Last Modified: Mon, 03 Mar 2025 21:15:00 GMT  
		Size: 278.1 MB (278122053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c9bd5c78945d857d38fe8fa1ac884fe625c77e20599616076ad6721182c2f9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e04d921f393c225935b32033dca57f0e95c593bc7adb10b09f97d690f21a8e4`

```dockerfile
```

-	Layers:
	-	`sha256:6814569f1e5d4ef57f4bea7482e085eb9fb50e1857c3855319e7648690f598ae`  
		Last Modified: Mon, 03 Mar 2025 21:14:54 GMT  
		Size: 3.8 MB (3771368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86dd27a840b3d8ec5e099dd6964b60024cf9d327bb8bc7ecae0b35a82d999080`  
		Last Modified: Mon, 03 Mar 2025 21:14:53 GMT  
		Size: 13.4 KB (13378 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2592404bc1c86ee8445a2102a9a6927ac6f91aaa8821a4ff764884ac7984094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352689188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379c3debf1acbd8228d0dac86005b4fe2aa9dae005b2e1d825e5c1462322dd7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51868c8eb2680ac4209dae1f73861b9c082564efc6f5a6b39e39ac0d7d6ff6b5`  
		Last Modified: Mon, 03 Mar 2025 21:29:50 GMT  
		Size: 324.6 MB (324640763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1e31d6a2695c5af40509bfd2eb1d961a0fb7988b0c1f26bff5d8f6e61c418412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52299a9631b27c74dd842e31aa7e0da8e26a849b4a815ba25015741e88c0ae46`

```dockerfile
```

-	Layers:
	-	`sha256:f273ab084a2e7575d05d06fa8ba8cf7e2d8f8da05b88269989a9ddde03493037`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 4.0 MB (3977648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b19592b0bba92266591738d7b34e3def4520d60096b6a10a024f01b3bedd90e`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:88ba2b4761e6d4257c7060aae566853aca592df9e026d748f161b37fb1c2764b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307630505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35b195ee846be85652a54550356ce979af10471acbd66a58ac492de03315688`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a89d68e962de64b429c772557a0e0a429dc425b2a14dcb31802e63de2e4e6bd`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 278.4 MB (278435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b3a7a9e30f6b551540715acbe44f408f539191ad77cc92d3276a74e91dfe0fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed2d74491588bf1f3886ac5c1ba7ef38f7f513a0298f405327e9be21f7af5da`

```dockerfile
```

-	Layers:
	-	`sha256:f2761352b9bb345b81ef703154b559b8e013093b8599a35ed94fdefb3c7327aa`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 3.9 MB (3935220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bacf9a7e03faf1ff9bf9fbd5138346c494c6f27d2ca9c99b3e3b0f5e79c2fe71`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d17f48a04c1c202eb18025d892fddf578cedbdc537fa56a041db85189882ab6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355168893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8c917d31b3a645483187dd86afa887442274f948403c6ba0cb7530982f308f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a5a9edf391ebe6e786c0c06eb206b9f00800b0262e795ed3ae7f7a0618588f`  
		Last Modified: Mon, 03 Mar 2025 21:16:50 GMT  
		Size: 323.1 MB (323116579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:77418e4a89328c9c95965a089ff40eb2c4ae1bf5bece9a92578f48b38d198a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce5ae98dec6ba000aab82460ddc24921096bc35a28c42968b20cbe7a9b19d05`

```dockerfile
```

-	Layers:
	-	`sha256:9fc9db7381e23b41c20dcc2dea87608b0cf0c9091ea543bafb588a1cbb532d21`  
		Last Modified: Mon, 03 Mar 2025 21:16:33 GMT  
		Size: 3.9 MB (3927866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6eb443440c8ecf14e727b7761eed1b229ee61670c0190619f7a21685eb501b`  
		Last Modified: Mon, 03 Mar 2025 21:16:32 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:5703e183e49c0e1dc763e6bdbe2c9bac4d8b652267f0bb85718f9e1c359f1b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358827701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d0faf0f8207be9497615f4b7573829e4fc8b2977f1a06d02e4b28d030c1d41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078929da424ac5687fa6c367c58665828a7d802e10e816e2ae05060d62a114e9`  
		Last Modified: Mon, 03 Mar 2025 21:15:44 GMT  
		Size: 332.0 MB (331962863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:22316782835c59c254cf08a9f94d0fbf9c7d97933beeca3f7be35411f06e5640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40c95061e80226561af8a4a6448bc3128287baf27bd094ecbb1af08b0ca6d00`

```dockerfile
```

-	Layers:
	-	`sha256:db5d3a28f1d73244b43980f7869840e4d6b6a7e6815101a9c53f1f060eb04089`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 3.8 MB (3797205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f1036a2309ba1a573101a8d36570d74e90b4a1095fdd22f30435cae8bfa61e`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85-slim-bullseye`

```console
$ docker pull rust@sha256:e94e2d2e0a9df48fdfcacb47d8b60d036abe60b7c6fa3ac3de1dd16a3d18f19a
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

### `rust:1.85-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:dccdc77b5b046c078e76f4ca452308e213f4b7ba3e8a6c215393381d36d5b280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283883304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35d2ada2c353b98b46aff96c86cc0c21d362da854c48fcd0aa754b13b83eb20`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e0052749e7f2c9ab3a91aad47ad13df4c7c8911c162e2bdb7d08f691e99aac`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 253.6 MB (253629374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:19d324bd0c298ad1b3f5e6df1ce1df18225864b216efbb6c90ddce0a8ce24642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c80060630492f3b3f74f9d388000b5067bc23694bacc999541e6da57bf59ff`

```dockerfile
```

-	Layers:
	-	`sha256:df56ae19c38d79a9c6b3901f1921d9c3833a93218a082679bdb0a12883f3905e`  
		Last Modified: Mon, 03 Mar 2025 21:14:22 GMT  
		Size: 4.2 MB (4173204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9fc1edc1c95e2a303e127182409fafb9fc9e2d3f3ad0da80b896cad7720daaa`  
		Last Modified: Mon, 03 Mar 2025 21:14:21 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:1c291529dbe66cd22592a3d8ecc5cead222cb64a3d43b8aaadfa065746e28570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297882666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e350660ab01bd40fd4abffb3fd8ba3d377659d12c689daca3b6779053172617`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0ca501b624d9dae81049df15e1024733ee21141b25f8ca123d98e0d13df5d12`  
		Last Modified: Tue, 25 Feb 2025 01:31:18 GMT  
		Size: 25.5 MB (25535432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6d72cafe6043b15f5dabf082f52f18a84a9ac04dfbfe5fc6bba3fcbe37edd0`  
		Last Modified: Mon, 03 Mar 2025 21:20:57 GMT  
		Size: 272.3 MB (272347234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:07cd7090e5192facfdd11a8b0ed54d90c6c4f804c8c9a9059c3d3e7ba657c970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612130ff6bdfd39ede8255ddb232e9327ffb825112e6bb1017c80060be9e9c7d`

```dockerfile
```

-	Layers:
	-	`sha256:73bc2806f7ecf2f20576c7878e9d5e9b7dfc3b25b6132689e08490bce610f038`  
		Last Modified: Mon, 03 Mar 2025 21:20:39 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f927f926449a4f38eeebab517940bd75ca9acef94ae1a163391730411486b20`  
		Last Modified: Mon, 03 Mar 2025 21:20:38 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:de9c5b13bcc43221f1603fb03089d27e59603e8087525be9302e30fa4a75e3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343069561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e422222ab9bba42554ec25e8f7656f35c48de3d1930f29223b4c40648547e500`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ae7537677409c7e96b2e534829fe706743a9e1c1fc79c0e6c3a6ae631021d1`  
		Last Modified: Mon, 03 Mar 2025 21:34:48 GMT  
		Size: 314.3 MB (314323574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:cb9b665a79ff9d7407b5196e20d85e27ec9c2216b78c66b5a1dfa4a438542750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b594182c132405732dc65dec31b847e10c0314703f603d9728caf021dd2f8c3`

```dockerfile
```

-	Layers:
	-	`sha256:f87a9a1c38fe1dae028e9162ed79be83deebf92138b807780b636247a977d593`  
		Last Modified: Mon, 03 Mar 2025 21:34:40 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0c9191b26a4828e5bd697af4e870ad8de930043587eddf2407e36a5f19df4ea`  
		Last Modified: Mon, 03 Mar 2025 21:34:40 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:8ce46ac85186e75d85f9912eaea882d8fab038755ad48d921a2974b006f800a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302583357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66df80913375cbd40ebb9b025095b1856d1454a6206427f78c4846d5b5771158`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc6ac53dd3c2cb0c6fd992e5925fc15a335691c21c9dc26765ed22ae0d20371`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 271.4 MB (271402930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e925605333c9a3842c68db47ba3d21c3ba0539ccbf18a0231b3a8cfacca912b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55c2e9da4484fa31efbf5cc3c8d14b787bc24da1ef1871ff26f4e0ac811f26d`

```dockerfile
```

-	Layers:
	-	`sha256:d0d87fc423e5c2445348c3696ac9ef20a4fae6bfa1ceebb2a4a2a6b7af161b60`  
		Last Modified: Mon, 03 Mar 2025 21:14:33 GMT  
		Size: 4.2 MB (4163461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714de8d934c25f3276ae4b994be3302532085a4c69860853de35ef86540dd876`  
		Last Modified: Mon, 03 Mar 2025 21:14:33 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85.0`

```console
$ docker pull rust@sha256:e15c642b487dd013b2e425d001d32927391aca787ac582b98cca72234d466b60
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

### `rust:1.85.0` - linux; amd64

```console
$ docker pull rust@sha256:f6fc45b5a8d3b72dcff6442b5311f0b1f854a3480797f91ecbfb16c0fd5d4527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.0 MB (541963415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aac1c9ca934dcc8a2f93033651d5f86fb3b99783c81428ecce40198d4abc0af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c03d5625da4fd65f189b350dab8fda9ce3054bdd41f9a509973b3cd0cd571e`  
		Last Modified: Mon, 03 Mar 2025 21:14:28 GMT  
		Size: 193.7 MB (193695926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0` - unknown; unknown

```console
$ docker pull rust@sha256:4d1be75651ae6516c73cd01fb804f023e4d53bdf2b9d5cb9e5a78381266818c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca03f69ea0d5d937b5bf2bba4b75d5a4cb308e7460975b526f3138436e1a7f7b`

```dockerfile
```

-	Layers:
	-	`sha256:f2aa5e71de5c6e138f09eb61c0c64219101f7290d0719c4e4f2763b9cbbcafa9`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 15.5 MB (15474256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bfe55c7c856b4e205d1086d7f00a0c16d9544ceb0316ec5f5368e8f86a5a815`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0` - linux; arm variant v7

```console
$ docker pull rust@sha256:cb81fdf6321d7de7b04a0978a0f1af3d2ce2e9b5302a619b7d538132a0d783bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531318143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cba7271ee5cf51b3565fbb44d531aa336955fdf97d4159e8544e9e1ede35187`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70e25650a3be5d12fed3dfd4069f605d42d17b86fa4c689b69aa636aee22155`  
		Last Modified: Mon, 03 Mar 2025 21:18:08 GMT  
		Size: 230.3 MB (230264903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0` - unknown; unknown

```console
$ docker pull rust@sha256:c6712addcc809b8eb0fe21d81f7f7eba0637e2838086b119dcbbc41e4187a6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e9006d373cfef0bc4e89bb17079c2f22f1ae42ed8a2b7dcd57d4b3c67b04c9`

```dockerfile
```

-	Layers:
	-	`sha256:fab2c1c1f543fac09d7660a2054a25708a28b23b14e1f1c9a3a6e1644e54b678`  
		Last Modified: Mon, 03 Mar 2025 21:18:02 GMT  
		Size: 15.3 MB (15278698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f349b53969dfbfa675b8173f92a74dbd59458f6214685c9dd2c7318179f6cc32`  
		Last Modified: Mon, 03 Mar 2025 21:18:01 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be252dc02478902ea4c4a6e1e2b49181f1fa3aaeb96a47e40dc248b2598cf243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.8 MB (597772744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192cc1afeb41abe7df5d2c3f94eb7e40a991156c86412ad4cab156f754d7f291`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b5a4332d3d01f663d9e0b5d8a153c25ca20c2d7e94ce224b627a88380da001`  
		Last Modified: Mon, 03 Mar 2025 21:31:31 GMT  
		Size: 258.8 MB (258797571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0` - unknown; unknown

```console
$ docker pull rust@sha256:0cea832fdaaa30a9c04e35a4d5de0ede3f8723564efacebd2cae817dba8af26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef22842e59d31eab71173da3ae37fbcabd9b445839c9e49ffa7b0d93c64a8f51`

```dockerfile
```

-	Layers:
	-	`sha256:463dc9b45f12289d11de3d7eaffa14e7641471dd399b68728748be80a572fea3`  
		Last Modified: Mon, 03 Mar 2025 21:31:25 GMT  
		Size: 15.5 MB (15502831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:479aac264bc9d5563cda8973c1adf5fcc9d667f916488c189c512d2bb1d18d12`  
		Last Modified: Mon, 03 Mar 2025 21:31:24 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0` - linux; 386

```console
$ docker pull rust@sha256:c3ba8ba76e08440fcff73d04693fef720530890076f46b8761da0dddcedadb78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.7 MB (561694245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676197b0baccfd7dd45db61469de196ac15950aa10debfbcd2b0583af2dafed4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca163299b0e606d2916a03bd0f60c5903c6e5abeab65da3a8c490174697c929`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 24.9 MB (24899353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c3400be327e90dc9e848a16d4b0fcd191708de152e68c6b4888d83c61f441`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 66.2 MB (66237814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3ca8ca718f538c2871c3deeec438c611f0f26a3b97976b89d6d6abcca894dd`  
		Last Modified: Tue, 25 Feb 2025 05:12:06 GMT  
		Size: 210.3 MB (210255482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c5735fe88e109ded1d53e0e079c60705e16af5652ea6c119760594e52d6fb`  
		Last Modified: Mon, 03 Mar 2025 21:14:43 GMT  
		Size: 210.8 MB (210843144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0` - unknown; unknown

```console
$ docker pull rust@sha256:8c10ae28c24f12a5b3e3598c4abb8a26206a7edef522211dc27667c598621f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5c3c563ea6d86b133dd81fc4d8eaecefc99bc076f1c075059797e8116f36d3`

```dockerfile
```

-	Layers:
	-	`sha256:0ab28f08ca6a412da7f3016c8c2eb5dc331d3000a50c38114eb87924f817b53a`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 15.5 MB (15451518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd3c3e28ee8144d301f821eb5b432e99ec8f8776af706e07ba3a04d48e6f7ac`  
		Last Modified: Mon, 03 Mar 2025 21:14:37 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0` - linux; ppc64le

```console
$ docker pull rust@sha256:0fe5e17dc44d5fdbd2560266262d98e813b49ca1e9b0ba23d9b3675fe2adacb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.6 MB (616586281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d35305b8c7077eb68baa8b585fec750d11f2afc7094e64b59f8e368246879`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad13c90d099a380a8fc2ec9ef74de7ad957b1496d75b8d1c4617069765510053`  
		Last Modified: Mon, 03 Mar 2025 21:24:43 GMT  
		Size: 254.3 MB (254345476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0` - unknown; unknown

```console
$ docker pull rust@sha256:0676ad8c84ebbb134f5e3c3aab74a661c1ac924ee0fa1a042d90d7fbadfc4585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ad946c6e11f49c09021728047cc0f3fa4a83f0101fa1031085c8f8e0d2ca1c`

```dockerfile
```

-	Layers:
	-	`sha256:14a5009de22d0268d16a06051e63b1bd4e5a83615d08555e021663ada543f0e2`  
		Last Modified: Mon, 03 Mar 2025 21:24:31 GMT  
		Size: 15.4 MB (15449362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e237236a91844fef1f239951791ab5549d6226f7a182592fa6867fc48d952279`  
		Last Modified: Mon, 03 Mar 2025 21:24:28 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0` - linux; s390x

```console
$ docker pull rust@sha256:70fe5668b3762d8a81b5059f9c4bad31ac92bf152d57195193c433368ec36f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599864262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b0dc30045f5d2e53b0a2a92cd31f6f8e3bdeca4ccb1165d6d2ac3cdcf807a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f679165548785dd187eaea9af4ee69db5b37630f35ce564d064cd7512fcfb9`  
		Last Modified: Mon, 03 Mar 2025 21:31:35 GMT  
		Size: 281.8 MB (281820436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0` - unknown; unknown

```console
$ docker pull rust@sha256:dbf40b3fd37699736f3445354654c43b50a382b3ef92f0ea8de4366bcc1af9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d288575d5989682a9df5b6cb7dc314ca8e3380685956acf21030572b2fe26d2e`

```dockerfile
```

-	Layers:
	-	`sha256:83fad1cb4c19e71cbc100ba5c079f7fda458db61bafa47c1cc48e228ce18802f`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 15.3 MB (15286944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4d7f0c7c0907b0c5b392d225150310f20e92d9173b7a16ce384cd7507427f6`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85.0-alpine`

```console
$ docker pull rust@sha256:1030547bd568497d69e41771ada279179f0613369dc54779e46a3f6f376b3020
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.85.0-alpine` - linux; amd64

```console
$ docker pull rust@sha256:84b5e9c7c2f9437f62769913b419cc02a1e310bf40fd86720cd2b3b64bffb452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304368783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec94ecf18f99333d5bd8f2a15427ba1b4736299f4d5f4a35660f5fe75b6291a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b95e11be61c0eea8aadf788692bf0fcec5f9c75738d3f5713dfbcc016f337f4`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 61.6 MB (61565003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6fc4d476520099dcd8ba0f71c1e15bb2d762c9977506070eea6cb78a2a4c6`  
		Last Modified: Mon, 03 Mar 2025 21:14:31 GMT  
		Size: 239.2 MB (239161533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:d8cff90939ad06ca11df0fc881253dc5d1d768c2221f8466415334d2739cbfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4955895d71a1f61c0886f29ea5b6a23986cda0a9910e8ba13ff472aff21cac1f`

```dockerfile
```

-	Layers:
	-	`sha256:fd7a8c7ea021f7804add54b5f5efd33149b2e2c7d915f1622744e64dbbe08c7c`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457f860b4e4d19a0674d0ca4f6ec06ff6958c351407559ee9c974d2b3bbca63f`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bda9e5682eeb0013c19b06e469812ae54cbe76cf0128796def8eb9bfe30a5c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307415047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72195abfac34db128f0c99e35ad0a1a98210b81274e98b65ac2973dae8aeb0dd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b46568d489c620031542c16213dea9e63b74c664a11f85b1bb86a8e526e5a16`  
		Last Modified: Mon, 03 Mar 2025 21:23:23 GMT  
		Size: 59.1 MB (59101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51de9687e383104ad782ecb8afe38b4c33220f4e646112f07f0e47d399d0a9fd`  
		Last Modified: Mon, 03 Mar 2025 21:23:28 GMT  
		Size: 244.3 MB (244320886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:429bfdee3cf71b49563ad904faf2875e578ae734980bd44b1c38b27f5855fd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d07c59fd4b9553baf3c76bd773969e82fed14c0dcfa7ca467660406d07156`

```dockerfile
```

-	Layers:
	-	`sha256:fbed74b3e0b30a9432fe2ba4b82f04cb881dd5c6f374c1aff1f3d2f2018fb7f3`  
		Last Modified: Mon, 03 Mar 2025 21:23:22 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81eca9cb1582aed143c4d744ce7a925b1e10e4678aaf0916e76d40846bb2d61`  
		Last Modified: Mon, 03 Mar 2025 21:23:21 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85.0-alpine3.20`

```console
$ docker pull rust@sha256:f0cef6c65992995b1c7816cb667de95799852e3fbed9d06f95855cbc512a0fd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.85.0-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:6d824fef86a8532aecead5889d49d432d19e0dd58b958266c994cca9eb7a3357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298102813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c38e59fb99c1014ea6d250d396bb9bf55981f1d69fe17ed05047b90cd119ca9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0430b4a2b30329b0c06034d1df61c2f3533c436834a54b76def8756d804d888`  
		Last Modified: Mon, 03 Mar 2025 21:17:28 GMT  
		Size: 55.3 MB (55315558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fda7dd06f6e434e3727cd86155430a51568846533e3824548334e20f1078e28`  
		Last Modified: Mon, 03 Mar 2025 21:17:31 GMT  
		Size: 239.2 MB (239160358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:ab2a41c3a86b0e8de97e1cff7ca3624a6e69e478c7c29615df5979d5655d03c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e987a7ec625942a721de02dcd92bf4ea3f7481ee651c6aef639e3a2f3f16ba`

```dockerfile
```

-	Layers:
	-	`sha256:4100e90a822ec6152c54ec22e8ce0b4cfb24694b82b0d9252e191958ce4d59cf`  
		Last Modified: Mon, 03 Mar 2025 21:17:28 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca3c1b9b1144fd4038e19dea5e9afef77e4732804442cc1813ffcbd1c7289e4`  
		Last Modified: Mon, 03 Mar 2025 21:17:27 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f91c5c68a69111314bb721b7bb75aaa4b310b9ef676f2591e88769bbbb3bd933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301363171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61566cb96efc54b3ee29f6409c0e76059ca7b3c261b99a2940c188c54c3a66c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c8bee9c91c68545cb9604a6baaf13f4c921f1a8a851437cc7ce63f942e113d`  
		Last Modified: Mon, 03 Mar 2025 21:26:24 GMT  
		Size: 53.0 MB (52950488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998e7300919f154807a1ce8bdaa868228719c39a95b4c276a758f1bf480b361`  
		Last Modified: Mon, 03 Mar 2025 21:26:28 GMT  
		Size: 244.3 MB (244321518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1e4651facc4a66b01c40f8bec063469f936cbf603daf477c1003e794040d3e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beeb6c0426bb32cbdd133d31ad5ed10820561b72d66e1d95f332bfb42d012779`

```dockerfile
```

-	Layers:
	-	`sha256:183ceb0143fb3784d416af0d9e6e49059191e33606b5db6d715b5666f0fd139b`  
		Last Modified: Mon, 03 Mar 2025 21:26:22 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe75a1adc68e5615e04f2ea23b7e198a996bb1378319d115d5ca7b6fbef7602`  
		Last Modified: Mon, 03 Mar 2025 21:26:22 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85.0-alpine3.21`

```console
$ docker pull rust@sha256:1030547bd568497d69e41771ada279179f0613369dc54779e46a3f6f376b3020
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.85.0-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:84b5e9c7c2f9437f62769913b419cc02a1e310bf40fd86720cd2b3b64bffb452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304368783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec94ecf18f99333d5bd8f2a15427ba1b4736299f4d5f4a35660f5fe75b6291a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b95e11be61c0eea8aadf788692bf0fcec5f9c75738d3f5713dfbcc016f337f4`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 61.6 MB (61565003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6fc4d476520099dcd8ba0f71c1e15bb2d762c9977506070eea6cb78a2a4c6`  
		Last Modified: Mon, 03 Mar 2025 21:14:31 GMT  
		Size: 239.2 MB (239161533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:d8cff90939ad06ca11df0fc881253dc5d1d768c2221f8466415334d2739cbfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4955895d71a1f61c0886f29ea5b6a23986cda0a9910e8ba13ff472aff21cac1f`

```dockerfile
```

-	Layers:
	-	`sha256:fd7a8c7ea021f7804add54b5f5efd33149b2e2c7d915f1622744e64dbbe08c7c`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457f860b4e4d19a0674d0ca4f6ec06ff6958c351407559ee9c974d2b3bbca63f`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bda9e5682eeb0013c19b06e469812ae54cbe76cf0128796def8eb9bfe30a5c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307415047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72195abfac34db128f0c99e35ad0a1a98210b81274e98b65ac2973dae8aeb0dd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b46568d489c620031542c16213dea9e63b74c664a11f85b1bb86a8e526e5a16`  
		Last Modified: Mon, 03 Mar 2025 21:23:23 GMT  
		Size: 59.1 MB (59101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51de9687e383104ad782ecb8afe38b4c33220f4e646112f07f0e47d399d0a9fd`  
		Last Modified: Mon, 03 Mar 2025 21:23:28 GMT  
		Size: 244.3 MB (244320886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:429bfdee3cf71b49563ad904faf2875e578ae734980bd44b1c38b27f5855fd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d07c59fd4b9553baf3c76bd773969e82fed14c0dcfa7ca467660406d07156`

```dockerfile
```

-	Layers:
	-	`sha256:fbed74b3e0b30a9432fe2ba4b82f04cb881dd5c6f374c1aff1f3d2f2018fb7f3`  
		Last Modified: Mon, 03 Mar 2025 21:23:22 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81eca9cb1582aed143c4d744ce7a925b1e10e4678aaf0916e76d40846bb2d61`  
		Last Modified: Mon, 03 Mar 2025 21:23:21 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85.0-bookworm`

```console
$ docker pull rust@sha256:e15c642b487dd013b2e425d001d32927391aca787ac582b98cca72234d466b60
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

### `rust:1.85.0-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:f6fc45b5a8d3b72dcff6442b5311f0b1f854a3480797f91ecbfb16c0fd5d4527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.0 MB (541963415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aac1c9ca934dcc8a2f93033651d5f86fb3b99783c81428ecce40198d4abc0af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c03d5625da4fd65f189b350dab8fda9ce3054bdd41f9a509973b3cd0cd571e`  
		Last Modified: Mon, 03 Mar 2025 21:14:28 GMT  
		Size: 193.7 MB (193695926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4d1be75651ae6516c73cd01fb804f023e4d53bdf2b9d5cb9e5a78381266818c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca03f69ea0d5d937b5bf2bba4b75d5a4cb308e7460975b526f3138436e1a7f7b`

```dockerfile
```

-	Layers:
	-	`sha256:f2aa5e71de5c6e138f09eb61c0c64219101f7290d0719c4e4f2763b9cbbcafa9`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 15.5 MB (15474256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bfe55c7c856b4e205d1086d7f00a0c16d9544ceb0316ec5f5368e8f86a5a815`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:cb81fdf6321d7de7b04a0978a0f1af3d2ce2e9b5302a619b7d538132a0d783bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531318143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cba7271ee5cf51b3565fbb44d531aa336955fdf97d4159e8544e9e1ede35187`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70e25650a3be5d12fed3dfd4069f605d42d17b86fa4c689b69aa636aee22155`  
		Last Modified: Mon, 03 Mar 2025 21:18:08 GMT  
		Size: 230.3 MB (230264903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c6712addcc809b8eb0fe21d81f7f7eba0637e2838086b119dcbbc41e4187a6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e9006d373cfef0bc4e89bb17079c2f22f1ae42ed8a2b7dcd57d4b3c67b04c9`

```dockerfile
```

-	Layers:
	-	`sha256:fab2c1c1f543fac09d7660a2054a25708a28b23b14e1f1c9a3a6e1644e54b678`  
		Last Modified: Mon, 03 Mar 2025 21:18:02 GMT  
		Size: 15.3 MB (15278698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f349b53969dfbfa675b8173f92a74dbd59458f6214685c9dd2c7318179f6cc32`  
		Last Modified: Mon, 03 Mar 2025 21:18:01 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be252dc02478902ea4c4a6e1e2b49181f1fa3aaeb96a47e40dc248b2598cf243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.8 MB (597772744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192cc1afeb41abe7df5d2c3f94eb7e40a991156c86412ad4cab156f754d7f291`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b5a4332d3d01f663d9e0b5d8a153c25ca20c2d7e94ce224b627a88380da001`  
		Last Modified: Mon, 03 Mar 2025 21:31:31 GMT  
		Size: 258.8 MB (258797571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0cea832fdaaa30a9c04e35a4d5de0ede3f8723564efacebd2cae817dba8af26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef22842e59d31eab71173da3ae37fbcabd9b445839c9e49ffa7b0d93c64a8f51`

```dockerfile
```

-	Layers:
	-	`sha256:463dc9b45f12289d11de3d7eaffa14e7641471dd399b68728748be80a572fea3`  
		Last Modified: Mon, 03 Mar 2025 21:31:25 GMT  
		Size: 15.5 MB (15502831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:479aac264bc9d5563cda8973c1adf5fcc9d667f916488c189c512d2bb1d18d12`  
		Last Modified: Mon, 03 Mar 2025 21:31:24 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-bookworm` - linux; 386

```console
$ docker pull rust@sha256:c3ba8ba76e08440fcff73d04693fef720530890076f46b8761da0dddcedadb78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.7 MB (561694245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676197b0baccfd7dd45db61469de196ac15950aa10debfbcd2b0583af2dafed4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca163299b0e606d2916a03bd0f60c5903c6e5abeab65da3a8c490174697c929`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 24.9 MB (24899353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c3400be327e90dc9e848a16d4b0fcd191708de152e68c6b4888d83c61f441`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 66.2 MB (66237814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3ca8ca718f538c2871c3deeec438c611f0f26a3b97976b89d6d6abcca894dd`  
		Last Modified: Tue, 25 Feb 2025 05:12:06 GMT  
		Size: 210.3 MB (210255482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c5735fe88e109ded1d53e0e079c60705e16af5652ea6c119760594e52d6fb`  
		Last Modified: Mon, 03 Mar 2025 21:14:43 GMT  
		Size: 210.8 MB (210843144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8c10ae28c24f12a5b3e3598c4abb8a26206a7edef522211dc27667c598621f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5c3c563ea6d86b133dd81fc4d8eaecefc99bc076f1c075059797e8116f36d3`

```dockerfile
```

-	Layers:
	-	`sha256:0ab28f08ca6a412da7f3016c8c2eb5dc331d3000a50c38114eb87924f817b53a`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 15.5 MB (15451518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd3c3e28ee8144d301f821eb5b432e99ec8f8776af706e07ba3a04d48e6f7ac`  
		Last Modified: Mon, 03 Mar 2025 21:14:37 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:0fe5e17dc44d5fdbd2560266262d98e813b49ca1e9b0ba23d9b3675fe2adacb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.6 MB (616586281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d35305b8c7077eb68baa8b585fec750d11f2afc7094e64b59f8e368246879`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad13c90d099a380a8fc2ec9ef74de7ad957b1496d75b8d1c4617069765510053`  
		Last Modified: Mon, 03 Mar 2025 21:24:43 GMT  
		Size: 254.3 MB (254345476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0676ad8c84ebbb134f5e3c3aab74a661c1ac924ee0fa1a042d90d7fbadfc4585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ad946c6e11f49c09021728047cc0f3fa4a83f0101fa1031085c8f8e0d2ca1c`

```dockerfile
```

-	Layers:
	-	`sha256:14a5009de22d0268d16a06051e63b1bd4e5a83615d08555e021663ada543f0e2`  
		Last Modified: Mon, 03 Mar 2025 21:24:31 GMT  
		Size: 15.4 MB (15449362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e237236a91844fef1f239951791ab5549d6226f7a182592fa6867fc48d952279`  
		Last Modified: Mon, 03 Mar 2025 21:24:28 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:70fe5668b3762d8a81b5059f9c4bad31ac92bf152d57195193c433368ec36f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599864262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b0dc30045f5d2e53b0a2a92cd31f6f8e3bdeca4ccb1165d6d2ac3cdcf807a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f679165548785dd187eaea9af4ee69db5b37630f35ce564d064cd7512fcfb9`  
		Last Modified: Mon, 03 Mar 2025 21:31:35 GMT  
		Size: 281.8 MB (281820436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:dbf40b3fd37699736f3445354654c43b50a382b3ef92f0ea8de4366bcc1af9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d288575d5989682a9df5b6cb7dc314ca8e3380685956acf21030572b2fe26d2e`

```dockerfile
```

-	Layers:
	-	`sha256:83fad1cb4c19e71cbc100ba5c079f7fda458db61bafa47c1cc48e228ce18802f`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 15.3 MB (15286944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4d7f0c7c0907b0c5b392d225150310f20e92d9173b7a16ce384cd7507427f6`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85.0-bullseye`

```console
$ docker pull rust@sha256:6cb2cf341137cabc58d05942ca17e31c2c973ee50e2dac8bef4c0edc4e9e21ac
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

### `rust:1.85.0-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:4774472306a1c334734103f7bf6231ad1370d4f71c2ae394fe8978afac5b2e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.8 MB (514821415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63309be2c0345cac77307aa173b9782aa5a84f553951abd498d16f5c04a4fa8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bcbc2151ce4be9aa40b26468719dafd6528d7d11d6f6cb60e3a58a3447305`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 15.6 MB (15558424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36295709cc3855d0f98f8a6b939053cc43efcf3092756703c1fc518d73fe77`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 54.8 MB (54752085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e451f55144f64f697f2945598b3a000bbac10e699d6068b7d6e63f9aa2b7f3b5`  
		Last Modified: Tue, 25 Feb 2025 04:17:48 GMT  
		Size: 197.1 MB (197074397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c39801b95216b4260c69cafb56f78679aec6c847d1e3d1afc1de560c4cd5e9`  
		Last Modified: Mon, 03 Mar 2025 21:14:42 GMT  
		Size: 193.7 MB (193695108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:2ee0d74ac110bd1a17d8332af3912202fbe343a4a38370a9db6bc9fa364b9d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd28e732df28539d58b7d7f26dacd50370d93acc3d43ba5ae570174138f6aec`

```dockerfile
```

-	Layers:
	-	`sha256:b0537ca4f5998de091de7aadced2002bc586c005466354e27181079037c37733`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 15.1 MB (15073413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:323b971a0322980ccb6d5b56d28083ac175e1bd00757315708f1421f1797d01f`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:2ac2d9029c9950551413e86bd26d8ad86f61590dd45bb4cd2da0a4b001432ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.1 MB (512134009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5029ae4b22101f3709c37ae1b0f1483b2f9ff3209787eb6e49ad590cad55da6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b371c05b17ddc4521fa62e27633ef500c9e18d0922c933dc30ad692d163a6adb`  
		Last Modified: Tue, 25 Feb 2025 01:31:01 GMT  
		Size: 49.0 MB (49026733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce7f37fed942ce7eb6947b63b02cebac1a836c49ae19b59c3dfd4d0dafde5e9`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 14.7 MB (14673973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3908d2a88cdaeb59d430f53cffe54008e1006a05c4aa7a391f2dce9c9b9aff8`  
		Last Modified: Tue, 25 Feb 2025 14:18:51 GMT  
		Size: 50.6 MB (50640099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a931f277cb7dadd19c4ea31b7570c91e754bb6d034542896c14a613c77034a3e`  
		Last Modified: Tue, 25 Feb 2025 16:54:04 GMT  
		Size: 167.5 MB (167527903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8016ff31b139f4cc1ac2b37027c3a5c553771198a19e3563f9ebcc51e15f4999`  
		Last Modified: Mon, 03 Mar 2025 21:23:09 GMT  
		Size: 230.3 MB (230265301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0bd6feae8faa96fd3e378eaa561081d1edabb91e202219f3fa32d7468381c067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c7808076946af42d45e2924dc9a57c449d7f6c9539ed7801a920d87def0c75`

```dockerfile
```

-	Layers:
	-	`sha256:afaa1ab536f6764953fbf3d43692672f51fc56aa085586bfb78431ead85f5d36`  
		Last Modified: Mon, 03 Mar 2025 21:23:04 GMT  
		Size: 14.9 MB (14874204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d11f72eaf746d2a6aa73bdc233abd05555878019f6832b3a21234f539567442`  
		Last Modified: Mon, 03 Mar 2025 21:23:03 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5d6e25360f6d028455c8b643f8f53d7c4efbc0064b23759608b61ad6a3adc223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.4 MB (571431917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1371eb80ca3e9f7fe5098765803837081bef8ff5751aecccc695e544f321dec2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364a649b3acc0e2c47a31825e92a687c9eae217b5c8c062f3efaabe7bec06f7`  
		Last Modified: Tue, 25 Feb 2025 05:42:11 GMT  
		Size: 15.5 MB (15544146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8a227b92685cb13561fe06ec9cfa79231e26157c7e163ab5b9af993e63bd10`  
		Last Modified: Tue, 25 Feb 2025 11:54:42 GMT  
		Size: 54.9 MB (54855421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bd61bef017e8e3b4e6f403c074fa47f738d2ac56d92eb50f50fff5dc8bd03`  
		Last Modified: Tue, 25 Feb 2025 15:23:19 GMT  
		Size: 190.0 MB (189986146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0073060607bc719b0aa94e147a0b6b03b6aefcd068fff7a78b8f947eecf9d5`  
		Last Modified: Mon, 03 Mar 2025 21:36:29 GMT  
		Size: 258.8 MB (258797560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7c24d055c4c4a49c2b849357293da9e9e2988140bdd4d982de7271f0e3143c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ebf36916e6fb93d90caf00958262c0c8b9c86735cb8958a061bbc281f3fd85`

```dockerfile
```

-	Layers:
	-	`sha256:493bc9dc75ddde0e35de2091d2eac442ce52714aa89a6f684f07608dbbcc2dea`  
		Last Modified: Mon, 03 Mar 2025 21:36:24 GMT  
		Size: 15.1 MB (15075673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44037f8c5cd51ccebdbaed303063aa1b879764d15ae47c490d35c0fe101c959f`  
		Last Modified: Mon, 03 Mar 2025 21:36:24 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-bullseye` - linux; 386

```console
$ docker pull rust@sha256:d96bbc13b6e3f5741b38e2d39e57c378073d01c5cf0f2e18023d0bf7c730098a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.6 MB (537592438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fb3dfd29980bf4e4cf1a785df10f73d2a9093d02a06e3fb1789e2e0670f645`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1763bdfcd7e692c8f35c71602a5206ff9e4716856edf6ae712febb4cc579d3`  
		Last Modified: Tue, 25 Feb 2025 02:24:11 GMT  
		Size: 16.1 MB (16062177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820de11811e966e41fc39b6790cf28a33ce0645127033d9f041fa3707235430e`  
		Last Modified: Tue, 25 Feb 2025 03:13:43 GMT  
		Size: 56.0 MB (56030023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa00228844a300b416d3473480cea8953822058ab89fc86d0c3c4056d2fe123`  
		Last Modified: Tue, 25 Feb 2025 04:18:06 GMT  
		Size: 200.0 MB (199978138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883849d920b1b05e06838787b545a094134ce0719a6b7b9f208333a79ce9a242`  
		Last Modified: Mon, 03 Mar 2025 21:14:43 GMT  
		Size: 210.8 MB (210843237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:16c416c5f5c143b8d3d0444b211b06b0f4ce71c2d44bab44374d6c8e196621f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5baa792f584e43afed942f1cb227670cfbb389df99f48d8914c3676ae81592e`

```dockerfile
```

-	Layers:
	-	`sha256:6a66d8cce735ea8c5513f850111cf3a06be5855d644d3836537665c230246349`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 15.1 MB (15060440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4f74ec7a17331b1624aac92a9d8ebad6de4e7c0902f293d6a7495e63d14e456`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85.0-slim`

```console
$ docker pull rust@sha256:215987920101ed15967e9ab4bab3a20e1b71ab3c0551b5088b380e0d4e1758b1
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

### `rust:1.85.0-slim` - linux; amd64

```console
$ docker pull rust@sha256:d3d93642ae6fd2cd84c7912184bb459b7b0db7e8faac0426bd6dca3940a8e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292709649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f34a203a3c381506722cf3c29ff282ee2a7a6c3ea5f9122a253e5db711f00a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387149dce16056dbdb4b06942bebd598293454f04bcf825305789d3fbd03ccc2`  
		Last Modified: Mon, 03 Mar 2025 21:14:29 GMT  
		Size: 264.5 MB (264490348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:2cadfef9494fded06cb45ac7dd21cf8be95bbc29d29843982b1136d37965399b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b31992db534d2f4beea704cd6f87a532756c8285f835090e85c8f923d989e`

```dockerfile
```

-	Layers:
	-	`sha256:12dde0feb1e98f9767c8a92f79c123cbb093c4e7ae6e7eada09ffdbaa4d28854`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 4.0 MB (3955305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc39115291e4d274b7e0282badf83b093f4dbfb6c01e6213fb4ee57cc1166dc9`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:9b012a9e771ea654d5d5ca13df9b16d30c582cbd91b239a6fac4d1261df41dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302041787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84120db8ea77fcfa8688c3eff9973638aa867fa532f1e31f8c14ab72b3a64581`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d5d06d813118d1b82098ef607f6a62da0ee850225501b423d07dfd2711d755`  
		Last Modified: Mon, 03 Mar 2025 21:15:00 GMT  
		Size: 278.1 MB (278122053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:c9bd5c78945d857d38fe8fa1ac884fe625c77e20599616076ad6721182c2f9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e04d921f393c225935b32033dca57f0e95c593bc7adb10b09f97d690f21a8e4`

```dockerfile
```

-	Layers:
	-	`sha256:6814569f1e5d4ef57f4bea7482e085eb9fb50e1857c3855319e7648690f598ae`  
		Last Modified: Mon, 03 Mar 2025 21:14:54 GMT  
		Size: 3.8 MB (3771368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86dd27a840b3d8ec5e099dd6964b60024cf9d327bb8bc7ecae0b35a82d999080`  
		Last Modified: Mon, 03 Mar 2025 21:14:53 GMT  
		Size: 13.4 KB (13378 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2592404bc1c86ee8445a2102a9a6927ac6f91aaa8821a4ff764884ac7984094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352689188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379c3debf1acbd8228d0dac86005b4fe2aa9dae005b2e1d825e5c1462322dd7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51868c8eb2680ac4209dae1f73861b9c082564efc6f5a6b39e39ac0d7d6ff6b5`  
		Last Modified: Mon, 03 Mar 2025 21:29:50 GMT  
		Size: 324.6 MB (324640763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:1e31d6a2695c5af40509bfd2eb1d961a0fb7988b0c1f26bff5d8f6e61c418412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52299a9631b27c74dd842e31aa7e0da8e26a849b4a815ba25015741e88c0ae46`

```dockerfile
```

-	Layers:
	-	`sha256:f273ab084a2e7575d05d06fa8ba8cf7e2d8f8da05b88269989a9ddde03493037`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 4.0 MB (3977648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b19592b0bba92266591738d7b34e3def4520d60096b6a10a024f01b3bedd90e`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-slim` - linux; 386

```console
$ docker pull rust@sha256:88ba2b4761e6d4257c7060aae566853aca592df9e026d748f161b37fb1c2764b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307630505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35b195ee846be85652a54550356ce979af10471acbd66a58ac492de03315688`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a89d68e962de64b429c772557a0e0a429dc425b2a14dcb31802e63de2e4e6bd`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 278.4 MB (278435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b3a7a9e30f6b551540715acbe44f408f539191ad77cc92d3276a74e91dfe0fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed2d74491588bf1f3886ac5c1ba7ef38f7f513a0298f405327e9be21f7af5da`

```dockerfile
```

-	Layers:
	-	`sha256:f2761352b9bb345b81ef703154b559b8e013093b8599a35ed94fdefb3c7327aa`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 3.9 MB (3935220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bacf9a7e03faf1ff9bf9fbd5138346c494c6f27d2ca9c99b3e3b0f5e79c2fe71`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:d17f48a04c1c202eb18025d892fddf578cedbdc537fa56a041db85189882ab6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355168893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8c917d31b3a645483187dd86afa887442274f948403c6ba0cb7530982f308f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a5a9edf391ebe6e786c0c06eb206b9f00800b0262e795ed3ae7f7a0618588f`  
		Last Modified: Mon, 03 Mar 2025 21:16:50 GMT  
		Size: 323.1 MB (323116579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:77418e4a89328c9c95965a089ff40eb2c4ae1bf5bece9a92578f48b38d198a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce5ae98dec6ba000aab82460ddc24921096bc35a28c42968b20cbe7a9b19d05`

```dockerfile
```

-	Layers:
	-	`sha256:9fc9db7381e23b41c20dcc2dea87608b0cf0c9091ea543bafb588a1cbb532d21`  
		Last Modified: Mon, 03 Mar 2025 21:16:33 GMT  
		Size: 3.9 MB (3927866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6eb443440c8ecf14e727b7761eed1b229ee61670c0190619f7a21685eb501b`  
		Last Modified: Mon, 03 Mar 2025 21:16:32 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-slim` - linux; s390x

```console
$ docker pull rust@sha256:5703e183e49c0e1dc763e6bdbe2c9bac4d8b652267f0bb85718f9e1c359f1b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358827701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d0faf0f8207be9497615f4b7573829e4fc8b2977f1a06d02e4b28d030c1d41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078929da424ac5687fa6c367c58665828a7d802e10e816e2ae05060d62a114e9`  
		Last Modified: Mon, 03 Mar 2025 21:15:44 GMT  
		Size: 332.0 MB (331962863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:22316782835c59c254cf08a9f94d0fbf9c7d97933beeca3f7be35411f06e5640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40c95061e80226561af8a4a6448bc3128287baf27bd094ecbb1af08b0ca6d00`

```dockerfile
```

-	Layers:
	-	`sha256:db5d3a28f1d73244b43980f7869840e4d6b6a7e6815101a9c53f1f060eb04089`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 3.8 MB (3797205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f1036a2309ba1a573101a8d36570d74e90b4a1095fdd22f30435cae8bfa61e`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85.0-slim-bookworm`

```console
$ docker pull rust@sha256:215987920101ed15967e9ab4bab3a20e1b71ab3c0551b5088b380e0d4e1758b1
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

### `rust:1.85.0-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:d3d93642ae6fd2cd84c7912184bb459b7b0db7e8faac0426bd6dca3940a8e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292709649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f34a203a3c381506722cf3c29ff282ee2a7a6c3ea5f9122a253e5db711f00a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387149dce16056dbdb4b06942bebd598293454f04bcf825305789d3fbd03ccc2`  
		Last Modified: Mon, 03 Mar 2025 21:14:29 GMT  
		Size: 264.5 MB (264490348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2cadfef9494fded06cb45ac7dd21cf8be95bbc29d29843982b1136d37965399b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b31992db534d2f4beea704cd6f87a532756c8285f835090e85c8f923d989e`

```dockerfile
```

-	Layers:
	-	`sha256:12dde0feb1e98f9767c8a92f79c123cbb093c4e7ae6e7eada09ffdbaa4d28854`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 4.0 MB (3955305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc39115291e4d274b7e0282badf83b093f4dbfb6c01e6213fb4ee57cc1166dc9`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:9b012a9e771ea654d5d5ca13df9b16d30c582cbd91b239a6fac4d1261df41dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302041787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84120db8ea77fcfa8688c3eff9973638aa867fa532f1e31f8c14ab72b3a64581`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d5d06d813118d1b82098ef607f6a62da0ee850225501b423d07dfd2711d755`  
		Last Modified: Mon, 03 Mar 2025 21:15:00 GMT  
		Size: 278.1 MB (278122053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c9bd5c78945d857d38fe8fa1ac884fe625c77e20599616076ad6721182c2f9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e04d921f393c225935b32033dca57f0e95c593bc7adb10b09f97d690f21a8e4`

```dockerfile
```

-	Layers:
	-	`sha256:6814569f1e5d4ef57f4bea7482e085eb9fb50e1857c3855319e7648690f598ae`  
		Last Modified: Mon, 03 Mar 2025 21:14:54 GMT  
		Size: 3.8 MB (3771368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86dd27a840b3d8ec5e099dd6964b60024cf9d327bb8bc7ecae0b35a82d999080`  
		Last Modified: Mon, 03 Mar 2025 21:14:53 GMT  
		Size: 13.4 KB (13378 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2592404bc1c86ee8445a2102a9a6927ac6f91aaa8821a4ff764884ac7984094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352689188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379c3debf1acbd8228d0dac86005b4fe2aa9dae005b2e1d825e5c1462322dd7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51868c8eb2680ac4209dae1f73861b9c082564efc6f5a6b39e39ac0d7d6ff6b5`  
		Last Modified: Mon, 03 Mar 2025 21:29:50 GMT  
		Size: 324.6 MB (324640763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1e31d6a2695c5af40509bfd2eb1d961a0fb7988b0c1f26bff5d8f6e61c418412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52299a9631b27c74dd842e31aa7e0da8e26a849b4a815ba25015741e88c0ae46`

```dockerfile
```

-	Layers:
	-	`sha256:f273ab084a2e7575d05d06fa8ba8cf7e2d8f8da05b88269989a9ddde03493037`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 4.0 MB (3977648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b19592b0bba92266591738d7b34e3def4520d60096b6a10a024f01b3bedd90e`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:88ba2b4761e6d4257c7060aae566853aca592df9e026d748f161b37fb1c2764b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307630505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35b195ee846be85652a54550356ce979af10471acbd66a58ac492de03315688`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a89d68e962de64b429c772557a0e0a429dc425b2a14dcb31802e63de2e4e6bd`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 278.4 MB (278435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b3a7a9e30f6b551540715acbe44f408f539191ad77cc92d3276a74e91dfe0fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed2d74491588bf1f3886ac5c1ba7ef38f7f513a0298f405327e9be21f7af5da`

```dockerfile
```

-	Layers:
	-	`sha256:f2761352b9bb345b81ef703154b559b8e013093b8599a35ed94fdefb3c7327aa`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 3.9 MB (3935220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bacf9a7e03faf1ff9bf9fbd5138346c494c6f27d2ca9c99b3e3b0f5e79c2fe71`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d17f48a04c1c202eb18025d892fddf578cedbdc537fa56a041db85189882ab6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355168893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8c917d31b3a645483187dd86afa887442274f948403c6ba0cb7530982f308f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a5a9edf391ebe6e786c0c06eb206b9f00800b0262e795ed3ae7f7a0618588f`  
		Last Modified: Mon, 03 Mar 2025 21:16:50 GMT  
		Size: 323.1 MB (323116579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:77418e4a89328c9c95965a089ff40eb2c4ae1bf5bece9a92578f48b38d198a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce5ae98dec6ba000aab82460ddc24921096bc35a28c42968b20cbe7a9b19d05`

```dockerfile
```

-	Layers:
	-	`sha256:9fc9db7381e23b41c20dcc2dea87608b0cf0c9091ea543bafb588a1cbb532d21`  
		Last Modified: Mon, 03 Mar 2025 21:16:33 GMT  
		Size: 3.9 MB (3927866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6eb443440c8ecf14e727b7761eed1b229ee61670c0190619f7a21685eb501b`  
		Last Modified: Mon, 03 Mar 2025 21:16:32 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:5703e183e49c0e1dc763e6bdbe2c9bac4d8b652267f0bb85718f9e1c359f1b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358827701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d0faf0f8207be9497615f4b7573829e4fc8b2977f1a06d02e4b28d030c1d41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078929da424ac5687fa6c367c58665828a7d802e10e816e2ae05060d62a114e9`  
		Last Modified: Mon, 03 Mar 2025 21:15:44 GMT  
		Size: 332.0 MB (331962863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:22316782835c59c254cf08a9f94d0fbf9c7d97933beeca3f7be35411f06e5640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40c95061e80226561af8a4a6448bc3128287baf27bd094ecbb1af08b0ca6d00`

```dockerfile
```

-	Layers:
	-	`sha256:db5d3a28f1d73244b43980f7869840e4d6b6a7e6815101a9c53f1f060eb04089`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 3.8 MB (3797205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f1036a2309ba1a573101a8d36570d74e90b4a1095fdd22f30435cae8bfa61e`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.85.0-slim-bullseye`

```console
$ docker pull rust@sha256:e94e2d2e0a9df48fdfcacb47d8b60d036abe60b7c6fa3ac3de1dd16a3d18f19a
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

### `rust:1.85.0-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:dccdc77b5b046c078e76f4ca452308e213f4b7ba3e8a6c215393381d36d5b280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283883304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35d2ada2c353b98b46aff96c86cc0c21d362da854c48fcd0aa754b13b83eb20`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e0052749e7f2c9ab3a91aad47ad13df4c7c8911c162e2bdb7d08f691e99aac`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 253.6 MB (253629374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:19d324bd0c298ad1b3f5e6df1ce1df18225864b216efbb6c90ddce0a8ce24642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c80060630492f3b3f74f9d388000b5067bc23694bacc999541e6da57bf59ff`

```dockerfile
```

-	Layers:
	-	`sha256:df56ae19c38d79a9c6b3901f1921d9c3833a93218a082679bdb0a12883f3905e`  
		Last Modified: Mon, 03 Mar 2025 21:14:22 GMT  
		Size: 4.2 MB (4173204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9fc1edc1c95e2a303e127182409fafb9fc9e2d3f3ad0da80b896cad7720daaa`  
		Last Modified: Mon, 03 Mar 2025 21:14:21 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:1c291529dbe66cd22592a3d8ecc5cead222cb64a3d43b8aaadfa065746e28570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297882666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e350660ab01bd40fd4abffb3fd8ba3d377659d12c689daca3b6779053172617`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0ca501b624d9dae81049df15e1024733ee21141b25f8ca123d98e0d13df5d12`  
		Last Modified: Tue, 25 Feb 2025 01:31:18 GMT  
		Size: 25.5 MB (25535432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6d72cafe6043b15f5dabf082f52f18a84a9ac04dfbfe5fc6bba3fcbe37edd0`  
		Last Modified: Mon, 03 Mar 2025 21:20:57 GMT  
		Size: 272.3 MB (272347234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:07cd7090e5192facfdd11a8b0ed54d90c6c4f804c8c9a9059c3d3e7ba657c970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612130ff6bdfd39ede8255ddb232e9327ffb825112e6bb1017c80060be9e9c7d`

```dockerfile
```

-	Layers:
	-	`sha256:73bc2806f7ecf2f20576c7878e9d5e9b7dfc3b25b6132689e08490bce610f038`  
		Last Modified: Mon, 03 Mar 2025 21:20:39 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f927f926449a4f38eeebab517940bd75ca9acef94ae1a163391730411486b20`  
		Last Modified: Mon, 03 Mar 2025 21:20:38 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:de9c5b13bcc43221f1603fb03089d27e59603e8087525be9302e30fa4a75e3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343069561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e422222ab9bba42554ec25e8f7656f35c48de3d1930f29223b4c40648547e500`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ae7537677409c7e96b2e534829fe706743a9e1c1fc79c0e6c3a6ae631021d1`  
		Last Modified: Mon, 03 Mar 2025 21:34:48 GMT  
		Size: 314.3 MB (314323574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:cb9b665a79ff9d7407b5196e20d85e27ec9c2216b78c66b5a1dfa4a438542750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b594182c132405732dc65dec31b847e10c0314703f603d9728caf021dd2f8c3`

```dockerfile
```

-	Layers:
	-	`sha256:f87a9a1c38fe1dae028e9162ed79be83deebf92138b807780b636247a977d593`  
		Last Modified: Mon, 03 Mar 2025 21:34:40 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0c9191b26a4828e5bd697af4e870ad8de930043587eddf2407e36a5f19df4ea`  
		Last Modified: Mon, 03 Mar 2025 21:34:40 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.85.0-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:8ce46ac85186e75d85f9912eaea882d8fab038755ad48d921a2974b006f800a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302583357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66df80913375cbd40ebb9b025095b1856d1454a6206427f78c4846d5b5771158`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc6ac53dd3c2cb0c6fd992e5925fc15a335691c21c9dc26765ed22ae0d20371`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 271.4 MB (271402930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.85.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e925605333c9a3842c68db47ba3d21c3ba0539ccbf18a0231b3a8cfacca912b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55c2e9da4484fa31efbf5cc3c8d14b787bc24da1ef1871ff26f4e0ac811f26d`

```dockerfile
```

-	Layers:
	-	`sha256:d0d87fc423e5c2445348c3696ac9ef20a4fae6bfa1ceebb2a4a2a6b7af161b60`  
		Last Modified: Mon, 03 Mar 2025 21:14:33 GMT  
		Size: 4.2 MB (4163461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714de8d934c25f3276ae4b994be3302532085a4c69860853de35ef86540dd876`  
		Last Modified: Mon, 03 Mar 2025 21:14:33 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:1030547bd568497d69e41771ada279179f0613369dc54779e46a3f6f376b3020
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:84b5e9c7c2f9437f62769913b419cc02a1e310bf40fd86720cd2b3b64bffb452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304368783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec94ecf18f99333d5bd8f2a15427ba1b4736299f4d5f4a35660f5fe75b6291a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b95e11be61c0eea8aadf788692bf0fcec5f9c75738d3f5713dfbcc016f337f4`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 61.6 MB (61565003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6fc4d476520099dcd8ba0f71c1e15bb2d762c9977506070eea6cb78a2a4c6`  
		Last Modified: Mon, 03 Mar 2025 21:14:31 GMT  
		Size: 239.2 MB (239161533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:d8cff90939ad06ca11df0fc881253dc5d1d768c2221f8466415334d2739cbfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4955895d71a1f61c0886f29ea5b6a23986cda0a9910e8ba13ff472aff21cac1f`

```dockerfile
```

-	Layers:
	-	`sha256:fd7a8c7ea021f7804add54b5f5efd33149b2e2c7d915f1622744e64dbbe08c7c`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457f860b4e4d19a0674d0ca4f6ec06ff6958c351407559ee9c974d2b3bbca63f`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bda9e5682eeb0013c19b06e469812ae54cbe76cf0128796def8eb9bfe30a5c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307415047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72195abfac34db128f0c99e35ad0a1a98210b81274e98b65ac2973dae8aeb0dd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b46568d489c620031542c16213dea9e63b74c664a11f85b1bb86a8e526e5a16`  
		Last Modified: Mon, 03 Mar 2025 21:23:23 GMT  
		Size: 59.1 MB (59101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51de9687e383104ad782ecb8afe38b4c33220f4e646112f07f0e47d399d0a9fd`  
		Last Modified: Mon, 03 Mar 2025 21:23:28 GMT  
		Size: 244.3 MB (244320886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:429bfdee3cf71b49563ad904faf2875e578ae734980bd44b1c38b27f5855fd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d07c59fd4b9553baf3c76bd773969e82fed14c0dcfa7ca467660406d07156`

```dockerfile
```

-	Layers:
	-	`sha256:fbed74b3e0b30a9432fe2ba4b82f04cb881dd5c6f374c1aff1f3d2f2018fb7f3`  
		Last Modified: Mon, 03 Mar 2025 21:23:22 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81eca9cb1582aed143c4d744ce7a925b1e10e4678aaf0916e76d40846bb2d61`  
		Last Modified: Mon, 03 Mar 2025 21:23:21 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.20`

```console
$ docker pull rust@sha256:f0cef6c65992995b1c7816cb667de95799852e3fbed9d06f95855cbc512a0fd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:6d824fef86a8532aecead5889d49d432d19e0dd58b958266c994cca9eb7a3357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298102813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c38e59fb99c1014ea6d250d396bb9bf55981f1d69fe17ed05047b90cd119ca9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0430b4a2b30329b0c06034d1df61c2f3533c436834a54b76def8756d804d888`  
		Last Modified: Mon, 03 Mar 2025 21:17:28 GMT  
		Size: 55.3 MB (55315558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fda7dd06f6e434e3727cd86155430a51568846533e3824548334e20f1078e28`  
		Last Modified: Mon, 03 Mar 2025 21:17:31 GMT  
		Size: 239.2 MB (239160358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:ab2a41c3a86b0e8de97e1cff7ca3624a6e69e478c7c29615df5979d5655d03c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e987a7ec625942a721de02dcd92bf4ea3f7481ee651c6aef639e3a2f3f16ba`

```dockerfile
```

-	Layers:
	-	`sha256:4100e90a822ec6152c54ec22e8ce0b4cfb24694b82b0d9252e191958ce4d59cf`  
		Last Modified: Mon, 03 Mar 2025 21:17:28 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca3c1b9b1144fd4038e19dea5e9afef77e4732804442cc1813ffcbd1c7289e4`  
		Last Modified: Mon, 03 Mar 2025 21:17:27 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f91c5c68a69111314bb721b7bb75aaa4b310b9ef676f2591e88769bbbb3bd933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301363171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61566cb96efc54b3ee29f6409c0e76059ca7b3c261b99a2940c188c54c3a66c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c8bee9c91c68545cb9604a6baaf13f4c921f1a8a851437cc7ce63f942e113d`  
		Last Modified: Mon, 03 Mar 2025 21:26:24 GMT  
		Size: 53.0 MB (52950488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998e7300919f154807a1ce8bdaa868228719c39a95b4c276a758f1bf480b361`  
		Last Modified: Mon, 03 Mar 2025 21:26:28 GMT  
		Size: 244.3 MB (244321518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:1e4651facc4a66b01c40f8bec063469f936cbf603daf477c1003e794040d3e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beeb6c0426bb32cbdd133d31ad5ed10820561b72d66e1d95f332bfb42d012779`

```dockerfile
```

-	Layers:
	-	`sha256:183ceb0143fb3784d416af0d9e6e49059191e33606b5db6d715b5666f0fd139b`  
		Last Modified: Mon, 03 Mar 2025 21:26:22 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe75a1adc68e5615e04f2ea23b7e198a996bb1378319d115d5ca7b6fbef7602`  
		Last Modified: Mon, 03 Mar 2025 21:26:22 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.21`

```console
$ docker pull rust@sha256:1030547bd568497d69e41771ada279179f0613369dc54779e46a3f6f376b3020
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:84b5e9c7c2f9437f62769913b419cc02a1e310bf40fd86720cd2b3b64bffb452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.4 MB (304368783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec94ecf18f99333d5bd8f2a15427ba1b4736299f4d5f4a35660f5fe75b6291a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b95e11be61c0eea8aadf788692bf0fcec5f9c75738d3f5713dfbcc016f337f4`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 61.6 MB (61565003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6fc4d476520099dcd8ba0f71c1e15bb2d762c9977506070eea6cb78a2a4c6`  
		Last Modified: Mon, 03 Mar 2025 21:14:31 GMT  
		Size: 239.2 MB (239161533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:d8cff90939ad06ca11df0fc881253dc5d1d768c2221f8466415334d2739cbfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4955895d71a1f61c0886f29ea5b6a23986cda0a9910e8ba13ff472aff21cac1f`

```dockerfile
```

-	Layers:
	-	`sha256:fd7a8c7ea021f7804add54b5f5efd33149b2e2c7d915f1622744e64dbbe08c7c`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457f860b4e4d19a0674d0ca4f6ec06ff6958c351407559ee9c974d2b3bbca63f`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bda9e5682eeb0013c19b06e469812ae54cbe76cf0128796def8eb9bfe30a5c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307415047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72195abfac34db128f0c99e35ad0a1a98210b81274e98b65ac2973dae8aeb0dd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='55a7f503ce16250d1ffb227f0fa7aa8a9305924dca2890957c7fec7a4888111c' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='415c9461158325e0d58af7f8fc61e85cd7f079e93f9784d266c5ee9c95ed762c' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b46568d489c620031542c16213dea9e63b74c664a11f85b1bb86a8e526e5a16`  
		Last Modified: Mon, 03 Mar 2025 21:23:23 GMT  
		Size: 59.1 MB (59101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51de9687e383104ad782ecb8afe38b4c33220f4e646112f07f0e47d399d0a9fd`  
		Last Modified: Mon, 03 Mar 2025 21:23:28 GMT  
		Size: 244.3 MB (244320886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:429bfdee3cf71b49563ad904faf2875e578ae734980bd44b1c38b27f5855fd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d07c59fd4b9553baf3c76bd773969e82fed14c0dcfa7ca467660406d07156`

```dockerfile
```

-	Layers:
	-	`sha256:fbed74b3e0b30a9432fe2ba4b82f04cb881dd5c6f374c1aff1f3d2f2018fb7f3`  
		Last Modified: Mon, 03 Mar 2025 21:23:22 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81eca9cb1582aed143c4d744ce7a925b1e10e4678aaf0916e76d40846bb2d61`  
		Last Modified: Mon, 03 Mar 2025 21:23:21 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:e15c642b487dd013b2e425d001d32927391aca787ac582b98cca72234d466b60
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
$ docker pull rust@sha256:f6fc45b5a8d3b72dcff6442b5311f0b1f854a3480797f91ecbfb16c0fd5d4527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.0 MB (541963415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aac1c9ca934dcc8a2f93033651d5f86fb3b99783c81428ecce40198d4abc0af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c03d5625da4fd65f189b350dab8fda9ce3054bdd41f9a509973b3cd0cd571e`  
		Last Modified: Mon, 03 Mar 2025 21:14:28 GMT  
		Size: 193.7 MB (193695926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4d1be75651ae6516c73cd01fb804f023e4d53bdf2b9d5cb9e5a78381266818c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca03f69ea0d5d937b5bf2bba4b75d5a4cb308e7460975b526f3138436e1a7f7b`

```dockerfile
```

-	Layers:
	-	`sha256:f2aa5e71de5c6e138f09eb61c0c64219101f7290d0719c4e4f2763b9cbbcafa9`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 15.5 MB (15474256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bfe55c7c856b4e205d1086d7f00a0c16d9544ceb0316ec5f5368e8f86a5a815`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:cb81fdf6321d7de7b04a0978a0f1af3d2ce2e9b5302a619b7d538132a0d783bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531318143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cba7271ee5cf51b3565fbb44d531aa336955fdf97d4159e8544e9e1ede35187`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70e25650a3be5d12fed3dfd4069f605d42d17b86fa4c689b69aa636aee22155`  
		Last Modified: Mon, 03 Mar 2025 21:18:08 GMT  
		Size: 230.3 MB (230264903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c6712addcc809b8eb0fe21d81f7f7eba0637e2838086b119dcbbc41e4187a6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e9006d373cfef0bc4e89bb17079c2f22f1ae42ed8a2b7dcd57d4b3c67b04c9`

```dockerfile
```

-	Layers:
	-	`sha256:fab2c1c1f543fac09d7660a2054a25708a28b23b14e1f1c9a3a6e1644e54b678`  
		Last Modified: Mon, 03 Mar 2025 21:18:02 GMT  
		Size: 15.3 MB (15278698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f349b53969dfbfa675b8173f92a74dbd59458f6214685c9dd2c7318179f6cc32`  
		Last Modified: Mon, 03 Mar 2025 21:18:01 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be252dc02478902ea4c4a6e1e2b49181f1fa3aaeb96a47e40dc248b2598cf243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.8 MB (597772744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192cc1afeb41abe7df5d2c3f94eb7e40a991156c86412ad4cab156f754d7f291`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b5a4332d3d01f663d9e0b5d8a153c25ca20c2d7e94ce224b627a88380da001`  
		Last Modified: Mon, 03 Mar 2025 21:31:31 GMT  
		Size: 258.8 MB (258797571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0cea832fdaaa30a9c04e35a4d5de0ede3f8723564efacebd2cae817dba8af26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef22842e59d31eab71173da3ae37fbcabd9b445839c9e49ffa7b0d93c64a8f51`

```dockerfile
```

-	Layers:
	-	`sha256:463dc9b45f12289d11de3d7eaffa14e7641471dd399b68728748be80a572fea3`  
		Last Modified: Mon, 03 Mar 2025 21:31:25 GMT  
		Size: 15.5 MB (15502831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:479aac264bc9d5563cda8973c1adf5fcc9d667f916488c189c512d2bb1d18d12`  
		Last Modified: Mon, 03 Mar 2025 21:31:24 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:c3ba8ba76e08440fcff73d04693fef720530890076f46b8761da0dddcedadb78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.7 MB (561694245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676197b0baccfd7dd45db61469de196ac15950aa10debfbcd2b0583af2dafed4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca163299b0e606d2916a03bd0f60c5903c6e5abeab65da3a8c490174697c929`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 24.9 MB (24899353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c3400be327e90dc9e848a16d4b0fcd191708de152e68c6b4888d83c61f441`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 66.2 MB (66237814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3ca8ca718f538c2871c3deeec438c611f0f26a3b97976b89d6d6abcca894dd`  
		Last Modified: Tue, 25 Feb 2025 05:12:06 GMT  
		Size: 210.3 MB (210255482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c5735fe88e109ded1d53e0e079c60705e16af5652ea6c119760594e52d6fb`  
		Last Modified: Mon, 03 Mar 2025 21:14:43 GMT  
		Size: 210.8 MB (210843144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8c10ae28c24f12a5b3e3598c4abb8a26206a7edef522211dc27667c598621f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5c3c563ea6d86b133dd81fc4d8eaecefc99bc076f1c075059797e8116f36d3`

```dockerfile
```

-	Layers:
	-	`sha256:0ab28f08ca6a412da7f3016c8c2eb5dc331d3000a50c38114eb87924f817b53a`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 15.5 MB (15451518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd3c3e28ee8144d301f821eb5b432e99ec8f8776af706e07ba3a04d48e6f7ac`  
		Last Modified: Mon, 03 Mar 2025 21:14:37 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:0fe5e17dc44d5fdbd2560266262d98e813b49ca1e9b0ba23d9b3675fe2adacb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.6 MB (616586281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d35305b8c7077eb68baa8b585fec750d11f2afc7094e64b59f8e368246879`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad13c90d099a380a8fc2ec9ef74de7ad957b1496d75b8d1c4617069765510053`  
		Last Modified: Mon, 03 Mar 2025 21:24:43 GMT  
		Size: 254.3 MB (254345476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0676ad8c84ebbb134f5e3c3aab74a661c1ac924ee0fa1a042d90d7fbadfc4585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ad946c6e11f49c09021728047cc0f3fa4a83f0101fa1031085c8f8e0d2ca1c`

```dockerfile
```

-	Layers:
	-	`sha256:14a5009de22d0268d16a06051e63b1bd4e5a83615d08555e021663ada543f0e2`  
		Last Modified: Mon, 03 Mar 2025 21:24:31 GMT  
		Size: 15.4 MB (15449362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e237236a91844fef1f239951791ab5549d6226f7a182592fa6867fc48d952279`  
		Last Modified: Mon, 03 Mar 2025 21:24:28 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:70fe5668b3762d8a81b5059f9c4bad31ac92bf152d57195193c433368ec36f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599864262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b0dc30045f5d2e53b0a2a92cd31f6f8e3bdeca4ccb1165d6d2ac3cdcf807a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f679165548785dd187eaea9af4ee69db5b37630f35ce564d064cd7512fcfb9`  
		Last Modified: Mon, 03 Mar 2025 21:31:35 GMT  
		Size: 281.8 MB (281820436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:dbf40b3fd37699736f3445354654c43b50a382b3ef92f0ea8de4366bcc1af9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d288575d5989682a9df5b6cb7dc314ca8e3380685956acf21030572b2fe26d2e`

```dockerfile
```

-	Layers:
	-	`sha256:83fad1cb4c19e71cbc100ba5c079f7fda458db61bafa47c1cc48e228ce18802f`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 15.3 MB (15286944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4d7f0c7c0907b0c5b392d225150310f20e92d9173b7a16ce384cd7507427f6`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:6cb2cf341137cabc58d05942ca17e31c2c973ee50e2dac8bef4c0edc4e9e21ac
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
$ docker pull rust@sha256:4774472306a1c334734103f7bf6231ad1370d4f71c2ae394fe8978afac5b2e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.8 MB (514821415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63309be2c0345cac77307aa173b9782aa5a84f553951abd498d16f5c04a4fa8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bcbc2151ce4be9aa40b26468719dafd6528d7d11d6f6cb60e3a58a3447305`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 15.6 MB (15558424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36295709cc3855d0f98f8a6b939053cc43efcf3092756703c1fc518d73fe77`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 54.8 MB (54752085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e451f55144f64f697f2945598b3a000bbac10e699d6068b7d6e63f9aa2b7f3b5`  
		Last Modified: Tue, 25 Feb 2025 04:17:48 GMT  
		Size: 197.1 MB (197074397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c39801b95216b4260c69cafb56f78679aec6c847d1e3d1afc1de560c4cd5e9`  
		Last Modified: Mon, 03 Mar 2025 21:14:42 GMT  
		Size: 193.7 MB (193695108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:2ee0d74ac110bd1a17d8332af3912202fbe343a4a38370a9db6bc9fa364b9d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd28e732df28539d58b7d7f26dacd50370d93acc3d43ba5ae570174138f6aec`

```dockerfile
```

-	Layers:
	-	`sha256:b0537ca4f5998de091de7aadced2002bc586c005466354e27181079037c37733`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 15.1 MB (15073413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:323b971a0322980ccb6d5b56d28083ac175e1bd00757315708f1421f1797d01f`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:2ac2d9029c9950551413e86bd26d8ad86f61590dd45bb4cd2da0a4b001432ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.1 MB (512134009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5029ae4b22101f3709c37ae1b0f1483b2f9ff3209787eb6e49ad590cad55da6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b371c05b17ddc4521fa62e27633ef500c9e18d0922c933dc30ad692d163a6adb`  
		Last Modified: Tue, 25 Feb 2025 01:31:01 GMT  
		Size: 49.0 MB (49026733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce7f37fed942ce7eb6947b63b02cebac1a836c49ae19b59c3dfd4d0dafde5e9`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 14.7 MB (14673973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3908d2a88cdaeb59d430f53cffe54008e1006a05c4aa7a391f2dce9c9b9aff8`  
		Last Modified: Tue, 25 Feb 2025 14:18:51 GMT  
		Size: 50.6 MB (50640099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a931f277cb7dadd19c4ea31b7570c91e754bb6d034542896c14a613c77034a3e`  
		Last Modified: Tue, 25 Feb 2025 16:54:04 GMT  
		Size: 167.5 MB (167527903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8016ff31b139f4cc1ac2b37027c3a5c553771198a19e3563f9ebcc51e15f4999`  
		Last Modified: Mon, 03 Mar 2025 21:23:09 GMT  
		Size: 230.3 MB (230265301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0bd6feae8faa96fd3e378eaa561081d1edabb91e202219f3fa32d7468381c067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c7808076946af42d45e2924dc9a57c449d7f6c9539ed7801a920d87def0c75`

```dockerfile
```

-	Layers:
	-	`sha256:afaa1ab536f6764953fbf3d43692672f51fc56aa085586bfb78431ead85f5d36`  
		Last Modified: Mon, 03 Mar 2025 21:23:04 GMT  
		Size: 14.9 MB (14874204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d11f72eaf746d2a6aa73bdc233abd05555878019f6832b3a21234f539567442`  
		Last Modified: Mon, 03 Mar 2025 21:23:03 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5d6e25360f6d028455c8b643f8f53d7c4efbc0064b23759608b61ad6a3adc223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.4 MB (571431917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1371eb80ca3e9f7fe5098765803837081bef8ff5751aecccc695e544f321dec2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364a649b3acc0e2c47a31825e92a687c9eae217b5c8c062f3efaabe7bec06f7`  
		Last Modified: Tue, 25 Feb 2025 05:42:11 GMT  
		Size: 15.5 MB (15544146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8a227b92685cb13561fe06ec9cfa79231e26157c7e163ab5b9af993e63bd10`  
		Last Modified: Tue, 25 Feb 2025 11:54:42 GMT  
		Size: 54.9 MB (54855421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bd61bef017e8e3b4e6f403c074fa47f738d2ac56d92eb50f50fff5dc8bd03`  
		Last Modified: Tue, 25 Feb 2025 15:23:19 GMT  
		Size: 190.0 MB (189986146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0073060607bc719b0aa94e147a0b6b03b6aefcd068fff7a78b8f947eecf9d5`  
		Last Modified: Mon, 03 Mar 2025 21:36:29 GMT  
		Size: 258.8 MB (258797560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7c24d055c4c4a49c2b849357293da9e9e2988140bdd4d982de7271f0e3143c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ebf36916e6fb93d90caf00958262c0c8b9c86735cb8958a061bbc281f3fd85`

```dockerfile
```

-	Layers:
	-	`sha256:493bc9dc75ddde0e35de2091d2eac442ce52714aa89a6f684f07608dbbcc2dea`  
		Last Modified: Mon, 03 Mar 2025 21:36:24 GMT  
		Size: 15.1 MB (15075673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44037f8c5cd51ccebdbaed303063aa1b879764d15ae47c490d35c0fe101c959f`  
		Last Modified: Mon, 03 Mar 2025 21:36:24 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:d96bbc13b6e3f5741b38e2d39e57c378073d01c5cf0f2e18023d0bf7c730098a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.6 MB (537592438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fb3dfd29980bf4e4cf1a785df10f73d2a9093d02a06e3fb1789e2e0670f645`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1763bdfcd7e692c8f35c71602a5206ff9e4716856edf6ae712febb4cc579d3`  
		Last Modified: Tue, 25 Feb 2025 02:24:11 GMT  
		Size: 16.1 MB (16062177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820de11811e966e41fc39b6790cf28a33ce0645127033d9f041fa3707235430e`  
		Last Modified: Tue, 25 Feb 2025 03:13:43 GMT  
		Size: 56.0 MB (56030023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa00228844a300b416d3473480cea8953822058ab89fc86d0c3c4056d2fe123`  
		Last Modified: Tue, 25 Feb 2025 04:18:06 GMT  
		Size: 200.0 MB (199978138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883849d920b1b05e06838787b545a094134ce0719a6b7b9f208333a79ce9a242`  
		Last Modified: Mon, 03 Mar 2025 21:14:43 GMT  
		Size: 210.8 MB (210843237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:16c416c5f5c143b8d3d0444b211b06b0f4ce71c2d44bab44374d6c8e196621f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5baa792f584e43afed942f1cb227670cfbb389df99f48d8914c3676ae81592e`

```dockerfile
```

-	Layers:
	-	`sha256:6a66d8cce735ea8c5513f850111cf3a06be5855d644d3836537665c230246349`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 15.1 MB (15060440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4f74ec7a17331b1624aac92a9d8ebad6de4e7c0902f293d6a7495e63d14e456`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:e15c642b487dd013b2e425d001d32927391aca787ac582b98cca72234d466b60
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
$ docker pull rust@sha256:f6fc45b5a8d3b72dcff6442b5311f0b1f854a3480797f91ecbfb16c0fd5d4527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.0 MB (541963415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aac1c9ca934dcc8a2f93033651d5f86fb3b99783c81428ecce40198d4abc0af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c03d5625da4fd65f189b350dab8fda9ce3054bdd41f9a509973b3cd0cd571e`  
		Last Modified: Mon, 03 Mar 2025 21:14:28 GMT  
		Size: 193.7 MB (193695926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:4d1be75651ae6516c73cd01fb804f023e4d53bdf2b9d5cb9e5a78381266818c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca03f69ea0d5d937b5bf2bba4b75d5a4cb308e7460975b526f3138436e1a7f7b`

```dockerfile
```

-	Layers:
	-	`sha256:f2aa5e71de5c6e138f09eb61c0c64219101f7290d0719c4e4f2763b9cbbcafa9`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 15.5 MB (15474256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bfe55c7c856b4e205d1086d7f00a0c16d9544ceb0316ec5f5368e8f86a5a815`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:cb81fdf6321d7de7b04a0978a0f1af3d2ce2e9b5302a619b7d538132a0d783bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.3 MB (531318143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cba7271ee5cf51b3565fbb44d531aa336955fdf97d4159e8544e9e1ede35187`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70e25650a3be5d12fed3dfd4069f605d42d17b86fa4c689b69aa636aee22155`  
		Last Modified: Mon, 03 Mar 2025 21:18:08 GMT  
		Size: 230.3 MB (230264903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:c6712addcc809b8eb0fe21d81f7f7eba0637e2838086b119dcbbc41e4187a6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e9006d373cfef0bc4e89bb17079c2f22f1ae42ed8a2b7dcd57d4b3c67b04c9`

```dockerfile
```

-	Layers:
	-	`sha256:fab2c1c1f543fac09d7660a2054a25708a28b23b14e1f1c9a3a6e1644e54b678`  
		Last Modified: Mon, 03 Mar 2025 21:18:02 GMT  
		Size: 15.3 MB (15278698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f349b53969dfbfa675b8173f92a74dbd59458f6214685c9dd2c7318179f6cc32`  
		Last Modified: Mon, 03 Mar 2025 21:18:01 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be252dc02478902ea4c4a6e1e2b49181f1fa3aaeb96a47e40dc248b2598cf243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.8 MB (597772744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192cc1afeb41abe7df5d2c3f94eb7e40a991156c86412ad4cab156f754d7f291`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b5a4332d3d01f663d9e0b5d8a153c25ca20c2d7e94ce224b627a88380da001`  
		Last Modified: Mon, 03 Mar 2025 21:31:31 GMT  
		Size: 258.8 MB (258797571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:0cea832fdaaa30a9c04e35a4d5de0ede3f8723564efacebd2cae817dba8af26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef22842e59d31eab71173da3ae37fbcabd9b445839c9e49ffa7b0d93c64a8f51`

```dockerfile
```

-	Layers:
	-	`sha256:463dc9b45f12289d11de3d7eaffa14e7641471dd399b68728748be80a572fea3`  
		Last Modified: Mon, 03 Mar 2025 21:31:25 GMT  
		Size: 15.5 MB (15502831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:479aac264bc9d5563cda8973c1adf5fcc9d667f916488c189c512d2bb1d18d12`  
		Last Modified: Mon, 03 Mar 2025 21:31:24 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:c3ba8ba76e08440fcff73d04693fef720530890076f46b8761da0dddcedadb78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.7 MB (561694245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676197b0baccfd7dd45db61469de196ac15950aa10debfbcd2b0583af2dafed4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca163299b0e606d2916a03bd0f60c5903c6e5abeab65da3a8c490174697c929`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 24.9 MB (24899353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c3400be327e90dc9e848a16d4b0fcd191708de152e68c6b4888d83c61f441`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 66.2 MB (66237814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3ca8ca718f538c2871c3deeec438c611f0f26a3b97976b89d6d6abcca894dd`  
		Last Modified: Tue, 25 Feb 2025 05:12:06 GMT  
		Size: 210.3 MB (210255482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c5735fe88e109ded1d53e0e079c60705e16af5652ea6c119760594e52d6fb`  
		Last Modified: Mon, 03 Mar 2025 21:14:43 GMT  
		Size: 210.8 MB (210843144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:8c10ae28c24f12a5b3e3598c4abb8a26206a7edef522211dc27667c598621f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5c3c563ea6d86b133dd81fc4d8eaecefc99bc076f1c075059797e8116f36d3`

```dockerfile
```

-	Layers:
	-	`sha256:0ab28f08ca6a412da7f3016c8c2eb5dc331d3000a50c38114eb87924f817b53a`  
		Last Modified: Mon, 03 Mar 2025 21:14:38 GMT  
		Size: 15.5 MB (15451518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd3c3e28ee8144d301f821eb5b432e99ec8f8776af706e07ba3a04d48e6f7ac`  
		Last Modified: Mon, 03 Mar 2025 21:14:37 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:0fe5e17dc44d5fdbd2560266262d98e813b49ca1e9b0ba23d9b3675fe2adacb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.6 MB (616586281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d35305b8c7077eb68baa8b585fec750d11f2afc7094e64b59f8e368246879`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad13c90d099a380a8fc2ec9ef74de7ad957b1496d75b8d1c4617069765510053`  
		Last Modified: Mon, 03 Mar 2025 21:24:43 GMT  
		Size: 254.3 MB (254345476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:0676ad8c84ebbb134f5e3c3aab74a661c1ac924ee0fa1a042d90d7fbadfc4585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ad946c6e11f49c09021728047cc0f3fa4a83f0101fa1031085c8f8e0d2ca1c`

```dockerfile
```

-	Layers:
	-	`sha256:14a5009de22d0268d16a06051e63b1bd4e5a83615d08555e021663ada543f0e2`  
		Last Modified: Mon, 03 Mar 2025 21:24:31 GMT  
		Size: 15.4 MB (15449362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e237236a91844fef1f239951791ab5549d6226f7a182592fa6867fc48d952279`  
		Last Modified: Mon, 03 Mar 2025 21:24:28 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:70fe5668b3762d8a81b5059f9c4bad31ac92bf152d57195193c433368ec36f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599864262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b0dc30045f5d2e53b0a2a92cd31f6f8e3bdeca4ccb1165d6d2ac3cdcf807a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f679165548785dd187eaea9af4ee69db5b37630f35ce564d064cd7512fcfb9`  
		Last Modified: Mon, 03 Mar 2025 21:31:35 GMT  
		Size: 281.8 MB (281820436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:dbf40b3fd37699736f3445354654c43b50a382b3ef92f0ea8de4366bcc1af9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d288575d5989682a9df5b6cb7dc314ca8e3380685956acf21030572b2fe26d2e`

```dockerfile
```

-	Layers:
	-	`sha256:83fad1cb4c19e71cbc100ba5c079f7fda458db61bafa47c1cc48e228ce18802f`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 15.3 MB (15286944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4d7f0c7c0907b0c5b392d225150310f20e92d9173b7a16ce384cd7507427f6`  
		Last Modified: Mon, 03 Mar 2025 21:31:30 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:215987920101ed15967e9ab4bab3a20e1b71ab3c0551b5088b380e0d4e1758b1
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
$ docker pull rust@sha256:d3d93642ae6fd2cd84c7912184bb459b7b0db7e8faac0426bd6dca3940a8e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292709649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f34a203a3c381506722cf3c29ff282ee2a7a6c3ea5f9122a253e5db711f00a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387149dce16056dbdb4b06942bebd598293454f04bcf825305789d3fbd03ccc2`  
		Last Modified: Mon, 03 Mar 2025 21:14:29 GMT  
		Size: 264.5 MB (264490348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:2cadfef9494fded06cb45ac7dd21cf8be95bbc29d29843982b1136d37965399b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b31992db534d2f4beea704cd6f87a532756c8285f835090e85c8f923d989e`

```dockerfile
```

-	Layers:
	-	`sha256:12dde0feb1e98f9767c8a92f79c123cbb093c4e7ae6e7eada09ffdbaa4d28854`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 4.0 MB (3955305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc39115291e4d274b7e0282badf83b093f4dbfb6c01e6213fb4ee57cc1166dc9`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:9b012a9e771ea654d5d5ca13df9b16d30c582cbd91b239a6fac4d1261df41dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302041787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84120db8ea77fcfa8688c3eff9973638aa867fa532f1e31f8c14ab72b3a64581`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d5d06d813118d1b82098ef607f6a62da0ee850225501b423d07dfd2711d755`  
		Last Modified: Mon, 03 Mar 2025 21:15:00 GMT  
		Size: 278.1 MB (278122053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:c9bd5c78945d857d38fe8fa1ac884fe625c77e20599616076ad6721182c2f9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e04d921f393c225935b32033dca57f0e95c593bc7adb10b09f97d690f21a8e4`

```dockerfile
```

-	Layers:
	-	`sha256:6814569f1e5d4ef57f4bea7482e085eb9fb50e1857c3855319e7648690f598ae`  
		Last Modified: Mon, 03 Mar 2025 21:14:54 GMT  
		Size: 3.8 MB (3771368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86dd27a840b3d8ec5e099dd6964b60024cf9d327bb8bc7ecae0b35a82d999080`  
		Last Modified: Mon, 03 Mar 2025 21:14:53 GMT  
		Size: 13.4 KB (13378 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2592404bc1c86ee8445a2102a9a6927ac6f91aaa8821a4ff764884ac7984094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352689188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379c3debf1acbd8228d0dac86005b4fe2aa9dae005b2e1d825e5c1462322dd7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51868c8eb2680ac4209dae1f73861b9c082564efc6f5a6b39e39ac0d7d6ff6b5`  
		Last Modified: Mon, 03 Mar 2025 21:29:50 GMT  
		Size: 324.6 MB (324640763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:1e31d6a2695c5af40509bfd2eb1d961a0fb7988b0c1f26bff5d8f6e61c418412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52299a9631b27c74dd842e31aa7e0da8e26a849b4a815ba25015741e88c0ae46`

```dockerfile
```

-	Layers:
	-	`sha256:f273ab084a2e7575d05d06fa8ba8cf7e2d8f8da05b88269989a9ddde03493037`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 4.0 MB (3977648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b19592b0bba92266591738d7b34e3def4520d60096b6a10a024f01b3bedd90e`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:88ba2b4761e6d4257c7060aae566853aca592df9e026d748f161b37fb1c2764b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307630505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35b195ee846be85652a54550356ce979af10471acbd66a58ac492de03315688`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a89d68e962de64b429c772557a0e0a429dc425b2a14dcb31802e63de2e4e6bd`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 278.4 MB (278435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:b3a7a9e30f6b551540715acbe44f408f539191ad77cc92d3276a74e91dfe0fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed2d74491588bf1f3886ac5c1ba7ef38f7f513a0298f405327e9be21f7af5da`

```dockerfile
```

-	Layers:
	-	`sha256:f2761352b9bb345b81ef703154b559b8e013093b8599a35ed94fdefb3c7327aa`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 3.9 MB (3935220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bacf9a7e03faf1ff9bf9fbd5138346c494c6f27d2ca9c99b3e3b0f5e79c2fe71`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:d17f48a04c1c202eb18025d892fddf578cedbdc537fa56a041db85189882ab6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355168893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8c917d31b3a645483187dd86afa887442274f948403c6ba0cb7530982f308f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a5a9edf391ebe6e786c0c06eb206b9f00800b0262e795ed3ae7f7a0618588f`  
		Last Modified: Mon, 03 Mar 2025 21:16:50 GMT  
		Size: 323.1 MB (323116579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:77418e4a89328c9c95965a089ff40eb2c4ae1bf5bece9a92578f48b38d198a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce5ae98dec6ba000aab82460ddc24921096bc35a28c42968b20cbe7a9b19d05`

```dockerfile
```

-	Layers:
	-	`sha256:9fc9db7381e23b41c20dcc2dea87608b0cf0c9091ea543bafb588a1cbb532d21`  
		Last Modified: Mon, 03 Mar 2025 21:16:33 GMT  
		Size: 3.9 MB (3927866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6eb443440c8ecf14e727b7761eed1b229ee61670c0190619f7a21685eb501b`  
		Last Modified: Mon, 03 Mar 2025 21:16:32 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:5703e183e49c0e1dc763e6bdbe2c9bac4d8b652267f0bb85718f9e1c359f1b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358827701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d0faf0f8207be9497615f4b7573829e4fc8b2977f1a06d02e4b28d030c1d41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078929da424ac5687fa6c367c58665828a7d802e10e816e2ae05060d62a114e9`  
		Last Modified: Mon, 03 Mar 2025 21:15:44 GMT  
		Size: 332.0 MB (331962863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:22316782835c59c254cf08a9f94d0fbf9c7d97933beeca3f7be35411f06e5640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40c95061e80226561af8a4a6448bc3128287baf27bd094ecbb1af08b0ca6d00`

```dockerfile
```

-	Layers:
	-	`sha256:db5d3a28f1d73244b43980f7869840e4d6b6a7e6815101a9c53f1f060eb04089`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 3.8 MB (3797205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f1036a2309ba1a573101a8d36570d74e90b4a1095fdd22f30435cae8bfa61e`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:215987920101ed15967e9ab4bab3a20e1b71ab3c0551b5088b380e0d4e1758b1
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
$ docker pull rust@sha256:d3d93642ae6fd2cd84c7912184bb459b7b0db7e8faac0426bd6dca3940a8e761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292709649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f34a203a3c381506722cf3c29ff282ee2a7a6c3ea5f9122a253e5db711f00a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387149dce16056dbdb4b06942bebd598293454f04bcf825305789d3fbd03ccc2`  
		Last Modified: Mon, 03 Mar 2025 21:14:29 GMT  
		Size: 264.5 MB (264490348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2cadfef9494fded06cb45ac7dd21cf8be95bbc29d29843982b1136d37965399b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b31992db534d2f4beea704cd6f87a532756c8285f835090e85c8f923d989e`

```dockerfile
```

-	Layers:
	-	`sha256:12dde0feb1e98f9767c8a92f79c123cbb093c4e7ae6e7eada09ffdbaa4d28854`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 4.0 MB (3955305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc39115291e4d274b7e0282badf83b093f4dbfb6c01e6213fb4ee57cc1166dc9`  
		Last Modified: Mon, 03 Mar 2025 21:14:26 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:9b012a9e771ea654d5d5ca13df9b16d30c582cbd91b239a6fac4d1261df41dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302041787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84120db8ea77fcfa8688c3eff9973638aa867fa532f1e31f8c14ab72b3a64581`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d5d06d813118d1b82098ef607f6a62da0ee850225501b423d07dfd2711d755`  
		Last Modified: Mon, 03 Mar 2025 21:15:00 GMT  
		Size: 278.1 MB (278122053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c9bd5c78945d857d38fe8fa1ac884fe625c77e20599616076ad6721182c2f9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e04d921f393c225935b32033dca57f0e95c593bc7adb10b09f97d690f21a8e4`

```dockerfile
```

-	Layers:
	-	`sha256:6814569f1e5d4ef57f4bea7482e085eb9fb50e1857c3855319e7648690f598ae`  
		Last Modified: Mon, 03 Mar 2025 21:14:54 GMT  
		Size: 3.8 MB (3771368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86dd27a840b3d8ec5e099dd6964b60024cf9d327bb8bc7ecae0b35a82d999080`  
		Last Modified: Mon, 03 Mar 2025 21:14:53 GMT  
		Size: 13.4 KB (13378 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2592404bc1c86ee8445a2102a9a6927ac6f91aaa8821a4ff764884ac7984094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352689188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379c3debf1acbd8228d0dac86005b4fe2aa9dae005b2e1d825e5c1462322dd7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51868c8eb2680ac4209dae1f73861b9c082564efc6f5a6b39e39ac0d7d6ff6b5`  
		Last Modified: Mon, 03 Mar 2025 21:29:50 GMT  
		Size: 324.6 MB (324640763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1e31d6a2695c5af40509bfd2eb1d961a0fb7988b0c1f26bff5d8f6e61c418412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52299a9631b27c74dd842e31aa7e0da8e26a849b4a815ba25015741e88c0ae46`

```dockerfile
```

-	Layers:
	-	`sha256:f273ab084a2e7575d05d06fa8ba8cf7e2d8f8da05b88269989a9ddde03493037`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 4.0 MB (3977648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b19592b0bba92266591738d7b34e3def4520d60096b6a10a024f01b3bedd90e`  
		Last Modified: Mon, 03 Mar 2025 21:29:43 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:88ba2b4761e6d4257c7060aae566853aca592df9e026d748f161b37fb1c2764b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307630505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35b195ee846be85652a54550356ce979af10471acbd66a58ac492de03315688`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a89d68e962de64b429c772557a0e0a429dc425b2a14dcb31802e63de2e4e6bd`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 278.4 MB (278435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b3a7a9e30f6b551540715acbe44f408f539191ad77cc92d3276a74e91dfe0fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed2d74491588bf1f3886ac5c1ba7ef38f7f513a0298f405327e9be21f7af5da`

```dockerfile
```

-	Layers:
	-	`sha256:f2761352b9bb345b81ef703154b559b8e013093b8599a35ed94fdefb3c7327aa`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 3.9 MB (3935220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bacf9a7e03faf1ff9bf9fbd5138346c494c6f27d2ca9c99b3e3b0f5e79c2fe71`  
		Last Modified: Mon, 03 Mar 2025 21:14:32 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d17f48a04c1c202eb18025d892fddf578cedbdc537fa56a041db85189882ab6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355168893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8c917d31b3a645483187dd86afa887442274f948403c6ba0cb7530982f308f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a5a9edf391ebe6e786c0c06eb206b9f00800b0262e795ed3ae7f7a0618588f`  
		Last Modified: Mon, 03 Mar 2025 21:16:50 GMT  
		Size: 323.1 MB (323116579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:77418e4a89328c9c95965a089ff40eb2c4ae1bf5bece9a92578f48b38d198a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce5ae98dec6ba000aab82460ddc24921096bc35a28c42968b20cbe7a9b19d05`

```dockerfile
```

-	Layers:
	-	`sha256:9fc9db7381e23b41c20dcc2dea87608b0cf0c9091ea543bafb588a1cbb532d21`  
		Last Modified: Mon, 03 Mar 2025 21:16:33 GMT  
		Size: 3.9 MB (3927866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6eb443440c8ecf14e727b7761eed1b229ee61670c0190619f7a21685eb501b`  
		Last Modified: Mon, 03 Mar 2025 21:16:32 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:5703e183e49c0e1dc763e6bdbe2c9bac4d8b652267f0bb85718f9e1c359f1b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358827701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d0faf0f8207be9497615f4b7573829e4fc8b2977f1a06d02e4b28d030c1d41`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='570e9a36a9c981a67b7e44f28776f7ece60141e2b63ba279ff0989c6053f3c67' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='f48e2d5a41a057b758e4cb9daf60e9adfcfc555e83eff2d62caa2dc51f9bc6da' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078929da424ac5687fa6c367c58665828a7d802e10e816e2ae05060d62a114e9`  
		Last Modified: Mon, 03 Mar 2025 21:15:44 GMT  
		Size: 332.0 MB (331962863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:22316782835c59c254cf08a9f94d0fbf9c7d97933beeca3f7be35411f06e5640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40c95061e80226561af8a4a6448bc3128287baf27bd094ecbb1af08b0ca6d00`

```dockerfile
```

-	Layers:
	-	`sha256:db5d3a28f1d73244b43980f7869840e4d6b6a7e6815101a9c53f1f060eb04089`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 3.8 MB (3797205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f1036a2309ba1a573101a8d36570d74e90b4a1095fdd22f30435cae8bfa61e`  
		Last Modified: Mon, 03 Mar 2025 21:15:38 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:e94e2d2e0a9df48fdfcacb47d8b60d036abe60b7c6fa3ac3de1dd16a3d18f19a
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
$ docker pull rust@sha256:dccdc77b5b046c078e76f4ca452308e213f4b7ba3e8a6c215393381d36d5b280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283883304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35d2ada2c353b98b46aff96c86cc0c21d362da854c48fcd0aa754b13b83eb20`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e0052749e7f2c9ab3a91aad47ad13df4c7c8911c162e2bdb7d08f691e99aac`  
		Last Modified: Mon, 03 Mar 2025 21:14:25 GMT  
		Size: 253.6 MB (253629374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:19d324bd0c298ad1b3f5e6df1ce1df18225864b216efbb6c90ddce0a8ce24642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c80060630492f3b3f74f9d388000b5067bc23694bacc999541e6da57bf59ff`

```dockerfile
```

-	Layers:
	-	`sha256:df56ae19c38d79a9c6b3901f1921d9c3833a93218a082679bdb0a12883f3905e`  
		Last Modified: Mon, 03 Mar 2025 21:14:22 GMT  
		Size: 4.2 MB (4173204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9fc1edc1c95e2a303e127182409fafb9fc9e2d3f3ad0da80b896cad7720daaa`  
		Last Modified: Mon, 03 Mar 2025 21:14:21 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:1c291529dbe66cd22592a3d8ecc5cead222cb64a3d43b8aaadfa065746e28570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297882666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e350660ab01bd40fd4abffb3fd8ba3d377659d12c689daca3b6779053172617`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0ca501b624d9dae81049df15e1024733ee21141b25f8ca123d98e0d13df5d12`  
		Last Modified: Tue, 25 Feb 2025 01:31:18 GMT  
		Size: 25.5 MB (25535432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6d72cafe6043b15f5dabf082f52f18a84a9ac04dfbfe5fc6bba3fcbe37edd0`  
		Last Modified: Mon, 03 Mar 2025 21:20:57 GMT  
		Size: 272.3 MB (272347234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:07cd7090e5192facfdd11a8b0ed54d90c6c4f804c8c9a9059c3d3e7ba657c970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612130ff6bdfd39ede8255ddb232e9327ffb825112e6bb1017c80060be9e9c7d`

```dockerfile
```

-	Layers:
	-	`sha256:73bc2806f7ecf2f20576c7878e9d5e9b7dfc3b25b6132689e08490bce610f038`  
		Last Modified: Mon, 03 Mar 2025 21:20:39 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f927f926449a4f38eeebab517940bd75ca9acef94ae1a163391730411486b20`  
		Last Modified: Mon, 03 Mar 2025 21:20:38 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:de9c5b13bcc43221f1603fb03089d27e59603e8087525be9302e30fa4a75e3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343069561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e422222ab9bba42554ec25e8f7656f35c48de3d1930f29223b4c40648547e500`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ae7537677409c7e96b2e534829fe706743a9e1c1fc79c0e6c3a6ae631021d1`  
		Last Modified: Mon, 03 Mar 2025 21:34:48 GMT  
		Size: 314.3 MB (314323574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:cb9b665a79ff9d7407b5196e20d85e27ec9c2216b78c66b5a1dfa4a438542750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b594182c132405732dc65dec31b847e10c0314703f603d9728caf021dd2f8c3`

```dockerfile
```

-	Layers:
	-	`sha256:f87a9a1c38fe1dae028e9162ed79be83deebf92138b807780b636247a977d593`  
		Last Modified: Mon, 03 Mar 2025 21:34:40 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0c9191b26a4828e5bd697af4e870ad8de930043587eddf2407e36a5f19df4ea`  
		Last Modified: Mon, 03 Mar 2025 21:34:40 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:8ce46ac85186e75d85f9912eaea882d8fab038755ad48d921a2974b006f800a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302583357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66df80913375cbd40ebb9b025095b1856d1454a6206427f78c4846d5b5771158`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Mon, 03 Mar 2025 15:10:05 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 03 Mar 2025 15:10:05 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Mon, 03 Mar 2025 15:10:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='c8d03f559a2335693379e1d3eaee76622b2a6580807e63bcd61faea709b9f664' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='fe8bc715bb116b86cb8c126bd4ad96efe9cb6f965c19a64e2aa8bd844c9e9ed5' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='46ccc85ca7f6c5ed28141cdc0a107c51a8ae71272899213a1f44820c7f6440b5' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='27ee6b6e0ca43a37ee4fcbe1ab2d5ad4fbf224bbfbbfda085345c2bfb63ab785' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc6ac53dd3c2cb0c6fd992e5925fc15a335691c21c9dc26765ed22ae0d20371`  
		Last Modified: Mon, 03 Mar 2025 21:14:39 GMT  
		Size: 271.4 MB (271402930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e925605333c9a3842c68db47ba3d21c3ba0539ccbf18a0231b3a8cfacca912b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55c2e9da4484fa31efbf5cc3c8d14b787bc24da1ef1871ff26f4e0ac811f26d`

```dockerfile
```

-	Layers:
	-	`sha256:d0d87fc423e5c2445348c3696ac9ef20a4fae6bfa1ceebb2a4a2a6b7af161b60`  
		Last Modified: Mon, 03 Mar 2025 21:14:33 GMT  
		Size: 4.2 MB (4163461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714de8d934c25f3276ae4b994be3302532085a4c69860853de35ef86540dd876`  
		Last Modified: Mon, 03 Mar 2025 21:14:33 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json
