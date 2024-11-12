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
$ docker pull rust@sha256:3da385318a04f89f7a8e5d12b0c7091f1cafc5805e160451394926c12101cd7b
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
$ docker pull rust@sha256:4d776039a9a357be19ca9ead57b0656a213619c7298982097a0857d5a605ac5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530870052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea03bd0e673bbc1777121a59412ca6c31511dbd935bcdd06c3ddb1ffe9ced63`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad67b816dd3ebfab16dd19d0768f67e218ed3070e064a66bfa1b026ea84191e`  
		Last Modified: Sat, 19 Oct 2024 08:07:03 GMT  
		Size: 175.2 MB (175210957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f62c598e0e4b12d38b7e9ac6d1e37417fddac22e7efa57555e76096c3484517`  
		Last Modified: Sat, 19 Oct 2024 20:27:03 GMT  
		Size: 228.9 MB (228918647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:4d72eab67be576c01e790395a1efc82aa1e3450e34f2c66965ed128ea73929c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7da09c2def11516f2cac29397dd79e45e13edd6a595770e1c583d3f89d9944c`

```dockerfile
```

-	Layers:
	-	`sha256:df68194a4679648dafbc2ce121470f555dc6c97bca93205f2b8b4d349281e903`  
		Last Modified: Sat, 19 Oct 2024 20:26:58 GMT  
		Size: 15.3 MB (15305316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a34b03d3951e72b491cfe93d2ef4efee2d02c129efc7f6c165735b24919d166`  
		Last Modified: Sat, 19 Oct 2024 20:26:57 GMT  
		Size: 13.3 KB (13259 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d82d65d48a0b6d0f5d39f7e8cdd1689fd2c6685007b66b4f021ee6e0704f642b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596180926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4bc4718cff8ac4db4e0cd8f6fb22ad73df411fc871ce08aa34e313e9e769cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d4884f85282b9a352dbcedf2cccd073a63e60b151be84375ce9279dec1c553`  
		Last Modified: Sat, 19 Oct 2024 06:16:07 GMT  
		Size: 202.6 MB (202644222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a5b77d8d49ee81a31cd491be54a349b09b6537083730e14be2f68804799c67`  
		Last Modified: Sat, 19 Oct 2024 20:04:17 GMT  
		Size: 256.0 MB (256007848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:a992d3d7fa41a9bf8aa6c833c923c0e21a0dc25a6c95ab6b972a3bf938e60bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f84fa5c1c33f2991055fe2dfed397aa3de67ebdee0e01aa4c66271fc8e2b46`

```dockerfile
```

-	Layers:
	-	`sha256:194d3ee80b090fdab62b570cc0b990cda05ace7cb3697e836047312452491f3e`  
		Last Modified: Sat, 19 Oct 2024 20:04:11 GMT  
		Size: 15.5 MB (15529783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2396872dec21a26fe49789692367fe840fd8d80316a7738dd410585be99ae02`  
		Last Modified: Sat, 19 Oct 2024 20:04:10 GMT  
		Size: 13.3 KB (13303 bytes)  
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
$ docker pull rust@sha256:565a7cef7c714e30d829290ac51d2523b887f2d9f4d75d56e1cee253d91331c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615970277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ee5a636017f864b10932ed1ffffaa50aae11a9cafbeb51f484d37b4d8bfdb9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
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
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3666a280304f3727f745e818ab5e252dd98676495517a360e23f821dee0fa6`  
		Last Modified: Sat, 19 Oct 2024 04:07:03 GMT  
		Size: 69.8 MB (69825530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81280667d7d6fa822ac7a45807cf98017526f614373fad289bacbeb84f61f73`  
		Last Modified: Sat, 19 Oct 2024 05:17:30 GMT  
		Size: 214.3 MB (214300420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd89c17397182837a76641fe74c5ac4688f9cd2afce20f782ae95d0846367cb`  
		Last Modified: Sat, 19 Oct 2024 19:43:12 GMT  
		Size: 252.6 MB (252582753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:55c7db0912be66850720729eb8e68d6d46fcb2806fb1121e3d3ea93c77ff6bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f618aee8535497d6062b875e019ec722cddc0c4322c0a5d64f34c366adb0dafa`

```dockerfile
```

-	Layers:
	-	`sha256:494207d1c19a9f9c9a8a4d0dc0e1f0c0633a0363ad0ec57ef7d284e49afb0805`  
		Last Modified: Sat, 19 Oct 2024 19:42:48 GMT  
		Size: 15.5 MB (15475454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22834bd3dee1022aa23492cd8fbb261876cccacd3df3528af3474cb30116f067`  
		Last Modified: Sat, 19 Oct 2024 19:42:45 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:6713c368dfe236fe7be2509ddce84bf70cca0af2dc709d903ae1ce92be79cd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597392132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda7509db578b0d8f0347aa0bd40839f820e2765c0c04f5b130d0576bac6b6d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
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
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2eccbc8d9b18898de6fc12769f52101d4af82f32957d095f8ab217c6886c2e`  
		Last Modified: Sat, 19 Oct 2024 05:04:19 GMT  
		Size: 183.3 MB (183299744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3c72db5de57d361c959f82e0a383ee33cd8c91b7fecf0aa70ac994ea864dea`  
		Last Modified: Sat, 19 Oct 2024 16:02:42 GMT  
		Size: 278.6 MB (278608964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:71ed314b5bcc9dfacb1b917dad0530f8b0b9c8cf5b0ddbc9493bcc04cbd1bab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6641dd5f17c0fcc76f37070190c900b941c711d4bea89b3494702d5090279d`

```dockerfile
```

-	Layers:
	-	`sha256:eb80b4b6b53506fb47fce58bfe36989307286364157f2aee1c04ae0541182d5e`  
		Last Modified: Sat, 19 Oct 2024 16:02:36 GMT  
		Size: 15.3 MB (15313614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b27a840fe6712fe1894cbbf106e9afa7c2de5d825a7891252b2e6d2004405e`  
		Last Modified: Sat, 19 Oct 2024 16:02:34 GMT  
		Size: 13.2 KB (13151 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:00c2107fa0e7a3eecf1fb31c814cd11a450026fae3fe375a1eed141be5fe75bc
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
$ docker pull rust@sha256:cc55868374fa1817218125ef6c0ef12201e2787cb400e941fbab95cb03e4dce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8955b5af103ec2e50ddf887aa77173599a206f1bd158b9f60531e84aeaf27c5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e451e7d55fdf7e0ddcc65ceb40f1e7f11a0c8e3188735a9d77443640951d42`  
		Last Modified: Fri, 18 Oct 2024 00:31:10 GMT  
		Size: 52.9 MB (52946227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67db9729fe0f06f4a5f2a64007565ed87dad3e2955a71d1f5b31eb1992c1ee77`  
		Last Modified: Fri, 18 Oct 2024 00:31:13 GMT  
		Size: 241.8 MB (241799131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:7fa5fb93c33118b5ace2225168e3a66220b4a4f7c0ea94b599f22a39649623fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 KB (758862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc1bc460aee8e1e08dfb95db95786730c4a0b58aec5352403da9bd51c50c52d`

```dockerfile
```

-	Layers:
	-	`sha256:8b91b6f48c74e79f8c38eef16aa7af99c79834dcac8ab6ee8c27425433e72b2c`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 747.0 KB (746984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5587688eb47137d37d13b14e84da8cc45bdc8079dd0cd8f15d98eb2ee4cc79fb`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 11.9 KB (11878 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:fcd6117426b140d94e833c54c6e05612c1fa15d9f065b7ca21f7a266a8327870
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
$ docker pull rust@sha256:499c93a743c096822c3ce050e96df3f22ceb5abf517422c3cfc3e34be779b334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298153503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb195d39c948c729c2a621ced30c3cb838d44b72fc12084fe9c364ba5daaf1c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832c2f560bcd7cc2071a2ff7b80d28d566d9bc6644db81915a561a051e27d00e`  
		Last Modified: Fri, 18 Oct 2024 00:29:56 GMT  
		Size: 53.0 MB (52995407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e9dcbde1ac8d276d321ba07f80f05e9ffee4fae318dae571a76d7cf5264f3c`  
		Last Modified: Fri, 18 Oct 2024 00:30:00 GMT  
		Size: 241.8 MB (241798993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:985e97b0beed650244a2e606b90ea14955f2e370312715ead82e5c874bb39aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.0 KB (760049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e44d5402fbaee4e101aecb1bf614fdbb58f6c24413a149931fd7cfc97b7621`

```dockerfile
```

-	Layers:
	-	`sha256:7f55f4dc6a64459bf97682966e85d4d3faaa31836315dd9bd160eea17bc2a50f`  
		Last Modified: Fri, 18 Oct 2024 00:29:55 GMT  
		Size: 749.4 KB (749423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8624b8420bd192f3fcc11e096d27439030ddff55ca81b0b89530581ea062c2a9`  
		Last Modified: Fri, 18 Oct 2024 00:29:55 GMT  
		Size: 10.6 KB (10626 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:00c2107fa0e7a3eecf1fb31c814cd11a450026fae3fe375a1eed141be5fe75bc
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
$ docker pull rust@sha256:cc55868374fa1817218125ef6c0ef12201e2787cb400e941fbab95cb03e4dce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8955b5af103ec2e50ddf887aa77173599a206f1bd158b9f60531e84aeaf27c5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e451e7d55fdf7e0ddcc65ceb40f1e7f11a0c8e3188735a9d77443640951d42`  
		Last Modified: Fri, 18 Oct 2024 00:31:10 GMT  
		Size: 52.9 MB (52946227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67db9729fe0f06f4a5f2a64007565ed87dad3e2955a71d1f5b31eb1992c1ee77`  
		Last Modified: Fri, 18 Oct 2024 00:31:13 GMT  
		Size: 241.8 MB (241799131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:7fa5fb93c33118b5ace2225168e3a66220b4a4f7c0ea94b599f22a39649623fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 KB (758862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc1bc460aee8e1e08dfb95db95786730c4a0b58aec5352403da9bd51c50c52d`

```dockerfile
```

-	Layers:
	-	`sha256:8b91b6f48c74e79f8c38eef16aa7af99c79834dcac8ab6ee8c27425433e72b2c`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 747.0 KB (746984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5587688eb47137d37d13b14e84da8cc45bdc8079dd0cd8f15d98eb2ee4cc79fb`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 11.9 KB (11878 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:3da385318a04f89f7a8e5d12b0c7091f1cafc5805e160451394926c12101cd7b
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
$ docker pull rust@sha256:4d776039a9a357be19ca9ead57b0656a213619c7298982097a0857d5a605ac5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530870052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea03bd0e673bbc1777121a59412ca6c31511dbd935bcdd06c3ddb1ffe9ced63`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad67b816dd3ebfab16dd19d0768f67e218ed3070e064a66bfa1b026ea84191e`  
		Last Modified: Sat, 19 Oct 2024 08:07:03 GMT  
		Size: 175.2 MB (175210957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f62c598e0e4b12d38b7e9ac6d1e37417fddac22e7efa57555e76096c3484517`  
		Last Modified: Sat, 19 Oct 2024 20:27:03 GMT  
		Size: 228.9 MB (228918647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4d72eab67be576c01e790395a1efc82aa1e3450e34f2c66965ed128ea73929c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7da09c2def11516f2cac29397dd79e45e13edd6a595770e1c583d3f89d9944c`

```dockerfile
```

-	Layers:
	-	`sha256:df68194a4679648dafbc2ce121470f555dc6c97bca93205f2b8b4d349281e903`  
		Last Modified: Sat, 19 Oct 2024 20:26:58 GMT  
		Size: 15.3 MB (15305316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a34b03d3951e72b491cfe93d2ef4efee2d02c129efc7f6c165735b24919d166`  
		Last Modified: Sat, 19 Oct 2024 20:26:57 GMT  
		Size: 13.3 KB (13259 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d82d65d48a0b6d0f5d39f7e8cdd1689fd2c6685007b66b4f021ee6e0704f642b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596180926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4bc4718cff8ac4db4e0cd8f6fb22ad73df411fc871ce08aa34e313e9e769cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d4884f85282b9a352dbcedf2cccd073a63e60b151be84375ce9279dec1c553`  
		Last Modified: Sat, 19 Oct 2024 06:16:07 GMT  
		Size: 202.6 MB (202644222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a5b77d8d49ee81a31cd491be54a349b09b6537083730e14be2f68804799c67`  
		Last Modified: Sat, 19 Oct 2024 20:04:17 GMT  
		Size: 256.0 MB (256007848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a992d3d7fa41a9bf8aa6c833c923c0e21a0dc25a6c95ab6b972a3bf938e60bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f84fa5c1c33f2991055fe2dfed397aa3de67ebdee0e01aa4c66271fc8e2b46`

```dockerfile
```

-	Layers:
	-	`sha256:194d3ee80b090fdab62b570cc0b990cda05ace7cb3697e836047312452491f3e`  
		Last Modified: Sat, 19 Oct 2024 20:04:11 GMT  
		Size: 15.5 MB (15529783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2396872dec21a26fe49789692367fe840fd8d80316a7738dd410585be99ae02`  
		Last Modified: Sat, 19 Oct 2024 20:04:10 GMT  
		Size: 13.3 KB (13303 bytes)  
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
$ docker pull rust@sha256:565a7cef7c714e30d829290ac51d2523b887f2d9f4d75d56e1cee253d91331c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615970277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ee5a636017f864b10932ed1ffffaa50aae11a9cafbeb51f484d37b4d8bfdb9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
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
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3666a280304f3727f745e818ab5e252dd98676495517a360e23f821dee0fa6`  
		Last Modified: Sat, 19 Oct 2024 04:07:03 GMT  
		Size: 69.8 MB (69825530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81280667d7d6fa822ac7a45807cf98017526f614373fad289bacbeb84f61f73`  
		Last Modified: Sat, 19 Oct 2024 05:17:30 GMT  
		Size: 214.3 MB (214300420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd89c17397182837a76641fe74c5ac4688f9cd2afce20f782ae95d0846367cb`  
		Last Modified: Sat, 19 Oct 2024 19:43:12 GMT  
		Size: 252.6 MB (252582753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:55c7db0912be66850720729eb8e68d6d46fcb2806fb1121e3d3ea93c77ff6bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f618aee8535497d6062b875e019ec722cddc0c4322c0a5d64f34c366adb0dafa`

```dockerfile
```

-	Layers:
	-	`sha256:494207d1c19a9f9c9a8a4d0dc0e1f0c0633a0363ad0ec57ef7d284e49afb0805`  
		Last Modified: Sat, 19 Oct 2024 19:42:48 GMT  
		Size: 15.5 MB (15475454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22834bd3dee1022aa23492cd8fbb261876cccacd3df3528af3474cb30116f067`  
		Last Modified: Sat, 19 Oct 2024 19:42:45 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:6713c368dfe236fe7be2509ddce84bf70cca0af2dc709d903ae1ce92be79cd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597392132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda7509db578b0d8f0347aa0bd40839f820e2765c0c04f5b130d0576bac6b6d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
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
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2eccbc8d9b18898de6fc12769f52101d4af82f32957d095f8ab217c6886c2e`  
		Last Modified: Sat, 19 Oct 2024 05:04:19 GMT  
		Size: 183.3 MB (183299744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3c72db5de57d361c959f82e0a383ee33cd8c91b7fecf0aa70ac994ea864dea`  
		Last Modified: Sat, 19 Oct 2024 16:02:42 GMT  
		Size: 278.6 MB (278608964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:71ed314b5bcc9dfacb1b917dad0530f8b0b9c8cf5b0ddbc9493bcc04cbd1bab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6641dd5f17c0fcc76f37070190c900b941c711d4bea89b3494702d5090279d`

```dockerfile
```

-	Layers:
	-	`sha256:eb80b4b6b53506fb47fce58bfe36989307286364157f2aee1c04ae0541182d5e`  
		Last Modified: Sat, 19 Oct 2024 16:02:36 GMT  
		Size: 15.3 MB (15313614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b27a840fe6712fe1894cbbf106e9afa7c2de5d825a7891252b2e6d2004405e`  
		Last Modified: Sat, 19 Oct 2024 16:02:34 GMT  
		Size: 13.2 KB (13151 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:f60dc7ea30e61d39082e0cbf1f92d951e0d5fda2e4a509dd3ed2d5a42e0c4e20
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
$ docker pull rust@sha256:8af7361ea620d72c1f9a173332d936485d3e6ada68c1fc7cf010c8c5e12ec581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.2 MB (512163900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9997bd184a1622957654856fc5ebe3fc26090106fd7183f192aa70de6f36a9e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
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
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a9032c7c4d1cfb31e96212773919f51ec2f6be760fc0f5c35bafbcdb50249`  
		Last Modified: Sat, 19 Oct 2024 06:37:59 GMT  
		Size: 50.6 MB (50613654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0525b656ff73752501ad6cdcf4137840983e49d8b07af0619e3185c5e925fb`  
		Last Modified: Sat, 19 Oct 2024 08:10:07 GMT  
		Size: 167.5 MB (167512354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c43aa88ff2e8544cbb34cb7bc9c4263de3a33dd12595b204ddf8969b943c22`  
		Last Modified: Sat, 19 Oct 2024 20:24:39 GMT  
		Size: 228.9 MB (228918612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c92ce165138230bdc8d92f2774f21b6ff173b0a20a5817d01af1f5b7bb149a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14912080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2d3bb2dd404797f5454017dbdbca9674cf2163035f688ddc8b718e10fb12e`

```dockerfile
```

-	Layers:
	-	`sha256:141db802f68f589a42b222b577ef6b35b39a754ffec66c5715966c6312b9a949`  
		Last Modified: Sat, 19 Oct 2024 20:24:34 GMT  
		Size: 14.9 MB (14900743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e125043ad782c9f35d6018b39446890cd253c6e05a61acee96b6c9d0052428`  
		Last Modified: Sat, 19 Oct 2024 20:24:34 GMT  
		Size: 11.3 KB (11337 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f70e8bd2b2868a1f0cb7a711bb71f74ee77fbc2dd33c0d956251e955e323e21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.3 MB (570294243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3f4d291ce1ea3d241dd96079dafcf5d00bd4f99ec210b356e5bad749185461`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc6072bf5318ca0f9f250b4fcc6254d92483650689f0b0d77274be187abd96`  
		Last Modified: Sat, 19 Oct 2024 05:18:19 GMT  
		Size: 54.8 MB (54832658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13f3e7a61817231ad609702b6918e16648b3eec453567dbedd80952df7e3957`  
		Last Modified: Sat, 19 Oct 2024 06:17:47 GMT  
		Size: 190.0 MB (189971242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93765710d73d66b5b4443516a375c9c981b9ecd07f1ac581fefb956b0624a66`  
		Last Modified: Sat, 19 Oct 2024 20:02:46 GMT  
		Size: 256.0 MB (256007659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e45140ffd2b699e4c5cbdfb96804f7d756a9b862ee163f7d8c74947743b5c51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15113859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d173d7479537f73d26bb16b761a8a0265ca5a070e525ee96191099186ac199f`

```dockerfile
```

-	Layers:
	-	`sha256:38be245007626b5bcaf4d9ab6bc3f6f6e7a944590c035bed3647f40f3ea3fe34`  
		Last Modified: Sat, 19 Oct 2024 20:02:40 GMT  
		Size: 15.1 MB (15102494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcf7d213da88bc30da54c88258c32d3eb563da066517dfdede3d0f2ebfc82ca`  
		Last Modified: Sat, 19 Oct 2024 20:02:40 GMT  
		Size: 11.4 KB (11365 bytes)  
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
$ docker pull rust@sha256:60fe5b3207c39d9d52d2b1cc5075f4c71ca7a3ed23dbfa96a19747dafba99afc
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
$ docker pull rust@sha256:6af06831c441ea6efe5da0841875f10c9143e27e2068f7971dc3cb4493777c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301463797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5193a64b31f6521a36ef2a9b1ff2e63c0b09ec71e19c880765a69322380ad8a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65593264902c7ef0684f69975da9c31f1d677a35eb904b8858d752363894bbf`  
		Last Modified: Fri, 18 Oct 2024 04:55:44 GMT  
		Size: 276.7 MB (276745600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:07cd606a2467e9c8ca156915edf6217316d0b6102a08aaa068ce38398d0c8da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec8d2eea1e2fdd0cab72470cfea9e17ba71367f3f8771d876e8f0b01f29744f`

```dockerfile
```

-	Layers:
	-	`sha256:51505a3fb8a002b908713bda6232480bf93d778a2cd307af0732ff66d0af4ef5`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01fab3537dc20a8b760c33a1bcf432402dbbb9e1378901458dee5bc53c51dfb`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 13.2 KB (13194 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:24cfb92a68669bf577b74a7a6e12046851b9d153e0de06e8f902d0aec217ec39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350996361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b376079c1d1c0d19aac1a6d084bdffe036f9c6a0cafab7d6301be6434ac5790d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e35824bcc3a12d7039bc1e45a08bce002fd267d99d1978d3b01ce7613413cd`  
		Last Modified: Fri, 18 Oct 2024 00:28:42 GMT  
		Size: 321.8 MB (321840020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:5a8b2746c65775e6acb4139b0071e720fcddaf9949803347ff1cce9ace3ee2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781b40760ab6bde89d9fd1eaf24672d71f8b0a1557e490646521a2255e054848`

```dockerfile
```

-	Layers:
	-	`sha256:3999435d6d71bfb3d6d5d77e720ef535934122b4b4f23ea3c3b74509b2121080`  
		Last Modified: Fri, 18 Oct 2024 00:28:36 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fbee966e4be75c4c34c2a283707d8db1c220c6dea79aeb970bbd1412776002`  
		Last Modified: Fri, 18 Oct 2024 00:28:35 GMT  
		Size: 13.2 KB (13238 bytes)  
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
$ docker pull rust@sha256:3b3291ce9a66c2810bda45239d5a3204156862ad19a2242f33677249a8cfc792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f37690e23b0d7eeacf9b82ad65ea93c3515164fe329039cf6c3b68b52eadd38`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f43badb6d18c1b7c35c88dd66c3530d7112c29ed622050dccf5b67e8e87040a`  
		Last Modified: Fri, 18 Oct 2024 01:11:21 GMT  
		Size: 321.3 MB (321340278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:cdb656b3036da27b5de1f8da7a2c7649b503346c968c5e98576e50967daafe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c71fdc69f1717530372cc23714c3698b5e2188adf646bb78da5df4383806808`

```dockerfile
```

-	Layers:
	-	`sha256:27eade1d9d895465bc2b8901153021d7ed125b6b270e683c41f8f3fa762fd2ad`  
		Last Modified: Fri, 18 Oct 2024 01:11:13 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d343e81522d031d59cbf59c4478117043e268a002fcae2252af4afee8edfd6`  
		Last Modified: Fri, 18 Oct 2024 01:11:12 GMT  
		Size: 13.2 KB (13154 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:2f15097849b373f3334d043a19a1e2aed41324dfe17969afe5982cb7870d126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356216165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa853f32b6e73890d038285e2b30fc11040dbc95793ddf7db9c55e6742d91af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203d547d95b548a5a647f46a5b304047a4084df212db4a5188e5db5983b530ca`  
		Last Modified: Thu, 17 Oct 2024 23:42:15 GMT  
		Size: 328.7 MB (328726081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:00ee1eca709e062e0adb277cb380fda87dcf1a4a441f517506dca62708eec1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7433567ec5ed96973704f1f3f0a3c1175fc80bab52299c7609f52801f6ddf80`

```dockerfile
```

-	Layers:
	-	`sha256:3a52844eec2dcfc9ce0941a96703ef6a9183abefb170c89f7aaddc53cafa57fc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca49a9d06e01cc7a03e2c5215a23b874c4216aec674651cc808436288f055cc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 13.1 KB (13091 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:60fe5b3207c39d9d52d2b1cc5075f4c71ca7a3ed23dbfa96a19747dafba99afc
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
$ docker pull rust@sha256:6af06831c441ea6efe5da0841875f10c9143e27e2068f7971dc3cb4493777c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301463797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5193a64b31f6521a36ef2a9b1ff2e63c0b09ec71e19c880765a69322380ad8a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65593264902c7ef0684f69975da9c31f1d677a35eb904b8858d752363894bbf`  
		Last Modified: Fri, 18 Oct 2024 04:55:44 GMT  
		Size: 276.7 MB (276745600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:07cd606a2467e9c8ca156915edf6217316d0b6102a08aaa068ce38398d0c8da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec8d2eea1e2fdd0cab72470cfea9e17ba71367f3f8771d876e8f0b01f29744f`

```dockerfile
```

-	Layers:
	-	`sha256:51505a3fb8a002b908713bda6232480bf93d778a2cd307af0732ff66d0af4ef5`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01fab3537dc20a8b760c33a1bcf432402dbbb9e1378901458dee5bc53c51dfb`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 13.2 KB (13194 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:24cfb92a68669bf577b74a7a6e12046851b9d153e0de06e8f902d0aec217ec39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350996361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b376079c1d1c0d19aac1a6d084bdffe036f9c6a0cafab7d6301be6434ac5790d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e35824bcc3a12d7039bc1e45a08bce002fd267d99d1978d3b01ce7613413cd`  
		Last Modified: Fri, 18 Oct 2024 00:28:42 GMT  
		Size: 321.8 MB (321840020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5a8b2746c65775e6acb4139b0071e720fcddaf9949803347ff1cce9ace3ee2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781b40760ab6bde89d9fd1eaf24672d71f8b0a1557e490646521a2255e054848`

```dockerfile
```

-	Layers:
	-	`sha256:3999435d6d71bfb3d6d5d77e720ef535934122b4b4f23ea3c3b74509b2121080`  
		Last Modified: Fri, 18 Oct 2024 00:28:36 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fbee966e4be75c4c34c2a283707d8db1c220c6dea79aeb970bbd1412776002`  
		Last Modified: Fri, 18 Oct 2024 00:28:35 GMT  
		Size: 13.2 KB (13238 bytes)  
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
$ docker pull rust@sha256:3b3291ce9a66c2810bda45239d5a3204156862ad19a2242f33677249a8cfc792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f37690e23b0d7eeacf9b82ad65ea93c3515164fe329039cf6c3b68b52eadd38`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f43badb6d18c1b7c35c88dd66c3530d7112c29ed622050dccf5b67e8e87040a`  
		Last Modified: Fri, 18 Oct 2024 01:11:21 GMT  
		Size: 321.3 MB (321340278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:cdb656b3036da27b5de1f8da7a2c7649b503346c968c5e98576e50967daafe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c71fdc69f1717530372cc23714c3698b5e2188adf646bb78da5df4383806808`

```dockerfile
```

-	Layers:
	-	`sha256:27eade1d9d895465bc2b8901153021d7ed125b6b270e683c41f8f3fa762fd2ad`  
		Last Modified: Fri, 18 Oct 2024 01:11:13 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d343e81522d031d59cbf59c4478117043e268a002fcae2252af4afee8edfd6`  
		Last Modified: Fri, 18 Oct 2024 01:11:12 GMT  
		Size: 13.2 KB (13154 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:2f15097849b373f3334d043a19a1e2aed41324dfe17969afe5982cb7870d126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356216165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa853f32b6e73890d038285e2b30fc11040dbc95793ddf7db9c55e6742d91af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203d547d95b548a5a647f46a5b304047a4084df212db4a5188e5db5983b530ca`  
		Last Modified: Thu, 17 Oct 2024 23:42:15 GMT  
		Size: 328.7 MB (328726081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:00ee1eca709e062e0adb277cb380fda87dcf1a4a441f517506dca62708eec1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7433567ec5ed96973704f1f3f0a3c1175fc80bab52299c7609f52801f6ddf80`

```dockerfile
```

-	Layers:
	-	`sha256:3a52844eec2dcfc9ce0941a96703ef6a9183abefb170c89f7aaddc53cafa57fc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca49a9d06e01cc7a03e2c5215a23b874c4216aec674651cc808436288f055cc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 13.1 KB (13091 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:6ecf4bda0e2b5e7f4610ac8612bc6e01adb3f4451dd8ff16b160be6e07d8c054
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
$ docker pull rust@sha256:cb4937b32194f99b394b565b351807eaa88ca11ad728ccd77ac3f29d3670f85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297762491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789d4d1356befa56ac46e1dd3002047d504df6604c5f112c786846745c11d493`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:45 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Thu, 17 Oct 2024 03:03:46 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f127f81679252c87ada20a6442aab050daaa6280455d330c2ed0e0312ad263`  
		Last Modified: Fri, 18 Oct 2024 04:51:41 GMT  
		Size: 271.2 MB (271172936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7a86756242f0ba3629f641732e0444d8519cb35f5436097966d6e2355c809fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811a4eb5f5f1ce78ce34703dd8554a6e58cbaa0edff11528ac95ebe6d7ca1dcc`

```dockerfile
```

-	Layers:
	-	`sha256:75b8d4d1890e668869883ff090be72445c0bb046190b26558bc015fabccc07b2`  
		Last Modified: Fri, 18 Oct 2024 04:51:36 GMT  
		Size: 4.0 MB (3973767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241f7e92e93b1ef933ca9018e07bab3fb08cc5e31e31246cb29b3057f6c83402`  
		Last Modified: Fri, 18 Oct 2024 04:51:35 GMT  
		Size: 11.2 KB (11246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d453636ade10ddd4286ec5ecdcb24f1a99cedccc09c5c13ad7289b53d33cd31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341766510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e871be81f15e4e120ba9ff8708fa70d21e83ce85e0870e19adae88e2bf2c6e86`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548d0c25fc9eeb4d349077a60a496f321d329205b3f5b06ef193b2adda85c179`  
		Last Modified: Fri, 18 Oct 2024 00:24:20 GMT  
		Size: 311.7 MB (311690753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5ea1413c96faa2e8729eafce7b57890ee56fa150674852e2b38ade7b654fb007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4172471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524fb398c788a87e7ea0b080c814f8340c81e2417be3e25f1b4537c834c21b72`

```dockerfile
```

-	Layers:
	-	`sha256:11b63d16de5274387c9f87faa0b807ce8c15e3150180bddf60776c4ff0e857a7`  
		Last Modified: Fri, 18 Oct 2024 00:24:13 GMT  
		Size: 4.2 MB (4161198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b701d88e21beef1d4a70fdc8b97a5303b2415f3728fdbbef255b1db4950a6e3f`  
		Last Modified: Fri, 18 Oct 2024 00:24:13 GMT  
		Size: 11.3 KB (11273 bytes)  
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
$ docker pull rust@sha256:3da385318a04f89f7a8e5d12b0c7091f1cafc5805e160451394926c12101cd7b
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
$ docker pull rust@sha256:4d776039a9a357be19ca9ead57b0656a213619c7298982097a0857d5a605ac5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530870052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea03bd0e673bbc1777121a59412ca6c31511dbd935bcdd06c3ddb1ffe9ced63`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad67b816dd3ebfab16dd19d0768f67e218ed3070e064a66bfa1b026ea84191e`  
		Last Modified: Sat, 19 Oct 2024 08:07:03 GMT  
		Size: 175.2 MB (175210957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f62c598e0e4b12d38b7e9ac6d1e37417fddac22e7efa57555e76096c3484517`  
		Last Modified: Sat, 19 Oct 2024 20:27:03 GMT  
		Size: 228.9 MB (228918647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82` - unknown; unknown

```console
$ docker pull rust@sha256:4d72eab67be576c01e790395a1efc82aa1e3450e34f2c66965ed128ea73929c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7da09c2def11516f2cac29397dd79e45e13edd6a595770e1c583d3f89d9944c`

```dockerfile
```

-	Layers:
	-	`sha256:df68194a4679648dafbc2ce121470f555dc6c97bca93205f2b8b4d349281e903`  
		Last Modified: Sat, 19 Oct 2024 20:26:58 GMT  
		Size: 15.3 MB (15305316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a34b03d3951e72b491cfe93d2ef4efee2d02c129efc7f6c165735b24919d166`  
		Last Modified: Sat, 19 Oct 2024 20:26:57 GMT  
		Size: 13.3 KB (13259 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d82d65d48a0b6d0f5d39f7e8cdd1689fd2c6685007b66b4f021ee6e0704f642b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596180926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4bc4718cff8ac4db4e0cd8f6fb22ad73df411fc871ce08aa34e313e9e769cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d4884f85282b9a352dbcedf2cccd073a63e60b151be84375ce9279dec1c553`  
		Last Modified: Sat, 19 Oct 2024 06:16:07 GMT  
		Size: 202.6 MB (202644222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a5b77d8d49ee81a31cd491be54a349b09b6537083730e14be2f68804799c67`  
		Last Modified: Sat, 19 Oct 2024 20:04:17 GMT  
		Size: 256.0 MB (256007848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82` - unknown; unknown

```console
$ docker pull rust@sha256:a992d3d7fa41a9bf8aa6c833c923c0e21a0dc25a6c95ab6b972a3bf938e60bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f84fa5c1c33f2991055fe2dfed397aa3de67ebdee0e01aa4c66271fc8e2b46`

```dockerfile
```

-	Layers:
	-	`sha256:194d3ee80b090fdab62b570cc0b990cda05ace7cb3697e836047312452491f3e`  
		Last Modified: Sat, 19 Oct 2024 20:04:11 GMT  
		Size: 15.5 MB (15529783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2396872dec21a26fe49789692367fe840fd8d80316a7738dd410585be99ae02`  
		Last Modified: Sat, 19 Oct 2024 20:04:10 GMT  
		Size: 13.3 KB (13303 bytes)  
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
$ docker pull rust@sha256:565a7cef7c714e30d829290ac51d2523b887f2d9f4d75d56e1cee253d91331c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615970277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ee5a636017f864b10932ed1ffffaa50aae11a9cafbeb51f484d37b4d8bfdb9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
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
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3666a280304f3727f745e818ab5e252dd98676495517a360e23f821dee0fa6`  
		Last Modified: Sat, 19 Oct 2024 04:07:03 GMT  
		Size: 69.8 MB (69825530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81280667d7d6fa822ac7a45807cf98017526f614373fad289bacbeb84f61f73`  
		Last Modified: Sat, 19 Oct 2024 05:17:30 GMT  
		Size: 214.3 MB (214300420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd89c17397182837a76641fe74c5ac4688f9cd2afce20f782ae95d0846367cb`  
		Last Modified: Sat, 19 Oct 2024 19:43:12 GMT  
		Size: 252.6 MB (252582753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82` - unknown; unknown

```console
$ docker pull rust@sha256:55c7db0912be66850720729eb8e68d6d46fcb2806fb1121e3d3ea93c77ff6bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f618aee8535497d6062b875e019ec722cddc0c4322c0a5d64f34c366adb0dafa`

```dockerfile
```

-	Layers:
	-	`sha256:494207d1c19a9f9c9a8a4d0dc0e1f0c0633a0363ad0ec57ef7d284e49afb0805`  
		Last Modified: Sat, 19 Oct 2024 19:42:48 GMT  
		Size: 15.5 MB (15475454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22834bd3dee1022aa23492cd8fbb261876cccacd3df3528af3474cb30116f067`  
		Last Modified: Sat, 19 Oct 2024 19:42:45 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82` - linux; s390x

```console
$ docker pull rust@sha256:6713c368dfe236fe7be2509ddce84bf70cca0af2dc709d903ae1ce92be79cd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597392132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda7509db578b0d8f0347aa0bd40839f820e2765c0c04f5b130d0576bac6b6d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
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
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2eccbc8d9b18898de6fc12769f52101d4af82f32957d095f8ab217c6886c2e`  
		Last Modified: Sat, 19 Oct 2024 05:04:19 GMT  
		Size: 183.3 MB (183299744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3c72db5de57d361c959f82e0a383ee33cd8c91b7fecf0aa70ac994ea864dea`  
		Last Modified: Sat, 19 Oct 2024 16:02:42 GMT  
		Size: 278.6 MB (278608964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82` - unknown; unknown

```console
$ docker pull rust@sha256:71ed314b5bcc9dfacb1b917dad0530f8b0b9c8cf5b0ddbc9493bcc04cbd1bab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6641dd5f17c0fcc76f37070190c900b941c711d4bea89b3494702d5090279d`

```dockerfile
```

-	Layers:
	-	`sha256:eb80b4b6b53506fb47fce58bfe36989307286364157f2aee1c04ae0541182d5e`  
		Last Modified: Sat, 19 Oct 2024 16:02:36 GMT  
		Size: 15.3 MB (15313614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b27a840fe6712fe1894cbbf106e9afa7c2de5d825a7891252b2e6d2004405e`  
		Last Modified: Sat, 19 Oct 2024 16:02:34 GMT  
		Size: 13.2 KB (13151 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82-alpine`

```console
$ docker pull rust@sha256:00c2107fa0e7a3eecf1fb31c814cd11a450026fae3fe375a1eed141be5fe75bc
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
$ docker pull rust@sha256:cc55868374fa1817218125ef6c0ef12201e2787cb400e941fbab95cb03e4dce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8955b5af103ec2e50ddf887aa77173599a206f1bd158b9f60531e84aeaf27c5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e451e7d55fdf7e0ddcc65ceb40f1e7f11a0c8e3188735a9d77443640951d42`  
		Last Modified: Fri, 18 Oct 2024 00:31:10 GMT  
		Size: 52.9 MB (52946227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67db9729fe0f06f4a5f2a64007565ed87dad3e2955a71d1f5b31eb1992c1ee77`  
		Last Modified: Fri, 18 Oct 2024 00:31:13 GMT  
		Size: 241.8 MB (241799131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:7fa5fb93c33118b5ace2225168e3a66220b4a4f7c0ea94b599f22a39649623fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 KB (758862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc1bc460aee8e1e08dfb95db95786730c4a0b58aec5352403da9bd51c50c52d`

```dockerfile
```

-	Layers:
	-	`sha256:8b91b6f48c74e79f8c38eef16aa7af99c79834dcac8ab6ee8c27425433e72b2c`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 747.0 KB (746984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5587688eb47137d37d13b14e84da8cc45bdc8079dd0cd8f15d98eb2ee4cc79fb`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 11.9 KB (11878 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82-alpine3.19`

```console
$ docker pull rust@sha256:fcd6117426b140d94e833c54c6e05612c1fa15d9f065b7ca21f7a266a8327870
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
$ docker pull rust@sha256:499c93a743c096822c3ce050e96df3f22ceb5abf517422c3cfc3e34be779b334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298153503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb195d39c948c729c2a621ced30c3cb838d44b72fc12084fe9c364ba5daaf1c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832c2f560bcd7cc2071a2ff7b80d28d566d9bc6644db81915a561a051e27d00e`  
		Last Modified: Fri, 18 Oct 2024 00:29:56 GMT  
		Size: 53.0 MB (52995407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e9dcbde1ac8d276d321ba07f80f05e9ffee4fae318dae571a76d7cf5264f3c`  
		Last Modified: Fri, 18 Oct 2024 00:30:00 GMT  
		Size: 241.8 MB (241798993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:985e97b0beed650244a2e606b90ea14955f2e370312715ead82e5c874bb39aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.0 KB (760049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e44d5402fbaee4e101aecb1bf614fdbb58f6c24413a149931fd7cfc97b7621`

```dockerfile
```

-	Layers:
	-	`sha256:7f55f4dc6a64459bf97682966e85d4d3faaa31836315dd9bd160eea17bc2a50f`  
		Last Modified: Fri, 18 Oct 2024 00:29:55 GMT  
		Size: 749.4 KB (749423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8624b8420bd192f3fcc11e096d27439030ddff55ca81b0b89530581ea062c2a9`  
		Last Modified: Fri, 18 Oct 2024 00:29:55 GMT  
		Size: 10.6 KB (10626 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82-alpine3.20`

```console
$ docker pull rust@sha256:00c2107fa0e7a3eecf1fb31c814cd11a450026fae3fe375a1eed141be5fe75bc
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
$ docker pull rust@sha256:cc55868374fa1817218125ef6c0ef12201e2787cb400e941fbab95cb03e4dce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8955b5af103ec2e50ddf887aa77173599a206f1bd158b9f60531e84aeaf27c5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e451e7d55fdf7e0ddcc65ceb40f1e7f11a0c8e3188735a9d77443640951d42`  
		Last Modified: Fri, 18 Oct 2024 00:31:10 GMT  
		Size: 52.9 MB (52946227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67db9729fe0f06f4a5f2a64007565ed87dad3e2955a71d1f5b31eb1992c1ee77`  
		Last Modified: Fri, 18 Oct 2024 00:31:13 GMT  
		Size: 241.8 MB (241799131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:7fa5fb93c33118b5ace2225168e3a66220b4a4f7c0ea94b599f22a39649623fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 KB (758862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc1bc460aee8e1e08dfb95db95786730c4a0b58aec5352403da9bd51c50c52d`

```dockerfile
```

-	Layers:
	-	`sha256:8b91b6f48c74e79f8c38eef16aa7af99c79834dcac8ab6ee8c27425433e72b2c`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 747.0 KB (746984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5587688eb47137d37d13b14e84da8cc45bdc8079dd0cd8f15d98eb2ee4cc79fb`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 11.9 KB (11878 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82-bookworm`

```console
$ docker pull rust@sha256:3da385318a04f89f7a8e5d12b0c7091f1cafc5805e160451394926c12101cd7b
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
$ docker pull rust@sha256:4d776039a9a357be19ca9ead57b0656a213619c7298982097a0857d5a605ac5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530870052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea03bd0e673bbc1777121a59412ca6c31511dbd935bcdd06c3ddb1ffe9ced63`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad67b816dd3ebfab16dd19d0768f67e218ed3070e064a66bfa1b026ea84191e`  
		Last Modified: Sat, 19 Oct 2024 08:07:03 GMT  
		Size: 175.2 MB (175210957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f62c598e0e4b12d38b7e9ac6d1e37417fddac22e7efa57555e76096c3484517`  
		Last Modified: Sat, 19 Oct 2024 20:27:03 GMT  
		Size: 228.9 MB (228918647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4d72eab67be576c01e790395a1efc82aa1e3450e34f2c66965ed128ea73929c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7da09c2def11516f2cac29397dd79e45e13edd6a595770e1c583d3f89d9944c`

```dockerfile
```

-	Layers:
	-	`sha256:df68194a4679648dafbc2ce121470f555dc6c97bca93205f2b8b4d349281e903`  
		Last Modified: Sat, 19 Oct 2024 20:26:58 GMT  
		Size: 15.3 MB (15305316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a34b03d3951e72b491cfe93d2ef4efee2d02c129efc7f6c165735b24919d166`  
		Last Modified: Sat, 19 Oct 2024 20:26:57 GMT  
		Size: 13.3 KB (13259 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d82d65d48a0b6d0f5d39f7e8cdd1689fd2c6685007b66b4f021ee6e0704f642b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596180926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4bc4718cff8ac4db4e0cd8f6fb22ad73df411fc871ce08aa34e313e9e769cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d4884f85282b9a352dbcedf2cccd073a63e60b151be84375ce9279dec1c553`  
		Last Modified: Sat, 19 Oct 2024 06:16:07 GMT  
		Size: 202.6 MB (202644222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a5b77d8d49ee81a31cd491be54a349b09b6537083730e14be2f68804799c67`  
		Last Modified: Sat, 19 Oct 2024 20:04:17 GMT  
		Size: 256.0 MB (256007848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a992d3d7fa41a9bf8aa6c833c923c0e21a0dc25a6c95ab6b972a3bf938e60bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f84fa5c1c33f2991055fe2dfed397aa3de67ebdee0e01aa4c66271fc8e2b46`

```dockerfile
```

-	Layers:
	-	`sha256:194d3ee80b090fdab62b570cc0b990cda05ace7cb3697e836047312452491f3e`  
		Last Modified: Sat, 19 Oct 2024 20:04:11 GMT  
		Size: 15.5 MB (15529783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2396872dec21a26fe49789692367fe840fd8d80316a7738dd410585be99ae02`  
		Last Modified: Sat, 19 Oct 2024 20:04:10 GMT  
		Size: 13.3 KB (13303 bytes)  
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
$ docker pull rust@sha256:565a7cef7c714e30d829290ac51d2523b887f2d9f4d75d56e1cee253d91331c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615970277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ee5a636017f864b10932ed1ffffaa50aae11a9cafbeb51f484d37b4d8bfdb9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
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
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3666a280304f3727f745e818ab5e252dd98676495517a360e23f821dee0fa6`  
		Last Modified: Sat, 19 Oct 2024 04:07:03 GMT  
		Size: 69.8 MB (69825530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81280667d7d6fa822ac7a45807cf98017526f614373fad289bacbeb84f61f73`  
		Last Modified: Sat, 19 Oct 2024 05:17:30 GMT  
		Size: 214.3 MB (214300420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd89c17397182837a76641fe74c5ac4688f9cd2afce20f782ae95d0846367cb`  
		Last Modified: Sat, 19 Oct 2024 19:43:12 GMT  
		Size: 252.6 MB (252582753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:55c7db0912be66850720729eb8e68d6d46fcb2806fb1121e3d3ea93c77ff6bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f618aee8535497d6062b875e019ec722cddc0c4322c0a5d64f34c366adb0dafa`

```dockerfile
```

-	Layers:
	-	`sha256:494207d1c19a9f9c9a8a4d0dc0e1f0c0633a0363ad0ec57ef7d284e49afb0805`  
		Last Modified: Sat, 19 Oct 2024 19:42:48 GMT  
		Size: 15.5 MB (15475454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22834bd3dee1022aa23492cd8fbb261876cccacd3df3528af3474cb30116f067`  
		Last Modified: Sat, 19 Oct 2024 19:42:45 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:6713c368dfe236fe7be2509ddce84bf70cca0af2dc709d903ae1ce92be79cd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597392132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda7509db578b0d8f0347aa0bd40839f820e2765c0c04f5b130d0576bac6b6d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
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
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2eccbc8d9b18898de6fc12769f52101d4af82f32957d095f8ab217c6886c2e`  
		Last Modified: Sat, 19 Oct 2024 05:04:19 GMT  
		Size: 183.3 MB (183299744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3c72db5de57d361c959f82e0a383ee33cd8c91b7fecf0aa70ac994ea864dea`  
		Last Modified: Sat, 19 Oct 2024 16:02:42 GMT  
		Size: 278.6 MB (278608964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:71ed314b5bcc9dfacb1b917dad0530f8b0b9c8cf5b0ddbc9493bcc04cbd1bab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6641dd5f17c0fcc76f37070190c900b941c711d4bea89b3494702d5090279d`

```dockerfile
```

-	Layers:
	-	`sha256:eb80b4b6b53506fb47fce58bfe36989307286364157f2aee1c04ae0541182d5e`  
		Last Modified: Sat, 19 Oct 2024 16:02:36 GMT  
		Size: 15.3 MB (15313614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b27a840fe6712fe1894cbbf106e9afa7c2de5d825a7891252b2e6d2004405e`  
		Last Modified: Sat, 19 Oct 2024 16:02:34 GMT  
		Size: 13.2 KB (13151 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82-bullseye`

```console
$ docker pull rust@sha256:f60dc7ea30e61d39082e0cbf1f92d951e0d5fda2e4a509dd3ed2d5a42e0c4e20
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
$ docker pull rust@sha256:8af7361ea620d72c1f9a173332d936485d3e6ada68c1fc7cf010c8c5e12ec581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.2 MB (512163900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9997bd184a1622957654856fc5ebe3fc26090106fd7183f192aa70de6f36a9e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
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
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a9032c7c4d1cfb31e96212773919f51ec2f6be760fc0f5c35bafbcdb50249`  
		Last Modified: Sat, 19 Oct 2024 06:37:59 GMT  
		Size: 50.6 MB (50613654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0525b656ff73752501ad6cdcf4137840983e49d8b07af0619e3185c5e925fb`  
		Last Modified: Sat, 19 Oct 2024 08:10:07 GMT  
		Size: 167.5 MB (167512354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c43aa88ff2e8544cbb34cb7bc9c4263de3a33dd12595b204ddf8969b943c22`  
		Last Modified: Sat, 19 Oct 2024 20:24:39 GMT  
		Size: 228.9 MB (228918612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c92ce165138230bdc8d92f2774f21b6ff173b0a20a5817d01af1f5b7bb149a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14912080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2d3bb2dd404797f5454017dbdbca9674cf2163035f688ddc8b718e10fb12e`

```dockerfile
```

-	Layers:
	-	`sha256:141db802f68f589a42b222b577ef6b35b39a754ffec66c5715966c6312b9a949`  
		Last Modified: Sat, 19 Oct 2024 20:24:34 GMT  
		Size: 14.9 MB (14900743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e125043ad782c9f35d6018b39446890cd253c6e05a61acee96b6c9d0052428`  
		Last Modified: Sat, 19 Oct 2024 20:24:34 GMT  
		Size: 11.3 KB (11337 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f70e8bd2b2868a1f0cb7a711bb71f74ee77fbc2dd33c0d956251e955e323e21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.3 MB (570294243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3f4d291ce1ea3d241dd96079dafcf5d00bd4f99ec210b356e5bad749185461`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc6072bf5318ca0f9f250b4fcc6254d92483650689f0b0d77274be187abd96`  
		Last Modified: Sat, 19 Oct 2024 05:18:19 GMT  
		Size: 54.8 MB (54832658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13f3e7a61817231ad609702b6918e16648b3eec453567dbedd80952df7e3957`  
		Last Modified: Sat, 19 Oct 2024 06:17:47 GMT  
		Size: 190.0 MB (189971242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93765710d73d66b5b4443516a375c9c981b9ecd07f1ac581fefb956b0624a66`  
		Last Modified: Sat, 19 Oct 2024 20:02:46 GMT  
		Size: 256.0 MB (256007659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e45140ffd2b699e4c5cbdfb96804f7d756a9b862ee163f7d8c74947743b5c51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15113859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d173d7479537f73d26bb16b761a8a0265ca5a070e525ee96191099186ac199f`

```dockerfile
```

-	Layers:
	-	`sha256:38be245007626b5bcaf4d9ab6bc3f6f6e7a944590c035bed3647f40f3ea3fe34`  
		Last Modified: Sat, 19 Oct 2024 20:02:40 GMT  
		Size: 15.1 MB (15102494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcf7d213da88bc30da54c88258c32d3eb563da066517dfdede3d0f2ebfc82ca`  
		Last Modified: Sat, 19 Oct 2024 20:02:40 GMT  
		Size: 11.4 KB (11365 bytes)  
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
$ docker pull rust@sha256:60fe5b3207c39d9d52d2b1cc5075f4c71ca7a3ed23dbfa96a19747dafba99afc
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
$ docker pull rust@sha256:6af06831c441ea6efe5da0841875f10c9143e27e2068f7971dc3cb4493777c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301463797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5193a64b31f6521a36ef2a9b1ff2e63c0b09ec71e19c880765a69322380ad8a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65593264902c7ef0684f69975da9c31f1d677a35eb904b8858d752363894bbf`  
		Last Modified: Fri, 18 Oct 2024 04:55:44 GMT  
		Size: 276.7 MB (276745600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim` - unknown; unknown

```console
$ docker pull rust@sha256:07cd606a2467e9c8ca156915edf6217316d0b6102a08aaa068ce38398d0c8da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec8d2eea1e2fdd0cab72470cfea9e17ba71367f3f8771d876e8f0b01f29744f`

```dockerfile
```

-	Layers:
	-	`sha256:51505a3fb8a002b908713bda6232480bf93d778a2cd307af0732ff66d0af4ef5`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01fab3537dc20a8b760c33a1bcf432402dbbb9e1378901458dee5bc53c51dfb`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 13.2 KB (13194 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:24cfb92a68669bf577b74a7a6e12046851b9d153e0de06e8f902d0aec217ec39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350996361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b376079c1d1c0d19aac1a6d084bdffe036f9c6a0cafab7d6301be6434ac5790d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e35824bcc3a12d7039bc1e45a08bce002fd267d99d1978d3b01ce7613413cd`  
		Last Modified: Fri, 18 Oct 2024 00:28:42 GMT  
		Size: 321.8 MB (321840020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim` - unknown; unknown

```console
$ docker pull rust@sha256:5a8b2746c65775e6acb4139b0071e720fcddaf9949803347ff1cce9ace3ee2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781b40760ab6bde89d9fd1eaf24672d71f8b0a1557e490646521a2255e054848`

```dockerfile
```

-	Layers:
	-	`sha256:3999435d6d71bfb3d6d5d77e720ef535934122b4b4f23ea3c3b74509b2121080`  
		Last Modified: Fri, 18 Oct 2024 00:28:36 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fbee966e4be75c4c34c2a283707d8db1c220c6dea79aeb970bbd1412776002`  
		Last Modified: Fri, 18 Oct 2024 00:28:35 GMT  
		Size: 13.2 KB (13238 bytes)  
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
$ docker pull rust@sha256:3b3291ce9a66c2810bda45239d5a3204156862ad19a2242f33677249a8cfc792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f37690e23b0d7eeacf9b82ad65ea93c3515164fe329039cf6c3b68b52eadd38`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f43badb6d18c1b7c35c88dd66c3530d7112c29ed622050dccf5b67e8e87040a`  
		Last Modified: Fri, 18 Oct 2024 01:11:21 GMT  
		Size: 321.3 MB (321340278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim` - unknown; unknown

```console
$ docker pull rust@sha256:cdb656b3036da27b5de1f8da7a2c7649b503346c968c5e98576e50967daafe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c71fdc69f1717530372cc23714c3698b5e2188adf646bb78da5df4383806808`

```dockerfile
```

-	Layers:
	-	`sha256:27eade1d9d895465bc2b8901153021d7ed125b6b270e683c41f8f3fa762fd2ad`  
		Last Modified: Fri, 18 Oct 2024 01:11:13 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d343e81522d031d59cbf59c4478117043e268a002fcae2252af4afee8edfd6`  
		Last Modified: Fri, 18 Oct 2024 01:11:12 GMT  
		Size: 13.2 KB (13154 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim` - linux; s390x

```console
$ docker pull rust@sha256:2f15097849b373f3334d043a19a1e2aed41324dfe17969afe5982cb7870d126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356216165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa853f32b6e73890d038285e2b30fc11040dbc95793ddf7db9c55e6742d91af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203d547d95b548a5a647f46a5b304047a4084df212db4a5188e5db5983b530ca`  
		Last Modified: Thu, 17 Oct 2024 23:42:15 GMT  
		Size: 328.7 MB (328726081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim` - unknown; unknown

```console
$ docker pull rust@sha256:00ee1eca709e062e0adb277cb380fda87dcf1a4a441f517506dca62708eec1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7433567ec5ed96973704f1f3f0a3c1175fc80bab52299c7609f52801f6ddf80`

```dockerfile
```

-	Layers:
	-	`sha256:3a52844eec2dcfc9ce0941a96703ef6a9183abefb170c89f7aaddc53cafa57fc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca49a9d06e01cc7a03e2c5215a23b874c4216aec674651cc808436288f055cc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 13.1 KB (13091 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82-slim-bookworm`

```console
$ docker pull rust@sha256:60fe5b3207c39d9d52d2b1cc5075f4c71ca7a3ed23dbfa96a19747dafba99afc
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
$ docker pull rust@sha256:6af06831c441ea6efe5da0841875f10c9143e27e2068f7971dc3cb4493777c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301463797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5193a64b31f6521a36ef2a9b1ff2e63c0b09ec71e19c880765a69322380ad8a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65593264902c7ef0684f69975da9c31f1d677a35eb904b8858d752363894bbf`  
		Last Modified: Fri, 18 Oct 2024 04:55:44 GMT  
		Size: 276.7 MB (276745600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:07cd606a2467e9c8ca156915edf6217316d0b6102a08aaa068ce38398d0c8da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec8d2eea1e2fdd0cab72470cfea9e17ba71367f3f8771d876e8f0b01f29744f`

```dockerfile
```

-	Layers:
	-	`sha256:51505a3fb8a002b908713bda6232480bf93d778a2cd307af0732ff66d0af4ef5`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01fab3537dc20a8b760c33a1bcf432402dbbb9e1378901458dee5bc53c51dfb`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 13.2 KB (13194 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:24cfb92a68669bf577b74a7a6e12046851b9d153e0de06e8f902d0aec217ec39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350996361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b376079c1d1c0d19aac1a6d084bdffe036f9c6a0cafab7d6301be6434ac5790d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e35824bcc3a12d7039bc1e45a08bce002fd267d99d1978d3b01ce7613413cd`  
		Last Modified: Fri, 18 Oct 2024 00:28:42 GMT  
		Size: 321.8 MB (321840020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5a8b2746c65775e6acb4139b0071e720fcddaf9949803347ff1cce9ace3ee2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781b40760ab6bde89d9fd1eaf24672d71f8b0a1557e490646521a2255e054848`

```dockerfile
```

-	Layers:
	-	`sha256:3999435d6d71bfb3d6d5d77e720ef535934122b4b4f23ea3c3b74509b2121080`  
		Last Modified: Fri, 18 Oct 2024 00:28:36 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fbee966e4be75c4c34c2a283707d8db1c220c6dea79aeb970bbd1412776002`  
		Last Modified: Fri, 18 Oct 2024 00:28:35 GMT  
		Size: 13.2 KB (13238 bytes)  
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
$ docker pull rust@sha256:3b3291ce9a66c2810bda45239d5a3204156862ad19a2242f33677249a8cfc792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f37690e23b0d7eeacf9b82ad65ea93c3515164fe329039cf6c3b68b52eadd38`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f43badb6d18c1b7c35c88dd66c3530d7112c29ed622050dccf5b67e8e87040a`  
		Last Modified: Fri, 18 Oct 2024 01:11:21 GMT  
		Size: 321.3 MB (321340278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:cdb656b3036da27b5de1f8da7a2c7649b503346c968c5e98576e50967daafe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c71fdc69f1717530372cc23714c3698b5e2188adf646bb78da5df4383806808`

```dockerfile
```

-	Layers:
	-	`sha256:27eade1d9d895465bc2b8901153021d7ed125b6b270e683c41f8f3fa762fd2ad`  
		Last Modified: Fri, 18 Oct 2024 01:11:13 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d343e81522d031d59cbf59c4478117043e268a002fcae2252af4afee8edfd6`  
		Last Modified: Fri, 18 Oct 2024 01:11:12 GMT  
		Size: 13.2 KB (13154 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:2f15097849b373f3334d043a19a1e2aed41324dfe17969afe5982cb7870d126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356216165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa853f32b6e73890d038285e2b30fc11040dbc95793ddf7db9c55e6742d91af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203d547d95b548a5a647f46a5b304047a4084df212db4a5188e5db5983b530ca`  
		Last Modified: Thu, 17 Oct 2024 23:42:15 GMT  
		Size: 328.7 MB (328726081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:00ee1eca709e062e0adb277cb380fda87dcf1a4a441f517506dca62708eec1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7433567ec5ed96973704f1f3f0a3c1175fc80bab52299c7609f52801f6ddf80`

```dockerfile
```

-	Layers:
	-	`sha256:3a52844eec2dcfc9ce0941a96703ef6a9183abefb170c89f7aaddc53cafa57fc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca49a9d06e01cc7a03e2c5215a23b874c4216aec674651cc808436288f055cc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 13.1 KB (13091 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82-slim-bullseye`

```console
$ docker pull rust@sha256:6ecf4bda0e2b5e7f4610ac8612bc6e01adb3f4451dd8ff16b160be6e07d8c054
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
$ docker pull rust@sha256:cb4937b32194f99b394b565b351807eaa88ca11ad728ccd77ac3f29d3670f85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297762491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789d4d1356befa56ac46e1dd3002047d504df6604c5f112c786846745c11d493`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:45 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Thu, 17 Oct 2024 03:03:46 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f127f81679252c87ada20a6442aab050daaa6280455d330c2ed0e0312ad263`  
		Last Modified: Fri, 18 Oct 2024 04:51:41 GMT  
		Size: 271.2 MB (271172936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7a86756242f0ba3629f641732e0444d8519cb35f5436097966d6e2355c809fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811a4eb5f5f1ce78ce34703dd8554a6e58cbaa0edff11528ac95ebe6d7ca1dcc`

```dockerfile
```

-	Layers:
	-	`sha256:75b8d4d1890e668869883ff090be72445c0bb046190b26558bc015fabccc07b2`  
		Last Modified: Fri, 18 Oct 2024 04:51:36 GMT  
		Size: 4.0 MB (3973767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241f7e92e93b1ef933ca9018e07bab3fb08cc5e31e31246cb29b3057f6c83402`  
		Last Modified: Fri, 18 Oct 2024 04:51:35 GMT  
		Size: 11.2 KB (11246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d453636ade10ddd4286ec5ecdcb24f1a99cedccc09c5c13ad7289b53d33cd31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341766510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e871be81f15e4e120ba9ff8708fa70d21e83ce85e0870e19adae88e2bf2c6e86`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548d0c25fc9eeb4d349077a60a496f321d329205b3f5b06ef193b2adda85c179`  
		Last Modified: Fri, 18 Oct 2024 00:24:20 GMT  
		Size: 311.7 MB (311690753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5ea1413c96faa2e8729eafce7b57890ee56fa150674852e2b38ade7b654fb007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4172471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524fb398c788a87e7ea0b080c814f8340c81e2417be3e25f1b4537c834c21b72`

```dockerfile
```

-	Layers:
	-	`sha256:11b63d16de5274387c9f87faa0b807ce8c15e3150180bddf60776c4ff0e857a7`  
		Last Modified: Fri, 18 Oct 2024 00:24:13 GMT  
		Size: 4.2 MB (4161198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b701d88e21beef1d4a70fdc8b97a5303b2415f3728fdbbef255b1db4950a6e3f`  
		Last Modified: Fri, 18 Oct 2024 00:24:13 GMT  
		Size: 11.3 KB (11273 bytes)  
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
$ docker pull rust@sha256:3da385318a04f89f7a8e5d12b0c7091f1cafc5805e160451394926c12101cd7b
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
$ docker pull rust@sha256:4d776039a9a357be19ca9ead57b0656a213619c7298982097a0857d5a605ac5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530870052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea03bd0e673bbc1777121a59412ca6c31511dbd935bcdd06c3ddb1ffe9ced63`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad67b816dd3ebfab16dd19d0768f67e218ed3070e064a66bfa1b026ea84191e`  
		Last Modified: Sat, 19 Oct 2024 08:07:03 GMT  
		Size: 175.2 MB (175210957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f62c598e0e4b12d38b7e9ac6d1e37417fddac22e7efa57555e76096c3484517`  
		Last Modified: Sat, 19 Oct 2024 20:27:03 GMT  
		Size: 228.9 MB (228918647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0` - unknown; unknown

```console
$ docker pull rust@sha256:4d72eab67be576c01e790395a1efc82aa1e3450e34f2c66965ed128ea73929c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7da09c2def11516f2cac29397dd79e45e13edd6a595770e1c583d3f89d9944c`

```dockerfile
```

-	Layers:
	-	`sha256:df68194a4679648dafbc2ce121470f555dc6c97bca93205f2b8b4d349281e903`  
		Last Modified: Sat, 19 Oct 2024 20:26:58 GMT  
		Size: 15.3 MB (15305316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a34b03d3951e72b491cfe93d2ef4efee2d02c129efc7f6c165735b24919d166`  
		Last Modified: Sat, 19 Oct 2024 20:26:57 GMT  
		Size: 13.3 KB (13259 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d82d65d48a0b6d0f5d39f7e8cdd1689fd2c6685007b66b4f021ee6e0704f642b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596180926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4bc4718cff8ac4db4e0cd8f6fb22ad73df411fc871ce08aa34e313e9e769cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d4884f85282b9a352dbcedf2cccd073a63e60b151be84375ce9279dec1c553`  
		Last Modified: Sat, 19 Oct 2024 06:16:07 GMT  
		Size: 202.6 MB (202644222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a5b77d8d49ee81a31cd491be54a349b09b6537083730e14be2f68804799c67`  
		Last Modified: Sat, 19 Oct 2024 20:04:17 GMT  
		Size: 256.0 MB (256007848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0` - unknown; unknown

```console
$ docker pull rust@sha256:a992d3d7fa41a9bf8aa6c833c923c0e21a0dc25a6c95ab6b972a3bf938e60bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f84fa5c1c33f2991055fe2dfed397aa3de67ebdee0e01aa4c66271fc8e2b46`

```dockerfile
```

-	Layers:
	-	`sha256:194d3ee80b090fdab62b570cc0b990cda05ace7cb3697e836047312452491f3e`  
		Last Modified: Sat, 19 Oct 2024 20:04:11 GMT  
		Size: 15.5 MB (15529783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2396872dec21a26fe49789692367fe840fd8d80316a7738dd410585be99ae02`  
		Last Modified: Sat, 19 Oct 2024 20:04:10 GMT  
		Size: 13.3 KB (13303 bytes)  
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
$ docker pull rust@sha256:565a7cef7c714e30d829290ac51d2523b887f2d9f4d75d56e1cee253d91331c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615970277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ee5a636017f864b10932ed1ffffaa50aae11a9cafbeb51f484d37b4d8bfdb9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
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
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3666a280304f3727f745e818ab5e252dd98676495517a360e23f821dee0fa6`  
		Last Modified: Sat, 19 Oct 2024 04:07:03 GMT  
		Size: 69.8 MB (69825530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81280667d7d6fa822ac7a45807cf98017526f614373fad289bacbeb84f61f73`  
		Last Modified: Sat, 19 Oct 2024 05:17:30 GMT  
		Size: 214.3 MB (214300420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd89c17397182837a76641fe74c5ac4688f9cd2afce20f782ae95d0846367cb`  
		Last Modified: Sat, 19 Oct 2024 19:43:12 GMT  
		Size: 252.6 MB (252582753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0` - unknown; unknown

```console
$ docker pull rust@sha256:55c7db0912be66850720729eb8e68d6d46fcb2806fb1121e3d3ea93c77ff6bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f618aee8535497d6062b875e019ec722cddc0c4322c0a5d64f34c366adb0dafa`

```dockerfile
```

-	Layers:
	-	`sha256:494207d1c19a9f9c9a8a4d0dc0e1f0c0633a0363ad0ec57ef7d284e49afb0805`  
		Last Modified: Sat, 19 Oct 2024 19:42:48 GMT  
		Size: 15.5 MB (15475454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22834bd3dee1022aa23492cd8fbb261876cccacd3df3528af3474cb30116f067`  
		Last Modified: Sat, 19 Oct 2024 19:42:45 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0` - linux; s390x

```console
$ docker pull rust@sha256:6713c368dfe236fe7be2509ddce84bf70cca0af2dc709d903ae1ce92be79cd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597392132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda7509db578b0d8f0347aa0bd40839f820e2765c0c04f5b130d0576bac6b6d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
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
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2eccbc8d9b18898de6fc12769f52101d4af82f32957d095f8ab217c6886c2e`  
		Last Modified: Sat, 19 Oct 2024 05:04:19 GMT  
		Size: 183.3 MB (183299744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3c72db5de57d361c959f82e0a383ee33cd8c91b7fecf0aa70ac994ea864dea`  
		Last Modified: Sat, 19 Oct 2024 16:02:42 GMT  
		Size: 278.6 MB (278608964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0` - unknown; unknown

```console
$ docker pull rust@sha256:71ed314b5bcc9dfacb1b917dad0530f8b0b9c8cf5b0ddbc9493bcc04cbd1bab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6641dd5f17c0fcc76f37070190c900b941c711d4bea89b3494702d5090279d`

```dockerfile
```

-	Layers:
	-	`sha256:eb80b4b6b53506fb47fce58bfe36989307286364157f2aee1c04ae0541182d5e`  
		Last Modified: Sat, 19 Oct 2024 16:02:36 GMT  
		Size: 15.3 MB (15313614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b27a840fe6712fe1894cbbf106e9afa7c2de5d825a7891252b2e6d2004405e`  
		Last Modified: Sat, 19 Oct 2024 16:02:34 GMT  
		Size: 13.2 KB (13151 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0-alpine`

```console
$ docker pull rust@sha256:00c2107fa0e7a3eecf1fb31c814cd11a450026fae3fe375a1eed141be5fe75bc
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
$ docker pull rust@sha256:cc55868374fa1817218125ef6c0ef12201e2787cb400e941fbab95cb03e4dce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8955b5af103ec2e50ddf887aa77173599a206f1bd158b9f60531e84aeaf27c5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e451e7d55fdf7e0ddcc65ceb40f1e7f11a0c8e3188735a9d77443640951d42`  
		Last Modified: Fri, 18 Oct 2024 00:31:10 GMT  
		Size: 52.9 MB (52946227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67db9729fe0f06f4a5f2a64007565ed87dad3e2955a71d1f5b31eb1992c1ee77`  
		Last Modified: Fri, 18 Oct 2024 00:31:13 GMT  
		Size: 241.8 MB (241799131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:7fa5fb93c33118b5ace2225168e3a66220b4a4f7c0ea94b599f22a39649623fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 KB (758862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc1bc460aee8e1e08dfb95db95786730c4a0b58aec5352403da9bd51c50c52d`

```dockerfile
```

-	Layers:
	-	`sha256:8b91b6f48c74e79f8c38eef16aa7af99c79834dcac8ab6ee8c27425433e72b2c`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 747.0 KB (746984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5587688eb47137d37d13b14e84da8cc45bdc8079dd0cd8f15d98eb2ee4cc79fb`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 11.9 KB (11878 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0-alpine3.19`

```console
$ docker pull rust@sha256:fcd6117426b140d94e833c54c6e05612c1fa15d9f065b7ca21f7a266a8327870
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
$ docker pull rust@sha256:499c93a743c096822c3ce050e96df3f22ceb5abf517422c3cfc3e34be779b334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298153503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb195d39c948c729c2a621ced30c3cb838d44b72fc12084fe9c364ba5daaf1c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832c2f560bcd7cc2071a2ff7b80d28d566d9bc6644db81915a561a051e27d00e`  
		Last Modified: Fri, 18 Oct 2024 00:29:56 GMT  
		Size: 53.0 MB (52995407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e9dcbde1ac8d276d321ba07f80f05e9ffee4fae318dae571a76d7cf5264f3c`  
		Last Modified: Fri, 18 Oct 2024 00:30:00 GMT  
		Size: 241.8 MB (241798993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:985e97b0beed650244a2e606b90ea14955f2e370312715ead82e5c874bb39aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.0 KB (760049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e44d5402fbaee4e101aecb1bf614fdbb58f6c24413a149931fd7cfc97b7621`

```dockerfile
```

-	Layers:
	-	`sha256:7f55f4dc6a64459bf97682966e85d4d3faaa31836315dd9bd160eea17bc2a50f`  
		Last Modified: Fri, 18 Oct 2024 00:29:55 GMT  
		Size: 749.4 KB (749423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8624b8420bd192f3fcc11e096d27439030ddff55ca81b0b89530581ea062c2a9`  
		Last Modified: Fri, 18 Oct 2024 00:29:55 GMT  
		Size: 10.6 KB (10626 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0-alpine3.20`

```console
$ docker pull rust@sha256:00c2107fa0e7a3eecf1fb31c814cd11a450026fae3fe375a1eed141be5fe75bc
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
$ docker pull rust@sha256:cc55868374fa1817218125ef6c0ef12201e2787cb400e941fbab95cb03e4dce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8955b5af103ec2e50ddf887aa77173599a206f1bd158b9f60531e84aeaf27c5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e451e7d55fdf7e0ddcc65ceb40f1e7f11a0c8e3188735a9d77443640951d42`  
		Last Modified: Fri, 18 Oct 2024 00:31:10 GMT  
		Size: 52.9 MB (52946227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67db9729fe0f06f4a5f2a64007565ed87dad3e2955a71d1f5b31eb1992c1ee77`  
		Last Modified: Fri, 18 Oct 2024 00:31:13 GMT  
		Size: 241.8 MB (241799131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:7fa5fb93c33118b5ace2225168e3a66220b4a4f7c0ea94b599f22a39649623fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 KB (758862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc1bc460aee8e1e08dfb95db95786730c4a0b58aec5352403da9bd51c50c52d`

```dockerfile
```

-	Layers:
	-	`sha256:8b91b6f48c74e79f8c38eef16aa7af99c79834dcac8ab6ee8c27425433e72b2c`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 747.0 KB (746984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5587688eb47137d37d13b14e84da8cc45bdc8079dd0cd8f15d98eb2ee4cc79fb`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 11.9 KB (11878 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0-bookworm`

```console
$ docker pull rust@sha256:3da385318a04f89f7a8e5d12b0c7091f1cafc5805e160451394926c12101cd7b
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
$ docker pull rust@sha256:4d776039a9a357be19ca9ead57b0656a213619c7298982097a0857d5a605ac5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530870052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea03bd0e673bbc1777121a59412ca6c31511dbd935bcdd06c3ddb1ffe9ced63`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad67b816dd3ebfab16dd19d0768f67e218ed3070e064a66bfa1b026ea84191e`  
		Last Modified: Sat, 19 Oct 2024 08:07:03 GMT  
		Size: 175.2 MB (175210957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f62c598e0e4b12d38b7e9ac6d1e37417fddac22e7efa57555e76096c3484517`  
		Last Modified: Sat, 19 Oct 2024 20:27:03 GMT  
		Size: 228.9 MB (228918647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4d72eab67be576c01e790395a1efc82aa1e3450e34f2c66965ed128ea73929c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7da09c2def11516f2cac29397dd79e45e13edd6a595770e1c583d3f89d9944c`

```dockerfile
```

-	Layers:
	-	`sha256:df68194a4679648dafbc2ce121470f555dc6c97bca93205f2b8b4d349281e903`  
		Last Modified: Sat, 19 Oct 2024 20:26:58 GMT  
		Size: 15.3 MB (15305316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a34b03d3951e72b491cfe93d2ef4efee2d02c129efc7f6c165735b24919d166`  
		Last Modified: Sat, 19 Oct 2024 20:26:57 GMT  
		Size: 13.3 KB (13259 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d82d65d48a0b6d0f5d39f7e8cdd1689fd2c6685007b66b4f021ee6e0704f642b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596180926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4bc4718cff8ac4db4e0cd8f6fb22ad73df411fc871ce08aa34e313e9e769cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d4884f85282b9a352dbcedf2cccd073a63e60b151be84375ce9279dec1c553`  
		Last Modified: Sat, 19 Oct 2024 06:16:07 GMT  
		Size: 202.6 MB (202644222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a5b77d8d49ee81a31cd491be54a349b09b6537083730e14be2f68804799c67`  
		Last Modified: Sat, 19 Oct 2024 20:04:17 GMT  
		Size: 256.0 MB (256007848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a992d3d7fa41a9bf8aa6c833c923c0e21a0dc25a6c95ab6b972a3bf938e60bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f84fa5c1c33f2991055fe2dfed397aa3de67ebdee0e01aa4c66271fc8e2b46`

```dockerfile
```

-	Layers:
	-	`sha256:194d3ee80b090fdab62b570cc0b990cda05ace7cb3697e836047312452491f3e`  
		Last Modified: Sat, 19 Oct 2024 20:04:11 GMT  
		Size: 15.5 MB (15529783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2396872dec21a26fe49789692367fe840fd8d80316a7738dd410585be99ae02`  
		Last Modified: Sat, 19 Oct 2024 20:04:10 GMT  
		Size: 13.3 KB (13303 bytes)  
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
$ docker pull rust@sha256:565a7cef7c714e30d829290ac51d2523b887f2d9f4d75d56e1cee253d91331c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615970277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ee5a636017f864b10932ed1ffffaa50aae11a9cafbeb51f484d37b4d8bfdb9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
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
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3666a280304f3727f745e818ab5e252dd98676495517a360e23f821dee0fa6`  
		Last Modified: Sat, 19 Oct 2024 04:07:03 GMT  
		Size: 69.8 MB (69825530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81280667d7d6fa822ac7a45807cf98017526f614373fad289bacbeb84f61f73`  
		Last Modified: Sat, 19 Oct 2024 05:17:30 GMT  
		Size: 214.3 MB (214300420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd89c17397182837a76641fe74c5ac4688f9cd2afce20f782ae95d0846367cb`  
		Last Modified: Sat, 19 Oct 2024 19:43:12 GMT  
		Size: 252.6 MB (252582753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:55c7db0912be66850720729eb8e68d6d46fcb2806fb1121e3d3ea93c77ff6bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f618aee8535497d6062b875e019ec722cddc0c4322c0a5d64f34c366adb0dafa`

```dockerfile
```

-	Layers:
	-	`sha256:494207d1c19a9f9c9a8a4d0dc0e1f0c0633a0363ad0ec57ef7d284e49afb0805`  
		Last Modified: Sat, 19 Oct 2024 19:42:48 GMT  
		Size: 15.5 MB (15475454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22834bd3dee1022aa23492cd8fbb261876cccacd3df3528af3474cb30116f067`  
		Last Modified: Sat, 19 Oct 2024 19:42:45 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:6713c368dfe236fe7be2509ddce84bf70cca0af2dc709d903ae1ce92be79cd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597392132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda7509db578b0d8f0347aa0bd40839f820e2765c0c04f5b130d0576bac6b6d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
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
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2eccbc8d9b18898de6fc12769f52101d4af82f32957d095f8ab217c6886c2e`  
		Last Modified: Sat, 19 Oct 2024 05:04:19 GMT  
		Size: 183.3 MB (183299744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3c72db5de57d361c959f82e0a383ee33cd8c91b7fecf0aa70ac994ea864dea`  
		Last Modified: Sat, 19 Oct 2024 16:02:42 GMT  
		Size: 278.6 MB (278608964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:71ed314b5bcc9dfacb1b917dad0530f8b0b9c8cf5b0ddbc9493bcc04cbd1bab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6641dd5f17c0fcc76f37070190c900b941c711d4bea89b3494702d5090279d`

```dockerfile
```

-	Layers:
	-	`sha256:eb80b4b6b53506fb47fce58bfe36989307286364157f2aee1c04ae0541182d5e`  
		Last Modified: Sat, 19 Oct 2024 16:02:36 GMT  
		Size: 15.3 MB (15313614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b27a840fe6712fe1894cbbf106e9afa7c2de5d825a7891252b2e6d2004405e`  
		Last Modified: Sat, 19 Oct 2024 16:02:34 GMT  
		Size: 13.2 KB (13151 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0-bullseye`

```console
$ docker pull rust@sha256:f60dc7ea30e61d39082e0cbf1f92d951e0d5fda2e4a509dd3ed2d5a42e0c4e20
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
$ docker pull rust@sha256:8af7361ea620d72c1f9a173332d936485d3e6ada68c1fc7cf010c8c5e12ec581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.2 MB (512163900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9997bd184a1622957654856fc5ebe3fc26090106fd7183f192aa70de6f36a9e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
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
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a9032c7c4d1cfb31e96212773919f51ec2f6be760fc0f5c35bafbcdb50249`  
		Last Modified: Sat, 19 Oct 2024 06:37:59 GMT  
		Size: 50.6 MB (50613654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0525b656ff73752501ad6cdcf4137840983e49d8b07af0619e3185c5e925fb`  
		Last Modified: Sat, 19 Oct 2024 08:10:07 GMT  
		Size: 167.5 MB (167512354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c43aa88ff2e8544cbb34cb7bc9c4263de3a33dd12595b204ddf8969b943c22`  
		Last Modified: Sat, 19 Oct 2024 20:24:39 GMT  
		Size: 228.9 MB (228918612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c92ce165138230bdc8d92f2774f21b6ff173b0a20a5817d01af1f5b7bb149a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14912080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2d3bb2dd404797f5454017dbdbca9674cf2163035f688ddc8b718e10fb12e`

```dockerfile
```

-	Layers:
	-	`sha256:141db802f68f589a42b222b577ef6b35b39a754ffec66c5715966c6312b9a949`  
		Last Modified: Sat, 19 Oct 2024 20:24:34 GMT  
		Size: 14.9 MB (14900743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e125043ad782c9f35d6018b39446890cd253c6e05a61acee96b6c9d0052428`  
		Last Modified: Sat, 19 Oct 2024 20:24:34 GMT  
		Size: 11.3 KB (11337 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f70e8bd2b2868a1f0cb7a711bb71f74ee77fbc2dd33c0d956251e955e323e21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.3 MB (570294243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3f4d291ce1ea3d241dd96079dafcf5d00bd4f99ec210b356e5bad749185461`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc6072bf5318ca0f9f250b4fcc6254d92483650689f0b0d77274be187abd96`  
		Last Modified: Sat, 19 Oct 2024 05:18:19 GMT  
		Size: 54.8 MB (54832658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13f3e7a61817231ad609702b6918e16648b3eec453567dbedd80952df7e3957`  
		Last Modified: Sat, 19 Oct 2024 06:17:47 GMT  
		Size: 190.0 MB (189971242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93765710d73d66b5b4443516a375c9c981b9ecd07f1ac581fefb956b0624a66`  
		Last Modified: Sat, 19 Oct 2024 20:02:46 GMT  
		Size: 256.0 MB (256007659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e45140ffd2b699e4c5cbdfb96804f7d756a9b862ee163f7d8c74947743b5c51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15113859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d173d7479537f73d26bb16b761a8a0265ca5a070e525ee96191099186ac199f`

```dockerfile
```

-	Layers:
	-	`sha256:38be245007626b5bcaf4d9ab6bc3f6f6e7a944590c035bed3647f40f3ea3fe34`  
		Last Modified: Sat, 19 Oct 2024 20:02:40 GMT  
		Size: 15.1 MB (15102494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcf7d213da88bc30da54c88258c32d3eb563da066517dfdede3d0f2ebfc82ca`  
		Last Modified: Sat, 19 Oct 2024 20:02:40 GMT  
		Size: 11.4 KB (11365 bytes)  
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
$ docker pull rust@sha256:60fe5b3207c39d9d52d2b1cc5075f4c71ca7a3ed23dbfa96a19747dafba99afc
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
$ docker pull rust@sha256:6af06831c441ea6efe5da0841875f10c9143e27e2068f7971dc3cb4493777c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301463797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5193a64b31f6521a36ef2a9b1ff2e63c0b09ec71e19c880765a69322380ad8a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65593264902c7ef0684f69975da9c31f1d677a35eb904b8858d752363894bbf`  
		Last Modified: Fri, 18 Oct 2024 04:55:44 GMT  
		Size: 276.7 MB (276745600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:07cd606a2467e9c8ca156915edf6217316d0b6102a08aaa068ce38398d0c8da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec8d2eea1e2fdd0cab72470cfea9e17ba71367f3f8771d876e8f0b01f29744f`

```dockerfile
```

-	Layers:
	-	`sha256:51505a3fb8a002b908713bda6232480bf93d778a2cd307af0732ff66d0af4ef5`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01fab3537dc20a8b760c33a1bcf432402dbbb9e1378901458dee5bc53c51dfb`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 13.2 KB (13194 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:24cfb92a68669bf577b74a7a6e12046851b9d153e0de06e8f902d0aec217ec39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350996361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b376079c1d1c0d19aac1a6d084bdffe036f9c6a0cafab7d6301be6434ac5790d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e35824bcc3a12d7039bc1e45a08bce002fd267d99d1978d3b01ce7613413cd`  
		Last Modified: Fri, 18 Oct 2024 00:28:42 GMT  
		Size: 321.8 MB (321840020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:5a8b2746c65775e6acb4139b0071e720fcddaf9949803347ff1cce9ace3ee2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781b40760ab6bde89d9fd1eaf24672d71f8b0a1557e490646521a2255e054848`

```dockerfile
```

-	Layers:
	-	`sha256:3999435d6d71bfb3d6d5d77e720ef535934122b4b4f23ea3c3b74509b2121080`  
		Last Modified: Fri, 18 Oct 2024 00:28:36 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fbee966e4be75c4c34c2a283707d8db1c220c6dea79aeb970bbd1412776002`  
		Last Modified: Fri, 18 Oct 2024 00:28:35 GMT  
		Size: 13.2 KB (13238 bytes)  
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
$ docker pull rust@sha256:3b3291ce9a66c2810bda45239d5a3204156862ad19a2242f33677249a8cfc792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f37690e23b0d7eeacf9b82ad65ea93c3515164fe329039cf6c3b68b52eadd38`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f43badb6d18c1b7c35c88dd66c3530d7112c29ed622050dccf5b67e8e87040a`  
		Last Modified: Fri, 18 Oct 2024 01:11:21 GMT  
		Size: 321.3 MB (321340278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:cdb656b3036da27b5de1f8da7a2c7649b503346c968c5e98576e50967daafe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c71fdc69f1717530372cc23714c3698b5e2188adf646bb78da5df4383806808`

```dockerfile
```

-	Layers:
	-	`sha256:27eade1d9d895465bc2b8901153021d7ed125b6b270e683c41f8f3fa762fd2ad`  
		Last Modified: Fri, 18 Oct 2024 01:11:13 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d343e81522d031d59cbf59c4478117043e268a002fcae2252af4afee8edfd6`  
		Last Modified: Fri, 18 Oct 2024 01:11:12 GMT  
		Size: 13.2 KB (13154 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim` - linux; s390x

```console
$ docker pull rust@sha256:2f15097849b373f3334d043a19a1e2aed41324dfe17969afe5982cb7870d126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356216165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa853f32b6e73890d038285e2b30fc11040dbc95793ddf7db9c55e6742d91af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203d547d95b548a5a647f46a5b304047a4084df212db4a5188e5db5983b530ca`  
		Last Modified: Thu, 17 Oct 2024 23:42:15 GMT  
		Size: 328.7 MB (328726081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:00ee1eca709e062e0adb277cb380fda87dcf1a4a441f517506dca62708eec1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7433567ec5ed96973704f1f3f0a3c1175fc80bab52299c7609f52801f6ddf80`

```dockerfile
```

-	Layers:
	-	`sha256:3a52844eec2dcfc9ce0941a96703ef6a9183abefb170c89f7aaddc53cafa57fc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca49a9d06e01cc7a03e2c5215a23b874c4216aec674651cc808436288f055cc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 13.1 KB (13091 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0-slim-bookworm`

```console
$ docker pull rust@sha256:60fe5b3207c39d9d52d2b1cc5075f4c71ca7a3ed23dbfa96a19747dafba99afc
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
$ docker pull rust@sha256:6af06831c441ea6efe5da0841875f10c9143e27e2068f7971dc3cb4493777c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301463797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5193a64b31f6521a36ef2a9b1ff2e63c0b09ec71e19c880765a69322380ad8a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65593264902c7ef0684f69975da9c31f1d677a35eb904b8858d752363894bbf`  
		Last Modified: Fri, 18 Oct 2024 04:55:44 GMT  
		Size: 276.7 MB (276745600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:07cd606a2467e9c8ca156915edf6217316d0b6102a08aaa068ce38398d0c8da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec8d2eea1e2fdd0cab72470cfea9e17ba71367f3f8771d876e8f0b01f29744f`

```dockerfile
```

-	Layers:
	-	`sha256:51505a3fb8a002b908713bda6232480bf93d778a2cd307af0732ff66d0af4ef5`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01fab3537dc20a8b760c33a1bcf432402dbbb9e1378901458dee5bc53c51dfb`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 13.2 KB (13194 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:24cfb92a68669bf577b74a7a6e12046851b9d153e0de06e8f902d0aec217ec39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350996361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b376079c1d1c0d19aac1a6d084bdffe036f9c6a0cafab7d6301be6434ac5790d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e35824bcc3a12d7039bc1e45a08bce002fd267d99d1978d3b01ce7613413cd`  
		Last Modified: Fri, 18 Oct 2024 00:28:42 GMT  
		Size: 321.8 MB (321840020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5a8b2746c65775e6acb4139b0071e720fcddaf9949803347ff1cce9ace3ee2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781b40760ab6bde89d9fd1eaf24672d71f8b0a1557e490646521a2255e054848`

```dockerfile
```

-	Layers:
	-	`sha256:3999435d6d71bfb3d6d5d77e720ef535934122b4b4f23ea3c3b74509b2121080`  
		Last Modified: Fri, 18 Oct 2024 00:28:36 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fbee966e4be75c4c34c2a283707d8db1c220c6dea79aeb970bbd1412776002`  
		Last Modified: Fri, 18 Oct 2024 00:28:35 GMT  
		Size: 13.2 KB (13238 bytes)  
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
$ docker pull rust@sha256:3b3291ce9a66c2810bda45239d5a3204156862ad19a2242f33677249a8cfc792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f37690e23b0d7eeacf9b82ad65ea93c3515164fe329039cf6c3b68b52eadd38`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f43badb6d18c1b7c35c88dd66c3530d7112c29ed622050dccf5b67e8e87040a`  
		Last Modified: Fri, 18 Oct 2024 01:11:21 GMT  
		Size: 321.3 MB (321340278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:cdb656b3036da27b5de1f8da7a2c7649b503346c968c5e98576e50967daafe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c71fdc69f1717530372cc23714c3698b5e2188adf646bb78da5df4383806808`

```dockerfile
```

-	Layers:
	-	`sha256:27eade1d9d895465bc2b8901153021d7ed125b6b270e683c41f8f3fa762fd2ad`  
		Last Modified: Fri, 18 Oct 2024 01:11:13 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d343e81522d031d59cbf59c4478117043e268a002fcae2252af4afee8edfd6`  
		Last Modified: Fri, 18 Oct 2024 01:11:12 GMT  
		Size: 13.2 KB (13154 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:2f15097849b373f3334d043a19a1e2aed41324dfe17969afe5982cb7870d126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356216165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa853f32b6e73890d038285e2b30fc11040dbc95793ddf7db9c55e6742d91af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203d547d95b548a5a647f46a5b304047a4084df212db4a5188e5db5983b530ca`  
		Last Modified: Thu, 17 Oct 2024 23:42:15 GMT  
		Size: 328.7 MB (328726081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:00ee1eca709e062e0adb277cb380fda87dcf1a4a441f517506dca62708eec1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7433567ec5ed96973704f1f3f0a3c1175fc80bab52299c7609f52801f6ddf80`

```dockerfile
```

-	Layers:
	-	`sha256:3a52844eec2dcfc9ce0941a96703ef6a9183abefb170c89f7aaddc53cafa57fc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca49a9d06e01cc7a03e2c5215a23b874c4216aec674651cc808436288f055cc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 13.1 KB (13091 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.82.0-slim-bullseye`

```console
$ docker pull rust@sha256:6ecf4bda0e2b5e7f4610ac8612bc6e01adb3f4451dd8ff16b160be6e07d8c054
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
$ docker pull rust@sha256:cb4937b32194f99b394b565b351807eaa88ca11ad728ccd77ac3f29d3670f85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297762491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789d4d1356befa56ac46e1dd3002047d504df6604c5f112c786846745c11d493`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:45 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Thu, 17 Oct 2024 03:03:46 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f127f81679252c87ada20a6442aab050daaa6280455d330c2ed0e0312ad263`  
		Last Modified: Fri, 18 Oct 2024 04:51:41 GMT  
		Size: 271.2 MB (271172936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7a86756242f0ba3629f641732e0444d8519cb35f5436097966d6e2355c809fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811a4eb5f5f1ce78ce34703dd8554a6e58cbaa0edff11528ac95ebe6d7ca1dcc`

```dockerfile
```

-	Layers:
	-	`sha256:75b8d4d1890e668869883ff090be72445c0bb046190b26558bc015fabccc07b2`  
		Last Modified: Fri, 18 Oct 2024 04:51:36 GMT  
		Size: 4.0 MB (3973767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241f7e92e93b1ef933ca9018e07bab3fb08cc5e31e31246cb29b3057f6c83402`  
		Last Modified: Fri, 18 Oct 2024 04:51:35 GMT  
		Size: 11.2 KB (11246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.82.0-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d453636ade10ddd4286ec5ecdcb24f1a99cedccc09c5c13ad7289b53d33cd31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341766510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e871be81f15e4e120ba9ff8708fa70d21e83ce85e0870e19adae88e2bf2c6e86`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548d0c25fc9eeb4d349077a60a496f321d329205b3f5b06ef193b2adda85c179`  
		Last Modified: Fri, 18 Oct 2024 00:24:20 GMT  
		Size: 311.7 MB (311690753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.82.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5ea1413c96faa2e8729eafce7b57890ee56fa150674852e2b38ade7b654fb007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4172471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524fb398c788a87e7ea0b080c814f8340c81e2417be3e25f1b4537c834c21b72`

```dockerfile
```

-	Layers:
	-	`sha256:11b63d16de5274387c9f87faa0b807ce8c15e3150180bddf60776c4ff0e857a7`  
		Last Modified: Fri, 18 Oct 2024 00:24:13 GMT  
		Size: 4.2 MB (4161198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b701d88e21beef1d4a70fdc8b97a5303b2415f3728fdbbef255b1db4950a6e3f`  
		Last Modified: Fri, 18 Oct 2024 00:24:13 GMT  
		Size: 11.3 KB (11273 bytes)  
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
$ docker pull rust@sha256:00c2107fa0e7a3eecf1fb31c814cd11a450026fae3fe375a1eed141be5fe75bc
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
$ docker pull rust@sha256:cc55868374fa1817218125ef6c0ef12201e2787cb400e941fbab95cb03e4dce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8955b5af103ec2e50ddf887aa77173599a206f1bd158b9f60531e84aeaf27c5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e451e7d55fdf7e0ddcc65ceb40f1e7f11a0c8e3188735a9d77443640951d42`  
		Last Modified: Fri, 18 Oct 2024 00:31:10 GMT  
		Size: 52.9 MB (52946227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67db9729fe0f06f4a5f2a64007565ed87dad3e2955a71d1f5b31eb1992c1ee77`  
		Last Modified: Fri, 18 Oct 2024 00:31:13 GMT  
		Size: 241.8 MB (241799131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:7fa5fb93c33118b5ace2225168e3a66220b4a4f7c0ea94b599f22a39649623fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 KB (758862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc1bc460aee8e1e08dfb95db95786730c4a0b58aec5352403da9bd51c50c52d`

```dockerfile
```

-	Layers:
	-	`sha256:8b91b6f48c74e79f8c38eef16aa7af99c79834dcac8ab6ee8c27425433e72b2c`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 747.0 KB (746984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5587688eb47137d37d13b14e84da8cc45bdc8079dd0cd8f15d98eb2ee4cc79fb`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 11.9 KB (11878 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.19`

```console
$ docker pull rust@sha256:fcd6117426b140d94e833c54c6e05612c1fa15d9f065b7ca21f7a266a8327870
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
$ docker pull rust@sha256:499c93a743c096822c3ce050e96df3f22ceb5abf517422c3cfc3e34be779b334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298153503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb195d39c948c729c2a621ced30c3cb838d44b72fc12084fe9c364ba5daaf1c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832c2f560bcd7cc2071a2ff7b80d28d566d9bc6644db81915a561a051e27d00e`  
		Last Modified: Fri, 18 Oct 2024 00:29:56 GMT  
		Size: 53.0 MB (52995407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e9dcbde1ac8d276d321ba07f80f05e9ffee4fae318dae571a76d7cf5264f3c`  
		Last Modified: Fri, 18 Oct 2024 00:30:00 GMT  
		Size: 241.8 MB (241798993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:985e97b0beed650244a2e606b90ea14955f2e370312715ead82e5c874bb39aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.0 KB (760049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e44d5402fbaee4e101aecb1bf614fdbb58f6c24413a149931fd7cfc97b7621`

```dockerfile
```

-	Layers:
	-	`sha256:7f55f4dc6a64459bf97682966e85d4d3faaa31836315dd9bd160eea17bc2a50f`  
		Last Modified: Fri, 18 Oct 2024 00:29:55 GMT  
		Size: 749.4 KB (749423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8624b8420bd192f3fcc11e096d27439030ddff55ca81b0b89530581ea062c2a9`  
		Last Modified: Fri, 18 Oct 2024 00:29:55 GMT  
		Size: 10.6 KB (10626 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.20`

```console
$ docker pull rust@sha256:00c2107fa0e7a3eecf1fb31c814cd11a450026fae3fe375a1eed141be5fe75bc
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
$ docker pull rust@sha256:cc55868374fa1817218125ef6c0ef12201e2787cb400e941fbab95cb03e4dce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298833004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8955b5af103ec2e50ddf887aa77173599a206f1bd158b9f60531e84aeaf27c5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e451e7d55fdf7e0ddcc65ceb40f1e7f11a0c8e3188735a9d77443640951d42`  
		Last Modified: Fri, 18 Oct 2024 00:31:10 GMT  
		Size: 52.9 MB (52946227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67db9729fe0f06f4a5f2a64007565ed87dad3e2955a71d1f5b31eb1992c1ee77`  
		Last Modified: Fri, 18 Oct 2024 00:31:13 GMT  
		Size: 241.8 MB (241799131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:7fa5fb93c33118b5ace2225168e3a66220b4a4f7c0ea94b599f22a39649623fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.9 KB (758862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc1bc460aee8e1e08dfb95db95786730c4a0b58aec5352403da9bd51c50c52d`

```dockerfile
```

-	Layers:
	-	`sha256:8b91b6f48c74e79f8c38eef16aa7af99c79834dcac8ab6ee8c27425433e72b2c`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 747.0 KB (746984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5587688eb47137d37d13b14e84da8cc45bdc8079dd0cd8f15d98eb2ee4cc79fb`  
		Last Modified: Fri, 18 Oct 2024 00:31:08 GMT  
		Size: 11.9 KB (11878 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:3da385318a04f89f7a8e5d12b0c7091f1cafc5805e160451394926c12101cd7b
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
$ docker pull rust@sha256:4d776039a9a357be19ca9ead57b0656a213619c7298982097a0857d5a605ac5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530870052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea03bd0e673bbc1777121a59412ca6c31511dbd935bcdd06c3ddb1ffe9ced63`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad67b816dd3ebfab16dd19d0768f67e218ed3070e064a66bfa1b026ea84191e`  
		Last Modified: Sat, 19 Oct 2024 08:07:03 GMT  
		Size: 175.2 MB (175210957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f62c598e0e4b12d38b7e9ac6d1e37417fddac22e7efa57555e76096c3484517`  
		Last Modified: Sat, 19 Oct 2024 20:27:03 GMT  
		Size: 228.9 MB (228918647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4d72eab67be576c01e790395a1efc82aa1e3450e34f2c66965ed128ea73929c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7da09c2def11516f2cac29397dd79e45e13edd6a595770e1c583d3f89d9944c`

```dockerfile
```

-	Layers:
	-	`sha256:df68194a4679648dafbc2ce121470f555dc6c97bca93205f2b8b4d349281e903`  
		Last Modified: Sat, 19 Oct 2024 20:26:58 GMT  
		Size: 15.3 MB (15305316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a34b03d3951e72b491cfe93d2ef4efee2d02c129efc7f6c165735b24919d166`  
		Last Modified: Sat, 19 Oct 2024 20:26:57 GMT  
		Size: 13.3 KB (13259 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d82d65d48a0b6d0f5d39f7e8cdd1689fd2c6685007b66b4f021ee6e0704f642b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596180926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4bc4718cff8ac4db4e0cd8f6fb22ad73df411fc871ce08aa34e313e9e769cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d4884f85282b9a352dbcedf2cccd073a63e60b151be84375ce9279dec1c553`  
		Last Modified: Sat, 19 Oct 2024 06:16:07 GMT  
		Size: 202.6 MB (202644222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a5b77d8d49ee81a31cd491be54a349b09b6537083730e14be2f68804799c67`  
		Last Modified: Sat, 19 Oct 2024 20:04:17 GMT  
		Size: 256.0 MB (256007848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a992d3d7fa41a9bf8aa6c833c923c0e21a0dc25a6c95ab6b972a3bf938e60bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f84fa5c1c33f2991055fe2dfed397aa3de67ebdee0e01aa4c66271fc8e2b46`

```dockerfile
```

-	Layers:
	-	`sha256:194d3ee80b090fdab62b570cc0b990cda05ace7cb3697e836047312452491f3e`  
		Last Modified: Sat, 19 Oct 2024 20:04:11 GMT  
		Size: 15.5 MB (15529783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2396872dec21a26fe49789692367fe840fd8d80316a7738dd410585be99ae02`  
		Last Modified: Sat, 19 Oct 2024 20:04:10 GMT  
		Size: 13.3 KB (13303 bytes)  
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
$ docker pull rust@sha256:565a7cef7c714e30d829290ac51d2523b887f2d9f4d75d56e1cee253d91331c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615970277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ee5a636017f864b10932ed1ffffaa50aae11a9cafbeb51f484d37b4d8bfdb9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
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
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3666a280304f3727f745e818ab5e252dd98676495517a360e23f821dee0fa6`  
		Last Modified: Sat, 19 Oct 2024 04:07:03 GMT  
		Size: 69.8 MB (69825530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81280667d7d6fa822ac7a45807cf98017526f614373fad289bacbeb84f61f73`  
		Last Modified: Sat, 19 Oct 2024 05:17:30 GMT  
		Size: 214.3 MB (214300420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd89c17397182837a76641fe74c5ac4688f9cd2afce20f782ae95d0846367cb`  
		Last Modified: Sat, 19 Oct 2024 19:43:12 GMT  
		Size: 252.6 MB (252582753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:55c7db0912be66850720729eb8e68d6d46fcb2806fb1121e3d3ea93c77ff6bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f618aee8535497d6062b875e019ec722cddc0c4322c0a5d64f34c366adb0dafa`

```dockerfile
```

-	Layers:
	-	`sha256:494207d1c19a9f9c9a8a4d0dc0e1f0c0633a0363ad0ec57ef7d284e49afb0805`  
		Last Modified: Sat, 19 Oct 2024 19:42:48 GMT  
		Size: 15.5 MB (15475454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22834bd3dee1022aa23492cd8fbb261876cccacd3df3528af3474cb30116f067`  
		Last Modified: Sat, 19 Oct 2024 19:42:45 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:6713c368dfe236fe7be2509ddce84bf70cca0af2dc709d903ae1ce92be79cd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597392132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda7509db578b0d8f0347aa0bd40839f820e2765c0c04f5b130d0576bac6b6d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
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
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2eccbc8d9b18898de6fc12769f52101d4af82f32957d095f8ab217c6886c2e`  
		Last Modified: Sat, 19 Oct 2024 05:04:19 GMT  
		Size: 183.3 MB (183299744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3c72db5de57d361c959f82e0a383ee33cd8c91b7fecf0aa70ac994ea864dea`  
		Last Modified: Sat, 19 Oct 2024 16:02:42 GMT  
		Size: 278.6 MB (278608964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:71ed314b5bcc9dfacb1b917dad0530f8b0b9c8cf5b0ddbc9493bcc04cbd1bab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6641dd5f17c0fcc76f37070190c900b941c711d4bea89b3494702d5090279d`

```dockerfile
```

-	Layers:
	-	`sha256:eb80b4b6b53506fb47fce58bfe36989307286364157f2aee1c04ae0541182d5e`  
		Last Modified: Sat, 19 Oct 2024 16:02:36 GMT  
		Size: 15.3 MB (15313614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b27a840fe6712fe1894cbbf106e9afa7c2de5d825a7891252b2e6d2004405e`  
		Last Modified: Sat, 19 Oct 2024 16:02:34 GMT  
		Size: 13.2 KB (13151 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:f60dc7ea30e61d39082e0cbf1f92d951e0d5fda2e4a509dd3ed2d5a42e0c4e20
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
$ docker pull rust@sha256:8af7361ea620d72c1f9a173332d936485d3e6ada68c1fc7cf010c8c5e12ec581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.2 MB (512163900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9997bd184a1622957654856fc5ebe3fc26090106fd7183f192aa70de6f36a9e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
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
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a9032c7c4d1cfb31e96212773919f51ec2f6be760fc0f5c35bafbcdb50249`  
		Last Modified: Sat, 19 Oct 2024 06:37:59 GMT  
		Size: 50.6 MB (50613654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0525b656ff73752501ad6cdcf4137840983e49d8b07af0619e3185c5e925fb`  
		Last Modified: Sat, 19 Oct 2024 08:10:07 GMT  
		Size: 167.5 MB (167512354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c43aa88ff2e8544cbb34cb7bc9c4263de3a33dd12595b204ddf8969b943c22`  
		Last Modified: Sat, 19 Oct 2024 20:24:39 GMT  
		Size: 228.9 MB (228918612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c92ce165138230bdc8d92f2774f21b6ff173b0a20a5817d01af1f5b7bb149a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14912080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2d3bb2dd404797f5454017dbdbca9674cf2163035f688ddc8b718e10fb12e`

```dockerfile
```

-	Layers:
	-	`sha256:141db802f68f589a42b222b577ef6b35b39a754ffec66c5715966c6312b9a949`  
		Last Modified: Sat, 19 Oct 2024 20:24:34 GMT  
		Size: 14.9 MB (14900743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e125043ad782c9f35d6018b39446890cd253c6e05a61acee96b6c9d0052428`  
		Last Modified: Sat, 19 Oct 2024 20:24:34 GMT  
		Size: 11.3 KB (11337 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f70e8bd2b2868a1f0cb7a711bb71f74ee77fbc2dd33c0d956251e955e323e21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.3 MB (570294243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3f4d291ce1ea3d241dd96079dafcf5d00bd4f99ec210b356e5bad749185461`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc6072bf5318ca0f9f250b4fcc6254d92483650689f0b0d77274be187abd96`  
		Last Modified: Sat, 19 Oct 2024 05:18:19 GMT  
		Size: 54.8 MB (54832658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13f3e7a61817231ad609702b6918e16648b3eec453567dbedd80952df7e3957`  
		Last Modified: Sat, 19 Oct 2024 06:17:47 GMT  
		Size: 190.0 MB (189971242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93765710d73d66b5b4443516a375c9c981b9ecd07f1ac581fefb956b0624a66`  
		Last Modified: Sat, 19 Oct 2024 20:02:46 GMT  
		Size: 256.0 MB (256007659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e45140ffd2b699e4c5cbdfb96804f7d756a9b862ee163f7d8c74947743b5c51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15113859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d173d7479537f73d26bb16b761a8a0265ca5a070e525ee96191099186ac199f`

```dockerfile
```

-	Layers:
	-	`sha256:38be245007626b5bcaf4d9ab6bc3f6f6e7a944590c035bed3647f40f3ea3fe34`  
		Last Modified: Sat, 19 Oct 2024 20:02:40 GMT  
		Size: 15.1 MB (15102494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddcf7d213da88bc30da54c88258c32d3eb563da066517dfdede3d0f2ebfc82ca`  
		Last Modified: Sat, 19 Oct 2024 20:02:40 GMT  
		Size: 11.4 KB (11365 bytes)  
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
$ docker pull rust@sha256:3da385318a04f89f7a8e5d12b0c7091f1cafc5805e160451394926c12101cd7b
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
$ docker pull rust@sha256:4d776039a9a357be19ca9ead57b0656a213619c7298982097a0857d5a605ac5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530870052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea03bd0e673bbc1777121a59412ca6c31511dbd935bcdd06c3ddb1ffe9ced63`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
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
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad67b816dd3ebfab16dd19d0768f67e218ed3070e064a66bfa1b026ea84191e`  
		Last Modified: Sat, 19 Oct 2024 08:07:03 GMT  
		Size: 175.2 MB (175210957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f62c598e0e4b12d38b7e9ac6d1e37417fddac22e7efa57555e76096c3484517`  
		Last Modified: Sat, 19 Oct 2024 20:27:03 GMT  
		Size: 228.9 MB (228918647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:4d72eab67be576c01e790395a1efc82aa1e3450e34f2c66965ed128ea73929c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15318575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7da09c2def11516f2cac29397dd79e45e13edd6a595770e1c583d3f89d9944c`

```dockerfile
```

-	Layers:
	-	`sha256:df68194a4679648dafbc2ce121470f555dc6c97bca93205f2b8b4d349281e903`  
		Last Modified: Sat, 19 Oct 2024 20:26:58 GMT  
		Size: 15.3 MB (15305316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a34b03d3951e72b491cfe93d2ef4efee2d02c129efc7f6c165735b24919d166`  
		Last Modified: Sat, 19 Oct 2024 20:26:57 GMT  
		Size: 13.3 KB (13259 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d82d65d48a0b6d0f5d39f7e8cdd1689fd2c6685007b66b4f021ee6e0704f642b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.2 MB (596180926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4bc4718cff8ac4db4e0cd8f6fb22ad73df411fc871ce08aa34e313e9e769cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d4884f85282b9a352dbcedf2cccd073a63e60b151be84375ce9279dec1c553`  
		Last Modified: Sat, 19 Oct 2024 06:16:07 GMT  
		Size: 202.6 MB (202644222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a5b77d8d49ee81a31cd491be54a349b09b6537083730e14be2f68804799c67`  
		Last Modified: Sat, 19 Oct 2024 20:04:17 GMT  
		Size: 256.0 MB (256007848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:a992d3d7fa41a9bf8aa6c833c923c0e21a0dc25a6c95ab6b972a3bf938e60bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15543086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f84fa5c1c33f2991055fe2dfed397aa3de67ebdee0e01aa4c66271fc8e2b46`

```dockerfile
```

-	Layers:
	-	`sha256:194d3ee80b090fdab62b570cc0b990cda05ace7cb3697e836047312452491f3e`  
		Last Modified: Sat, 19 Oct 2024 20:04:11 GMT  
		Size: 15.5 MB (15529783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2396872dec21a26fe49789692367fe840fd8d80316a7738dd410585be99ae02`  
		Last Modified: Sat, 19 Oct 2024 20:04:10 GMT  
		Size: 13.3 KB (13303 bytes)  
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
$ docker pull rust@sha256:565a7cef7c714e30d829290ac51d2523b887f2d9f4d75d56e1cee253d91331c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615970277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ee5a636017f864b10932ed1ffffaa50aae11a9cafbeb51f484d37b4d8bfdb9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
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
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3666a280304f3727f745e818ab5e252dd98676495517a360e23f821dee0fa6`  
		Last Modified: Sat, 19 Oct 2024 04:07:03 GMT  
		Size: 69.8 MB (69825530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81280667d7d6fa822ac7a45807cf98017526f614373fad289bacbeb84f61f73`  
		Last Modified: Sat, 19 Oct 2024 05:17:30 GMT  
		Size: 214.3 MB (214300420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd89c17397182837a76641fe74c5ac4688f9cd2afce20f782ae95d0846367cb`  
		Last Modified: Sat, 19 Oct 2024 19:43:12 GMT  
		Size: 252.6 MB (252582753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:55c7db0912be66850720729eb8e68d6d46fcb2806fb1121e3d3ea93c77ff6bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15488673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f618aee8535497d6062b875e019ec722cddc0c4322c0a5d64f34c366adb0dafa`

```dockerfile
```

-	Layers:
	-	`sha256:494207d1c19a9f9c9a8a4d0dc0e1f0c0633a0363ad0ec57ef7d284e49afb0805`  
		Last Modified: Sat, 19 Oct 2024 19:42:48 GMT  
		Size: 15.5 MB (15475454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22834bd3dee1022aa23492cd8fbb261876cccacd3df3528af3474cb30116f067`  
		Last Modified: Sat, 19 Oct 2024 19:42:45 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:6713c368dfe236fe7be2509ddce84bf70cca0af2dc709d903ae1ce92be79cd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597392132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda7509db578b0d8f0347aa0bd40839f820e2765c0c04f5b130d0576bac6b6d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
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
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2eccbc8d9b18898de6fc12769f52101d4af82f32957d095f8ab217c6886c2e`  
		Last Modified: Sat, 19 Oct 2024 05:04:19 GMT  
		Size: 183.3 MB (183299744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3c72db5de57d361c959f82e0a383ee33cd8c91b7fecf0aa70ac994ea864dea`  
		Last Modified: Sat, 19 Oct 2024 16:02:42 GMT  
		Size: 278.6 MB (278608964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:71ed314b5bcc9dfacb1b917dad0530f8b0b9c8cf5b0ddbc9493bcc04cbd1bab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15326765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6641dd5f17c0fcc76f37070190c900b941c711d4bea89b3494702d5090279d`

```dockerfile
```

-	Layers:
	-	`sha256:eb80b4b6b53506fb47fce58bfe36989307286364157f2aee1c04ae0541182d5e`  
		Last Modified: Sat, 19 Oct 2024 16:02:36 GMT  
		Size: 15.3 MB (15313614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b27a840fe6712fe1894cbbf106e9afa7c2de5d825a7891252b2e6d2004405e`  
		Last Modified: Sat, 19 Oct 2024 16:02:34 GMT  
		Size: 13.2 KB (13151 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:60fe5b3207c39d9d52d2b1cc5075f4c71ca7a3ed23dbfa96a19747dafba99afc
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
$ docker pull rust@sha256:6af06831c441ea6efe5da0841875f10c9143e27e2068f7971dc3cb4493777c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301463797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5193a64b31f6521a36ef2a9b1ff2e63c0b09ec71e19c880765a69322380ad8a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65593264902c7ef0684f69975da9c31f1d677a35eb904b8858d752363894bbf`  
		Last Modified: Fri, 18 Oct 2024 04:55:44 GMT  
		Size: 276.7 MB (276745600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:07cd606a2467e9c8ca156915edf6217316d0b6102a08aaa068ce38398d0c8da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec8d2eea1e2fdd0cab72470cfea9e17ba71367f3f8771d876e8f0b01f29744f`

```dockerfile
```

-	Layers:
	-	`sha256:51505a3fb8a002b908713bda6232480bf93d778a2cd307af0732ff66d0af4ef5`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01fab3537dc20a8b760c33a1bcf432402dbbb9e1378901458dee5bc53c51dfb`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 13.2 KB (13194 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:24cfb92a68669bf577b74a7a6e12046851b9d153e0de06e8f902d0aec217ec39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350996361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b376079c1d1c0d19aac1a6d084bdffe036f9c6a0cafab7d6301be6434ac5790d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e35824bcc3a12d7039bc1e45a08bce002fd267d99d1978d3b01ce7613413cd`  
		Last Modified: Fri, 18 Oct 2024 00:28:42 GMT  
		Size: 321.8 MB (321840020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:5a8b2746c65775e6acb4139b0071e720fcddaf9949803347ff1cce9ace3ee2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781b40760ab6bde89d9fd1eaf24672d71f8b0a1557e490646521a2255e054848`

```dockerfile
```

-	Layers:
	-	`sha256:3999435d6d71bfb3d6d5d77e720ef535934122b4b4f23ea3c3b74509b2121080`  
		Last Modified: Fri, 18 Oct 2024 00:28:36 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fbee966e4be75c4c34c2a283707d8db1c220c6dea79aeb970bbd1412776002`  
		Last Modified: Fri, 18 Oct 2024 00:28:35 GMT  
		Size: 13.2 KB (13238 bytes)  
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
$ docker pull rust@sha256:3b3291ce9a66c2810bda45239d5a3204156862ad19a2242f33677249a8cfc792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f37690e23b0d7eeacf9b82ad65ea93c3515164fe329039cf6c3b68b52eadd38`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f43badb6d18c1b7c35c88dd66c3530d7112c29ed622050dccf5b67e8e87040a`  
		Last Modified: Fri, 18 Oct 2024 01:11:21 GMT  
		Size: 321.3 MB (321340278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:cdb656b3036da27b5de1f8da7a2c7649b503346c968c5e98576e50967daafe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c71fdc69f1717530372cc23714c3698b5e2188adf646bb78da5df4383806808`

```dockerfile
```

-	Layers:
	-	`sha256:27eade1d9d895465bc2b8901153021d7ed125b6b270e683c41f8f3fa762fd2ad`  
		Last Modified: Fri, 18 Oct 2024 01:11:13 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d343e81522d031d59cbf59c4478117043e268a002fcae2252af4afee8edfd6`  
		Last Modified: Fri, 18 Oct 2024 01:11:12 GMT  
		Size: 13.2 KB (13154 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:2f15097849b373f3334d043a19a1e2aed41324dfe17969afe5982cb7870d126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356216165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa853f32b6e73890d038285e2b30fc11040dbc95793ddf7db9c55e6742d91af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203d547d95b548a5a647f46a5b304047a4084df212db4a5188e5db5983b530ca`  
		Last Modified: Thu, 17 Oct 2024 23:42:15 GMT  
		Size: 328.7 MB (328726081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:00ee1eca709e062e0adb277cb380fda87dcf1a4a441f517506dca62708eec1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7433567ec5ed96973704f1f3f0a3c1175fc80bab52299c7609f52801f6ddf80`

```dockerfile
```

-	Layers:
	-	`sha256:3a52844eec2dcfc9ce0941a96703ef6a9183abefb170c89f7aaddc53cafa57fc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca49a9d06e01cc7a03e2c5215a23b874c4216aec674651cc808436288f055cc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 13.1 KB (13091 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:60fe5b3207c39d9d52d2b1cc5075f4c71ca7a3ed23dbfa96a19747dafba99afc
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
$ docker pull rust@sha256:6af06831c441ea6efe5da0841875f10c9143e27e2068f7971dc3cb4493777c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301463797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5193a64b31f6521a36ef2a9b1ff2e63c0b09ec71e19c880765a69322380ad8a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65593264902c7ef0684f69975da9c31f1d677a35eb904b8858d752363894bbf`  
		Last Modified: Fri, 18 Oct 2024 04:55:44 GMT  
		Size: 276.7 MB (276745600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:07cd606a2467e9c8ca156915edf6217316d0b6102a08aaa068ce38398d0c8da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec8d2eea1e2fdd0cab72470cfea9e17ba71367f3f8771d876e8f0b01f29744f`

```dockerfile
```

-	Layers:
	-	`sha256:51505a3fb8a002b908713bda6232480bf93d778a2cd307af0732ff66d0af4ef5`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01fab3537dc20a8b760c33a1bcf432402dbbb9e1378901458dee5bc53c51dfb`  
		Last Modified: Fri, 18 Oct 2024 04:55:37 GMT  
		Size: 13.2 KB (13194 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:24cfb92a68669bf577b74a7a6e12046851b9d153e0de06e8f902d0aec217ec39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350996361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b376079c1d1c0d19aac1a6d084bdffe036f9c6a0cafab7d6301be6434ac5790d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e35824bcc3a12d7039bc1e45a08bce002fd267d99d1978d3b01ce7613413cd`  
		Last Modified: Fri, 18 Oct 2024 00:28:42 GMT  
		Size: 321.8 MB (321840020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5a8b2746c65775e6acb4139b0071e720fcddaf9949803347ff1cce9ace3ee2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781b40760ab6bde89d9fd1eaf24672d71f8b0a1557e490646521a2255e054848`

```dockerfile
```

-	Layers:
	-	`sha256:3999435d6d71bfb3d6d5d77e720ef535934122b4b4f23ea3c3b74509b2121080`  
		Last Modified: Fri, 18 Oct 2024 00:28:36 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fbee966e4be75c4c34c2a283707d8db1c220c6dea79aeb970bbd1412776002`  
		Last Modified: Fri, 18 Oct 2024 00:28:35 GMT  
		Size: 13.2 KB (13238 bytes)  
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
$ docker pull rust@sha256:3b3291ce9a66c2810bda45239d5a3204156862ad19a2242f33677249a8cfc792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354462479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f37690e23b0d7eeacf9b82ad65ea93c3515164fe329039cf6c3b68b52eadd38`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f43badb6d18c1b7c35c88dd66c3530d7112c29ed622050dccf5b67e8e87040a`  
		Last Modified: Fri, 18 Oct 2024 01:11:21 GMT  
		Size: 321.3 MB (321340278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:cdb656b3036da27b5de1f8da7a2c7649b503346c968c5e98576e50967daafe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c71fdc69f1717530372cc23714c3698b5e2188adf646bb78da5df4383806808`

```dockerfile
```

-	Layers:
	-	`sha256:27eade1d9d895465bc2b8901153021d7ed125b6b270e683c41f8f3fa762fd2ad`  
		Last Modified: Fri, 18 Oct 2024 01:11:13 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d343e81522d031d59cbf59c4478117043e268a002fcae2252af4afee8edfd6`  
		Last Modified: Fri, 18 Oct 2024 01:11:12 GMT  
		Size: 13.2 KB (13154 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:2f15097849b373f3334d043a19a1e2aed41324dfe17969afe5982cb7870d126f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356216165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa853f32b6e73890d038285e2b30fc11040dbc95793ddf7db9c55e6742d91af`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203d547d95b548a5a647f46a5b304047a4084df212db4a5188e5db5983b530ca`  
		Last Modified: Thu, 17 Oct 2024 23:42:15 GMT  
		Size: 328.7 MB (328726081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:00ee1eca709e062e0adb277cb380fda87dcf1a4a441f517506dca62708eec1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7433567ec5ed96973704f1f3f0a3c1175fc80bab52299c7609f52801f6ddf80`

```dockerfile
```

-	Layers:
	-	`sha256:3a52844eec2dcfc9ce0941a96703ef6a9183abefb170c89f7aaddc53cafa57fc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca49a9d06e01cc7a03e2c5215a23b874c4216aec674651cc808436288f055cc`  
		Last Modified: Thu, 17 Oct 2024 23:42:11 GMT  
		Size: 13.1 KB (13091 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:6ecf4bda0e2b5e7f4610ac8612bc6e01adb3f4451dd8ff16b160be6e07d8c054
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
$ docker pull rust@sha256:cb4937b32194f99b394b565b351807eaa88ca11ad728ccd77ac3f29d3670f85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297762491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789d4d1356befa56ac46e1dd3002047d504df6604c5f112c786846745c11d493`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:45 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Thu, 17 Oct 2024 03:03:46 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f127f81679252c87ada20a6442aab050daaa6280455d330c2ed0e0312ad263`  
		Last Modified: Fri, 18 Oct 2024 04:51:41 GMT  
		Size: 271.2 MB (271172936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7a86756242f0ba3629f641732e0444d8519cb35f5436097966d6e2355c809fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811a4eb5f5f1ce78ce34703dd8554a6e58cbaa0edff11528ac95ebe6d7ca1dcc`

```dockerfile
```

-	Layers:
	-	`sha256:75b8d4d1890e668869883ff090be72445c0bb046190b26558bc015fabccc07b2`  
		Last Modified: Fri, 18 Oct 2024 04:51:36 GMT  
		Size: 4.0 MB (3973767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241f7e92e93b1ef933ca9018e07bab3fb08cc5e31e31246cb29b3057f6c83402`  
		Last Modified: Fri, 18 Oct 2024 04:51:35 GMT  
		Size: 11.2 KB (11246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d453636ade10ddd4286ec5ecdcb24f1a99cedccc09c5c13ad7289b53d33cd31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341766510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e871be81f15e4e120ba9ff8708fa70d21e83ce85e0870e19adae88e2bf2c6e86`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548d0c25fc9eeb4d349077a60a496f321d329205b3f5b06ef193b2adda85c179`  
		Last Modified: Fri, 18 Oct 2024 00:24:20 GMT  
		Size: 311.7 MB (311690753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5ea1413c96faa2e8729eafce7b57890ee56fa150674852e2b38ade7b654fb007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4172471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524fb398c788a87e7ea0b080c814f8340c81e2417be3e25f1b4537c834c21b72`

```dockerfile
```

-	Layers:
	-	`sha256:11b63d16de5274387c9f87faa0b807ce8c15e3150180bddf60776c4ff0e857a7`  
		Last Modified: Fri, 18 Oct 2024 00:24:13 GMT  
		Size: 4.2 MB (4161198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b701d88e21beef1d4a70fdc8b97a5303b2415f3728fdbbef255b1db4950a6e3f`  
		Last Modified: Fri, 18 Oct 2024 00:24:13 GMT  
		Size: 11.3 KB (11273 bytes)  
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
