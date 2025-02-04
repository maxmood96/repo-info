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
-	[`rust:1.84.1`](#rust1841)
-	[`rust:1.84.1-alpine`](#rust1841-alpine)
-	[`rust:1.84.1-alpine3.20`](#rust1841-alpine320)
-	[`rust:1.84.1-alpine3.21`](#rust1841-alpine321)
-	[`rust:1.84.1-bookworm`](#rust1841-bookworm)
-	[`rust:1.84.1-bullseye`](#rust1841-bullseye)
-	[`rust:1.84.1-slim`](#rust1841-slim)
-	[`rust:1.84.1-slim-bookworm`](#rust1841-slim-bookworm)
-	[`rust:1.84.1-slim-bullseye`](#rust1841-slim-bullseye)
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
$ docker pull rust@sha256:efe14eee1be3fd2462fe349b5948b0d1b179b421c9fb23acb20b579f59299daf
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
$ docker pull rust@sha256:d6ffb8c473118907af9c82d36eea7be73220fc86ed49e19e598368093d225124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543203405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14ab37a2b4852c1ba2d6d366516e227688c72b84d99c788d23988ea95769eca`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:2d1bc9b6ae46247afd5d8d1c031d2892c5210d0a1988a7aa81e62b333048122a`  
		Last Modified: Fri, 31 Jan 2025 00:27:31 GMT  
		Size: 194.9 MB (194939965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:5980cc5c19d12031aa61cd2a0b8253fcea0c09ab078d4c8641717c50fce74fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3f7e22174b2c99f85e932d83a5f1afb64561c5542b1cefdabc6f8c4d0faf83`

```dockerfile
```

-	Layers:
	-	`sha256:9026efa626bf98ab0377ccf91c1cdf594bd92d12b04d9e46626ac25f113530cc`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a222081ff21e7b344c50335e732fbfc73127895fe219859f41b6281d09ce103`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:ba90d94af74485087d3bedb060b98f7514cb5eb159319b368db620b6cd849961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.9 MB (531924462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aed138a8a06a33630f51e17d33da618d521427b01bc53c24176f47f28704ec9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18144c873f034f0c1ea60ca2893ae2a4f80c8767a3435cd3a36b6e1d253c8383`  
		Last Modified: Fri, 31 Jan 2025 00:32:29 GMT  
		Size: 230.9 MB (230859587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:24c0bc46c8fb57aec5662c1ba786ebe9f4dcdb1078d38b7db4a8fdb0f8b61e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7749caa656f2cd715044a80e1d6caf2868eb120d5ed8d7853f95f0fa2d0a514a`

```dockerfile
```

-	Layers:
	-	`sha256:114bdef2ab1fe37e9f58ba56ede93a4cb5c6cbc62c6b4e595ba2ccd263add81d`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e977e5b469a4014b4892a72fadd42ef688db4274c78636251af31387c9f5456`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14953a14bbcadb5cac3b9b623a2e19d2d59f9d59a8c93c2924a01352716f07c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597292805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3eb4d2ac479f7339700da0c5bd3d1d8a1c6a0ca4ab1a78f8f04ce47e9be1b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5996c7a64a4f64139ff9df6a590216c8143f5bb1f4c0f41874cf5336645c0`  
		Last Modified: Tue, 14 Jan 2025 17:08:21 GMT  
		Size: 202.7 MB (202716994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0cd049daad112fb47a9e2dc7f5d7ad6cfa0b6d3f7133ad7340085bf7f3521`  
		Last Modified: Fri, 31 Jan 2025 00:33:34 GMT  
		Size: 258.3 MB (258314257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:f37dae26ffeb1e51ff3afdb0315ac4652c790e0937e1e7a86f7d1fa88d173b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d6a21597c6c46be6bcf440046e131973460eb4120a67296a673fb28f007b98`

```dockerfile
```

-	Layers:
	-	`sha256:7f117a3f9871f3caee51a40e122472de613100e18832d07a9ff1a2ec321bb334`  
		Last Modified: Fri, 31 Jan 2025 00:33:27 GMT  
		Size: 15.5 MB (15502759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072319fe7967b8c2719006732f2548e51280f95233f294259687c942ab4f468e`  
		Last Modified: Fri, 31 Jan 2025 00:33:26 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:821a7a54c3f58639c91978c1237d7fa01e3a65e44238481fd9c770976cbd0e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562262370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a43c27946e528ead9015a0e00f8ded1f86bc93b6b7512ffc08a35b7539a462b`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:0b9d29e39242117927b00082eced1422486e6bf62ed48fd1d3f7d4eea941b259`  
		Last Modified: Fri, 31 Jan 2025 00:27:40 GMT  
		Size: 211.4 MB (211430918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:9ff4e7a8299cf2f331d79afc3fabfd39991b4beb4ea9c6237f06dd8826635db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08733e110be67a5cf02046201f755ec7f7ad7f00549188b91633be0e25c38d75`

```dockerfile
```

-	Layers:
	-	`sha256:8289295e1eb2e71548b9790670abc045a9972cb92a1c524c67f4d34c0a77c551`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd86c221361bfb6476de8f5a7a8137335371177cb4960b16f37f2d59d14173e`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:c98ba917122d2941ed71ef0198e5dd450094a0ff2b61d5e4ad86c03b600f6f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.0 MB (617042336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db8805653b8f10d290d02effd1a5a9a5c19720cb0484d99386ff6611a43cbd9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc81baa5d59fc087ff9c3033ea4eb1bfa715f31d7e3ea65371060635cb593034`  
		Last Modified: Fri, 31 Jan 2025 00:28:41 GMT  
		Size: 254.8 MB (254802966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:37354536f1477490c54912769c533260bffb8fb982d4fceeaa620e43762b803a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d416eaf25b6818b699095b9b17260d6abffe59157e6bbd857eb9bf38d85073`

```dockerfile
```

-	Layers:
	-	`sha256:dd4b0559fbf93a64f693655a44f3f7e091038e0508cd2af9cb660159b9a853a2`  
		Last Modified: Fri, 31 Jan 2025 00:28:34 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f020d262064a1f8e6aa92c5030c699e1f215c9db15a0e712436ec6f070378770`  
		Last Modified: Fri, 31 Jan 2025 00:28:33 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:d5960a1389fd5d0c8cd692f1e03bd49d89ea89599a0bd364b5fb3564795424f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599964843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f1fd155400b48e6e5b702ece9550a582f33605caf345c92e428b1fd248f9ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69de93bafada368b0e0985055a008874d24d736e83961f9b10d61d5a68bf51c3`  
		Last Modified: Fri, 31 Jan 2025 00:29:24 GMT  
		Size: 281.9 MB (281918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:188d0a76db21e823b3b424dc44f3d32f1f0d7a9fd734d505dd093a5c8ae04b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f291615bd9af8888d1d4c5a8b528d1ee3349885227ba2c2906f6219f646b808d`

```dockerfile
```

-	Layers:
	-	`sha256:3c1643fc4bdd3ec8efd59a842bce38261ffbcb07139b970d7db83df83ecf5baf`  
		Last Modified: Fri, 31 Jan 2025 00:29:20 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30c0064df1d0ffc289ce1d91423cf2048228fb82276833b98b9b1ba5bf4c4bb`  
		Last Modified: Fri, 31 Jan 2025 00:29:19 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:18be086bb0b8b45a04e6cb1a55863852cfdf81d7abed75ea588acb7f4aa6748e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:919360958a6d487fa56f8d7cb102c897466991a98d195417ba975b28ac9432dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304581935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173cee671d366c16cd437003be211507d5afe676e262e62cb3ece9c22a3e3fa5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a339c2254caf5d4b71a878c1f61c73ed11450f099b1d317e8f3d3b0d2ba7d24`  
		Last Modified: Fri, 31 Jan 2025 00:27:25 GMT  
		Size: 61.6 MB (61564867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18309f435aeec843fd40d87f81417cf4fc4a669e1a697ae887b1b6364dad8f45`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 239.4 MB (239375353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:f0e1697f58f041b40e13dfe200b3d2878c4947f75532b671ef2ab01a87b76954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be83ec1ac744d4c41931a1101fceb07ee7b35d2b08aa747d9633e128e0bc578`

```dockerfile
```

-	Layers:
	-	`sha256:4a60dc9b2069fb8f008a6ebb143dc0d471c227fbbdd7e471bd573d8f3a2ae301`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab6210992562f33b8fb8a048172b9f29dd7c2f3b614e5a27ab729c42b9a7ad6`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:31bede8f9a632bc843e74af6757b35e56c7236086ba3992f51b3850fe864c922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307001444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afac4100d4af97dfac2eacb50ce61762f686680e5e8b577e83383d5effbcaf76`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548af7367683a8ad83d856786059e3f702f6e555d4c6fa75b5ae9ca66c6a853`  
		Last Modified: Fri, 31 Jan 2025 00:37:15 GMT  
		Size: 59.1 MB (59101145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2468ea22c5495d7b5836325b324ac275679df6c2762c658eb36b38e6107108`  
		Last Modified: Fri, 31 Jan 2025 00:37:19 GMT  
		Size: 243.9 MB (243907940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:e909bda5d8bab6cd1e6be99142887733fb6eb509306720ce2d566866768e2f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4954689616e540d48c85cb359d67157da8bd72d844188e2e7f0387049acd01`

```dockerfile
```

-	Layers:
	-	`sha256:513f93d9e310f3e8b4ddb854244e175c468d3e6c308bcc64ab9a83e594bdb444`  
		Last Modified: Fri, 31 Jan 2025 00:37:14 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed14993fe5fbca94a7caf5f00ed99b23d749da67a5db0083c4430891c910d80f`  
		Last Modified: Fri, 31 Jan 2025 00:37:13 GMT  
		Size: 12.1 KB (12083 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:5b65959f00c8fcc9bfabb76644c4eefa0b97f8af37040dd163592536dbd6e107
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:90846f2d591b7df8b6a24acf0b3b49b7c6505703190371f40d2f442498d2aa84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298316995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dfb378cd0fe965ee75d63fe3291757ea7876f5f7a4663e818d135f8ff2fbdc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77927bf1e96f21719646e6bae28029a1ae3f345fbe3909a6339189205890e1a`  
		Last Modified: Fri, 31 Jan 2025 00:27:17 GMT  
		Size: 55.3 MB (55315542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f429e09b0fa861e6542ecd21fefac35a3c2b405055fd9b74e31db3677f9db3`  
		Last Modified: Fri, 31 Jan 2025 00:27:20 GMT  
		Size: 239.4 MB (239375193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:03c2f4be77e68d8908fa4675b8cd24b056465943604991e23d40ae0961f1eca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1b5a1a42abcdcd793be2182d1682cd4e866f179bcebde2d0ddff81565cd141`

```dockerfile
```

-	Layers:
	-	`sha256:453fda6d733a61c5795fb7921bfbc21174ce9d1a30bfd83612d6e2e341b4028d`  
		Last Modified: Fri, 31 Jan 2025 00:27:16 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:571392ac9483c44b5395d2f6c12baae68eb19d840a081880a6c4f3194dc317ee`  
		Last Modified: Fri, 31 Jan 2025 00:27:16 GMT  
		Size: 10.7 KB (10713 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:59d7abf2b2cdc63cd4917924cb23135299f18b1aa5152baddab0fc0db9d851b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300949670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda6582639290a8a26ebbe011b767cf366d257472d3b950df2bbeb6c91b2cd3d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f023fbab63b00375fb771d16cd745c9a1ff513cda460f1e701e3b66e9ff86d`  
		Last Modified: Fri, 31 Jan 2025 00:36:11 GMT  
		Size: 53.0 MB (52951018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f22d4c62442d75cfd04ad26c9c5455e25bebf3384ec4e5be257e364d6aeb4`  
		Last Modified: Fri, 31 Jan 2025 00:36:15 GMT  
		Size: 243.9 MB (243907883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:c87b653694e961dff4fcbd925991fb2db9f8afbf3a05ace8351287adc3e8f29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ea31be4c87b9f661044c3b4d19d40df023745400966e4e2ddbebd135a3f62b`

```dockerfile
```

-	Layers:
	-	`sha256:2371f11175124cfba85292d79ffac38eea16a98d653da2f12fc5e9ba206099e4`  
		Last Modified: Fri, 31 Jan 2025 00:36:09 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10caafcae281ac20e919dcc1e71c9cb267ab5d223ab59cffe4fcf159262c0fa5`  
		Last Modified: Fri, 31 Jan 2025 00:36:09 GMT  
		Size: 10.8 KB (10832 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.21`

```console
$ docker pull rust@sha256:18be086bb0b8b45a04e6cb1a55863852cfdf81d7abed75ea588acb7f4aa6748e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:919360958a6d487fa56f8d7cb102c897466991a98d195417ba975b28ac9432dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304581935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173cee671d366c16cd437003be211507d5afe676e262e62cb3ece9c22a3e3fa5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a339c2254caf5d4b71a878c1f61c73ed11450f099b1d317e8f3d3b0d2ba7d24`  
		Last Modified: Fri, 31 Jan 2025 00:27:25 GMT  
		Size: 61.6 MB (61564867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18309f435aeec843fd40d87f81417cf4fc4a669e1a697ae887b1b6364dad8f45`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 239.4 MB (239375353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:f0e1697f58f041b40e13dfe200b3d2878c4947f75532b671ef2ab01a87b76954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be83ec1ac744d4c41931a1101fceb07ee7b35d2b08aa747d9633e128e0bc578`

```dockerfile
```

-	Layers:
	-	`sha256:4a60dc9b2069fb8f008a6ebb143dc0d471c227fbbdd7e471bd573d8f3a2ae301`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab6210992562f33b8fb8a048172b9f29dd7c2f3b614e5a27ab729c42b9a7ad6`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:31bede8f9a632bc843e74af6757b35e56c7236086ba3992f51b3850fe864c922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307001444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afac4100d4af97dfac2eacb50ce61762f686680e5e8b577e83383d5effbcaf76`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548af7367683a8ad83d856786059e3f702f6e555d4c6fa75b5ae9ca66c6a853`  
		Last Modified: Fri, 31 Jan 2025 00:37:15 GMT  
		Size: 59.1 MB (59101145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2468ea22c5495d7b5836325b324ac275679df6c2762c658eb36b38e6107108`  
		Last Modified: Fri, 31 Jan 2025 00:37:19 GMT  
		Size: 243.9 MB (243907940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:e909bda5d8bab6cd1e6be99142887733fb6eb509306720ce2d566866768e2f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4954689616e540d48c85cb359d67157da8bd72d844188e2e7f0387049acd01`

```dockerfile
```

-	Layers:
	-	`sha256:513f93d9e310f3e8b4ddb854244e175c468d3e6c308bcc64ab9a83e594bdb444`  
		Last Modified: Fri, 31 Jan 2025 00:37:14 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed14993fe5fbca94a7caf5f00ed99b23d749da67a5db0083c4430891c910d80f`  
		Last Modified: Fri, 31 Jan 2025 00:37:13 GMT  
		Size: 12.1 KB (12083 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:efe14eee1be3fd2462fe349b5948b0d1b179b421c9fb23acb20b579f59299daf
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
$ docker pull rust@sha256:d6ffb8c473118907af9c82d36eea7be73220fc86ed49e19e598368093d225124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543203405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14ab37a2b4852c1ba2d6d366516e227688c72b84d99c788d23988ea95769eca`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:2d1bc9b6ae46247afd5d8d1c031d2892c5210d0a1988a7aa81e62b333048122a`  
		Last Modified: Fri, 31 Jan 2025 00:27:31 GMT  
		Size: 194.9 MB (194939965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5980cc5c19d12031aa61cd2a0b8253fcea0c09ab078d4c8641717c50fce74fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3f7e22174b2c99f85e932d83a5f1afb64561c5542b1cefdabc6f8c4d0faf83`

```dockerfile
```

-	Layers:
	-	`sha256:9026efa626bf98ab0377ccf91c1cdf594bd92d12b04d9e46626ac25f113530cc`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a222081ff21e7b344c50335e732fbfc73127895fe219859f41b6281d09ce103`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ba90d94af74485087d3bedb060b98f7514cb5eb159319b368db620b6cd849961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.9 MB (531924462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aed138a8a06a33630f51e17d33da618d521427b01bc53c24176f47f28704ec9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18144c873f034f0c1ea60ca2893ae2a4f80c8767a3435cd3a36b6e1d253c8383`  
		Last Modified: Fri, 31 Jan 2025 00:32:29 GMT  
		Size: 230.9 MB (230859587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:24c0bc46c8fb57aec5662c1ba786ebe9f4dcdb1078d38b7db4a8fdb0f8b61e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7749caa656f2cd715044a80e1d6caf2868eb120d5ed8d7853f95f0fa2d0a514a`

```dockerfile
```

-	Layers:
	-	`sha256:114bdef2ab1fe37e9f58ba56ede93a4cb5c6cbc62c6b4e595ba2ccd263add81d`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e977e5b469a4014b4892a72fadd42ef688db4274c78636251af31387c9f5456`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14953a14bbcadb5cac3b9b623a2e19d2d59f9d59a8c93c2924a01352716f07c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597292805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3eb4d2ac479f7339700da0c5bd3d1d8a1c6a0ca4ab1a78f8f04ce47e9be1b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5996c7a64a4f64139ff9df6a590216c8143f5bb1f4c0f41874cf5336645c0`  
		Last Modified: Tue, 14 Jan 2025 17:08:21 GMT  
		Size: 202.7 MB (202716994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0cd049daad112fb47a9e2dc7f5d7ad6cfa0b6d3f7133ad7340085bf7f3521`  
		Last Modified: Fri, 31 Jan 2025 00:33:34 GMT  
		Size: 258.3 MB (258314257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f37dae26ffeb1e51ff3afdb0315ac4652c790e0937e1e7a86f7d1fa88d173b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d6a21597c6c46be6bcf440046e131973460eb4120a67296a673fb28f007b98`

```dockerfile
```

-	Layers:
	-	`sha256:7f117a3f9871f3caee51a40e122472de613100e18832d07a9ff1a2ec321bb334`  
		Last Modified: Fri, 31 Jan 2025 00:33:27 GMT  
		Size: 15.5 MB (15502759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072319fe7967b8c2719006732f2548e51280f95233f294259687c942ab4f468e`  
		Last Modified: Fri, 31 Jan 2025 00:33:26 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:821a7a54c3f58639c91978c1237d7fa01e3a65e44238481fd9c770976cbd0e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562262370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a43c27946e528ead9015a0e00f8ded1f86bc93b6b7512ffc08a35b7539a462b`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:0b9d29e39242117927b00082eced1422486e6bf62ed48fd1d3f7d4eea941b259`  
		Last Modified: Fri, 31 Jan 2025 00:27:40 GMT  
		Size: 211.4 MB (211430918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9ff4e7a8299cf2f331d79afc3fabfd39991b4beb4ea9c6237f06dd8826635db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08733e110be67a5cf02046201f755ec7f7ad7f00549188b91633be0e25c38d75`

```dockerfile
```

-	Layers:
	-	`sha256:8289295e1eb2e71548b9790670abc045a9972cb92a1c524c67f4d34c0a77c551`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd86c221361bfb6476de8f5a7a8137335371177cb4960b16f37f2d59d14173e`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:c98ba917122d2941ed71ef0198e5dd450094a0ff2b61d5e4ad86c03b600f6f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.0 MB (617042336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db8805653b8f10d290d02effd1a5a9a5c19720cb0484d99386ff6611a43cbd9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc81baa5d59fc087ff9c3033ea4eb1bfa715f31d7e3ea65371060635cb593034`  
		Last Modified: Fri, 31 Jan 2025 00:28:41 GMT  
		Size: 254.8 MB (254802966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:37354536f1477490c54912769c533260bffb8fb982d4fceeaa620e43762b803a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d416eaf25b6818b699095b9b17260d6abffe59157e6bbd857eb9bf38d85073`

```dockerfile
```

-	Layers:
	-	`sha256:dd4b0559fbf93a64f693655a44f3f7e091038e0508cd2af9cb660159b9a853a2`  
		Last Modified: Fri, 31 Jan 2025 00:28:34 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f020d262064a1f8e6aa92c5030c699e1f215c9db15a0e712436ec6f070378770`  
		Last Modified: Fri, 31 Jan 2025 00:28:33 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:d5960a1389fd5d0c8cd692f1e03bd49d89ea89599a0bd364b5fb3564795424f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599964843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f1fd155400b48e6e5b702ece9550a582f33605caf345c92e428b1fd248f9ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69de93bafada368b0e0985055a008874d24d736e83961f9b10d61d5a68bf51c3`  
		Last Modified: Fri, 31 Jan 2025 00:29:24 GMT  
		Size: 281.9 MB (281918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:188d0a76db21e823b3b424dc44f3d32f1f0d7a9fd734d505dd093a5c8ae04b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f291615bd9af8888d1d4c5a8b528d1ee3349885227ba2c2906f6219f646b808d`

```dockerfile
```

-	Layers:
	-	`sha256:3c1643fc4bdd3ec8efd59a842bce38261ffbcb07139b970d7db83df83ecf5baf`  
		Last Modified: Fri, 31 Jan 2025 00:29:20 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30c0064df1d0ffc289ce1d91423cf2048228fb82276833b98b9b1ba5bf4c4bb`  
		Last Modified: Fri, 31 Jan 2025 00:29:19 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:c4b1a57d45f13da4e88a581f5a2afec8fe88f5e34f1b42ad6b57263e007a10a8
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
$ docker pull rust@sha256:19e8e36b68de2035d1973180ade2170e4774b690f212e85426f8bb0f937bd235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.1 MB (516065029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9297b737a5f133ae508b1fd5c45759abd800a6f61fad6de049c5d1bf07090fe0`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:af5ffb44a6cd66d2c8993ddcc676a7100f7e86dc7808d0e11f1c5334d647a801`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 194.9 MB (194939976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:11213337bcc0a4d8064ffe13cb4f22bbcc652db9a58641d38f6019449cfad416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20ff9776cd1189493fc85a07efa4f9d8b3a87b85b1bb57986292831864c0237`

```dockerfile
```

-	Layers:
	-	`sha256:652e654fbafc7f8f0e97a8b25d486384e065ce80757ee0d4034910960ec1c289`  
		Last Modified: Fri, 31 Jan 2025 00:27:26 GMT  
		Size: 15.1 MB (15073395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410b01f8bbd6b016bb9db97e55638faaed4bf3dd7330dd758b5377d378bed762`  
		Last Modified: Fri, 31 Jan 2025 00:27:26 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:75471b41a597a6b1cfe6b24d628778f83796fb8575be44203e271c72a632e756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.7 MB (512724563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b15ecb05694d471bab508c576f8f71eb5867995620ba8f3759697e468f4975`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526075af1d9c0b728ff0e8888d46f79edd8fb9bacc975b1eb824b9bca2c06ee2`  
		Last Modified: Tue, 14 Jan 2025 21:56:34 GMT  
		Size: 167.5 MB (167525487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87cd816ef0e7cda0866402374e031c5b8eb8ea446c803396cee74b94e63493`  
		Last Modified: Fri, 31 Jan 2025 00:28:09 GMT  
		Size: 230.9 MB (230859536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f1c0976e1db9aafadb3c580636078c95f7985e70f131d271e03a322ac5d14abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e17bf1d055434cff4b3dbe7e53bb338f902850477ceb27958427bf7f6606a6`

```dockerfile
```

-	Layers:
	-	`sha256:cc2c8998bd0731810057c3b6047bab175c7016f12fd655d5aa1e755b96e2c50b`  
		Last Modified: Fri, 31 Jan 2025 00:27:59 GMT  
		Size: 14.9 MB (14874186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e376b8a774cb79f115c38a0a607c8d05c504e16ee1d897d8c21f0a6d7ecbeb48`  
		Last Modified: Fri, 31 Jan 2025 00:27:58 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:44dacf67a0f2d6e45cf20069750d1134fe117313e6b2dcb50425c28f6379f2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.9 MB (570937169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3120e33651377b4d4ddf5f4045cd3dde40315ba55c184b30928df0e844e35d08`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5936a36467e76a2d54993295f16ff38dd2c24f30cf89a1f83a922f2440b869`  
		Last Modified: Tue, 14 Jan 2025 17:09:53 GMT  
		Size: 190.0 MB (189980217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c97e0ab9340a3d9325e91e9d4f4b0681104e08ea083ef3914b9651b0a37ac`  
		Last Modified: Fri, 31 Jan 2025 00:30:23 GMT  
		Size: 258.3 MB (258314197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c1efe8411d5ddbd6ca7a84d0818c74e3bc1323fa49726ee6d4377e71186528f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7407ece2d925e5125f770ec29fbf720030c739a4ee20f89da0b24b6f1ca0ed29`

```dockerfile
```

-	Layers:
	-	`sha256:a791efb39aced3bfe7117d624ded6cb55bea86b2271b1b444ef7ecf2e35e65df`  
		Last Modified: Fri, 31 Jan 2025 00:30:18 GMT  
		Size: 15.1 MB (15075655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57cc19c32562fe05349d5c04dc3d40ca3fc4def915ca05fa9c1e4ccbc766ccd8`  
		Last Modified: Fri, 31 Jan 2025 00:30:17 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:ac7ebc2fbe359f9f7ad0c39453c80fd51a95e36f18a701d6df27390ca80c15ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.2 MB (538175938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4364c30642d359ebfdc54b274d0009f14e9cfbff1615478473abcd5291f960`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:ee8b3ada43c92b49d5a6758eda5322a4cfce6900a0c9996fb07cbc761dac8c45`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 211.4 MB (211430901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c1401012f1340b3d4d9623d00a4943177803bda897ca5651d637abc44a4c0812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2931a49ceab2dabcdff00bf99889b9353ec2ae41c99a5c3a85fa06101969c019`

```dockerfile
```

-	Layers:
	-	`sha256:b6652171b2db2c97f124d831aa76fe73fa658a589f1ac3fc9075a0a2dbcc608e`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 15.1 MB (15060422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1076671420ac46738dce103d762c400e7b9a9ed43be6137e7305585e331f26e`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:38ed9b34e7f3014723818a33871f4c244f3cf36c019d7341f6d9e5114cbdb596
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
$ docker pull rust@sha256:f1c6e953d9cfe4bd8eb4512a82647ef68965484714eb63d925b955458a357133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293935426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988feec34834b11f5aa7cb2677d196dbfb5bbfdfc4861134f6a01a22db095311`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1020b52149c924fa9f87f51bccb15dda19dec1c715e94e820355a3ea83202f7a`  
		Last Modified: Tue, 04 Feb 2025 04:48:25 GMT  
		Size: 265.7 MB (265723123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:79b36bc5042f238a4f3cffa1cbae990fec5b128951bd59298d1ccca3889bb1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c142e6c658521625b57a6e7bde7086b8625cea33c465791bf28cfe3745d8162`

```dockerfile
```

-	Layers:
	-	`sha256:8b1d943955598274f0f568ee76323314f21350045e470ad5a88fde875d1fccf6`  
		Last Modified: Tue, 04 Feb 2025 04:48:19 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8851e0f18f7ad661f6aed4f8fa89d47fcba726ffd8f76a32f5549dc3ea59379`  
		Last Modified: Tue, 04 Feb 2025 04:48:18 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:7895aa006490737a03b7cbe889f7ed3d8d5e28db4e894d3f79a5268aa0833dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302634826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f66ad885bf45b2d1a94ddc15323fd2d3928947e6973936ca6ca470f72c3bced`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e30f41f234176f2c16ce777337f908a1a5494227de2d5a8d969a9dd5c123a18`  
		Last Modified: Fri, 31 Jan 2025 00:34:31 GMT  
		Size: 278.7 MB (278720226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a423820d19893d117d3df4fc559613e7530115a5bc0d8cf3c33fd06c0a6e99c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ddadfc654a5a9aac9217f3fac5ff192f87119cad1733955a064f26eaa22138`

```dockerfile
```

-	Layers:
	-	`sha256:cfbe61d6317e4746f8563feb4f577d0e41544c362913a508ebf36365509cebaa`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2cc265269c6bdf19d72d395d5c8bdc5d5c6ad462c4fb8ebb54d824b01cf809a`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bd37300c571a784c02cc6511be16d9f94edb5dbd0e02095213552efb4f06ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352196288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd2883e9d25ded400d0c78e03183e85ceac746ce72f11b2087bdd25d5aafc12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2851b7f466da485d0e64c4855d4ab4b2db80c9c50770dd57605c43fd6c7cdfd`  
		Last Modified: Fri, 31 Jan 2025 00:35:06 GMT  
		Size: 324.2 MB (324155257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:7d5eefa74740563880088f83d8890ff19bad3c43632520ce3217dbc1c7e4df04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb4bb2ea3aa5392b9be7b81d22a58b0149ef8d1151ba02341049dd9f638b663`

```dockerfile
```

-	Layers:
	-	`sha256:bf9fcdda35b8ab6ece9a6cb4a44f12efe6de3c8dd5bfa18d73cd9d75d00f91a3`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ba4b082669b49e4b3c44cb5d514d34fb2702a836c5f399a486a5e78c5de35c`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:d482b4787a73d9059bf5cba29999c0001d86767bf1b59b0cd8234504f1752539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308216502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5909b6178c847cfba84bcfa51b9d15491e08801021fbe9ec32369dc9a5cc9d72`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a1bebc92f7ad633f86d3b27faacbf962b234bef49b7ac15d9fa204f831a39d`  
		Last Modified: Tue, 04 Feb 2025 04:41:58 GMT  
		Size: 279.0 MB (279029046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:9b55b0bc360983ef31668d29f0831fd2f4fa885b45aeeb2e233a3ddb2a1e124d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edd34bcca496a057e05b0f78d548c9eddf9b6a2708b44833ce347d301ce24a`

```dockerfile
```

-	Layers:
	-	`sha256:b1be01bfc9316ad7a57a60c173d15ea8d7a8530d42e3983624bc3d266eeeb8d8`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1188dc47ed580591433d16de41cd10911b115b3f2865d23a352e584d38d565e`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:0ae493364decaf0420efa4ddc9cbf1554fcf147142049c52ddef57f14ed17c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355608891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ab5118ccde6aebb13da6de1ca490126cd64d28370c877db5be19bccce4685a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc73567e881b68c8629ad1da7bb11b2b21a1caa40e61c21f214bd45f2ad0aec`  
		Last Modified: Fri, 31 Jan 2025 00:31:21 GMT  
		Size: 323.6 MB (323564044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:5f9bc075b26d9f54a8993714fef535de2c3e525df84032f34f4e2cf036e57b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4572aa06386fc1be43fc645e09df3c69c1e4255b9c0dc6b9c381e50fcad395a1`

```dockerfile
```

-	Layers:
	-	`sha256:951b107c9596b3fd7667ac8fd8883145e533afb92e754bcbb6cc37abf43ab36f`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6707e52cd8b0edb10aa0f3f29ac9c470549477008999a2c916b77361a8312a8d`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:424e8413fb24c88edcaf1b689d990cc1b5d81b583332b5e8a4ebce0096a63407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358910439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a330311272f88ad3a31b23af36f93ea27b553e9eea634ea85e9ee60bf5ced46`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62668347d57abb66f2a0fab8774ffa016537604baf01fcee21fed7e2eb0f2f2d`  
		Last Modified: Fri, 31 Jan 2025 00:31:50 GMT  
		Size: 332.1 MB (332051701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:9fac2330e6da662b2713d2fde23bccfece116ba1bae59e81caaf18ec826d894c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e108fb041bf31c5ba2da80bed4e81113f09211cc58c1fa5ec8b48a6b532a90f`

```dockerfile
```

-	Layers:
	-	`sha256:a2a614ddb9300e6a218d557b5695ac3ab1776f904ceb81622d2cf584fcafad94`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb8842e3556a08959bdf1331108cdf9b1b1ab475e502e6cf2e1863ef156cad6f`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:38ed9b34e7f3014723818a33871f4c244f3cf36c019d7341f6d9e5114cbdb596
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
$ docker pull rust@sha256:f1c6e953d9cfe4bd8eb4512a82647ef68965484714eb63d925b955458a357133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293935426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988feec34834b11f5aa7cb2677d196dbfb5bbfdfc4861134f6a01a22db095311`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1020b52149c924fa9f87f51bccb15dda19dec1c715e94e820355a3ea83202f7a`  
		Last Modified: Tue, 04 Feb 2025 04:48:25 GMT  
		Size: 265.7 MB (265723123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:79b36bc5042f238a4f3cffa1cbae990fec5b128951bd59298d1ccca3889bb1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c142e6c658521625b57a6e7bde7086b8625cea33c465791bf28cfe3745d8162`

```dockerfile
```

-	Layers:
	-	`sha256:8b1d943955598274f0f568ee76323314f21350045e470ad5a88fde875d1fccf6`  
		Last Modified: Tue, 04 Feb 2025 04:48:19 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8851e0f18f7ad661f6aed4f8fa89d47fcba726ffd8f76a32f5549dc3ea59379`  
		Last Modified: Tue, 04 Feb 2025 04:48:18 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:7895aa006490737a03b7cbe889f7ed3d8d5e28db4e894d3f79a5268aa0833dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302634826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f66ad885bf45b2d1a94ddc15323fd2d3928947e6973936ca6ca470f72c3bced`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e30f41f234176f2c16ce777337f908a1a5494227de2d5a8d969a9dd5c123a18`  
		Last Modified: Fri, 31 Jan 2025 00:34:31 GMT  
		Size: 278.7 MB (278720226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a423820d19893d117d3df4fc559613e7530115a5bc0d8cf3c33fd06c0a6e99c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ddadfc654a5a9aac9217f3fac5ff192f87119cad1733955a064f26eaa22138`

```dockerfile
```

-	Layers:
	-	`sha256:cfbe61d6317e4746f8563feb4f577d0e41544c362913a508ebf36365509cebaa`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2cc265269c6bdf19d72d395d5c8bdc5d5c6ad462c4fb8ebb54d824b01cf809a`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bd37300c571a784c02cc6511be16d9f94edb5dbd0e02095213552efb4f06ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352196288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd2883e9d25ded400d0c78e03183e85ceac746ce72f11b2087bdd25d5aafc12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2851b7f466da485d0e64c4855d4ab4b2db80c9c50770dd57605c43fd6c7cdfd`  
		Last Modified: Fri, 31 Jan 2025 00:35:06 GMT  
		Size: 324.2 MB (324155257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7d5eefa74740563880088f83d8890ff19bad3c43632520ce3217dbc1c7e4df04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb4bb2ea3aa5392b9be7b81d22a58b0149ef8d1151ba02341049dd9f638b663`

```dockerfile
```

-	Layers:
	-	`sha256:bf9fcdda35b8ab6ece9a6cb4a44f12efe6de3c8dd5bfa18d73cd9d75d00f91a3`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ba4b082669b49e4b3c44cb5d514d34fb2702a836c5f399a486a5e78c5de35c`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:d482b4787a73d9059bf5cba29999c0001d86767bf1b59b0cd8234504f1752539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308216502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5909b6178c847cfba84bcfa51b9d15491e08801021fbe9ec32369dc9a5cc9d72`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a1bebc92f7ad633f86d3b27faacbf962b234bef49b7ac15d9fa204f831a39d`  
		Last Modified: Tue, 04 Feb 2025 04:41:58 GMT  
		Size: 279.0 MB (279029046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9b55b0bc360983ef31668d29f0831fd2f4fa885b45aeeb2e233a3ddb2a1e124d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edd34bcca496a057e05b0f78d548c9eddf9b6a2708b44833ce347d301ce24a`

```dockerfile
```

-	Layers:
	-	`sha256:b1be01bfc9316ad7a57a60c173d15ea8d7a8530d42e3983624bc3d266eeeb8d8`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1188dc47ed580591433d16de41cd10911b115b3f2865d23a352e584d38d565e`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:0ae493364decaf0420efa4ddc9cbf1554fcf147142049c52ddef57f14ed17c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355608891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ab5118ccde6aebb13da6de1ca490126cd64d28370c877db5be19bccce4685a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc73567e881b68c8629ad1da7bb11b2b21a1caa40e61c21f214bd45f2ad0aec`  
		Last Modified: Fri, 31 Jan 2025 00:31:21 GMT  
		Size: 323.6 MB (323564044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5f9bc075b26d9f54a8993714fef535de2c3e525df84032f34f4e2cf036e57b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4572aa06386fc1be43fc645e09df3c69c1e4255b9c0dc6b9c381e50fcad395a1`

```dockerfile
```

-	Layers:
	-	`sha256:951b107c9596b3fd7667ac8fd8883145e533afb92e754bcbb6cc37abf43ab36f`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6707e52cd8b0edb10aa0f3f29ac9c470549477008999a2c916b77361a8312a8d`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:424e8413fb24c88edcaf1b689d990cc1b5d81b583332b5e8a4ebce0096a63407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358910439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a330311272f88ad3a31b23af36f93ea27b553e9eea634ea85e9ee60bf5ced46`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62668347d57abb66f2a0fab8774ffa016537604baf01fcee21fed7e2eb0f2f2d`  
		Last Modified: Fri, 31 Jan 2025 00:31:50 GMT  
		Size: 332.1 MB (332051701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9fac2330e6da662b2713d2fde23bccfece116ba1bae59e81caaf18ec826d894c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e108fb041bf31c5ba2da80bed4e81113f09211cc58c1fa5ec8b48a6b532a90f`

```dockerfile
```

-	Layers:
	-	`sha256:a2a614ddb9300e6a218d557b5695ac3ab1776f904ceb81622d2cf584fcafad94`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb8842e3556a08959bdf1331108cdf9b1b1ab475e502e6cf2e1863ef156cad6f`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:daeff596870266ef69308e65d01c8007ba61afb96a027eb80da16a4bf62e8c8e
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
$ docker pull rust@sha256:2b7845424e9284f1c26bd56fedd1483e6ca44e639ac4bf9141d9ad9c88b973ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285143356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee24319d37d90b47217bc8804087eb7618520d2d2998feaf3f673390cea2aa2f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38d52395664bc85f1e799519d83f7fac8d684946c51459db24960ed59d1aa7c`  
		Last Modified: Tue, 04 Feb 2025 04:48:14 GMT  
		Size: 254.9 MB (254890768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:40a8dc8468f83fe69082db8cc94d464f6986e7d5c4f3602a922cbfcc9e0db833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257a7ca891da9b98541d5a34a69aa9d1418765d9d43df2afbc37bbf746077841`

```dockerfile
```

-	Layers:
	-	`sha256:74c2a3b55bbe8ee8de0fc32d1f7c014a8d6adea0a3a76eae2b8609b756d302b7`  
		Last Modified: Tue, 04 Feb 2025 04:48:10 GMT  
		Size: 4.2 MB (4173204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62bd9b848e9f353bdcbab8a94cd249871f38eadc446271e5b4762c61273d9cb0`  
		Last Modified: Tue, 04 Feb 2025 04:48:10 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:93ec9878f9a9b3a46a284876e63171a6210b3736bb972b0c5d4796cda5453087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298475567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44041d0af34fcdbd74b6937cdd4fcde2cdb43dc3f5c382aa55e45a4c5bab912`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aff5a21b61cbe7871bdf8da2a3702062b03bce04a51ee677a9cbf3ba03638d`  
		Last Modified: Fri, 31 Jan 2025 00:30:10 GMT  
		Size: 272.9 MB (272941607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c983ebc16ff345a95ca08a171a8493f927087037cecae8f2b9b2f389b9031858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3eaff357bd32cb0f544f34a2365fa44d90a99114ec62745ebf85b5b7d3d9a38`

```dockerfile
```

-	Layers:
	-	`sha256:b54ace4e0ccfeff5aac11fdb5578f073c0527c00cbdc6aeb18c81c95e404fe97`  
		Last Modified: Fri, 31 Jan 2025 00:30:04 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf064fad6a270bd0bf856ffdc2d3190c5e5053b91fff4f39cecbacbb63d812d4`  
		Last Modified: Fri, 31 Jan 2025 00:30:03 GMT  
		Size: 11.4 KB (11431 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8926d7a03ffae36f85f51efb4500e9597cad63234aa4ef9a76b4cd52c65f1e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342555234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a0cc20d49b5df9482865823bf0790b94fdb2914357f8e52c6cdd78eaba7cf3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a08aeb6d94617daae47a33f519e8e57f62a92c68f9d7e0ab641e1a0db2388`  
		Last Modified: Fri, 31 Jan 2025 00:31:48 GMT  
		Size: 313.8 MB (313810321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a7e7639473ff883d127d9da2ca0a48b97a7ef5dbad30604359a8fcf08d5de9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2daa0ffecf4f2d5331e07e093f1c8b315763ccb8f81df2603598631b896ffa`

```dockerfile
```

-	Layers:
	-	`sha256:7537be7790632603cef656f944c4e7ee941a3c5277ba066e9b3f47f977ded99f`  
		Last Modified: Fri, 31 Jan 2025 00:31:42 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77131571b2e3554fde3e602115f73b6ae828709aeda119480a7eb63a5d2b4dd9`  
		Last Modified: Fri, 31 Jan 2025 00:31:42 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b4cb84f8237773ab2a9d909067e793672803a6a60891045162d71a041ec1aa84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303168402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5776fc9e1a4653e5dba7bac53c11c61b037e78e61a18aa27373901d3f0b8ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6520efae94ff86fb3a7d20c8a870e4887e3ef3a03f2fdd5f0f9693734495ae12`  
		Last Modified: Tue, 04 Feb 2025 04:41:45 GMT  
		Size: 272.0 MB (271989527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:647a1f67479f3f4281e439e65b7548234a1c5c6b725e94de11996a76eed4ceaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b69c0ca583da0b23217c4526bda4a29c5bdb6be6aeb8fa0b525a3bda0b22831`

```dockerfile
```

-	Layers:
	-	`sha256:fa17f1add2389c6162bfc65f9f177539beb333228d0c6010c96cbefb1e0e6551`  
		Last Modified: Tue, 04 Feb 2025 04:41:39 GMT  
		Size: 4.2 MB (4163461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:366959658334956233be4dc44a27efdd98c6582055be5243f0fbf01f4cbcf624`  
		Last Modified: Tue, 04 Feb 2025 04:41:39 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84`

```console
$ docker pull rust@sha256:efe14eee1be3fd2462fe349b5948b0d1b179b421c9fb23acb20b579f59299daf
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
$ docker pull rust@sha256:d6ffb8c473118907af9c82d36eea7be73220fc86ed49e19e598368093d225124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543203405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14ab37a2b4852c1ba2d6d366516e227688c72b84d99c788d23988ea95769eca`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:2d1bc9b6ae46247afd5d8d1c031d2892c5210d0a1988a7aa81e62b333048122a`  
		Last Modified: Fri, 31 Jan 2025 00:27:31 GMT  
		Size: 194.9 MB (194939965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84` - unknown; unknown

```console
$ docker pull rust@sha256:5980cc5c19d12031aa61cd2a0b8253fcea0c09ab078d4c8641717c50fce74fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3f7e22174b2c99f85e932d83a5f1afb64561c5542b1cefdabc6f8c4d0faf83`

```dockerfile
```

-	Layers:
	-	`sha256:9026efa626bf98ab0377ccf91c1cdf594bd92d12b04d9e46626ac25f113530cc`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a222081ff21e7b344c50335e732fbfc73127895fe219859f41b6281d09ce103`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84` - linux; arm variant v7

```console
$ docker pull rust@sha256:ba90d94af74485087d3bedb060b98f7514cb5eb159319b368db620b6cd849961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.9 MB (531924462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aed138a8a06a33630f51e17d33da618d521427b01bc53c24176f47f28704ec9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18144c873f034f0c1ea60ca2893ae2a4f80c8767a3435cd3a36b6e1d253c8383`  
		Last Modified: Fri, 31 Jan 2025 00:32:29 GMT  
		Size: 230.9 MB (230859587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84` - unknown; unknown

```console
$ docker pull rust@sha256:24c0bc46c8fb57aec5662c1ba786ebe9f4dcdb1078d38b7db4a8fdb0f8b61e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7749caa656f2cd715044a80e1d6caf2868eb120d5ed8d7853f95f0fa2d0a514a`

```dockerfile
```

-	Layers:
	-	`sha256:114bdef2ab1fe37e9f58ba56ede93a4cb5c6cbc62c6b4e595ba2ccd263add81d`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e977e5b469a4014b4892a72fadd42ef688db4274c78636251af31387c9f5456`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14953a14bbcadb5cac3b9b623a2e19d2d59f9d59a8c93c2924a01352716f07c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597292805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3eb4d2ac479f7339700da0c5bd3d1d8a1c6a0ca4ab1a78f8f04ce47e9be1b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5996c7a64a4f64139ff9df6a590216c8143f5bb1f4c0f41874cf5336645c0`  
		Last Modified: Tue, 14 Jan 2025 17:08:21 GMT  
		Size: 202.7 MB (202716994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0cd049daad112fb47a9e2dc7f5d7ad6cfa0b6d3f7133ad7340085bf7f3521`  
		Last Modified: Fri, 31 Jan 2025 00:33:34 GMT  
		Size: 258.3 MB (258314257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84` - unknown; unknown

```console
$ docker pull rust@sha256:f37dae26ffeb1e51ff3afdb0315ac4652c790e0937e1e7a86f7d1fa88d173b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d6a21597c6c46be6bcf440046e131973460eb4120a67296a673fb28f007b98`

```dockerfile
```

-	Layers:
	-	`sha256:7f117a3f9871f3caee51a40e122472de613100e18832d07a9ff1a2ec321bb334`  
		Last Modified: Fri, 31 Jan 2025 00:33:27 GMT  
		Size: 15.5 MB (15502759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072319fe7967b8c2719006732f2548e51280f95233f294259687c942ab4f468e`  
		Last Modified: Fri, 31 Jan 2025 00:33:26 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84` - linux; 386

```console
$ docker pull rust@sha256:821a7a54c3f58639c91978c1237d7fa01e3a65e44238481fd9c770976cbd0e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562262370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a43c27946e528ead9015a0e00f8ded1f86bc93b6b7512ffc08a35b7539a462b`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:0b9d29e39242117927b00082eced1422486e6bf62ed48fd1d3f7d4eea941b259`  
		Last Modified: Fri, 31 Jan 2025 00:27:40 GMT  
		Size: 211.4 MB (211430918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84` - unknown; unknown

```console
$ docker pull rust@sha256:9ff4e7a8299cf2f331d79afc3fabfd39991b4beb4ea9c6237f06dd8826635db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08733e110be67a5cf02046201f755ec7f7ad7f00549188b91633be0e25c38d75`

```dockerfile
```

-	Layers:
	-	`sha256:8289295e1eb2e71548b9790670abc045a9972cb92a1c524c67f4d34c0a77c551`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd86c221361bfb6476de8f5a7a8137335371177cb4960b16f37f2d59d14173e`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84` - linux; ppc64le

```console
$ docker pull rust@sha256:c98ba917122d2941ed71ef0198e5dd450094a0ff2b61d5e4ad86c03b600f6f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.0 MB (617042336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db8805653b8f10d290d02effd1a5a9a5c19720cb0484d99386ff6611a43cbd9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc81baa5d59fc087ff9c3033ea4eb1bfa715f31d7e3ea65371060635cb593034`  
		Last Modified: Fri, 31 Jan 2025 00:28:41 GMT  
		Size: 254.8 MB (254802966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84` - unknown; unknown

```console
$ docker pull rust@sha256:37354536f1477490c54912769c533260bffb8fb982d4fceeaa620e43762b803a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d416eaf25b6818b699095b9b17260d6abffe59157e6bbd857eb9bf38d85073`

```dockerfile
```

-	Layers:
	-	`sha256:dd4b0559fbf93a64f693655a44f3f7e091038e0508cd2af9cb660159b9a853a2`  
		Last Modified: Fri, 31 Jan 2025 00:28:34 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f020d262064a1f8e6aa92c5030c699e1f215c9db15a0e712436ec6f070378770`  
		Last Modified: Fri, 31 Jan 2025 00:28:33 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84` - linux; s390x

```console
$ docker pull rust@sha256:d5960a1389fd5d0c8cd692f1e03bd49d89ea89599a0bd364b5fb3564795424f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599964843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f1fd155400b48e6e5b702ece9550a582f33605caf345c92e428b1fd248f9ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69de93bafada368b0e0985055a008874d24d736e83961f9b10d61d5a68bf51c3`  
		Last Modified: Fri, 31 Jan 2025 00:29:24 GMT  
		Size: 281.9 MB (281918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84` - unknown; unknown

```console
$ docker pull rust@sha256:188d0a76db21e823b3b424dc44f3d32f1f0d7a9fd734d505dd093a5c8ae04b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f291615bd9af8888d1d4c5a8b528d1ee3349885227ba2c2906f6219f646b808d`

```dockerfile
```

-	Layers:
	-	`sha256:3c1643fc4bdd3ec8efd59a842bce38261ffbcb07139b970d7db83df83ecf5baf`  
		Last Modified: Fri, 31 Jan 2025 00:29:20 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30c0064df1d0ffc289ce1d91423cf2048228fb82276833b98b9b1ba5bf4c4bb`  
		Last Modified: Fri, 31 Jan 2025 00:29:19 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-alpine`

```console
$ docker pull rust@sha256:18be086bb0b8b45a04e6cb1a55863852cfdf81d7abed75ea588acb7f4aa6748e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.84-alpine` - linux; amd64

```console
$ docker pull rust@sha256:919360958a6d487fa56f8d7cb102c897466991a98d195417ba975b28ac9432dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304581935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173cee671d366c16cd437003be211507d5afe676e262e62cb3ece9c22a3e3fa5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a339c2254caf5d4b71a878c1f61c73ed11450f099b1d317e8f3d3b0d2ba7d24`  
		Last Modified: Fri, 31 Jan 2025 00:27:25 GMT  
		Size: 61.6 MB (61564867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18309f435aeec843fd40d87f81417cf4fc4a669e1a697ae887b1b6364dad8f45`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 239.4 MB (239375353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:f0e1697f58f041b40e13dfe200b3d2878c4947f75532b671ef2ab01a87b76954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be83ec1ac744d4c41931a1101fceb07ee7b35d2b08aa747d9633e128e0bc578`

```dockerfile
```

-	Layers:
	-	`sha256:4a60dc9b2069fb8f008a6ebb143dc0d471c227fbbdd7e471bd573d8f3a2ae301`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab6210992562f33b8fb8a048172b9f29dd7c2f3b614e5a27ab729c42b9a7ad6`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:31bede8f9a632bc843e74af6757b35e56c7236086ba3992f51b3850fe864c922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307001444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afac4100d4af97dfac2eacb50ce61762f686680e5e8b577e83383d5effbcaf76`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548af7367683a8ad83d856786059e3f702f6e555d4c6fa75b5ae9ca66c6a853`  
		Last Modified: Fri, 31 Jan 2025 00:37:15 GMT  
		Size: 59.1 MB (59101145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2468ea22c5495d7b5836325b324ac275679df6c2762c658eb36b38e6107108`  
		Last Modified: Fri, 31 Jan 2025 00:37:19 GMT  
		Size: 243.9 MB (243907940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:e909bda5d8bab6cd1e6be99142887733fb6eb509306720ce2d566866768e2f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4954689616e540d48c85cb359d67157da8bd72d844188e2e7f0387049acd01`

```dockerfile
```

-	Layers:
	-	`sha256:513f93d9e310f3e8b4ddb854244e175c468d3e6c308bcc64ab9a83e594bdb444`  
		Last Modified: Fri, 31 Jan 2025 00:37:14 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed14993fe5fbca94a7caf5f00ed99b23d749da67a5db0083c4430891c910d80f`  
		Last Modified: Fri, 31 Jan 2025 00:37:13 GMT  
		Size: 12.1 KB (12083 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-alpine3.20`

```console
$ docker pull rust@sha256:5b65959f00c8fcc9bfabb76644c4eefa0b97f8af37040dd163592536dbd6e107
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.84-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:90846f2d591b7df8b6a24acf0b3b49b7c6505703190371f40d2f442498d2aa84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298316995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dfb378cd0fe965ee75d63fe3291757ea7876f5f7a4663e818d135f8ff2fbdc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77927bf1e96f21719646e6bae28029a1ae3f345fbe3909a6339189205890e1a`  
		Last Modified: Fri, 31 Jan 2025 00:27:17 GMT  
		Size: 55.3 MB (55315542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f429e09b0fa861e6542ecd21fefac35a3c2b405055fd9b74e31db3677f9db3`  
		Last Modified: Fri, 31 Jan 2025 00:27:20 GMT  
		Size: 239.4 MB (239375193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:03c2f4be77e68d8908fa4675b8cd24b056465943604991e23d40ae0961f1eca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1b5a1a42abcdcd793be2182d1682cd4e866f179bcebde2d0ddff81565cd141`

```dockerfile
```

-	Layers:
	-	`sha256:453fda6d733a61c5795fb7921bfbc21174ce9d1a30bfd83612d6e2e341b4028d`  
		Last Modified: Fri, 31 Jan 2025 00:27:16 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:571392ac9483c44b5395d2f6c12baae68eb19d840a081880a6c4f3194dc317ee`  
		Last Modified: Fri, 31 Jan 2025 00:27:16 GMT  
		Size: 10.7 KB (10713 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:59d7abf2b2cdc63cd4917924cb23135299f18b1aa5152baddab0fc0db9d851b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300949670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda6582639290a8a26ebbe011b767cf366d257472d3b950df2bbeb6c91b2cd3d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f023fbab63b00375fb771d16cd745c9a1ff513cda460f1e701e3b66e9ff86d`  
		Last Modified: Fri, 31 Jan 2025 00:36:11 GMT  
		Size: 53.0 MB (52951018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f22d4c62442d75cfd04ad26c9c5455e25bebf3384ec4e5be257e364d6aeb4`  
		Last Modified: Fri, 31 Jan 2025 00:36:15 GMT  
		Size: 243.9 MB (243907883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:c87b653694e961dff4fcbd925991fb2db9f8afbf3a05ace8351287adc3e8f29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ea31be4c87b9f661044c3b4d19d40df023745400966e4e2ddbebd135a3f62b`

```dockerfile
```

-	Layers:
	-	`sha256:2371f11175124cfba85292d79ffac38eea16a98d653da2f12fc5e9ba206099e4`  
		Last Modified: Fri, 31 Jan 2025 00:36:09 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10caafcae281ac20e919dcc1e71c9cb267ab5d223ab59cffe4fcf159262c0fa5`  
		Last Modified: Fri, 31 Jan 2025 00:36:09 GMT  
		Size: 10.8 KB (10832 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-alpine3.21`

```console
$ docker pull rust@sha256:18be086bb0b8b45a04e6cb1a55863852cfdf81d7abed75ea588acb7f4aa6748e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.84-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:919360958a6d487fa56f8d7cb102c897466991a98d195417ba975b28ac9432dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304581935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173cee671d366c16cd437003be211507d5afe676e262e62cb3ece9c22a3e3fa5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a339c2254caf5d4b71a878c1f61c73ed11450f099b1d317e8f3d3b0d2ba7d24`  
		Last Modified: Fri, 31 Jan 2025 00:27:25 GMT  
		Size: 61.6 MB (61564867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18309f435aeec843fd40d87f81417cf4fc4a669e1a697ae887b1b6364dad8f45`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 239.4 MB (239375353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:f0e1697f58f041b40e13dfe200b3d2878c4947f75532b671ef2ab01a87b76954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be83ec1ac744d4c41931a1101fceb07ee7b35d2b08aa747d9633e128e0bc578`

```dockerfile
```

-	Layers:
	-	`sha256:4a60dc9b2069fb8f008a6ebb143dc0d471c227fbbdd7e471bd573d8f3a2ae301`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab6210992562f33b8fb8a048172b9f29dd7c2f3b614e5a27ab729c42b9a7ad6`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:31bede8f9a632bc843e74af6757b35e56c7236086ba3992f51b3850fe864c922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307001444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afac4100d4af97dfac2eacb50ce61762f686680e5e8b577e83383d5effbcaf76`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548af7367683a8ad83d856786059e3f702f6e555d4c6fa75b5ae9ca66c6a853`  
		Last Modified: Fri, 31 Jan 2025 00:37:15 GMT  
		Size: 59.1 MB (59101145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2468ea22c5495d7b5836325b324ac275679df6c2762c658eb36b38e6107108`  
		Last Modified: Fri, 31 Jan 2025 00:37:19 GMT  
		Size: 243.9 MB (243907940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:e909bda5d8bab6cd1e6be99142887733fb6eb509306720ce2d566866768e2f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4954689616e540d48c85cb359d67157da8bd72d844188e2e7f0387049acd01`

```dockerfile
```

-	Layers:
	-	`sha256:513f93d9e310f3e8b4ddb854244e175c468d3e6c308bcc64ab9a83e594bdb444`  
		Last Modified: Fri, 31 Jan 2025 00:37:14 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed14993fe5fbca94a7caf5f00ed99b23d749da67a5db0083c4430891c910d80f`  
		Last Modified: Fri, 31 Jan 2025 00:37:13 GMT  
		Size: 12.1 KB (12083 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-bookworm`

```console
$ docker pull rust@sha256:efe14eee1be3fd2462fe349b5948b0d1b179b421c9fb23acb20b579f59299daf
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
$ docker pull rust@sha256:d6ffb8c473118907af9c82d36eea7be73220fc86ed49e19e598368093d225124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543203405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14ab37a2b4852c1ba2d6d366516e227688c72b84d99c788d23988ea95769eca`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:2d1bc9b6ae46247afd5d8d1c031d2892c5210d0a1988a7aa81e62b333048122a`  
		Last Modified: Fri, 31 Jan 2025 00:27:31 GMT  
		Size: 194.9 MB (194939965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5980cc5c19d12031aa61cd2a0b8253fcea0c09ab078d4c8641717c50fce74fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3f7e22174b2c99f85e932d83a5f1afb64561c5542b1cefdabc6f8c4d0faf83`

```dockerfile
```

-	Layers:
	-	`sha256:9026efa626bf98ab0377ccf91c1cdf594bd92d12b04d9e46626ac25f113530cc`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a222081ff21e7b344c50335e732fbfc73127895fe219859f41b6281d09ce103`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ba90d94af74485087d3bedb060b98f7514cb5eb159319b368db620b6cd849961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.9 MB (531924462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aed138a8a06a33630f51e17d33da618d521427b01bc53c24176f47f28704ec9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18144c873f034f0c1ea60ca2893ae2a4f80c8767a3435cd3a36b6e1d253c8383`  
		Last Modified: Fri, 31 Jan 2025 00:32:29 GMT  
		Size: 230.9 MB (230859587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:24c0bc46c8fb57aec5662c1ba786ebe9f4dcdb1078d38b7db4a8fdb0f8b61e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7749caa656f2cd715044a80e1d6caf2868eb120d5ed8d7853f95f0fa2d0a514a`

```dockerfile
```

-	Layers:
	-	`sha256:114bdef2ab1fe37e9f58ba56ede93a4cb5c6cbc62c6b4e595ba2ccd263add81d`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e977e5b469a4014b4892a72fadd42ef688db4274c78636251af31387c9f5456`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14953a14bbcadb5cac3b9b623a2e19d2d59f9d59a8c93c2924a01352716f07c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597292805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3eb4d2ac479f7339700da0c5bd3d1d8a1c6a0ca4ab1a78f8f04ce47e9be1b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5996c7a64a4f64139ff9df6a590216c8143f5bb1f4c0f41874cf5336645c0`  
		Last Modified: Tue, 14 Jan 2025 17:08:21 GMT  
		Size: 202.7 MB (202716994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0cd049daad112fb47a9e2dc7f5d7ad6cfa0b6d3f7133ad7340085bf7f3521`  
		Last Modified: Fri, 31 Jan 2025 00:33:34 GMT  
		Size: 258.3 MB (258314257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f37dae26ffeb1e51ff3afdb0315ac4652c790e0937e1e7a86f7d1fa88d173b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d6a21597c6c46be6bcf440046e131973460eb4120a67296a673fb28f007b98`

```dockerfile
```

-	Layers:
	-	`sha256:7f117a3f9871f3caee51a40e122472de613100e18832d07a9ff1a2ec321bb334`  
		Last Modified: Fri, 31 Jan 2025 00:33:27 GMT  
		Size: 15.5 MB (15502759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072319fe7967b8c2719006732f2548e51280f95233f294259687c942ab4f468e`  
		Last Modified: Fri, 31 Jan 2025 00:33:26 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bookworm` - linux; 386

```console
$ docker pull rust@sha256:821a7a54c3f58639c91978c1237d7fa01e3a65e44238481fd9c770976cbd0e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562262370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a43c27946e528ead9015a0e00f8ded1f86bc93b6b7512ffc08a35b7539a462b`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:0b9d29e39242117927b00082eced1422486e6bf62ed48fd1d3f7d4eea941b259`  
		Last Modified: Fri, 31 Jan 2025 00:27:40 GMT  
		Size: 211.4 MB (211430918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9ff4e7a8299cf2f331d79afc3fabfd39991b4beb4ea9c6237f06dd8826635db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08733e110be67a5cf02046201f755ec7f7ad7f00549188b91633be0e25c38d75`

```dockerfile
```

-	Layers:
	-	`sha256:8289295e1eb2e71548b9790670abc045a9972cb92a1c524c67f4d34c0a77c551`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd86c221361bfb6476de8f5a7a8137335371177cb4960b16f37f2d59d14173e`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:c98ba917122d2941ed71ef0198e5dd450094a0ff2b61d5e4ad86c03b600f6f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.0 MB (617042336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db8805653b8f10d290d02effd1a5a9a5c19720cb0484d99386ff6611a43cbd9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc81baa5d59fc087ff9c3033ea4eb1bfa715f31d7e3ea65371060635cb593034`  
		Last Modified: Fri, 31 Jan 2025 00:28:41 GMT  
		Size: 254.8 MB (254802966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:37354536f1477490c54912769c533260bffb8fb982d4fceeaa620e43762b803a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d416eaf25b6818b699095b9b17260d6abffe59157e6bbd857eb9bf38d85073`

```dockerfile
```

-	Layers:
	-	`sha256:dd4b0559fbf93a64f693655a44f3f7e091038e0508cd2af9cb660159b9a853a2`  
		Last Modified: Fri, 31 Jan 2025 00:28:34 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f020d262064a1f8e6aa92c5030c699e1f215c9db15a0e712436ec6f070378770`  
		Last Modified: Fri, 31 Jan 2025 00:28:33 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:d5960a1389fd5d0c8cd692f1e03bd49d89ea89599a0bd364b5fb3564795424f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599964843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f1fd155400b48e6e5b702ece9550a582f33605caf345c92e428b1fd248f9ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69de93bafada368b0e0985055a008874d24d736e83961f9b10d61d5a68bf51c3`  
		Last Modified: Fri, 31 Jan 2025 00:29:24 GMT  
		Size: 281.9 MB (281918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:188d0a76db21e823b3b424dc44f3d32f1f0d7a9fd734d505dd093a5c8ae04b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f291615bd9af8888d1d4c5a8b528d1ee3349885227ba2c2906f6219f646b808d`

```dockerfile
```

-	Layers:
	-	`sha256:3c1643fc4bdd3ec8efd59a842bce38261ffbcb07139b970d7db83df83ecf5baf`  
		Last Modified: Fri, 31 Jan 2025 00:29:20 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30c0064df1d0ffc289ce1d91423cf2048228fb82276833b98b9b1ba5bf4c4bb`  
		Last Modified: Fri, 31 Jan 2025 00:29:19 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-bullseye`

```console
$ docker pull rust@sha256:c4b1a57d45f13da4e88a581f5a2afec8fe88f5e34f1b42ad6b57263e007a10a8
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
$ docker pull rust@sha256:19e8e36b68de2035d1973180ade2170e4774b690f212e85426f8bb0f937bd235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.1 MB (516065029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9297b737a5f133ae508b1fd5c45759abd800a6f61fad6de049c5d1bf07090fe0`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:af5ffb44a6cd66d2c8993ddcc676a7100f7e86dc7808d0e11f1c5334d647a801`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 194.9 MB (194939976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:11213337bcc0a4d8064ffe13cb4f22bbcc652db9a58641d38f6019449cfad416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20ff9776cd1189493fc85a07efa4f9d8b3a87b85b1bb57986292831864c0237`

```dockerfile
```

-	Layers:
	-	`sha256:652e654fbafc7f8f0e97a8b25d486384e065ce80757ee0d4034910960ec1c289`  
		Last Modified: Fri, 31 Jan 2025 00:27:26 GMT  
		Size: 15.1 MB (15073395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410b01f8bbd6b016bb9db97e55638faaed4bf3dd7330dd758b5377d378bed762`  
		Last Modified: Fri, 31 Jan 2025 00:27:26 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:75471b41a597a6b1cfe6b24d628778f83796fb8575be44203e271c72a632e756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.7 MB (512724563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b15ecb05694d471bab508c576f8f71eb5867995620ba8f3759697e468f4975`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526075af1d9c0b728ff0e8888d46f79edd8fb9bacc975b1eb824b9bca2c06ee2`  
		Last Modified: Tue, 14 Jan 2025 21:56:34 GMT  
		Size: 167.5 MB (167525487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87cd816ef0e7cda0866402374e031c5b8eb8ea446c803396cee74b94e63493`  
		Last Modified: Fri, 31 Jan 2025 00:28:09 GMT  
		Size: 230.9 MB (230859536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f1c0976e1db9aafadb3c580636078c95f7985e70f131d271e03a322ac5d14abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e17bf1d055434cff4b3dbe7e53bb338f902850477ceb27958427bf7f6606a6`

```dockerfile
```

-	Layers:
	-	`sha256:cc2c8998bd0731810057c3b6047bab175c7016f12fd655d5aa1e755b96e2c50b`  
		Last Modified: Fri, 31 Jan 2025 00:27:59 GMT  
		Size: 14.9 MB (14874186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e376b8a774cb79f115c38a0a607c8d05c504e16ee1d897d8c21f0a6d7ecbeb48`  
		Last Modified: Fri, 31 Jan 2025 00:27:58 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:44dacf67a0f2d6e45cf20069750d1134fe117313e6b2dcb50425c28f6379f2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.9 MB (570937169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3120e33651377b4d4ddf5f4045cd3dde40315ba55c184b30928df0e844e35d08`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5936a36467e76a2d54993295f16ff38dd2c24f30cf89a1f83a922f2440b869`  
		Last Modified: Tue, 14 Jan 2025 17:09:53 GMT  
		Size: 190.0 MB (189980217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c97e0ab9340a3d9325e91e9d4f4b0681104e08ea083ef3914b9651b0a37ac`  
		Last Modified: Fri, 31 Jan 2025 00:30:23 GMT  
		Size: 258.3 MB (258314197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c1efe8411d5ddbd6ca7a84d0818c74e3bc1323fa49726ee6d4377e71186528f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7407ece2d925e5125f770ec29fbf720030c739a4ee20f89da0b24b6f1ca0ed29`

```dockerfile
```

-	Layers:
	-	`sha256:a791efb39aced3bfe7117d624ded6cb55bea86b2271b1b444ef7ecf2e35e65df`  
		Last Modified: Fri, 31 Jan 2025 00:30:18 GMT  
		Size: 15.1 MB (15075655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57cc19c32562fe05349d5c04dc3d40ca3fc4def915ca05fa9c1e4ccbc766ccd8`  
		Last Modified: Fri, 31 Jan 2025 00:30:17 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-bullseye` - linux; 386

```console
$ docker pull rust@sha256:ac7ebc2fbe359f9f7ad0c39453c80fd51a95e36f18a701d6df27390ca80c15ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.2 MB (538175938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4364c30642d359ebfdc54b274d0009f14e9cfbff1615478473abcd5291f960`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:ee8b3ada43c92b49d5a6758eda5322a4cfce6900a0c9996fb07cbc761dac8c45`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 211.4 MB (211430901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c1401012f1340b3d4d9623d00a4943177803bda897ca5651d637abc44a4c0812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2931a49ceab2dabcdff00bf99889b9353ec2ae41c99a5c3a85fa06101969c019`

```dockerfile
```

-	Layers:
	-	`sha256:b6652171b2db2c97f124d831aa76fe73fa658a589f1ac3fc9075a0a2dbcc608e`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 15.1 MB (15060422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1076671420ac46738dce103d762c400e7b9a9ed43be6137e7305585e331f26e`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-slim`

```console
$ docker pull rust@sha256:38ed9b34e7f3014723818a33871f4c244f3cf36c019d7341f6d9e5114cbdb596
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
$ docker pull rust@sha256:f1c6e953d9cfe4bd8eb4512a82647ef68965484714eb63d925b955458a357133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293935426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988feec34834b11f5aa7cb2677d196dbfb5bbfdfc4861134f6a01a22db095311`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1020b52149c924fa9f87f51bccb15dda19dec1c715e94e820355a3ea83202f7a`  
		Last Modified: Tue, 04 Feb 2025 04:48:25 GMT  
		Size: 265.7 MB (265723123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim` - unknown; unknown

```console
$ docker pull rust@sha256:79b36bc5042f238a4f3cffa1cbae990fec5b128951bd59298d1ccca3889bb1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c142e6c658521625b57a6e7bde7086b8625cea33c465791bf28cfe3745d8162`

```dockerfile
```

-	Layers:
	-	`sha256:8b1d943955598274f0f568ee76323314f21350045e470ad5a88fde875d1fccf6`  
		Last Modified: Tue, 04 Feb 2025 04:48:19 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8851e0f18f7ad661f6aed4f8fa89d47fcba726ffd8f76a32f5549dc3ea59379`  
		Last Modified: Tue, 04 Feb 2025 04:48:18 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:7895aa006490737a03b7cbe889f7ed3d8d5e28db4e894d3f79a5268aa0833dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302634826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f66ad885bf45b2d1a94ddc15323fd2d3928947e6973936ca6ca470f72c3bced`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e30f41f234176f2c16ce777337f908a1a5494227de2d5a8d969a9dd5c123a18`  
		Last Modified: Fri, 31 Jan 2025 00:34:31 GMT  
		Size: 278.7 MB (278720226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a423820d19893d117d3df4fc559613e7530115a5bc0d8cf3c33fd06c0a6e99c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ddadfc654a5a9aac9217f3fac5ff192f87119cad1733955a064f26eaa22138`

```dockerfile
```

-	Layers:
	-	`sha256:cfbe61d6317e4746f8563feb4f577d0e41544c362913a508ebf36365509cebaa`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2cc265269c6bdf19d72d395d5c8bdc5d5c6ad462c4fb8ebb54d824b01cf809a`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bd37300c571a784c02cc6511be16d9f94edb5dbd0e02095213552efb4f06ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352196288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd2883e9d25ded400d0c78e03183e85ceac746ce72f11b2087bdd25d5aafc12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2851b7f466da485d0e64c4855d4ab4b2db80c9c50770dd57605c43fd6c7cdfd`  
		Last Modified: Fri, 31 Jan 2025 00:35:06 GMT  
		Size: 324.2 MB (324155257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim` - unknown; unknown

```console
$ docker pull rust@sha256:7d5eefa74740563880088f83d8890ff19bad3c43632520ce3217dbc1c7e4df04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb4bb2ea3aa5392b9be7b81d22a58b0149ef8d1151ba02341049dd9f638b663`

```dockerfile
```

-	Layers:
	-	`sha256:bf9fcdda35b8ab6ece9a6cb4a44f12efe6de3c8dd5bfa18d73cd9d75d00f91a3`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ba4b082669b49e4b3c44cb5d514d34fb2702a836c5f399a486a5e78c5de35c`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim` - linux; 386

```console
$ docker pull rust@sha256:d482b4787a73d9059bf5cba29999c0001d86767bf1b59b0cd8234504f1752539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308216502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5909b6178c847cfba84bcfa51b9d15491e08801021fbe9ec32369dc9a5cc9d72`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a1bebc92f7ad633f86d3b27faacbf962b234bef49b7ac15d9fa204f831a39d`  
		Last Modified: Tue, 04 Feb 2025 04:41:58 GMT  
		Size: 279.0 MB (279029046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim` - unknown; unknown

```console
$ docker pull rust@sha256:9b55b0bc360983ef31668d29f0831fd2f4fa885b45aeeb2e233a3ddb2a1e124d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edd34bcca496a057e05b0f78d548c9eddf9b6a2708b44833ce347d301ce24a`

```dockerfile
```

-	Layers:
	-	`sha256:b1be01bfc9316ad7a57a60c173d15ea8d7a8530d42e3983624bc3d266eeeb8d8`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1188dc47ed580591433d16de41cd10911b115b3f2865d23a352e584d38d565e`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:0ae493364decaf0420efa4ddc9cbf1554fcf147142049c52ddef57f14ed17c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355608891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ab5118ccde6aebb13da6de1ca490126cd64d28370c877db5be19bccce4685a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc73567e881b68c8629ad1da7bb11b2b21a1caa40e61c21f214bd45f2ad0aec`  
		Last Modified: Fri, 31 Jan 2025 00:31:21 GMT  
		Size: 323.6 MB (323564044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim` - unknown; unknown

```console
$ docker pull rust@sha256:5f9bc075b26d9f54a8993714fef535de2c3e525df84032f34f4e2cf036e57b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4572aa06386fc1be43fc645e09df3c69c1e4255b9c0dc6b9c381e50fcad395a1`

```dockerfile
```

-	Layers:
	-	`sha256:951b107c9596b3fd7667ac8fd8883145e533afb92e754bcbb6cc37abf43ab36f`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6707e52cd8b0edb10aa0f3f29ac9c470549477008999a2c916b77361a8312a8d`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim` - linux; s390x

```console
$ docker pull rust@sha256:424e8413fb24c88edcaf1b689d990cc1b5d81b583332b5e8a4ebce0096a63407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358910439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a330311272f88ad3a31b23af36f93ea27b553e9eea634ea85e9ee60bf5ced46`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62668347d57abb66f2a0fab8774ffa016537604baf01fcee21fed7e2eb0f2f2d`  
		Last Modified: Fri, 31 Jan 2025 00:31:50 GMT  
		Size: 332.1 MB (332051701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim` - unknown; unknown

```console
$ docker pull rust@sha256:9fac2330e6da662b2713d2fde23bccfece116ba1bae59e81caaf18ec826d894c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e108fb041bf31c5ba2da80bed4e81113f09211cc58c1fa5ec8b48a6b532a90f`

```dockerfile
```

-	Layers:
	-	`sha256:a2a614ddb9300e6a218d557b5695ac3ab1776f904ceb81622d2cf584fcafad94`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb8842e3556a08959bdf1331108cdf9b1b1ab475e502e6cf2e1863ef156cad6f`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-slim-bookworm`

```console
$ docker pull rust@sha256:38ed9b34e7f3014723818a33871f4c244f3cf36c019d7341f6d9e5114cbdb596
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
$ docker pull rust@sha256:f1c6e953d9cfe4bd8eb4512a82647ef68965484714eb63d925b955458a357133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293935426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988feec34834b11f5aa7cb2677d196dbfb5bbfdfc4861134f6a01a22db095311`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1020b52149c924fa9f87f51bccb15dda19dec1c715e94e820355a3ea83202f7a`  
		Last Modified: Tue, 04 Feb 2025 04:48:25 GMT  
		Size: 265.7 MB (265723123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:79b36bc5042f238a4f3cffa1cbae990fec5b128951bd59298d1ccca3889bb1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c142e6c658521625b57a6e7bde7086b8625cea33c465791bf28cfe3745d8162`

```dockerfile
```

-	Layers:
	-	`sha256:8b1d943955598274f0f568ee76323314f21350045e470ad5a88fde875d1fccf6`  
		Last Modified: Tue, 04 Feb 2025 04:48:19 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8851e0f18f7ad661f6aed4f8fa89d47fcba726ffd8f76a32f5549dc3ea59379`  
		Last Modified: Tue, 04 Feb 2025 04:48:18 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:7895aa006490737a03b7cbe889f7ed3d8d5e28db4e894d3f79a5268aa0833dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302634826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f66ad885bf45b2d1a94ddc15323fd2d3928947e6973936ca6ca470f72c3bced`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e30f41f234176f2c16ce777337f908a1a5494227de2d5a8d969a9dd5c123a18`  
		Last Modified: Fri, 31 Jan 2025 00:34:31 GMT  
		Size: 278.7 MB (278720226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a423820d19893d117d3df4fc559613e7530115a5bc0d8cf3c33fd06c0a6e99c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ddadfc654a5a9aac9217f3fac5ff192f87119cad1733955a064f26eaa22138`

```dockerfile
```

-	Layers:
	-	`sha256:cfbe61d6317e4746f8563feb4f577d0e41544c362913a508ebf36365509cebaa`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2cc265269c6bdf19d72d395d5c8bdc5d5c6ad462c4fb8ebb54d824b01cf809a`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bd37300c571a784c02cc6511be16d9f94edb5dbd0e02095213552efb4f06ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352196288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd2883e9d25ded400d0c78e03183e85ceac746ce72f11b2087bdd25d5aafc12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2851b7f466da485d0e64c4855d4ab4b2db80c9c50770dd57605c43fd6c7cdfd`  
		Last Modified: Fri, 31 Jan 2025 00:35:06 GMT  
		Size: 324.2 MB (324155257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7d5eefa74740563880088f83d8890ff19bad3c43632520ce3217dbc1c7e4df04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb4bb2ea3aa5392b9be7b81d22a58b0149ef8d1151ba02341049dd9f638b663`

```dockerfile
```

-	Layers:
	-	`sha256:bf9fcdda35b8ab6ece9a6cb4a44f12efe6de3c8dd5bfa18d73cd9d75d00f91a3`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ba4b082669b49e4b3c44cb5d514d34fb2702a836c5f399a486a5e78c5de35c`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:d482b4787a73d9059bf5cba29999c0001d86767bf1b59b0cd8234504f1752539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308216502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5909b6178c847cfba84bcfa51b9d15491e08801021fbe9ec32369dc9a5cc9d72`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a1bebc92f7ad633f86d3b27faacbf962b234bef49b7ac15d9fa204f831a39d`  
		Last Modified: Tue, 04 Feb 2025 04:41:58 GMT  
		Size: 279.0 MB (279029046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9b55b0bc360983ef31668d29f0831fd2f4fa885b45aeeb2e233a3ddb2a1e124d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edd34bcca496a057e05b0f78d548c9eddf9b6a2708b44833ce347d301ce24a`

```dockerfile
```

-	Layers:
	-	`sha256:b1be01bfc9316ad7a57a60c173d15ea8d7a8530d42e3983624bc3d266eeeb8d8`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1188dc47ed580591433d16de41cd10911b115b3f2865d23a352e584d38d565e`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:0ae493364decaf0420efa4ddc9cbf1554fcf147142049c52ddef57f14ed17c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355608891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ab5118ccde6aebb13da6de1ca490126cd64d28370c877db5be19bccce4685a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc73567e881b68c8629ad1da7bb11b2b21a1caa40e61c21f214bd45f2ad0aec`  
		Last Modified: Fri, 31 Jan 2025 00:31:21 GMT  
		Size: 323.6 MB (323564044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5f9bc075b26d9f54a8993714fef535de2c3e525df84032f34f4e2cf036e57b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4572aa06386fc1be43fc645e09df3c69c1e4255b9c0dc6b9c381e50fcad395a1`

```dockerfile
```

-	Layers:
	-	`sha256:951b107c9596b3fd7667ac8fd8883145e533afb92e754bcbb6cc37abf43ab36f`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6707e52cd8b0edb10aa0f3f29ac9c470549477008999a2c916b77361a8312a8d`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:424e8413fb24c88edcaf1b689d990cc1b5d81b583332b5e8a4ebce0096a63407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358910439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a330311272f88ad3a31b23af36f93ea27b553e9eea634ea85e9ee60bf5ced46`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62668347d57abb66f2a0fab8774ffa016537604baf01fcee21fed7e2eb0f2f2d`  
		Last Modified: Fri, 31 Jan 2025 00:31:50 GMT  
		Size: 332.1 MB (332051701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9fac2330e6da662b2713d2fde23bccfece116ba1bae59e81caaf18ec826d894c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e108fb041bf31c5ba2da80bed4e81113f09211cc58c1fa5ec8b48a6b532a90f`

```dockerfile
```

-	Layers:
	-	`sha256:a2a614ddb9300e6a218d557b5695ac3ab1776f904ceb81622d2cf584fcafad94`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb8842e3556a08959bdf1331108cdf9b1b1ab475e502e6cf2e1863ef156cad6f`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84-slim-bullseye`

```console
$ docker pull rust@sha256:daeff596870266ef69308e65d01c8007ba61afb96a027eb80da16a4bf62e8c8e
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
$ docker pull rust@sha256:2b7845424e9284f1c26bd56fedd1483e6ca44e639ac4bf9141d9ad9c88b973ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285143356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee24319d37d90b47217bc8804087eb7618520d2d2998feaf3f673390cea2aa2f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38d52395664bc85f1e799519d83f7fac8d684946c51459db24960ed59d1aa7c`  
		Last Modified: Tue, 04 Feb 2025 04:48:14 GMT  
		Size: 254.9 MB (254890768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:40a8dc8468f83fe69082db8cc94d464f6986e7d5c4f3602a922cbfcc9e0db833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257a7ca891da9b98541d5a34a69aa9d1418765d9d43df2afbc37bbf746077841`

```dockerfile
```

-	Layers:
	-	`sha256:74c2a3b55bbe8ee8de0fc32d1f7c014a8d6adea0a3a76eae2b8609b756d302b7`  
		Last Modified: Tue, 04 Feb 2025 04:48:10 GMT  
		Size: 4.2 MB (4173204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62bd9b848e9f353bdcbab8a94cd249871f38eadc446271e5b4762c61273d9cb0`  
		Last Modified: Tue, 04 Feb 2025 04:48:10 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:93ec9878f9a9b3a46a284876e63171a6210b3736bb972b0c5d4796cda5453087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298475567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44041d0af34fcdbd74b6937cdd4fcde2cdb43dc3f5c382aa55e45a4c5bab912`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aff5a21b61cbe7871bdf8da2a3702062b03bce04a51ee677a9cbf3ba03638d`  
		Last Modified: Fri, 31 Jan 2025 00:30:10 GMT  
		Size: 272.9 MB (272941607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c983ebc16ff345a95ca08a171a8493f927087037cecae8f2b9b2f389b9031858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3eaff357bd32cb0f544f34a2365fa44d90a99114ec62745ebf85b5b7d3d9a38`

```dockerfile
```

-	Layers:
	-	`sha256:b54ace4e0ccfeff5aac11fdb5578f073c0527c00cbdc6aeb18c81c95e404fe97`  
		Last Modified: Fri, 31 Jan 2025 00:30:04 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf064fad6a270bd0bf856ffdc2d3190c5e5053b91fff4f39cecbacbb63d812d4`  
		Last Modified: Fri, 31 Jan 2025 00:30:03 GMT  
		Size: 11.4 KB (11431 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8926d7a03ffae36f85f51efb4500e9597cad63234aa4ef9a76b4cd52c65f1e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342555234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a0cc20d49b5df9482865823bf0790b94fdb2914357f8e52c6cdd78eaba7cf3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a08aeb6d94617daae47a33f519e8e57f62a92c68f9d7e0ab641e1a0db2388`  
		Last Modified: Fri, 31 Jan 2025 00:31:48 GMT  
		Size: 313.8 MB (313810321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a7e7639473ff883d127d9da2ca0a48b97a7ef5dbad30604359a8fcf08d5de9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2daa0ffecf4f2d5331e07e093f1c8b315763ccb8f81df2603598631b896ffa`

```dockerfile
```

-	Layers:
	-	`sha256:7537be7790632603cef656f944c4e7ee941a3c5277ba066e9b3f47f977ded99f`  
		Last Modified: Fri, 31 Jan 2025 00:31:42 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77131571b2e3554fde3e602115f73b6ae828709aeda119480a7eb63a5d2b4dd9`  
		Last Modified: Fri, 31 Jan 2025 00:31:42 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b4cb84f8237773ab2a9d909067e793672803a6a60891045162d71a041ec1aa84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303168402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5776fc9e1a4653e5dba7bac53c11c61b037e78e61a18aa27373901d3f0b8ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6520efae94ff86fb3a7d20c8a870e4887e3ef3a03f2fdd5f0f9693734495ae12`  
		Last Modified: Tue, 04 Feb 2025 04:41:45 GMT  
		Size: 272.0 MB (271989527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:647a1f67479f3f4281e439e65b7548234a1c5c6b725e94de11996a76eed4ceaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b69c0ca583da0b23217c4526bda4a29c5bdb6be6aeb8fa0b525a3bda0b22831`

```dockerfile
```

-	Layers:
	-	`sha256:fa17f1add2389c6162bfc65f9f177539beb333228d0c6010c96cbefb1e0e6551`  
		Last Modified: Tue, 04 Feb 2025 04:41:39 GMT  
		Size: 4.2 MB (4163461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:366959658334956233be4dc44a27efdd98c6582055be5243f0fbf01f4cbcf624`  
		Last Modified: Tue, 04 Feb 2025 04:41:39 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.1`

```console
$ docker pull rust@sha256:efe14eee1be3fd2462fe349b5948b0d1b179b421c9fb23acb20b579f59299daf
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

### `rust:1.84.1` - linux; amd64

```console
$ docker pull rust@sha256:d6ffb8c473118907af9c82d36eea7be73220fc86ed49e19e598368093d225124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543203405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14ab37a2b4852c1ba2d6d366516e227688c72b84d99c788d23988ea95769eca`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:2d1bc9b6ae46247afd5d8d1c031d2892c5210d0a1988a7aa81e62b333048122a`  
		Last Modified: Fri, 31 Jan 2025 00:27:31 GMT  
		Size: 194.9 MB (194939965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1` - unknown; unknown

```console
$ docker pull rust@sha256:5980cc5c19d12031aa61cd2a0b8253fcea0c09ab078d4c8641717c50fce74fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3f7e22174b2c99f85e932d83a5f1afb64561c5542b1cefdabc6f8c4d0faf83`

```dockerfile
```

-	Layers:
	-	`sha256:9026efa626bf98ab0377ccf91c1cdf594bd92d12b04d9e46626ac25f113530cc`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a222081ff21e7b344c50335e732fbfc73127895fe219859f41b6281d09ce103`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1` - linux; arm variant v7

```console
$ docker pull rust@sha256:ba90d94af74485087d3bedb060b98f7514cb5eb159319b368db620b6cd849961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.9 MB (531924462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aed138a8a06a33630f51e17d33da618d521427b01bc53c24176f47f28704ec9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18144c873f034f0c1ea60ca2893ae2a4f80c8767a3435cd3a36b6e1d253c8383`  
		Last Modified: Fri, 31 Jan 2025 00:32:29 GMT  
		Size: 230.9 MB (230859587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1` - unknown; unknown

```console
$ docker pull rust@sha256:24c0bc46c8fb57aec5662c1ba786ebe9f4dcdb1078d38b7db4a8fdb0f8b61e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7749caa656f2cd715044a80e1d6caf2868eb120d5ed8d7853f95f0fa2d0a514a`

```dockerfile
```

-	Layers:
	-	`sha256:114bdef2ab1fe37e9f58ba56ede93a4cb5c6cbc62c6b4e595ba2ccd263add81d`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e977e5b469a4014b4892a72fadd42ef688db4274c78636251af31387c9f5456`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14953a14bbcadb5cac3b9b623a2e19d2d59f9d59a8c93c2924a01352716f07c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597292805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3eb4d2ac479f7339700da0c5bd3d1d8a1c6a0ca4ab1a78f8f04ce47e9be1b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5996c7a64a4f64139ff9df6a590216c8143f5bb1f4c0f41874cf5336645c0`  
		Last Modified: Tue, 14 Jan 2025 17:08:21 GMT  
		Size: 202.7 MB (202716994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0cd049daad112fb47a9e2dc7f5d7ad6cfa0b6d3f7133ad7340085bf7f3521`  
		Last Modified: Fri, 31 Jan 2025 00:33:34 GMT  
		Size: 258.3 MB (258314257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1` - unknown; unknown

```console
$ docker pull rust@sha256:f37dae26ffeb1e51ff3afdb0315ac4652c790e0937e1e7a86f7d1fa88d173b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d6a21597c6c46be6bcf440046e131973460eb4120a67296a673fb28f007b98`

```dockerfile
```

-	Layers:
	-	`sha256:7f117a3f9871f3caee51a40e122472de613100e18832d07a9ff1a2ec321bb334`  
		Last Modified: Fri, 31 Jan 2025 00:33:27 GMT  
		Size: 15.5 MB (15502759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072319fe7967b8c2719006732f2548e51280f95233f294259687c942ab4f468e`  
		Last Modified: Fri, 31 Jan 2025 00:33:26 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1` - linux; 386

```console
$ docker pull rust@sha256:821a7a54c3f58639c91978c1237d7fa01e3a65e44238481fd9c770976cbd0e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562262370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a43c27946e528ead9015a0e00f8ded1f86bc93b6b7512ffc08a35b7539a462b`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:0b9d29e39242117927b00082eced1422486e6bf62ed48fd1d3f7d4eea941b259`  
		Last Modified: Fri, 31 Jan 2025 00:27:40 GMT  
		Size: 211.4 MB (211430918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1` - unknown; unknown

```console
$ docker pull rust@sha256:9ff4e7a8299cf2f331d79afc3fabfd39991b4beb4ea9c6237f06dd8826635db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08733e110be67a5cf02046201f755ec7f7ad7f00549188b91633be0e25c38d75`

```dockerfile
```

-	Layers:
	-	`sha256:8289295e1eb2e71548b9790670abc045a9972cb92a1c524c67f4d34c0a77c551`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd86c221361bfb6476de8f5a7a8137335371177cb4960b16f37f2d59d14173e`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1` - linux; ppc64le

```console
$ docker pull rust@sha256:c98ba917122d2941ed71ef0198e5dd450094a0ff2b61d5e4ad86c03b600f6f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.0 MB (617042336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db8805653b8f10d290d02effd1a5a9a5c19720cb0484d99386ff6611a43cbd9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc81baa5d59fc087ff9c3033ea4eb1bfa715f31d7e3ea65371060635cb593034`  
		Last Modified: Fri, 31 Jan 2025 00:28:41 GMT  
		Size: 254.8 MB (254802966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1` - unknown; unknown

```console
$ docker pull rust@sha256:37354536f1477490c54912769c533260bffb8fb982d4fceeaa620e43762b803a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d416eaf25b6818b699095b9b17260d6abffe59157e6bbd857eb9bf38d85073`

```dockerfile
```

-	Layers:
	-	`sha256:dd4b0559fbf93a64f693655a44f3f7e091038e0508cd2af9cb660159b9a853a2`  
		Last Modified: Fri, 31 Jan 2025 00:28:34 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f020d262064a1f8e6aa92c5030c699e1f215c9db15a0e712436ec6f070378770`  
		Last Modified: Fri, 31 Jan 2025 00:28:33 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1` - linux; s390x

```console
$ docker pull rust@sha256:d5960a1389fd5d0c8cd692f1e03bd49d89ea89599a0bd364b5fb3564795424f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599964843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f1fd155400b48e6e5b702ece9550a582f33605caf345c92e428b1fd248f9ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69de93bafada368b0e0985055a008874d24d736e83961f9b10d61d5a68bf51c3`  
		Last Modified: Fri, 31 Jan 2025 00:29:24 GMT  
		Size: 281.9 MB (281918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1` - unknown; unknown

```console
$ docker pull rust@sha256:188d0a76db21e823b3b424dc44f3d32f1f0d7a9fd734d505dd093a5c8ae04b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f291615bd9af8888d1d4c5a8b528d1ee3349885227ba2c2906f6219f646b808d`

```dockerfile
```

-	Layers:
	-	`sha256:3c1643fc4bdd3ec8efd59a842bce38261ffbcb07139b970d7db83df83ecf5baf`  
		Last Modified: Fri, 31 Jan 2025 00:29:20 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30c0064df1d0ffc289ce1d91423cf2048228fb82276833b98b9b1ba5bf4c4bb`  
		Last Modified: Fri, 31 Jan 2025 00:29:19 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.1-alpine`

```console
$ docker pull rust@sha256:18be086bb0b8b45a04e6cb1a55863852cfdf81d7abed75ea588acb7f4aa6748e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.84.1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:919360958a6d487fa56f8d7cb102c897466991a98d195417ba975b28ac9432dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304581935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173cee671d366c16cd437003be211507d5afe676e262e62cb3ece9c22a3e3fa5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a339c2254caf5d4b71a878c1f61c73ed11450f099b1d317e8f3d3b0d2ba7d24`  
		Last Modified: Fri, 31 Jan 2025 00:27:25 GMT  
		Size: 61.6 MB (61564867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18309f435aeec843fd40d87f81417cf4fc4a669e1a697ae887b1b6364dad8f45`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 239.4 MB (239375353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:f0e1697f58f041b40e13dfe200b3d2878c4947f75532b671ef2ab01a87b76954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be83ec1ac744d4c41931a1101fceb07ee7b35d2b08aa747d9633e128e0bc578`

```dockerfile
```

-	Layers:
	-	`sha256:4a60dc9b2069fb8f008a6ebb143dc0d471c227fbbdd7e471bd573d8f3a2ae301`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab6210992562f33b8fb8a048172b9f29dd7c2f3b614e5a27ab729c42b9a7ad6`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:31bede8f9a632bc843e74af6757b35e56c7236086ba3992f51b3850fe864c922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307001444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afac4100d4af97dfac2eacb50ce61762f686680e5e8b577e83383d5effbcaf76`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548af7367683a8ad83d856786059e3f702f6e555d4c6fa75b5ae9ca66c6a853`  
		Last Modified: Fri, 31 Jan 2025 00:37:15 GMT  
		Size: 59.1 MB (59101145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2468ea22c5495d7b5836325b324ac275679df6c2762c658eb36b38e6107108`  
		Last Modified: Fri, 31 Jan 2025 00:37:19 GMT  
		Size: 243.9 MB (243907940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:e909bda5d8bab6cd1e6be99142887733fb6eb509306720ce2d566866768e2f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4954689616e540d48c85cb359d67157da8bd72d844188e2e7f0387049acd01`

```dockerfile
```

-	Layers:
	-	`sha256:513f93d9e310f3e8b4ddb854244e175c468d3e6c308bcc64ab9a83e594bdb444`  
		Last Modified: Fri, 31 Jan 2025 00:37:14 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed14993fe5fbca94a7caf5f00ed99b23d749da67a5db0083c4430891c910d80f`  
		Last Modified: Fri, 31 Jan 2025 00:37:13 GMT  
		Size: 12.1 KB (12083 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.1-alpine3.20`

```console
$ docker pull rust@sha256:5b65959f00c8fcc9bfabb76644c4eefa0b97f8af37040dd163592536dbd6e107
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.84.1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:90846f2d591b7df8b6a24acf0b3b49b7c6505703190371f40d2f442498d2aa84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298316995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dfb378cd0fe965ee75d63fe3291757ea7876f5f7a4663e818d135f8ff2fbdc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77927bf1e96f21719646e6bae28029a1ae3f345fbe3909a6339189205890e1a`  
		Last Modified: Fri, 31 Jan 2025 00:27:17 GMT  
		Size: 55.3 MB (55315542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f429e09b0fa861e6542ecd21fefac35a3c2b405055fd9b74e31db3677f9db3`  
		Last Modified: Fri, 31 Jan 2025 00:27:20 GMT  
		Size: 239.4 MB (239375193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:03c2f4be77e68d8908fa4675b8cd24b056465943604991e23d40ae0961f1eca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1b5a1a42abcdcd793be2182d1682cd4e866f179bcebde2d0ddff81565cd141`

```dockerfile
```

-	Layers:
	-	`sha256:453fda6d733a61c5795fb7921bfbc21174ce9d1a30bfd83612d6e2e341b4028d`  
		Last Modified: Fri, 31 Jan 2025 00:27:16 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:571392ac9483c44b5395d2f6c12baae68eb19d840a081880a6c4f3194dc317ee`  
		Last Modified: Fri, 31 Jan 2025 00:27:16 GMT  
		Size: 10.7 KB (10713 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:59d7abf2b2cdc63cd4917924cb23135299f18b1aa5152baddab0fc0db9d851b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300949670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda6582639290a8a26ebbe011b767cf366d257472d3b950df2bbeb6c91b2cd3d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f023fbab63b00375fb771d16cd745c9a1ff513cda460f1e701e3b66e9ff86d`  
		Last Modified: Fri, 31 Jan 2025 00:36:11 GMT  
		Size: 53.0 MB (52951018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f22d4c62442d75cfd04ad26c9c5455e25bebf3384ec4e5be257e364d6aeb4`  
		Last Modified: Fri, 31 Jan 2025 00:36:15 GMT  
		Size: 243.9 MB (243907883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:c87b653694e961dff4fcbd925991fb2db9f8afbf3a05ace8351287adc3e8f29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ea31be4c87b9f661044c3b4d19d40df023745400966e4e2ddbebd135a3f62b`

```dockerfile
```

-	Layers:
	-	`sha256:2371f11175124cfba85292d79ffac38eea16a98d653da2f12fc5e9ba206099e4`  
		Last Modified: Fri, 31 Jan 2025 00:36:09 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10caafcae281ac20e919dcc1e71c9cb267ab5d223ab59cffe4fcf159262c0fa5`  
		Last Modified: Fri, 31 Jan 2025 00:36:09 GMT  
		Size: 10.8 KB (10832 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.1-alpine3.21`

```console
$ docker pull rust@sha256:18be086bb0b8b45a04e6cb1a55863852cfdf81d7abed75ea588acb7f4aa6748e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.84.1-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:919360958a6d487fa56f8d7cb102c897466991a98d195417ba975b28ac9432dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304581935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173cee671d366c16cd437003be211507d5afe676e262e62cb3ece9c22a3e3fa5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a339c2254caf5d4b71a878c1f61c73ed11450f099b1d317e8f3d3b0d2ba7d24`  
		Last Modified: Fri, 31 Jan 2025 00:27:25 GMT  
		Size: 61.6 MB (61564867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18309f435aeec843fd40d87f81417cf4fc4a669e1a697ae887b1b6364dad8f45`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 239.4 MB (239375353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:f0e1697f58f041b40e13dfe200b3d2878c4947f75532b671ef2ab01a87b76954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be83ec1ac744d4c41931a1101fceb07ee7b35d2b08aa747d9633e128e0bc578`

```dockerfile
```

-	Layers:
	-	`sha256:4a60dc9b2069fb8f008a6ebb143dc0d471c227fbbdd7e471bd573d8f3a2ae301`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab6210992562f33b8fb8a048172b9f29dd7c2f3b614e5a27ab729c42b9a7ad6`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:31bede8f9a632bc843e74af6757b35e56c7236086ba3992f51b3850fe864c922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307001444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afac4100d4af97dfac2eacb50ce61762f686680e5e8b577e83383d5effbcaf76`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548af7367683a8ad83d856786059e3f702f6e555d4c6fa75b5ae9ca66c6a853`  
		Last Modified: Fri, 31 Jan 2025 00:37:15 GMT  
		Size: 59.1 MB (59101145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2468ea22c5495d7b5836325b324ac275679df6c2762c658eb36b38e6107108`  
		Last Modified: Fri, 31 Jan 2025 00:37:19 GMT  
		Size: 243.9 MB (243907940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:e909bda5d8bab6cd1e6be99142887733fb6eb509306720ce2d566866768e2f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4954689616e540d48c85cb359d67157da8bd72d844188e2e7f0387049acd01`

```dockerfile
```

-	Layers:
	-	`sha256:513f93d9e310f3e8b4ddb854244e175c468d3e6c308bcc64ab9a83e594bdb444`  
		Last Modified: Fri, 31 Jan 2025 00:37:14 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed14993fe5fbca94a7caf5f00ed99b23d749da67a5db0083c4430891c910d80f`  
		Last Modified: Fri, 31 Jan 2025 00:37:13 GMT  
		Size: 12.1 KB (12083 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.1-bookworm`

```console
$ docker pull rust@sha256:efe14eee1be3fd2462fe349b5948b0d1b179b421c9fb23acb20b579f59299daf
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

### `rust:1.84.1-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:d6ffb8c473118907af9c82d36eea7be73220fc86ed49e19e598368093d225124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543203405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14ab37a2b4852c1ba2d6d366516e227688c72b84d99c788d23988ea95769eca`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:2d1bc9b6ae46247afd5d8d1c031d2892c5210d0a1988a7aa81e62b333048122a`  
		Last Modified: Fri, 31 Jan 2025 00:27:31 GMT  
		Size: 194.9 MB (194939965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5980cc5c19d12031aa61cd2a0b8253fcea0c09ab078d4c8641717c50fce74fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3f7e22174b2c99f85e932d83a5f1afb64561c5542b1cefdabc6f8c4d0faf83`

```dockerfile
```

-	Layers:
	-	`sha256:9026efa626bf98ab0377ccf91c1cdf594bd92d12b04d9e46626ac25f113530cc`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a222081ff21e7b344c50335e732fbfc73127895fe219859f41b6281d09ce103`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ba90d94af74485087d3bedb060b98f7514cb5eb159319b368db620b6cd849961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.9 MB (531924462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aed138a8a06a33630f51e17d33da618d521427b01bc53c24176f47f28704ec9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18144c873f034f0c1ea60ca2893ae2a4f80c8767a3435cd3a36b6e1d253c8383`  
		Last Modified: Fri, 31 Jan 2025 00:32:29 GMT  
		Size: 230.9 MB (230859587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:24c0bc46c8fb57aec5662c1ba786ebe9f4dcdb1078d38b7db4a8fdb0f8b61e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7749caa656f2cd715044a80e1d6caf2868eb120d5ed8d7853f95f0fa2d0a514a`

```dockerfile
```

-	Layers:
	-	`sha256:114bdef2ab1fe37e9f58ba56ede93a4cb5c6cbc62c6b4e595ba2ccd263add81d`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e977e5b469a4014b4892a72fadd42ef688db4274c78636251af31387c9f5456`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14953a14bbcadb5cac3b9b623a2e19d2d59f9d59a8c93c2924a01352716f07c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597292805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3eb4d2ac479f7339700da0c5bd3d1d8a1c6a0ca4ab1a78f8f04ce47e9be1b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5996c7a64a4f64139ff9df6a590216c8143f5bb1f4c0f41874cf5336645c0`  
		Last Modified: Tue, 14 Jan 2025 17:08:21 GMT  
		Size: 202.7 MB (202716994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0cd049daad112fb47a9e2dc7f5d7ad6cfa0b6d3f7133ad7340085bf7f3521`  
		Last Modified: Fri, 31 Jan 2025 00:33:34 GMT  
		Size: 258.3 MB (258314257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f37dae26ffeb1e51ff3afdb0315ac4652c790e0937e1e7a86f7d1fa88d173b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d6a21597c6c46be6bcf440046e131973460eb4120a67296a673fb28f007b98`

```dockerfile
```

-	Layers:
	-	`sha256:7f117a3f9871f3caee51a40e122472de613100e18832d07a9ff1a2ec321bb334`  
		Last Modified: Fri, 31 Jan 2025 00:33:27 GMT  
		Size: 15.5 MB (15502759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072319fe7967b8c2719006732f2548e51280f95233f294259687c942ab4f468e`  
		Last Modified: Fri, 31 Jan 2025 00:33:26 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:821a7a54c3f58639c91978c1237d7fa01e3a65e44238481fd9c770976cbd0e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562262370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a43c27946e528ead9015a0e00f8ded1f86bc93b6b7512ffc08a35b7539a462b`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:0b9d29e39242117927b00082eced1422486e6bf62ed48fd1d3f7d4eea941b259`  
		Last Modified: Fri, 31 Jan 2025 00:27:40 GMT  
		Size: 211.4 MB (211430918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9ff4e7a8299cf2f331d79afc3fabfd39991b4beb4ea9c6237f06dd8826635db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08733e110be67a5cf02046201f755ec7f7ad7f00549188b91633be0e25c38d75`

```dockerfile
```

-	Layers:
	-	`sha256:8289295e1eb2e71548b9790670abc045a9972cb92a1c524c67f4d34c0a77c551`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd86c221361bfb6476de8f5a7a8137335371177cb4960b16f37f2d59d14173e`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:c98ba917122d2941ed71ef0198e5dd450094a0ff2b61d5e4ad86c03b600f6f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.0 MB (617042336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db8805653b8f10d290d02effd1a5a9a5c19720cb0484d99386ff6611a43cbd9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc81baa5d59fc087ff9c3033ea4eb1bfa715f31d7e3ea65371060635cb593034`  
		Last Modified: Fri, 31 Jan 2025 00:28:41 GMT  
		Size: 254.8 MB (254802966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:37354536f1477490c54912769c533260bffb8fb982d4fceeaa620e43762b803a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d416eaf25b6818b699095b9b17260d6abffe59157e6bbd857eb9bf38d85073`

```dockerfile
```

-	Layers:
	-	`sha256:dd4b0559fbf93a64f693655a44f3f7e091038e0508cd2af9cb660159b9a853a2`  
		Last Modified: Fri, 31 Jan 2025 00:28:34 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f020d262064a1f8e6aa92c5030c699e1f215c9db15a0e712436ec6f070378770`  
		Last Modified: Fri, 31 Jan 2025 00:28:33 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:d5960a1389fd5d0c8cd692f1e03bd49d89ea89599a0bd364b5fb3564795424f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599964843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f1fd155400b48e6e5b702ece9550a582f33605caf345c92e428b1fd248f9ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69de93bafada368b0e0985055a008874d24d736e83961f9b10d61d5a68bf51c3`  
		Last Modified: Fri, 31 Jan 2025 00:29:24 GMT  
		Size: 281.9 MB (281918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:188d0a76db21e823b3b424dc44f3d32f1f0d7a9fd734d505dd093a5c8ae04b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f291615bd9af8888d1d4c5a8b528d1ee3349885227ba2c2906f6219f646b808d`

```dockerfile
```

-	Layers:
	-	`sha256:3c1643fc4bdd3ec8efd59a842bce38261ffbcb07139b970d7db83df83ecf5baf`  
		Last Modified: Fri, 31 Jan 2025 00:29:20 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30c0064df1d0ffc289ce1d91423cf2048228fb82276833b98b9b1ba5bf4c4bb`  
		Last Modified: Fri, 31 Jan 2025 00:29:19 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.1-bullseye`

```console
$ docker pull rust@sha256:c4b1a57d45f13da4e88a581f5a2afec8fe88f5e34f1b42ad6b57263e007a10a8
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

### `rust:1.84.1-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:19e8e36b68de2035d1973180ade2170e4774b690f212e85426f8bb0f937bd235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.1 MB (516065029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9297b737a5f133ae508b1fd5c45759abd800a6f61fad6de049c5d1bf07090fe0`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:af5ffb44a6cd66d2c8993ddcc676a7100f7e86dc7808d0e11f1c5334d647a801`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 194.9 MB (194939976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:11213337bcc0a4d8064ffe13cb4f22bbcc652db9a58641d38f6019449cfad416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20ff9776cd1189493fc85a07efa4f9d8b3a87b85b1bb57986292831864c0237`

```dockerfile
```

-	Layers:
	-	`sha256:652e654fbafc7f8f0e97a8b25d486384e065ce80757ee0d4034910960ec1c289`  
		Last Modified: Fri, 31 Jan 2025 00:27:26 GMT  
		Size: 15.1 MB (15073395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410b01f8bbd6b016bb9db97e55638faaed4bf3dd7330dd758b5377d378bed762`  
		Last Modified: Fri, 31 Jan 2025 00:27:26 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:75471b41a597a6b1cfe6b24d628778f83796fb8575be44203e271c72a632e756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.7 MB (512724563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b15ecb05694d471bab508c576f8f71eb5867995620ba8f3759697e468f4975`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526075af1d9c0b728ff0e8888d46f79edd8fb9bacc975b1eb824b9bca2c06ee2`  
		Last Modified: Tue, 14 Jan 2025 21:56:34 GMT  
		Size: 167.5 MB (167525487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87cd816ef0e7cda0866402374e031c5b8eb8ea446c803396cee74b94e63493`  
		Last Modified: Fri, 31 Jan 2025 00:28:09 GMT  
		Size: 230.9 MB (230859536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f1c0976e1db9aafadb3c580636078c95f7985e70f131d271e03a322ac5d14abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e17bf1d055434cff4b3dbe7e53bb338f902850477ceb27958427bf7f6606a6`

```dockerfile
```

-	Layers:
	-	`sha256:cc2c8998bd0731810057c3b6047bab175c7016f12fd655d5aa1e755b96e2c50b`  
		Last Modified: Fri, 31 Jan 2025 00:27:59 GMT  
		Size: 14.9 MB (14874186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e376b8a774cb79f115c38a0a607c8d05c504e16ee1d897d8c21f0a6d7ecbeb48`  
		Last Modified: Fri, 31 Jan 2025 00:27:58 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:44dacf67a0f2d6e45cf20069750d1134fe117313e6b2dcb50425c28f6379f2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.9 MB (570937169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3120e33651377b4d4ddf5f4045cd3dde40315ba55c184b30928df0e844e35d08`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5936a36467e76a2d54993295f16ff38dd2c24f30cf89a1f83a922f2440b869`  
		Last Modified: Tue, 14 Jan 2025 17:09:53 GMT  
		Size: 190.0 MB (189980217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c97e0ab9340a3d9325e91e9d4f4b0681104e08ea083ef3914b9651b0a37ac`  
		Last Modified: Fri, 31 Jan 2025 00:30:23 GMT  
		Size: 258.3 MB (258314197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c1efe8411d5ddbd6ca7a84d0818c74e3bc1323fa49726ee6d4377e71186528f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7407ece2d925e5125f770ec29fbf720030c739a4ee20f89da0b24b6f1ca0ed29`

```dockerfile
```

-	Layers:
	-	`sha256:a791efb39aced3bfe7117d624ded6cb55bea86b2271b1b444ef7ecf2e35e65df`  
		Last Modified: Fri, 31 Jan 2025 00:30:18 GMT  
		Size: 15.1 MB (15075655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57cc19c32562fe05349d5c04dc3d40ca3fc4def915ca05fa9c1e4ccbc766ccd8`  
		Last Modified: Fri, 31 Jan 2025 00:30:17 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:ac7ebc2fbe359f9f7ad0c39453c80fd51a95e36f18a701d6df27390ca80c15ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.2 MB (538175938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4364c30642d359ebfdc54b274d0009f14e9cfbff1615478473abcd5291f960`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:ee8b3ada43c92b49d5a6758eda5322a4cfce6900a0c9996fb07cbc761dac8c45`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 211.4 MB (211430901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c1401012f1340b3d4d9623d00a4943177803bda897ca5651d637abc44a4c0812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2931a49ceab2dabcdff00bf99889b9353ec2ae41c99a5c3a85fa06101969c019`

```dockerfile
```

-	Layers:
	-	`sha256:b6652171b2db2c97f124d831aa76fe73fa658a589f1ac3fc9075a0a2dbcc608e`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 15.1 MB (15060422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1076671420ac46738dce103d762c400e7b9a9ed43be6137e7305585e331f26e`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.1-slim`

```console
$ docker pull rust@sha256:38ed9b34e7f3014723818a33871f4c244f3cf36c019d7341f6d9e5114cbdb596
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

### `rust:1.84.1-slim` - linux; amd64

```console
$ docker pull rust@sha256:f1c6e953d9cfe4bd8eb4512a82647ef68965484714eb63d925b955458a357133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293935426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988feec34834b11f5aa7cb2677d196dbfb5bbfdfc4861134f6a01a22db095311`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1020b52149c924fa9f87f51bccb15dda19dec1c715e94e820355a3ea83202f7a`  
		Last Modified: Tue, 04 Feb 2025 04:48:25 GMT  
		Size: 265.7 MB (265723123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:79b36bc5042f238a4f3cffa1cbae990fec5b128951bd59298d1ccca3889bb1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c142e6c658521625b57a6e7bde7086b8625cea33c465791bf28cfe3745d8162`

```dockerfile
```

-	Layers:
	-	`sha256:8b1d943955598274f0f568ee76323314f21350045e470ad5a88fde875d1fccf6`  
		Last Modified: Tue, 04 Feb 2025 04:48:19 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8851e0f18f7ad661f6aed4f8fa89d47fcba726ffd8f76a32f5549dc3ea59379`  
		Last Modified: Tue, 04 Feb 2025 04:48:18 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:7895aa006490737a03b7cbe889f7ed3d8d5e28db4e894d3f79a5268aa0833dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302634826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f66ad885bf45b2d1a94ddc15323fd2d3928947e6973936ca6ca470f72c3bced`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e30f41f234176f2c16ce777337f908a1a5494227de2d5a8d969a9dd5c123a18`  
		Last Modified: Fri, 31 Jan 2025 00:34:31 GMT  
		Size: 278.7 MB (278720226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a423820d19893d117d3df4fc559613e7530115a5bc0d8cf3c33fd06c0a6e99c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ddadfc654a5a9aac9217f3fac5ff192f87119cad1733955a064f26eaa22138`

```dockerfile
```

-	Layers:
	-	`sha256:cfbe61d6317e4746f8563feb4f577d0e41544c362913a508ebf36365509cebaa`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2cc265269c6bdf19d72d395d5c8bdc5d5c6ad462c4fb8ebb54d824b01cf809a`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bd37300c571a784c02cc6511be16d9f94edb5dbd0e02095213552efb4f06ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352196288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd2883e9d25ded400d0c78e03183e85ceac746ce72f11b2087bdd25d5aafc12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2851b7f466da485d0e64c4855d4ab4b2db80c9c50770dd57605c43fd6c7cdfd`  
		Last Modified: Fri, 31 Jan 2025 00:35:06 GMT  
		Size: 324.2 MB (324155257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:7d5eefa74740563880088f83d8890ff19bad3c43632520ce3217dbc1c7e4df04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb4bb2ea3aa5392b9be7b81d22a58b0149ef8d1151ba02341049dd9f638b663`

```dockerfile
```

-	Layers:
	-	`sha256:bf9fcdda35b8ab6ece9a6cb4a44f12efe6de3c8dd5bfa18d73cd9d75d00f91a3`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ba4b082669b49e4b3c44cb5d514d34fb2702a836c5f399a486a5e78c5de35c`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-slim` - linux; 386

```console
$ docker pull rust@sha256:d482b4787a73d9059bf5cba29999c0001d86767bf1b59b0cd8234504f1752539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308216502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5909b6178c847cfba84bcfa51b9d15491e08801021fbe9ec32369dc9a5cc9d72`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a1bebc92f7ad633f86d3b27faacbf962b234bef49b7ac15d9fa204f831a39d`  
		Last Modified: Tue, 04 Feb 2025 04:41:58 GMT  
		Size: 279.0 MB (279029046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:9b55b0bc360983ef31668d29f0831fd2f4fa885b45aeeb2e233a3ddb2a1e124d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edd34bcca496a057e05b0f78d548c9eddf9b6a2708b44833ce347d301ce24a`

```dockerfile
```

-	Layers:
	-	`sha256:b1be01bfc9316ad7a57a60c173d15ea8d7a8530d42e3983624bc3d266eeeb8d8`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1188dc47ed580591433d16de41cd10911b115b3f2865d23a352e584d38d565e`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:0ae493364decaf0420efa4ddc9cbf1554fcf147142049c52ddef57f14ed17c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355608891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ab5118ccde6aebb13da6de1ca490126cd64d28370c877db5be19bccce4685a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc73567e881b68c8629ad1da7bb11b2b21a1caa40e61c21f214bd45f2ad0aec`  
		Last Modified: Fri, 31 Jan 2025 00:31:21 GMT  
		Size: 323.6 MB (323564044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:5f9bc075b26d9f54a8993714fef535de2c3e525df84032f34f4e2cf036e57b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4572aa06386fc1be43fc645e09df3c69c1e4255b9c0dc6b9c381e50fcad395a1`

```dockerfile
```

-	Layers:
	-	`sha256:951b107c9596b3fd7667ac8fd8883145e533afb92e754bcbb6cc37abf43ab36f`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6707e52cd8b0edb10aa0f3f29ac9c470549477008999a2c916b77361a8312a8d`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-slim` - linux; s390x

```console
$ docker pull rust@sha256:424e8413fb24c88edcaf1b689d990cc1b5d81b583332b5e8a4ebce0096a63407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358910439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a330311272f88ad3a31b23af36f93ea27b553e9eea634ea85e9ee60bf5ced46`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62668347d57abb66f2a0fab8774ffa016537604baf01fcee21fed7e2eb0f2f2d`  
		Last Modified: Fri, 31 Jan 2025 00:31:50 GMT  
		Size: 332.1 MB (332051701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:9fac2330e6da662b2713d2fde23bccfece116ba1bae59e81caaf18ec826d894c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e108fb041bf31c5ba2da80bed4e81113f09211cc58c1fa5ec8b48a6b532a90f`

```dockerfile
```

-	Layers:
	-	`sha256:a2a614ddb9300e6a218d557b5695ac3ab1776f904ceb81622d2cf584fcafad94`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb8842e3556a08959bdf1331108cdf9b1b1ab475e502e6cf2e1863ef156cad6f`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.1-slim-bookworm`

```console
$ docker pull rust@sha256:38ed9b34e7f3014723818a33871f4c244f3cf36c019d7341f6d9e5114cbdb596
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

### `rust:1.84.1-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:f1c6e953d9cfe4bd8eb4512a82647ef68965484714eb63d925b955458a357133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293935426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988feec34834b11f5aa7cb2677d196dbfb5bbfdfc4861134f6a01a22db095311`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1020b52149c924fa9f87f51bccb15dda19dec1c715e94e820355a3ea83202f7a`  
		Last Modified: Tue, 04 Feb 2025 04:48:25 GMT  
		Size: 265.7 MB (265723123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:79b36bc5042f238a4f3cffa1cbae990fec5b128951bd59298d1ccca3889bb1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c142e6c658521625b57a6e7bde7086b8625cea33c465791bf28cfe3745d8162`

```dockerfile
```

-	Layers:
	-	`sha256:8b1d943955598274f0f568ee76323314f21350045e470ad5a88fde875d1fccf6`  
		Last Modified: Tue, 04 Feb 2025 04:48:19 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8851e0f18f7ad661f6aed4f8fa89d47fcba726ffd8f76a32f5549dc3ea59379`  
		Last Modified: Tue, 04 Feb 2025 04:48:18 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:7895aa006490737a03b7cbe889f7ed3d8d5e28db4e894d3f79a5268aa0833dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302634826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f66ad885bf45b2d1a94ddc15323fd2d3928947e6973936ca6ca470f72c3bced`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e30f41f234176f2c16ce777337f908a1a5494227de2d5a8d969a9dd5c123a18`  
		Last Modified: Fri, 31 Jan 2025 00:34:31 GMT  
		Size: 278.7 MB (278720226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a423820d19893d117d3df4fc559613e7530115a5bc0d8cf3c33fd06c0a6e99c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ddadfc654a5a9aac9217f3fac5ff192f87119cad1733955a064f26eaa22138`

```dockerfile
```

-	Layers:
	-	`sha256:cfbe61d6317e4746f8563feb4f577d0e41544c362913a508ebf36365509cebaa`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2cc265269c6bdf19d72d395d5c8bdc5d5c6ad462c4fb8ebb54d824b01cf809a`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bd37300c571a784c02cc6511be16d9f94edb5dbd0e02095213552efb4f06ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352196288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd2883e9d25ded400d0c78e03183e85ceac746ce72f11b2087bdd25d5aafc12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2851b7f466da485d0e64c4855d4ab4b2db80c9c50770dd57605c43fd6c7cdfd`  
		Last Modified: Fri, 31 Jan 2025 00:35:06 GMT  
		Size: 324.2 MB (324155257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7d5eefa74740563880088f83d8890ff19bad3c43632520ce3217dbc1c7e4df04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb4bb2ea3aa5392b9be7b81d22a58b0149ef8d1151ba02341049dd9f638b663`

```dockerfile
```

-	Layers:
	-	`sha256:bf9fcdda35b8ab6ece9a6cb4a44f12efe6de3c8dd5bfa18d73cd9d75d00f91a3`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ba4b082669b49e4b3c44cb5d514d34fb2702a836c5f399a486a5e78c5de35c`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:d482b4787a73d9059bf5cba29999c0001d86767bf1b59b0cd8234504f1752539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308216502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5909b6178c847cfba84bcfa51b9d15491e08801021fbe9ec32369dc9a5cc9d72`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a1bebc92f7ad633f86d3b27faacbf962b234bef49b7ac15d9fa204f831a39d`  
		Last Modified: Tue, 04 Feb 2025 04:41:58 GMT  
		Size: 279.0 MB (279029046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9b55b0bc360983ef31668d29f0831fd2f4fa885b45aeeb2e233a3ddb2a1e124d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edd34bcca496a057e05b0f78d548c9eddf9b6a2708b44833ce347d301ce24a`

```dockerfile
```

-	Layers:
	-	`sha256:b1be01bfc9316ad7a57a60c173d15ea8d7a8530d42e3983624bc3d266eeeb8d8`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1188dc47ed580591433d16de41cd10911b115b3f2865d23a352e584d38d565e`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:0ae493364decaf0420efa4ddc9cbf1554fcf147142049c52ddef57f14ed17c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355608891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ab5118ccde6aebb13da6de1ca490126cd64d28370c877db5be19bccce4685a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc73567e881b68c8629ad1da7bb11b2b21a1caa40e61c21f214bd45f2ad0aec`  
		Last Modified: Fri, 31 Jan 2025 00:31:21 GMT  
		Size: 323.6 MB (323564044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5f9bc075b26d9f54a8993714fef535de2c3e525df84032f34f4e2cf036e57b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4572aa06386fc1be43fc645e09df3c69c1e4255b9c0dc6b9c381e50fcad395a1`

```dockerfile
```

-	Layers:
	-	`sha256:951b107c9596b3fd7667ac8fd8883145e533afb92e754bcbb6cc37abf43ab36f`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6707e52cd8b0edb10aa0f3f29ac9c470549477008999a2c916b77361a8312a8d`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:424e8413fb24c88edcaf1b689d990cc1b5d81b583332b5e8a4ebce0096a63407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358910439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a330311272f88ad3a31b23af36f93ea27b553e9eea634ea85e9ee60bf5ced46`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62668347d57abb66f2a0fab8774ffa016537604baf01fcee21fed7e2eb0f2f2d`  
		Last Modified: Fri, 31 Jan 2025 00:31:50 GMT  
		Size: 332.1 MB (332051701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9fac2330e6da662b2713d2fde23bccfece116ba1bae59e81caaf18ec826d894c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e108fb041bf31c5ba2da80bed4e81113f09211cc58c1fa5ec8b48a6b532a90f`

```dockerfile
```

-	Layers:
	-	`sha256:a2a614ddb9300e6a218d557b5695ac3ab1776f904ceb81622d2cf584fcafad94`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb8842e3556a08959bdf1331108cdf9b1b1ab475e502e6cf2e1863ef156cad6f`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.84.1-slim-bullseye`

```console
$ docker pull rust@sha256:daeff596870266ef69308e65d01c8007ba61afb96a027eb80da16a4bf62e8c8e
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

### `rust:1.84.1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:2b7845424e9284f1c26bd56fedd1483e6ca44e639ac4bf9141d9ad9c88b973ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285143356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee24319d37d90b47217bc8804087eb7618520d2d2998feaf3f673390cea2aa2f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38d52395664bc85f1e799519d83f7fac8d684946c51459db24960ed59d1aa7c`  
		Last Modified: Tue, 04 Feb 2025 04:48:14 GMT  
		Size: 254.9 MB (254890768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:40a8dc8468f83fe69082db8cc94d464f6986e7d5c4f3602a922cbfcc9e0db833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257a7ca891da9b98541d5a34a69aa9d1418765d9d43df2afbc37bbf746077841`

```dockerfile
```

-	Layers:
	-	`sha256:74c2a3b55bbe8ee8de0fc32d1f7c014a8d6adea0a3a76eae2b8609b756d302b7`  
		Last Modified: Tue, 04 Feb 2025 04:48:10 GMT  
		Size: 4.2 MB (4173204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62bd9b848e9f353bdcbab8a94cd249871f38eadc446271e5b4762c61273d9cb0`  
		Last Modified: Tue, 04 Feb 2025 04:48:10 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:93ec9878f9a9b3a46a284876e63171a6210b3736bb972b0c5d4796cda5453087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298475567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44041d0af34fcdbd74b6937cdd4fcde2cdb43dc3f5c382aa55e45a4c5bab912`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aff5a21b61cbe7871bdf8da2a3702062b03bce04a51ee677a9cbf3ba03638d`  
		Last Modified: Fri, 31 Jan 2025 00:30:10 GMT  
		Size: 272.9 MB (272941607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c983ebc16ff345a95ca08a171a8493f927087037cecae8f2b9b2f389b9031858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3eaff357bd32cb0f544f34a2365fa44d90a99114ec62745ebf85b5b7d3d9a38`

```dockerfile
```

-	Layers:
	-	`sha256:b54ace4e0ccfeff5aac11fdb5578f073c0527c00cbdc6aeb18c81c95e404fe97`  
		Last Modified: Fri, 31 Jan 2025 00:30:04 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf064fad6a270bd0bf856ffdc2d3190c5e5053b91fff4f39cecbacbb63d812d4`  
		Last Modified: Fri, 31 Jan 2025 00:30:03 GMT  
		Size: 11.4 KB (11431 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8926d7a03ffae36f85f51efb4500e9597cad63234aa4ef9a76b4cd52c65f1e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342555234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a0cc20d49b5df9482865823bf0790b94fdb2914357f8e52c6cdd78eaba7cf3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a08aeb6d94617daae47a33f519e8e57f62a92c68f9d7e0ab641e1a0db2388`  
		Last Modified: Fri, 31 Jan 2025 00:31:48 GMT  
		Size: 313.8 MB (313810321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a7e7639473ff883d127d9da2ca0a48b97a7ef5dbad30604359a8fcf08d5de9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2daa0ffecf4f2d5331e07e093f1c8b315763ccb8f81df2603598631b896ffa`

```dockerfile
```

-	Layers:
	-	`sha256:7537be7790632603cef656f944c4e7ee941a3c5277ba066e9b3f47f977ded99f`  
		Last Modified: Fri, 31 Jan 2025 00:31:42 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77131571b2e3554fde3e602115f73b6ae828709aeda119480a7eb63a5d2b4dd9`  
		Last Modified: Fri, 31 Jan 2025 00:31:42 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.84.1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b4cb84f8237773ab2a9d909067e793672803a6a60891045162d71a041ec1aa84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303168402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5776fc9e1a4653e5dba7bac53c11c61b037e78e61a18aa27373901d3f0b8ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6520efae94ff86fb3a7d20c8a870e4887e3ef3a03f2fdd5f0f9693734495ae12`  
		Last Modified: Tue, 04 Feb 2025 04:41:45 GMT  
		Size: 272.0 MB (271989527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.84.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:647a1f67479f3f4281e439e65b7548234a1c5c6b725e94de11996a76eed4ceaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b69c0ca583da0b23217c4526bda4a29c5bdb6be6aeb8fa0b525a3bda0b22831`

```dockerfile
```

-	Layers:
	-	`sha256:fa17f1add2389c6162bfc65f9f177539beb333228d0c6010c96cbefb1e0e6551`  
		Last Modified: Tue, 04 Feb 2025 04:41:39 GMT  
		Size: 4.2 MB (4163461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:366959658334956233be4dc44a27efdd98c6582055be5243f0fbf01f4cbcf624`  
		Last Modified: Tue, 04 Feb 2025 04:41:39 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:18be086bb0b8b45a04e6cb1a55863852cfdf81d7abed75ea588acb7f4aa6748e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:919360958a6d487fa56f8d7cb102c897466991a98d195417ba975b28ac9432dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304581935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173cee671d366c16cd437003be211507d5afe676e262e62cb3ece9c22a3e3fa5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a339c2254caf5d4b71a878c1f61c73ed11450f099b1d317e8f3d3b0d2ba7d24`  
		Last Modified: Fri, 31 Jan 2025 00:27:25 GMT  
		Size: 61.6 MB (61564867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18309f435aeec843fd40d87f81417cf4fc4a669e1a697ae887b1b6364dad8f45`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 239.4 MB (239375353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:f0e1697f58f041b40e13dfe200b3d2878c4947f75532b671ef2ab01a87b76954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be83ec1ac744d4c41931a1101fceb07ee7b35d2b08aa747d9633e128e0bc578`

```dockerfile
```

-	Layers:
	-	`sha256:4a60dc9b2069fb8f008a6ebb143dc0d471c227fbbdd7e471bd573d8f3a2ae301`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab6210992562f33b8fb8a048172b9f29dd7c2f3b614e5a27ab729c42b9a7ad6`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:31bede8f9a632bc843e74af6757b35e56c7236086ba3992f51b3850fe864c922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307001444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afac4100d4af97dfac2eacb50ce61762f686680e5e8b577e83383d5effbcaf76`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548af7367683a8ad83d856786059e3f702f6e555d4c6fa75b5ae9ca66c6a853`  
		Last Modified: Fri, 31 Jan 2025 00:37:15 GMT  
		Size: 59.1 MB (59101145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2468ea22c5495d7b5836325b324ac275679df6c2762c658eb36b38e6107108`  
		Last Modified: Fri, 31 Jan 2025 00:37:19 GMT  
		Size: 243.9 MB (243907940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:e909bda5d8bab6cd1e6be99142887733fb6eb509306720ce2d566866768e2f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4954689616e540d48c85cb359d67157da8bd72d844188e2e7f0387049acd01`

```dockerfile
```

-	Layers:
	-	`sha256:513f93d9e310f3e8b4ddb854244e175c468d3e6c308bcc64ab9a83e594bdb444`  
		Last Modified: Fri, 31 Jan 2025 00:37:14 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed14993fe5fbca94a7caf5f00ed99b23d749da67a5db0083c4430891c910d80f`  
		Last Modified: Fri, 31 Jan 2025 00:37:13 GMT  
		Size: 12.1 KB (12083 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.20`

```console
$ docker pull rust@sha256:5b65959f00c8fcc9bfabb76644c4eefa0b97f8af37040dd163592536dbd6e107
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:90846f2d591b7df8b6a24acf0b3b49b7c6505703190371f40d2f442498d2aa84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298316995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dfb378cd0fe965ee75d63fe3291757ea7876f5f7a4663e818d135f8ff2fbdc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77927bf1e96f21719646e6bae28029a1ae3f345fbe3909a6339189205890e1a`  
		Last Modified: Fri, 31 Jan 2025 00:27:17 GMT  
		Size: 55.3 MB (55315542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f429e09b0fa861e6542ecd21fefac35a3c2b405055fd9b74e31db3677f9db3`  
		Last Modified: Fri, 31 Jan 2025 00:27:20 GMT  
		Size: 239.4 MB (239375193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:03c2f4be77e68d8908fa4675b8cd24b056465943604991e23d40ae0961f1eca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1b5a1a42abcdcd793be2182d1682cd4e866f179bcebde2d0ddff81565cd141`

```dockerfile
```

-	Layers:
	-	`sha256:453fda6d733a61c5795fb7921bfbc21174ce9d1a30bfd83612d6e2e341b4028d`  
		Last Modified: Fri, 31 Jan 2025 00:27:16 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:571392ac9483c44b5395d2f6c12baae68eb19d840a081880a6c4f3194dc317ee`  
		Last Modified: Fri, 31 Jan 2025 00:27:16 GMT  
		Size: 10.7 KB (10713 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:59d7abf2b2cdc63cd4917924cb23135299f18b1aa5152baddab0fc0db9d851b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300949670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda6582639290a8a26ebbe011b767cf366d257472d3b950df2bbeb6c91b2cd3d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f023fbab63b00375fb771d16cd745c9a1ff513cda460f1e701e3b66e9ff86d`  
		Last Modified: Fri, 31 Jan 2025 00:36:11 GMT  
		Size: 53.0 MB (52951018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f22d4c62442d75cfd04ad26c9c5455e25bebf3384ec4e5be257e364d6aeb4`  
		Last Modified: Fri, 31 Jan 2025 00:36:15 GMT  
		Size: 243.9 MB (243907883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:c87b653694e961dff4fcbd925991fb2db9f8afbf3a05ace8351287adc3e8f29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ea31be4c87b9f661044c3b4d19d40df023745400966e4e2ddbebd135a3f62b`

```dockerfile
```

-	Layers:
	-	`sha256:2371f11175124cfba85292d79ffac38eea16a98d653da2f12fc5e9ba206099e4`  
		Last Modified: Fri, 31 Jan 2025 00:36:09 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10caafcae281ac20e919dcc1e71c9cb267ab5d223ab59cffe4fcf159262c0fa5`  
		Last Modified: Fri, 31 Jan 2025 00:36:09 GMT  
		Size: 10.8 KB (10832 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.21`

```console
$ docker pull rust@sha256:18be086bb0b8b45a04e6cb1a55863852cfdf81d7abed75ea588acb7f4aa6748e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:919360958a6d487fa56f8d7cb102c897466991a98d195417ba975b28ac9432dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304581935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173cee671d366c16cd437003be211507d5afe676e262e62cb3ece9c22a3e3fa5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a339c2254caf5d4b71a878c1f61c73ed11450f099b1d317e8f3d3b0d2ba7d24`  
		Last Modified: Fri, 31 Jan 2025 00:27:25 GMT  
		Size: 61.6 MB (61564867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18309f435aeec843fd40d87f81417cf4fc4a669e1a697ae887b1b6364dad8f45`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 239.4 MB (239375353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:f0e1697f58f041b40e13dfe200b3d2878c4947f75532b671ef2ab01a87b76954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be83ec1ac744d4c41931a1101fceb07ee7b35d2b08aa747d9633e128e0bc578`

```dockerfile
```

-	Layers:
	-	`sha256:4a60dc9b2069fb8f008a6ebb143dc0d471c227fbbdd7e471bd573d8f3a2ae301`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 781.3 KB (781339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab6210992562f33b8fb8a048172b9f29dd7c2f3b614e5a27ab729c42b9a7ad6`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:31bede8f9a632bc843e74af6757b35e56c7236086ba3992f51b3850fe864c922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307001444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afac4100d4af97dfac2eacb50ce61762f686680e5e8b577e83383d5effbcaf76`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b548af7367683a8ad83d856786059e3f702f6e555d4c6fa75b5ae9ca66c6a853`  
		Last Modified: Fri, 31 Jan 2025 00:37:15 GMT  
		Size: 59.1 MB (59101145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2468ea22c5495d7b5836325b324ac275679df6c2762c658eb36b38e6107108`  
		Last Modified: Fri, 31 Jan 2025 00:37:19 GMT  
		Size: 243.9 MB (243907940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:e909bda5d8bab6cd1e6be99142887733fb6eb509306720ce2d566866768e2f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4954689616e540d48c85cb359d67157da8bd72d844188e2e7f0387049acd01`

```dockerfile
```

-	Layers:
	-	`sha256:513f93d9e310f3e8b4ddb854244e175c468d3e6c308bcc64ab9a83e594bdb444`  
		Last Modified: Fri, 31 Jan 2025 00:37:14 GMT  
		Size: 860.9 KB (860925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed14993fe5fbca94a7caf5f00ed99b23d749da67a5db0083c4430891c910d80f`  
		Last Modified: Fri, 31 Jan 2025 00:37:13 GMT  
		Size: 12.1 KB (12083 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:efe14eee1be3fd2462fe349b5948b0d1b179b421c9fb23acb20b579f59299daf
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
$ docker pull rust@sha256:d6ffb8c473118907af9c82d36eea7be73220fc86ed49e19e598368093d225124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543203405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14ab37a2b4852c1ba2d6d366516e227688c72b84d99c788d23988ea95769eca`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:2d1bc9b6ae46247afd5d8d1c031d2892c5210d0a1988a7aa81e62b333048122a`  
		Last Modified: Fri, 31 Jan 2025 00:27:31 GMT  
		Size: 194.9 MB (194939965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5980cc5c19d12031aa61cd2a0b8253fcea0c09ab078d4c8641717c50fce74fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3f7e22174b2c99f85e932d83a5f1afb64561c5542b1cefdabc6f8c4d0faf83`

```dockerfile
```

-	Layers:
	-	`sha256:9026efa626bf98ab0377ccf91c1cdf594bd92d12b04d9e46626ac25f113530cc`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a222081ff21e7b344c50335e732fbfc73127895fe219859f41b6281d09ce103`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ba90d94af74485087d3bedb060b98f7514cb5eb159319b368db620b6cd849961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.9 MB (531924462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aed138a8a06a33630f51e17d33da618d521427b01bc53c24176f47f28704ec9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18144c873f034f0c1ea60ca2893ae2a4f80c8767a3435cd3a36b6e1d253c8383`  
		Last Modified: Fri, 31 Jan 2025 00:32:29 GMT  
		Size: 230.9 MB (230859587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:24c0bc46c8fb57aec5662c1ba786ebe9f4dcdb1078d38b7db4a8fdb0f8b61e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7749caa656f2cd715044a80e1d6caf2868eb120d5ed8d7853f95f0fa2d0a514a`

```dockerfile
```

-	Layers:
	-	`sha256:114bdef2ab1fe37e9f58ba56ede93a4cb5c6cbc62c6b4e595ba2ccd263add81d`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e977e5b469a4014b4892a72fadd42ef688db4274c78636251af31387c9f5456`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14953a14bbcadb5cac3b9b623a2e19d2d59f9d59a8c93c2924a01352716f07c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597292805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3eb4d2ac479f7339700da0c5bd3d1d8a1c6a0ca4ab1a78f8f04ce47e9be1b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5996c7a64a4f64139ff9df6a590216c8143f5bb1f4c0f41874cf5336645c0`  
		Last Modified: Tue, 14 Jan 2025 17:08:21 GMT  
		Size: 202.7 MB (202716994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0cd049daad112fb47a9e2dc7f5d7ad6cfa0b6d3f7133ad7340085bf7f3521`  
		Last Modified: Fri, 31 Jan 2025 00:33:34 GMT  
		Size: 258.3 MB (258314257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f37dae26ffeb1e51ff3afdb0315ac4652c790e0937e1e7a86f7d1fa88d173b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d6a21597c6c46be6bcf440046e131973460eb4120a67296a673fb28f007b98`

```dockerfile
```

-	Layers:
	-	`sha256:7f117a3f9871f3caee51a40e122472de613100e18832d07a9ff1a2ec321bb334`  
		Last Modified: Fri, 31 Jan 2025 00:33:27 GMT  
		Size: 15.5 MB (15502759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072319fe7967b8c2719006732f2548e51280f95233f294259687c942ab4f468e`  
		Last Modified: Fri, 31 Jan 2025 00:33:26 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:821a7a54c3f58639c91978c1237d7fa01e3a65e44238481fd9c770976cbd0e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562262370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a43c27946e528ead9015a0e00f8ded1f86bc93b6b7512ffc08a35b7539a462b`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:0b9d29e39242117927b00082eced1422486e6bf62ed48fd1d3f7d4eea941b259`  
		Last Modified: Fri, 31 Jan 2025 00:27:40 GMT  
		Size: 211.4 MB (211430918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9ff4e7a8299cf2f331d79afc3fabfd39991b4beb4ea9c6237f06dd8826635db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08733e110be67a5cf02046201f755ec7f7ad7f00549188b91633be0e25c38d75`

```dockerfile
```

-	Layers:
	-	`sha256:8289295e1eb2e71548b9790670abc045a9972cb92a1c524c67f4d34c0a77c551`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd86c221361bfb6476de8f5a7a8137335371177cb4960b16f37f2d59d14173e`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:c98ba917122d2941ed71ef0198e5dd450094a0ff2b61d5e4ad86c03b600f6f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.0 MB (617042336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db8805653b8f10d290d02effd1a5a9a5c19720cb0484d99386ff6611a43cbd9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc81baa5d59fc087ff9c3033ea4eb1bfa715f31d7e3ea65371060635cb593034`  
		Last Modified: Fri, 31 Jan 2025 00:28:41 GMT  
		Size: 254.8 MB (254802966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:37354536f1477490c54912769c533260bffb8fb982d4fceeaa620e43762b803a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d416eaf25b6818b699095b9b17260d6abffe59157e6bbd857eb9bf38d85073`

```dockerfile
```

-	Layers:
	-	`sha256:dd4b0559fbf93a64f693655a44f3f7e091038e0508cd2af9cb660159b9a853a2`  
		Last Modified: Fri, 31 Jan 2025 00:28:34 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f020d262064a1f8e6aa92c5030c699e1f215c9db15a0e712436ec6f070378770`  
		Last Modified: Fri, 31 Jan 2025 00:28:33 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:d5960a1389fd5d0c8cd692f1e03bd49d89ea89599a0bd364b5fb3564795424f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599964843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f1fd155400b48e6e5b702ece9550a582f33605caf345c92e428b1fd248f9ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69de93bafada368b0e0985055a008874d24d736e83961f9b10d61d5a68bf51c3`  
		Last Modified: Fri, 31 Jan 2025 00:29:24 GMT  
		Size: 281.9 MB (281918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:188d0a76db21e823b3b424dc44f3d32f1f0d7a9fd734d505dd093a5c8ae04b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f291615bd9af8888d1d4c5a8b528d1ee3349885227ba2c2906f6219f646b808d`

```dockerfile
```

-	Layers:
	-	`sha256:3c1643fc4bdd3ec8efd59a842bce38261ffbcb07139b970d7db83df83ecf5baf`  
		Last Modified: Fri, 31 Jan 2025 00:29:20 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30c0064df1d0ffc289ce1d91423cf2048228fb82276833b98b9b1ba5bf4c4bb`  
		Last Modified: Fri, 31 Jan 2025 00:29:19 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:c4b1a57d45f13da4e88a581f5a2afec8fe88f5e34f1b42ad6b57263e007a10a8
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
$ docker pull rust@sha256:19e8e36b68de2035d1973180ade2170e4774b690f212e85426f8bb0f937bd235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.1 MB (516065029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9297b737a5f133ae508b1fd5c45759abd800a6f61fad6de049c5d1bf07090fe0`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:af5ffb44a6cd66d2c8993ddcc676a7100f7e86dc7808d0e11f1c5334d647a801`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 194.9 MB (194939976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:11213337bcc0a4d8064ffe13cb4f22bbcc652db9a58641d38f6019449cfad416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20ff9776cd1189493fc85a07efa4f9d8b3a87b85b1bb57986292831864c0237`

```dockerfile
```

-	Layers:
	-	`sha256:652e654fbafc7f8f0e97a8b25d486384e065ce80757ee0d4034910960ec1c289`  
		Last Modified: Fri, 31 Jan 2025 00:27:26 GMT  
		Size: 15.1 MB (15073395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410b01f8bbd6b016bb9db97e55638faaed4bf3dd7330dd758b5377d378bed762`  
		Last Modified: Fri, 31 Jan 2025 00:27:26 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:75471b41a597a6b1cfe6b24d628778f83796fb8575be44203e271c72a632e756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.7 MB (512724563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b15ecb05694d471bab508c576f8f71eb5867995620ba8f3759697e468f4975`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526075af1d9c0b728ff0e8888d46f79edd8fb9bacc975b1eb824b9bca2c06ee2`  
		Last Modified: Tue, 14 Jan 2025 21:56:34 GMT  
		Size: 167.5 MB (167525487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87cd816ef0e7cda0866402374e031c5b8eb8ea446c803396cee74b94e63493`  
		Last Modified: Fri, 31 Jan 2025 00:28:09 GMT  
		Size: 230.9 MB (230859536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f1c0976e1db9aafadb3c580636078c95f7985e70f131d271e03a322ac5d14abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e17bf1d055434cff4b3dbe7e53bb338f902850477ceb27958427bf7f6606a6`

```dockerfile
```

-	Layers:
	-	`sha256:cc2c8998bd0731810057c3b6047bab175c7016f12fd655d5aa1e755b96e2c50b`  
		Last Modified: Fri, 31 Jan 2025 00:27:59 GMT  
		Size: 14.9 MB (14874186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e376b8a774cb79f115c38a0a607c8d05c504e16ee1d897d8c21f0a6d7ecbeb48`  
		Last Modified: Fri, 31 Jan 2025 00:27:58 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:44dacf67a0f2d6e45cf20069750d1134fe117313e6b2dcb50425c28f6379f2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.9 MB (570937169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3120e33651377b4d4ddf5f4045cd3dde40315ba55c184b30928df0e844e35d08`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5936a36467e76a2d54993295f16ff38dd2c24f30cf89a1f83a922f2440b869`  
		Last Modified: Tue, 14 Jan 2025 17:09:53 GMT  
		Size: 190.0 MB (189980217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c97e0ab9340a3d9325e91e9d4f4b0681104e08ea083ef3914b9651b0a37ac`  
		Last Modified: Fri, 31 Jan 2025 00:30:23 GMT  
		Size: 258.3 MB (258314197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c1efe8411d5ddbd6ca7a84d0818c74e3bc1323fa49726ee6d4377e71186528f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7407ece2d925e5125f770ec29fbf720030c739a4ee20f89da0b24b6f1ca0ed29`

```dockerfile
```

-	Layers:
	-	`sha256:a791efb39aced3bfe7117d624ded6cb55bea86b2271b1b444ef7ecf2e35e65df`  
		Last Modified: Fri, 31 Jan 2025 00:30:18 GMT  
		Size: 15.1 MB (15075655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57cc19c32562fe05349d5c04dc3d40ca3fc4def915ca05fa9c1e4ccbc766ccd8`  
		Last Modified: Fri, 31 Jan 2025 00:30:17 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:ac7ebc2fbe359f9f7ad0c39453c80fd51a95e36f18a701d6df27390ca80c15ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.2 MB (538175938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4364c30642d359ebfdc54b274d0009f14e9cfbff1615478473abcd5291f960`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:ee8b3ada43c92b49d5a6758eda5322a4cfce6900a0c9996fb07cbc761dac8c45`  
		Last Modified: Fri, 31 Jan 2025 00:27:29 GMT  
		Size: 211.4 MB (211430901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c1401012f1340b3d4d9623d00a4943177803bda897ca5651d637abc44a4c0812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2931a49ceab2dabcdff00bf99889b9353ec2ae41c99a5c3a85fa06101969c019`

```dockerfile
```

-	Layers:
	-	`sha256:b6652171b2db2c97f124d831aa76fe73fa658a589f1ac3fc9075a0a2dbcc608e`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 15.1 MB (15060422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1076671420ac46738dce103d762c400e7b9a9ed43be6137e7305585e331f26e`  
		Last Modified: Fri, 31 Jan 2025 00:27:23 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:efe14eee1be3fd2462fe349b5948b0d1b179b421c9fb23acb20b579f59299daf
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
$ docker pull rust@sha256:d6ffb8c473118907af9c82d36eea7be73220fc86ed49e19e598368093d225124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543203405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14ab37a2b4852c1ba2d6d366516e227688c72b84d99c788d23988ea95769eca`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:2d1bc9b6ae46247afd5d8d1c031d2892c5210d0a1988a7aa81e62b333048122a`  
		Last Modified: Fri, 31 Jan 2025 00:27:31 GMT  
		Size: 194.9 MB (194939965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:5980cc5c19d12031aa61cd2a0b8253fcea0c09ab078d4c8641717c50fce74fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3f7e22174b2c99f85e932d83a5f1afb64561c5542b1cefdabc6f8c4d0faf83`

```dockerfile
```

-	Layers:
	-	`sha256:9026efa626bf98ab0377ccf91c1cdf594bd92d12b04d9e46626ac25f113530cc`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 15.5 MB (15474184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a222081ff21e7b344c50335e732fbfc73127895fe219859f41b6281d09ce103`  
		Last Modified: Fri, 31 Jan 2025 00:27:28 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:ba90d94af74485087d3bedb060b98f7514cb5eb159319b368db620b6cd849961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.9 MB (531924462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aed138a8a06a33630f51e17d33da618d521427b01bc53c24176f47f28704ec9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18144c873f034f0c1ea60ca2893ae2a4f80c8767a3435cd3a36b6e1d253c8383`  
		Last Modified: Fri, 31 Jan 2025 00:32:29 GMT  
		Size: 230.9 MB (230859587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:24c0bc46c8fb57aec5662c1ba786ebe9f4dcdb1078d38b7db4a8fdb0f8b61e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7749caa656f2cd715044a80e1d6caf2868eb120d5ed8d7853f95f0fa2d0a514a`

```dockerfile
```

-	Layers:
	-	`sha256:114bdef2ab1fe37e9f58ba56ede93a4cb5c6cbc62c6b4e595ba2ccd263add81d`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 15.3 MB (15278626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e977e5b469a4014b4892a72fadd42ef688db4274c78636251af31387c9f5456`  
		Last Modified: Fri, 31 Jan 2025 00:32:23 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:14953a14bbcadb5cac3b9b623a2e19d2d59f9d59a8c93c2924a01352716f07c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597292805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3eb4d2ac479f7339700da0c5bd3d1d8a1c6a0ca4ab1a78f8f04ce47e9be1b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5996c7a64a4f64139ff9df6a590216c8143f5bb1f4c0f41874cf5336645c0`  
		Last Modified: Tue, 14 Jan 2025 17:08:21 GMT  
		Size: 202.7 MB (202716994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0cd049daad112fb47a9e2dc7f5d7ad6cfa0b6d3f7133ad7340085bf7f3521`  
		Last Modified: Fri, 31 Jan 2025 00:33:34 GMT  
		Size: 258.3 MB (258314257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:f37dae26ffeb1e51ff3afdb0315ac4652c790e0937e1e7a86f7d1fa88d173b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15516050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d6a21597c6c46be6bcf440046e131973460eb4120a67296a673fb28f007b98`

```dockerfile
```

-	Layers:
	-	`sha256:7f117a3f9871f3caee51a40e122472de613100e18832d07a9ff1a2ec321bb334`  
		Last Modified: Fri, 31 Jan 2025 00:33:27 GMT  
		Size: 15.5 MB (15502759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072319fe7967b8c2719006732f2548e51280f95233f294259687c942ab4f468e`  
		Last Modified: Fri, 31 Jan 2025 00:33:26 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:821a7a54c3f58639c91978c1237d7fa01e3a65e44238481fd9c770976cbd0e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.3 MB (562262370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a43c27946e528ead9015a0e00f8ded1f86bc93b6b7512ffc08a35b7539a462b`
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
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
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
	-	`sha256:0b9d29e39242117927b00082eced1422486e6bf62ed48fd1d3f7d4eea941b259`  
		Last Modified: Fri, 31 Jan 2025 00:27:40 GMT  
		Size: 211.4 MB (211430918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:9ff4e7a8299cf2f331d79afc3fabfd39991b4beb4ea9c6237f06dd8826635db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08733e110be67a5cf02046201f755ec7f7ad7f00549188b91633be0e25c38d75`

```dockerfile
```

-	Layers:
	-	`sha256:8289295e1eb2e71548b9790670abc045a9972cb92a1c524c67f4d34c0a77c551`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 15.5 MB (15451446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd86c221361bfb6476de8f5a7a8137335371177cb4960b16f37f2d59d14173e`  
		Last Modified: Fri, 31 Jan 2025 00:27:35 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:c98ba917122d2941ed71ef0198e5dd450094a0ff2b61d5e4ad86c03b600f6f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.0 MB (617042336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db8805653b8f10d290d02effd1a5a9a5c19720cb0484d99386ff6611a43cbd9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc81baa5d59fc087ff9c3033ea4eb1bfa715f31d7e3ea65371060635cb593034`  
		Last Modified: Fri, 31 Jan 2025 00:28:41 GMT  
		Size: 254.8 MB (254802966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:37354536f1477490c54912769c533260bffb8fb982d4fceeaa620e43762b803a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d416eaf25b6818b699095b9b17260d6abffe59157e6bbd857eb9bf38d85073`

```dockerfile
```

-	Layers:
	-	`sha256:dd4b0559fbf93a64f693655a44f3f7e091038e0508cd2af9cb660159b9a853a2`  
		Last Modified: Fri, 31 Jan 2025 00:28:34 GMT  
		Size: 15.4 MB (15449290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f020d262064a1f8e6aa92c5030c699e1f215c9db15a0e712436ec6f070378770`  
		Last Modified: Fri, 31 Jan 2025 00:28:33 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:d5960a1389fd5d0c8cd692f1e03bd49d89ea89599a0bd364b5fb3564795424f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599964843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f1fd155400b48e6e5b702ece9550a582f33605caf345c92e428b1fd248f9ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69de93bafada368b0e0985055a008874d24d736e83961f9b10d61d5a68bf51c3`  
		Last Modified: Fri, 31 Jan 2025 00:29:24 GMT  
		Size: 281.9 MB (281918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:188d0a76db21e823b3b424dc44f3d32f1f0d7a9fd734d505dd093a5c8ae04b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f291615bd9af8888d1d4c5a8b528d1ee3349885227ba2c2906f6219f646b808d`

```dockerfile
```

-	Layers:
	-	`sha256:3c1643fc4bdd3ec8efd59a842bce38261ffbcb07139b970d7db83df83ecf5baf`  
		Last Modified: Fri, 31 Jan 2025 00:29:20 GMT  
		Size: 15.3 MB (15286872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30c0064df1d0ffc289ce1d91423cf2048228fb82276833b98b9b1ba5bf4c4bb`  
		Last Modified: Fri, 31 Jan 2025 00:29:19 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:38ed9b34e7f3014723818a33871f4c244f3cf36c019d7341f6d9e5114cbdb596
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
$ docker pull rust@sha256:f1c6e953d9cfe4bd8eb4512a82647ef68965484714eb63d925b955458a357133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293935426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988feec34834b11f5aa7cb2677d196dbfb5bbfdfc4861134f6a01a22db095311`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1020b52149c924fa9f87f51bccb15dda19dec1c715e94e820355a3ea83202f7a`  
		Last Modified: Tue, 04 Feb 2025 04:48:25 GMT  
		Size: 265.7 MB (265723123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:79b36bc5042f238a4f3cffa1cbae990fec5b128951bd59298d1ccca3889bb1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c142e6c658521625b57a6e7bde7086b8625cea33c465791bf28cfe3745d8162`

```dockerfile
```

-	Layers:
	-	`sha256:8b1d943955598274f0f568ee76323314f21350045e470ad5a88fde875d1fccf6`  
		Last Modified: Tue, 04 Feb 2025 04:48:19 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8851e0f18f7ad661f6aed4f8fa89d47fcba726ffd8f76a32f5549dc3ea59379`  
		Last Modified: Tue, 04 Feb 2025 04:48:18 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:7895aa006490737a03b7cbe889f7ed3d8d5e28db4e894d3f79a5268aa0833dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302634826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f66ad885bf45b2d1a94ddc15323fd2d3928947e6973936ca6ca470f72c3bced`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e30f41f234176f2c16ce777337f908a1a5494227de2d5a8d969a9dd5c123a18`  
		Last Modified: Fri, 31 Jan 2025 00:34:31 GMT  
		Size: 278.7 MB (278720226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:a423820d19893d117d3df4fc559613e7530115a5bc0d8cf3c33fd06c0a6e99c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ddadfc654a5a9aac9217f3fac5ff192f87119cad1733955a064f26eaa22138`

```dockerfile
```

-	Layers:
	-	`sha256:cfbe61d6317e4746f8563feb4f577d0e41544c362913a508ebf36365509cebaa`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2cc265269c6bdf19d72d395d5c8bdc5d5c6ad462c4fb8ebb54d824b01cf809a`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bd37300c571a784c02cc6511be16d9f94edb5dbd0e02095213552efb4f06ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352196288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd2883e9d25ded400d0c78e03183e85ceac746ce72f11b2087bdd25d5aafc12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2851b7f466da485d0e64c4855d4ab4b2db80c9c50770dd57605c43fd6c7cdfd`  
		Last Modified: Fri, 31 Jan 2025 00:35:06 GMT  
		Size: 324.2 MB (324155257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:7d5eefa74740563880088f83d8890ff19bad3c43632520ce3217dbc1c7e4df04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb4bb2ea3aa5392b9be7b81d22a58b0149ef8d1151ba02341049dd9f638b663`

```dockerfile
```

-	Layers:
	-	`sha256:bf9fcdda35b8ab6ece9a6cb4a44f12efe6de3c8dd5bfa18d73cd9d75d00f91a3`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ba4b082669b49e4b3c44cb5d514d34fb2702a836c5f399a486a5e78c5de35c`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:d482b4787a73d9059bf5cba29999c0001d86767bf1b59b0cd8234504f1752539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308216502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5909b6178c847cfba84bcfa51b9d15491e08801021fbe9ec32369dc9a5cc9d72`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a1bebc92f7ad633f86d3b27faacbf962b234bef49b7ac15d9fa204f831a39d`  
		Last Modified: Tue, 04 Feb 2025 04:41:58 GMT  
		Size: 279.0 MB (279029046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:9b55b0bc360983ef31668d29f0831fd2f4fa885b45aeeb2e233a3ddb2a1e124d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edd34bcca496a057e05b0f78d548c9eddf9b6a2708b44833ce347d301ce24a`

```dockerfile
```

-	Layers:
	-	`sha256:b1be01bfc9316ad7a57a60c173d15ea8d7a8530d42e3983624bc3d266eeeb8d8`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1188dc47ed580591433d16de41cd10911b115b3f2865d23a352e584d38d565e`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:0ae493364decaf0420efa4ddc9cbf1554fcf147142049c52ddef57f14ed17c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355608891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ab5118ccde6aebb13da6de1ca490126cd64d28370c877db5be19bccce4685a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc73567e881b68c8629ad1da7bb11b2b21a1caa40e61c21f214bd45f2ad0aec`  
		Last Modified: Fri, 31 Jan 2025 00:31:21 GMT  
		Size: 323.6 MB (323564044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:5f9bc075b26d9f54a8993714fef535de2c3e525df84032f34f4e2cf036e57b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4572aa06386fc1be43fc645e09df3c69c1e4255b9c0dc6b9c381e50fcad395a1`

```dockerfile
```

-	Layers:
	-	`sha256:951b107c9596b3fd7667ac8fd8883145e533afb92e754bcbb6cc37abf43ab36f`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6707e52cd8b0edb10aa0f3f29ac9c470549477008999a2c916b77361a8312a8d`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:424e8413fb24c88edcaf1b689d990cc1b5d81b583332b5e8a4ebce0096a63407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358910439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a330311272f88ad3a31b23af36f93ea27b553e9eea634ea85e9ee60bf5ced46`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62668347d57abb66f2a0fab8774ffa016537604baf01fcee21fed7e2eb0f2f2d`  
		Last Modified: Fri, 31 Jan 2025 00:31:50 GMT  
		Size: 332.1 MB (332051701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:9fac2330e6da662b2713d2fde23bccfece116ba1bae59e81caaf18ec826d894c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e108fb041bf31c5ba2da80bed4e81113f09211cc58c1fa5ec8b48a6b532a90f`

```dockerfile
```

-	Layers:
	-	`sha256:a2a614ddb9300e6a218d557b5695ac3ab1776f904ceb81622d2cf584fcafad94`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb8842e3556a08959bdf1331108cdf9b1b1ab475e502e6cf2e1863ef156cad6f`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:38ed9b34e7f3014723818a33871f4c244f3cf36c019d7341f6d9e5114cbdb596
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
$ docker pull rust@sha256:f1c6e953d9cfe4bd8eb4512a82647ef68965484714eb63d925b955458a357133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293935426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988feec34834b11f5aa7cb2677d196dbfb5bbfdfc4861134f6a01a22db095311`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1020b52149c924fa9f87f51bccb15dda19dec1c715e94e820355a3ea83202f7a`  
		Last Modified: Tue, 04 Feb 2025 04:48:25 GMT  
		Size: 265.7 MB (265723123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:79b36bc5042f238a4f3cffa1cbae990fec5b128951bd59298d1ccca3889bb1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c142e6c658521625b57a6e7bde7086b8625cea33c465791bf28cfe3745d8162`

```dockerfile
```

-	Layers:
	-	`sha256:8b1d943955598274f0f568ee76323314f21350045e470ad5a88fde875d1fccf6`  
		Last Modified: Tue, 04 Feb 2025 04:48:19 GMT  
		Size: 4.0 MB (3955287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8851e0f18f7ad661f6aed4f8fa89d47fcba726ffd8f76a32f5549dc3ea59379`  
		Last Modified: Tue, 04 Feb 2025 04:48:18 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:7895aa006490737a03b7cbe889f7ed3d8d5e28db4e894d3f79a5268aa0833dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302634826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f66ad885bf45b2d1a94ddc15323fd2d3928947e6973936ca6ca470f72c3bced`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e30f41f234176f2c16ce777337f908a1a5494227de2d5a8d969a9dd5c123a18`  
		Last Modified: Fri, 31 Jan 2025 00:34:31 GMT  
		Size: 278.7 MB (278720226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a423820d19893d117d3df4fc559613e7530115a5bc0d8cf3c33fd06c0a6e99c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ddadfc654a5a9aac9217f3fac5ff192f87119cad1733955a064f26eaa22138`

```dockerfile
```

-	Layers:
	-	`sha256:cfbe61d6317e4746f8563feb4f577d0e41544c362913a508ebf36365509cebaa`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 3.8 MB (3771350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2cc265269c6bdf19d72d395d5c8bdc5d5c6ad462c4fb8ebb54d824b01cf809a`  
		Last Modified: Fri, 31 Jan 2025 00:34:24 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bd37300c571a784c02cc6511be16d9f94edb5dbd0e02095213552efb4f06ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352196288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd2883e9d25ded400d0c78e03183e85ceac746ce72f11b2087bdd25d5aafc12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2851b7f466da485d0e64c4855d4ab4b2db80c9c50770dd57605c43fd6c7cdfd`  
		Last Modified: Fri, 31 Jan 2025 00:35:06 GMT  
		Size: 324.2 MB (324155257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7d5eefa74740563880088f83d8890ff19bad3c43632520ce3217dbc1c7e4df04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb4bb2ea3aa5392b9be7b81d22a58b0149ef8d1151ba02341049dd9f638b663`

```dockerfile
```

-	Layers:
	-	`sha256:bf9fcdda35b8ab6ece9a6cb4a44f12efe6de3c8dd5bfa18d73cd9d75d00f91a3`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 4.0 MB (3977630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3ba4b082669b49e4b3c44cb5d514d34fb2702a836c5f399a486a5e78c5de35c`  
		Last Modified: Fri, 31 Jan 2025 00:34:59 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:d482b4787a73d9059bf5cba29999c0001d86767bf1b59b0cd8234504f1752539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308216502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5909b6178c847cfba84bcfa51b9d15491e08801021fbe9ec32369dc9a5cc9d72`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a1bebc92f7ad633f86d3b27faacbf962b234bef49b7ac15d9fa204f831a39d`  
		Last Modified: Tue, 04 Feb 2025 04:41:58 GMT  
		Size: 279.0 MB (279029046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9b55b0bc360983ef31668d29f0831fd2f4fa885b45aeeb2e233a3ddb2a1e124d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83edd34bcca496a057e05b0f78d548c9eddf9b6a2708b44833ce347d301ce24a`

```dockerfile
```

-	Layers:
	-	`sha256:b1be01bfc9316ad7a57a60c173d15ea8d7a8530d42e3983624bc3d266eeeb8d8`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 3.9 MB (3935202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1188dc47ed580591433d16de41cd10911b115b3f2865d23a352e584d38d565e`  
		Last Modified: Tue, 04 Feb 2025 04:41:52 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:0ae493364decaf0420efa4ddc9cbf1554fcf147142049c52ddef57f14ed17c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355608891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ab5118ccde6aebb13da6de1ca490126cd64d28370c877db5be19bccce4685a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc73567e881b68c8629ad1da7bb11b2b21a1caa40e61c21f214bd45f2ad0aec`  
		Last Modified: Fri, 31 Jan 2025 00:31:21 GMT  
		Size: 323.6 MB (323564044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5f9bc075b26d9f54a8993714fef535de2c3e525df84032f34f4e2cf036e57b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4572aa06386fc1be43fc645e09df3c69c1e4255b9c0dc6b9c381e50fcad395a1`

```dockerfile
```

-	Layers:
	-	`sha256:951b107c9596b3fd7667ac8fd8883145e533afb92e754bcbb6cc37abf43ab36f`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 3.9 MB (3927848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6707e52cd8b0edb10aa0f3f29ac9c470549477008999a2c916b77361a8312a8d`  
		Last Modified: Fri, 31 Jan 2025 00:31:13 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:424e8413fb24c88edcaf1b689d990cc1b5d81b583332b5e8a4ebce0096a63407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358910439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a330311272f88ad3a31b23af36f93ea27b553e9eea634ea85e9ee60bf5ced46`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62668347d57abb66f2a0fab8774ffa016537604baf01fcee21fed7e2eb0f2f2d`  
		Last Modified: Fri, 31 Jan 2025 00:31:50 GMT  
		Size: 332.1 MB (332051701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9fac2330e6da662b2713d2fde23bccfece116ba1bae59e81caaf18ec826d894c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e108fb041bf31c5ba2da80bed4e81113f09211cc58c1fa5ec8b48a6b532a90f`

```dockerfile
```

-	Layers:
	-	`sha256:a2a614ddb9300e6a218d557b5695ac3ab1776f904ceb81622d2cf584fcafad94`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 3.8 MB (3797187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb8842e3556a08959bdf1331108cdf9b1b1ab475e502e6cf2e1863ef156cad6f`  
		Last Modified: Fri, 31 Jan 2025 00:31:45 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:daeff596870266ef69308e65d01c8007ba61afb96a027eb80da16a4bf62e8c8e
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
$ docker pull rust@sha256:2b7845424e9284f1c26bd56fedd1483e6ca44e639ac4bf9141d9ad9c88b973ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285143356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee24319d37d90b47217bc8804087eb7618520d2d2998feaf3f673390cea2aa2f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38d52395664bc85f1e799519d83f7fac8d684946c51459db24960ed59d1aa7c`  
		Last Modified: Tue, 04 Feb 2025 04:48:14 GMT  
		Size: 254.9 MB (254890768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:40a8dc8468f83fe69082db8cc94d464f6986e7d5c4f3602a922cbfcc9e0db833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257a7ca891da9b98541d5a34a69aa9d1418765d9d43df2afbc37bbf746077841`

```dockerfile
```

-	Layers:
	-	`sha256:74c2a3b55bbe8ee8de0fc32d1f7c014a8d6adea0a3a76eae2b8609b756d302b7`  
		Last Modified: Tue, 04 Feb 2025 04:48:10 GMT  
		Size: 4.2 MB (4173204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62bd9b848e9f353bdcbab8a94cd249871f38eadc446271e5b4762c61273d9cb0`  
		Last Modified: Tue, 04 Feb 2025 04:48:10 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:93ec9878f9a9b3a46a284876e63171a6210b3736bb972b0c5d4796cda5453087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298475567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44041d0af34fcdbd74b6937cdd4fcde2cdb43dc3f5c382aa55e45a4c5bab912`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aff5a21b61cbe7871bdf8da2a3702062b03bce04a51ee677a9cbf3ba03638d`  
		Last Modified: Fri, 31 Jan 2025 00:30:10 GMT  
		Size: 272.9 MB (272941607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c983ebc16ff345a95ca08a171a8493f927087037cecae8f2b9b2f389b9031858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3eaff357bd32cb0f544f34a2365fa44d90a99114ec62745ebf85b5b7d3d9a38`

```dockerfile
```

-	Layers:
	-	`sha256:b54ace4e0ccfeff5aac11fdb5578f073c0527c00cbdc6aeb18c81c95e404fe97`  
		Last Modified: Fri, 31 Jan 2025 00:30:04 GMT  
		Size: 4.0 MB (3982354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf064fad6a270bd0bf856ffdc2d3190c5e5053b91fff4f39cecbacbb63d812d4`  
		Last Modified: Fri, 31 Jan 2025 00:30:03 GMT  
		Size: 11.4 KB (11431 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8926d7a03ffae36f85f51efb4500e9597cad63234aa4ef9a76b4cd52c65f1e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342555234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a0cc20d49b5df9482865823bf0790b94fdb2914357f8e52c6cdd78eaba7cf3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a08aeb6d94617daae47a33f519e8e57f62a92c68f9d7e0ab641e1a0db2388`  
		Last Modified: Fri, 31 Jan 2025 00:31:48 GMT  
		Size: 313.8 MB (313810321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a7e7639473ff883d127d9da2ca0a48b97a7ef5dbad30604359a8fcf08d5de9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2daa0ffecf4f2d5331e07e093f1c8b315763ccb8f81df2603598631b896ffa`

```dockerfile
```

-	Layers:
	-	`sha256:7537be7790632603cef656f944c4e7ee941a3c5277ba066e9b3f47f977ded99f`  
		Last Modified: Fri, 31 Jan 2025 00:31:42 GMT  
		Size: 4.2 MB (4169882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77131571b2e3554fde3e602115f73b6ae828709aeda119480a7eb63a5d2b4dd9`  
		Last Modified: Fri, 31 Jan 2025 00:31:42 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b4cb84f8237773ab2a9d909067e793672803a6a60891045162d71a041ec1aa84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303168402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5776fc9e1a4653e5dba7bac53c11c61b037e78e61a18aa27373901d3f0b8ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 22:09:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Thu, 30 Jan 2025 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Jan 2025 22:09:18 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.84.1
# Thu, 30 Jan 2025 22:09:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6520efae94ff86fb3a7d20c8a870e4887e3ef3a03f2fdd5f0f9693734495ae12`  
		Last Modified: Tue, 04 Feb 2025 04:41:45 GMT  
		Size: 272.0 MB (271989527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:647a1f67479f3f4281e439e65b7548234a1c5c6b725e94de11996a76eed4ceaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b69c0ca583da0b23217c4526bda4a29c5bdb6be6aeb8fa0b525a3bda0b22831`

```dockerfile
```

-	Layers:
	-	`sha256:fa17f1add2389c6162bfc65f9f177539beb333228d0c6010c96cbefb1e0e6551`  
		Last Modified: Tue, 04 Feb 2025 04:41:39 GMT  
		Size: 4.2 MB (4163461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:366959658334956233be4dc44a27efdd98c6582055be5243f0fbf01f4cbcf624`  
		Last Modified: Tue, 04 Feb 2025 04:41:39 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json
