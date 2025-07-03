<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rust`

-	[`rust:1`](#rust1)
-	[`rust:1-alpine`](#rust1-alpine)
-	[`rust:1-alpine3.20`](#rust1-alpine320)
-	[`rust:1-alpine3.21`](#rust1-alpine321)
-	[`rust:1-alpine3.22`](#rust1-alpine322)
-	[`rust:1-bookworm`](#rust1-bookworm)
-	[`rust:1-bullseye`](#rust1-bullseye)
-	[`rust:1-slim`](#rust1-slim)
-	[`rust:1-slim-bookworm`](#rust1-slim-bookworm)
-	[`rust:1-slim-bullseye`](#rust1-slim-bullseye)
-	[`rust:1-slim-trixie`](#rust1-slim-trixie)
-	[`rust:1-trixie`](#rust1-trixie)
-	[`rust:1.88`](#rust188)
-	[`rust:1.88-alpine`](#rust188-alpine)
-	[`rust:1.88-alpine3.20`](#rust188-alpine320)
-	[`rust:1.88-alpine3.21`](#rust188-alpine321)
-	[`rust:1.88-alpine3.22`](#rust188-alpine322)
-	[`rust:1.88-bookworm`](#rust188-bookworm)
-	[`rust:1.88-bullseye`](#rust188-bullseye)
-	[`rust:1.88-slim`](#rust188-slim)
-	[`rust:1.88-slim-bookworm`](#rust188-slim-bookworm)
-	[`rust:1.88-slim-bullseye`](#rust188-slim-bullseye)
-	[`rust:1.88-slim-trixie`](#rust188-slim-trixie)
-	[`rust:1.88-trixie`](#rust188-trixie)
-	[`rust:1.88.0`](#rust1880)
-	[`rust:1.88.0-alpine`](#rust1880-alpine)
-	[`rust:1.88.0-alpine3.20`](#rust1880-alpine320)
-	[`rust:1.88.0-alpine3.21`](#rust1880-alpine321)
-	[`rust:1.88.0-alpine3.22`](#rust1880-alpine322)
-	[`rust:1.88.0-bookworm`](#rust1880-bookworm)
-	[`rust:1.88.0-bullseye`](#rust1880-bullseye)
-	[`rust:1.88.0-slim`](#rust1880-slim)
-	[`rust:1.88.0-slim-bookworm`](#rust1880-slim-bookworm)
-	[`rust:1.88.0-slim-bullseye`](#rust1880-slim-bullseye)
-	[`rust:1.88.0-slim-trixie`](#rust1880-slim-trixie)
-	[`rust:1.88.0-trixie`](#rust1880-trixie)
-	[`rust:alpine`](#rustalpine)
-	[`rust:alpine3.20`](#rustalpine320)
-	[`rust:alpine3.21`](#rustalpine321)
-	[`rust:alpine3.22`](#rustalpine322)
-	[`rust:bookworm`](#rustbookworm)
-	[`rust:bullseye`](#rustbullseye)
-	[`rust:latest`](#rustlatest)
-	[`rust:slim`](#rustslim)
-	[`rust:slim-bookworm`](#rustslim-bookworm)
-	[`rust:slim-bullseye`](#rustslim-bullseye)
-	[`rust:slim-trixie`](#rustslim-trixie)
-	[`rust:trixie`](#rusttrixie)

## `rust:1`

```console
$ docker pull rust@sha256:5771a3cc2081935c59ac52b92d49c9e164d4fed92c9f6420aa8cc50364aead6e
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
$ docker pull rust@sha256:95f6d6956bf8abd7461763ba7ccd243d8964a41c8eb3f41d895490c782628d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553347880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a479811b82446e6bf598238bb2fcd3ae41b351a1a7c87e53d8f2333a7bbe001d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe9c1abe6f3b8ca9fc6abe710405f830f95262f1d356e8f6545d823b5840a5c`  
		Last Modified: Tue, 01 Jul 2025 05:12:07 GMT  
		Size: 211.4 MB (211373500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0545d5f3de1a8249849f4342031613d732af87e31f13755f5fac287119ed13e8`  
		Last Modified: Tue, 01 Jul 2025 06:18:35 GMT  
		Size: 205.1 MB (205059525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:0e0dc34caec6b81f1b5ab4c9a559c11b4d7440382c69d8a2cdbe5002a71523e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15877001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81308c8e2c35f38fbef285c685f2ca642508d83efc22df71984838afd98ac55d`

```dockerfile
```

-	Layers:
	-	`sha256:3260e53bff48cf37775cac874c3e2920680f90a7669e12d2c322771f16c50614`  
		Last Modified: Tue, 01 Jul 2025 08:44:24 GMT  
		Size: 15.9 MB (15863862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a629d4f8f234144e7bda08172e21d63709f916bfe46836348a616c43d2cdd880`  
		Last Modified: Tue, 01 Jul 2025 08:44:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:b12fb2b0506d2b8fde83230531af65c46d2e1cb65c7b965a23de3015d7feff05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546880259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe31256245950fcf402e7f41d298a8bd3859cf9558a2e1ff584d64071362bda1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc606b1195a348c6a47399c1a54ab936d4477a526d62306ddce89fe76a2d22`  
		Last Modified: Tue, 01 Jul 2025 08:59:56 GMT  
		Size: 21.9 MB (21928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f4c85f426e2c955b1dac4fa88bc182d725644c23ad01bdcbf64d9664e34a8`  
		Last Modified: Tue, 01 Jul 2025 18:28:59 GMT  
		Size: 59.7 MB (59656492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda2264dd6dda88971c220cda9283a6c337d04aeb92012d9d160887d4ec0b556`  
		Last Modified: Wed, 02 Jul 2025 00:17:51 GMT  
		Size: 175.3 MB (175294922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5ff6581ced6c9c0cc98e703fa5901cda1814bee9d3ac91337dfcb2eeaa3fa`  
		Last Modified: Wed, 02 Jul 2025 12:16:49 GMT  
		Size: 245.8 MB (245792330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:a6b6613abe69a8ea05c159027354fad9e25a0f58f5a61a4c761bd608e9118f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15679627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0222859d21f0de033a308a561262ae0c61dc1ab6441395c68809f9d9455913d`

```dockerfile
```

-	Layers:
	-	`sha256:d6bf21d47ea4882f2e19fc8c2018d3473ff3633b948a8a2912ffa2fb5dc5c75c`  
		Last Modified: Wed, 02 Jul 2025 11:44:31 GMT  
		Size: 15.7 MB (15666380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f88163f4b88d616cf50cd1d0bb3bb47eda6485492c98f7f4bc8035c0d832d762`  
		Last Modified: Wed, 02 Jul 2025 11:44:32 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:66b553fe51fe4eba929ee31c39d66506fe41b72cf403dab3117de2bd5d43e645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513346599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5424600217354e80a3f0ab99133ec64aa48f464a2f1c29a93cbd0f95758e5af7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a65abb6272f500a9ae5d14c9ae8ef9cb0e4009b02acfccb4dabc478f252d44`  
		Last Modified: Tue, 01 Jul 2025 19:38:43 GMT  
		Size: 202.8 MB (202827049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b360d25d0e207b0afc74cd93a7662c88e8399a9798db1e3baa5665c7aa6c157`  
		Last Modified: Wed, 02 Jul 2025 03:35:58 GMT  
		Size: 174.3 MB (174259463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:2f4addd958f6c23177ba57cb0b62703dba22d22d022fa5ff6111f60b883e3dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15905729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3c6db7f65484d03b4cc60245a2ead7632bf36cf44fdf76c3720b3831df124c`

```dockerfile
```

-	Layers:
	-	`sha256:ac641e00624bd7b454d162d456dcbebc72d34940b2f4aa530da90b3cbe71d493`  
		Last Modified: Wed, 02 Jul 2025 05:44:37 GMT  
		Size: 15.9 MB (15892438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1fa12a678c68a338b4e49d70c17dbded6143e0d3861664cbccf02c362f6879`  
		Last Modified: Wed, 02 Jul 2025 05:44:38 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:628fa076d84051d529c70e5978ae2488cc27c057e4378e6d6b4427cd1f48f5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (580031340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b007959168ba93c975145eae21e48f1112c685910223873e0805f91c16efcf81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99742b01aaf231df6992d8ecab593f6a7668b9047c6bb8cae0cc211c42b656d6`  
		Last Modified: Tue, 01 Jul 2025 05:11:03 GMT  
		Size: 210.3 MB (210310619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a36703fa30e50f1e2d2d9b8d6ee38f74b5c49158c0331edd0ac22489b68c9d`  
		Last Modified: Tue, 01 Jul 2025 08:59:26 GMT  
		Size: 229.2 MB (229161050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:60118c6a0bd04b58edbef1c693c60eef0a5c39a11250ffab32588f40429c495a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15853847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a0f3771a2d9e6d62cb0c6bcec0264fbabb8e5129657775262a756a4ab9cc9`

```dockerfile
```

-	Layers:
	-	`sha256:aede24ae4b2038e2305b863ac4a0808c493737d5ec9bc1219a2ffcdf76249352`  
		Last Modified: Tue, 01 Jul 2025 08:44:58 GMT  
		Size: 15.8 MB (15840760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adee46bd81fb5e17001fc933d0596dd15dc9c7296c5efe1c744ecb38885cff77`  
		Last Modified: Tue, 01 Jul 2025 08:44:59 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:f4c7cad30a4575e18ae53f14b5bccb71451b44d720253a8f73f1cb12780bbf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635985035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442858853b317d76b745617081af4451d23840bd47301b0eabc620759c4b714`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7082fff0db11ec79e9a3c8fc9c05691e086d30ca51023010805fccbeac2b8dad`  
		Last Modified: Tue, 01 Jul 2025 05:07:55 GMT  
		Size: 25.7 MB (25663667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6cd79d875ce6ba17d2080d5bd4d0d55f7eec0f6bb923ae0b53e5bec14ef9b`  
		Last Modified: Tue, 01 Jul 2025 10:09:38 GMT  
		Size: 69.8 MB (69840014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575c9bdfba8d02bb3354a6a72904306bd1ae2c4432d14255385a153c75887837`  
		Last Modified: Tue, 01 Jul 2025 16:27:30 GMT  
		Size: 214.4 MB (214424908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078767722b4e04b7787f0ea5f95284ec4da0e1c5dc7804af4c26dc5181ec096c`  
		Last Modified: Wed, 02 Jul 2025 00:02:53 GMT  
		Size: 273.7 MB (273719203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:1a33a8b84d73eb3cf5fe4d5eb91a7212e3e015e40670b51ddebf3b52c4dbe0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee34f793447401153bab355f4bfbba25c4161b769172568c3b013931ffcfc953`

```dockerfile
```

-	Layers:
	-	`sha256:a169d322c59d3a0ddff0bf27d48dbe267dff9b48aaddd2ed30804cb885ff2527`  
		Last Modified: Tue, 01 Jul 2025 23:44:57 GMT  
		Size: 15.8 MB (15839092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d4887067e8590d2b12056401643ede686e2b3a83a2fccdfca0b762a5961e6a7`  
		Last Modified: Tue, 01 Jul 2025 23:44:58 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:79ee189d40fd6c859e15a1e9c69b6da58d451b096e16a52dfec29b9bd0d76a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.5 MB (601452429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924b21bb8e92662795debcd307e3f3204964743780a9f028dfb3700b0ae8640b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1e32b479a11528098c70ba4af6292099abafcb29e0823d2861c86032c9b0b`  
		Last Modified: Tue, 01 Jul 2025 13:41:28 GMT  
		Size: 63.5 MB (63497964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2254c2dc3c53615f5f6a5adcfafb558670473622cb504cb0a6d02fd2b89d2667`  
		Last Modified: Tue, 01 Jul 2025 14:10:41 GMT  
		Size: 183.4 MB (183421934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c312814d252c566d3c3ee8f98763bedd5510a970a7460965bac0ea117ac8071c`  
		Last Modified: Tue, 01 Jul 2025 21:03:03 GMT  
		Size: 283.4 MB (283362703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:a4f9cf4a09562544ef011200268fb453c235bc5b972df93f32ca2dbf4ac1e349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15684597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afc1cf86bd3504dbe315e3c93562fc2ff8e92d15305627e7b38023518ec873b`

```dockerfile
```

-	Layers:
	-	`sha256:39dbb3c0f9a78d73aea412786fb8fabb2d333d5f18f4608bab4734aaa8e60fd7`  
		Last Modified: Tue, 01 Jul 2025 20:45:07 GMT  
		Size: 15.7 MB (15671458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d32a8a23e2b1c8cb3fdec2c521041d1a7fc5c908e5a6ce6bd3048f58dfefe8`  
		Last Modified: Tue, 01 Jul 2025 20:45:08 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:ec0413a092f4cc01b32e08f991485abe4467ef95c7416a6643a063a141c2e0ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:b18203be0f58e16fe47250bf98bbe83c61bbfa97a0f5a94cebf34605bb000137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324842014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccfa6e07df925301f1f0b76b6784e617369e209ccfd7b16e76a3f50bca1e544`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c179a1cc9cc1626cd02fbb4866ee1705894a35d0acf8458e7f0274620ded46`  
		Last Modified: Thu, 26 Jun 2025 19:02:56 GMT  
		Size: 61.6 MB (61613765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b44eb86436bd74e3289f02e42ae2c9df9c6a39ac3ff054f893f7cbaddbcf08b`  
		Last Modified: Thu, 26 Jun 2025 20:45:29 GMT  
		Size: 259.4 MB (259431403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:3a48955a20cd88465d43306589af8be8e9aab9bc4983ebf983267397b0038f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8794bb5882365fcd697f232d90c928f4dfc42f2d9dee1f418d14cba22fc740`

```dockerfile
```

-	Layers:
	-	`sha256:4af3880faef85aba29ec3559478d1219bcd27ba3aa3e498970fa8eb110c9fbbe`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d7d4050c4275c54863ef9a56b9e59d3e338bc902f05df72abcbf103b3bf06c`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:43c5afb577aa21180b984fe215c836db0e8da8c6d6e29f4f5d60fcac8f6747e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324286625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037fc7bdc081378f949b34f5b57abb98ba2f2308d8e24c81eec1dc00f8095344`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe32611e1706eb5e71110ea02f0a43bcf8d9d5b31375d8372476ca0151ea4e79`  
		Last Modified: Thu, 26 Jun 2025 19:09:40 GMT  
		Size: 59.2 MB (59154287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd9ba9c44d35a05a92f10caaf51df4bf98f7cd9e90070d71790f3fa3de848fa`  
		Last Modified: Thu, 26 Jun 2025 20:48:42 GMT  
		Size: 261.0 MB (260996397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:f7f6eaadbe7a000ba5420c2ea8c78d7812aea2e2ba405d6f47c7dcc77af1c77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fcba7c7ba45a16b412de43acab6b32790c948a2de7b038009b4fe3f5344978`

```dockerfile
```

-	Layers:
	-	`sha256:0ece12c371cca20fa75cd9470ad9eb8f90b1172dae46baaf4940565722fcf88e`  
		Last Modified: Thu, 26 Jun 2025 20:44:43 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49231f16442a61f2a0b6140092b2b40d1a3786b17de63fc044fabaa5fbcee312`  
		Last Modified: Thu, 26 Jun 2025 20:44:44 GMT  
		Size: 12.1 KB (12084 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:3ab9b805c8d2444f6f63f1ae7a38b5e04949d6b0d9e8a314e1ee3ad502deae45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:985c5bffc08709b4c04506340fcdc2542dfd0604070a993c409a6565e200c488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318374251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4468520ebd63f0d5993bf50e71ce97ce1770aee2cf170f4b68416cbd826434`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd8e343fc1e8b59389632b1aa1fec9897eb0d70d9a028c4953824eaca48506`  
		Last Modified: Thu, 26 Jun 2025 19:02:57 GMT  
		Size: 55.3 MB (55315554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af473c39e92f0a526585dfa175d2324b3bcc5653f1f8b4a0197290536a1a4b82`  
		Last Modified: Thu, 26 Jun 2025 22:03:51 GMT  
		Size: 259.4 MB (259431800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:6d1398d665e6f2fad6e604e6b35246a23905cff0473753ad60eee908c8602f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.5 KB (722503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ed6595279fc3b8ec29033696b6a0ff4d9c437f59ceeaf9052d8a7b745cac53`

```dockerfile
```

-	Layers:
	-	`sha256:172a379c01373f9fa6f1f7546d8f14ca43f16dbed174f0fb1038d9ad729985b4`  
		Last Modified: Thu, 26 Jun 2025 20:44:46 GMT  
		Size: 711.8 KB (711789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c520dac29e5f70b8c11a8c70a95fc0a3a9bb4ca3b5499c004ab4cf05e37e7ce2`  
		Last Modified: Thu, 26 Jun 2025 20:44:46 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bbc890fbb4cfe63267e61b157106ae17e22fea8965bd86dad3ba2895731fd832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.0 MB (318036721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2562e20c93fbfe25e95e223728ea45fdabb24f56872078249b32a94618aef470`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f73dbcfd8a123487699fe68590b2bd9f99926de28d20db07b032c7c04a77d5b`  
		Last Modified: Thu, 26 Jun 2025 19:07:09 GMT  
		Size: 53.0 MB (52950135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35f71611cb454ac5691276f7fb4f820ad5cca79bd33a16a47b3383d0199fd5d`  
		Last Modified: Thu, 26 Jun 2025 22:04:01 GMT  
		Size: 261.0 MB (260995421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:ffe59248eec0f167209f1689d76dc0cf65197edb7123968bab9d9736ed5dbe1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bf25ee4d7342c1573d066bf9d6490bc899c772b46d58fb99616651dff2a12a`

```dockerfile
```

-	Layers:
	-	`sha256:fb91044d3c55c5b9a10f560693a397817a79b1c3e9cac98794b2cc2378ddf88f`  
		Last Modified: Thu, 26 Jun 2025 20:44:50 GMT  
		Size: 747.7 KB (747721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619847fa4854614400d1faefbfd3dca469c0ddb922f14d8b21e0cfee7113e7b2`  
		Last Modified: Thu, 26 Jun 2025 20:44:51 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.21`

```console
$ docker pull rust@sha256:9c6a4baf58661f99a5441b15e3ad8295dabf35e849c4935e77ad35d9809be1d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:f76a41f6a9d96aca247c6789369bb5986c9faaef5d0ab080ae28346725d86c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324637733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd470e8018c4c8d13c36bb6d82b21b2b35e0cab903eaabfd2ba2cdbc0d49d8c9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a9008c78a14e56fc9106b9415625622b22d3e7d7ed88d4c9f168084a5b930a`  
		Last Modified: Thu, 26 Jun 2025 19:02:57 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99aa10cef404820ac909a9c36a9398af421599896d89f5216fe03a0484938cbc`  
		Last Modified: Thu, 26 Jun 2025 20:47:21 GMT  
		Size: 259.4 MB (259430674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:bfe3ce46af8506744eb91a950436d78f9b57aa1c89dab3f0c8cf5796a6964767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063fdf51672810ea7124832520f622f7d4a1bd29ff180e4e39b155177f6ce538`

```dockerfile
```

-	Layers:
	-	`sha256:bd239d1a7ba898b4e5db9276ef7089d6bd3dc5fbc114c96a656434c2b620e7a4`  
		Last Modified: Thu, 26 Jun 2025 20:44:52 GMT  
		Size: 782.6 KB (782619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68bd06a7d86815924cf9c1da819c34ded738a4b417cf24f9b33b853d7a3d1bb2`  
		Last Modified: Thu, 26 Jun 2025 20:44:53 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:390d7bebae8a355bd9e439bffd1f0f0124d0ade0a01602308b3c663490f66a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.1 MB (324089393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c931f5d71d48f4c73a17c302da0df6ebc23b15ced06b4f4ab775f1ec6e5228`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa43a6919f3e4298c4ac7012f740c568baceb922776f8df0f76856cc3ee4662`  
		Last Modified: Thu, 26 Jun 2025 19:08:40 GMT  
		Size: 59.1 MB (59101301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aad9f05f3e21035ae8f9c44b60e6bd73096afc6f6fa0e572587f6b65e6ece8`  
		Last Modified: Thu, 26 Jun 2025 20:47:22 GMT  
		Size: 261.0 MB (260995063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:03bf0509d1cc316b17044231bd28292d0828891ee21cde73471813fed5ee7435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (872990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eaca6f25dcca1d3f5272d1eef631f701b29c34b87f57293ddd1769d867a156`

```dockerfile
```

-	Layers:
	-	`sha256:263657c33753a7119953e3eaf32bfa7eb0f92250b29093be5e85cee6402a4952`  
		Last Modified: Thu, 26 Jun 2025 20:44:57 GMT  
		Size: 862.2 KB (862157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7daa109bbb3d9da7db18c495a2c43ac74998f6a27162c51bbc993b97bf68fa0`  
		Last Modified: Thu, 26 Jun 2025 20:44:57 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.22`

```console
$ docker pull rust@sha256:ec0413a092f4cc01b32e08f991485abe4467ef95c7416a6643a063a141c2e0ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.22` - linux; amd64

```console
$ docker pull rust@sha256:b18203be0f58e16fe47250bf98bbe83c61bbfa97a0f5a94cebf34605bb000137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324842014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccfa6e07df925301f1f0b76b6784e617369e209ccfd7b16e76a3f50bca1e544`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c179a1cc9cc1626cd02fbb4866ee1705894a35d0acf8458e7f0274620ded46`  
		Last Modified: Thu, 26 Jun 2025 19:02:56 GMT  
		Size: 61.6 MB (61613765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b44eb86436bd74e3289f02e42ae2c9df9c6a39ac3ff054f893f7cbaddbcf08b`  
		Last Modified: Thu, 26 Jun 2025 20:45:29 GMT  
		Size: 259.4 MB (259431403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:3a48955a20cd88465d43306589af8be8e9aab9bc4983ebf983267397b0038f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8794bb5882365fcd697f232d90c928f4dfc42f2d9dee1f418d14cba22fc740`

```dockerfile
```

-	Layers:
	-	`sha256:4af3880faef85aba29ec3559478d1219bcd27ba3aa3e498970fa8eb110c9fbbe`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d7d4050c4275c54863ef9a56b9e59d3e338bc902f05df72abcbf103b3bf06c`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:43c5afb577aa21180b984fe215c836db0e8da8c6d6e29f4f5d60fcac8f6747e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324286625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037fc7bdc081378f949b34f5b57abb98ba2f2308d8e24c81eec1dc00f8095344`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe32611e1706eb5e71110ea02f0a43bcf8d9d5b31375d8372476ca0151ea4e79`  
		Last Modified: Thu, 26 Jun 2025 19:09:40 GMT  
		Size: 59.2 MB (59154287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd9ba9c44d35a05a92f10caaf51df4bf98f7cd9e90070d71790f3fa3de848fa`  
		Last Modified: Thu, 26 Jun 2025 20:48:42 GMT  
		Size: 261.0 MB (260996397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:f7f6eaadbe7a000ba5420c2ea8c78d7812aea2e2ba405d6f47c7dcc77af1c77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fcba7c7ba45a16b412de43acab6b32790c948a2de7b038009b4fe3f5344978`

```dockerfile
```

-	Layers:
	-	`sha256:0ece12c371cca20fa75cd9470ad9eb8f90b1172dae46baaf4940565722fcf88e`  
		Last Modified: Thu, 26 Jun 2025 20:44:43 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49231f16442a61f2a0b6140092b2b40d1a3786b17de63fc044fabaa5fbcee312`  
		Last Modified: Thu, 26 Jun 2025 20:44:44 GMT  
		Size: 12.1 KB (12084 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:5771a3cc2081935c59ac52b92d49c9e164d4fed92c9f6420aa8cc50364aead6e
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
$ docker pull rust@sha256:95f6d6956bf8abd7461763ba7ccd243d8964a41c8eb3f41d895490c782628d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553347880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a479811b82446e6bf598238bb2fcd3ae41b351a1a7c87e53d8f2333a7bbe001d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe9c1abe6f3b8ca9fc6abe710405f830f95262f1d356e8f6545d823b5840a5c`  
		Last Modified: Tue, 01 Jul 2025 05:12:07 GMT  
		Size: 211.4 MB (211373500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0545d5f3de1a8249849f4342031613d732af87e31f13755f5fac287119ed13e8`  
		Last Modified: Tue, 01 Jul 2025 06:18:35 GMT  
		Size: 205.1 MB (205059525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0e0dc34caec6b81f1b5ab4c9a559c11b4d7440382c69d8a2cdbe5002a71523e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15877001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81308c8e2c35f38fbef285c685f2ca642508d83efc22df71984838afd98ac55d`

```dockerfile
```

-	Layers:
	-	`sha256:3260e53bff48cf37775cac874c3e2920680f90a7669e12d2c322771f16c50614`  
		Last Modified: Tue, 01 Jul 2025 08:44:24 GMT  
		Size: 15.9 MB (15863862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a629d4f8f234144e7bda08172e21d63709f916bfe46836348a616c43d2cdd880`  
		Last Modified: Tue, 01 Jul 2025 08:44:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:b12fb2b0506d2b8fde83230531af65c46d2e1cb65c7b965a23de3015d7feff05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546880259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe31256245950fcf402e7f41d298a8bd3859cf9558a2e1ff584d64071362bda1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc606b1195a348c6a47399c1a54ab936d4477a526d62306ddce89fe76a2d22`  
		Last Modified: Tue, 01 Jul 2025 08:59:56 GMT  
		Size: 21.9 MB (21928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f4c85f426e2c955b1dac4fa88bc182d725644c23ad01bdcbf64d9664e34a8`  
		Last Modified: Tue, 01 Jul 2025 18:28:59 GMT  
		Size: 59.7 MB (59656492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda2264dd6dda88971c220cda9283a6c337d04aeb92012d9d160887d4ec0b556`  
		Last Modified: Wed, 02 Jul 2025 00:17:51 GMT  
		Size: 175.3 MB (175294922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5ff6581ced6c9c0cc98e703fa5901cda1814bee9d3ac91337dfcb2eeaa3fa`  
		Last Modified: Wed, 02 Jul 2025 12:16:49 GMT  
		Size: 245.8 MB (245792330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a6b6613abe69a8ea05c159027354fad9e25a0f58f5a61a4c761bd608e9118f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15679627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0222859d21f0de033a308a561262ae0c61dc1ab6441395c68809f9d9455913d`

```dockerfile
```

-	Layers:
	-	`sha256:d6bf21d47ea4882f2e19fc8c2018d3473ff3633b948a8a2912ffa2fb5dc5c75c`  
		Last Modified: Wed, 02 Jul 2025 11:44:31 GMT  
		Size: 15.7 MB (15666380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f88163f4b88d616cf50cd1d0bb3bb47eda6485492c98f7f4bc8035c0d832d762`  
		Last Modified: Wed, 02 Jul 2025 11:44:32 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:66b553fe51fe4eba929ee31c39d66506fe41b72cf403dab3117de2bd5d43e645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513346599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5424600217354e80a3f0ab99133ec64aa48f464a2f1c29a93cbd0f95758e5af7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a65abb6272f500a9ae5d14c9ae8ef9cb0e4009b02acfccb4dabc478f252d44`  
		Last Modified: Tue, 01 Jul 2025 19:38:43 GMT  
		Size: 202.8 MB (202827049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b360d25d0e207b0afc74cd93a7662c88e8399a9798db1e3baa5665c7aa6c157`  
		Last Modified: Wed, 02 Jul 2025 03:35:58 GMT  
		Size: 174.3 MB (174259463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2f4addd958f6c23177ba57cb0b62703dba22d22d022fa5ff6111f60b883e3dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15905729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3c6db7f65484d03b4cc60245a2ead7632bf36cf44fdf76c3720b3831df124c`

```dockerfile
```

-	Layers:
	-	`sha256:ac641e00624bd7b454d162d456dcbebc72d34940b2f4aa530da90b3cbe71d493`  
		Last Modified: Wed, 02 Jul 2025 05:44:37 GMT  
		Size: 15.9 MB (15892438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1fa12a678c68a338b4e49d70c17dbded6143e0d3861664cbccf02c362f6879`  
		Last Modified: Wed, 02 Jul 2025 05:44:38 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:628fa076d84051d529c70e5978ae2488cc27c057e4378e6d6b4427cd1f48f5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (580031340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b007959168ba93c975145eae21e48f1112c685910223873e0805f91c16efcf81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99742b01aaf231df6992d8ecab593f6a7668b9047c6bb8cae0cc211c42b656d6`  
		Last Modified: Tue, 01 Jul 2025 05:11:03 GMT  
		Size: 210.3 MB (210310619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a36703fa30e50f1e2d2d9b8d6ee38f74b5c49158c0331edd0ac22489b68c9d`  
		Last Modified: Tue, 01 Jul 2025 08:59:26 GMT  
		Size: 229.2 MB (229161050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:60118c6a0bd04b58edbef1c693c60eef0a5c39a11250ffab32588f40429c495a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15853847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a0f3771a2d9e6d62cb0c6bcec0264fbabb8e5129657775262a756a4ab9cc9`

```dockerfile
```

-	Layers:
	-	`sha256:aede24ae4b2038e2305b863ac4a0808c493737d5ec9bc1219a2ffcdf76249352`  
		Last Modified: Tue, 01 Jul 2025 08:44:58 GMT  
		Size: 15.8 MB (15840760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adee46bd81fb5e17001fc933d0596dd15dc9c7296c5efe1c744ecb38885cff77`  
		Last Modified: Tue, 01 Jul 2025 08:44:59 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:f4c7cad30a4575e18ae53f14b5bccb71451b44d720253a8f73f1cb12780bbf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635985035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442858853b317d76b745617081af4451d23840bd47301b0eabc620759c4b714`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7082fff0db11ec79e9a3c8fc9c05691e086d30ca51023010805fccbeac2b8dad`  
		Last Modified: Tue, 01 Jul 2025 05:07:55 GMT  
		Size: 25.7 MB (25663667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6cd79d875ce6ba17d2080d5bd4d0d55f7eec0f6bb923ae0b53e5bec14ef9b`  
		Last Modified: Tue, 01 Jul 2025 10:09:38 GMT  
		Size: 69.8 MB (69840014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575c9bdfba8d02bb3354a6a72904306bd1ae2c4432d14255385a153c75887837`  
		Last Modified: Tue, 01 Jul 2025 16:27:30 GMT  
		Size: 214.4 MB (214424908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078767722b4e04b7787f0ea5f95284ec4da0e1c5dc7804af4c26dc5181ec096c`  
		Last Modified: Wed, 02 Jul 2025 00:02:53 GMT  
		Size: 273.7 MB (273719203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1a33a8b84d73eb3cf5fe4d5eb91a7212e3e015e40670b51ddebf3b52c4dbe0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee34f793447401153bab355f4bfbba25c4161b769172568c3b013931ffcfc953`

```dockerfile
```

-	Layers:
	-	`sha256:a169d322c59d3a0ddff0bf27d48dbe267dff9b48aaddd2ed30804cb885ff2527`  
		Last Modified: Tue, 01 Jul 2025 23:44:57 GMT  
		Size: 15.8 MB (15839092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d4887067e8590d2b12056401643ede686e2b3a83a2fccdfca0b762a5961e6a7`  
		Last Modified: Tue, 01 Jul 2025 23:44:58 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:79ee189d40fd6c859e15a1e9c69b6da58d451b096e16a52dfec29b9bd0d76a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.5 MB (601452429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924b21bb8e92662795debcd307e3f3204964743780a9f028dfb3700b0ae8640b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1e32b479a11528098c70ba4af6292099abafcb29e0823d2861c86032c9b0b`  
		Last Modified: Tue, 01 Jul 2025 13:41:28 GMT  
		Size: 63.5 MB (63497964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2254c2dc3c53615f5f6a5adcfafb558670473622cb504cb0a6d02fd2b89d2667`  
		Last Modified: Tue, 01 Jul 2025 14:10:41 GMT  
		Size: 183.4 MB (183421934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c312814d252c566d3c3ee8f98763bedd5510a970a7460965bac0ea117ac8071c`  
		Last Modified: Tue, 01 Jul 2025 21:03:03 GMT  
		Size: 283.4 MB (283362703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a4f9cf4a09562544ef011200268fb453c235bc5b972df93f32ca2dbf4ac1e349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15684597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afc1cf86bd3504dbe315e3c93562fc2ff8e92d15305627e7b38023518ec873b`

```dockerfile
```

-	Layers:
	-	`sha256:39dbb3c0f9a78d73aea412786fb8fabb2d333d5f18f4608bab4734aaa8e60fd7`  
		Last Modified: Tue, 01 Jul 2025 20:45:07 GMT  
		Size: 15.7 MB (15671458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d32a8a23e2b1c8cb3fdec2c521041d1a7fc5c908e5a6ce6bd3048f58dfefe8`  
		Last Modified: Tue, 01 Jul 2025 20:45:08 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:8eb96c7c77c04660a95d5e256869de0a18130f97624ef75c522ea886d4e51d95
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
$ docker pull rust@sha256:4fe592966775f3396e3d099d674f0664e4383336371ca5600e40c2fe3b575383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526479452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e24231a2d9ba56b24304902b7106252b1ba5aa98dc98b58ac09df699a11813e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06772a4eff3df697497bb68b4dcdeb97fdb9338b5e7dde7d1a53579c3203c9ba`  
		Last Modified: Tue, 01 Jul 2025 03:20:06 GMT  
		Size: 54.8 MB (54757481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd49c17bd36c59d7bf7afe446ee52f36cad8a6393628526989f2db44b4486c1`  
		Last Modified: Tue, 01 Jul 2025 05:11:29 GMT  
		Size: 197.1 MB (197142751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b35768b15c47fe75ef345baf1601f003231cf7fa1353d4b05177acb4b38d712`  
		Last Modified: Tue, 01 Jul 2025 06:44:33 GMT  
		Size: 205.1 MB (205059062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f26b96d6cf3fe96312784ed4c21daceefd839ea7ec263a286a9c464c17889bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15475219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4229b2d8712383288725ba877fc8da75d82f25002251269162108f995d12061e`

```dockerfile
```

-	Layers:
	-	`sha256:2186b18143b7f42f67f19ba8594c9c55a420158d4af543684506320400941527`  
		Last Modified: Tue, 01 Jul 2025 08:44:36 GMT  
		Size: 15.5 MB (15463971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c86f9b373cccbb5f795ae509ad60503878f0f8e5a247421fd1a6f1461968cb`  
		Last Modified: Tue, 01 Jul 2025 08:44:37 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:d9735061f6bd324ad5d9a6b1f353e919d01b9515946a2de100568511a1182afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.9 MB (527938900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c390dbe5f1131b80bb7b105624994b79e2115d8dec0bcace50edd510c2198b13`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:efcf40eae0046ccd92d3b47ff685e1e9cf7a34d0a92f6de893078f115e01f20f`  
		Last Modified: Tue, 01 Jul 2025 01:15:14 GMT  
		Size: 49.0 MB (49043960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6769ed354ec7fde57e63bdf9788543b96fd8f93923607ad70767b9c4cfa25b`  
		Last Modified: Tue, 01 Jul 2025 08:59:49 GMT  
		Size: 14.9 MB (14880774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28365fa3b8363bfd29e20b4b17838c65ddc4bdacb1bf15ca9af5a4045e4feaf7`  
		Last Modified: Tue, 01 Jul 2025 18:29:48 GMT  
		Size: 50.6 MB (50631320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31eafcbc0a8afc051ea3519738dd6b4e501ce5f603e4a10bdf1f0f6720a29f58`  
		Last Modified: Wed, 02 Jul 2025 00:17:56 GMT  
		Size: 167.6 MB (167589980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d954ab622638b81a76f8faca7f27cdbead519ce4a96bfe58ce0ce8c04de4c07c`  
		Last Modified: Wed, 02 Jul 2025 12:59:39 GMT  
		Size: 245.8 MB (245792866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:533dd51110aa122013299169d3241c8ff7b0a167ac026488a451cc3cf5a32242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15274640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43196c04d844d43946f4c7a75dd78f798c69fa8488debfc89ba320795b1e927b`

```dockerfile
```

-	Layers:
	-	`sha256:652198c66ccabc1746f6054da6a0b040aa11e579f227a638a7db763062f6b11e`  
		Last Modified: Wed, 02 Jul 2025 11:44:40 GMT  
		Size: 15.3 MB (15263315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9c99c87037228c8be536fc6fd298ab2a611a1fbd6a3d52d733fb4a29c90c2d`  
		Last Modified: Wed, 02 Jul 2025 11:44:41 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8b22455a7ce2adb1355067638284ee99d21cc516fab63a96c4514beaf370aa94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.2 MB (487172791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc77b2b3e794e11c9031f129feea6f9dd3649f86a9b70ad373910e70e5761458`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5424250d141bf5f4ec62e698bba9b5695482a3015186d3b14a633da8916bf7dd`  
		Last Modified: Tue, 01 Jul 2025 06:52:24 GMT  
		Size: 15.8 MB (15750716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7766ba090abb327ecb7e9e14ac90bbcc45c5ba6bb8a568ae531c960ff1acad55`  
		Last Modified: Tue, 01 Jul 2025 13:29:45 GMT  
		Size: 54.9 MB (54855722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1801db58ebce0297c6d03187f6e882ae0b8ba8838f3e18a17f3bcd9137be277`  
		Last Modified: Tue, 01 Jul 2025 20:13:40 GMT  
		Size: 190.1 MB (190053793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714498f74a0f367b5e69c9e7e3bd688c25db146ed8b97acec1446cb2218e705`  
		Last Modified: Wed, 02 Jul 2025 06:40:03 GMT  
		Size: 174.3 MB (174260306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e2730dd90c1b51e30c613c774511479688800225d93c02bdaf36189e99891fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15477294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b9b0c706b4ad223660013177c4a118765a26d87add26bb8babfbdf979efb1d`

```dockerfile
```

-	Layers:
	-	`sha256:12453b011a0f7bb3aac0c83948f50551f0d4d5ae1b1e0c7c3a472d44e1f5c7da`  
		Last Modified: Wed, 02 Jul 2025 05:44:46 GMT  
		Size: 15.5 MB (15465942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccba5cc2249b25264628303f496f30cecf3ead2e13e1dc3399d7f98b1951ce12`  
		Last Modified: Wed, 02 Jul 2025 05:44:46 GMT  
		Size: 11.4 KB (11352 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:2aaf00b554cd4ff148c16a3e58146641b87aa7c629bbb67c6731554afa3c2d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 MB (556215637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab21c61c4d19a041fcae82560e48bb7233059e80ef65189d4d830b0493e23dbc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113be81052ec8e8323c4db158dc9c99295355934e950a6367e5c27038fd1e04c`  
		Last Modified: Tue, 01 Jul 2025 02:24:43 GMT  
		Size: 16.3 MB (16268907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05b439f6df174e28bd21dc59eead603def3bcbd47ec6462f86b7758c4db6ef`  
		Last Modified: Tue, 01 Jul 2025 03:19:57 GMT  
		Size: 56.0 MB (56049937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d170ad31938c07c5739c923eaf5f7569c644e2ea2ead929bbc107d7eac895f78`  
		Last Modified: Tue, 01 Jul 2025 05:11:30 GMT  
		Size: 200.0 MB (200043566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7271fc5f55db8e0b012c06b0785adf36c8ade5d9f290c40fa07be956a5eecde`  
		Last Modified: Tue, 01 Jul 2025 13:00:23 GMT  
		Size: 229.2 MB (229163293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3cb1daa21e1c22f0ea3d5100504d1da2f45a788bcf4f0c42396ea073969b5df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd9075c8dc525761d3e7cf32a7d172eaaee78ecc359ee8f83da3b6bf52859ef`

```dockerfile
```

-	Layers:
	-	`sha256:4ba2cd6c29aab7b896485ed38a1fc73dd8448a29ef9bf4744495334a3e930f89`  
		Last Modified: Tue, 01 Jul 2025 08:45:13 GMT  
		Size: 15.5 MB (15450673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8861a1fd041f7cf768c0ad3c6f4dc87d554c6bcb084c979d61f7a6af8ff9a715`  
		Last Modified: Tue, 01 Jul 2025 08:45:13 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:1c7eb658b16d48458a4808f15de8264a3c20d449d0cabdae47654d98e9dcecfb
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
$ docker pull rust@sha256:b0c0357c60eca8fe29b8280974a44483a28319278a5ff5c57b3e7e9c5708f643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbda49f92a1f159dfbe623e790c2a5b9c1c6c3ba68bd9e362679a9cb48c4925e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff2b7b26c381c0c4ba90768f39bf5193252f27f4e625debf008d09438b195ef`  
		Last Modified: Tue, 01 Jul 2025 05:08:00 GMT  
		Size: 275.8 MB (275821106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:ade5b81bacfe5c6c7e52b85eafa1965c8ff433a6b2c5dbe95ffdac9b636a4098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a4805359ec86648c4fa15446b7df199cdb6a6e1a03490dcb11b527cd557473`

```dockerfile
```

-	Layers:
	-	`sha256:7df8be7b6f1e71053bb68baafbd18a0da5e3196678a329e5267ab3a5a709ffd6`  
		Last Modified: Tue, 01 Jul 2025 05:44:31 GMT  
		Size: 4.1 MB (4094552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a712f57ad2be1eb1eb0de48182654c5bcff269ed26b9ac1f7e737790730b63d`  
		Last Modified: Tue, 01 Jul 2025 05:44:32 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:85f37f11d046da1808026326b03493679b5d14c2f0f4523cf5bc8d5cc0e0ee0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317565661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7f9b3c433121c615480c6153d82080be95a30629221317a4cea09c08b0a573`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4db19ae3ab5266032020a2b07eb5414e4e5af2ea274e14d76e0e545b488f04d`  
		Last Modified: Tue, 01 Jul 2025 21:04:24 GMT  
		Size: 293.6 MB (293626917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:f5c7c3079e6be98cf7906e069b6a07af60bc9f5410e2deba15738732d1776661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b45c40a162ec803cc4480e1a932c1658154fae9d07c32b6cd1ff7053f34a7f7`

```dockerfile
```

-	Layers:
	-	`sha256:c7b3d0ac3ecfb43b93f6888077022d4165a1bd97012372bb37d32a5e2e76ccde`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 3.9 MB (3908981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd6ab2ec5e6066af386464396673a5d060f5b1a51cf8099cafde5bf8cb46451`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:35d3b11bbc6b7f45a174551689621906e5785d4e6e79f2aa3b4ace967a97a055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268179917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1880617faa9ea5bc0df720923e7d75c521d91fc7a3583e3360d6068d359c2b84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e130c413bba66f1a532f016096e1ca99fc7921a6d03f4ae5e7eef4f9de7197`  
		Last Modified: Tue, 01 Jul 2025 14:52:04 GMT  
		Size: 240.1 MB (240102239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b42e61db7f4c7471a71877c4a53f4d0391e7954c21dc20f7a3973cec0a2e7057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd222f432ceb8c15e86b58486cf5fd9c4582036ac9dcb8cede1be44821594ae1`

```dockerfile
```

-	Layers:
	-	`sha256:4c92de7432ff997c7c9d6fd67c06d2e50d70c9800c27e05fa0d04b2dcc4d42dd`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 4.1 MB (4116896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d1589208f0a8f59560905b8c36a4c4ecf08601526c55cbaaabc4a10846fb78`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:ff6fcb7ad6293f4a4c28db122754d93e024b99ca56a9f5027ddced08234ef721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325992228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4eb540ded896f027e6b1931f38d7618a4364b4643343cf6a82ef2de0e775e79`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3f2ceb310dae022b26d227eecca523fe07e1383bbc8cf746de0a949d9a3650`  
		Last Modified: Tue, 01 Jul 2025 06:01:36 GMT  
		Size: 296.8 MB (296779796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:310296d66708c74b8f7df786253dabb1763763f3ae996499d228c97b5defc6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad4a9c0226f971d47fbf4e1e3b0972b7052bb0257233fab74bc5c4b8783fb1e`

```dockerfile
```

-	Layers:
	-	`sha256:2a6a2a00284fbce671a5f0f7c61ebfbf8c2d5771cda8a1bd5445be27b699d096`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 4.1 MB (4073915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d875623e01bac8366b22e9a8bf9378721a880661602db1d20b97da37bd0c7c2a`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:e00cab06ebef6d7bb5580cedac63b15bf337fd68225ac6a152bdeb1d08bca552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374561374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8452adee592dd5981efa36540ccd9dd66cc2273fd2272ece300389cc198997a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a95af4d06128b392493eba88f8150c9e90691be1c0f0e8024d5929b44de3930`  
		Last Modified: Tue, 01 Jul 2025 13:00:07 GMT  
		Size: 342.5 MB (342488554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:ad4355591f63f7acdbf5366f8fb6d2241920c664d093c0327bd30a320b228ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687a2175e85119fb64fa7d37bd7720459fed5f9513594f53bbddccbef9cbce8d`

```dockerfile
```

-	Layers:
	-	`sha256:b40dd3069d53ab3fd2d2a8604ee2b563e69d54a6f2f4e29cd2f5cb441d80ae60`  
		Last Modified: Tue, 01 Jul 2025 11:44:38 GMT  
		Size: 4.1 MB (4066865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44f89002a1ae239b997acfc875a4c4a4fc8423278688b1ec444ca96cf66b74f`  
		Last Modified: Tue, 01 Jul 2025 11:44:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:1cf72ceabd44d186a6f08948bad51ee0050ed17cb47657c6b74e1e879451a34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360392180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871910d1ab2a752b966ffce7ec56ab4866c791bce0f9fc075cb26d7744e75884`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8a3025335a2a160722cb689b6c389f0316ea4b027c2dad34fef52df858c365`  
		Last Modified: Tue, 01 Jul 2025 10:42:01 GMT  
		Size: 333.5 MB (333504369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:d04b9fa09c2d16e830240aaa30f0b46002ffc117461d7109c104bd5c6732a461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6791cd1d0129cc03fe2cbcb7c2269397f8348bb85df5bd5b9a8e6575a8923e`

```dockerfile
```

-	Layers:
	-	`sha256:2a8e89592d0564890623c9199bb211483a145b510ce0c49afc579dabe00180f9`  
		Last Modified: Tue, 01 Jul 2025 08:44:56 GMT  
		Size: 3.9 MB (3932230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52770394e7f7570572f6a897500a0bc0f14d82302ff5f32b5db7076d7a67ab3a`  
		Last Modified: Tue, 01 Jul 2025 08:44:57 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:1c7eb658b16d48458a4808f15de8264a3c20d449d0cabdae47654d98e9dcecfb
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
$ docker pull rust@sha256:b0c0357c60eca8fe29b8280974a44483a28319278a5ff5c57b3e7e9c5708f643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbda49f92a1f159dfbe623e790c2a5b9c1c6c3ba68bd9e362679a9cb48c4925e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff2b7b26c381c0c4ba90768f39bf5193252f27f4e625debf008d09438b195ef`  
		Last Modified: Tue, 01 Jul 2025 05:08:00 GMT  
		Size: 275.8 MB (275821106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ade5b81bacfe5c6c7e52b85eafa1965c8ff433a6b2c5dbe95ffdac9b636a4098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a4805359ec86648c4fa15446b7df199cdb6a6e1a03490dcb11b527cd557473`

```dockerfile
```

-	Layers:
	-	`sha256:7df8be7b6f1e71053bb68baafbd18a0da5e3196678a329e5267ab3a5a709ffd6`  
		Last Modified: Tue, 01 Jul 2025 05:44:31 GMT  
		Size: 4.1 MB (4094552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a712f57ad2be1eb1eb0de48182654c5bcff269ed26b9ac1f7e737790730b63d`  
		Last Modified: Tue, 01 Jul 2025 05:44:32 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:85f37f11d046da1808026326b03493679b5d14c2f0f4523cf5bc8d5cc0e0ee0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317565661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7f9b3c433121c615480c6153d82080be95a30629221317a4cea09c08b0a573`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4db19ae3ab5266032020a2b07eb5414e4e5af2ea274e14d76e0e545b488f04d`  
		Last Modified: Tue, 01 Jul 2025 21:04:24 GMT  
		Size: 293.6 MB (293626917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f5c7c3079e6be98cf7906e069b6a07af60bc9f5410e2deba15738732d1776661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b45c40a162ec803cc4480e1a932c1658154fae9d07c32b6cd1ff7053f34a7f7`

```dockerfile
```

-	Layers:
	-	`sha256:c7b3d0ac3ecfb43b93f6888077022d4165a1bd97012372bb37d32a5e2e76ccde`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 3.9 MB (3908981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd6ab2ec5e6066af386464396673a5d060f5b1a51cf8099cafde5bf8cb46451`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:35d3b11bbc6b7f45a174551689621906e5785d4e6e79f2aa3b4ace967a97a055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268179917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1880617faa9ea5bc0df720923e7d75c521d91fc7a3583e3360d6068d359c2b84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e130c413bba66f1a532f016096e1ca99fc7921a6d03f4ae5e7eef4f9de7197`  
		Last Modified: Tue, 01 Jul 2025 14:52:04 GMT  
		Size: 240.1 MB (240102239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b42e61db7f4c7471a71877c4a53f4d0391e7954c21dc20f7a3973cec0a2e7057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd222f432ceb8c15e86b58486cf5fd9c4582036ac9dcb8cede1be44821594ae1`

```dockerfile
```

-	Layers:
	-	`sha256:4c92de7432ff997c7c9d6fd67c06d2e50d70c9800c27e05fa0d04b2dcc4d42dd`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 4.1 MB (4116896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d1589208f0a8f59560905b8c36a4c4ecf08601526c55cbaaabc4a10846fb78`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:ff6fcb7ad6293f4a4c28db122754d93e024b99ca56a9f5027ddced08234ef721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325992228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4eb540ded896f027e6b1931f38d7618a4364b4643343cf6a82ef2de0e775e79`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3f2ceb310dae022b26d227eecca523fe07e1383bbc8cf746de0a949d9a3650`  
		Last Modified: Tue, 01 Jul 2025 06:01:36 GMT  
		Size: 296.8 MB (296779796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:310296d66708c74b8f7df786253dabb1763763f3ae996499d228c97b5defc6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad4a9c0226f971d47fbf4e1e3b0972b7052bb0257233fab74bc5c4b8783fb1e`

```dockerfile
```

-	Layers:
	-	`sha256:2a6a2a00284fbce671a5f0f7c61ebfbf8c2d5771cda8a1bd5445be27b699d096`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 4.1 MB (4073915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d875623e01bac8366b22e9a8bf9378721a880661602db1d20b97da37bd0c7c2a`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:e00cab06ebef6d7bb5580cedac63b15bf337fd68225ac6a152bdeb1d08bca552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374561374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8452adee592dd5981efa36540ccd9dd66cc2273fd2272ece300389cc198997a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a95af4d06128b392493eba88f8150c9e90691be1c0f0e8024d5929b44de3930`  
		Last Modified: Tue, 01 Jul 2025 13:00:07 GMT  
		Size: 342.5 MB (342488554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ad4355591f63f7acdbf5366f8fb6d2241920c664d093c0327bd30a320b228ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687a2175e85119fb64fa7d37bd7720459fed5f9513594f53bbddccbef9cbce8d`

```dockerfile
```

-	Layers:
	-	`sha256:b40dd3069d53ab3fd2d2a8604ee2b563e69d54a6f2f4e29cd2f5cb441d80ae60`  
		Last Modified: Tue, 01 Jul 2025 11:44:38 GMT  
		Size: 4.1 MB (4066865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44f89002a1ae239b997acfc875a4c4a4fc8423278688b1ec444ca96cf66b74f`  
		Last Modified: Tue, 01 Jul 2025 11:44:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:1cf72ceabd44d186a6f08948bad51ee0050ed17cb47657c6b74e1e879451a34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360392180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871910d1ab2a752b966ffce7ec56ab4866c791bce0f9fc075cb26d7744e75884`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8a3025335a2a160722cb689b6c389f0316ea4b027c2dad34fef52df858c365`  
		Last Modified: Tue, 01 Jul 2025 10:42:01 GMT  
		Size: 333.5 MB (333504369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d04b9fa09c2d16e830240aaa30f0b46002ffc117461d7109c104bd5c6732a461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6791cd1d0129cc03fe2cbcb7c2269397f8348bb85df5bd5b9a8e6575a8923e`

```dockerfile
```

-	Layers:
	-	`sha256:2a8e89592d0564890623c9199bb211483a145b510ce0c49afc579dabe00180f9`  
		Last Modified: Tue, 01 Jul 2025 08:44:56 GMT  
		Size: 3.9 MB (3932230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52770394e7f7570572f6a897500a0bc0f14d82302ff5f32b5db7076d7a67ab3a`  
		Last Modified: Tue, 01 Jul 2025 08:44:57 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:12d9a0ff4f3c87badbf56a27ffd6c4774ebe1b5fe5c6b7b1a39cfee537fcb62f
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
$ docker pull rust@sha256:fc66d738f64bca39b62f4a8602bce8239a58d813a073dec6eb87c26ed46190c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead6f32afcd0798a56c170ce2851030ab2ae5772cc7aaaec8b47346331cd33a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d114182f83d2bc4d73e02cc5bb74bda2938943a605a1efe8e8e5921a9334c06b`  
		Last Modified: Tue, 01 Jul 2025 04:34:37 GMT  
		Size: 265.2 MB (265206650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f2b2479ca7328f021feef75a9a45f117ffc3ee13a53990561c1dde6401e77ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e7b91d95fa7f94247595b016c4b0afdf5c4568be554c642efa57ecedd45917`

```dockerfile
```

-	Layers:
	-	`sha256:17df34ae2e3f1174c3451942d63bf066080013096af8da1c1fae497282282c74`  
		Last Modified: Tue, 01 Jul 2025 05:44:38 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86c3b78ad1853f15af29c20213d59684bc1b948a20593345e4229e0c91d938ac`  
		Last Modified: Tue, 01 Jul 2025 05:44:39 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:2a8251a939f0d13ed2a1ea24d1f9ef251bbbf030d520485b394de2b9c23f1575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313623477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b182ed292d4c08791794619177de2b422b06a63b5f34f388d6e1f7c828ccf4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:96b51e81cdb8508366118f41a9ec499f52f0d0211b084d5d516e1be131b35266`  
		Last Modified: Tue, 01 Jul 2025 01:15:21 GMT  
		Size: 25.5 MB (25544163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e8ad713014c96437118acd9656b3f10b47964888722c469680e6042510ccb`  
		Last Modified: Wed, 02 Jul 2025 00:48:15 GMT  
		Size: 288.1 MB (288079314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d16acf27c46754346860ce745ea5760b105c162694adc9d454c94f795a796f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2cfe874064a2b600d64ab76c2b059316a0d09778b241f6d9ef1fe2850a3e56`

```dockerfile
```

-	Layers:
	-	`sha256:08e8559715569c50dc0f3e68ebbed15841af5fa459ca720c38fa15b3c2a035d4`  
		Last Modified: Tue, 01 Jul 2025 20:44:41 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffbb508550ec246d38153bd7938e330e200f9c02ca0f0d1d4b1abcc527101490`  
		Last Modified: Tue, 01 Jul 2025 20:44:42 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d7bf42de9bb8c46335f1541a795bd167560ad0c7d211e67cad3f5a7417243fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258705512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28cce79db40ab1d0fa12cbfa105d6ef1dff13b63c1a93b8fb9e9682a0418a59`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4458b4f354b132ede276e7da54a33c211b23ceac4f34da5ed2b7fae09bb95d6f`  
		Last Modified: Tue, 01 Jul 2025 14:45:32 GMT  
		Size: 230.0 MB (229961372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f8cb1c53bc02e47f1e50499e70854d43e2f98ddf439fa5b52d34a6424733aed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f09370c05fb448311182a49164c612c0299712281c47b1564078e73ebb6a67`

```dockerfile
```

-	Layers:
	-	`sha256:263fa190fe34f81500ba2e8ac8bf53f05869282f02579d474166a6be2567d51c`  
		Last Modified: Tue, 01 Jul 2025 14:44:39 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a44a181f21adc0542d1acb35f17b1f20343532cfd22efc73efb5044556e05115`  
		Last Modified: Tue, 01 Jul 2025 14:44:39 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:6aeeeeaf3ed73638e4135dce21527f418f6a192d3e2de9c4d26664694f90c0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.1 MB (321133034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e7dcea35fc6893afae54fc7ac2446ea032b06889451f72c5fb09918d9ba66c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:40be1da6146972d9df50a98eef7b5c0f729cd95a3a38782418f354f3b9355a9a`  
		Last Modified: Tue, 01 Jul 2025 01:14:57 GMT  
		Size: 31.2 MB (31189680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e1a302797c6fe4ad387e823eb711877bfcee5af925dcfc3decc2b4083fef72`  
		Last Modified: Tue, 01 Jul 2025 12:59:38 GMT  
		Size: 289.9 MB (289943354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8c4db6ccf78a02913434449b05bc26924375a6fa2a57e1fb8cdc0a9149a6128d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60622052414fe9b2982743aeebbe224601c12752ff8f4cbe89d50b54c59a8ad0`

```dockerfile
```

-	Layers:
	-	`sha256:423e3a39660d3cd9304a2f3cd9a7f0037ec79d19c72661b55bb7ed8a8d78a9ad`  
		Last Modified: Tue, 01 Jul 2025 05:44:54 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a0678dc17cc916be60884c0469158c1664b2dcd59755d390b82d7f534f97fa`  
		Last Modified: Tue, 01 Jul 2025 05:44:54 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-trixie`

```console
$ docker pull rust@sha256:e68d2ba3397c3c04c47647ad5d615afaca80ae00dcc4f5140e43495c537746c6
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

### `rust:1-slim-trixie` - linux; amd64

```console
$ docker pull rust@sha256:7721d2705af97fbfbf241d1f329e1e7144cb2743b2ecac5711352c8ea4fe3251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310236807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0d0605178c491bdb2bc093d06776322acffdddadb8d6b3ae47a7aba111cc68`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2b9064154c24154965e1b574cfe4999144b627db7f678b3a566d3eeeac02dc`  
		Last Modified: Thu, 03 Jul 2025 20:42:04 GMT  
		Size: 280.5 MB (280475701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:d619583f10fabd5f99a621389b8e4043ffa188cbd8eb305b7c2e7e8f2d63ed54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89914cf1279171e30ef2a59799b98b1a4e83babe84c87f1ff92ef591c7fc3ec`

```dockerfile
```

-	Layers:
	-	`sha256:c1e52b080a5caaa75906ac1aef51b1a4e5905284978a04a29d5def27fdaceafb`  
		Last Modified: Thu, 03 Jul 2025 17:45:05 GMT  
		Size: 4.2 MB (4162901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d4390982a55f7e70f969a7af51b2b195f34be5ebbe6c6f17d939bb524e497b`  
		Last Modified: Thu, 03 Jul 2025 17:45:06 GMT  
		Size: 12.1 KB (12061 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:57b1df7d4a1e8b0b231b0e8a09ae0cf89c7939542d2f1e1ff4a05f7de70f2a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322260431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a609326c1f09c4e6aa554b61b16080a0783429c62de582cd5e3ec4188913f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75cb2c2919cdd5f70bd8208e02191091cad32dd857e56bfd33f35cd6d531c82a`  
		Last Modified: Tue, 01 Jul 2025 01:18:55 GMT  
		Size: 26.2 MB (26201517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49ee1c5650c50a45b3eef84571458d78cbbf30fc06a0035bfa2a082ea8108d9`  
		Last Modified: Thu, 03 Jul 2025 20:48:22 GMT  
		Size: 296.1 MB (296058914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:cc54c83fc01e12d9d41cfdac572a59e588a4c54287deec7161e4b89d69757700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103636073af3a7f76abb00f7559b02484569bf5618ed3d571538a7ca3b02fc19`

```dockerfile
```

-	Layers:
	-	`sha256:ffce2eaa705d9368bce2a80cd6890bc3c2bf66295174b466a2007a02c4370d2b`  
		Last Modified: Thu, 03 Jul 2025 20:44:36 GMT  
		Size: 4.0 MB (3967745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb0ae2602c3fab378c0fcb74ec00c46711ce55c947b8f99952dd9d8fcae5488`  
		Last Modified: Thu, 03 Jul 2025 20:44:37 GMT  
		Size: 12.1 KB (12138 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:88a9c0d2b3c1ef6e0ab769f130a15a6cb2d10ed82ac6c779e1d5b543fa6a5a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274045556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47d037deb756e369db48be32af79a4b9410405268eb60580dffcfc577e67aad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:dfa10e860e0106510a14bae8331a4dd762d3d3737fdba0dbec102458f9853b71`  
		Last Modified: Tue, 01 Jul 2025 01:18:18 GMT  
		Size: 30.1 MB (30126864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab982be4b2f9d93ec333ffb69526256503de560bde0bd8a510e3b1acf793c40`  
		Last Modified: Thu, 03 Jul 2025 20:49:17 GMT  
		Size: 243.9 MB (243918692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:ec6e0fb8e467b4d66a4e91bfc44764be1efadf6791fcd25f1df5437d48d299dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a618e7a2fe30262bf7503eb5b80999a202d3e87df932a890048ca1fcb3b7b55a`

```dockerfile
```

-	Layers:
	-	`sha256:a7390525f3e02590517ad48faeb0649b52dd80e6a083feb652819a8c0320984b`  
		Last Modified: Thu, 03 Jul 2025 17:45:23 GMT  
		Size: 4.3 MB (4254069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad846470cf4d23ec2c6804afdf350c7808432e565fc39d3035fe1556cf21361e`  
		Last Modified: Thu, 03 Jul 2025 17:45:24 GMT  
		Size: 12.2 KB (12165 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; 386

```console
$ docker pull rust@sha256:6fe11019a3d4d7e50e48f4727120357e98b6e3242ea944d72f20a57ccde3976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332943226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c31842ba66bed838d3be4cddc274c3b25d4f5c056d036b9d9c5646f2f83c35`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:27b0922c0fcc2ccb534e806841adaba77d7b1a639b51fa3d953ccfa3af3a57e6`  
		Last Modified: Tue, 01 Jul 2025 01:14:55 GMT  
		Size: 31.3 MB (31281109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfea6381854ff5a1288e44fcd71c127bf8f5c12b73fca05a53a0fdf766da33e`  
		Last Modified: Thu, 03 Jul 2025 20:49:34 GMT  
		Size: 301.7 MB (301662117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:709dfc3e62d11137fe59c004c57be56ba78c0370578c39fc986245bcc924fd3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d862b9c54929822ee442cfebc6bb3152f1e05190d3476d52017e9c30cbe3777`

```dockerfile
```

-	Layers:
	-	`sha256:d76b88999182b5b6e9bf50bf33640536dbe258725e8c01c0e11481b295d36251`  
		Last Modified: Thu, 03 Jul 2025 17:45:49 GMT  
		Size: 4.1 MB (4136434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff406b796b327df9d21a85be2fa42ed6e856e504634069cad7fdc6a139e510ad`  
		Last Modified: Thu, 03 Jul 2025 17:45:49 GMT  
		Size: 12.0 KB (12030 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; ppc64le

```console
$ docker pull rust@sha256:cbef1f31e6e9d539b5e201653bc0553eadee350cf0a81efd0bdc75654187d7c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.2 MB (374189714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fe51377754a44b3b68c6389474ced3297711aa727c85fae16272f257d4d87f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05113943712185aeb07e0e0bfb3fa35e088bd6f08df1e776cc806f8bddc6db1`  
		Last Modified: Thu, 03 Jul 2025 20:50:14 GMT  
		Size: 340.6 MB (340603679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:03e00179fb0709f08bca4819fb0a5100a86a4f3d137fc7e3dd77ed4fb2bb5f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fb1b4f2f8d43288ca62d234578bbfb1d9527b44d43b4e8790007f3e694af6b`

```dockerfile
```

-	Layers:
	-	`sha256:187a0b4809cba5785eef2febd443d1c4537bde12b677052c85f9367e5c060989`  
		Last Modified: Thu, 03 Jul 2025 20:44:49 GMT  
		Size: 4.2 MB (4158025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79ae8b64b453a46d0ae29840bdd1a9e8658feec181cb272ffe4e3c012b5e5bb`  
		Last Modified: Thu, 03 Jul 2025 20:44:49 GMT  
		Size: 12.1 KB (12106 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; s390x

```console
$ docker pull rust@sha256:95bd23402ed6a90153634a026962a9c6cb52036c619765e75882d1401cc2b899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.6 MB (365571899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a7d73fb037181cda5b98fb9704a92758f96457c24664ac81eb41524bc2a693`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:728fbd29b8599bd56dcb8703b5c428523bcf0f3d48c5e95804f60267a128a3bc`  
		Last Modified: Tue, 01 Jul 2025 01:19:25 GMT  
		Size: 29.8 MB (29838345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1456ed2701051abe37f5ce865394b5d3d701095089b1c134b195eebb09d77cb`  
		Last Modified: Thu, 03 Jul 2025 20:51:48 GMT  
		Size: 335.7 MB (335733554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:b3db53400e5e90db3bf6bafadf7ed5ba7942e99fdc2b1f29db7d9338241b026a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717ea3ea743c46facb7642e47482c5e4e2469868c735a4096c86797b8e34e0a4`

```dockerfile
```

-	Layers:
	-	`sha256:f44d67311a40081884ea925705988428fd00e3afd55d1da73c10871c627143af`  
		Last Modified: Thu, 03 Jul 2025 20:44:54 GMT  
		Size: 4.0 MB (3980649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e254e26728aaa08e68b3041c15896d2bbf46234e284651a8ca903e32d7f2794c`  
		Last Modified: Thu, 03 Jul 2025 20:44:55 GMT  
		Size: 12.1 KB (12062 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-trixie`

```console
$ docker pull rust@sha256:b730c57c4c1679f1c847f0481ba8863a15d00cae22d367a7565f4422bf40d478
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

### `rust:1-trixie` - linux; amd64

```console
$ docker pull rust@sha256:777127bd6a86eae87d512c696f1b5d500307cae84a4b948e4b25942516d780ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.5 MB (583494432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392aa965c60a10bdc5365931c80308a245dfea6cc9bbe1aa073fb9cbb6d5c274`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13567152126a6abf6e98a928a4206f022be687e979bd113ce89b0b1f41fcbaf`  
		Last Modified: Tue, 01 Jul 2025 03:19:07 GMT  
		Size: 25.6 MB (25617737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f696393bed22361a2f932d3f084750c0cdf7e1f7186888c327230081e6257b0`  
		Last Modified: Tue, 01 Jul 2025 04:12:14 GMT  
		Size: 67.8 MB (67789682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b76da92f9efb17dc4a68c682bacce1ec791a87b62ee76639b08bfc2ee4577cd`  
		Last Modified: Tue, 01 Jul 2025 12:07:57 GMT  
		Size: 235.8 MB (235764377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9b092ebb229c418b5f5feea9ad11427731515a1d8dbf01adb95c1959d6bac6`  
		Last Modified: Thu, 03 Jul 2025 20:41:59 GMT  
		Size: 205.1 MB (205058759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:8568cd48443fa4a0c33851892d9da52f3d656b2399dcd83e6ea414378cb1e83b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17214539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06eb85b483e6f006b4ae1adf7622a1abf1ed4b6581de2f1824c28c05b4fafb0`

```dockerfile
```

-	Layers:
	-	`sha256:3e339bf185a305476f2c298204c80a4fa1d966d3dea7c9964a8704dd8772bff2`  
		Last Modified: Thu, 03 Jul 2025 17:45:24 GMT  
		Size: 17.2 MB (17202584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4abb423fff15f1c22361c92de405fb0ef8a88535b600fc76d86d707b3b09260`  
		Last Modified: Thu, 03 Jul 2025 17:45:25 GMT  
		Size: 12.0 KB (11955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:f0d61b9434bb38e2fc365679bf6ca2b15ac36a477ee4488bca51ab2432ded2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.7 MB (570716850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e270a7c2c6520ab1bc80e5bf40b5af01074724375045b6d1103cd5fab68e50`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0611a9c58dddfe7f00bb5fe6c8f5ccecfceeb1785acc68dc070068a94adf2092`  
		Last Modified: Tue, 01 Jul 2025 01:18:31 GMT  
		Size: 45.7 MB (45708080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571abb678dad668afa2696a67ffe4981c3b5aeb37fa4c14a0cc24fdac7949b6e`  
		Last Modified: Tue, 01 Jul 2025 08:59:50 GMT  
		Size: 23.6 MB (23617932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd28b3d9ecc5ff8b97a4e765e8a818c8ca6ea137650adb3df7d53acf265e9e4e`  
		Last Modified: Tue, 01 Jul 2025 18:31:52 GMT  
		Size: 62.8 MB (62760034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7255cfd7fa333e12d9432924dd0af6dceb8b6fca12f12faa2b5157b7e9cacc6`  
		Last Modified: Thu, 03 Jul 2025 10:55:31 GMT  
		Size: 192.8 MB (192838492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990aa9e5561becb9a9a31b185a40c4e082059b4a2f864a5ea4a0c72aa5306a5`  
		Last Modified: Thu, 03 Jul 2025 20:42:55 GMT  
		Size: 245.8 MB (245792312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:6eaf53d99ce3e71a7ea943eea06e0b1786528694755a32e99ac4ee29064aa755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16982621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8631aabd5bb545bf8056ef9539ea5075a0a8067a69adf2344dc7f33f9dcfbe7`

```dockerfile
```

-	Layers:
	-	`sha256:e1b2e6ea0d58fef7a142159e950d4cd70fad767db1159baa5d2ca9e850c1b39f`  
		Last Modified: Thu, 03 Jul 2025 17:45:54 GMT  
		Size: 17.0 MB (16970590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895c99ae34ac4942be372edd159f3a98dfcc60436b134a088738443b03f4f306`  
		Last Modified: Thu, 03 Jul 2025 17:45:56 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7c5ac5114acbafb83337d764aadd88ca774223507a916c6dd30bb082a20ec7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.5 MB (542536176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0697dd2649fdc7fa59d4cf781665f05caae4122011784ccef9a0f023a0570c48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064b8e4cb92aed27a99de363dac49c85bcb74d556fa925c921727dcdf03f7cb4`  
		Last Modified: Tue, 01 Jul 2025 06:53:32 GMT  
		Size: 25.0 MB (25008002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01789681d750567cf92706d649b58054ae1e27e35947e671160777a30538c3a2`  
		Last Modified: Wed, 02 Jul 2025 05:58:28 GMT  
		Size: 67.6 MB (67611970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4fcde14125f9212ba8ee255667590e6596810c45bdc694a8db749d7ff6d2bf`  
		Last Modified: Wed, 02 Jul 2025 06:00:35 GMT  
		Size: 226.0 MB (226025553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65018ead03f0d4f0382753ee911bff501d98c7ce180a3aabfb426c24deef1054`  
		Last Modified: Thu, 03 Jul 2025 20:12:11 GMT  
		Size: 174.3 MB (174260497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:5fd381b02f79c5c1f30501a2e74b4143d494518193a407ab4bd263d5d4495b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17298951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960a72fcf1731c737694fba1d68b27e7546e2cafa11ed72bdf7a1711136c2ca5`

```dockerfile
```

-	Layers:
	-	`sha256:beca260f3051e49975118b198c4e96523199398c5bfe36285d4ffc2c15e5afe1`  
		Last Modified: Thu, 03 Jul 2025 17:46:11 GMT  
		Size: 17.3 MB (17286892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637b38306d48fc5fd76b15fe7b2603dc5a04735734490c149d9278c4bd7ef21e`  
		Last Modified: Thu, 03 Jul 2025 17:46:14 GMT  
		Size: 12.1 KB (12059 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-trixie` - linux; 386

```console
$ docker pull rust@sha256:d4508bf7617fc0667b9f76693bfb223e42469dc1abfd62bc4affcf61fdec1d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.4 MB (616411351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f713341993075dddfd01eb0a193e3e5a746dc11f9c4688e2c3c41ab15827a02`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d223755a7489df8352d3a71955e26d35281b9c0f0609e017af54d9e75e3b435b`  
		Last Modified: Tue, 01 Jul 2025 01:14:59 GMT  
		Size: 50.8 MB (50786756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d932d83e6c250bb0f5c2003ae98b3b4dc3d40d3915a7ebed763f315741368`  
		Last Modified: Tue, 01 Jul 2025 02:24:58 GMT  
		Size: 26.8 MB (26772148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34925744005802787be957c67125f2aabf94afd5e8609668cc037c46d09591`  
		Last Modified: Tue, 01 Jul 2025 03:20:07 GMT  
		Size: 69.8 MB (69830306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f64900f9b3ef26b18f567a74a96e250e42a8eed2ff1fadd54a41cc0359ad74`  
		Last Modified: Tue, 01 Jul 2025 13:17:44 GMT  
		Size: 239.9 MB (239860428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786dd06ef0c1d508b04b744e9509815e8b97edb82567dae2ecc2f7f4608eb087`  
		Last Modified: Thu, 03 Jul 2025 20:45:12 GMT  
		Size: 229.2 MB (229161713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:f67a9186cf1554037b5bebdc2a29731e33b0560fb6f00acc72a972c06a6a8024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17182790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fa8116b6bed9af5ae6689a9a22779a1678697a915c5cd4d7e6b36066700e02`

```dockerfile
```

-	Layers:
	-	`sha256:0bc4ae22361d8be206beacebda88e0a0d9907d13fe49752729264b691a2573a4`  
		Last Modified: Thu, 03 Jul 2025 17:46:46 GMT  
		Size: 17.2 MB (17170867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00512048af2e89f74659ec4afeed8cb648de2fbc4c194e045bb7360d66547db4`  
		Last Modified: Thu, 03 Jul 2025 17:46:47 GMT  
		Size: 11.9 KB (11923 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-trixie` - linux; ppc64le

```console
$ docker pull rust@sha256:2b364c8eda85704eca9497cb33fca2d56eef23b799891c48db05140faffe245c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.9 MB (657910004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e48352ed179962dff629d52064abbff1ea21fc4849959f709243b2e442fae7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e868292aa714037cbba25d912564e5f392a5d355c383b03a8854e789c98ef`  
		Last Modified: Tue, 01 Jul 2025 05:08:57 GMT  
		Size: 27.0 MB (27003269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7107fc95f855d7880e921bbc85bf915f07c907c70d7d6f6a5334a32ad6c832`  
		Last Modified: Tue, 01 Jul 2025 10:12:36 GMT  
		Size: 73.1 MB (73068943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4744a5ce78804175c7109fb3df660a6bb53b2954bc5f2c48184739c714dfc8`  
		Last Modified: Thu, 03 Jul 2025 10:55:19 GMT  
		Size: 231.0 MB (231021360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c94c7eb559acad5a878c6b10fbcb0ecafad636824170be34ede5261baa6a2`  
		Last Modified: Thu, 03 Jul 2025 20:46:35 GMT  
		Size: 273.7 MB (273719196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:712f5014e1f676151678dfb32f438ebfc5c6ccce041ee1bfe0822c9f6e6a92b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17208092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e648406175ad5a0fff773fd402a380664ca93211dc1dc02b0e30ec1857290a`

```dockerfile
```

-	Layers:
	-	`sha256:e90c41129150eeb1baf61bb144eb1a5bf5136c3753a5e7ff747a93519edbced8`  
		Last Modified: Thu, 03 Jul 2025 17:47:19 GMT  
		Size: 17.2 MB (17196093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:223be277a3e6da23a3d10ec7c56a85066daeacf3199f6e2852aed61471673c6e`  
		Last Modified: Thu, 03 Jul 2025 17:47:20 GMT  
		Size: 12.0 KB (11999 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-trixie` - linux; s390x

```console
$ docker pull rust@sha256:b78680ff95452516a2a1ba080766115b52b09915350132aa95d221d83bb4a29f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 MB (634484977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b39c24e77ca6d3f82b32ead83f3c0c127e66c3c126e6397457389779e52ec7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8974c848015ae735631f879693069b8c536e3428274d79917837c027655a80`  
		Last Modified: Tue, 01 Jul 2025 05:31:56 GMT  
		Size: 26.8 MB (26785709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7360cccf58cfa285cf20d3ce14642c23bf3a2795b93396d0b9b743ee2e0779`  
		Last Modified: Tue, 01 Jul 2025 08:59:15 GMT  
		Size: 68.7 MB (68663824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694ce909d21b7fbf7c3fb87f40db93cf7588c89986fe25d341208d7b9ae60852`  
		Last Modified: Thu, 03 Jul 2025 10:55:27 GMT  
		Size: 206.3 MB (206329374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2362089a7d48f29102d6359bd8041b42be3e05af339f3916bfaefb996c680c`  
		Last Modified: Thu, 03 Jul 2025 20:47:14 GMT  
		Size: 283.4 MB (283362410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:f0605e4fb8dba38beea68b41893e3e6983c85a8d7ebe00d7b438ec8414f6d6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17001023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fec9741de5a55dec8253a44c86e746da1d1ec5db93d53031d57e5006c179026`

```dockerfile
```

-	Layers:
	-	`sha256:56417f7df327de8d5d5e7e0de1e2f59e7226739f9c6c2324cd0165abb66c39d8`  
		Last Modified: Thu, 03 Jul 2025 17:47:40 GMT  
		Size: 17.0 MB (16989068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bba5fb71a8222ba1b28462e4175f250445ba54f02cf3948e9d08d931e57d0ec`  
		Last Modified: Thu, 03 Jul 2025 17:47:40 GMT  
		Size: 12.0 KB (11955 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88`

```console
$ docker pull rust@sha256:5771a3cc2081935c59ac52b92d49c9e164d4fed92c9f6420aa8cc50364aead6e
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

### `rust:1.88` - linux; amd64

```console
$ docker pull rust@sha256:95f6d6956bf8abd7461763ba7ccd243d8964a41c8eb3f41d895490c782628d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553347880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a479811b82446e6bf598238bb2fcd3ae41b351a1a7c87e53d8f2333a7bbe001d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe9c1abe6f3b8ca9fc6abe710405f830f95262f1d356e8f6545d823b5840a5c`  
		Last Modified: Tue, 01 Jul 2025 05:12:07 GMT  
		Size: 211.4 MB (211373500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0545d5f3de1a8249849f4342031613d732af87e31f13755f5fac287119ed13e8`  
		Last Modified: Tue, 01 Jul 2025 06:18:35 GMT  
		Size: 205.1 MB (205059525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88` - unknown; unknown

```console
$ docker pull rust@sha256:0e0dc34caec6b81f1b5ab4c9a559c11b4d7440382c69d8a2cdbe5002a71523e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15877001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81308c8e2c35f38fbef285c685f2ca642508d83efc22df71984838afd98ac55d`

```dockerfile
```

-	Layers:
	-	`sha256:3260e53bff48cf37775cac874c3e2920680f90a7669e12d2c322771f16c50614`  
		Last Modified: Tue, 01 Jul 2025 08:44:24 GMT  
		Size: 15.9 MB (15863862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a629d4f8f234144e7bda08172e21d63709f916bfe46836348a616c43d2cdd880`  
		Last Modified: Tue, 01 Jul 2025 08:44:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88` - linux; arm variant v7

```console
$ docker pull rust@sha256:b12fb2b0506d2b8fde83230531af65c46d2e1cb65c7b965a23de3015d7feff05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546880259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe31256245950fcf402e7f41d298a8bd3859cf9558a2e1ff584d64071362bda1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc606b1195a348c6a47399c1a54ab936d4477a526d62306ddce89fe76a2d22`  
		Last Modified: Tue, 01 Jul 2025 08:59:56 GMT  
		Size: 21.9 MB (21928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f4c85f426e2c955b1dac4fa88bc182d725644c23ad01bdcbf64d9664e34a8`  
		Last Modified: Tue, 01 Jul 2025 18:28:59 GMT  
		Size: 59.7 MB (59656492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda2264dd6dda88971c220cda9283a6c337d04aeb92012d9d160887d4ec0b556`  
		Last Modified: Wed, 02 Jul 2025 00:17:51 GMT  
		Size: 175.3 MB (175294922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5ff6581ced6c9c0cc98e703fa5901cda1814bee9d3ac91337dfcb2eeaa3fa`  
		Last Modified: Wed, 02 Jul 2025 12:16:49 GMT  
		Size: 245.8 MB (245792330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88` - unknown; unknown

```console
$ docker pull rust@sha256:a6b6613abe69a8ea05c159027354fad9e25a0f58f5a61a4c761bd608e9118f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15679627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0222859d21f0de033a308a561262ae0c61dc1ab6441395c68809f9d9455913d`

```dockerfile
```

-	Layers:
	-	`sha256:d6bf21d47ea4882f2e19fc8c2018d3473ff3633b948a8a2912ffa2fb5dc5c75c`  
		Last Modified: Wed, 02 Jul 2025 11:44:31 GMT  
		Size: 15.7 MB (15666380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f88163f4b88d616cf50cd1d0bb3bb47eda6485492c98f7f4bc8035c0d832d762`  
		Last Modified: Wed, 02 Jul 2025 11:44:32 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:66b553fe51fe4eba929ee31c39d66506fe41b72cf403dab3117de2bd5d43e645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513346599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5424600217354e80a3f0ab99133ec64aa48f464a2f1c29a93cbd0f95758e5af7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a65abb6272f500a9ae5d14c9ae8ef9cb0e4009b02acfccb4dabc478f252d44`  
		Last Modified: Tue, 01 Jul 2025 19:38:43 GMT  
		Size: 202.8 MB (202827049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b360d25d0e207b0afc74cd93a7662c88e8399a9798db1e3baa5665c7aa6c157`  
		Last Modified: Wed, 02 Jul 2025 03:35:58 GMT  
		Size: 174.3 MB (174259463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88` - unknown; unknown

```console
$ docker pull rust@sha256:2f4addd958f6c23177ba57cb0b62703dba22d22d022fa5ff6111f60b883e3dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15905729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3c6db7f65484d03b4cc60245a2ead7632bf36cf44fdf76c3720b3831df124c`

```dockerfile
```

-	Layers:
	-	`sha256:ac641e00624bd7b454d162d456dcbebc72d34940b2f4aa530da90b3cbe71d493`  
		Last Modified: Wed, 02 Jul 2025 05:44:37 GMT  
		Size: 15.9 MB (15892438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1fa12a678c68a338b4e49d70c17dbded6143e0d3861664cbccf02c362f6879`  
		Last Modified: Wed, 02 Jul 2025 05:44:38 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88` - linux; 386

```console
$ docker pull rust@sha256:628fa076d84051d529c70e5978ae2488cc27c057e4378e6d6b4427cd1f48f5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (580031340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b007959168ba93c975145eae21e48f1112c685910223873e0805f91c16efcf81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99742b01aaf231df6992d8ecab593f6a7668b9047c6bb8cae0cc211c42b656d6`  
		Last Modified: Tue, 01 Jul 2025 05:11:03 GMT  
		Size: 210.3 MB (210310619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a36703fa30e50f1e2d2d9b8d6ee38f74b5c49158c0331edd0ac22489b68c9d`  
		Last Modified: Tue, 01 Jul 2025 08:59:26 GMT  
		Size: 229.2 MB (229161050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88` - unknown; unknown

```console
$ docker pull rust@sha256:60118c6a0bd04b58edbef1c693c60eef0a5c39a11250ffab32588f40429c495a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15853847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a0f3771a2d9e6d62cb0c6bcec0264fbabb8e5129657775262a756a4ab9cc9`

```dockerfile
```

-	Layers:
	-	`sha256:aede24ae4b2038e2305b863ac4a0808c493737d5ec9bc1219a2ffcdf76249352`  
		Last Modified: Tue, 01 Jul 2025 08:44:58 GMT  
		Size: 15.8 MB (15840760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adee46bd81fb5e17001fc933d0596dd15dc9c7296c5efe1c744ecb38885cff77`  
		Last Modified: Tue, 01 Jul 2025 08:44:59 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88` - linux; ppc64le

```console
$ docker pull rust@sha256:f4c7cad30a4575e18ae53f14b5bccb71451b44d720253a8f73f1cb12780bbf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635985035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442858853b317d76b745617081af4451d23840bd47301b0eabc620759c4b714`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7082fff0db11ec79e9a3c8fc9c05691e086d30ca51023010805fccbeac2b8dad`  
		Last Modified: Tue, 01 Jul 2025 05:07:55 GMT  
		Size: 25.7 MB (25663667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6cd79d875ce6ba17d2080d5bd4d0d55f7eec0f6bb923ae0b53e5bec14ef9b`  
		Last Modified: Tue, 01 Jul 2025 10:09:38 GMT  
		Size: 69.8 MB (69840014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575c9bdfba8d02bb3354a6a72904306bd1ae2c4432d14255385a153c75887837`  
		Last Modified: Tue, 01 Jul 2025 16:27:30 GMT  
		Size: 214.4 MB (214424908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078767722b4e04b7787f0ea5f95284ec4da0e1c5dc7804af4c26dc5181ec096c`  
		Last Modified: Wed, 02 Jul 2025 00:02:53 GMT  
		Size: 273.7 MB (273719203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88` - unknown; unknown

```console
$ docker pull rust@sha256:1a33a8b84d73eb3cf5fe4d5eb91a7212e3e015e40670b51ddebf3b52c4dbe0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee34f793447401153bab355f4bfbba25c4161b769172568c3b013931ffcfc953`

```dockerfile
```

-	Layers:
	-	`sha256:a169d322c59d3a0ddff0bf27d48dbe267dff9b48aaddd2ed30804cb885ff2527`  
		Last Modified: Tue, 01 Jul 2025 23:44:57 GMT  
		Size: 15.8 MB (15839092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d4887067e8590d2b12056401643ede686e2b3a83a2fccdfca0b762a5961e6a7`  
		Last Modified: Tue, 01 Jul 2025 23:44:58 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88` - linux; s390x

```console
$ docker pull rust@sha256:79ee189d40fd6c859e15a1e9c69b6da58d451b096e16a52dfec29b9bd0d76a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.5 MB (601452429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924b21bb8e92662795debcd307e3f3204964743780a9f028dfb3700b0ae8640b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1e32b479a11528098c70ba4af6292099abafcb29e0823d2861c86032c9b0b`  
		Last Modified: Tue, 01 Jul 2025 13:41:28 GMT  
		Size: 63.5 MB (63497964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2254c2dc3c53615f5f6a5adcfafb558670473622cb504cb0a6d02fd2b89d2667`  
		Last Modified: Tue, 01 Jul 2025 14:10:41 GMT  
		Size: 183.4 MB (183421934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c312814d252c566d3c3ee8f98763bedd5510a970a7460965bac0ea117ac8071c`  
		Last Modified: Tue, 01 Jul 2025 21:03:03 GMT  
		Size: 283.4 MB (283362703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88` - unknown; unknown

```console
$ docker pull rust@sha256:a4f9cf4a09562544ef011200268fb453c235bc5b972df93f32ca2dbf4ac1e349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15684597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afc1cf86bd3504dbe315e3c93562fc2ff8e92d15305627e7b38023518ec873b`

```dockerfile
```

-	Layers:
	-	`sha256:39dbb3c0f9a78d73aea412786fb8fabb2d333d5f18f4608bab4734aaa8e60fd7`  
		Last Modified: Tue, 01 Jul 2025 20:45:07 GMT  
		Size: 15.7 MB (15671458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d32a8a23e2b1c8cb3fdec2c521041d1a7fc5c908e5a6ce6bd3048f58dfefe8`  
		Last Modified: Tue, 01 Jul 2025 20:45:08 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88-alpine`

```console
$ docker pull rust@sha256:ec0413a092f4cc01b32e08f991485abe4467ef95c7416a6643a063a141c2e0ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.88-alpine` - linux; amd64

```console
$ docker pull rust@sha256:b18203be0f58e16fe47250bf98bbe83c61bbfa97a0f5a94cebf34605bb000137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324842014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccfa6e07df925301f1f0b76b6784e617369e209ccfd7b16e76a3f50bca1e544`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c179a1cc9cc1626cd02fbb4866ee1705894a35d0acf8458e7f0274620ded46`  
		Last Modified: Thu, 26 Jun 2025 19:02:56 GMT  
		Size: 61.6 MB (61613765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b44eb86436bd74e3289f02e42ae2c9df9c6a39ac3ff054f893f7cbaddbcf08b`  
		Last Modified: Thu, 26 Jun 2025 20:45:29 GMT  
		Size: 259.4 MB (259431403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:3a48955a20cd88465d43306589af8be8e9aab9bc4983ebf983267397b0038f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8794bb5882365fcd697f232d90c928f4dfc42f2d9dee1f418d14cba22fc740`

```dockerfile
```

-	Layers:
	-	`sha256:4af3880faef85aba29ec3559478d1219bcd27ba3aa3e498970fa8eb110c9fbbe`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d7d4050c4275c54863ef9a56b9e59d3e338bc902f05df72abcbf103b3bf06c`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:43c5afb577aa21180b984fe215c836db0e8da8c6d6e29f4f5d60fcac8f6747e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324286625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037fc7bdc081378f949b34f5b57abb98ba2f2308d8e24c81eec1dc00f8095344`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe32611e1706eb5e71110ea02f0a43bcf8d9d5b31375d8372476ca0151ea4e79`  
		Last Modified: Thu, 26 Jun 2025 19:09:40 GMT  
		Size: 59.2 MB (59154287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd9ba9c44d35a05a92f10caaf51df4bf98f7cd9e90070d71790f3fa3de848fa`  
		Last Modified: Thu, 26 Jun 2025 20:48:42 GMT  
		Size: 261.0 MB (260996397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:f7f6eaadbe7a000ba5420c2ea8c78d7812aea2e2ba405d6f47c7dcc77af1c77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fcba7c7ba45a16b412de43acab6b32790c948a2de7b038009b4fe3f5344978`

```dockerfile
```

-	Layers:
	-	`sha256:0ece12c371cca20fa75cd9470ad9eb8f90b1172dae46baaf4940565722fcf88e`  
		Last Modified: Thu, 26 Jun 2025 20:44:43 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49231f16442a61f2a0b6140092b2b40d1a3786b17de63fc044fabaa5fbcee312`  
		Last Modified: Thu, 26 Jun 2025 20:44:44 GMT  
		Size: 12.1 KB (12084 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88-alpine3.20`

```console
$ docker pull rust@sha256:3ab9b805c8d2444f6f63f1ae7a38b5e04949d6b0d9e8a314e1ee3ad502deae45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.88-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:985c5bffc08709b4c04506340fcdc2542dfd0604070a993c409a6565e200c488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318374251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4468520ebd63f0d5993bf50e71ce97ce1770aee2cf170f4b68416cbd826434`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd8e343fc1e8b59389632b1aa1fec9897eb0d70d9a028c4953824eaca48506`  
		Last Modified: Thu, 26 Jun 2025 19:02:57 GMT  
		Size: 55.3 MB (55315554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af473c39e92f0a526585dfa175d2324b3bcc5653f1f8b4a0197290536a1a4b82`  
		Last Modified: Thu, 26 Jun 2025 22:03:51 GMT  
		Size: 259.4 MB (259431800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:6d1398d665e6f2fad6e604e6b35246a23905cff0473753ad60eee908c8602f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.5 KB (722503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ed6595279fc3b8ec29033696b6a0ff4d9c437f59ceeaf9052d8a7b745cac53`

```dockerfile
```

-	Layers:
	-	`sha256:172a379c01373f9fa6f1f7546d8f14ca43f16dbed174f0fb1038d9ad729985b4`  
		Last Modified: Thu, 26 Jun 2025 20:44:46 GMT  
		Size: 711.8 KB (711789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c520dac29e5f70b8c11a8c70a95fc0a3a9bb4ca3b5499c004ab4cf05e37e7ce2`  
		Last Modified: Thu, 26 Jun 2025 20:44:46 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bbc890fbb4cfe63267e61b157106ae17e22fea8965bd86dad3ba2895731fd832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.0 MB (318036721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2562e20c93fbfe25e95e223728ea45fdabb24f56872078249b32a94618aef470`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f73dbcfd8a123487699fe68590b2bd9f99926de28d20db07b032c7c04a77d5b`  
		Last Modified: Thu, 26 Jun 2025 19:07:09 GMT  
		Size: 53.0 MB (52950135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35f71611cb454ac5691276f7fb4f820ad5cca79bd33a16a47b3383d0199fd5d`  
		Last Modified: Thu, 26 Jun 2025 22:04:01 GMT  
		Size: 261.0 MB (260995421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:ffe59248eec0f167209f1689d76dc0cf65197edb7123968bab9d9736ed5dbe1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bf25ee4d7342c1573d066bf9d6490bc899c772b46d58fb99616651dff2a12a`

```dockerfile
```

-	Layers:
	-	`sha256:fb91044d3c55c5b9a10f560693a397817a79b1c3e9cac98794b2cc2378ddf88f`  
		Last Modified: Thu, 26 Jun 2025 20:44:50 GMT  
		Size: 747.7 KB (747721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619847fa4854614400d1faefbfd3dca469c0ddb922f14d8b21e0cfee7113e7b2`  
		Last Modified: Thu, 26 Jun 2025 20:44:51 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88-alpine3.21`

```console
$ docker pull rust@sha256:9c6a4baf58661f99a5441b15e3ad8295dabf35e849c4935e77ad35d9809be1d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.88-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:f76a41f6a9d96aca247c6789369bb5986c9faaef5d0ab080ae28346725d86c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324637733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd470e8018c4c8d13c36bb6d82b21b2b35e0cab903eaabfd2ba2cdbc0d49d8c9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a9008c78a14e56fc9106b9415625622b22d3e7d7ed88d4c9f168084a5b930a`  
		Last Modified: Thu, 26 Jun 2025 19:02:57 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99aa10cef404820ac909a9c36a9398af421599896d89f5216fe03a0484938cbc`  
		Last Modified: Thu, 26 Jun 2025 20:47:21 GMT  
		Size: 259.4 MB (259430674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:bfe3ce46af8506744eb91a950436d78f9b57aa1c89dab3f0c8cf5796a6964767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063fdf51672810ea7124832520f622f7d4a1bd29ff180e4e39b155177f6ce538`

```dockerfile
```

-	Layers:
	-	`sha256:bd239d1a7ba898b4e5db9276ef7089d6bd3dc5fbc114c96a656434c2b620e7a4`  
		Last Modified: Thu, 26 Jun 2025 20:44:52 GMT  
		Size: 782.6 KB (782619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68bd06a7d86815924cf9c1da819c34ded738a4b417cf24f9b33b853d7a3d1bb2`  
		Last Modified: Thu, 26 Jun 2025 20:44:53 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:390d7bebae8a355bd9e439bffd1f0f0124d0ade0a01602308b3c663490f66a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.1 MB (324089393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c931f5d71d48f4c73a17c302da0df6ebc23b15ced06b4f4ab775f1ec6e5228`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa43a6919f3e4298c4ac7012f740c568baceb922776f8df0f76856cc3ee4662`  
		Last Modified: Thu, 26 Jun 2025 19:08:40 GMT  
		Size: 59.1 MB (59101301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aad9f05f3e21035ae8f9c44b60e6bd73096afc6f6fa0e572587f6b65e6ece8`  
		Last Modified: Thu, 26 Jun 2025 20:47:22 GMT  
		Size: 261.0 MB (260995063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:03bf0509d1cc316b17044231bd28292d0828891ee21cde73471813fed5ee7435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (872990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eaca6f25dcca1d3f5272d1eef631f701b29c34b87f57293ddd1769d867a156`

```dockerfile
```

-	Layers:
	-	`sha256:263657c33753a7119953e3eaf32bfa7eb0f92250b29093be5e85cee6402a4952`  
		Last Modified: Thu, 26 Jun 2025 20:44:57 GMT  
		Size: 862.2 KB (862157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7daa109bbb3d9da7db18c495a2c43ac74998f6a27162c51bbc993b97bf68fa0`  
		Last Modified: Thu, 26 Jun 2025 20:44:57 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88-alpine3.22`

```console
$ docker pull rust@sha256:ec0413a092f4cc01b32e08f991485abe4467ef95c7416a6643a063a141c2e0ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.88-alpine3.22` - linux; amd64

```console
$ docker pull rust@sha256:b18203be0f58e16fe47250bf98bbe83c61bbfa97a0f5a94cebf34605bb000137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324842014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccfa6e07df925301f1f0b76b6784e617369e209ccfd7b16e76a3f50bca1e544`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c179a1cc9cc1626cd02fbb4866ee1705894a35d0acf8458e7f0274620ded46`  
		Last Modified: Thu, 26 Jun 2025 19:02:56 GMT  
		Size: 61.6 MB (61613765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b44eb86436bd74e3289f02e42ae2c9df9c6a39ac3ff054f893f7cbaddbcf08b`  
		Last Modified: Thu, 26 Jun 2025 20:45:29 GMT  
		Size: 259.4 MB (259431403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:3a48955a20cd88465d43306589af8be8e9aab9bc4983ebf983267397b0038f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8794bb5882365fcd697f232d90c928f4dfc42f2d9dee1f418d14cba22fc740`

```dockerfile
```

-	Layers:
	-	`sha256:4af3880faef85aba29ec3559478d1219bcd27ba3aa3e498970fa8eb110c9fbbe`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d7d4050c4275c54863ef9a56b9e59d3e338bc902f05df72abcbf103b3bf06c`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:43c5afb577aa21180b984fe215c836db0e8da8c6d6e29f4f5d60fcac8f6747e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324286625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037fc7bdc081378f949b34f5b57abb98ba2f2308d8e24c81eec1dc00f8095344`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe32611e1706eb5e71110ea02f0a43bcf8d9d5b31375d8372476ca0151ea4e79`  
		Last Modified: Thu, 26 Jun 2025 19:09:40 GMT  
		Size: 59.2 MB (59154287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd9ba9c44d35a05a92f10caaf51df4bf98f7cd9e90070d71790f3fa3de848fa`  
		Last Modified: Thu, 26 Jun 2025 20:48:42 GMT  
		Size: 261.0 MB (260996397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:f7f6eaadbe7a000ba5420c2ea8c78d7812aea2e2ba405d6f47c7dcc77af1c77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fcba7c7ba45a16b412de43acab6b32790c948a2de7b038009b4fe3f5344978`

```dockerfile
```

-	Layers:
	-	`sha256:0ece12c371cca20fa75cd9470ad9eb8f90b1172dae46baaf4940565722fcf88e`  
		Last Modified: Thu, 26 Jun 2025 20:44:43 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49231f16442a61f2a0b6140092b2b40d1a3786b17de63fc044fabaa5fbcee312`  
		Last Modified: Thu, 26 Jun 2025 20:44:44 GMT  
		Size: 12.1 KB (12084 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88-bookworm`

```console
$ docker pull rust@sha256:5771a3cc2081935c59ac52b92d49c9e164d4fed92c9f6420aa8cc50364aead6e
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

### `rust:1.88-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:95f6d6956bf8abd7461763ba7ccd243d8964a41c8eb3f41d895490c782628d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553347880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a479811b82446e6bf598238bb2fcd3ae41b351a1a7c87e53d8f2333a7bbe001d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe9c1abe6f3b8ca9fc6abe710405f830f95262f1d356e8f6545d823b5840a5c`  
		Last Modified: Tue, 01 Jul 2025 05:12:07 GMT  
		Size: 211.4 MB (211373500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0545d5f3de1a8249849f4342031613d732af87e31f13755f5fac287119ed13e8`  
		Last Modified: Tue, 01 Jul 2025 06:18:35 GMT  
		Size: 205.1 MB (205059525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0e0dc34caec6b81f1b5ab4c9a559c11b4d7440382c69d8a2cdbe5002a71523e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15877001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81308c8e2c35f38fbef285c685f2ca642508d83efc22df71984838afd98ac55d`

```dockerfile
```

-	Layers:
	-	`sha256:3260e53bff48cf37775cac874c3e2920680f90a7669e12d2c322771f16c50614`  
		Last Modified: Tue, 01 Jul 2025 08:44:24 GMT  
		Size: 15.9 MB (15863862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a629d4f8f234144e7bda08172e21d63709f916bfe46836348a616c43d2cdd880`  
		Last Modified: Tue, 01 Jul 2025 08:44:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:b12fb2b0506d2b8fde83230531af65c46d2e1cb65c7b965a23de3015d7feff05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546880259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe31256245950fcf402e7f41d298a8bd3859cf9558a2e1ff584d64071362bda1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc606b1195a348c6a47399c1a54ab936d4477a526d62306ddce89fe76a2d22`  
		Last Modified: Tue, 01 Jul 2025 08:59:56 GMT  
		Size: 21.9 MB (21928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f4c85f426e2c955b1dac4fa88bc182d725644c23ad01bdcbf64d9664e34a8`  
		Last Modified: Tue, 01 Jul 2025 18:28:59 GMT  
		Size: 59.7 MB (59656492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda2264dd6dda88971c220cda9283a6c337d04aeb92012d9d160887d4ec0b556`  
		Last Modified: Wed, 02 Jul 2025 00:17:51 GMT  
		Size: 175.3 MB (175294922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5ff6581ced6c9c0cc98e703fa5901cda1814bee9d3ac91337dfcb2eeaa3fa`  
		Last Modified: Wed, 02 Jul 2025 12:16:49 GMT  
		Size: 245.8 MB (245792330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a6b6613abe69a8ea05c159027354fad9e25a0f58f5a61a4c761bd608e9118f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15679627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0222859d21f0de033a308a561262ae0c61dc1ab6441395c68809f9d9455913d`

```dockerfile
```

-	Layers:
	-	`sha256:d6bf21d47ea4882f2e19fc8c2018d3473ff3633b948a8a2912ffa2fb5dc5c75c`  
		Last Modified: Wed, 02 Jul 2025 11:44:31 GMT  
		Size: 15.7 MB (15666380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f88163f4b88d616cf50cd1d0bb3bb47eda6485492c98f7f4bc8035c0d832d762`  
		Last Modified: Wed, 02 Jul 2025 11:44:32 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:66b553fe51fe4eba929ee31c39d66506fe41b72cf403dab3117de2bd5d43e645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513346599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5424600217354e80a3f0ab99133ec64aa48f464a2f1c29a93cbd0f95758e5af7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a65abb6272f500a9ae5d14c9ae8ef9cb0e4009b02acfccb4dabc478f252d44`  
		Last Modified: Tue, 01 Jul 2025 19:38:43 GMT  
		Size: 202.8 MB (202827049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b360d25d0e207b0afc74cd93a7662c88e8399a9798db1e3baa5665c7aa6c157`  
		Last Modified: Wed, 02 Jul 2025 03:35:58 GMT  
		Size: 174.3 MB (174259463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2f4addd958f6c23177ba57cb0b62703dba22d22d022fa5ff6111f60b883e3dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15905729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3c6db7f65484d03b4cc60245a2ead7632bf36cf44fdf76c3720b3831df124c`

```dockerfile
```

-	Layers:
	-	`sha256:ac641e00624bd7b454d162d456dcbebc72d34940b2f4aa530da90b3cbe71d493`  
		Last Modified: Wed, 02 Jul 2025 05:44:37 GMT  
		Size: 15.9 MB (15892438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1fa12a678c68a338b4e49d70c17dbded6143e0d3861664cbccf02c362f6879`  
		Last Modified: Wed, 02 Jul 2025 05:44:38 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-bookworm` - linux; 386

```console
$ docker pull rust@sha256:628fa076d84051d529c70e5978ae2488cc27c057e4378e6d6b4427cd1f48f5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (580031340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b007959168ba93c975145eae21e48f1112c685910223873e0805f91c16efcf81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99742b01aaf231df6992d8ecab593f6a7668b9047c6bb8cae0cc211c42b656d6`  
		Last Modified: Tue, 01 Jul 2025 05:11:03 GMT  
		Size: 210.3 MB (210310619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a36703fa30e50f1e2d2d9b8d6ee38f74b5c49158c0331edd0ac22489b68c9d`  
		Last Modified: Tue, 01 Jul 2025 08:59:26 GMT  
		Size: 229.2 MB (229161050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:60118c6a0bd04b58edbef1c693c60eef0a5c39a11250ffab32588f40429c495a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15853847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a0f3771a2d9e6d62cb0c6bcec0264fbabb8e5129657775262a756a4ab9cc9`

```dockerfile
```

-	Layers:
	-	`sha256:aede24ae4b2038e2305b863ac4a0808c493737d5ec9bc1219a2ffcdf76249352`  
		Last Modified: Tue, 01 Jul 2025 08:44:58 GMT  
		Size: 15.8 MB (15840760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adee46bd81fb5e17001fc933d0596dd15dc9c7296c5efe1c744ecb38885cff77`  
		Last Modified: Tue, 01 Jul 2025 08:44:59 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:f4c7cad30a4575e18ae53f14b5bccb71451b44d720253a8f73f1cb12780bbf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635985035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442858853b317d76b745617081af4451d23840bd47301b0eabc620759c4b714`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7082fff0db11ec79e9a3c8fc9c05691e086d30ca51023010805fccbeac2b8dad`  
		Last Modified: Tue, 01 Jul 2025 05:07:55 GMT  
		Size: 25.7 MB (25663667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6cd79d875ce6ba17d2080d5bd4d0d55f7eec0f6bb923ae0b53e5bec14ef9b`  
		Last Modified: Tue, 01 Jul 2025 10:09:38 GMT  
		Size: 69.8 MB (69840014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575c9bdfba8d02bb3354a6a72904306bd1ae2c4432d14255385a153c75887837`  
		Last Modified: Tue, 01 Jul 2025 16:27:30 GMT  
		Size: 214.4 MB (214424908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078767722b4e04b7787f0ea5f95284ec4da0e1c5dc7804af4c26dc5181ec096c`  
		Last Modified: Wed, 02 Jul 2025 00:02:53 GMT  
		Size: 273.7 MB (273719203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1a33a8b84d73eb3cf5fe4d5eb91a7212e3e015e40670b51ddebf3b52c4dbe0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee34f793447401153bab355f4bfbba25c4161b769172568c3b013931ffcfc953`

```dockerfile
```

-	Layers:
	-	`sha256:a169d322c59d3a0ddff0bf27d48dbe267dff9b48aaddd2ed30804cb885ff2527`  
		Last Modified: Tue, 01 Jul 2025 23:44:57 GMT  
		Size: 15.8 MB (15839092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d4887067e8590d2b12056401643ede686e2b3a83a2fccdfca0b762a5961e6a7`  
		Last Modified: Tue, 01 Jul 2025 23:44:58 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:79ee189d40fd6c859e15a1e9c69b6da58d451b096e16a52dfec29b9bd0d76a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.5 MB (601452429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924b21bb8e92662795debcd307e3f3204964743780a9f028dfb3700b0ae8640b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1e32b479a11528098c70ba4af6292099abafcb29e0823d2861c86032c9b0b`  
		Last Modified: Tue, 01 Jul 2025 13:41:28 GMT  
		Size: 63.5 MB (63497964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2254c2dc3c53615f5f6a5adcfafb558670473622cb504cb0a6d02fd2b89d2667`  
		Last Modified: Tue, 01 Jul 2025 14:10:41 GMT  
		Size: 183.4 MB (183421934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c312814d252c566d3c3ee8f98763bedd5510a970a7460965bac0ea117ac8071c`  
		Last Modified: Tue, 01 Jul 2025 21:03:03 GMT  
		Size: 283.4 MB (283362703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a4f9cf4a09562544ef011200268fb453c235bc5b972df93f32ca2dbf4ac1e349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15684597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afc1cf86bd3504dbe315e3c93562fc2ff8e92d15305627e7b38023518ec873b`

```dockerfile
```

-	Layers:
	-	`sha256:39dbb3c0f9a78d73aea412786fb8fabb2d333d5f18f4608bab4734aaa8e60fd7`  
		Last Modified: Tue, 01 Jul 2025 20:45:07 GMT  
		Size: 15.7 MB (15671458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d32a8a23e2b1c8cb3fdec2c521041d1a7fc5c908e5a6ce6bd3048f58dfefe8`  
		Last Modified: Tue, 01 Jul 2025 20:45:08 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88-bullseye`

```console
$ docker pull rust@sha256:8eb96c7c77c04660a95d5e256869de0a18130f97624ef75c522ea886d4e51d95
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

### `rust:1.88-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:4fe592966775f3396e3d099d674f0664e4383336371ca5600e40c2fe3b575383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526479452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e24231a2d9ba56b24304902b7106252b1ba5aa98dc98b58ac09df699a11813e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06772a4eff3df697497bb68b4dcdeb97fdb9338b5e7dde7d1a53579c3203c9ba`  
		Last Modified: Tue, 01 Jul 2025 03:20:06 GMT  
		Size: 54.8 MB (54757481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd49c17bd36c59d7bf7afe446ee52f36cad8a6393628526989f2db44b4486c1`  
		Last Modified: Tue, 01 Jul 2025 05:11:29 GMT  
		Size: 197.1 MB (197142751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b35768b15c47fe75ef345baf1601f003231cf7fa1353d4b05177acb4b38d712`  
		Last Modified: Tue, 01 Jul 2025 06:44:33 GMT  
		Size: 205.1 MB (205059062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f26b96d6cf3fe96312784ed4c21daceefd839ea7ec263a286a9c464c17889bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15475219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4229b2d8712383288725ba877fc8da75d82f25002251269162108f995d12061e`

```dockerfile
```

-	Layers:
	-	`sha256:2186b18143b7f42f67f19ba8594c9c55a420158d4af543684506320400941527`  
		Last Modified: Tue, 01 Jul 2025 08:44:36 GMT  
		Size: 15.5 MB (15463971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c86f9b373cccbb5f795ae509ad60503878f0f8e5a247421fd1a6f1461968cb`  
		Last Modified: Tue, 01 Jul 2025 08:44:37 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:d9735061f6bd324ad5d9a6b1f353e919d01b9515946a2de100568511a1182afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.9 MB (527938900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c390dbe5f1131b80bb7b105624994b79e2115d8dec0bcace50edd510c2198b13`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:efcf40eae0046ccd92d3b47ff685e1e9cf7a34d0a92f6de893078f115e01f20f`  
		Last Modified: Tue, 01 Jul 2025 01:15:14 GMT  
		Size: 49.0 MB (49043960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6769ed354ec7fde57e63bdf9788543b96fd8f93923607ad70767b9c4cfa25b`  
		Last Modified: Tue, 01 Jul 2025 08:59:49 GMT  
		Size: 14.9 MB (14880774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28365fa3b8363bfd29e20b4b17838c65ddc4bdacb1bf15ca9af5a4045e4feaf7`  
		Last Modified: Tue, 01 Jul 2025 18:29:48 GMT  
		Size: 50.6 MB (50631320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31eafcbc0a8afc051ea3519738dd6b4e501ce5f603e4a10bdf1f0f6720a29f58`  
		Last Modified: Wed, 02 Jul 2025 00:17:56 GMT  
		Size: 167.6 MB (167589980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d954ab622638b81a76f8faca7f27cdbead519ce4a96bfe58ce0ce8c04de4c07c`  
		Last Modified: Wed, 02 Jul 2025 12:59:39 GMT  
		Size: 245.8 MB (245792866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:533dd51110aa122013299169d3241c8ff7b0a167ac026488a451cc3cf5a32242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15274640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43196c04d844d43946f4c7a75dd78f798c69fa8488debfc89ba320795b1e927b`

```dockerfile
```

-	Layers:
	-	`sha256:652198c66ccabc1746f6054da6a0b040aa11e579f227a638a7db763062f6b11e`  
		Last Modified: Wed, 02 Jul 2025 11:44:40 GMT  
		Size: 15.3 MB (15263315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9c99c87037228c8be536fc6fd298ab2a611a1fbd6a3d52d733fb4a29c90c2d`  
		Last Modified: Wed, 02 Jul 2025 11:44:41 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8b22455a7ce2adb1355067638284ee99d21cc516fab63a96c4514beaf370aa94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.2 MB (487172791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc77b2b3e794e11c9031f129feea6f9dd3649f86a9b70ad373910e70e5761458`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5424250d141bf5f4ec62e698bba9b5695482a3015186d3b14a633da8916bf7dd`  
		Last Modified: Tue, 01 Jul 2025 06:52:24 GMT  
		Size: 15.8 MB (15750716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7766ba090abb327ecb7e9e14ac90bbcc45c5ba6bb8a568ae531c960ff1acad55`  
		Last Modified: Tue, 01 Jul 2025 13:29:45 GMT  
		Size: 54.9 MB (54855722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1801db58ebce0297c6d03187f6e882ae0b8ba8838f3e18a17f3bcd9137be277`  
		Last Modified: Tue, 01 Jul 2025 20:13:40 GMT  
		Size: 190.1 MB (190053793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714498f74a0f367b5e69c9e7e3bd688c25db146ed8b97acec1446cb2218e705`  
		Last Modified: Wed, 02 Jul 2025 06:40:03 GMT  
		Size: 174.3 MB (174260306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e2730dd90c1b51e30c613c774511479688800225d93c02bdaf36189e99891fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15477294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b9b0c706b4ad223660013177c4a118765a26d87add26bb8babfbdf979efb1d`

```dockerfile
```

-	Layers:
	-	`sha256:12453b011a0f7bb3aac0c83948f50551f0d4d5ae1b1e0c7c3a472d44e1f5c7da`  
		Last Modified: Wed, 02 Jul 2025 05:44:46 GMT  
		Size: 15.5 MB (15465942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccba5cc2249b25264628303f496f30cecf3ead2e13e1dc3399d7f98b1951ce12`  
		Last Modified: Wed, 02 Jul 2025 05:44:46 GMT  
		Size: 11.4 KB (11352 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-bullseye` - linux; 386

```console
$ docker pull rust@sha256:2aaf00b554cd4ff148c16a3e58146641b87aa7c629bbb67c6731554afa3c2d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 MB (556215637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab21c61c4d19a041fcae82560e48bb7233059e80ef65189d4d830b0493e23dbc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113be81052ec8e8323c4db158dc9c99295355934e950a6367e5c27038fd1e04c`  
		Last Modified: Tue, 01 Jul 2025 02:24:43 GMT  
		Size: 16.3 MB (16268907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05b439f6df174e28bd21dc59eead603def3bcbd47ec6462f86b7758c4db6ef`  
		Last Modified: Tue, 01 Jul 2025 03:19:57 GMT  
		Size: 56.0 MB (56049937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d170ad31938c07c5739c923eaf5f7569c644e2ea2ead929bbc107d7eac895f78`  
		Last Modified: Tue, 01 Jul 2025 05:11:30 GMT  
		Size: 200.0 MB (200043566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7271fc5f55db8e0b012c06b0785adf36c8ade5d9f290c40fa07be956a5eecde`  
		Last Modified: Tue, 01 Jul 2025 13:00:23 GMT  
		Size: 229.2 MB (229163293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3cb1daa21e1c22f0ea3d5100504d1da2f45a788bcf4f0c42396ea073969b5df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd9075c8dc525761d3e7cf32a7d172eaaee78ecc359ee8f83da3b6bf52859ef`

```dockerfile
```

-	Layers:
	-	`sha256:4ba2cd6c29aab7b896485ed38a1fc73dd8448a29ef9bf4744495334a3e930f89`  
		Last Modified: Tue, 01 Jul 2025 08:45:13 GMT  
		Size: 15.5 MB (15450673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8861a1fd041f7cf768c0ad3c6f4dc87d554c6bcb084c979d61f7a6af8ff9a715`  
		Last Modified: Tue, 01 Jul 2025 08:45:13 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88-slim`

```console
$ docker pull rust@sha256:1c7eb658b16d48458a4808f15de8264a3c20d449d0cabdae47654d98e9dcecfb
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

### `rust:1.88-slim` - linux; amd64

```console
$ docker pull rust@sha256:b0c0357c60eca8fe29b8280974a44483a28319278a5ff5c57b3e7e9c5708f643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbda49f92a1f159dfbe623e790c2a5b9c1c6c3ba68bd9e362679a9cb48c4925e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff2b7b26c381c0c4ba90768f39bf5193252f27f4e625debf008d09438b195ef`  
		Last Modified: Tue, 01 Jul 2025 05:08:00 GMT  
		Size: 275.8 MB (275821106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim` - unknown; unknown

```console
$ docker pull rust@sha256:ade5b81bacfe5c6c7e52b85eafa1965c8ff433a6b2c5dbe95ffdac9b636a4098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a4805359ec86648c4fa15446b7df199cdb6a6e1a03490dcb11b527cd557473`

```dockerfile
```

-	Layers:
	-	`sha256:7df8be7b6f1e71053bb68baafbd18a0da5e3196678a329e5267ab3a5a709ffd6`  
		Last Modified: Tue, 01 Jul 2025 05:44:31 GMT  
		Size: 4.1 MB (4094552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a712f57ad2be1eb1eb0de48182654c5bcff269ed26b9ac1f7e737790730b63d`  
		Last Modified: Tue, 01 Jul 2025 05:44:32 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:85f37f11d046da1808026326b03493679b5d14c2f0f4523cf5bc8d5cc0e0ee0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317565661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7f9b3c433121c615480c6153d82080be95a30629221317a4cea09c08b0a573`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4db19ae3ab5266032020a2b07eb5414e4e5af2ea274e14d76e0e545b488f04d`  
		Last Modified: Tue, 01 Jul 2025 21:04:24 GMT  
		Size: 293.6 MB (293626917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim` - unknown; unknown

```console
$ docker pull rust@sha256:f5c7c3079e6be98cf7906e069b6a07af60bc9f5410e2deba15738732d1776661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b45c40a162ec803cc4480e1a932c1658154fae9d07c32b6cd1ff7053f34a7f7`

```dockerfile
```

-	Layers:
	-	`sha256:c7b3d0ac3ecfb43b93f6888077022d4165a1bd97012372bb37d32a5e2e76ccde`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 3.9 MB (3908981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd6ab2ec5e6066af386464396673a5d060f5b1a51cf8099cafde5bf8cb46451`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:35d3b11bbc6b7f45a174551689621906e5785d4e6e79f2aa3b4ace967a97a055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268179917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1880617faa9ea5bc0df720923e7d75c521d91fc7a3583e3360d6068d359c2b84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e130c413bba66f1a532f016096e1ca99fc7921a6d03f4ae5e7eef4f9de7197`  
		Last Modified: Tue, 01 Jul 2025 14:52:04 GMT  
		Size: 240.1 MB (240102239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b42e61db7f4c7471a71877c4a53f4d0391e7954c21dc20f7a3973cec0a2e7057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd222f432ceb8c15e86b58486cf5fd9c4582036ac9dcb8cede1be44821594ae1`

```dockerfile
```

-	Layers:
	-	`sha256:4c92de7432ff997c7c9d6fd67c06d2e50d70c9800c27e05fa0d04b2dcc4d42dd`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 4.1 MB (4116896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d1589208f0a8f59560905b8c36a4c4ecf08601526c55cbaaabc4a10846fb78`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim` - linux; 386

```console
$ docker pull rust@sha256:ff6fcb7ad6293f4a4c28db122754d93e024b99ca56a9f5027ddced08234ef721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325992228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4eb540ded896f027e6b1931f38d7618a4364b4643343cf6a82ef2de0e775e79`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3f2ceb310dae022b26d227eecca523fe07e1383bbc8cf746de0a949d9a3650`  
		Last Modified: Tue, 01 Jul 2025 06:01:36 GMT  
		Size: 296.8 MB (296779796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim` - unknown; unknown

```console
$ docker pull rust@sha256:310296d66708c74b8f7df786253dabb1763763f3ae996499d228c97b5defc6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad4a9c0226f971d47fbf4e1e3b0972b7052bb0257233fab74bc5c4b8783fb1e`

```dockerfile
```

-	Layers:
	-	`sha256:2a6a2a00284fbce671a5f0f7c61ebfbf8c2d5771cda8a1bd5445be27b699d096`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 4.1 MB (4073915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d875623e01bac8366b22e9a8bf9378721a880661602db1d20b97da37bd0c7c2a`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:e00cab06ebef6d7bb5580cedac63b15bf337fd68225ac6a152bdeb1d08bca552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374561374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8452adee592dd5981efa36540ccd9dd66cc2273fd2272ece300389cc198997a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a95af4d06128b392493eba88f8150c9e90691be1c0f0e8024d5929b44de3930`  
		Last Modified: Tue, 01 Jul 2025 13:00:07 GMT  
		Size: 342.5 MB (342488554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim` - unknown; unknown

```console
$ docker pull rust@sha256:ad4355591f63f7acdbf5366f8fb6d2241920c664d093c0327bd30a320b228ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687a2175e85119fb64fa7d37bd7720459fed5f9513594f53bbddccbef9cbce8d`

```dockerfile
```

-	Layers:
	-	`sha256:b40dd3069d53ab3fd2d2a8604ee2b563e69d54a6f2f4e29cd2f5cb441d80ae60`  
		Last Modified: Tue, 01 Jul 2025 11:44:38 GMT  
		Size: 4.1 MB (4066865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44f89002a1ae239b997acfc875a4c4a4fc8423278688b1ec444ca96cf66b74f`  
		Last Modified: Tue, 01 Jul 2025 11:44:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim` - linux; s390x

```console
$ docker pull rust@sha256:1cf72ceabd44d186a6f08948bad51ee0050ed17cb47657c6b74e1e879451a34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360392180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871910d1ab2a752b966ffce7ec56ab4866c791bce0f9fc075cb26d7744e75884`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8a3025335a2a160722cb689b6c389f0316ea4b027c2dad34fef52df858c365`  
		Last Modified: Tue, 01 Jul 2025 10:42:01 GMT  
		Size: 333.5 MB (333504369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim` - unknown; unknown

```console
$ docker pull rust@sha256:d04b9fa09c2d16e830240aaa30f0b46002ffc117461d7109c104bd5c6732a461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6791cd1d0129cc03fe2cbcb7c2269397f8348bb85df5bd5b9a8e6575a8923e`

```dockerfile
```

-	Layers:
	-	`sha256:2a8e89592d0564890623c9199bb211483a145b510ce0c49afc579dabe00180f9`  
		Last Modified: Tue, 01 Jul 2025 08:44:56 GMT  
		Size: 3.9 MB (3932230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52770394e7f7570572f6a897500a0bc0f14d82302ff5f32b5db7076d7a67ab3a`  
		Last Modified: Tue, 01 Jul 2025 08:44:57 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88-slim-bookworm`

```console
$ docker pull rust@sha256:1c7eb658b16d48458a4808f15de8264a3c20d449d0cabdae47654d98e9dcecfb
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

### `rust:1.88-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:b0c0357c60eca8fe29b8280974a44483a28319278a5ff5c57b3e7e9c5708f643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbda49f92a1f159dfbe623e790c2a5b9c1c6c3ba68bd9e362679a9cb48c4925e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff2b7b26c381c0c4ba90768f39bf5193252f27f4e625debf008d09438b195ef`  
		Last Modified: Tue, 01 Jul 2025 05:08:00 GMT  
		Size: 275.8 MB (275821106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ade5b81bacfe5c6c7e52b85eafa1965c8ff433a6b2c5dbe95ffdac9b636a4098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a4805359ec86648c4fa15446b7df199cdb6a6e1a03490dcb11b527cd557473`

```dockerfile
```

-	Layers:
	-	`sha256:7df8be7b6f1e71053bb68baafbd18a0da5e3196678a329e5267ab3a5a709ffd6`  
		Last Modified: Tue, 01 Jul 2025 05:44:31 GMT  
		Size: 4.1 MB (4094552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a712f57ad2be1eb1eb0de48182654c5bcff269ed26b9ac1f7e737790730b63d`  
		Last Modified: Tue, 01 Jul 2025 05:44:32 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:85f37f11d046da1808026326b03493679b5d14c2f0f4523cf5bc8d5cc0e0ee0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317565661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7f9b3c433121c615480c6153d82080be95a30629221317a4cea09c08b0a573`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4db19ae3ab5266032020a2b07eb5414e4e5af2ea274e14d76e0e545b488f04d`  
		Last Modified: Tue, 01 Jul 2025 21:04:24 GMT  
		Size: 293.6 MB (293626917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f5c7c3079e6be98cf7906e069b6a07af60bc9f5410e2deba15738732d1776661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b45c40a162ec803cc4480e1a932c1658154fae9d07c32b6cd1ff7053f34a7f7`

```dockerfile
```

-	Layers:
	-	`sha256:c7b3d0ac3ecfb43b93f6888077022d4165a1bd97012372bb37d32a5e2e76ccde`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 3.9 MB (3908981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd6ab2ec5e6066af386464396673a5d060f5b1a51cf8099cafde5bf8cb46451`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:35d3b11bbc6b7f45a174551689621906e5785d4e6e79f2aa3b4ace967a97a055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268179917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1880617faa9ea5bc0df720923e7d75c521d91fc7a3583e3360d6068d359c2b84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e130c413bba66f1a532f016096e1ca99fc7921a6d03f4ae5e7eef4f9de7197`  
		Last Modified: Tue, 01 Jul 2025 14:52:04 GMT  
		Size: 240.1 MB (240102239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b42e61db7f4c7471a71877c4a53f4d0391e7954c21dc20f7a3973cec0a2e7057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd222f432ceb8c15e86b58486cf5fd9c4582036ac9dcb8cede1be44821594ae1`

```dockerfile
```

-	Layers:
	-	`sha256:4c92de7432ff997c7c9d6fd67c06d2e50d70c9800c27e05fa0d04b2dcc4d42dd`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 4.1 MB (4116896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d1589208f0a8f59560905b8c36a4c4ecf08601526c55cbaaabc4a10846fb78`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:ff6fcb7ad6293f4a4c28db122754d93e024b99ca56a9f5027ddced08234ef721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325992228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4eb540ded896f027e6b1931f38d7618a4364b4643343cf6a82ef2de0e775e79`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3f2ceb310dae022b26d227eecca523fe07e1383bbc8cf746de0a949d9a3650`  
		Last Modified: Tue, 01 Jul 2025 06:01:36 GMT  
		Size: 296.8 MB (296779796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:310296d66708c74b8f7df786253dabb1763763f3ae996499d228c97b5defc6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad4a9c0226f971d47fbf4e1e3b0972b7052bb0257233fab74bc5c4b8783fb1e`

```dockerfile
```

-	Layers:
	-	`sha256:2a6a2a00284fbce671a5f0f7c61ebfbf8c2d5771cda8a1bd5445be27b699d096`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 4.1 MB (4073915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d875623e01bac8366b22e9a8bf9378721a880661602db1d20b97da37bd0c7c2a`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:e00cab06ebef6d7bb5580cedac63b15bf337fd68225ac6a152bdeb1d08bca552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374561374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8452adee592dd5981efa36540ccd9dd66cc2273fd2272ece300389cc198997a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a95af4d06128b392493eba88f8150c9e90691be1c0f0e8024d5929b44de3930`  
		Last Modified: Tue, 01 Jul 2025 13:00:07 GMT  
		Size: 342.5 MB (342488554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ad4355591f63f7acdbf5366f8fb6d2241920c664d093c0327bd30a320b228ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687a2175e85119fb64fa7d37bd7720459fed5f9513594f53bbddccbef9cbce8d`

```dockerfile
```

-	Layers:
	-	`sha256:b40dd3069d53ab3fd2d2a8604ee2b563e69d54a6f2f4e29cd2f5cb441d80ae60`  
		Last Modified: Tue, 01 Jul 2025 11:44:38 GMT  
		Size: 4.1 MB (4066865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44f89002a1ae239b997acfc875a4c4a4fc8423278688b1ec444ca96cf66b74f`  
		Last Modified: Tue, 01 Jul 2025 11:44:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:1cf72ceabd44d186a6f08948bad51ee0050ed17cb47657c6b74e1e879451a34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360392180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871910d1ab2a752b966ffce7ec56ab4866c791bce0f9fc075cb26d7744e75884`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8a3025335a2a160722cb689b6c389f0316ea4b027c2dad34fef52df858c365`  
		Last Modified: Tue, 01 Jul 2025 10:42:01 GMT  
		Size: 333.5 MB (333504369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d04b9fa09c2d16e830240aaa30f0b46002ffc117461d7109c104bd5c6732a461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6791cd1d0129cc03fe2cbcb7c2269397f8348bb85df5bd5b9a8e6575a8923e`

```dockerfile
```

-	Layers:
	-	`sha256:2a8e89592d0564890623c9199bb211483a145b510ce0c49afc579dabe00180f9`  
		Last Modified: Tue, 01 Jul 2025 08:44:56 GMT  
		Size: 3.9 MB (3932230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52770394e7f7570572f6a897500a0bc0f14d82302ff5f32b5db7076d7a67ab3a`  
		Last Modified: Tue, 01 Jul 2025 08:44:57 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88-slim-bullseye`

```console
$ docker pull rust@sha256:12d9a0ff4f3c87badbf56a27ffd6c4774ebe1b5fe5c6b7b1a39cfee537fcb62f
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

### `rust:1.88-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:fc66d738f64bca39b62f4a8602bce8239a58d813a073dec6eb87c26ed46190c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead6f32afcd0798a56c170ce2851030ab2ae5772cc7aaaec8b47346331cd33a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d114182f83d2bc4d73e02cc5bb74bda2938943a605a1efe8e8e5921a9334c06b`  
		Last Modified: Tue, 01 Jul 2025 04:34:37 GMT  
		Size: 265.2 MB (265206650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f2b2479ca7328f021feef75a9a45f117ffc3ee13a53990561c1dde6401e77ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e7b91d95fa7f94247595b016c4b0afdf5c4568be554c642efa57ecedd45917`

```dockerfile
```

-	Layers:
	-	`sha256:17df34ae2e3f1174c3451942d63bf066080013096af8da1c1fae497282282c74`  
		Last Modified: Tue, 01 Jul 2025 05:44:38 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86c3b78ad1853f15af29c20213d59684bc1b948a20593345e4229e0c91d938ac`  
		Last Modified: Tue, 01 Jul 2025 05:44:39 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:2a8251a939f0d13ed2a1ea24d1f9ef251bbbf030d520485b394de2b9c23f1575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313623477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b182ed292d4c08791794619177de2b422b06a63b5f34f388d6e1f7c828ccf4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:96b51e81cdb8508366118f41a9ec499f52f0d0211b084d5d516e1be131b35266`  
		Last Modified: Tue, 01 Jul 2025 01:15:21 GMT  
		Size: 25.5 MB (25544163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e8ad713014c96437118acd9656b3f10b47964888722c469680e6042510ccb`  
		Last Modified: Wed, 02 Jul 2025 00:48:15 GMT  
		Size: 288.1 MB (288079314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d16acf27c46754346860ce745ea5760b105c162694adc9d454c94f795a796f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2cfe874064a2b600d64ab76c2b059316a0d09778b241f6d9ef1fe2850a3e56`

```dockerfile
```

-	Layers:
	-	`sha256:08e8559715569c50dc0f3e68ebbed15841af5fa459ca720c38fa15b3c2a035d4`  
		Last Modified: Tue, 01 Jul 2025 20:44:41 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffbb508550ec246d38153bd7938e330e200f9c02ca0f0d1d4b1abcc527101490`  
		Last Modified: Tue, 01 Jul 2025 20:44:42 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d7bf42de9bb8c46335f1541a795bd167560ad0c7d211e67cad3f5a7417243fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258705512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28cce79db40ab1d0fa12cbfa105d6ef1dff13b63c1a93b8fb9e9682a0418a59`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4458b4f354b132ede276e7da54a33c211b23ceac4f34da5ed2b7fae09bb95d6f`  
		Last Modified: Tue, 01 Jul 2025 14:45:32 GMT  
		Size: 230.0 MB (229961372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f8cb1c53bc02e47f1e50499e70854d43e2f98ddf439fa5b52d34a6424733aed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f09370c05fb448311182a49164c612c0299712281c47b1564078e73ebb6a67`

```dockerfile
```

-	Layers:
	-	`sha256:263fa190fe34f81500ba2e8ac8bf53f05869282f02579d474166a6be2567d51c`  
		Last Modified: Tue, 01 Jul 2025 14:44:39 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a44a181f21adc0542d1acb35f17b1f20343532cfd22efc73efb5044556e05115`  
		Last Modified: Tue, 01 Jul 2025 14:44:39 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:6aeeeeaf3ed73638e4135dce21527f418f6a192d3e2de9c4d26664694f90c0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.1 MB (321133034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e7dcea35fc6893afae54fc7ac2446ea032b06889451f72c5fb09918d9ba66c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:40be1da6146972d9df50a98eef7b5c0f729cd95a3a38782418f354f3b9355a9a`  
		Last Modified: Tue, 01 Jul 2025 01:14:57 GMT  
		Size: 31.2 MB (31189680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e1a302797c6fe4ad387e823eb711877bfcee5af925dcfc3decc2b4083fef72`  
		Last Modified: Tue, 01 Jul 2025 12:59:38 GMT  
		Size: 289.9 MB (289943354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8c4db6ccf78a02913434449b05bc26924375a6fa2a57e1fb8cdc0a9149a6128d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60622052414fe9b2982743aeebbe224601c12752ff8f4cbe89d50b54c59a8ad0`

```dockerfile
```

-	Layers:
	-	`sha256:423e3a39660d3cd9304a2f3cd9a7f0037ec79d19c72661b55bb7ed8a8d78a9ad`  
		Last Modified: Tue, 01 Jul 2025 05:44:54 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a0678dc17cc916be60884c0469158c1664b2dcd59755d390b82d7f534f97fa`  
		Last Modified: Tue, 01 Jul 2025 05:44:54 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88-slim-trixie`

```console
$ docker pull rust@sha256:e68d2ba3397c3c04c47647ad5d615afaca80ae00dcc4f5140e43495c537746c6
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

### `rust:1.88-slim-trixie` - linux; amd64

```console
$ docker pull rust@sha256:7721d2705af97fbfbf241d1f329e1e7144cb2743b2ecac5711352c8ea4fe3251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310236807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0d0605178c491bdb2bc093d06776322acffdddadb8d6b3ae47a7aba111cc68`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2b9064154c24154965e1b574cfe4999144b627db7f678b3a566d3eeeac02dc`  
		Last Modified: Thu, 03 Jul 2025 20:42:04 GMT  
		Size: 280.5 MB (280475701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:d619583f10fabd5f99a621389b8e4043ffa188cbd8eb305b7c2e7e8f2d63ed54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89914cf1279171e30ef2a59799b98b1a4e83babe84c87f1ff92ef591c7fc3ec`

```dockerfile
```

-	Layers:
	-	`sha256:c1e52b080a5caaa75906ac1aef51b1a4e5905284978a04a29d5def27fdaceafb`  
		Last Modified: Thu, 03 Jul 2025 17:45:05 GMT  
		Size: 4.2 MB (4162901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d4390982a55f7e70f969a7af51b2b195f34be5ebbe6c6f17d939bb524e497b`  
		Last Modified: Thu, 03 Jul 2025 17:45:06 GMT  
		Size: 12.1 KB (12061 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:57b1df7d4a1e8b0b231b0e8a09ae0cf89c7939542d2f1e1ff4a05f7de70f2a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322260431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a609326c1f09c4e6aa554b61b16080a0783429c62de582cd5e3ec4188913f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75cb2c2919cdd5f70bd8208e02191091cad32dd857e56bfd33f35cd6d531c82a`  
		Last Modified: Tue, 01 Jul 2025 01:18:55 GMT  
		Size: 26.2 MB (26201517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49ee1c5650c50a45b3eef84571458d78cbbf30fc06a0035bfa2a082ea8108d9`  
		Last Modified: Thu, 03 Jul 2025 20:48:22 GMT  
		Size: 296.1 MB (296058914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:cc54c83fc01e12d9d41cfdac572a59e588a4c54287deec7161e4b89d69757700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103636073af3a7f76abb00f7559b02484569bf5618ed3d571538a7ca3b02fc19`

```dockerfile
```

-	Layers:
	-	`sha256:ffce2eaa705d9368bce2a80cd6890bc3c2bf66295174b466a2007a02c4370d2b`  
		Last Modified: Thu, 03 Jul 2025 20:44:36 GMT  
		Size: 4.0 MB (3967745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb0ae2602c3fab378c0fcb74ec00c46711ce55c947b8f99952dd9d8fcae5488`  
		Last Modified: Thu, 03 Jul 2025 20:44:37 GMT  
		Size: 12.1 KB (12138 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:88a9c0d2b3c1ef6e0ab769f130a15a6cb2d10ed82ac6c779e1d5b543fa6a5a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274045556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47d037deb756e369db48be32af79a4b9410405268eb60580dffcfc577e67aad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:dfa10e860e0106510a14bae8331a4dd762d3d3737fdba0dbec102458f9853b71`  
		Last Modified: Tue, 01 Jul 2025 01:18:18 GMT  
		Size: 30.1 MB (30126864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab982be4b2f9d93ec333ffb69526256503de560bde0bd8a510e3b1acf793c40`  
		Last Modified: Thu, 03 Jul 2025 20:49:17 GMT  
		Size: 243.9 MB (243918692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:ec6e0fb8e467b4d66a4e91bfc44764be1efadf6791fcd25f1df5437d48d299dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a618e7a2fe30262bf7503eb5b80999a202d3e87df932a890048ca1fcb3b7b55a`

```dockerfile
```

-	Layers:
	-	`sha256:a7390525f3e02590517ad48faeb0649b52dd80e6a083feb652819a8c0320984b`  
		Last Modified: Thu, 03 Jul 2025 17:45:23 GMT  
		Size: 4.3 MB (4254069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad846470cf4d23ec2c6804afdf350c7808432e565fc39d3035fe1556cf21361e`  
		Last Modified: Thu, 03 Jul 2025 17:45:24 GMT  
		Size: 12.2 KB (12165 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim-trixie` - linux; 386

```console
$ docker pull rust@sha256:6fe11019a3d4d7e50e48f4727120357e98b6e3242ea944d72f20a57ccde3976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332943226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c31842ba66bed838d3be4cddc274c3b25d4f5c056d036b9d9c5646f2f83c35`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:27b0922c0fcc2ccb534e806841adaba77d7b1a639b51fa3d953ccfa3af3a57e6`  
		Last Modified: Tue, 01 Jul 2025 01:14:55 GMT  
		Size: 31.3 MB (31281109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfea6381854ff5a1288e44fcd71c127bf8f5c12b73fca05a53a0fdf766da33e`  
		Last Modified: Thu, 03 Jul 2025 20:49:34 GMT  
		Size: 301.7 MB (301662117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:709dfc3e62d11137fe59c004c57be56ba78c0370578c39fc986245bcc924fd3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d862b9c54929822ee442cfebc6bb3152f1e05190d3476d52017e9c30cbe3777`

```dockerfile
```

-	Layers:
	-	`sha256:d76b88999182b5b6e9bf50bf33640536dbe258725e8c01c0e11481b295d36251`  
		Last Modified: Thu, 03 Jul 2025 17:45:49 GMT  
		Size: 4.1 MB (4136434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff406b796b327df9d21a85be2fa42ed6e856e504634069cad7fdc6a139e510ad`  
		Last Modified: Thu, 03 Jul 2025 17:45:49 GMT  
		Size: 12.0 KB (12030 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim-trixie` - linux; ppc64le

```console
$ docker pull rust@sha256:cbef1f31e6e9d539b5e201653bc0553eadee350cf0a81efd0bdc75654187d7c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.2 MB (374189714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fe51377754a44b3b68c6389474ced3297711aa727c85fae16272f257d4d87f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05113943712185aeb07e0e0bfb3fa35e088bd6f08df1e776cc806f8bddc6db1`  
		Last Modified: Thu, 03 Jul 2025 20:50:14 GMT  
		Size: 340.6 MB (340603679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:03e00179fb0709f08bca4819fb0a5100a86a4f3d137fc7e3dd77ed4fb2bb5f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fb1b4f2f8d43288ca62d234578bbfb1d9527b44d43b4e8790007f3e694af6b`

```dockerfile
```

-	Layers:
	-	`sha256:187a0b4809cba5785eef2febd443d1c4537bde12b677052c85f9367e5c060989`  
		Last Modified: Thu, 03 Jul 2025 20:44:49 GMT  
		Size: 4.2 MB (4158025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79ae8b64b453a46d0ae29840bdd1a9e8658feec181cb272ffe4e3c012b5e5bb`  
		Last Modified: Thu, 03 Jul 2025 20:44:49 GMT  
		Size: 12.1 KB (12106 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-slim-trixie` - linux; s390x

```console
$ docker pull rust@sha256:95bd23402ed6a90153634a026962a9c6cb52036c619765e75882d1401cc2b899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.6 MB (365571899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a7d73fb037181cda5b98fb9704a92758f96457c24664ac81eb41524bc2a693`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:728fbd29b8599bd56dcb8703b5c428523bcf0f3d48c5e95804f60267a128a3bc`  
		Last Modified: Tue, 01 Jul 2025 01:19:25 GMT  
		Size: 29.8 MB (29838345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1456ed2701051abe37f5ce865394b5d3d701095089b1c134b195eebb09d77cb`  
		Last Modified: Thu, 03 Jul 2025 20:51:48 GMT  
		Size: 335.7 MB (335733554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:b3db53400e5e90db3bf6bafadf7ed5ba7942e99fdc2b1f29db7d9338241b026a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717ea3ea743c46facb7642e47482c5e4e2469868c735a4096c86797b8e34e0a4`

```dockerfile
```

-	Layers:
	-	`sha256:f44d67311a40081884ea925705988428fd00e3afd55d1da73c10871c627143af`  
		Last Modified: Thu, 03 Jul 2025 20:44:54 GMT  
		Size: 4.0 MB (3980649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e254e26728aaa08e68b3041c15896d2bbf46234e284651a8ca903e32d7f2794c`  
		Last Modified: Thu, 03 Jul 2025 20:44:55 GMT  
		Size: 12.1 KB (12062 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88-trixie`

```console
$ docker pull rust@sha256:b730c57c4c1679f1c847f0481ba8863a15d00cae22d367a7565f4422bf40d478
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

### `rust:1.88-trixie` - linux; amd64

```console
$ docker pull rust@sha256:777127bd6a86eae87d512c696f1b5d500307cae84a4b948e4b25942516d780ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.5 MB (583494432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392aa965c60a10bdc5365931c80308a245dfea6cc9bbe1aa073fb9cbb6d5c274`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13567152126a6abf6e98a928a4206f022be687e979bd113ce89b0b1f41fcbaf`  
		Last Modified: Tue, 01 Jul 2025 03:19:07 GMT  
		Size: 25.6 MB (25617737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f696393bed22361a2f932d3f084750c0cdf7e1f7186888c327230081e6257b0`  
		Last Modified: Tue, 01 Jul 2025 04:12:14 GMT  
		Size: 67.8 MB (67789682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b76da92f9efb17dc4a68c682bacce1ec791a87b62ee76639b08bfc2ee4577cd`  
		Last Modified: Tue, 01 Jul 2025 12:07:57 GMT  
		Size: 235.8 MB (235764377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9b092ebb229c418b5f5feea9ad11427731515a1d8dbf01adb95c1959d6bac6`  
		Last Modified: Thu, 03 Jul 2025 20:41:59 GMT  
		Size: 205.1 MB (205058759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:8568cd48443fa4a0c33851892d9da52f3d656b2399dcd83e6ea414378cb1e83b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17214539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06eb85b483e6f006b4ae1adf7622a1abf1ed4b6581de2f1824c28c05b4fafb0`

```dockerfile
```

-	Layers:
	-	`sha256:3e339bf185a305476f2c298204c80a4fa1d966d3dea7c9964a8704dd8772bff2`  
		Last Modified: Thu, 03 Jul 2025 17:45:24 GMT  
		Size: 17.2 MB (17202584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4abb423fff15f1c22361c92de405fb0ef8a88535b600fc76d86d707b3b09260`  
		Last Modified: Thu, 03 Jul 2025 17:45:25 GMT  
		Size: 12.0 KB (11955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:f0d61b9434bb38e2fc365679bf6ca2b15ac36a477ee4488bca51ab2432ded2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.7 MB (570716850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e270a7c2c6520ab1bc80e5bf40b5af01074724375045b6d1103cd5fab68e50`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0611a9c58dddfe7f00bb5fe6c8f5ccecfceeb1785acc68dc070068a94adf2092`  
		Last Modified: Tue, 01 Jul 2025 01:18:31 GMT  
		Size: 45.7 MB (45708080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571abb678dad668afa2696a67ffe4981c3b5aeb37fa4c14a0cc24fdac7949b6e`  
		Last Modified: Tue, 01 Jul 2025 08:59:50 GMT  
		Size: 23.6 MB (23617932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd28b3d9ecc5ff8b97a4e765e8a818c8ca6ea137650adb3df7d53acf265e9e4e`  
		Last Modified: Tue, 01 Jul 2025 18:31:52 GMT  
		Size: 62.8 MB (62760034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7255cfd7fa333e12d9432924dd0af6dceb8b6fca12f12faa2b5157b7e9cacc6`  
		Last Modified: Thu, 03 Jul 2025 10:55:31 GMT  
		Size: 192.8 MB (192838492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990aa9e5561becb9a9a31b185a40c4e082059b4a2f864a5ea4a0c72aa5306a5`  
		Last Modified: Thu, 03 Jul 2025 20:42:55 GMT  
		Size: 245.8 MB (245792312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:6eaf53d99ce3e71a7ea943eea06e0b1786528694755a32e99ac4ee29064aa755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16982621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8631aabd5bb545bf8056ef9539ea5075a0a8067a69adf2344dc7f33f9dcfbe7`

```dockerfile
```

-	Layers:
	-	`sha256:e1b2e6ea0d58fef7a142159e950d4cd70fad767db1159baa5d2ca9e850c1b39f`  
		Last Modified: Thu, 03 Jul 2025 17:45:54 GMT  
		Size: 17.0 MB (16970590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895c99ae34ac4942be372edd159f3a98dfcc60436b134a088738443b03f4f306`  
		Last Modified: Thu, 03 Jul 2025 17:45:56 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7c5ac5114acbafb83337d764aadd88ca774223507a916c6dd30bb082a20ec7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.5 MB (542536176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0697dd2649fdc7fa59d4cf781665f05caae4122011784ccef9a0f023a0570c48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064b8e4cb92aed27a99de363dac49c85bcb74d556fa925c921727dcdf03f7cb4`  
		Last Modified: Tue, 01 Jul 2025 06:53:32 GMT  
		Size: 25.0 MB (25008002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01789681d750567cf92706d649b58054ae1e27e35947e671160777a30538c3a2`  
		Last Modified: Wed, 02 Jul 2025 05:58:28 GMT  
		Size: 67.6 MB (67611970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4fcde14125f9212ba8ee255667590e6596810c45bdc694a8db749d7ff6d2bf`  
		Last Modified: Wed, 02 Jul 2025 06:00:35 GMT  
		Size: 226.0 MB (226025553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65018ead03f0d4f0382753ee911bff501d98c7ce180a3aabfb426c24deef1054`  
		Last Modified: Thu, 03 Jul 2025 20:12:11 GMT  
		Size: 174.3 MB (174260497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:5fd381b02f79c5c1f30501a2e74b4143d494518193a407ab4bd263d5d4495b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17298951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960a72fcf1731c737694fba1d68b27e7546e2cafa11ed72bdf7a1711136c2ca5`

```dockerfile
```

-	Layers:
	-	`sha256:beca260f3051e49975118b198c4e96523199398c5bfe36285d4ffc2c15e5afe1`  
		Last Modified: Thu, 03 Jul 2025 17:46:11 GMT  
		Size: 17.3 MB (17286892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637b38306d48fc5fd76b15fe7b2603dc5a04735734490c149d9278c4bd7ef21e`  
		Last Modified: Thu, 03 Jul 2025 17:46:14 GMT  
		Size: 12.1 KB (12059 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-trixie` - linux; 386

```console
$ docker pull rust@sha256:d4508bf7617fc0667b9f76693bfb223e42469dc1abfd62bc4affcf61fdec1d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.4 MB (616411351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f713341993075dddfd01eb0a193e3e5a746dc11f9c4688e2c3c41ab15827a02`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d223755a7489df8352d3a71955e26d35281b9c0f0609e017af54d9e75e3b435b`  
		Last Modified: Tue, 01 Jul 2025 01:14:59 GMT  
		Size: 50.8 MB (50786756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d932d83e6c250bb0f5c2003ae98b3b4dc3d40d3915a7ebed763f315741368`  
		Last Modified: Tue, 01 Jul 2025 02:24:58 GMT  
		Size: 26.8 MB (26772148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34925744005802787be957c67125f2aabf94afd5e8609668cc037c46d09591`  
		Last Modified: Tue, 01 Jul 2025 03:20:07 GMT  
		Size: 69.8 MB (69830306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f64900f9b3ef26b18f567a74a96e250e42a8eed2ff1fadd54a41cc0359ad74`  
		Last Modified: Tue, 01 Jul 2025 13:17:44 GMT  
		Size: 239.9 MB (239860428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786dd06ef0c1d508b04b744e9509815e8b97edb82567dae2ecc2f7f4608eb087`  
		Last Modified: Thu, 03 Jul 2025 20:45:12 GMT  
		Size: 229.2 MB (229161713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:f67a9186cf1554037b5bebdc2a29731e33b0560fb6f00acc72a972c06a6a8024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17182790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fa8116b6bed9af5ae6689a9a22779a1678697a915c5cd4d7e6b36066700e02`

```dockerfile
```

-	Layers:
	-	`sha256:0bc4ae22361d8be206beacebda88e0a0d9907d13fe49752729264b691a2573a4`  
		Last Modified: Thu, 03 Jul 2025 17:46:46 GMT  
		Size: 17.2 MB (17170867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00512048af2e89f74659ec4afeed8cb648de2fbc4c194e045bb7360d66547db4`  
		Last Modified: Thu, 03 Jul 2025 17:46:47 GMT  
		Size: 11.9 KB (11923 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-trixie` - linux; ppc64le

```console
$ docker pull rust@sha256:2b364c8eda85704eca9497cb33fca2d56eef23b799891c48db05140faffe245c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.9 MB (657910004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e48352ed179962dff629d52064abbff1ea21fc4849959f709243b2e442fae7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e868292aa714037cbba25d912564e5f392a5d355c383b03a8854e789c98ef`  
		Last Modified: Tue, 01 Jul 2025 05:08:57 GMT  
		Size: 27.0 MB (27003269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7107fc95f855d7880e921bbc85bf915f07c907c70d7d6f6a5334a32ad6c832`  
		Last Modified: Tue, 01 Jul 2025 10:12:36 GMT  
		Size: 73.1 MB (73068943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4744a5ce78804175c7109fb3df660a6bb53b2954bc5f2c48184739c714dfc8`  
		Last Modified: Thu, 03 Jul 2025 10:55:19 GMT  
		Size: 231.0 MB (231021360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c94c7eb559acad5a878c6b10fbcb0ecafad636824170be34ede5261baa6a2`  
		Last Modified: Thu, 03 Jul 2025 20:46:35 GMT  
		Size: 273.7 MB (273719196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:712f5014e1f676151678dfb32f438ebfc5c6ccce041ee1bfe0822c9f6e6a92b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17208092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e648406175ad5a0fff773fd402a380664ca93211dc1dc02b0e30ec1857290a`

```dockerfile
```

-	Layers:
	-	`sha256:e90c41129150eeb1baf61bb144eb1a5bf5136c3753a5e7ff747a93519edbced8`  
		Last Modified: Thu, 03 Jul 2025 17:47:19 GMT  
		Size: 17.2 MB (17196093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:223be277a3e6da23a3d10ec7c56a85066daeacf3199f6e2852aed61471673c6e`  
		Last Modified: Thu, 03 Jul 2025 17:47:20 GMT  
		Size: 12.0 KB (11999 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-trixie` - linux; s390x

```console
$ docker pull rust@sha256:b78680ff95452516a2a1ba080766115b52b09915350132aa95d221d83bb4a29f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 MB (634484977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b39c24e77ca6d3f82b32ead83f3c0c127e66c3c126e6397457389779e52ec7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8974c848015ae735631f879693069b8c536e3428274d79917837c027655a80`  
		Last Modified: Tue, 01 Jul 2025 05:31:56 GMT  
		Size: 26.8 MB (26785709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7360cccf58cfa285cf20d3ce14642c23bf3a2795b93396d0b9b743ee2e0779`  
		Last Modified: Tue, 01 Jul 2025 08:59:15 GMT  
		Size: 68.7 MB (68663824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694ce909d21b7fbf7c3fb87f40db93cf7588c89986fe25d341208d7b9ae60852`  
		Last Modified: Thu, 03 Jul 2025 10:55:27 GMT  
		Size: 206.3 MB (206329374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2362089a7d48f29102d6359bd8041b42be3e05af339f3916bfaefb996c680c`  
		Last Modified: Thu, 03 Jul 2025 20:47:14 GMT  
		Size: 283.4 MB (283362410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:f0605e4fb8dba38beea68b41893e3e6983c85a8d7ebe00d7b438ec8414f6d6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17001023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fec9741de5a55dec8253a44c86e746da1d1ec5db93d53031d57e5006c179026`

```dockerfile
```

-	Layers:
	-	`sha256:56417f7df327de8d5d5e7e0de1e2f59e7226739f9c6c2324cd0165abb66c39d8`  
		Last Modified: Thu, 03 Jul 2025 17:47:40 GMT  
		Size: 17.0 MB (16989068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bba5fb71a8222ba1b28462e4175f250445ba54f02cf3948e9d08d931e57d0ec`  
		Last Modified: Thu, 03 Jul 2025 17:47:40 GMT  
		Size: 12.0 KB (11955 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88.0`

```console
$ docker pull rust@sha256:5771a3cc2081935c59ac52b92d49c9e164d4fed92c9f6420aa8cc50364aead6e
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

### `rust:1.88.0` - linux; amd64

```console
$ docker pull rust@sha256:95f6d6956bf8abd7461763ba7ccd243d8964a41c8eb3f41d895490c782628d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553347880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a479811b82446e6bf598238bb2fcd3ae41b351a1a7c87e53d8f2333a7bbe001d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe9c1abe6f3b8ca9fc6abe710405f830f95262f1d356e8f6545d823b5840a5c`  
		Last Modified: Tue, 01 Jul 2025 05:12:07 GMT  
		Size: 211.4 MB (211373500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0545d5f3de1a8249849f4342031613d732af87e31f13755f5fac287119ed13e8`  
		Last Modified: Tue, 01 Jul 2025 06:18:35 GMT  
		Size: 205.1 MB (205059525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0` - unknown; unknown

```console
$ docker pull rust@sha256:0e0dc34caec6b81f1b5ab4c9a559c11b4d7440382c69d8a2cdbe5002a71523e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15877001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81308c8e2c35f38fbef285c685f2ca642508d83efc22df71984838afd98ac55d`

```dockerfile
```

-	Layers:
	-	`sha256:3260e53bff48cf37775cac874c3e2920680f90a7669e12d2c322771f16c50614`  
		Last Modified: Tue, 01 Jul 2025 08:44:24 GMT  
		Size: 15.9 MB (15863862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a629d4f8f234144e7bda08172e21d63709f916bfe46836348a616c43d2cdd880`  
		Last Modified: Tue, 01 Jul 2025 08:44:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0` - linux; arm variant v7

```console
$ docker pull rust@sha256:b12fb2b0506d2b8fde83230531af65c46d2e1cb65c7b965a23de3015d7feff05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546880259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe31256245950fcf402e7f41d298a8bd3859cf9558a2e1ff584d64071362bda1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc606b1195a348c6a47399c1a54ab936d4477a526d62306ddce89fe76a2d22`  
		Last Modified: Tue, 01 Jul 2025 08:59:56 GMT  
		Size: 21.9 MB (21928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f4c85f426e2c955b1dac4fa88bc182d725644c23ad01bdcbf64d9664e34a8`  
		Last Modified: Tue, 01 Jul 2025 18:28:59 GMT  
		Size: 59.7 MB (59656492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda2264dd6dda88971c220cda9283a6c337d04aeb92012d9d160887d4ec0b556`  
		Last Modified: Wed, 02 Jul 2025 00:17:51 GMT  
		Size: 175.3 MB (175294922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5ff6581ced6c9c0cc98e703fa5901cda1814bee9d3ac91337dfcb2eeaa3fa`  
		Last Modified: Wed, 02 Jul 2025 12:16:49 GMT  
		Size: 245.8 MB (245792330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0` - unknown; unknown

```console
$ docker pull rust@sha256:a6b6613abe69a8ea05c159027354fad9e25a0f58f5a61a4c761bd608e9118f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15679627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0222859d21f0de033a308a561262ae0c61dc1ab6441395c68809f9d9455913d`

```dockerfile
```

-	Layers:
	-	`sha256:d6bf21d47ea4882f2e19fc8c2018d3473ff3633b948a8a2912ffa2fb5dc5c75c`  
		Last Modified: Wed, 02 Jul 2025 11:44:31 GMT  
		Size: 15.7 MB (15666380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f88163f4b88d616cf50cd1d0bb3bb47eda6485492c98f7f4bc8035c0d832d762`  
		Last Modified: Wed, 02 Jul 2025 11:44:32 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:66b553fe51fe4eba929ee31c39d66506fe41b72cf403dab3117de2bd5d43e645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513346599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5424600217354e80a3f0ab99133ec64aa48f464a2f1c29a93cbd0f95758e5af7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a65abb6272f500a9ae5d14c9ae8ef9cb0e4009b02acfccb4dabc478f252d44`  
		Last Modified: Tue, 01 Jul 2025 19:38:43 GMT  
		Size: 202.8 MB (202827049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b360d25d0e207b0afc74cd93a7662c88e8399a9798db1e3baa5665c7aa6c157`  
		Last Modified: Wed, 02 Jul 2025 03:35:58 GMT  
		Size: 174.3 MB (174259463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0` - unknown; unknown

```console
$ docker pull rust@sha256:2f4addd958f6c23177ba57cb0b62703dba22d22d022fa5ff6111f60b883e3dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15905729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3c6db7f65484d03b4cc60245a2ead7632bf36cf44fdf76c3720b3831df124c`

```dockerfile
```

-	Layers:
	-	`sha256:ac641e00624bd7b454d162d456dcbebc72d34940b2f4aa530da90b3cbe71d493`  
		Last Modified: Wed, 02 Jul 2025 05:44:37 GMT  
		Size: 15.9 MB (15892438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1fa12a678c68a338b4e49d70c17dbded6143e0d3861664cbccf02c362f6879`  
		Last Modified: Wed, 02 Jul 2025 05:44:38 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0` - linux; 386

```console
$ docker pull rust@sha256:628fa076d84051d529c70e5978ae2488cc27c057e4378e6d6b4427cd1f48f5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (580031340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b007959168ba93c975145eae21e48f1112c685910223873e0805f91c16efcf81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99742b01aaf231df6992d8ecab593f6a7668b9047c6bb8cae0cc211c42b656d6`  
		Last Modified: Tue, 01 Jul 2025 05:11:03 GMT  
		Size: 210.3 MB (210310619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a36703fa30e50f1e2d2d9b8d6ee38f74b5c49158c0331edd0ac22489b68c9d`  
		Last Modified: Tue, 01 Jul 2025 08:59:26 GMT  
		Size: 229.2 MB (229161050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0` - unknown; unknown

```console
$ docker pull rust@sha256:60118c6a0bd04b58edbef1c693c60eef0a5c39a11250ffab32588f40429c495a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15853847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a0f3771a2d9e6d62cb0c6bcec0264fbabb8e5129657775262a756a4ab9cc9`

```dockerfile
```

-	Layers:
	-	`sha256:aede24ae4b2038e2305b863ac4a0808c493737d5ec9bc1219a2ffcdf76249352`  
		Last Modified: Tue, 01 Jul 2025 08:44:58 GMT  
		Size: 15.8 MB (15840760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adee46bd81fb5e17001fc933d0596dd15dc9c7296c5efe1c744ecb38885cff77`  
		Last Modified: Tue, 01 Jul 2025 08:44:59 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0` - linux; ppc64le

```console
$ docker pull rust@sha256:f4c7cad30a4575e18ae53f14b5bccb71451b44d720253a8f73f1cb12780bbf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635985035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442858853b317d76b745617081af4451d23840bd47301b0eabc620759c4b714`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7082fff0db11ec79e9a3c8fc9c05691e086d30ca51023010805fccbeac2b8dad`  
		Last Modified: Tue, 01 Jul 2025 05:07:55 GMT  
		Size: 25.7 MB (25663667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6cd79d875ce6ba17d2080d5bd4d0d55f7eec0f6bb923ae0b53e5bec14ef9b`  
		Last Modified: Tue, 01 Jul 2025 10:09:38 GMT  
		Size: 69.8 MB (69840014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575c9bdfba8d02bb3354a6a72904306bd1ae2c4432d14255385a153c75887837`  
		Last Modified: Tue, 01 Jul 2025 16:27:30 GMT  
		Size: 214.4 MB (214424908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078767722b4e04b7787f0ea5f95284ec4da0e1c5dc7804af4c26dc5181ec096c`  
		Last Modified: Wed, 02 Jul 2025 00:02:53 GMT  
		Size: 273.7 MB (273719203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0` - unknown; unknown

```console
$ docker pull rust@sha256:1a33a8b84d73eb3cf5fe4d5eb91a7212e3e015e40670b51ddebf3b52c4dbe0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee34f793447401153bab355f4bfbba25c4161b769172568c3b013931ffcfc953`

```dockerfile
```

-	Layers:
	-	`sha256:a169d322c59d3a0ddff0bf27d48dbe267dff9b48aaddd2ed30804cb885ff2527`  
		Last Modified: Tue, 01 Jul 2025 23:44:57 GMT  
		Size: 15.8 MB (15839092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d4887067e8590d2b12056401643ede686e2b3a83a2fccdfca0b762a5961e6a7`  
		Last Modified: Tue, 01 Jul 2025 23:44:58 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0` - linux; s390x

```console
$ docker pull rust@sha256:79ee189d40fd6c859e15a1e9c69b6da58d451b096e16a52dfec29b9bd0d76a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.5 MB (601452429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924b21bb8e92662795debcd307e3f3204964743780a9f028dfb3700b0ae8640b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1e32b479a11528098c70ba4af6292099abafcb29e0823d2861c86032c9b0b`  
		Last Modified: Tue, 01 Jul 2025 13:41:28 GMT  
		Size: 63.5 MB (63497964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2254c2dc3c53615f5f6a5adcfafb558670473622cb504cb0a6d02fd2b89d2667`  
		Last Modified: Tue, 01 Jul 2025 14:10:41 GMT  
		Size: 183.4 MB (183421934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c312814d252c566d3c3ee8f98763bedd5510a970a7460965bac0ea117ac8071c`  
		Last Modified: Tue, 01 Jul 2025 21:03:03 GMT  
		Size: 283.4 MB (283362703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0` - unknown; unknown

```console
$ docker pull rust@sha256:a4f9cf4a09562544ef011200268fb453c235bc5b972df93f32ca2dbf4ac1e349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15684597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afc1cf86bd3504dbe315e3c93562fc2ff8e92d15305627e7b38023518ec873b`

```dockerfile
```

-	Layers:
	-	`sha256:39dbb3c0f9a78d73aea412786fb8fabb2d333d5f18f4608bab4734aaa8e60fd7`  
		Last Modified: Tue, 01 Jul 2025 20:45:07 GMT  
		Size: 15.7 MB (15671458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d32a8a23e2b1c8cb3fdec2c521041d1a7fc5c908e5a6ce6bd3048f58dfefe8`  
		Last Modified: Tue, 01 Jul 2025 20:45:08 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88.0-alpine`

```console
$ docker pull rust@sha256:ec0413a092f4cc01b32e08f991485abe4467ef95c7416a6643a063a141c2e0ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.88.0-alpine` - linux; amd64

```console
$ docker pull rust@sha256:b18203be0f58e16fe47250bf98bbe83c61bbfa97a0f5a94cebf34605bb000137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324842014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccfa6e07df925301f1f0b76b6784e617369e209ccfd7b16e76a3f50bca1e544`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c179a1cc9cc1626cd02fbb4866ee1705894a35d0acf8458e7f0274620ded46`  
		Last Modified: Thu, 26 Jun 2025 19:02:56 GMT  
		Size: 61.6 MB (61613765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b44eb86436bd74e3289f02e42ae2c9df9c6a39ac3ff054f893f7cbaddbcf08b`  
		Last Modified: Thu, 26 Jun 2025 20:45:29 GMT  
		Size: 259.4 MB (259431403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:3a48955a20cd88465d43306589af8be8e9aab9bc4983ebf983267397b0038f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8794bb5882365fcd697f232d90c928f4dfc42f2d9dee1f418d14cba22fc740`

```dockerfile
```

-	Layers:
	-	`sha256:4af3880faef85aba29ec3559478d1219bcd27ba3aa3e498970fa8eb110c9fbbe`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d7d4050c4275c54863ef9a56b9e59d3e338bc902f05df72abcbf103b3bf06c`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:43c5afb577aa21180b984fe215c836db0e8da8c6d6e29f4f5d60fcac8f6747e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324286625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037fc7bdc081378f949b34f5b57abb98ba2f2308d8e24c81eec1dc00f8095344`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe32611e1706eb5e71110ea02f0a43bcf8d9d5b31375d8372476ca0151ea4e79`  
		Last Modified: Thu, 26 Jun 2025 19:09:40 GMT  
		Size: 59.2 MB (59154287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd9ba9c44d35a05a92f10caaf51df4bf98f7cd9e90070d71790f3fa3de848fa`  
		Last Modified: Thu, 26 Jun 2025 20:48:42 GMT  
		Size: 261.0 MB (260996397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:f7f6eaadbe7a000ba5420c2ea8c78d7812aea2e2ba405d6f47c7dcc77af1c77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fcba7c7ba45a16b412de43acab6b32790c948a2de7b038009b4fe3f5344978`

```dockerfile
```

-	Layers:
	-	`sha256:0ece12c371cca20fa75cd9470ad9eb8f90b1172dae46baaf4940565722fcf88e`  
		Last Modified: Thu, 26 Jun 2025 20:44:43 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49231f16442a61f2a0b6140092b2b40d1a3786b17de63fc044fabaa5fbcee312`  
		Last Modified: Thu, 26 Jun 2025 20:44:44 GMT  
		Size: 12.1 KB (12084 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88.0-alpine3.20`

```console
$ docker pull rust@sha256:3ab9b805c8d2444f6f63f1ae7a38b5e04949d6b0d9e8a314e1ee3ad502deae45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.88.0-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:985c5bffc08709b4c04506340fcdc2542dfd0604070a993c409a6565e200c488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318374251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4468520ebd63f0d5993bf50e71ce97ce1770aee2cf170f4b68416cbd826434`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd8e343fc1e8b59389632b1aa1fec9897eb0d70d9a028c4953824eaca48506`  
		Last Modified: Thu, 26 Jun 2025 19:02:57 GMT  
		Size: 55.3 MB (55315554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af473c39e92f0a526585dfa175d2324b3bcc5653f1f8b4a0197290536a1a4b82`  
		Last Modified: Thu, 26 Jun 2025 22:03:51 GMT  
		Size: 259.4 MB (259431800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:6d1398d665e6f2fad6e604e6b35246a23905cff0473753ad60eee908c8602f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.5 KB (722503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ed6595279fc3b8ec29033696b6a0ff4d9c437f59ceeaf9052d8a7b745cac53`

```dockerfile
```

-	Layers:
	-	`sha256:172a379c01373f9fa6f1f7546d8f14ca43f16dbed174f0fb1038d9ad729985b4`  
		Last Modified: Thu, 26 Jun 2025 20:44:46 GMT  
		Size: 711.8 KB (711789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c520dac29e5f70b8c11a8c70a95fc0a3a9bb4ca3b5499c004ab4cf05e37e7ce2`  
		Last Modified: Thu, 26 Jun 2025 20:44:46 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bbc890fbb4cfe63267e61b157106ae17e22fea8965bd86dad3ba2895731fd832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.0 MB (318036721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2562e20c93fbfe25e95e223728ea45fdabb24f56872078249b32a94618aef470`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f73dbcfd8a123487699fe68590b2bd9f99926de28d20db07b032c7c04a77d5b`  
		Last Modified: Thu, 26 Jun 2025 19:07:09 GMT  
		Size: 53.0 MB (52950135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35f71611cb454ac5691276f7fb4f820ad5cca79bd33a16a47b3383d0199fd5d`  
		Last Modified: Thu, 26 Jun 2025 22:04:01 GMT  
		Size: 261.0 MB (260995421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:ffe59248eec0f167209f1689d76dc0cf65197edb7123968bab9d9736ed5dbe1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bf25ee4d7342c1573d066bf9d6490bc899c772b46d58fb99616651dff2a12a`

```dockerfile
```

-	Layers:
	-	`sha256:fb91044d3c55c5b9a10f560693a397817a79b1c3e9cac98794b2cc2378ddf88f`  
		Last Modified: Thu, 26 Jun 2025 20:44:50 GMT  
		Size: 747.7 KB (747721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619847fa4854614400d1faefbfd3dca469c0ddb922f14d8b21e0cfee7113e7b2`  
		Last Modified: Thu, 26 Jun 2025 20:44:51 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88.0-alpine3.21`

```console
$ docker pull rust@sha256:9c6a4baf58661f99a5441b15e3ad8295dabf35e849c4935e77ad35d9809be1d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.88.0-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:f76a41f6a9d96aca247c6789369bb5986c9faaef5d0ab080ae28346725d86c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324637733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd470e8018c4c8d13c36bb6d82b21b2b35e0cab903eaabfd2ba2cdbc0d49d8c9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a9008c78a14e56fc9106b9415625622b22d3e7d7ed88d4c9f168084a5b930a`  
		Last Modified: Thu, 26 Jun 2025 19:02:57 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99aa10cef404820ac909a9c36a9398af421599896d89f5216fe03a0484938cbc`  
		Last Modified: Thu, 26 Jun 2025 20:47:21 GMT  
		Size: 259.4 MB (259430674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:bfe3ce46af8506744eb91a950436d78f9b57aa1c89dab3f0c8cf5796a6964767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063fdf51672810ea7124832520f622f7d4a1bd29ff180e4e39b155177f6ce538`

```dockerfile
```

-	Layers:
	-	`sha256:bd239d1a7ba898b4e5db9276ef7089d6bd3dc5fbc114c96a656434c2b620e7a4`  
		Last Modified: Thu, 26 Jun 2025 20:44:52 GMT  
		Size: 782.6 KB (782619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68bd06a7d86815924cf9c1da819c34ded738a4b417cf24f9b33b853d7a3d1bb2`  
		Last Modified: Thu, 26 Jun 2025 20:44:53 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:390d7bebae8a355bd9e439bffd1f0f0124d0ade0a01602308b3c663490f66a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.1 MB (324089393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c931f5d71d48f4c73a17c302da0df6ebc23b15ced06b4f4ab775f1ec6e5228`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa43a6919f3e4298c4ac7012f740c568baceb922776f8df0f76856cc3ee4662`  
		Last Modified: Thu, 26 Jun 2025 19:08:40 GMT  
		Size: 59.1 MB (59101301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aad9f05f3e21035ae8f9c44b60e6bd73096afc6f6fa0e572587f6b65e6ece8`  
		Last Modified: Thu, 26 Jun 2025 20:47:22 GMT  
		Size: 261.0 MB (260995063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:03bf0509d1cc316b17044231bd28292d0828891ee21cde73471813fed5ee7435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (872990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eaca6f25dcca1d3f5272d1eef631f701b29c34b87f57293ddd1769d867a156`

```dockerfile
```

-	Layers:
	-	`sha256:263657c33753a7119953e3eaf32bfa7eb0f92250b29093be5e85cee6402a4952`  
		Last Modified: Thu, 26 Jun 2025 20:44:57 GMT  
		Size: 862.2 KB (862157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7daa109bbb3d9da7db18c495a2c43ac74998f6a27162c51bbc993b97bf68fa0`  
		Last Modified: Thu, 26 Jun 2025 20:44:57 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88.0-alpine3.22`

```console
$ docker pull rust@sha256:ec0413a092f4cc01b32e08f991485abe4467ef95c7416a6643a063a141c2e0ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.88.0-alpine3.22` - linux; amd64

```console
$ docker pull rust@sha256:b18203be0f58e16fe47250bf98bbe83c61bbfa97a0f5a94cebf34605bb000137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324842014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccfa6e07df925301f1f0b76b6784e617369e209ccfd7b16e76a3f50bca1e544`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c179a1cc9cc1626cd02fbb4866ee1705894a35d0acf8458e7f0274620ded46`  
		Last Modified: Thu, 26 Jun 2025 19:02:56 GMT  
		Size: 61.6 MB (61613765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b44eb86436bd74e3289f02e42ae2c9df9c6a39ac3ff054f893f7cbaddbcf08b`  
		Last Modified: Thu, 26 Jun 2025 20:45:29 GMT  
		Size: 259.4 MB (259431403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:3a48955a20cd88465d43306589af8be8e9aab9bc4983ebf983267397b0038f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8794bb5882365fcd697f232d90c928f4dfc42f2d9dee1f418d14cba22fc740`

```dockerfile
```

-	Layers:
	-	`sha256:4af3880faef85aba29ec3559478d1219bcd27ba3aa3e498970fa8eb110c9fbbe`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d7d4050c4275c54863ef9a56b9e59d3e338bc902f05df72abcbf103b3bf06c`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:43c5afb577aa21180b984fe215c836db0e8da8c6d6e29f4f5d60fcac8f6747e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324286625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037fc7bdc081378f949b34f5b57abb98ba2f2308d8e24c81eec1dc00f8095344`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe32611e1706eb5e71110ea02f0a43bcf8d9d5b31375d8372476ca0151ea4e79`  
		Last Modified: Thu, 26 Jun 2025 19:09:40 GMT  
		Size: 59.2 MB (59154287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd9ba9c44d35a05a92f10caaf51df4bf98f7cd9e90070d71790f3fa3de848fa`  
		Last Modified: Thu, 26 Jun 2025 20:48:42 GMT  
		Size: 261.0 MB (260996397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:f7f6eaadbe7a000ba5420c2ea8c78d7812aea2e2ba405d6f47c7dcc77af1c77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fcba7c7ba45a16b412de43acab6b32790c948a2de7b038009b4fe3f5344978`

```dockerfile
```

-	Layers:
	-	`sha256:0ece12c371cca20fa75cd9470ad9eb8f90b1172dae46baaf4940565722fcf88e`  
		Last Modified: Thu, 26 Jun 2025 20:44:43 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49231f16442a61f2a0b6140092b2b40d1a3786b17de63fc044fabaa5fbcee312`  
		Last Modified: Thu, 26 Jun 2025 20:44:44 GMT  
		Size: 12.1 KB (12084 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88.0-bookworm`

```console
$ docker pull rust@sha256:5771a3cc2081935c59ac52b92d49c9e164d4fed92c9f6420aa8cc50364aead6e
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

### `rust:1.88.0-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:95f6d6956bf8abd7461763ba7ccd243d8964a41c8eb3f41d895490c782628d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553347880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a479811b82446e6bf598238bb2fcd3ae41b351a1a7c87e53d8f2333a7bbe001d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe9c1abe6f3b8ca9fc6abe710405f830f95262f1d356e8f6545d823b5840a5c`  
		Last Modified: Tue, 01 Jul 2025 05:12:07 GMT  
		Size: 211.4 MB (211373500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0545d5f3de1a8249849f4342031613d732af87e31f13755f5fac287119ed13e8`  
		Last Modified: Tue, 01 Jul 2025 06:18:35 GMT  
		Size: 205.1 MB (205059525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0e0dc34caec6b81f1b5ab4c9a559c11b4d7440382c69d8a2cdbe5002a71523e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15877001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81308c8e2c35f38fbef285c685f2ca642508d83efc22df71984838afd98ac55d`

```dockerfile
```

-	Layers:
	-	`sha256:3260e53bff48cf37775cac874c3e2920680f90a7669e12d2c322771f16c50614`  
		Last Modified: Tue, 01 Jul 2025 08:44:24 GMT  
		Size: 15.9 MB (15863862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a629d4f8f234144e7bda08172e21d63709f916bfe46836348a616c43d2cdd880`  
		Last Modified: Tue, 01 Jul 2025 08:44:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:b12fb2b0506d2b8fde83230531af65c46d2e1cb65c7b965a23de3015d7feff05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546880259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe31256245950fcf402e7f41d298a8bd3859cf9558a2e1ff584d64071362bda1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc606b1195a348c6a47399c1a54ab936d4477a526d62306ddce89fe76a2d22`  
		Last Modified: Tue, 01 Jul 2025 08:59:56 GMT  
		Size: 21.9 MB (21928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f4c85f426e2c955b1dac4fa88bc182d725644c23ad01bdcbf64d9664e34a8`  
		Last Modified: Tue, 01 Jul 2025 18:28:59 GMT  
		Size: 59.7 MB (59656492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda2264dd6dda88971c220cda9283a6c337d04aeb92012d9d160887d4ec0b556`  
		Last Modified: Wed, 02 Jul 2025 00:17:51 GMT  
		Size: 175.3 MB (175294922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5ff6581ced6c9c0cc98e703fa5901cda1814bee9d3ac91337dfcb2eeaa3fa`  
		Last Modified: Wed, 02 Jul 2025 12:16:49 GMT  
		Size: 245.8 MB (245792330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a6b6613abe69a8ea05c159027354fad9e25a0f58f5a61a4c761bd608e9118f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15679627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0222859d21f0de033a308a561262ae0c61dc1ab6441395c68809f9d9455913d`

```dockerfile
```

-	Layers:
	-	`sha256:d6bf21d47ea4882f2e19fc8c2018d3473ff3633b948a8a2912ffa2fb5dc5c75c`  
		Last Modified: Wed, 02 Jul 2025 11:44:31 GMT  
		Size: 15.7 MB (15666380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f88163f4b88d616cf50cd1d0bb3bb47eda6485492c98f7f4bc8035c0d832d762`  
		Last Modified: Wed, 02 Jul 2025 11:44:32 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:66b553fe51fe4eba929ee31c39d66506fe41b72cf403dab3117de2bd5d43e645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513346599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5424600217354e80a3f0ab99133ec64aa48f464a2f1c29a93cbd0f95758e5af7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a65abb6272f500a9ae5d14c9ae8ef9cb0e4009b02acfccb4dabc478f252d44`  
		Last Modified: Tue, 01 Jul 2025 19:38:43 GMT  
		Size: 202.8 MB (202827049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b360d25d0e207b0afc74cd93a7662c88e8399a9798db1e3baa5665c7aa6c157`  
		Last Modified: Wed, 02 Jul 2025 03:35:58 GMT  
		Size: 174.3 MB (174259463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2f4addd958f6c23177ba57cb0b62703dba22d22d022fa5ff6111f60b883e3dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15905729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3c6db7f65484d03b4cc60245a2ead7632bf36cf44fdf76c3720b3831df124c`

```dockerfile
```

-	Layers:
	-	`sha256:ac641e00624bd7b454d162d456dcbebc72d34940b2f4aa530da90b3cbe71d493`  
		Last Modified: Wed, 02 Jul 2025 05:44:37 GMT  
		Size: 15.9 MB (15892438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1fa12a678c68a338b4e49d70c17dbded6143e0d3861664cbccf02c362f6879`  
		Last Modified: Wed, 02 Jul 2025 05:44:38 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-bookworm` - linux; 386

```console
$ docker pull rust@sha256:628fa076d84051d529c70e5978ae2488cc27c057e4378e6d6b4427cd1f48f5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (580031340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b007959168ba93c975145eae21e48f1112c685910223873e0805f91c16efcf81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99742b01aaf231df6992d8ecab593f6a7668b9047c6bb8cae0cc211c42b656d6`  
		Last Modified: Tue, 01 Jul 2025 05:11:03 GMT  
		Size: 210.3 MB (210310619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a36703fa30e50f1e2d2d9b8d6ee38f74b5c49158c0331edd0ac22489b68c9d`  
		Last Modified: Tue, 01 Jul 2025 08:59:26 GMT  
		Size: 229.2 MB (229161050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:60118c6a0bd04b58edbef1c693c60eef0a5c39a11250ffab32588f40429c495a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15853847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a0f3771a2d9e6d62cb0c6bcec0264fbabb8e5129657775262a756a4ab9cc9`

```dockerfile
```

-	Layers:
	-	`sha256:aede24ae4b2038e2305b863ac4a0808c493737d5ec9bc1219a2ffcdf76249352`  
		Last Modified: Tue, 01 Jul 2025 08:44:58 GMT  
		Size: 15.8 MB (15840760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adee46bd81fb5e17001fc933d0596dd15dc9c7296c5efe1c744ecb38885cff77`  
		Last Modified: Tue, 01 Jul 2025 08:44:59 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:f4c7cad30a4575e18ae53f14b5bccb71451b44d720253a8f73f1cb12780bbf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635985035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442858853b317d76b745617081af4451d23840bd47301b0eabc620759c4b714`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7082fff0db11ec79e9a3c8fc9c05691e086d30ca51023010805fccbeac2b8dad`  
		Last Modified: Tue, 01 Jul 2025 05:07:55 GMT  
		Size: 25.7 MB (25663667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6cd79d875ce6ba17d2080d5bd4d0d55f7eec0f6bb923ae0b53e5bec14ef9b`  
		Last Modified: Tue, 01 Jul 2025 10:09:38 GMT  
		Size: 69.8 MB (69840014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575c9bdfba8d02bb3354a6a72904306bd1ae2c4432d14255385a153c75887837`  
		Last Modified: Tue, 01 Jul 2025 16:27:30 GMT  
		Size: 214.4 MB (214424908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078767722b4e04b7787f0ea5f95284ec4da0e1c5dc7804af4c26dc5181ec096c`  
		Last Modified: Wed, 02 Jul 2025 00:02:53 GMT  
		Size: 273.7 MB (273719203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1a33a8b84d73eb3cf5fe4d5eb91a7212e3e015e40670b51ddebf3b52c4dbe0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee34f793447401153bab355f4bfbba25c4161b769172568c3b013931ffcfc953`

```dockerfile
```

-	Layers:
	-	`sha256:a169d322c59d3a0ddff0bf27d48dbe267dff9b48aaddd2ed30804cb885ff2527`  
		Last Modified: Tue, 01 Jul 2025 23:44:57 GMT  
		Size: 15.8 MB (15839092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d4887067e8590d2b12056401643ede686e2b3a83a2fccdfca0b762a5961e6a7`  
		Last Modified: Tue, 01 Jul 2025 23:44:58 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:79ee189d40fd6c859e15a1e9c69b6da58d451b096e16a52dfec29b9bd0d76a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.5 MB (601452429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924b21bb8e92662795debcd307e3f3204964743780a9f028dfb3700b0ae8640b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1e32b479a11528098c70ba4af6292099abafcb29e0823d2861c86032c9b0b`  
		Last Modified: Tue, 01 Jul 2025 13:41:28 GMT  
		Size: 63.5 MB (63497964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2254c2dc3c53615f5f6a5adcfafb558670473622cb504cb0a6d02fd2b89d2667`  
		Last Modified: Tue, 01 Jul 2025 14:10:41 GMT  
		Size: 183.4 MB (183421934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c312814d252c566d3c3ee8f98763bedd5510a970a7460965bac0ea117ac8071c`  
		Last Modified: Tue, 01 Jul 2025 21:03:03 GMT  
		Size: 283.4 MB (283362703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a4f9cf4a09562544ef011200268fb453c235bc5b972df93f32ca2dbf4ac1e349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15684597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afc1cf86bd3504dbe315e3c93562fc2ff8e92d15305627e7b38023518ec873b`

```dockerfile
```

-	Layers:
	-	`sha256:39dbb3c0f9a78d73aea412786fb8fabb2d333d5f18f4608bab4734aaa8e60fd7`  
		Last Modified: Tue, 01 Jul 2025 20:45:07 GMT  
		Size: 15.7 MB (15671458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d32a8a23e2b1c8cb3fdec2c521041d1a7fc5c908e5a6ce6bd3048f58dfefe8`  
		Last Modified: Tue, 01 Jul 2025 20:45:08 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88.0-bullseye`

```console
$ docker pull rust@sha256:8eb96c7c77c04660a95d5e256869de0a18130f97624ef75c522ea886d4e51d95
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

### `rust:1.88.0-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:4fe592966775f3396e3d099d674f0664e4383336371ca5600e40c2fe3b575383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526479452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e24231a2d9ba56b24304902b7106252b1ba5aa98dc98b58ac09df699a11813e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06772a4eff3df697497bb68b4dcdeb97fdb9338b5e7dde7d1a53579c3203c9ba`  
		Last Modified: Tue, 01 Jul 2025 03:20:06 GMT  
		Size: 54.8 MB (54757481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd49c17bd36c59d7bf7afe446ee52f36cad8a6393628526989f2db44b4486c1`  
		Last Modified: Tue, 01 Jul 2025 05:11:29 GMT  
		Size: 197.1 MB (197142751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b35768b15c47fe75ef345baf1601f003231cf7fa1353d4b05177acb4b38d712`  
		Last Modified: Tue, 01 Jul 2025 06:44:33 GMT  
		Size: 205.1 MB (205059062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f26b96d6cf3fe96312784ed4c21daceefd839ea7ec263a286a9c464c17889bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15475219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4229b2d8712383288725ba877fc8da75d82f25002251269162108f995d12061e`

```dockerfile
```

-	Layers:
	-	`sha256:2186b18143b7f42f67f19ba8594c9c55a420158d4af543684506320400941527`  
		Last Modified: Tue, 01 Jul 2025 08:44:36 GMT  
		Size: 15.5 MB (15463971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c86f9b373cccbb5f795ae509ad60503878f0f8e5a247421fd1a6f1461968cb`  
		Last Modified: Tue, 01 Jul 2025 08:44:37 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:d9735061f6bd324ad5d9a6b1f353e919d01b9515946a2de100568511a1182afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.9 MB (527938900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c390dbe5f1131b80bb7b105624994b79e2115d8dec0bcace50edd510c2198b13`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:efcf40eae0046ccd92d3b47ff685e1e9cf7a34d0a92f6de893078f115e01f20f`  
		Last Modified: Tue, 01 Jul 2025 01:15:14 GMT  
		Size: 49.0 MB (49043960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6769ed354ec7fde57e63bdf9788543b96fd8f93923607ad70767b9c4cfa25b`  
		Last Modified: Tue, 01 Jul 2025 08:59:49 GMT  
		Size: 14.9 MB (14880774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28365fa3b8363bfd29e20b4b17838c65ddc4bdacb1bf15ca9af5a4045e4feaf7`  
		Last Modified: Tue, 01 Jul 2025 18:29:48 GMT  
		Size: 50.6 MB (50631320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31eafcbc0a8afc051ea3519738dd6b4e501ce5f603e4a10bdf1f0f6720a29f58`  
		Last Modified: Wed, 02 Jul 2025 00:17:56 GMT  
		Size: 167.6 MB (167589980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d954ab622638b81a76f8faca7f27cdbead519ce4a96bfe58ce0ce8c04de4c07c`  
		Last Modified: Wed, 02 Jul 2025 12:59:39 GMT  
		Size: 245.8 MB (245792866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:533dd51110aa122013299169d3241c8ff7b0a167ac026488a451cc3cf5a32242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15274640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43196c04d844d43946f4c7a75dd78f798c69fa8488debfc89ba320795b1e927b`

```dockerfile
```

-	Layers:
	-	`sha256:652198c66ccabc1746f6054da6a0b040aa11e579f227a638a7db763062f6b11e`  
		Last Modified: Wed, 02 Jul 2025 11:44:40 GMT  
		Size: 15.3 MB (15263315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9c99c87037228c8be536fc6fd298ab2a611a1fbd6a3d52d733fb4a29c90c2d`  
		Last Modified: Wed, 02 Jul 2025 11:44:41 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8b22455a7ce2adb1355067638284ee99d21cc516fab63a96c4514beaf370aa94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.2 MB (487172791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc77b2b3e794e11c9031f129feea6f9dd3649f86a9b70ad373910e70e5761458`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5424250d141bf5f4ec62e698bba9b5695482a3015186d3b14a633da8916bf7dd`  
		Last Modified: Tue, 01 Jul 2025 06:52:24 GMT  
		Size: 15.8 MB (15750716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7766ba090abb327ecb7e9e14ac90bbcc45c5ba6bb8a568ae531c960ff1acad55`  
		Last Modified: Tue, 01 Jul 2025 13:29:45 GMT  
		Size: 54.9 MB (54855722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1801db58ebce0297c6d03187f6e882ae0b8ba8838f3e18a17f3bcd9137be277`  
		Last Modified: Tue, 01 Jul 2025 20:13:40 GMT  
		Size: 190.1 MB (190053793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714498f74a0f367b5e69c9e7e3bd688c25db146ed8b97acec1446cb2218e705`  
		Last Modified: Wed, 02 Jul 2025 06:40:03 GMT  
		Size: 174.3 MB (174260306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e2730dd90c1b51e30c613c774511479688800225d93c02bdaf36189e99891fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15477294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b9b0c706b4ad223660013177c4a118765a26d87add26bb8babfbdf979efb1d`

```dockerfile
```

-	Layers:
	-	`sha256:12453b011a0f7bb3aac0c83948f50551f0d4d5ae1b1e0c7c3a472d44e1f5c7da`  
		Last Modified: Wed, 02 Jul 2025 05:44:46 GMT  
		Size: 15.5 MB (15465942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccba5cc2249b25264628303f496f30cecf3ead2e13e1dc3399d7f98b1951ce12`  
		Last Modified: Wed, 02 Jul 2025 05:44:46 GMT  
		Size: 11.4 KB (11352 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-bullseye` - linux; 386

```console
$ docker pull rust@sha256:2aaf00b554cd4ff148c16a3e58146641b87aa7c629bbb67c6731554afa3c2d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 MB (556215637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab21c61c4d19a041fcae82560e48bb7233059e80ef65189d4d830b0493e23dbc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113be81052ec8e8323c4db158dc9c99295355934e950a6367e5c27038fd1e04c`  
		Last Modified: Tue, 01 Jul 2025 02:24:43 GMT  
		Size: 16.3 MB (16268907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05b439f6df174e28bd21dc59eead603def3bcbd47ec6462f86b7758c4db6ef`  
		Last Modified: Tue, 01 Jul 2025 03:19:57 GMT  
		Size: 56.0 MB (56049937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d170ad31938c07c5739c923eaf5f7569c644e2ea2ead929bbc107d7eac895f78`  
		Last Modified: Tue, 01 Jul 2025 05:11:30 GMT  
		Size: 200.0 MB (200043566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7271fc5f55db8e0b012c06b0785adf36c8ade5d9f290c40fa07be956a5eecde`  
		Last Modified: Tue, 01 Jul 2025 13:00:23 GMT  
		Size: 229.2 MB (229163293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3cb1daa21e1c22f0ea3d5100504d1da2f45a788bcf4f0c42396ea073969b5df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd9075c8dc525761d3e7cf32a7d172eaaee78ecc359ee8f83da3b6bf52859ef`

```dockerfile
```

-	Layers:
	-	`sha256:4ba2cd6c29aab7b896485ed38a1fc73dd8448a29ef9bf4744495334a3e930f89`  
		Last Modified: Tue, 01 Jul 2025 08:45:13 GMT  
		Size: 15.5 MB (15450673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8861a1fd041f7cf768c0ad3c6f4dc87d554c6bcb084c979d61f7a6af8ff9a715`  
		Last Modified: Tue, 01 Jul 2025 08:45:13 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88.0-slim`

```console
$ docker pull rust@sha256:1c7eb658b16d48458a4808f15de8264a3c20d449d0cabdae47654d98e9dcecfb
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

### `rust:1.88.0-slim` - linux; amd64

```console
$ docker pull rust@sha256:b0c0357c60eca8fe29b8280974a44483a28319278a5ff5c57b3e7e9c5708f643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbda49f92a1f159dfbe623e790c2a5b9c1c6c3ba68bd9e362679a9cb48c4925e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff2b7b26c381c0c4ba90768f39bf5193252f27f4e625debf008d09438b195ef`  
		Last Modified: Tue, 01 Jul 2025 05:08:00 GMT  
		Size: 275.8 MB (275821106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:ade5b81bacfe5c6c7e52b85eafa1965c8ff433a6b2c5dbe95ffdac9b636a4098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a4805359ec86648c4fa15446b7df199cdb6a6e1a03490dcb11b527cd557473`

```dockerfile
```

-	Layers:
	-	`sha256:7df8be7b6f1e71053bb68baafbd18a0da5e3196678a329e5267ab3a5a709ffd6`  
		Last Modified: Tue, 01 Jul 2025 05:44:31 GMT  
		Size: 4.1 MB (4094552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a712f57ad2be1eb1eb0de48182654c5bcff269ed26b9ac1f7e737790730b63d`  
		Last Modified: Tue, 01 Jul 2025 05:44:32 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:85f37f11d046da1808026326b03493679b5d14c2f0f4523cf5bc8d5cc0e0ee0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317565661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7f9b3c433121c615480c6153d82080be95a30629221317a4cea09c08b0a573`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4db19ae3ab5266032020a2b07eb5414e4e5af2ea274e14d76e0e545b488f04d`  
		Last Modified: Tue, 01 Jul 2025 21:04:24 GMT  
		Size: 293.6 MB (293626917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:f5c7c3079e6be98cf7906e069b6a07af60bc9f5410e2deba15738732d1776661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b45c40a162ec803cc4480e1a932c1658154fae9d07c32b6cd1ff7053f34a7f7`

```dockerfile
```

-	Layers:
	-	`sha256:c7b3d0ac3ecfb43b93f6888077022d4165a1bd97012372bb37d32a5e2e76ccde`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 3.9 MB (3908981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd6ab2ec5e6066af386464396673a5d060f5b1a51cf8099cafde5bf8cb46451`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:35d3b11bbc6b7f45a174551689621906e5785d4e6e79f2aa3b4ace967a97a055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268179917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1880617faa9ea5bc0df720923e7d75c521d91fc7a3583e3360d6068d359c2b84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e130c413bba66f1a532f016096e1ca99fc7921a6d03f4ae5e7eef4f9de7197`  
		Last Modified: Tue, 01 Jul 2025 14:52:04 GMT  
		Size: 240.1 MB (240102239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b42e61db7f4c7471a71877c4a53f4d0391e7954c21dc20f7a3973cec0a2e7057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd222f432ceb8c15e86b58486cf5fd9c4582036ac9dcb8cede1be44821594ae1`

```dockerfile
```

-	Layers:
	-	`sha256:4c92de7432ff997c7c9d6fd67c06d2e50d70c9800c27e05fa0d04b2dcc4d42dd`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 4.1 MB (4116896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d1589208f0a8f59560905b8c36a4c4ecf08601526c55cbaaabc4a10846fb78`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim` - linux; 386

```console
$ docker pull rust@sha256:ff6fcb7ad6293f4a4c28db122754d93e024b99ca56a9f5027ddced08234ef721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325992228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4eb540ded896f027e6b1931f38d7618a4364b4643343cf6a82ef2de0e775e79`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3f2ceb310dae022b26d227eecca523fe07e1383bbc8cf746de0a949d9a3650`  
		Last Modified: Tue, 01 Jul 2025 06:01:36 GMT  
		Size: 296.8 MB (296779796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:310296d66708c74b8f7df786253dabb1763763f3ae996499d228c97b5defc6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad4a9c0226f971d47fbf4e1e3b0972b7052bb0257233fab74bc5c4b8783fb1e`

```dockerfile
```

-	Layers:
	-	`sha256:2a6a2a00284fbce671a5f0f7c61ebfbf8c2d5771cda8a1bd5445be27b699d096`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 4.1 MB (4073915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d875623e01bac8366b22e9a8bf9378721a880661602db1d20b97da37bd0c7c2a`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:e00cab06ebef6d7bb5580cedac63b15bf337fd68225ac6a152bdeb1d08bca552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374561374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8452adee592dd5981efa36540ccd9dd66cc2273fd2272ece300389cc198997a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a95af4d06128b392493eba88f8150c9e90691be1c0f0e8024d5929b44de3930`  
		Last Modified: Tue, 01 Jul 2025 13:00:07 GMT  
		Size: 342.5 MB (342488554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:ad4355591f63f7acdbf5366f8fb6d2241920c664d093c0327bd30a320b228ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687a2175e85119fb64fa7d37bd7720459fed5f9513594f53bbddccbef9cbce8d`

```dockerfile
```

-	Layers:
	-	`sha256:b40dd3069d53ab3fd2d2a8604ee2b563e69d54a6f2f4e29cd2f5cb441d80ae60`  
		Last Modified: Tue, 01 Jul 2025 11:44:38 GMT  
		Size: 4.1 MB (4066865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44f89002a1ae239b997acfc875a4c4a4fc8423278688b1ec444ca96cf66b74f`  
		Last Modified: Tue, 01 Jul 2025 11:44:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim` - linux; s390x

```console
$ docker pull rust@sha256:1cf72ceabd44d186a6f08948bad51ee0050ed17cb47657c6b74e1e879451a34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360392180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871910d1ab2a752b966ffce7ec56ab4866c791bce0f9fc075cb26d7744e75884`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8a3025335a2a160722cb689b6c389f0316ea4b027c2dad34fef52df858c365`  
		Last Modified: Tue, 01 Jul 2025 10:42:01 GMT  
		Size: 333.5 MB (333504369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:d04b9fa09c2d16e830240aaa30f0b46002ffc117461d7109c104bd5c6732a461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6791cd1d0129cc03fe2cbcb7c2269397f8348bb85df5bd5b9a8e6575a8923e`

```dockerfile
```

-	Layers:
	-	`sha256:2a8e89592d0564890623c9199bb211483a145b510ce0c49afc579dabe00180f9`  
		Last Modified: Tue, 01 Jul 2025 08:44:56 GMT  
		Size: 3.9 MB (3932230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52770394e7f7570572f6a897500a0bc0f14d82302ff5f32b5db7076d7a67ab3a`  
		Last Modified: Tue, 01 Jul 2025 08:44:57 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88.0-slim-bookworm`

```console
$ docker pull rust@sha256:1c7eb658b16d48458a4808f15de8264a3c20d449d0cabdae47654d98e9dcecfb
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

### `rust:1.88.0-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:b0c0357c60eca8fe29b8280974a44483a28319278a5ff5c57b3e7e9c5708f643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbda49f92a1f159dfbe623e790c2a5b9c1c6c3ba68bd9e362679a9cb48c4925e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff2b7b26c381c0c4ba90768f39bf5193252f27f4e625debf008d09438b195ef`  
		Last Modified: Tue, 01 Jul 2025 05:08:00 GMT  
		Size: 275.8 MB (275821106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ade5b81bacfe5c6c7e52b85eafa1965c8ff433a6b2c5dbe95ffdac9b636a4098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a4805359ec86648c4fa15446b7df199cdb6a6e1a03490dcb11b527cd557473`

```dockerfile
```

-	Layers:
	-	`sha256:7df8be7b6f1e71053bb68baafbd18a0da5e3196678a329e5267ab3a5a709ffd6`  
		Last Modified: Tue, 01 Jul 2025 05:44:31 GMT  
		Size: 4.1 MB (4094552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a712f57ad2be1eb1eb0de48182654c5bcff269ed26b9ac1f7e737790730b63d`  
		Last Modified: Tue, 01 Jul 2025 05:44:32 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:85f37f11d046da1808026326b03493679b5d14c2f0f4523cf5bc8d5cc0e0ee0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317565661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7f9b3c433121c615480c6153d82080be95a30629221317a4cea09c08b0a573`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4db19ae3ab5266032020a2b07eb5414e4e5af2ea274e14d76e0e545b488f04d`  
		Last Modified: Tue, 01 Jul 2025 21:04:24 GMT  
		Size: 293.6 MB (293626917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f5c7c3079e6be98cf7906e069b6a07af60bc9f5410e2deba15738732d1776661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b45c40a162ec803cc4480e1a932c1658154fae9d07c32b6cd1ff7053f34a7f7`

```dockerfile
```

-	Layers:
	-	`sha256:c7b3d0ac3ecfb43b93f6888077022d4165a1bd97012372bb37d32a5e2e76ccde`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 3.9 MB (3908981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd6ab2ec5e6066af386464396673a5d060f5b1a51cf8099cafde5bf8cb46451`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:35d3b11bbc6b7f45a174551689621906e5785d4e6e79f2aa3b4ace967a97a055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268179917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1880617faa9ea5bc0df720923e7d75c521d91fc7a3583e3360d6068d359c2b84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e130c413bba66f1a532f016096e1ca99fc7921a6d03f4ae5e7eef4f9de7197`  
		Last Modified: Tue, 01 Jul 2025 14:52:04 GMT  
		Size: 240.1 MB (240102239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b42e61db7f4c7471a71877c4a53f4d0391e7954c21dc20f7a3973cec0a2e7057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd222f432ceb8c15e86b58486cf5fd9c4582036ac9dcb8cede1be44821594ae1`

```dockerfile
```

-	Layers:
	-	`sha256:4c92de7432ff997c7c9d6fd67c06d2e50d70c9800c27e05fa0d04b2dcc4d42dd`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 4.1 MB (4116896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d1589208f0a8f59560905b8c36a4c4ecf08601526c55cbaaabc4a10846fb78`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:ff6fcb7ad6293f4a4c28db122754d93e024b99ca56a9f5027ddced08234ef721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325992228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4eb540ded896f027e6b1931f38d7618a4364b4643343cf6a82ef2de0e775e79`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3f2ceb310dae022b26d227eecca523fe07e1383bbc8cf746de0a949d9a3650`  
		Last Modified: Tue, 01 Jul 2025 06:01:36 GMT  
		Size: 296.8 MB (296779796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:310296d66708c74b8f7df786253dabb1763763f3ae996499d228c97b5defc6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad4a9c0226f971d47fbf4e1e3b0972b7052bb0257233fab74bc5c4b8783fb1e`

```dockerfile
```

-	Layers:
	-	`sha256:2a6a2a00284fbce671a5f0f7c61ebfbf8c2d5771cda8a1bd5445be27b699d096`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 4.1 MB (4073915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d875623e01bac8366b22e9a8bf9378721a880661602db1d20b97da37bd0c7c2a`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:e00cab06ebef6d7bb5580cedac63b15bf337fd68225ac6a152bdeb1d08bca552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374561374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8452adee592dd5981efa36540ccd9dd66cc2273fd2272ece300389cc198997a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a95af4d06128b392493eba88f8150c9e90691be1c0f0e8024d5929b44de3930`  
		Last Modified: Tue, 01 Jul 2025 13:00:07 GMT  
		Size: 342.5 MB (342488554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ad4355591f63f7acdbf5366f8fb6d2241920c664d093c0327bd30a320b228ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687a2175e85119fb64fa7d37bd7720459fed5f9513594f53bbddccbef9cbce8d`

```dockerfile
```

-	Layers:
	-	`sha256:b40dd3069d53ab3fd2d2a8604ee2b563e69d54a6f2f4e29cd2f5cb441d80ae60`  
		Last Modified: Tue, 01 Jul 2025 11:44:38 GMT  
		Size: 4.1 MB (4066865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44f89002a1ae239b997acfc875a4c4a4fc8423278688b1ec444ca96cf66b74f`  
		Last Modified: Tue, 01 Jul 2025 11:44:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:1cf72ceabd44d186a6f08948bad51ee0050ed17cb47657c6b74e1e879451a34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360392180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871910d1ab2a752b966ffce7ec56ab4866c791bce0f9fc075cb26d7744e75884`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8a3025335a2a160722cb689b6c389f0316ea4b027c2dad34fef52df858c365`  
		Last Modified: Tue, 01 Jul 2025 10:42:01 GMT  
		Size: 333.5 MB (333504369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d04b9fa09c2d16e830240aaa30f0b46002ffc117461d7109c104bd5c6732a461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6791cd1d0129cc03fe2cbcb7c2269397f8348bb85df5bd5b9a8e6575a8923e`

```dockerfile
```

-	Layers:
	-	`sha256:2a8e89592d0564890623c9199bb211483a145b510ce0c49afc579dabe00180f9`  
		Last Modified: Tue, 01 Jul 2025 08:44:56 GMT  
		Size: 3.9 MB (3932230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52770394e7f7570572f6a897500a0bc0f14d82302ff5f32b5db7076d7a67ab3a`  
		Last Modified: Tue, 01 Jul 2025 08:44:57 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88.0-slim-bullseye`

```console
$ docker pull rust@sha256:12d9a0ff4f3c87badbf56a27ffd6c4774ebe1b5fe5c6b7b1a39cfee537fcb62f
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

### `rust:1.88.0-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:fc66d738f64bca39b62f4a8602bce8239a58d813a073dec6eb87c26ed46190c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead6f32afcd0798a56c170ce2851030ab2ae5772cc7aaaec8b47346331cd33a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d114182f83d2bc4d73e02cc5bb74bda2938943a605a1efe8e8e5921a9334c06b`  
		Last Modified: Tue, 01 Jul 2025 04:34:37 GMT  
		Size: 265.2 MB (265206650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f2b2479ca7328f021feef75a9a45f117ffc3ee13a53990561c1dde6401e77ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e7b91d95fa7f94247595b016c4b0afdf5c4568be554c642efa57ecedd45917`

```dockerfile
```

-	Layers:
	-	`sha256:17df34ae2e3f1174c3451942d63bf066080013096af8da1c1fae497282282c74`  
		Last Modified: Tue, 01 Jul 2025 05:44:38 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86c3b78ad1853f15af29c20213d59684bc1b948a20593345e4229e0c91d938ac`  
		Last Modified: Tue, 01 Jul 2025 05:44:39 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:2a8251a939f0d13ed2a1ea24d1f9ef251bbbf030d520485b394de2b9c23f1575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313623477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b182ed292d4c08791794619177de2b422b06a63b5f34f388d6e1f7c828ccf4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:96b51e81cdb8508366118f41a9ec499f52f0d0211b084d5d516e1be131b35266`  
		Last Modified: Tue, 01 Jul 2025 01:15:21 GMT  
		Size: 25.5 MB (25544163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e8ad713014c96437118acd9656b3f10b47964888722c469680e6042510ccb`  
		Last Modified: Wed, 02 Jul 2025 00:48:15 GMT  
		Size: 288.1 MB (288079314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d16acf27c46754346860ce745ea5760b105c162694adc9d454c94f795a796f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2cfe874064a2b600d64ab76c2b059316a0d09778b241f6d9ef1fe2850a3e56`

```dockerfile
```

-	Layers:
	-	`sha256:08e8559715569c50dc0f3e68ebbed15841af5fa459ca720c38fa15b3c2a035d4`  
		Last Modified: Tue, 01 Jul 2025 20:44:41 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffbb508550ec246d38153bd7938e330e200f9c02ca0f0d1d4b1abcc527101490`  
		Last Modified: Tue, 01 Jul 2025 20:44:42 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d7bf42de9bb8c46335f1541a795bd167560ad0c7d211e67cad3f5a7417243fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258705512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28cce79db40ab1d0fa12cbfa105d6ef1dff13b63c1a93b8fb9e9682a0418a59`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4458b4f354b132ede276e7da54a33c211b23ceac4f34da5ed2b7fae09bb95d6f`  
		Last Modified: Tue, 01 Jul 2025 14:45:32 GMT  
		Size: 230.0 MB (229961372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f8cb1c53bc02e47f1e50499e70854d43e2f98ddf439fa5b52d34a6424733aed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f09370c05fb448311182a49164c612c0299712281c47b1564078e73ebb6a67`

```dockerfile
```

-	Layers:
	-	`sha256:263fa190fe34f81500ba2e8ac8bf53f05869282f02579d474166a6be2567d51c`  
		Last Modified: Tue, 01 Jul 2025 14:44:39 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a44a181f21adc0542d1acb35f17b1f20343532cfd22efc73efb5044556e05115`  
		Last Modified: Tue, 01 Jul 2025 14:44:39 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:6aeeeeaf3ed73638e4135dce21527f418f6a192d3e2de9c4d26664694f90c0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.1 MB (321133034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e7dcea35fc6893afae54fc7ac2446ea032b06889451f72c5fb09918d9ba66c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:40be1da6146972d9df50a98eef7b5c0f729cd95a3a38782418f354f3b9355a9a`  
		Last Modified: Tue, 01 Jul 2025 01:14:57 GMT  
		Size: 31.2 MB (31189680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e1a302797c6fe4ad387e823eb711877bfcee5af925dcfc3decc2b4083fef72`  
		Last Modified: Tue, 01 Jul 2025 12:59:38 GMT  
		Size: 289.9 MB (289943354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8c4db6ccf78a02913434449b05bc26924375a6fa2a57e1fb8cdc0a9149a6128d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60622052414fe9b2982743aeebbe224601c12752ff8f4cbe89d50b54c59a8ad0`

```dockerfile
```

-	Layers:
	-	`sha256:423e3a39660d3cd9304a2f3cd9a7f0037ec79d19c72661b55bb7ed8a8d78a9ad`  
		Last Modified: Tue, 01 Jul 2025 05:44:54 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a0678dc17cc916be60884c0469158c1664b2dcd59755d390b82d7f534f97fa`  
		Last Modified: Tue, 01 Jul 2025 05:44:54 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88.0-slim-trixie`

```console
$ docker pull rust@sha256:e68d2ba3397c3c04c47647ad5d615afaca80ae00dcc4f5140e43495c537746c6
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

### `rust:1.88.0-slim-trixie` - linux; amd64

```console
$ docker pull rust@sha256:7721d2705af97fbfbf241d1f329e1e7144cb2743b2ecac5711352c8ea4fe3251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310236807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0d0605178c491bdb2bc093d06776322acffdddadb8d6b3ae47a7aba111cc68`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2b9064154c24154965e1b574cfe4999144b627db7f678b3a566d3eeeac02dc`  
		Last Modified: Thu, 03 Jul 2025 20:42:04 GMT  
		Size: 280.5 MB (280475701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:d619583f10fabd5f99a621389b8e4043ffa188cbd8eb305b7c2e7e8f2d63ed54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89914cf1279171e30ef2a59799b98b1a4e83babe84c87f1ff92ef591c7fc3ec`

```dockerfile
```

-	Layers:
	-	`sha256:c1e52b080a5caaa75906ac1aef51b1a4e5905284978a04a29d5def27fdaceafb`  
		Last Modified: Thu, 03 Jul 2025 17:45:05 GMT  
		Size: 4.2 MB (4162901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d4390982a55f7e70f969a7af51b2b195f34be5ebbe6c6f17d939bb524e497b`  
		Last Modified: Thu, 03 Jul 2025 17:45:06 GMT  
		Size: 12.1 KB (12061 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:57b1df7d4a1e8b0b231b0e8a09ae0cf89c7939542d2f1e1ff4a05f7de70f2a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322260431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a609326c1f09c4e6aa554b61b16080a0783429c62de582cd5e3ec4188913f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75cb2c2919cdd5f70bd8208e02191091cad32dd857e56bfd33f35cd6d531c82a`  
		Last Modified: Tue, 01 Jul 2025 01:18:55 GMT  
		Size: 26.2 MB (26201517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49ee1c5650c50a45b3eef84571458d78cbbf30fc06a0035bfa2a082ea8108d9`  
		Last Modified: Thu, 03 Jul 2025 20:48:22 GMT  
		Size: 296.1 MB (296058914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:cc54c83fc01e12d9d41cfdac572a59e588a4c54287deec7161e4b89d69757700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103636073af3a7f76abb00f7559b02484569bf5618ed3d571538a7ca3b02fc19`

```dockerfile
```

-	Layers:
	-	`sha256:ffce2eaa705d9368bce2a80cd6890bc3c2bf66295174b466a2007a02c4370d2b`  
		Last Modified: Thu, 03 Jul 2025 20:44:36 GMT  
		Size: 4.0 MB (3967745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb0ae2602c3fab378c0fcb74ec00c46711ce55c947b8f99952dd9d8fcae5488`  
		Last Modified: Thu, 03 Jul 2025 20:44:37 GMT  
		Size: 12.1 KB (12138 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:88a9c0d2b3c1ef6e0ab769f130a15a6cb2d10ed82ac6c779e1d5b543fa6a5a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274045556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47d037deb756e369db48be32af79a4b9410405268eb60580dffcfc577e67aad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:dfa10e860e0106510a14bae8331a4dd762d3d3737fdba0dbec102458f9853b71`  
		Last Modified: Tue, 01 Jul 2025 01:18:18 GMT  
		Size: 30.1 MB (30126864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab982be4b2f9d93ec333ffb69526256503de560bde0bd8a510e3b1acf793c40`  
		Last Modified: Thu, 03 Jul 2025 20:49:17 GMT  
		Size: 243.9 MB (243918692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:ec6e0fb8e467b4d66a4e91bfc44764be1efadf6791fcd25f1df5437d48d299dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a618e7a2fe30262bf7503eb5b80999a202d3e87df932a890048ca1fcb3b7b55a`

```dockerfile
```

-	Layers:
	-	`sha256:a7390525f3e02590517ad48faeb0649b52dd80e6a083feb652819a8c0320984b`  
		Last Modified: Thu, 03 Jul 2025 17:45:23 GMT  
		Size: 4.3 MB (4254069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad846470cf4d23ec2c6804afdf350c7808432e565fc39d3035fe1556cf21361e`  
		Last Modified: Thu, 03 Jul 2025 17:45:24 GMT  
		Size: 12.2 KB (12165 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim-trixie` - linux; 386

```console
$ docker pull rust@sha256:6fe11019a3d4d7e50e48f4727120357e98b6e3242ea944d72f20a57ccde3976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332943226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c31842ba66bed838d3be4cddc274c3b25d4f5c056d036b9d9c5646f2f83c35`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:27b0922c0fcc2ccb534e806841adaba77d7b1a639b51fa3d953ccfa3af3a57e6`  
		Last Modified: Tue, 01 Jul 2025 01:14:55 GMT  
		Size: 31.3 MB (31281109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfea6381854ff5a1288e44fcd71c127bf8f5c12b73fca05a53a0fdf766da33e`  
		Last Modified: Thu, 03 Jul 2025 20:49:34 GMT  
		Size: 301.7 MB (301662117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:709dfc3e62d11137fe59c004c57be56ba78c0370578c39fc986245bcc924fd3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d862b9c54929822ee442cfebc6bb3152f1e05190d3476d52017e9c30cbe3777`

```dockerfile
```

-	Layers:
	-	`sha256:d76b88999182b5b6e9bf50bf33640536dbe258725e8c01c0e11481b295d36251`  
		Last Modified: Thu, 03 Jul 2025 17:45:49 GMT  
		Size: 4.1 MB (4136434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff406b796b327df9d21a85be2fa42ed6e856e504634069cad7fdc6a139e510ad`  
		Last Modified: Thu, 03 Jul 2025 17:45:49 GMT  
		Size: 12.0 KB (12030 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim-trixie` - linux; ppc64le

```console
$ docker pull rust@sha256:cbef1f31e6e9d539b5e201653bc0553eadee350cf0a81efd0bdc75654187d7c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.2 MB (374189714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fe51377754a44b3b68c6389474ced3297711aa727c85fae16272f257d4d87f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05113943712185aeb07e0e0bfb3fa35e088bd6f08df1e776cc806f8bddc6db1`  
		Last Modified: Thu, 03 Jul 2025 20:50:14 GMT  
		Size: 340.6 MB (340603679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:03e00179fb0709f08bca4819fb0a5100a86a4f3d137fc7e3dd77ed4fb2bb5f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fb1b4f2f8d43288ca62d234578bbfb1d9527b44d43b4e8790007f3e694af6b`

```dockerfile
```

-	Layers:
	-	`sha256:187a0b4809cba5785eef2febd443d1c4537bde12b677052c85f9367e5c060989`  
		Last Modified: Thu, 03 Jul 2025 20:44:49 GMT  
		Size: 4.2 MB (4158025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79ae8b64b453a46d0ae29840bdd1a9e8658feec181cb272ffe4e3c012b5e5bb`  
		Last Modified: Thu, 03 Jul 2025 20:44:49 GMT  
		Size: 12.1 KB (12106 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-slim-trixie` - linux; s390x

```console
$ docker pull rust@sha256:95bd23402ed6a90153634a026962a9c6cb52036c619765e75882d1401cc2b899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.6 MB (365571899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a7d73fb037181cda5b98fb9704a92758f96457c24664ac81eb41524bc2a693`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:728fbd29b8599bd56dcb8703b5c428523bcf0f3d48c5e95804f60267a128a3bc`  
		Last Modified: Tue, 01 Jul 2025 01:19:25 GMT  
		Size: 29.8 MB (29838345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1456ed2701051abe37f5ce865394b5d3d701095089b1c134b195eebb09d77cb`  
		Last Modified: Thu, 03 Jul 2025 20:51:48 GMT  
		Size: 335.7 MB (335733554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:b3db53400e5e90db3bf6bafadf7ed5ba7942e99fdc2b1f29db7d9338241b026a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717ea3ea743c46facb7642e47482c5e4e2469868c735a4096c86797b8e34e0a4`

```dockerfile
```

-	Layers:
	-	`sha256:f44d67311a40081884ea925705988428fd00e3afd55d1da73c10871c627143af`  
		Last Modified: Thu, 03 Jul 2025 20:44:54 GMT  
		Size: 4.0 MB (3980649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e254e26728aaa08e68b3041c15896d2bbf46234e284651a8ca903e32d7f2794c`  
		Last Modified: Thu, 03 Jul 2025 20:44:55 GMT  
		Size: 12.1 KB (12062 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.88.0-trixie`

```console
$ docker pull rust@sha256:b730c57c4c1679f1c847f0481ba8863a15d00cae22d367a7565f4422bf40d478
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

### `rust:1.88.0-trixie` - linux; amd64

```console
$ docker pull rust@sha256:777127bd6a86eae87d512c696f1b5d500307cae84a4b948e4b25942516d780ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.5 MB (583494432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392aa965c60a10bdc5365931c80308a245dfea6cc9bbe1aa073fb9cbb6d5c274`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13567152126a6abf6e98a928a4206f022be687e979bd113ce89b0b1f41fcbaf`  
		Last Modified: Tue, 01 Jul 2025 03:19:07 GMT  
		Size: 25.6 MB (25617737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f696393bed22361a2f932d3f084750c0cdf7e1f7186888c327230081e6257b0`  
		Last Modified: Tue, 01 Jul 2025 04:12:14 GMT  
		Size: 67.8 MB (67789682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b76da92f9efb17dc4a68c682bacce1ec791a87b62ee76639b08bfc2ee4577cd`  
		Last Modified: Tue, 01 Jul 2025 12:07:57 GMT  
		Size: 235.8 MB (235764377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9b092ebb229c418b5f5feea9ad11427731515a1d8dbf01adb95c1959d6bac6`  
		Last Modified: Thu, 03 Jul 2025 20:41:59 GMT  
		Size: 205.1 MB (205058759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:8568cd48443fa4a0c33851892d9da52f3d656b2399dcd83e6ea414378cb1e83b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17214539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06eb85b483e6f006b4ae1adf7622a1abf1ed4b6581de2f1824c28c05b4fafb0`

```dockerfile
```

-	Layers:
	-	`sha256:3e339bf185a305476f2c298204c80a4fa1d966d3dea7c9964a8704dd8772bff2`  
		Last Modified: Thu, 03 Jul 2025 17:45:24 GMT  
		Size: 17.2 MB (17202584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4abb423fff15f1c22361c92de405fb0ef8a88535b600fc76d86d707b3b09260`  
		Last Modified: Thu, 03 Jul 2025 17:45:25 GMT  
		Size: 12.0 KB (11955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:f0d61b9434bb38e2fc365679bf6ca2b15ac36a477ee4488bca51ab2432ded2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.7 MB (570716850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e270a7c2c6520ab1bc80e5bf40b5af01074724375045b6d1103cd5fab68e50`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0611a9c58dddfe7f00bb5fe6c8f5ccecfceeb1785acc68dc070068a94adf2092`  
		Last Modified: Tue, 01 Jul 2025 01:18:31 GMT  
		Size: 45.7 MB (45708080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571abb678dad668afa2696a67ffe4981c3b5aeb37fa4c14a0cc24fdac7949b6e`  
		Last Modified: Tue, 01 Jul 2025 08:59:50 GMT  
		Size: 23.6 MB (23617932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd28b3d9ecc5ff8b97a4e765e8a818c8ca6ea137650adb3df7d53acf265e9e4e`  
		Last Modified: Tue, 01 Jul 2025 18:31:52 GMT  
		Size: 62.8 MB (62760034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7255cfd7fa333e12d9432924dd0af6dceb8b6fca12f12faa2b5157b7e9cacc6`  
		Last Modified: Thu, 03 Jul 2025 10:55:31 GMT  
		Size: 192.8 MB (192838492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990aa9e5561becb9a9a31b185a40c4e082059b4a2f864a5ea4a0c72aa5306a5`  
		Last Modified: Thu, 03 Jul 2025 20:42:55 GMT  
		Size: 245.8 MB (245792312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:6eaf53d99ce3e71a7ea943eea06e0b1786528694755a32e99ac4ee29064aa755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16982621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8631aabd5bb545bf8056ef9539ea5075a0a8067a69adf2344dc7f33f9dcfbe7`

```dockerfile
```

-	Layers:
	-	`sha256:e1b2e6ea0d58fef7a142159e950d4cd70fad767db1159baa5d2ca9e850c1b39f`  
		Last Modified: Thu, 03 Jul 2025 17:45:54 GMT  
		Size: 17.0 MB (16970590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895c99ae34ac4942be372edd159f3a98dfcc60436b134a088738443b03f4f306`  
		Last Modified: Thu, 03 Jul 2025 17:45:56 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7c5ac5114acbafb83337d764aadd88ca774223507a916c6dd30bb082a20ec7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.5 MB (542536176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0697dd2649fdc7fa59d4cf781665f05caae4122011784ccef9a0f023a0570c48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064b8e4cb92aed27a99de363dac49c85bcb74d556fa925c921727dcdf03f7cb4`  
		Last Modified: Tue, 01 Jul 2025 06:53:32 GMT  
		Size: 25.0 MB (25008002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01789681d750567cf92706d649b58054ae1e27e35947e671160777a30538c3a2`  
		Last Modified: Wed, 02 Jul 2025 05:58:28 GMT  
		Size: 67.6 MB (67611970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4fcde14125f9212ba8ee255667590e6596810c45bdc694a8db749d7ff6d2bf`  
		Last Modified: Wed, 02 Jul 2025 06:00:35 GMT  
		Size: 226.0 MB (226025553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65018ead03f0d4f0382753ee911bff501d98c7ce180a3aabfb426c24deef1054`  
		Last Modified: Thu, 03 Jul 2025 20:12:11 GMT  
		Size: 174.3 MB (174260497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:5fd381b02f79c5c1f30501a2e74b4143d494518193a407ab4bd263d5d4495b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17298951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960a72fcf1731c737694fba1d68b27e7546e2cafa11ed72bdf7a1711136c2ca5`

```dockerfile
```

-	Layers:
	-	`sha256:beca260f3051e49975118b198c4e96523199398c5bfe36285d4ffc2c15e5afe1`  
		Last Modified: Thu, 03 Jul 2025 17:46:11 GMT  
		Size: 17.3 MB (17286892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637b38306d48fc5fd76b15fe7b2603dc5a04735734490c149d9278c4bd7ef21e`  
		Last Modified: Thu, 03 Jul 2025 17:46:14 GMT  
		Size: 12.1 KB (12059 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-trixie` - linux; 386

```console
$ docker pull rust@sha256:d4508bf7617fc0667b9f76693bfb223e42469dc1abfd62bc4affcf61fdec1d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.4 MB (616411351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f713341993075dddfd01eb0a193e3e5a746dc11f9c4688e2c3c41ab15827a02`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d223755a7489df8352d3a71955e26d35281b9c0f0609e017af54d9e75e3b435b`  
		Last Modified: Tue, 01 Jul 2025 01:14:59 GMT  
		Size: 50.8 MB (50786756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d932d83e6c250bb0f5c2003ae98b3b4dc3d40d3915a7ebed763f315741368`  
		Last Modified: Tue, 01 Jul 2025 02:24:58 GMT  
		Size: 26.8 MB (26772148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34925744005802787be957c67125f2aabf94afd5e8609668cc037c46d09591`  
		Last Modified: Tue, 01 Jul 2025 03:20:07 GMT  
		Size: 69.8 MB (69830306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f64900f9b3ef26b18f567a74a96e250e42a8eed2ff1fadd54a41cc0359ad74`  
		Last Modified: Tue, 01 Jul 2025 13:17:44 GMT  
		Size: 239.9 MB (239860428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786dd06ef0c1d508b04b744e9509815e8b97edb82567dae2ecc2f7f4608eb087`  
		Last Modified: Thu, 03 Jul 2025 20:45:12 GMT  
		Size: 229.2 MB (229161713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:f67a9186cf1554037b5bebdc2a29731e33b0560fb6f00acc72a972c06a6a8024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17182790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fa8116b6bed9af5ae6689a9a22779a1678697a915c5cd4d7e6b36066700e02`

```dockerfile
```

-	Layers:
	-	`sha256:0bc4ae22361d8be206beacebda88e0a0d9907d13fe49752729264b691a2573a4`  
		Last Modified: Thu, 03 Jul 2025 17:46:46 GMT  
		Size: 17.2 MB (17170867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00512048af2e89f74659ec4afeed8cb648de2fbc4c194e045bb7360d66547db4`  
		Last Modified: Thu, 03 Jul 2025 17:46:47 GMT  
		Size: 11.9 KB (11923 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-trixie` - linux; ppc64le

```console
$ docker pull rust@sha256:2b364c8eda85704eca9497cb33fca2d56eef23b799891c48db05140faffe245c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.9 MB (657910004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e48352ed179962dff629d52064abbff1ea21fc4849959f709243b2e442fae7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e868292aa714037cbba25d912564e5f392a5d355c383b03a8854e789c98ef`  
		Last Modified: Tue, 01 Jul 2025 05:08:57 GMT  
		Size: 27.0 MB (27003269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7107fc95f855d7880e921bbc85bf915f07c907c70d7d6f6a5334a32ad6c832`  
		Last Modified: Tue, 01 Jul 2025 10:12:36 GMT  
		Size: 73.1 MB (73068943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4744a5ce78804175c7109fb3df660a6bb53b2954bc5f2c48184739c714dfc8`  
		Last Modified: Thu, 03 Jul 2025 10:55:19 GMT  
		Size: 231.0 MB (231021360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c94c7eb559acad5a878c6b10fbcb0ecafad636824170be34ede5261baa6a2`  
		Last Modified: Thu, 03 Jul 2025 20:46:35 GMT  
		Size: 273.7 MB (273719196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:712f5014e1f676151678dfb32f438ebfc5c6ccce041ee1bfe0822c9f6e6a92b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17208092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e648406175ad5a0fff773fd402a380664ca93211dc1dc02b0e30ec1857290a`

```dockerfile
```

-	Layers:
	-	`sha256:e90c41129150eeb1baf61bb144eb1a5bf5136c3753a5e7ff747a93519edbced8`  
		Last Modified: Thu, 03 Jul 2025 17:47:19 GMT  
		Size: 17.2 MB (17196093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:223be277a3e6da23a3d10ec7c56a85066daeacf3199f6e2852aed61471673c6e`  
		Last Modified: Thu, 03 Jul 2025 17:47:20 GMT  
		Size: 12.0 KB (11999 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-trixie` - linux; s390x

```console
$ docker pull rust@sha256:b78680ff95452516a2a1ba080766115b52b09915350132aa95d221d83bb4a29f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 MB (634484977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b39c24e77ca6d3f82b32ead83f3c0c127e66c3c126e6397457389779e52ec7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8974c848015ae735631f879693069b8c536e3428274d79917837c027655a80`  
		Last Modified: Tue, 01 Jul 2025 05:31:56 GMT  
		Size: 26.8 MB (26785709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7360cccf58cfa285cf20d3ce14642c23bf3a2795b93396d0b9b743ee2e0779`  
		Last Modified: Tue, 01 Jul 2025 08:59:15 GMT  
		Size: 68.7 MB (68663824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694ce909d21b7fbf7c3fb87f40db93cf7588c89986fe25d341208d7b9ae60852`  
		Last Modified: Thu, 03 Jul 2025 10:55:27 GMT  
		Size: 206.3 MB (206329374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2362089a7d48f29102d6359bd8041b42be3e05af339f3916bfaefb996c680c`  
		Last Modified: Thu, 03 Jul 2025 20:47:14 GMT  
		Size: 283.4 MB (283362410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:f0605e4fb8dba38beea68b41893e3e6983c85a8d7ebe00d7b438ec8414f6d6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17001023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fec9741de5a55dec8253a44c86e746da1d1ec5db93d53031d57e5006c179026`

```dockerfile
```

-	Layers:
	-	`sha256:56417f7df327de8d5d5e7e0de1e2f59e7226739f9c6c2324cd0165abb66c39d8`  
		Last Modified: Thu, 03 Jul 2025 17:47:40 GMT  
		Size: 17.0 MB (16989068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bba5fb71a8222ba1b28462e4175f250445ba54f02cf3948e9d08d931e57d0ec`  
		Last Modified: Thu, 03 Jul 2025 17:47:40 GMT  
		Size: 12.0 KB (11955 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:ec0413a092f4cc01b32e08f991485abe4467ef95c7416a6643a063a141c2e0ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:b18203be0f58e16fe47250bf98bbe83c61bbfa97a0f5a94cebf34605bb000137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324842014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccfa6e07df925301f1f0b76b6784e617369e209ccfd7b16e76a3f50bca1e544`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c179a1cc9cc1626cd02fbb4866ee1705894a35d0acf8458e7f0274620ded46`  
		Last Modified: Thu, 26 Jun 2025 19:02:56 GMT  
		Size: 61.6 MB (61613765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b44eb86436bd74e3289f02e42ae2c9df9c6a39ac3ff054f893f7cbaddbcf08b`  
		Last Modified: Thu, 26 Jun 2025 20:45:29 GMT  
		Size: 259.4 MB (259431403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:3a48955a20cd88465d43306589af8be8e9aab9bc4983ebf983267397b0038f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8794bb5882365fcd697f232d90c928f4dfc42f2d9dee1f418d14cba22fc740`

```dockerfile
```

-	Layers:
	-	`sha256:4af3880faef85aba29ec3559478d1219bcd27ba3aa3e498970fa8eb110c9fbbe`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d7d4050c4275c54863ef9a56b9e59d3e338bc902f05df72abcbf103b3bf06c`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:43c5afb577aa21180b984fe215c836db0e8da8c6d6e29f4f5d60fcac8f6747e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324286625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037fc7bdc081378f949b34f5b57abb98ba2f2308d8e24c81eec1dc00f8095344`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe32611e1706eb5e71110ea02f0a43bcf8d9d5b31375d8372476ca0151ea4e79`  
		Last Modified: Thu, 26 Jun 2025 19:09:40 GMT  
		Size: 59.2 MB (59154287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd9ba9c44d35a05a92f10caaf51df4bf98f7cd9e90070d71790f3fa3de848fa`  
		Last Modified: Thu, 26 Jun 2025 20:48:42 GMT  
		Size: 261.0 MB (260996397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:f7f6eaadbe7a000ba5420c2ea8c78d7812aea2e2ba405d6f47c7dcc77af1c77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fcba7c7ba45a16b412de43acab6b32790c948a2de7b038009b4fe3f5344978`

```dockerfile
```

-	Layers:
	-	`sha256:0ece12c371cca20fa75cd9470ad9eb8f90b1172dae46baaf4940565722fcf88e`  
		Last Modified: Thu, 26 Jun 2025 20:44:43 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49231f16442a61f2a0b6140092b2b40d1a3786b17de63fc044fabaa5fbcee312`  
		Last Modified: Thu, 26 Jun 2025 20:44:44 GMT  
		Size: 12.1 KB (12084 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.20`

```console
$ docker pull rust@sha256:3ab9b805c8d2444f6f63f1ae7a38b5e04949d6b0d9e8a314e1ee3ad502deae45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:985c5bffc08709b4c04506340fcdc2542dfd0604070a993c409a6565e200c488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318374251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4468520ebd63f0d5993bf50e71ce97ce1770aee2cf170f4b68416cbd826434`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd8e343fc1e8b59389632b1aa1fec9897eb0d70d9a028c4953824eaca48506`  
		Last Modified: Thu, 26 Jun 2025 19:02:57 GMT  
		Size: 55.3 MB (55315554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af473c39e92f0a526585dfa175d2324b3bcc5653f1f8b4a0197290536a1a4b82`  
		Last Modified: Thu, 26 Jun 2025 22:03:51 GMT  
		Size: 259.4 MB (259431800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:6d1398d665e6f2fad6e604e6b35246a23905cff0473753ad60eee908c8602f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.5 KB (722503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ed6595279fc3b8ec29033696b6a0ff4d9c437f59ceeaf9052d8a7b745cac53`

```dockerfile
```

-	Layers:
	-	`sha256:172a379c01373f9fa6f1f7546d8f14ca43f16dbed174f0fb1038d9ad729985b4`  
		Last Modified: Thu, 26 Jun 2025 20:44:46 GMT  
		Size: 711.8 KB (711789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c520dac29e5f70b8c11a8c70a95fc0a3a9bb4ca3b5499c004ab4cf05e37e7ce2`  
		Last Modified: Thu, 26 Jun 2025 20:44:46 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bbc890fbb4cfe63267e61b157106ae17e22fea8965bd86dad3ba2895731fd832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.0 MB (318036721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2562e20c93fbfe25e95e223728ea45fdabb24f56872078249b32a94618aef470`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f73dbcfd8a123487699fe68590b2bd9f99926de28d20db07b032c7c04a77d5b`  
		Last Modified: Thu, 26 Jun 2025 19:07:09 GMT  
		Size: 53.0 MB (52950135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35f71611cb454ac5691276f7fb4f820ad5cca79bd33a16a47b3383d0199fd5d`  
		Last Modified: Thu, 26 Jun 2025 22:04:01 GMT  
		Size: 261.0 MB (260995421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:ffe59248eec0f167209f1689d76dc0cf65197edb7123968bab9d9736ed5dbe1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bf25ee4d7342c1573d066bf9d6490bc899c772b46d58fb99616651dff2a12a`

```dockerfile
```

-	Layers:
	-	`sha256:fb91044d3c55c5b9a10f560693a397817a79b1c3e9cac98794b2cc2378ddf88f`  
		Last Modified: Thu, 26 Jun 2025 20:44:50 GMT  
		Size: 747.7 KB (747721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619847fa4854614400d1faefbfd3dca469c0ddb922f14d8b21e0cfee7113e7b2`  
		Last Modified: Thu, 26 Jun 2025 20:44:51 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.21`

```console
$ docker pull rust@sha256:9c6a4baf58661f99a5441b15e3ad8295dabf35e849c4935e77ad35d9809be1d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:f76a41f6a9d96aca247c6789369bb5986c9faaef5d0ab080ae28346725d86c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324637733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd470e8018c4c8d13c36bb6d82b21b2b35e0cab903eaabfd2ba2cdbc0d49d8c9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a9008c78a14e56fc9106b9415625622b22d3e7d7ed88d4c9f168084a5b930a`  
		Last Modified: Thu, 26 Jun 2025 19:02:57 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99aa10cef404820ac909a9c36a9398af421599896d89f5216fe03a0484938cbc`  
		Last Modified: Thu, 26 Jun 2025 20:47:21 GMT  
		Size: 259.4 MB (259430674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:bfe3ce46af8506744eb91a950436d78f9b57aa1c89dab3f0c8cf5796a6964767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063fdf51672810ea7124832520f622f7d4a1bd29ff180e4e39b155177f6ce538`

```dockerfile
```

-	Layers:
	-	`sha256:bd239d1a7ba898b4e5db9276ef7089d6bd3dc5fbc114c96a656434c2b620e7a4`  
		Last Modified: Thu, 26 Jun 2025 20:44:52 GMT  
		Size: 782.6 KB (782619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68bd06a7d86815924cf9c1da819c34ded738a4b417cf24f9b33b853d7a3d1bb2`  
		Last Modified: Thu, 26 Jun 2025 20:44:53 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:390d7bebae8a355bd9e439bffd1f0f0124d0ade0a01602308b3c663490f66a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.1 MB (324089393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c931f5d71d48f4c73a17c302da0df6ebc23b15ced06b4f4ab775f1ec6e5228`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa43a6919f3e4298c4ac7012f740c568baceb922776f8df0f76856cc3ee4662`  
		Last Modified: Thu, 26 Jun 2025 19:08:40 GMT  
		Size: 59.1 MB (59101301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aad9f05f3e21035ae8f9c44b60e6bd73096afc6f6fa0e572587f6b65e6ece8`  
		Last Modified: Thu, 26 Jun 2025 20:47:22 GMT  
		Size: 261.0 MB (260995063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:03bf0509d1cc316b17044231bd28292d0828891ee21cde73471813fed5ee7435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (872990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eaca6f25dcca1d3f5272d1eef631f701b29c34b87f57293ddd1769d867a156`

```dockerfile
```

-	Layers:
	-	`sha256:263657c33753a7119953e3eaf32bfa7eb0f92250b29093be5e85cee6402a4952`  
		Last Modified: Thu, 26 Jun 2025 20:44:57 GMT  
		Size: 862.2 KB (862157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7daa109bbb3d9da7db18c495a2c43ac74998f6a27162c51bbc993b97bf68fa0`  
		Last Modified: Thu, 26 Jun 2025 20:44:57 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.22`

```console
$ docker pull rust@sha256:ec0413a092f4cc01b32e08f991485abe4467ef95c7416a6643a063a141c2e0ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.22` - linux; amd64

```console
$ docker pull rust@sha256:b18203be0f58e16fe47250bf98bbe83c61bbfa97a0f5a94cebf34605bb000137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324842014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccfa6e07df925301f1f0b76b6784e617369e209ccfd7b16e76a3f50bca1e544`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c179a1cc9cc1626cd02fbb4866ee1705894a35d0acf8458e7f0274620ded46`  
		Last Modified: Thu, 26 Jun 2025 19:02:56 GMT  
		Size: 61.6 MB (61613765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b44eb86436bd74e3289f02e42ae2c9df9c6a39ac3ff054f893f7cbaddbcf08b`  
		Last Modified: Thu, 26 Jun 2025 20:45:29 GMT  
		Size: 259.4 MB (259431403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:3a48955a20cd88465d43306589af8be8e9aab9bc4983ebf983267397b0038f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8794bb5882365fcd697f232d90c928f4dfc42f2d9dee1f418d14cba22fc740`

```dockerfile
```

-	Layers:
	-	`sha256:4af3880faef85aba29ec3559478d1219bcd27ba3aa3e498970fa8eb110c9fbbe`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d7d4050c4275c54863ef9a56b9e59d3e338bc902f05df72abcbf103b3bf06c`  
		Last Modified: Thu, 26 Jun 2025 20:44:39 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:43c5afb577aa21180b984fe215c836db0e8da8c6d6e29f4f5d60fcac8f6747e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324286625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037fc7bdc081378f949b34f5b57abb98ba2f2308d8e24c81eec1dc00f8095344`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe32611e1706eb5e71110ea02f0a43bcf8d9d5b31375d8372476ca0151ea4e79`  
		Last Modified: Thu, 26 Jun 2025 19:09:40 GMT  
		Size: 59.2 MB (59154287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd9ba9c44d35a05a92f10caaf51df4bf98f7cd9e90070d71790f3fa3de848fa`  
		Last Modified: Thu, 26 Jun 2025 20:48:42 GMT  
		Size: 261.0 MB (260996397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:f7f6eaadbe7a000ba5420c2ea8c78d7812aea2e2ba405d6f47c7dcc77af1c77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fcba7c7ba45a16b412de43acab6b32790c948a2de7b038009b4fe3f5344978`

```dockerfile
```

-	Layers:
	-	`sha256:0ece12c371cca20fa75cd9470ad9eb8f90b1172dae46baaf4940565722fcf88e`  
		Last Modified: Thu, 26 Jun 2025 20:44:43 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49231f16442a61f2a0b6140092b2b40d1a3786b17de63fc044fabaa5fbcee312`  
		Last Modified: Thu, 26 Jun 2025 20:44:44 GMT  
		Size: 12.1 KB (12084 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:5771a3cc2081935c59ac52b92d49c9e164d4fed92c9f6420aa8cc50364aead6e
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
$ docker pull rust@sha256:95f6d6956bf8abd7461763ba7ccd243d8964a41c8eb3f41d895490c782628d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553347880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a479811b82446e6bf598238bb2fcd3ae41b351a1a7c87e53d8f2333a7bbe001d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe9c1abe6f3b8ca9fc6abe710405f830f95262f1d356e8f6545d823b5840a5c`  
		Last Modified: Tue, 01 Jul 2025 05:12:07 GMT  
		Size: 211.4 MB (211373500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0545d5f3de1a8249849f4342031613d732af87e31f13755f5fac287119ed13e8`  
		Last Modified: Tue, 01 Jul 2025 06:18:35 GMT  
		Size: 205.1 MB (205059525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0e0dc34caec6b81f1b5ab4c9a559c11b4d7440382c69d8a2cdbe5002a71523e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15877001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81308c8e2c35f38fbef285c685f2ca642508d83efc22df71984838afd98ac55d`

```dockerfile
```

-	Layers:
	-	`sha256:3260e53bff48cf37775cac874c3e2920680f90a7669e12d2c322771f16c50614`  
		Last Modified: Tue, 01 Jul 2025 08:44:24 GMT  
		Size: 15.9 MB (15863862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a629d4f8f234144e7bda08172e21d63709f916bfe46836348a616c43d2cdd880`  
		Last Modified: Tue, 01 Jul 2025 08:44:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:b12fb2b0506d2b8fde83230531af65c46d2e1cb65c7b965a23de3015d7feff05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546880259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe31256245950fcf402e7f41d298a8bd3859cf9558a2e1ff584d64071362bda1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc606b1195a348c6a47399c1a54ab936d4477a526d62306ddce89fe76a2d22`  
		Last Modified: Tue, 01 Jul 2025 08:59:56 GMT  
		Size: 21.9 MB (21928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f4c85f426e2c955b1dac4fa88bc182d725644c23ad01bdcbf64d9664e34a8`  
		Last Modified: Tue, 01 Jul 2025 18:28:59 GMT  
		Size: 59.7 MB (59656492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda2264dd6dda88971c220cda9283a6c337d04aeb92012d9d160887d4ec0b556`  
		Last Modified: Wed, 02 Jul 2025 00:17:51 GMT  
		Size: 175.3 MB (175294922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5ff6581ced6c9c0cc98e703fa5901cda1814bee9d3ac91337dfcb2eeaa3fa`  
		Last Modified: Wed, 02 Jul 2025 12:16:49 GMT  
		Size: 245.8 MB (245792330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a6b6613abe69a8ea05c159027354fad9e25a0f58f5a61a4c761bd608e9118f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15679627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0222859d21f0de033a308a561262ae0c61dc1ab6441395c68809f9d9455913d`

```dockerfile
```

-	Layers:
	-	`sha256:d6bf21d47ea4882f2e19fc8c2018d3473ff3633b948a8a2912ffa2fb5dc5c75c`  
		Last Modified: Wed, 02 Jul 2025 11:44:31 GMT  
		Size: 15.7 MB (15666380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f88163f4b88d616cf50cd1d0bb3bb47eda6485492c98f7f4bc8035c0d832d762`  
		Last Modified: Wed, 02 Jul 2025 11:44:32 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:66b553fe51fe4eba929ee31c39d66506fe41b72cf403dab3117de2bd5d43e645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513346599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5424600217354e80a3f0ab99133ec64aa48f464a2f1c29a93cbd0f95758e5af7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a65abb6272f500a9ae5d14c9ae8ef9cb0e4009b02acfccb4dabc478f252d44`  
		Last Modified: Tue, 01 Jul 2025 19:38:43 GMT  
		Size: 202.8 MB (202827049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b360d25d0e207b0afc74cd93a7662c88e8399a9798db1e3baa5665c7aa6c157`  
		Last Modified: Wed, 02 Jul 2025 03:35:58 GMT  
		Size: 174.3 MB (174259463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2f4addd958f6c23177ba57cb0b62703dba22d22d022fa5ff6111f60b883e3dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15905729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3c6db7f65484d03b4cc60245a2ead7632bf36cf44fdf76c3720b3831df124c`

```dockerfile
```

-	Layers:
	-	`sha256:ac641e00624bd7b454d162d456dcbebc72d34940b2f4aa530da90b3cbe71d493`  
		Last Modified: Wed, 02 Jul 2025 05:44:37 GMT  
		Size: 15.9 MB (15892438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1fa12a678c68a338b4e49d70c17dbded6143e0d3861664cbccf02c362f6879`  
		Last Modified: Wed, 02 Jul 2025 05:44:38 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:628fa076d84051d529c70e5978ae2488cc27c057e4378e6d6b4427cd1f48f5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (580031340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b007959168ba93c975145eae21e48f1112c685910223873e0805f91c16efcf81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99742b01aaf231df6992d8ecab593f6a7668b9047c6bb8cae0cc211c42b656d6`  
		Last Modified: Tue, 01 Jul 2025 05:11:03 GMT  
		Size: 210.3 MB (210310619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a36703fa30e50f1e2d2d9b8d6ee38f74b5c49158c0331edd0ac22489b68c9d`  
		Last Modified: Tue, 01 Jul 2025 08:59:26 GMT  
		Size: 229.2 MB (229161050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:60118c6a0bd04b58edbef1c693c60eef0a5c39a11250ffab32588f40429c495a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15853847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a0f3771a2d9e6d62cb0c6bcec0264fbabb8e5129657775262a756a4ab9cc9`

```dockerfile
```

-	Layers:
	-	`sha256:aede24ae4b2038e2305b863ac4a0808c493737d5ec9bc1219a2ffcdf76249352`  
		Last Modified: Tue, 01 Jul 2025 08:44:58 GMT  
		Size: 15.8 MB (15840760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adee46bd81fb5e17001fc933d0596dd15dc9c7296c5efe1c744ecb38885cff77`  
		Last Modified: Tue, 01 Jul 2025 08:44:59 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:f4c7cad30a4575e18ae53f14b5bccb71451b44d720253a8f73f1cb12780bbf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635985035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442858853b317d76b745617081af4451d23840bd47301b0eabc620759c4b714`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7082fff0db11ec79e9a3c8fc9c05691e086d30ca51023010805fccbeac2b8dad`  
		Last Modified: Tue, 01 Jul 2025 05:07:55 GMT  
		Size: 25.7 MB (25663667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6cd79d875ce6ba17d2080d5bd4d0d55f7eec0f6bb923ae0b53e5bec14ef9b`  
		Last Modified: Tue, 01 Jul 2025 10:09:38 GMT  
		Size: 69.8 MB (69840014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575c9bdfba8d02bb3354a6a72904306bd1ae2c4432d14255385a153c75887837`  
		Last Modified: Tue, 01 Jul 2025 16:27:30 GMT  
		Size: 214.4 MB (214424908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078767722b4e04b7787f0ea5f95284ec4da0e1c5dc7804af4c26dc5181ec096c`  
		Last Modified: Wed, 02 Jul 2025 00:02:53 GMT  
		Size: 273.7 MB (273719203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1a33a8b84d73eb3cf5fe4d5eb91a7212e3e015e40670b51ddebf3b52c4dbe0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee34f793447401153bab355f4bfbba25c4161b769172568c3b013931ffcfc953`

```dockerfile
```

-	Layers:
	-	`sha256:a169d322c59d3a0ddff0bf27d48dbe267dff9b48aaddd2ed30804cb885ff2527`  
		Last Modified: Tue, 01 Jul 2025 23:44:57 GMT  
		Size: 15.8 MB (15839092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d4887067e8590d2b12056401643ede686e2b3a83a2fccdfca0b762a5961e6a7`  
		Last Modified: Tue, 01 Jul 2025 23:44:58 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:79ee189d40fd6c859e15a1e9c69b6da58d451b096e16a52dfec29b9bd0d76a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.5 MB (601452429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924b21bb8e92662795debcd307e3f3204964743780a9f028dfb3700b0ae8640b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1e32b479a11528098c70ba4af6292099abafcb29e0823d2861c86032c9b0b`  
		Last Modified: Tue, 01 Jul 2025 13:41:28 GMT  
		Size: 63.5 MB (63497964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2254c2dc3c53615f5f6a5adcfafb558670473622cb504cb0a6d02fd2b89d2667`  
		Last Modified: Tue, 01 Jul 2025 14:10:41 GMT  
		Size: 183.4 MB (183421934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c312814d252c566d3c3ee8f98763bedd5510a970a7460965bac0ea117ac8071c`  
		Last Modified: Tue, 01 Jul 2025 21:03:03 GMT  
		Size: 283.4 MB (283362703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a4f9cf4a09562544ef011200268fb453c235bc5b972df93f32ca2dbf4ac1e349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15684597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afc1cf86bd3504dbe315e3c93562fc2ff8e92d15305627e7b38023518ec873b`

```dockerfile
```

-	Layers:
	-	`sha256:39dbb3c0f9a78d73aea412786fb8fabb2d333d5f18f4608bab4734aaa8e60fd7`  
		Last Modified: Tue, 01 Jul 2025 20:45:07 GMT  
		Size: 15.7 MB (15671458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d32a8a23e2b1c8cb3fdec2c521041d1a7fc5c908e5a6ce6bd3048f58dfefe8`  
		Last Modified: Tue, 01 Jul 2025 20:45:08 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:8eb96c7c77c04660a95d5e256869de0a18130f97624ef75c522ea886d4e51d95
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
$ docker pull rust@sha256:4fe592966775f3396e3d099d674f0664e4383336371ca5600e40c2fe3b575383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526479452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e24231a2d9ba56b24304902b7106252b1ba5aa98dc98b58ac09df699a11813e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06772a4eff3df697497bb68b4dcdeb97fdb9338b5e7dde7d1a53579c3203c9ba`  
		Last Modified: Tue, 01 Jul 2025 03:20:06 GMT  
		Size: 54.8 MB (54757481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd49c17bd36c59d7bf7afe446ee52f36cad8a6393628526989f2db44b4486c1`  
		Last Modified: Tue, 01 Jul 2025 05:11:29 GMT  
		Size: 197.1 MB (197142751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b35768b15c47fe75ef345baf1601f003231cf7fa1353d4b05177acb4b38d712`  
		Last Modified: Tue, 01 Jul 2025 06:44:33 GMT  
		Size: 205.1 MB (205059062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f26b96d6cf3fe96312784ed4c21daceefd839ea7ec263a286a9c464c17889bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15475219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4229b2d8712383288725ba877fc8da75d82f25002251269162108f995d12061e`

```dockerfile
```

-	Layers:
	-	`sha256:2186b18143b7f42f67f19ba8594c9c55a420158d4af543684506320400941527`  
		Last Modified: Tue, 01 Jul 2025 08:44:36 GMT  
		Size: 15.5 MB (15463971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c86f9b373cccbb5f795ae509ad60503878f0f8e5a247421fd1a6f1461968cb`  
		Last Modified: Tue, 01 Jul 2025 08:44:37 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:d9735061f6bd324ad5d9a6b1f353e919d01b9515946a2de100568511a1182afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.9 MB (527938900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c390dbe5f1131b80bb7b105624994b79e2115d8dec0bcace50edd510c2198b13`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:efcf40eae0046ccd92d3b47ff685e1e9cf7a34d0a92f6de893078f115e01f20f`  
		Last Modified: Tue, 01 Jul 2025 01:15:14 GMT  
		Size: 49.0 MB (49043960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6769ed354ec7fde57e63bdf9788543b96fd8f93923607ad70767b9c4cfa25b`  
		Last Modified: Tue, 01 Jul 2025 08:59:49 GMT  
		Size: 14.9 MB (14880774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28365fa3b8363bfd29e20b4b17838c65ddc4bdacb1bf15ca9af5a4045e4feaf7`  
		Last Modified: Tue, 01 Jul 2025 18:29:48 GMT  
		Size: 50.6 MB (50631320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31eafcbc0a8afc051ea3519738dd6b4e501ce5f603e4a10bdf1f0f6720a29f58`  
		Last Modified: Wed, 02 Jul 2025 00:17:56 GMT  
		Size: 167.6 MB (167589980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d954ab622638b81a76f8faca7f27cdbead519ce4a96bfe58ce0ce8c04de4c07c`  
		Last Modified: Wed, 02 Jul 2025 12:59:39 GMT  
		Size: 245.8 MB (245792866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:533dd51110aa122013299169d3241c8ff7b0a167ac026488a451cc3cf5a32242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15274640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43196c04d844d43946f4c7a75dd78f798c69fa8488debfc89ba320795b1e927b`

```dockerfile
```

-	Layers:
	-	`sha256:652198c66ccabc1746f6054da6a0b040aa11e579f227a638a7db763062f6b11e`  
		Last Modified: Wed, 02 Jul 2025 11:44:40 GMT  
		Size: 15.3 MB (15263315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9c99c87037228c8be536fc6fd298ab2a611a1fbd6a3d52d733fb4a29c90c2d`  
		Last Modified: Wed, 02 Jul 2025 11:44:41 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8b22455a7ce2adb1355067638284ee99d21cc516fab63a96c4514beaf370aa94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.2 MB (487172791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc77b2b3e794e11c9031f129feea6f9dd3649f86a9b70ad373910e70e5761458`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5424250d141bf5f4ec62e698bba9b5695482a3015186d3b14a633da8916bf7dd`  
		Last Modified: Tue, 01 Jul 2025 06:52:24 GMT  
		Size: 15.8 MB (15750716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7766ba090abb327ecb7e9e14ac90bbcc45c5ba6bb8a568ae531c960ff1acad55`  
		Last Modified: Tue, 01 Jul 2025 13:29:45 GMT  
		Size: 54.9 MB (54855722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1801db58ebce0297c6d03187f6e882ae0b8ba8838f3e18a17f3bcd9137be277`  
		Last Modified: Tue, 01 Jul 2025 20:13:40 GMT  
		Size: 190.1 MB (190053793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714498f74a0f367b5e69c9e7e3bd688c25db146ed8b97acec1446cb2218e705`  
		Last Modified: Wed, 02 Jul 2025 06:40:03 GMT  
		Size: 174.3 MB (174260306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e2730dd90c1b51e30c613c774511479688800225d93c02bdaf36189e99891fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15477294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b9b0c706b4ad223660013177c4a118765a26d87add26bb8babfbdf979efb1d`

```dockerfile
```

-	Layers:
	-	`sha256:12453b011a0f7bb3aac0c83948f50551f0d4d5ae1b1e0c7c3a472d44e1f5c7da`  
		Last Modified: Wed, 02 Jul 2025 05:44:46 GMT  
		Size: 15.5 MB (15465942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccba5cc2249b25264628303f496f30cecf3ead2e13e1dc3399d7f98b1951ce12`  
		Last Modified: Wed, 02 Jul 2025 05:44:46 GMT  
		Size: 11.4 KB (11352 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:2aaf00b554cd4ff148c16a3e58146641b87aa7c629bbb67c6731554afa3c2d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 MB (556215637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab21c61c4d19a041fcae82560e48bb7233059e80ef65189d4d830b0493e23dbc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113be81052ec8e8323c4db158dc9c99295355934e950a6367e5c27038fd1e04c`  
		Last Modified: Tue, 01 Jul 2025 02:24:43 GMT  
		Size: 16.3 MB (16268907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05b439f6df174e28bd21dc59eead603def3bcbd47ec6462f86b7758c4db6ef`  
		Last Modified: Tue, 01 Jul 2025 03:19:57 GMT  
		Size: 56.0 MB (56049937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d170ad31938c07c5739c923eaf5f7569c644e2ea2ead929bbc107d7eac895f78`  
		Last Modified: Tue, 01 Jul 2025 05:11:30 GMT  
		Size: 200.0 MB (200043566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7271fc5f55db8e0b012c06b0785adf36c8ade5d9f290c40fa07be956a5eecde`  
		Last Modified: Tue, 01 Jul 2025 13:00:23 GMT  
		Size: 229.2 MB (229163293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3cb1daa21e1c22f0ea3d5100504d1da2f45a788bcf4f0c42396ea073969b5df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd9075c8dc525761d3e7cf32a7d172eaaee78ecc359ee8f83da3b6bf52859ef`

```dockerfile
```

-	Layers:
	-	`sha256:4ba2cd6c29aab7b896485ed38a1fc73dd8448a29ef9bf4744495334a3e930f89`  
		Last Modified: Tue, 01 Jul 2025 08:45:13 GMT  
		Size: 15.5 MB (15450673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8861a1fd041f7cf768c0ad3c6f4dc87d554c6bcb084c979d61f7a6af8ff9a715`  
		Last Modified: Tue, 01 Jul 2025 08:45:13 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:5771a3cc2081935c59ac52b92d49c9e164d4fed92c9f6420aa8cc50364aead6e
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
$ docker pull rust@sha256:95f6d6956bf8abd7461763ba7ccd243d8964a41c8eb3f41d895490c782628d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553347880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a479811b82446e6bf598238bb2fcd3ae41b351a1a7c87e53d8f2333a7bbe001d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe9c1abe6f3b8ca9fc6abe710405f830f95262f1d356e8f6545d823b5840a5c`  
		Last Modified: Tue, 01 Jul 2025 05:12:07 GMT  
		Size: 211.4 MB (211373500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0545d5f3de1a8249849f4342031613d732af87e31f13755f5fac287119ed13e8`  
		Last Modified: Tue, 01 Jul 2025 06:18:35 GMT  
		Size: 205.1 MB (205059525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:0e0dc34caec6b81f1b5ab4c9a559c11b4d7440382c69d8a2cdbe5002a71523e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15877001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81308c8e2c35f38fbef285c685f2ca642508d83efc22df71984838afd98ac55d`

```dockerfile
```

-	Layers:
	-	`sha256:3260e53bff48cf37775cac874c3e2920680f90a7669e12d2c322771f16c50614`  
		Last Modified: Tue, 01 Jul 2025 08:44:24 GMT  
		Size: 15.9 MB (15863862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a629d4f8f234144e7bda08172e21d63709f916bfe46836348a616c43d2cdd880`  
		Last Modified: Tue, 01 Jul 2025 08:44:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:b12fb2b0506d2b8fde83230531af65c46d2e1cb65c7b965a23de3015d7feff05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546880259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe31256245950fcf402e7f41d298a8bd3859cf9558a2e1ff584d64071362bda1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc606b1195a348c6a47399c1a54ab936d4477a526d62306ddce89fe76a2d22`  
		Last Modified: Tue, 01 Jul 2025 08:59:56 GMT  
		Size: 21.9 MB (21928338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f4c85f426e2c955b1dac4fa88bc182d725644c23ad01bdcbf64d9664e34a8`  
		Last Modified: Tue, 01 Jul 2025 18:28:59 GMT  
		Size: 59.7 MB (59656492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda2264dd6dda88971c220cda9283a6c337d04aeb92012d9d160887d4ec0b556`  
		Last Modified: Wed, 02 Jul 2025 00:17:51 GMT  
		Size: 175.3 MB (175294922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e5ff6581ced6c9c0cc98e703fa5901cda1814bee9d3ac91337dfcb2eeaa3fa`  
		Last Modified: Wed, 02 Jul 2025 12:16:49 GMT  
		Size: 245.8 MB (245792330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:a6b6613abe69a8ea05c159027354fad9e25a0f58f5a61a4c761bd608e9118f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15679627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0222859d21f0de033a308a561262ae0c61dc1ab6441395c68809f9d9455913d`

```dockerfile
```

-	Layers:
	-	`sha256:d6bf21d47ea4882f2e19fc8c2018d3473ff3633b948a8a2912ffa2fb5dc5c75c`  
		Last Modified: Wed, 02 Jul 2025 11:44:31 GMT  
		Size: 15.7 MB (15666380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f88163f4b88d616cf50cd1d0bb3bb47eda6485492c98f7f4bc8035c0d832d762`  
		Last Modified: Wed, 02 Jul 2025 11:44:32 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:66b553fe51fe4eba929ee31c39d66506fe41b72cf403dab3117de2bd5d43e645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513346599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5424600217354e80a3f0ab99133ec64aa48f464a2f1c29a93cbd0f95758e5af7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a65abb6272f500a9ae5d14c9ae8ef9cb0e4009b02acfccb4dabc478f252d44`  
		Last Modified: Tue, 01 Jul 2025 19:38:43 GMT  
		Size: 202.8 MB (202827049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b360d25d0e207b0afc74cd93a7662c88e8399a9798db1e3baa5665c7aa6c157`  
		Last Modified: Wed, 02 Jul 2025 03:35:58 GMT  
		Size: 174.3 MB (174259463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:2f4addd958f6c23177ba57cb0b62703dba22d22d022fa5ff6111f60b883e3dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15905729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3c6db7f65484d03b4cc60245a2ead7632bf36cf44fdf76c3720b3831df124c`

```dockerfile
```

-	Layers:
	-	`sha256:ac641e00624bd7b454d162d456dcbebc72d34940b2f4aa530da90b3cbe71d493`  
		Last Modified: Wed, 02 Jul 2025 05:44:37 GMT  
		Size: 15.9 MB (15892438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1fa12a678c68a338b4e49d70c17dbded6143e0d3861664cbccf02c362f6879`  
		Last Modified: Wed, 02 Jul 2025 05:44:38 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:628fa076d84051d529c70e5978ae2488cc27c057e4378e6d6b4427cd1f48f5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (580031340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b007959168ba93c975145eae21e48f1112c685910223873e0805f91c16efcf81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99742b01aaf231df6992d8ecab593f6a7668b9047c6bb8cae0cc211c42b656d6`  
		Last Modified: Tue, 01 Jul 2025 05:11:03 GMT  
		Size: 210.3 MB (210310619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a36703fa30e50f1e2d2d9b8d6ee38f74b5c49158c0331edd0ac22489b68c9d`  
		Last Modified: Tue, 01 Jul 2025 08:59:26 GMT  
		Size: 229.2 MB (229161050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:60118c6a0bd04b58edbef1c693c60eef0a5c39a11250ffab32588f40429c495a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15853847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842a0f3771a2d9e6d62cb0c6bcec0264fbabb8e5129657775262a756a4ab9cc9`

```dockerfile
```

-	Layers:
	-	`sha256:aede24ae4b2038e2305b863ac4a0808c493737d5ec9bc1219a2ffcdf76249352`  
		Last Modified: Tue, 01 Jul 2025 08:44:58 GMT  
		Size: 15.8 MB (15840760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adee46bd81fb5e17001fc933d0596dd15dc9c7296c5efe1c744ecb38885cff77`  
		Last Modified: Tue, 01 Jul 2025 08:44:59 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:f4c7cad30a4575e18ae53f14b5bccb71451b44d720253a8f73f1cb12780bbf80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635985035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442858853b317d76b745617081af4451d23840bd47301b0eabc620759c4b714`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7082fff0db11ec79e9a3c8fc9c05691e086d30ca51023010805fccbeac2b8dad`  
		Last Modified: Tue, 01 Jul 2025 05:07:55 GMT  
		Size: 25.7 MB (25663667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6cd79d875ce6ba17d2080d5bd4d0d55f7eec0f6bb923ae0b53e5bec14ef9b`  
		Last Modified: Tue, 01 Jul 2025 10:09:38 GMT  
		Size: 69.8 MB (69840014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575c9bdfba8d02bb3354a6a72904306bd1ae2c4432d14255385a153c75887837`  
		Last Modified: Tue, 01 Jul 2025 16:27:30 GMT  
		Size: 214.4 MB (214424908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078767722b4e04b7787f0ea5f95284ec4da0e1c5dc7804af4c26dc5181ec096c`  
		Last Modified: Wed, 02 Jul 2025 00:02:53 GMT  
		Size: 273.7 MB (273719203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:1a33a8b84d73eb3cf5fe4d5eb91a7212e3e015e40670b51ddebf3b52c4dbe0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee34f793447401153bab355f4bfbba25c4161b769172568c3b013931ffcfc953`

```dockerfile
```

-	Layers:
	-	`sha256:a169d322c59d3a0ddff0bf27d48dbe267dff9b48aaddd2ed30804cb885ff2527`  
		Last Modified: Tue, 01 Jul 2025 23:44:57 GMT  
		Size: 15.8 MB (15839092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d4887067e8590d2b12056401643ede686e2b3a83a2fccdfca0b762a5961e6a7`  
		Last Modified: Tue, 01 Jul 2025 23:44:58 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:79ee189d40fd6c859e15a1e9c69b6da58d451b096e16a52dfec29b9bd0d76a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.5 MB (601452429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924b21bb8e92662795debcd307e3f3204964743780a9f028dfb3700b0ae8640b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1e32b479a11528098c70ba4af6292099abafcb29e0823d2861c86032c9b0b`  
		Last Modified: Tue, 01 Jul 2025 13:41:28 GMT  
		Size: 63.5 MB (63497964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2254c2dc3c53615f5f6a5adcfafb558670473622cb504cb0a6d02fd2b89d2667`  
		Last Modified: Tue, 01 Jul 2025 14:10:41 GMT  
		Size: 183.4 MB (183421934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c312814d252c566d3c3ee8f98763bedd5510a970a7460965bac0ea117ac8071c`  
		Last Modified: Tue, 01 Jul 2025 21:03:03 GMT  
		Size: 283.4 MB (283362703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:a4f9cf4a09562544ef011200268fb453c235bc5b972df93f32ca2dbf4ac1e349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15684597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afc1cf86bd3504dbe315e3c93562fc2ff8e92d15305627e7b38023518ec873b`

```dockerfile
```

-	Layers:
	-	`sha256:39dbb3c0f9a78d73aea412786fb8fabb2d333d5f18f4608bab4734aaa8e60fd7`  
		Last Modified: Tue, 01 Jul 2025 20:45:07 GMT  
		Size: 15.7 MB (15671458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d32a8a23e2b1c8cb3fdec2c521041d1a7fc5c908e5a6ce6bd3048f58dfefe8`  
		Last Modified: Tue, 01 Jul 2025 20:45:08 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:1c7eb658b16d48458a4808f15de8264a3c20d449d0cabdae47654d98e9dcecfb
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
$ docker pull rust@sha256:b0c0357c60eca8fe29b8280974a44483a28319278a5ff5c57b3e7e9c5708f643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbda49f92a1f159dfbe623e790c2a5b9c1c6c3ba68bd9e362679a9cb48c4925e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff2b7b26c381c0c4ba90768f39bf5193252f27f4e625debf008d09438b195ef`  
		Last Modified: Tue, 01 Jul 2025 05:08:00 GMT  
		Size: 275.8 MB (275821106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:ade5b81bacfe5c6c7e52b85eafa1965c8ff433a6b2c5dbe95ffdac9b636a4098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a4805359ec86648c4fa15446b7df199cdb6a6e1a03490dcb11b527cd557473`

```dockerfile
```

-	Layers:
	-	`sha256:7df8be7b6f1e71053bb68baafbd18a0da5e3196678a329e5267ab3a5a709ffd6`  
		Last Modified: Tue, 01 Jul 2025 05:44:31 GMT  
		Size: 4.1 MB (4094552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a712f57ad2be1eb1eb0de48182654c5bcff269ed26b9ac1f7e737790730b63d`  
		Last Modified: Tue, 01 Jul 2025 05:44:32 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:85f37f11d046da1808026326b03493679b5d14c2f0f4523cf5bc8d5cc0e0ee0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317565661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7f9b3c433121c615480c6153d82080be95a30629221317a4cea09c08b0a573`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4db19ae3ab5266032020a2b07eb5414e4e5af2ea274e14d76e0e545b488f04d`  
		Last Modified: Tue, 01 Jul 2025 21:04:24 GMT  
		Size: 293.6 MB (293626917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:f5c7c3079e6be98cf7906e069b6a07af60bc9f5410e2deba15738732d1776661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b45c40a162ec803cc4480e1a932c1658154fae9d07c32b6cd1ff7053f34a7f7`

```dockerfile
```

-	Layers:
	-	`sha256:c7b3d0ac3ecfb43b93f6888077022d4165a1bd97012372bb37d32a5e2e76ccde`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 3.9 MB (3908981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd6ab2ec5e6066af386464396673a5d060f5b1a51cf8099cafde5bf8cb46451`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:35d3b11bbc6b7f45a174551689621906e5785d4e6e79f2aa3b4ace967a97a055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268179917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1880617faa9ea5bc0df720923e7d75c521d91fc7a3583e3360d6068d359c2b84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e130c413bba66f1a532f016096e1ca99fc7921a6d03f4ae5e7eef4f9de7197`  
		Last Modified: Tue, 01 Jul 2025 14:52:04 GMT  
		Size: 240.1 MB (240102239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:b42e61db7f4c7471a71877c4a53f4d0391e7954c21dc20f7a3973cec0a2e7057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd222f432ceb8c15e86b58486cf5fd9c4582036ac9dcb8cede1be44821594ae1`

```dockerfile
```

-	Layers:
	-	`sha256:4c92de7432ff997c7c9d6fd67c06d2e50d70c9800c27e05fa0d04b2dcc4d42dd`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 4.1 MB (4116896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d1589208f0a8f59560905b8c36a4c4ecf08601526c55cbaaabc4a10846fb78`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:ff6fcb7ad6293f4a4c28db122754d93e024b99ca56a9f5027ddced08234ef721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325992228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4eb540ded896f027e6b1931f38d7618a4364b4643343cf6a82ef2de0e775e79`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3f2ceb310dae022b26d227eecca523fe07e1383bbc8cf746de0a949d9a3650`  
		Last Modified: Tue, 01 Jul 2025 06:01:36 GMT  
		Size: 296.8 MB (296779796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:310296d66708c74b8f7df786253dabb1763763f3ae996499d228c97b5defc6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad4a9c0226f971d47fbf4e1e3b0972b7052bb0257233fab74bc5c4b8783fb1e`

```dockerfile
```

-	Layers:
	-	`sha256:2a6a2a00284fbce671a5f0f7c61ebfbf8c2d5771cda8a1bd5445be27b699d096`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 4.1 MB (4073915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d875623e01bac8366b22e9a8bf9378721a880661602db1d20b97da37bd0c7c2a`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:e00cab06ebef6d7bb5580cedac63b15bf337fd68225ac6a152bdeb1d08bca552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374561374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8452adee592dd5981efa36540ccd9dd66cc2273fd2272ece300389cc198997a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a95af4d06128b392493eba88f8150c9e90691be1c0f0e8024d5929b44de3930`  
		Last Modified: Tue, 01 Jul 2025 13:00:07 GMT  
		Size: 342.5 MB (342488554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:ad4355591f63f7acdbf5366f8fb6d2241920c664d093c0327bd30a320b228ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687a2175e85119fb64fa7d37bd7720459fed5f9513594f53bbddccbef9cbce8d`

```dockerfile
```

-	Layers:
	-	`sha256:b40dd3069d53ab3fd2d2a8604ee2b563e69d54a6f2f4e29cd2f5cb441d80ae60`  
		Last Modified: Tue, 01 Jul 2025 11:44:38 GMT  
		Size: 4.1 MB (4066865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44f89002a1ae239b997acfc875a4c4a4fc8423278688b1ec444ca96cf66b74f`  
		Last Modified: Tue, 01 Jul 2025 11:44:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:1cf72ceabd44d186a6f08948bad51ee0050ed17cb47657c6b74e1e879451a34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360392180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871910d1ab2a752b966ffce7ec56ab4866c791bce0f9fc075cb26d7744e75884`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8a3025335a2a160722cb689b6c389f0316ea4b027c2dad34fef52df858c365`  
		Last Modified: Tue, 01 Jul 2025 10:42:01 GMT  
		Size: 333.5 MB (333504369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:d04b9fa09c2d16e830240aaa30f0b46002ffc117461d7109c104bd5c6732a461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6791cd1d0129cc03fe2cbcb7c2269397f8348bb85df5bd5b9a8e6575a8923e`

```dockerfile
```

-	Layers:
	-	`sha256:2a8e89592d0564890623c9199bb211483a145b510ce0c49afc579dabe00180f9`  
		Last Modified: Tue, 01 Jul 2025 08:44:56 GMT  
		Size: 3.9 MB (3932230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52770394e7f7570572f6a897500a0bc0f14d82302ff5f32b5db7076d7a67ab3a`  
		Last Modified: Tue, 01 Jul 2025 08:44:57 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:1c7eb658b16d48458a4808f15de8264a3c20d449d0cabdae47654d98e9dcecfb
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
$ docker pull rust@sha256:b0c0357c60eca8fe29b8280974a44483a28319278a5ff5c57b3e7e9c5708f643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbda49f92a1f159dfbe623e790c2a5b9c1c6c3ba68bd9e362679a9cb48c4925e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff2b7b26c381c0c4ba90768f39bf5193252f27f4e625debf008d09438b195ef`  
		Last Modified: Tue, 01 Jul 2025 05:08:00 GMT  
		Size: 275.8 MB (275821106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ade5b81bacfe5c6c7e52b85eafa1965c8ff433a6b2c5dbe95ffdac9b636a4098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a4805359ec86648c4fa15446b7df199cdb6a6e1a03490dcb11b527cd557473`

```dockerfile
```

-	Layers:
	-	`sha256:7df8be7b6f1e71053bb68baafbd18a0da5e3196678a329e5267ab3a5a709ffd6`  
		Last Modified: Tue, 01 Jul 2025 05:44:31 GMT  
		Size: 4.1 MB (4094552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a712f57ad2be1eb1eb0de48182654c5bcff269ed26b9ac1f7e737790730b63d`  
		Last Modified: Tue, 01 Jul 2025 05:44:32 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:85f37f11d046da1808026326b03493679b5d14c2f0f4523cf5bc8d5cc0e0ee0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317565661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7f9b3c433121c615480c6153d82080be95a30629221317a4cea09c08b0a573`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4db19ae3ab5266032020a2b07eb5414e4e5af2ea274e14d76e0e545b488f04d`  
		Last Modified: Tue, 01 Jul 2025 21:04:24 GMT  
		Size: 293.6 MB (293626917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f5c7c3079e6be98cf7906e069b6a07af60bc9f5410e2deba15738732d1776661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b45c40a162ec803cc4480e1a932c1658154fae9d07c32b6cd1ff7053f34a7f7`

```dockerfile
```

-	Layers:
	-	`sha256:c7b3d0ac3ecfb43b93f6888077022d4165a1bd97012372bb37d32a5e2e76ccde`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 3.9 MB (3908981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd6ab2ec5e6066af386464396673a5d060f5b1a51cf8099cafde5bf8cb46451`  
		Last Modified: Tue, 01 Jul 2025 20:44:35 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:35d3b11bbc6b7f45a174551689621906e5785d4e6e79f2aa3b4ace967a97a055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268179917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1880617faa9ea5bc0df720923e7d75c521d91fc7a3583e3360d6068d359c2b84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e130c413bba66f1a532f016096e1ca99fc7921a6d03f4ae5e7eef4f9de7197`  
		Last Modified: Tue, 01 Jul 2025 14:52:04 GMT  
		Size: 240.1 MB (240102239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b42e61db7f4c7471a71877c4a53f4d0391e7954c21dc20f7a3973cec0a2e7057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd222f432ceb8c15e86b58486cf5fd9c4582036ac9dcb8cede1be44821594ae1`

```dockerfile
```

-	Layers:
	-	`sha256:4c92de7432ff997c7c9d6fd67c06d2e50d70c9800c27e05fa0d04b2dcc4d42dd`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 4.1 MB (4116896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d1589208f0a8f59560905b8c36a4c4ecf08601526c55cbaaabc4a10846fb78`  
		Last Modified: Tue, 01 Jul 2025 14:44:32 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:ff6fcb7ad6293f4a4c28db122754d93e024b99ca56a9f5027ddced08234ef721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325992228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4eb540ded896f027e6b1931f38d7618a4364b4643343cf6a82ef2de0e775e79`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3f2ceb310dae022b26d227eecca523fe07e1383bbc8cf746de0a949d9a3650`  
		Last Modified: Tue, 01 Jul 2025 06:01:36 GMT  
		Size: 296.8 MB (296779796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:310296d66708c74b8f7df786253dabb1763763f3ae996499d228c97b5defc6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad4a9c0226f971d47fbf4e1e3b0972b7052bb0257233fab74bc5c4b8783fb1e`

```dockerfile
```

-	Layers:
	-	`sha256:2a6a2a00284fbce671a5f0f7c61ebfbf8c2d5771cda8a1bd5445be27b699d096`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 4.1 MB (4073915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d875623e01bac8366b22e9a8bf9378721a880661602db1d20b97da37bd0c7c2a`  
		Last Modified: Tue, 01 Jul 2025 05:44:46 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:e00cab06ebef6d7bb5580cedac63b15bf337fd68225ac6a152bdeb1d08bca552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374561374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8452adee592dd5981efa36540ccd9dd66cc2273fd2272ece300389cc198997a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a95af4d06128b392493eba88f8150c9e90691be1c0f0e8024d5929b44de3930`  
		Last Modified: Tue, 01 Jul 2025 13:00:07 GMT  
		Size: 342.5 MB (342488554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ad4355591f63f7acdbf5366f8fb6d2241920c664d093c0327bd30a320b228ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687a2175e85119fb64fa7d37bd7720459fed5f9513594f53bbddccbef9cbce8d`

```dockerfile
```

-	Layers:
	-	`sha256:b40dd3069d53ab3fd2d2a8604ee2b563e69d54a6f2f4e29cd2f5cb441d80ae60`  
		Last Modified: Tue, 01 Jul 2025 11:44:38 GMT  
		Size: 4.1 MB (4066865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44f89002a1ae239b997acfc875a4c4a4fc8423278688b1ec444ca96cf66b74f`  
		Last Modified: Tue, 01 Jul 2025 11:44:39 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:1cf72ceabd44d186a6f08948bad51ee0050ed17cb47657c6b74e1e879451a34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360392180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871910d1ab2a752b966ffce7ec56ab4866c791bce0f9fc075cb26d7744e75884`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8a3025335a2a160722cb689b6c389f0316ea4b027c2dad34fef52df858c365`  
		Last Modified: Tue, 01 Jul 2025 10:42:01 GMT  
		Size: 333.5 MB (333504369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d04b9fa09c2d16e830240aaa30f0b46002ffc117461d7109c104bd5c6732a461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6791cd1d0129cc03fe2cbcb7c2269397f8348bb85df5bd5b9a8e6575a8923e`

```dockerfile
```

-	Layers:
	-	`sha256:2a8e89592d0564890623c9199bb211483a145b510ce0c49afc579dabe00180f9`  
		Last Modified: Tue, 01 Jul 2025 08:44:56 GMT  
		Size: 3.9 MB (3932230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52770394e7f7570572f6a897500a0bc0f14d82302ff5f32b5db7076d7a67ab3a`  
		Last Modified: Tue, 01 Jul 2025 08:44:57 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:12d9a0ff4f3c87badbf56a27ffd6c4774ebe1b5fe5c6b7b1a39cfee537fcb62f
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
$ docker pull rust@sha256:fc66d738f64bca39b62f4a8602bce8239a58d813a073dec6eb87c26ed46190c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead6f32afcd0798a56c170ce2851030ab2ae5772cc7aaaec8b47346331cd33a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d114182f83d2bc4d73e02cc5bb74bda2938943a605a1efe8e8e5921a9334c06b`  
		Last Modified: Tue, 01 Jul 2025 04:34:37 GMT  
		Size: 265.2 MB (265206650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f2b2479ca7328f021feef75a9a45f117ffc3ee13a53990561c1dde6401e77ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e7b91d95fa7f94247595b016c4b0afdf5c4568be554c642efa57ecedd45917`

```dockerfile
```

-	Layers:
	-	`sha256:17df34ae2e3f1174c3451942d63bf066080013096af8da1c1fae497282282c74`  
		Last Modified: Tue, 01 Jul 2025 05:44:38 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86c3b78ad1853f15af29c20213d59684bc1b948a20593345e4229e0c91d938ac`  
		Last Modified: Tue, 01 Jul 2025 05:44:39 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:2a8251a939f0d13ed2a1ea24d1f9ef251bbbf030d520485b394de2b9c23f1575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313623477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b182ed292d4c08791794619177de2b422b06a63b5f34f388d6e1f7c828ccf4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:96b51e81cdb8508366118f41a9ec499f52f0d0211b084d5d516e1be131b35266`  
		Last Modified: Tue, 01 Jul 2025 01:15:21 GMT  
		Size: 25.5 MB (25544163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e8ad713014c96437118acd9656b3f10b47964888722c469680e6042510ccb`  
		Last Modified: Wed, 02 Jul 2025 00:48:15 GMT  
		Size: 288.1 MB (288079314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d16acf27c46754346860ce745ea5760b105c162694adc9d454c94f795a796f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2cfe874064a2b600d64ab76c2b059316a0d09778b241f6d9ef1fe2850a3e56`

```dockerfile
```

-	Layers:
	-	`sha256:08e8559715569c50dc0f3e68ebbed15841af5fa459ca720c38fa15b3c2a035d4`  
		Last Modified: Tue, 01 Jul 2025 20:44:41 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffbb508550ec246d38153bd7938e330e200f9c02ca0f0d1d4b1abcc527101490`  
		Last Modified: Tue, 01 Jul 2025 20:44:42 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d7bf42de9bb8c46335f1541a795bd167560ad0c7d211e67cad3f5a7417243fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258705512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28cce79db40ab1d0fa12cbfa105d6ef1dff13b63c1a93b8fb9e9682a0418a59`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4458b4f354b132ede276e7da54a33c211b23ceac4f34da5ed2b7fae09bb95d6f`  
		Last Modified: Tue, 01 Jul 2025 14:45:32 GMT  
		Size: 230.0 MB (229961372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f8cb1c53bc02e47f1e50499e70854d43e2f98ddf439fa5b52d34a6424733aed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f09370c05fb448311182a49164c612c0299712281c47b1564078e73ebb6a67`

```dockerfile
```

-	Layers:
	-	`sha256:263fa190fe34f81500ba2e8ac8bf53f05869282f02579d474166a6be2567d51c`  
		Last Modified: Tue, 01 Jul 2025 14:44:39 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a44a181f21adc0542d1acb35f17b1f20343532cfd22efc73efb5044556e05115`  
		Last Modified: Tue, 01 Jul 2025 14:44:39 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:6aeeeeaf3ed73638e4135dce21527f418f6a192d3e2de9c4d26664694f90c0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.1 MB (321133034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e7dcea35fc6893afae54fc7ac2446ea032b06889451f72c5fb09918d9ba66c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jun 2025 18:18:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Thu, 26 Jun 2025 18:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 26 Jun 2025 18:18:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 26 Jun 2025 18:18:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:40be1da6146972d9df50a98eef7b5c0f729cd95a3a38782418f354f3b9355a9a`  
		Last Modified: Tue, 01 Jul 2025 01:14:57 GMT  
		Size: 31.2 MB (31189680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e1a302797c6fe4ad387e823eb711877bfcee5af925dcfc3decc2b4083fef72`  
		Last Modified: Tue, 01 Jul 2025 12:59:38 GMT  
		Size: 289.9 MB (289943354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8c4db6ccf78a02913434449b05bc26924375a6fa2a57e1fb8cdc0a9149a6128d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60622052414fe9b2982743aeebbe224601c12752ff8f4cbe89d50b54c59a8ad0`

```dockerfile
```

-	Layers:
	-	`sha256:423e3a39660d3cd9304a2f3cd9a7f0037ec79d19c72661b55bb7ed8a8d78a9ad`  
		Last Modified: Tue, 01 Jul 2025 05:44:54 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a0678dc17cc916be60884c0469158c1664b2dcd59755d390b82d7f534f97fa`  
		Last Modified: Tue, 01 Jul 2025 05:44:54 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-trixie`

```console
$ docker pull rust@sha256:e68d2ba3397c3c04c47647ad5d615afaca80ae00dcc4f5140e43495c537746c6
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

### `rust:slim-trixie` - linux; amd64

```console
$ docker pull rust@sha256:7721d2705af97fbfbf241d1f329e1e7144cb2743b2ecac5711352c8ea4fe3251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310236807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0d0605178c491bdb2bc093d06776322acffdddadb8d6b3ae47a7aba111cc68`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2b9064154c24154965e1b574cfe4999144b627db7f678b3a566d3eeeac02dc`  
		Last Modified: Thu, 03 Jul 2025 20:42:04 GMT  
		Size: 280.5 MB (280475701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:d619583f10fabd5f99a621389b8e4043ffa188cbd8eb305b7c2e7e8f2d63ed54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89914cf1279171e30ef2a59799b98b1a4e83babe84c87f1ff92ef591c7fc3ec`

```dockerfile
```

-	Layers:
	-	`sha256:c1e52b080a5caaa75906ac1aef51b1a4e5905284978a04a29d5def27fdaceafb`  
		Last Modified: Thu, 03 Jul 2025 17:45:05 GMT  
		Size: 4.2 MB (4162901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d4390982a55f7e70f969a7af51b2b195f34be5ebbe6c6f17d939bb524e497b`  
		Last Modified: Thu, 03 Jul 2025 17:45:06 GMT  
		Size: 12.1 KB (12061 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:57b1df7d4a1e8b0b231b0e8a09ae0cf89c7939542d2f1e1ff4a05f7de70f2a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322260431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a609326c1f09c4e6aa554b61b16080a0783429c62de582cd5e3ec4188913f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:75cb2c2919cdd5f70bd8208e02191091cad32dd857e56bfd33f35cd6d531c82a`  
		Last Modified: Tue, 01 Jul 2025 01:18:55 GMT  
		Size: 26.2 MB (26201517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49ee1c5650c50a45b3eef84571458d78cbbf30fc06a0035bfa2a082ea8108d9`  
		Last Modified: Thu, 03 Jul 2025 20:48:22 GMT  
		Size: 296.1 MB (296058914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:cc54c83fc01e12d9d41cfdac572a59e588a4c54287deec7161e4b89d69757700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3979883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103636073af3a7f76abb00f7559b02484569bf5618ed3d571538a7ca3b02fc19`

```dockerfile
```

-	Layers:
	-	`sha256:ffce2eaa705d9368bce2a80cd6890bc3c2bf66295174b466a2007a02c4370d2b`  
		Last Modified: Thu, 03 Jul 2025 20:44:36 GMT  
		Size: 4.0 MB (3967745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb0ae2602c3fab378c0fcb74ec00c46711ce55c947b8f99952dd9d8fcae5488`  
		Last Modified: Thu, 03 Jul 2025 20:44:37 GMT  
		Size: 12.1 KB (12138 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:88a9c0d2b3c1ef6e0ab769f130a15a6cb2d10ed82ac6c779e1d5b543fa6a5a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274045556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47d037deb756e369db48be32af79a4b9410405268eb60580dffcfc577e67aad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:dfa10e860e0106510a14bae8331a4dd762d3d3737fdba0dbec102458f9853b71`  
		Last Modified: Tue, 01 Jul 2025 01:18:18 GMT  
		Size: 30.1 MB (30126864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab982be4b2f9d93ec333ffb69526256503de560bde0bd8a510e3b1acf793c40`  
		Last Modified: Thu, 03 Jul 2025 20:49:17 GMT  
		Size: 243.9 MB (243918692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:ec6e0fb8e467b4d66a4e91bfc44764be1efadf6791fcd25f1df5437d48d299dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a618e7a2fe30262bf7503eb5b80999a202d3e87df932a890048ca1fcb3b7b55a`

```dockerfile
```

-	Layers:
	-	`sha256:a7390525f3e02590517ad48faeb0649b52dd80e6a083feb652819a8c0320984b`  
		Last Modified: Thu, 03 Jul 2025 17:45:23 GMT  
		Size: 4.3 MB (4254069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad846470cf4d23ec2c6804afdf350c7808432e565fc39d3035fe1556cf21361e`  
		Last Modified: Thu, 03 Jul 2025 17:45:24 GMT  
		Size: 12.2 KB (12165 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; 386

```console
$ docker pull rust@sha256:6fe11019a3d4d7e50e48f4727120357e98b6e3242ea944d72f20a57ccde3976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332943226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c31842ba66bed838d3be4cddc274c3b25d4f5c056d036b9d9c5646f2f83c35`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:27b0922c0fcc2ccb534e806841adaba77d7b1a639b51fa3d953ccfa3af3a57e6`  
		Last Modified: Tue, 01 Jul 2025 01:14:55 GMT  
		Size: 31.3 MB (31281109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfea6381854ff5a1288e44fcd71c127bf8f5c12b73fca05a53a0fdf766da33e`  
		Last Modified: Thu, 03 Jul 2025 20:49:34 GMT  
		Size: 301.7 MB (301662117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:709dfc3e62d11137fe59c004c57be56ba78c0370578c39fc986245bcc924fd3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d862b9c54929822ee442cfebc6bb3152f1e05190d3476d52017e9c30cbe3777`

```dockerfile
```

-	Layers:
	-	`sha256:d76b88999182b5b6e9bf50bf33640536dbe258725e8c01c0e11481b295d36251`  
		Last Modified: Thu, 03 Jul 2025 17:45:49 GMT  
		Size: 4.1 MB (4136434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff406b796b327df9d21a85be2fa42ed6e856e504634069cad7fdc6a139e510ad`  
		Last Modified: Thu, 03 Jul 2025 17:45:49 GMT  
		Size: 12.0 KB (12030 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; ppc64le

```console
$ docker pull rust@sha256:cbef1f31e6e9d539b5e201653bc0553eadee350cf0a81efd0bdc75654187d7c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.2 MB (374189714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fe51377754a44b3b68c6389474ced3297711aa727c85fae16272f257d4d87f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05113943712185aeb07e0e0bfb3fa35e088bd6f08df1e776cc806f8bddc6db1`  
		Last Modified: Thu, 03 Jul 2025 20:50:14 GMT  
		Size: 340.6 MB (340603679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:03e00179fb0709f08bca4819fb0a5100a86a4f3d137fc7e3dd77ed4fb2bb5f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fb1b4f2f8d43288ca62d234578bbfb1d9527b44d43b4e8790007f3e694af6b`

```dockerfile
```

-	Layers:
	-	`sha256:187a0b4809cba5785eef2febd443d1c4537bde12b677052c85f9367e5c060989`  
		Last Modified: Thu, 03 Jul 2025 20:44:49 GMT  
		Size: 4.2 MB (4158025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79ae8b64b453a46d0ae29840bdd1a9e8658feec181cb272ffe4e3c012b5e5bb`  
		Last Modified: Thu, 03 Jul 2025 20:44:49 GMT  
		Size: 12.1 KB (12106 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; s390x

```console
$ docker pull rust@sha256:95bd23402ed6a90153634a026962a9c6cb52036c619765e75882d1401cc2b899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.6 MB (365571899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a7d73fb037181cda5b98fb9704a92758f96457c24664ac81eb41524bc2a693`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:728fbd29b8599bd56dcb8703b5c428523bcf0f3d48c5e95804f60267a128a3bc`  
		Last Modified: Tue, 01 Jul 2025 01:19:25 GMT  
		Size: 29.8 MB (29838345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1456ed2701051abe37f5ce865394b5d3d701095089b1c134b195eebb09d77cb`  
		Last Modified: Thu, 03 Jul 2025 20:51:48 GMT  
		Size: 335.7 MB (335733554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:b3db53400e5e90db3bf6bafadf7ed5ba7942e99fdc2b1f29db7d9338241b026a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717ea3ea743c46facb7642e47482c5e4e2469868c735a4096c86797b8e34e0a4`

```dockerfile
```

-	Layers:
	-	`sha256:f44d67311a40081884ea925705988428fd00e3afd55d1da73c10871c627143af`  
		Last Modified: Thu, 03 Jul 2025 20:44:54 GMT  
		Size: 4.0 MB (3980649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e254e26728aaa08e68b3041c15896d2bbf46234e284651a8ca903e32d7f2794c`  
		Last Modified: Thu, 03 Jul 2025 20:44:55 GMT  
		Size: 12.1 KB (12062 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:trixie`

```console
$ docker pull rust@sha256:b730c57c4c1679f1c847f0481ba8863a15d00cae22d367a7565f4422bf40d478
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

### `rust:trixie` - linux; amd64

```console
$ docker pull rust@sha256:777127bd6a86eae87d512c696f1b5d500307cae84a4b948e4b25942516d780ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.5 MB (583494432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392aa965c60a10bdc5365931c80308a245dfea6cc9bbe1aa073fb9cbb6d5c274`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13567152126a6abf6e98a928a4206f022be687e979bd113ce89b0b1f41fcbaf`  
		Last Modified: Tue, 01 Jul 2025 03:19:07 GMT  
		Size: 25.6 MB (25617737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f696393bed22361a2f932d3f084750c0cdf7e1f7186888c327230081e6257b0`  
		Last Modified: Tue, 01 Jul 2025 04:12:14 GMT  
		Size: 67.8 MB (67789682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b76da92f9efb17dc4a68c682bacce1ec791a87b62ee76639b08bfc2ee4577cd`  
		Last Modified: Tue, 01 Jul 2025 12:07:57 GMT  
		Size: 235.8 MB (235764377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9b092ebb229c418b5f5feea9ad11427731515a1d8dbf01adb95c1959d6bac6`  
		Last Modified: Thu, 03 Jul 2025 20:41:59 GMT  
		Size: 205.1 MB (205058759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:trixie` - unknown; unknown

```console
$ docker pull rust@sha256:8568cd48443fa4a0c33851892d9da52f3d656b2399dcd83e6ea414378cb1e83b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17214539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06eb85b483e6f006b4ae1adf7622a1abf1ed4b6581de2f1824c28c05b4fafb0`

```dockerfile
```

-	Layers:
	-	`sha256:3e339bf185a305476f2c298204c80a4fa1d966d3dea7c9964a8704dd8772bff2`  
		Last Modified: Thu, 03 Jul 2025 17:45:24 GMT  
		Size: 17.2 MB (17202584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4abb423fff15f1c22361c92de405fb0ef8a88535b600fc76d86d707b3b09260`  
		Last Modified: Thu, 03 Jul 2025 17:45:25 GMT  
		Size: 12.0 KB (11955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:f0d61b9434bb38e2fc365679bf6ca2b15ac36a477ee4488bca51ab2432ded2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.7 MB (570716850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e270a7c2c6520ab1bc80e5bf40b5af01074724375045b6d1103cd5fab68e50`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0611a9c58dddfe7f00bb5fe6c8f5ccecfceeb1785acc68dc070068a94adf2092`  
		Last Modified: Tue, 01 Jul 2025 01:18:31 GMT  
		Size: 45.7 MB (45708080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571abb678dad668afa2696a67ffe4981c3b5aeb37fa4c14a0cc24fdac7949b6e`  
		Last Modified: Tue, 01 Jul 2025 08:59:50 GMT  
		Size: 23.6 MB (23617932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd28b3d9ecc5ff8b97a4e765e8a818c8ca6ea137650adb3df7d53acf265e9e4e`  
		Last Modified: Tue, 01 Jul 2025 18:31:52 GMT  
		Size: 62.8 MB (62760034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7255cfd7fa333e12d9432924dd0af6dceb8b6fca12f12faa2b5157b7e9cacc6`  
		Last Modified: Thu, 03 Jul 2025 10:55:31 GMT  
		Size: 192.8 MB (192838492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990aa9e5561becb9a9a31b185a40c4e082059b4a2f864a5ea4a0c72aa5306a5`  
		Last Modified: Thu, 03 Jul 2025 20:42:55 GMT  
		Size: 245.8 MB (245792312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:trixie` - unknown; unknown

```console
$ docker pull rust@sha256:6eaf53d99ce3e71a7ea943eea06e0b1786528694755a32e99ac4ee29064aa755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16982621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8631aabd5bb545bf8056ef9539ea5075a0a8067a69adf2344dc7f33f9dcfbe7`

```dockerfile
```

-	Layers:
	-	`sha256:e1b2e6ea0d58fef7a142159e950d4cd70fad767db1159baa5d2ca9e850c1b39f`  
		Last Modified: Thu, 03 Jul 2025 17:45:54 GMT  
		Size: 17.0 MB (16970590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895c99ae34ac4942be372edd159f3a98dfcc60436b134a088738443b03f4f306`  
		Last Modified: Thu, 03 Jul 2025 17:45:56 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7c5ac5114acbafb83337d764aadd88ca774223507a916c6dd30bb082a20ec7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.5 MB (542536176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0697dd2649fdc7fa59d4cf781665f05caae4122011784ccef9a0f023a0570c48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064b8e4cb92aed27a99de363dac49c85bcb74d556fa925c921727dcdf03f7cb4`  
		Last Modified: Tue, 01 Jul 2025 06:53:32 GMT  
		Size: 25.0 MB (25008002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01789681d750567cf92706d649b58054ae1e27e35947e671160777a30538c3a2`  
		Last Modified: Wed, 02 Jul 2025 05:58:28 GMT  
		Size: 67.6 MB (67611970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4fcde14125f9212ba8ee255667590e6596810c45bdc694a8db749d7ff6d2bf`  
		Last Modified: Wed, 02 Jul 2025 06:00:35 GMT  
		Size: 226.0 MB (226025553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65018ead03f0d4f0382753ee911bff501d98c7ce180a3aabfb426c24deef1054`  
		Last Modified: Thu, 03 Jul 2025 20:12:11 GMT  
		Size: 174.3 MB (174260497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:trixie` - unknown; unknown

```console
$ docker pull rust@sha256:5fd381b02f79c5c1f30501a2e74b4143d494518193a407ab4bd263d5d4495b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17298951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960a72fcf1731c737694fba1d68b27e7546e2cafa11ed72bdf7a1711136c2ca5`

```dockerfile
```

-	Layers:
	-	`sha256:beca260f3051e49975118b198c4e96523199398c5bfe36285d4ffc2c15e5afe1`  
		Last Modified: Thu, 03 Jul 2025 17:46:11 GMT  
		Size: 17.3 MB (17286892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637b38306d48fc5fd76b15fe7b2603dc5a04735734490c149d9278c4bd7ef21e`  
		Last Modified: Thu, 03 Jul 2025 17:46:14 GMT  
		Size: 12.1 KB (12059 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:trixie` - linux; 386

```console
$ docker pull rust@sha256:d4508bf7617fc0667b9f76693bfb223e42469dc1abfd62bc4affcf61fdec1d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.4 MB (616411351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f713341993075dddfd01eb0a193e3e5a746dc11f9c4688e2c3c41ab15827a02`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d223755a7489df8352d3a71955e26d35281b9c0f0609e017af54d9e75e3b435b`  
		Last Modified: Tue, 01 Jul 2025 01:14:59 GMT  
		Size: 50.8 MB (50786756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d932d83e6c250bb0f5c2003ae98b3b4dc3d40d3915a7ebed763f315741368`  
		Last Modified: Tue, 01 Jul 2025 02:24:58 GMT  
		Size: 26.8 MB (26772148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34925744005802787be957c67125f2aabf94afd5e8609668cc037c46d09591`  
		Last Modified: Tue, 01 Jul 2025 03:20:07 GMT  
		Size: 69.8 MB (69830306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f64900f9b3ef26b18f567a74a96e250e42a8eed2ff1fadd54a41cc0359ad74`  
		Last Modified: Tue, 01 Jul 2025 13:17:44 GMT  
		Size: 239.9 MB (239860428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786dd06ef0c1d508b04b744e9509815e8b97edb82567dae2ecc2f7f4608eb087`  
		Last Modified: Thu, 03 Jul 2025 20:45:12 GMT  
		Size: 229.2 MB (229161713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:trixie` - unknown; unknown

```console
$ docker pull rust@sha256:f67a9186cf1554037b5bebdc2a29731e33b0560fb6f00acc72a972c06a6a8024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17182790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fa8116b6bed9af5ae6689a9a22779a1678697a915c5cd4d7e6b36066700e02`

```dockerfile
```

-	Layers:
	-	`sha256:0bc4ae22361d8be206beacebda88e0a0d9907d13fe49752729264b691a2573a4`  
		Last Modified: Thu, 03 Jul 2025 17:46:46 GMT  
		Size: 17.2 MB (17170867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00512048af2e89f74659ec4afeed8cb648de2fbc4c194e045bb7360d66547db4`  
		Last Modified: Thu, 03 Jul 2025 17:46:47 GMT  
		Size: 11.9 KB (11923 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:trixie` - linux; ppc64le

```console
$ docker pull rust@sha256:2b364c8eda85704eca9497cb33fca2d56eef23b799891c48db05140faffe245c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.9 MB (657910004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e48352ed179962dff629d52064abbff1ea21fc4849959f709243b2e442fae7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e868292aa714037cbba25d912564e5f392a5d355c383b03a8854e789c98ef`  
		Last Modified: Tue, 01 Jul 2025 05:08:57 GMT  
		Size: 27.0 MB (27003269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7107fc95f855d7880e921bbc85bf915f07c907c70d7d6f6a5334a32ad6c832`  
		Last Modified: Tue, 01 Jul 2025 10:12:36 GMT  
		Size: 73.1 MB (73068943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4744a5ce78804175c7109fb3df660a6bb53b2954bc5f2c48184739c714dfc8`  
		Last Modified: Thu, 03 Jul 2025 10:55:19 GMT  
		Size: 231.0 MB (231021360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7c94c7eb559acad5a878c6b10fbcb0ecafad636824170be34ede5261baa6a2`  
		Last Modified: Thu, 03 Jul 2025 20:46:35 GMT  
		Size: 273.7 MB (273719196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:trixie` - unknown; unknown

```console
$ docker pull rust@sha256:712f5014e1f676151678dfb32f438ebfc5c6ccce041ee1bfe0822c9f6e6a92b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17208092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e648406175ad5a0fff773fd402a380664ca93211dc1dc02b0e30ec1857290a`

```dockerfile
```

-	Layers:
	-	`sha256:e90c41129150eeb1baf61bb144eb1a5bf5136c3753a5e7ff747a93519edbced8`  
		Last Modified: Thu, 03 Jul 2025 17:47:19 GMT  
		Size: 17.2 MB (17196093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:223be277a3e6da23a3d10ec7c56a85066daeacf3199f6e2852aed61471673c6e`  
		Last Modified: Thu, 03 Jul 2025 17:47:20 GMT  
		Size: 12.0 KB (11999 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:trixie` - linux; s390x

```console
$ docker pull rust@sha256:b78680ff95452516a2a1ba080766115b52b09915350132aa95d221d83bb4a29f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 MB (634484977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b39c24e77ca6d3f82b32ead83f3c0c127e66c3c126e6397457389779e52ec7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 03 Jul 2025 10:53:28 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Jul 2025 10:53:28 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.88.0
# Thu, 03 Jul 2025 10:53:28 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8974c848015ae735631f879693069b8c536e3428274d79917837c027655a80`  
		Last Modified: Tue, 01 Jul 2025 05:31:56 GMT  
		Size: 26.8 MB (26785709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7360cccf58cfa285cf20d3ce14642c23bf3a2795b93396d0b9b743ee2e0779`  
		Last Modified: Tue, 01 Jul 2025 08:59:15 GMT  
		Size: 68.7 MB (68663824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694ce909d21b7fbf7c3fb87f40db93cf7588c89986fe25d341208d7b9ae60852`  
		Last Modified: Thu, 03 Jul 2025 10:55:27 GMT  
		Size: 206.3 MB (206329374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2362089a7d48f29102d6359bd8041b42be3e05af339f3916bfaefb996c680c`  
		Last Modified: Thu, 03 Jul 2025 20:47:14 GMT  
		Size: 283.4 MB (283362410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:trixie` - unknown; unknown

```console
$ docker pull rust@sha256:f0605e4fb8dba38beea68b41893e3e6983c85a8d7ebe00d7b438ec8414f6d6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17001023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fec9741de5a55dec8253a44c86e746da1d1ec5db93d53031d57e5006c179026`

```dockerfile
```

-	Layers:
	-	`sha256:56417f7df327de8d5d5e7e0de1e2f59e7226739f9c6c2324cd0165abb66c39d8`  
		Last Modified: Thu, 03 Jul 2025 17:47:40 GMT  
		Size: 17.0 MB (16989068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bba5fb71a8222ba1b28462e4175f250445ba54f02cf3948e9d08d931e57d0ec`  
		Last Modified: Thu, 03 Jul 2025 17:47:40 GMT  
		Size: 12.0 KB (11955 bytes)  
		MIME: application/vnd.in-toto+json
