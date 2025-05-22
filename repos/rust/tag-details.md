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
-	[`rust:1.87`](#rust187)
-	[`rust:1.87-alpine`](#rust187-alpine)
-	[`rust:1.87-alpine3.20`](#rust187-alpine320)
-	[`rust:1.87-alpine3.21`](#rust187-alpine321)
-	[`rust:1.87-bookworm`](#rust187-bookworm)
-	[`rust:1.87-bullseye`](#rust187-bullseye)
-	[`rust:1.87-slim`](#rust187-slim)
-	[`rust:1.87-slim-bookworm`](#rust187-slim-bookworm)
-	[`rust:1.87-slim-bullseye`](#rust187-slim-bullseye)
-	[`rust:1.87.0`](#rust1870)
-	[`rust:1.87.0-alpine`](#rust1870-alpine)
-	[`rust:1.87.0-alpine3.20`](#rust1870-alpine320)
-	[`rust:1.87.0-alpine3.21`](#rust1870-alpine321)
-	[`rust:1.87.0-bookworm`](#rust1870-bookworm)
-	[`rust:1.87.0-bullseye`](#rust1870-bullseye)
-	[`rust:1.87.0-slim`](#rust1870-slim)
-	[`rust:1.87.0-slim-bookworm`](#rust1870-slim-bookworm)
-	[`rust:1.87.0-slim-bullseye`](#rust1870-slim-bullseye)
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
$ docker pull rust@sha256:893a03d96de2c0e6eb8b73e24b2266264b6dee244ce997d1bae246901093ba23
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
$ docker pull rust@sha256:3d4a2ab199238d07982c4b2bd663ed9e54d135eeecbfa326a8cc73d6659a57ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553331383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed12ea880e03238fe4e68bc7e19b72fe31649a20a35874431e0e3b9ee37bfcfe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f099911d692f62b851cf49a1e93294288a115f5cd2d014180e4d3684d34ab`  
		Last Modified: Thu, 22 May 2025 00:12:38 GMT  
		Size: 211.4 MB (211362119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60122453ea09122539d0bff9dd2ace9ad0fb5f94f28106482345e871b8776f`  
		Last Modified: Thu, 22 May 2025 01:22:53 GMT  
		Size: 205.1 MB (205065526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:c22e4e30bdb5ca31034eb63aa448f9c77a1102d1c161ad253c2925c9fb5de7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15583659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f90206053d1f253e46155a79fb7bb6966620d44bd8a39970cae527f1f819a1f`

```dockerfile
```

-	Layers:
	-	`sha256:6353069eb27b9defe4c9f76cfe25f6f0812b36dbd10a091e3f05bc17d5e07939`  
		Last Modified: Thu, 22 May 2025 01:22:51 GMT  
		Size: 15.6 MB (15570520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36489b5c50efe5ec3b3b1a288cc4d0a9ec10bd1986b2a4bed6d14eeb6f342209`  
		Last Modified: Thu, 22 May 2025 01:22:50 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:a717a4a677877e4c90506d6094ba956c65c8acbb675322e10051e026b84ac7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549353893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c15507a70a72169329e3fb52a9e9f8e6fda428fc8a10c673722a27ad87d7517`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Mon, 28 Apr 2025 21:15:27 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Tue, 29 Apr 2025 03:37:10 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3553b1499305feec4f182c1e2562e06daaecb3dc337d83b89b8c909f46c0a1`  
		Last Modified: Tue, 29 Apr 2025 13:22:56 GMT  
		Size: 59.6 MB (59640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d55cc6c59023a65c15579520e32553ab9f1e2d6377e8e4dd69393e113713d3`  
		Last Modified: Tue, 29 Apr 2025 16:44:12 GMT  
		Size: 175.3 MB (175316182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae6506bd78c8b0409ae60f919fcf0308fadded07bb677e52eaca831e32f27e4`  
		Last Modified: Fri, 16 May 2025 00:45:12 GMT  
		Size: 248.3 MB (248282041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:704762edf7170410c4143b57dc2c2592340918185bbd978e992015426067433c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15387590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118ae28de64f563725129ee9df3f3efdfd56f98689b846a2020a59babcd3a5a3`

```dockerfile
```

-	Layers:
	-	`sha256:0ed13d7d744dbbbcbf9675297a7a1707dc0b984f5b19f5a792be6856c23b4237`  
		Last Modified: Fri, 16 May 2025 00:45:09 GMT  
		Size: 15.4 MB (15374344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cc69fc971f6f9022f452d055c879d015b21e562a7728564f74f09f10c9bf7f`  
		Last Modified: Fri, 16 May 2025 00:45:06 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:79638f277b74a79352c910c6479b5cb8c25b0f2ef2b11af4b7f2d63a04bbe78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513058250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facc597070c63677b4fc7121846c580a1ee5f055d749af0856a73fc113dc99e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Tue, 29 Apr 2025 18:37:11 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d41c7623f41e51939686bf861fe89538ae4dc84481ff4136b55524e770d2603`  
		Last Modified: Wed, 30 Apr 2025 02:16:31 GMT  
		Size: 202.7 MB (202748227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2789ce74abfb6ada85cef976765f28a31f0d76101d35d89fe6f30e6a160f5cf7`  
		Last Modified: Thu, 15 May 2025 21:23:55 GMT  
		Size: 174.1 MB (174082434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:f7f0b6b46806bffe1c5d2161f9299dc0a9238fefa3183278ae6109c67595d89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15613623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79ce7216bf86b5ea593af61df25f8acf8b9a077a234befe5f780ee67da136ae`

```dockerfile
```

-	Layers:
	-	`sha256:00c23c1dc907f8d220ac1ef9c18b98380d358000cb5edabb21556f1ece3cc7ec`  
		Last Modified: Thu, 15 May 2025 21:23:51 GMT  
		Size: 15.6 MB (15600332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e5ccf8415d9f8e96f788c503d732dfce14045f3ba24d8366c936bf8762ef8`  
		Last Modified: Thu, 15 May 2025 21:23:50 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:d1548c29f4a54233ce3663dbf31e24697f803f2eaa51dc48517fc374e605cd53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579410243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599b9672494cb7a24c90726f5649fd8bb62e266686d6c92c3a70db98df8fb36a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Wed, 21 May 2025 23:20:06 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8c7f8292580c2c70e8cb47ec957249f0882ee6ee3737bf3250e44650a38db`  
		Last Modified: Wed, 21 May 2025 23:37:30 GMT  
		Size: 66.2 MB (66224115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e426a3a2617e34e93d75e9b5c79113e976623e3633255f578a7087d4221ba47`  
		Last Modified: Thu, 22 May 2025 00:12:45 GMT  
		Size: 210.3 MB (210303724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e15432acb4bbafe1b177dc4d3a8a7616460a38e03b58bf34ad9f8a4e54f229`  
		Last Modified: Thu, 22 May 2025 01:21:36 GMT  
		Size: 228.6 MB (228555174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:626889100874bfa993f52c41bf9e48649fc7b964c1dd889884eb3b1f106ed47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a19fecc316543561006e19323c1d5f88ff6b410323def3f15d858f5152634a`

```dockerfile
```

-	Layers:
	-	`sha256:d5613f30992ef58d04da59a0c3fc9df18e23a6aea5ddc9094597440de2585099`  
		Last Modified: Thu, 22 May 2025 01:21:31 GMT  
		Size: 15.5 MB (15547420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ffe58d9c1f399bf6345b1eae0a9b2681b28358b08f9b7a3333ff32c090bcda`  
		Last Modified: Thu, 22 May 2025 01:21:30 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:edad25bbea95469efae8b7575e3621376e99cdac3e8dc847e12990d79ffa15e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639187573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf09d1faa6098d8816d94f3129d858a3c9895d7ccb9d5f8c7510120d86649501`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Tue, 29 Apr 2025 07:46:58 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Tue, 29 Apr 2025 08:29:00 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f7f895e65e8530bee082db2e14aefaa34547b4753e60990faca2b691714e63`  
		Last Modified: Tue, 29 Apr 2025 09:10:46 GMT  
		Size: 214.4 MB (214409240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f771a754d3f6d9880020eef886dee95dbbc411da896e8d6188ce4b35d1ccea1`  
		Last Modified: Thu, 15 May 2025 21:41:17 GMT  
		Size: 277.0 MB (276955667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:25e42159bf1ae8fed15f948468f0850e56728c647b8dc63fc1178c7946f65a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b8b744207f149e1825389c70977eaaa027331392f4bb1af2cf53edda9e7348`

```dockerfile
```

-	Layers:
	-	`sha256:1261dadc28c70b94878106245907b72b29ecaecd634cf88ba53927741da602e3`  
		Last Modified: Thu, 15 May 2025 21:40:56 GMT  
		Size: 15.5 MB (15546986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43db0b6c0fb41e034652a717f321ad57ef840725dc6ecbddbb455e4ba85b36da`  
		Last Modified: Thu, 15 May 2025 21:40:55 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:a46b263c2cce2b762d073f453a72c33eb474d71183208ed22ebccb7841b9309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604372811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cc62b570c4d03e5e28a7b9abaeec07a8d1a0681c67877cdd087f829e8b5543`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Tue, 29 Apr 2025 00:01:21 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Tue, 29 Apr 2025 02:58:48 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfe8bd3e826ba76e4ad73b0a5ce638276af95b860bec9b25c2754c5600c5a61`  
		Last Modified: Tue, 29 Apr 2025 05:34:00 GMT  
		Size: 183.4 MB (183405963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589f590c508c398e3740adc2dd1d0915bdc9a36f36693dacb7d2cb83012bcca1`  
		Last Modified: Thu, 15 May 2025 23:34:36 GMT  
		Size: 286.3 MB (286310328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:0bb2f2b59196707a888cfccbc092b473f6e382739d12c2db5d9117cd4f490b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15395439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61693f885fe5810811eb46994aa1af308f091912dc96214dad8fd6651bc00831`

```dockerfile
```

-	Layers:
	-	`sha256:011ca34cbff4dd90ea475c3878d26371312698ea04d43f7886f8598f7f924610`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 15.4 MB (15382300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4311afc8d95a09e62d7f51e2603140152c818532e8aa83db3b1545ef3d7a15`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:fa7c28576553c431224a85c897c38f3a6443bd831be37061ab3560d9e797dc82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:77b6339cdb0832ad483e0d6389c4c6df605568e9c2f1a14fe76dd3b3cd3cd023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324247403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ffcf6a0b7e66d9cf8d858d524ebcd49bb36208a8c8d449ab6a1927df31f7b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b343ca42d769a088aad30a06435916be946b7bd77c275c4c48aa9c02d07ebc6`  
		Last Modified: Thu, 15 May 2025 18:37:40 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0312ddedcb8a05877b03a2214ddd4942d87d6bd8684a5f5bc0353f72d76def`  
		Last Modified: Thu, 15 May 2025 18:37:44 GMT  
		Size: 259.0 MB (259040344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:4e64c00b2317960a70850f4400db745c6cfb2bdd9f3d125aa41eae29aa6db0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.7 KB (795741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60b54f74613b5e61b7293457c23a015874a512e095a95d91dfbad52ebb043b4`

```dockerfile
```

-	Layers:
	-	`sha256:a5a1184050fab9829a713a4d20d0725d4538c6e742e9839d6591249330d5359e`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 783.8 KB (783823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05e06b11fae76f35a913f94980f7b264abfa081dffa29929dd773c6969a089d`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c46257a5086c247e6cf7f47f0b1bfd6829b0487f60ba421e09dc869a1cf8854e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 MB (326998595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4173638e4c107fec82a3872cebbc9896730ad56739846f1cab5b2d2a6662d444`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a8d04fc53dbb480e66cf7321229cda858c75a9bfa488474aabc6a3fbc3423`  
		Last Modified: Mon, 05 May 2025 22:59:43 GMT  
		Size: 59.1 MB (59101363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd10981d51d5c4342a74b76870500712f6977bafb0891f69b5b725cd3f83575b`  
		Last Modified: Thu, 15 May 2025 21:52:00 GMT  
		Size: 263.9 MB (263904203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:34672929840929fdaeda033ca2f79184da7ad0a5f4ca4c5afc3d17ab43dceceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.5 KB (875494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c7d1faabdd527c0adb51cec9eac15ffbf9a2ad32dd7bad9fd10768aef390ae`

```dockerfile
```

-	Layers:
	-	`sha256:5fad1a9258bc9e5e8818e557ec0496368c72e4184380ef235dc4bb26a03a6e03`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 863.4 KB (863409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4799a729390389da9955e76bdba397218c8fff4138d88735449c1364a6120788`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:126b44382fa926ce41eecac3ef4628de508f0df8556fe43e8d64cdcd1cbbe40b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:a6e21abdf25464282e9ebe77b75a597cbd0b21d375eafa86c38af1e1cb8a2d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.0 MB (317984256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69198b701be7dc50b960f31ef7f4fd2764b266e2d8adaa0bab88ab59ce2b2bf6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718715b3cbe3b4fd9094909206504e5958585bd739a34dc4fb5b7f6ed2131b8`  
		Last Modified: Thu, 15 May 2025 18:37:42 GMT  
		Size: 55.3 MB (55315586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeb4a9d8a98d7b7dadf2be0b1943267d81b081cb2fb12a85484c6aaadf235fb`  
		Last Modified: Thu, 15 May 2025 18:37:48 GMT  
		Size: 259.0 MB (259041773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:279079ce7141a696c62912e2b546d3b1db80da36385b8291b96bd87b06a333ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.5 KB (722503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f9514c3a9ca96fa531c453a6086450f8357d88a8602759b77fade775484d62`

```dockerfile
```

-	Layers:
	-	`sha256:7ef4df00128cf574a18437ccce5e6d348c5ac96f9e656076475640bc336b72b8`  
		Last Modified: Thu, 15 May 2025 18:37:41 GMT  
		Size: 711.8 KB (711789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a9394ddea85fc3e016d5927f8ce6a38638e7c7eeea1996460a0e68f6915e5c6`  
		Last Modified: Thu, 15 May 2025 18:37:40 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2881015e0b8d0d3e45e40cf26cedbea750dc4e4bae1f9492ea6ea20c3c478296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320946007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f9aeec89829426e53d9ec2993f49c4e8add3c62bbb31e1a8833ca8f6bba7b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c6aa5430354637d99185e3c6f997bb89b34d0340d714c59489470f3b28fb00`  
		Last Modified: Mon, 05 May 2025 22:58:37 GMT  
		Size: 53.0 MB (52950277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d7b743d7f5864c65b2894547a9334b33385928622ae90e6a32c6e8856c668`  
		Last Modified: Thu, 15 May 2025 21:26:08 GMT  
		Size: 263.9 MB (263904565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:b8cb278c3d3464f502ef0c4e303cc516cf61210f397481f3f916b0efd803552e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0465991995a77f18ceff0792501f873542ee79e340b0bc4e6a168e2d55cf0cfb`

```dockerfile
```

-	Layers:
	-	`sha256:13318289bd5cbf3b293bd9e48b8d9dfb9679941c1b10fefc888f757d08695f98`  
		Last Modified: Thu, 15 May 2025 21:26:00 GMT  
		Size: 747.7 KB (747721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5df0c715639e649fb2f087e25e05ab1d51803c9e80193b7ded83d66aa0f06e`  
		Last Modified: Thu, 15 May 2025 21:25:59 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.21`

```console
$ docker pull rust@sha256:fa7c28576553c431224a85c897c38f3a6443bd831be37061ab3560d9e797dc82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:77b6339cdb0832ad483e0d6389c4c6df605568e9c2f1a14fe76dd3b3cd3cd023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324247403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ffcf6a0b7e66d9cf8d858d524ebcd49bb36208a8c8d449ab6a1927df31f7b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b343ca42d769a088aad30a06435916be946b7bd77c275c4c48aa9c02d07ebc6`  
		Last Modified: Thu, 15 May 2025 18:37:40 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0312ddedcb8a05877b03a2214ddd4942d87d6bd8684a5f5bc0353f72d76def`  
		Last Modified: Thu, 15 May 2025 18:37:44 GMT  
		Size: 259.0 MB (259040344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:4e64c00b2317960a70850f4400db745c6cfb2bdd9f3d125aa41eae29aa6db0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.7 KB (795741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60b54f74613b5e61b7293457c23a015874a512e095a95d91dfbad52ebb043b4`

```dockerfile
```

-	Layers:
	-	`sha256:a5a1184050fab9829a713a4d20d0725d4538c6e742e9839d6591249330d5359e`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 783.8 KB (783823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05e06b11fae76f35a913f94980f7b264abfa081dffa29929dd773c6969a089d`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c46257a5086c247e6cf7f47f0b1bfd6829b0487f60ba421e09dc869a1cf8854e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 MB (326998595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4173638e4c107fec82a3872cebbc9896730ad56739846f1cab5b2d2a6662d444`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a8d04fc53dbb480e66cf7321229cda858c75a9bfa488474aabc6a3fbc3423`  
		Last Modified: Mon, 05 May 2025 22:59:43 GMT  
		Size: 59.1 MB (59101363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd10981d51d5c4342a74b76870500712f6977bafb0891f69b5b725cd3f83575b`  
		Last Modified: Thu, 15 May 2025 21:52:00 GMT  
		Size: 263.9 MB (263904203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:34672929840929fdaeda033ca2f79184da7ad0a5f4ca4c5afc3d17ab43dceceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.5 KB (875494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c7d1faabdd527c0adb51cec9eac15ffbf9a2ad32dd7bad9fd10768aef390ae`

```dockerfile
```

-	Layers:
	-	`sha256:5fad1a9258bc9e5e8818e557ec0496368c72e4184380ef235dc4bb26a03a6e03`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 863.4 KB (863409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4799a729390389da9955e76bdba397218c8fff4138d88735449c1364a6120788`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:893a03d96de2c0e6eb8b73e24b2266264b6dee244ce997d1bae246901093ba23
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
$ docker pull rust@sha256:3d4a2ab199238d07982c4b2bd663ed9e54d135eeecbfa326a8cc73d6659a57ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553331383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed12ea880e03238fe4e68bc7e19b72fe31649a20a35874431e0e3b9ee37bfcfe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f099911d692f62b851cf49a1e93294288a115f5cd2d014180e4d3684d34ab`  
		Last Modified: Thu, 22 May 2025 00:12:38 GMT  
		Size: 211.4 MB (211362119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60122453ea09122539d0bff9dd2ace9ad0fb5f94f28106482345e871b8776f`  
		Last Modified: Thu, 22 May 2025 01:22:53 GMT  
		Size: 205.1 MB (205065526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c22e4e30bdb5ca31034eb63aa448f9c77a1102d1c161ad253c2925c9fb5de7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15583659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f90206053d1f253e46155a79fb7bb6966620d44bd8a39970cae527f1f819a1f`

```dockerfile
```

-	Layers:
	-	`sha256:6353069eb27b9defe4c9f76cfe25f6f0812b36dbd10a091e3f05bc17d5e07939`  
		Last Modified: Thu, 22 May 2025 01:22:51 GMT  
		Size: 15.6 MB (15570520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36489b5c50efe5ec3b3b1a288cc4d0a9ec10bd1986b2a4bed6d14eeb6f342209`  
		Last Modified: Thu, 22 May 2025 01:22:50 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:a717a4a677877e4c90506d6094ba956c65c8acbb675322e10051e026b84ac7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549353893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c15507a70a72169329e3fb52a9e9f8e6fda428fc8a10c673722a27ad87d7517`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Mon, 28 Apr 2025 21:15:27 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Tue, 29 Apr 2025 03:37:10 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3553b1499305feec4f182c1e2562e06daaecb3dc337d83b89b8c909f46c0a1`  
		Last Modified: Tue, 29 Apr 2025 13:22:56 GMT  
		Size: 59.6 MB (59640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d55cc6c59023a65c15579520e32553ab9f1e2d6377e8e4dd69393e113713d3`  
		Last Modified: Tue, 29 Apr 2025 16:44:12 GMT  
		Size: 175.3 MB (175316182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae6506bd78c8b0409ae60f919fcf0308fadded07bb677e52eaca831e32f27e4`  
		Last Modified: Fri, 16 May 2025 00:45:12 GMT  
		Size: 248.3 MB (248282041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:704762edf7170410c4143b57dc2c2592340918185bbd978e992015426067433c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15387590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118ae28de64f563725129ee9df3f3efdfd56f98689b846a2020a59babcd3a5a3`

```dockerfile
```

-	Layers:
	-	`sha256:0ed13d7d744dbbbcbf9675297a7a1707dc0b984f5b19f5a792be6856c23b4237`  
		Last Modified: Fri, 16 May 2025 00:45:09 GMT  
		Size: 15.4 MB (15374344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cc69fc971f6f9022f452d055c879d015b21e562a7728564f74f09f10c9bf7f`  
		Last Modified: Fri, 16 May 2025 00:45:06 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:79638f277b74a79352c910c6479b5cb8c25b0f2ef2b11af4b7f2d63a04bbe78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513058250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facc597070c63677b4fc7121846c580a1ee5f055d749af0856a73fc113dc99e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Tue, 29 Apr 2025 18:37:11 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d41c7623f41e51939686bf861fe89538ae4dc84481ff4136b55524e770d2603`  
		Last Modified: Wed, 30 Apr 2025 02:16:31 GMT  
		Size: 202.7 MB (202748227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2789ce74abfb6ada85cef976765f28a31f0d76101d35d89fe6f30e6a160f5cf7`  
		Last Modified: Thu, 15 May 2025 21:23:55 GMT  
		Size: 174.1 MB (174082434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f7f0b6b46806bffe1c5d2161f9299dc0a9238fefa3183278ae6109c67595d89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15613623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79ce7216bf86b5ea593af61df25f8acf8b9a077a234befe5f780ee67da136ae`

```dockerfile
```

-	Layers:
	-	`sha256:00c23c1dc907f8d220ac1ef9c18b98380d358000cb5edabb21556f1ece3cc7ec`  
		Last Modified: Thu, 15 May 2025 21:23:51 GMT  
		Size: 15.6 MB (15600332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e5ccf8415d9f8e96f788c503d732dfce14045f3ba24d8366c936bf8762ef8`  
		Last Modified: Thu, 15 May 2025 21:23:50 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:d1548c29f4a54233ce3663dbf31e24697f803f2eaa51dc48517fc374e605cd53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579410243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599b9672494cb7a24c90726f5649fd8bb62e266686d6c92c3a70db98df8fb36a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Wed, 21 May 2025 23:20:06 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8c7f8292580c2c70e8cb47ec957249f0882ee6ee3737bf3250e44650a38db`  
		Last Modified: Wed, 21 May 2025 23:37:30 GMT  
		Size: 66.2 MB (66224115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e426a3a2617e34e93d75e9b5c79113e976623e3633255f578a7087d4221ba47`  
		Last Modified: Thu, 22 May 2025 00:12:45 GMT  
		Size: 210.3 MB (210303724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e15432acb4bbafe1b177dc4d3a8a7616460a38e03b58bf34ad9f8a4e54f229`  
		Last Modified: Thu, 22 May 2025 01:21:36 GMT  
		Size: 228.6 MB (228555174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:626889100874bfa993f52c41bf9e48649fc7b964c1dd889884eb3b1f106ed47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a19fecc316543561006e19323c1d5f88ff6b410323def3f15d858f5152634a`

```dockerfile
```

-	Layers:
	-	`sha256:d5613f30992ef58d04da59a0c3fc9df18e23a6aea5ddc9094597440de2585099`  
		Last Modified: Thu, 22 May 2025 01:21:31 GMT  
		Size: 15.5 MB (15547420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ffe58d9c1f399bf6345b1eae0a9b2681b28358b08f9b7a3333ff32c090bcda`  
		Last Modified: Thu, 22 May 2025 01:21:30 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:edad25bbea95469efae8b7575e3621376e99cdac3e8dc847e12990d79ffa15e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639187573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf09d1faa6098d8816d94f3129d858a3c9895d7ccb9d5f8c7510120d86649501`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Tue, 29 Apr 2025 07:46:58 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Tue, 29 Apr 2025 08:29:00 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f7f895e65e8530bee082db2e14aefaa34547b4753e60990faca2b691714e63`  
		Last Modified: Tue, 29 Apr 2025 09:10:46 GMT  
		Size: 214.4 MB (214409240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f771a754d3f6d9880020eef886dee95dbbc411da896e8d6188ce4b35d1ccea1`  
		Last Modified: Thu, 15 May 2025 21:41:17 GMT  
		Size: 277.0 MB (276955667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:25e42159bf1ae8fed15f948468f0850e56728c647b8dc63fc1178c7946f65a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b8b744207f149e1825389c70977eaaa027331392f4bb1af2cf53edda9e7348`

```dockerfile
```

-	Layers:
	-	`sha256:1261dadc28c70b94878106245907b72b29ecaecd634cf88ba53927741da602e3`  
		Last Modified: Thu, 15 May 2025 21:40:56 GMT  
		Size: 15.5 MB (15546986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43db0b6c0fb41e034652a717f321ad57ef840725dc6ecbddbb455e4ba85b36da`  
		Last Modified: Thu, 15 May 2025 21:40:55 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:a46b263c2cce2b762d073f453a72c33eb474d71183208ed22ebccb7841b9309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604372811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cc62b570c4d03e5e28a7b9abaeec07a8d1a0681c67877cdd087f829e8b5543`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Tue, 29 Apr 2025 00:01:21 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Tue, 29 Apr 2025 02:58:48 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfe8bd3e826ba76e4ad73b0a5ce638276af95b860bec9b25c2754c5600c5a61`  
		Last Modified: Tue, 29 Apr 2025 05:34:00 GMT  
		Size: 183.4 MB (183405963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589f590c508c398e3740adc2dd1d0915bdc9a36f36693dacb7d2cb83012bcca1`  
		Last Modified: Thu, 15 May 2025 23:34:36 GMT  
		Size: 286.3 MB (286310328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0bb2f2b59196707a888cfccbc092b473f6e382739d12c2db5d9117cd4f490b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15395439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61693f885fe5810811eb46994aa1af308f091912dc96214dad8fd6651bc00831`

```dockerfile
```

-	Layers:
	-	`sha256:011ca34cbff4dd90ea475c3878d26371312698ea04d43f7886f8598f7f924610`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 15.4 MB (15382300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4311afc8d95a09e62d7f51e2603140152c818532e8aa83db3b1545ef3d7a15`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:51f2d8c9d5c6c2506765a1f9e17c8ebc33aded193deffa72356a337ca396255a
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
$ docker pull rust@sha256:0b451f05a606a3b41c9a864500a9c50f9886a9aeb8c563d1b7ce1cf1bda5e56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526472326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bf6dd7679501c4f32309849fca9c4030a99afef60deb99454ca0ec09b18262`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Wed, 21 May 2025 23:20:29 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69a02035012d2783a66ac7ecc549af09c1718d81affa5f9c39abcf969da971`  
		Last Modified: Wed, 21 May 2025 23:37:39 GMT  
		Size: 54.8 MB (54757308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94932625c5ab18ebb7640ecd70dd33061ba90cc7666b7ff06042a8bd7cf63fb`  
		Last Modified: Thu, 22 May 2025 00:12:38 GMT  
		Size: 197.1 MB (197133895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f7643072d1ada9eba65bdb4a38d74d4c1a9411d53739374cd72e0419954af6`  
		Last Modified: Thu, 22 May 2025 01:22:46 GMT  
		Size: 205.1 MB (205066054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:73be1b1016ce85742cea899179b3476659dae35179498a4a4c22bda005e6fd13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15186206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dd4e66e59d674615efab4283c43eb93a71f55d7f04c60a4770da8c927e6a7a`

```dockerfile
```

-	Layers:
	-	`sha256:42e2775ff89b0e1ca092e8b334f36270b1c16e46d0b4457d9bd59a09a0b61499`  
		Last Modified: Thu, 22 May 2025 01:22:43 GMT  
		Size: 15.2 MB (15174957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954ef5cd1b91201a29c71b2b2d32806e4c10fcfd2bacb9671a09bf86b7820f49`  
		Last Modified: Thu, 22 May 2025 01:22:43 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:d7d4f233403022183f2af37fd51898a1d97b78dbed910fe576277af94e82d87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.4 MB (530385150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd03e62aeebdd1f83bdc094079d1c37453a5be372a0b838c1aecb8029ef3654`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Mon, 28 Apr 2025 21:16:06 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Tue, 29 Apr 2025 03:37:44 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4cecedb434598f97e33a3320b6af6e1676388e6c13b31f0aab4b7c9372012`  
		Last Modified: Tue, 29 Apr 2025 13:23:50 GMT  
		Size: 50.6 MB (50625161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce34362265f33a06975f249d19b3ebf3e131e052b1333868e863a53ee816bc45`  
		Last Modified: Tue, 29 Apr 2025 16:46:09 GMT  
		Size: 167.6 MB (167558886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9539bd9006e9f246574a8c2d9f897d10b5c6813afbfee941acec16d2754a253`  
		Last Modified: Fri, 16 May 2025 00:40:56 GMT  
		Size: 248.3 MB (248282029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:132febdf611c5e84d3d37871ca0910429259ce6b4d1deae9b87f53877127b12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14985623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c231e250c4ae7852218bf793df0bff4ce8abb50ba96b3716aea288f555f2b9a5`

```dockerfile
```

-	Layers:
	-	`sha256:abc988d1691a81eb6a0aa6a62af1d62907119d597c4ba544006f95b4fbf04e4c`  
		Last Modified: Fri, 16 May 2025 00:40:50 GMT  
		Size: 15.0 MB (14974298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d8d1c4bd3d1fa595a076fd516f16ff496c0d1db3b0bcf0e1585088e674aebf9`  
		Last Modified: Fri, 16 May 2025 00:40:50 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:237790655bcd54abab4c49c48259af2dd699173335de4e955048c62ddb2a3146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486950939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172df5659cc3f650a81e372d4074c690126a29a4b8873fdab84f99d05ddb3b6f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Tue, 29 Apr 2025 01:47:13 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Tue, 29 Apr 2025 18:37:49 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356545a2ed16b26897f2a271b3f4a7d7e64a9bf9bc0c78fdf4f1386401e37428`  
		Last Modified: Wed, 30 Apr 2025 02:18:06 GMT  
		Size: 190.0 MB (190024328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98136a9af2cf6c7fbc2743af98d832e725438a68b83e340d2dae7eaf7e34c4b4`  
		Last Modified: Thu, 15 May 2025 21:21:52 GMT  
		Size: 174.1 MB (174081523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:837bb4c602d1047b0f2f89e25c244920e3bae19537f888475e7494b23b57334a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce05b2083a6cd6c1338f72b13b1b2f39104bb810013782bd93110d997e51a630`

```dockerfile
```

-	Layers:
	-	`sha256:928ea9471f7f3720e5182302bc720fcc69c8958c677a45ae48ee625d81f5a9cb`  
		Last Modified: Thu, 15 May 2025 21:21:44 GMT  
		Size: 15.2 MB (15176927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fad39b7b7530b615cc7f2c4f42a809573b4e4e41b9423f8b02afdc2f31d3495a`  
		Last Modified: Thu, 15 May 2025 21:21:43 GMT  
		Size: 11.4 KB (11352 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:ae9554cbdf2ce6d8c237cf2e62fd8da4d3e7df981bf95d72dfb02636102a0223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555598704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7804a77f872b7bebd7c0c219c30213b20ee8e554d9e5fac9bb4cbb19e7738672`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde5c2ebb13d7ca154f5cc8b4e26e7e3a669b8bac689ec15851b65e299a0fd6`  
		Last Modified: Wed, 21 May 2025 23:19:38 GMT  
		Size: 16.3 MB (16268487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e052669a7dd77fed659f1b6d3fcf5171929214e8821aaf28744160fb71f4f1`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 56.0 MB (56049779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f06bdedcf2f8fa5a0d52d346902f8aceec74013af364956265940521230002`  
		Last Modified: Thu, 22 May 2025 00:13:14 GMT  
		Size: 200.0 MB (200039337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fee6831b1ed84af5ee781297e8478225fc1f1ccd5f724ec9187d1041829c86f`  
		Last Modified: Thu, 22 May 2025 01:21:26 GMT  
		Size: 228.6 MB (228555319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:99cd576357e873f7fc20c2b9a3a22e4305a969e9fc11165246cc866b8ddb5140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15172877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c047e879fdd094e6ee7ea60daeadb0ab59443f0c260184750cf5bb5a7c5c6022`

```dockerfile
```

-	Layers:
	-	`sha256:598d23bd2066f74b5b66e8e4d84a9eed0971a6998849692f35e8eb929c9570ec`  
		Last Modified: Thu, 22 May 2025 01:21:21 GMT  
		Size: 15.2 MB (15161661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f759815be291285c72b5589321a35711ca79f0ac7a669df83b713ceef6a54b26`  
		Last Modified: Thu, 22 May 2025 01:21:21 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:989095388527710c84035fb19f851eee7c1ef3280f20885afaa3f1ca40c132a0
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
$ docker pull rust@sha256:bb40fab9222e04479fcdd45dd897df82c6ce527f1be367d7af26b9d8b0ef6a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304047247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed37a08d4804ab8dc49d922940d98831dba0a9ab0d064517c16d3e8ebc61028`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfee91a65ac6ac51500a0ec06fef619ed43fb695781fb524461a5c4d2d637da`  
		Last Modified: Wed, 21 May 2025 23:30:50 GMT  
		Size: 275.8 MB (275821917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:efe02561cb166afdf2b5ceff7aa87559a0d4305e49b91aaf2b14ecea3dfac430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98fcfc56b3317ccdbefec9a1d8a372664b2c3fcb175e2a68692eb79b093238e`

```dockerfile
```

-	Layers:
	-	`sha256:8b0b25427736858183a7036091af78fd2db2d997da37facb6e4d05aaeae085ac`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 4.0 MB (3984195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d91ce431f3e8f53deb758af58dcf2d0d526914b7e949edc4a9194ad60d84b79`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:9e29ea2079cecf087bbda1c2fd2ad61236b36515fa51c6ff29828e8720467d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.1 MB (320057803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc73805e0130280f517428c036ce3ef1b66e23f5cfc530e79e9523fff52a2da`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2affe51206b495c552876f1361055b5ba2ba5c499a12dc799182e527f88fee8f`  
		Last Modified: Fri, 16 May 2025 00:47:33 GMT  
		Size: 296.1 MB (296119729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:7f307223876a0415ebe98e4232538d19ba2dfd94a4587afd1b6625bc10411268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b85b7e64240d9a4922e80471ff1f6d7ddf3fa2df0e3d30083ee3421d6afb6f`

```dockerfile
```

-	Layers:
	-	`sha256:8533123b469cd2f37a235ff4ae7f91614ee1dd9a8b02d36fd1828d5275843a82`  
		Last Modified: Fri, 16 May 2025 00:47:27 GMT  
		Size: 3.8 MB (3798367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3d2d35d257570cf330e2e8c1696e66fc0e1c593229df7b7735be317bae3977`  
		Last Modified: Fri, 16 May 2025 00:47:26 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:e42c600982c6907c6953b3067f6c48033e395f4d10181943c51ebac2f7f23bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267996219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3084e189f23691ae93614b7982a7e2cac388bca91738c5669989e7d8b796f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed633d6741d291fe9a1763e68d2cccb161b0647cba3b92db34f2082a23b9e0e5`  
		Last Modified: Thu, 15 May 2025 21:25:02 GMT  
		Size: 239.9 MB (239929597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:49d4587422ab4bfcf0173cab06c43b80c8984a7ab4c06e5735771535306cbd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4019635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ed220b85632009846640d2295c2f4ab23f854fa0b42e0c3243b5cefdd747ae`

```dockerfile
```

-	Layers:
	-	`sha256:3554280116bde06c2a965fd24a497d66881cd9d1aa281871d1b73769d8a2094d`  
		Last Modified: Thu, 15 May 2025 21:24:57 GMT  
		Size: 4.0 MB (4006212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec9148c526a826a45ec9302a772ebcdbad438372587030aeb75898a207f5529`  
		Last Modified: Thu, 15 May 2025 21:24:56 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:ba53dc2028f64403c6bd2a89614ec2e82ac8573537c865976e2cc6374ec2029b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325373122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2b704e3adfa1d07aa1cbc2987edbfeecfa1944de3fb2c3a968bd74c02ec417`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814ea34b52869e575de48c99d2f39a24d0e4d29694d8f3a01507831f57c2b06d`  
		Last Modified: Wed, 21 May 2025 23:24:41 GMT  
		Size: 296.2 MB (296165635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:889b0b25c9982cd5fd0571c6b2e686ec647c319ecab6c6d5a7adb6d0d6435a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3976779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8904643b41a0647ba565c4644b3392f328605ea998f3baade734ba5d2aacb870`

```dockerfile
```

-	Layers:
	-	`sha256:b1c6f53dcb1207b295e2a9b9c928c3d427f03fff1cda3c59d8cb153c959edd63`  
		Last Modified: Wed, 21 May 2025 23:24:35 GMT  
		Size: 4.0 MB (3963560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f37c60466f2e78fb30d52c14fbff69ffd5e0acccfafbf0eeb4d5f39c371cb4`  
		Last Modified: Wed, 21 May 2025 23:24:34 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:73839fb86f1fecdfa502eed34acc218fa19ea5b56c0c32411ea7a21108c4cd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377784662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3902494a5ed4edbc6b7649c8b67f6216b185ab73ac30aeb3191240f8c20079b2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf472daa2685f63de3e031e0501577d5082ab01e4cd68a594850d5b117971ab4`  
		Last Modified: Thu, 15 May 2025 21:44:03 GMT  
		Size: 345.7 MB (345716219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b15ebebde5337a1f5f6d3035e50b978c23924c91ade52b89e87fb0ea78553cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38b8f6da58da02263499e3598466193030911e6f0ffd21726d6f52111dd4a5c`

```dockerfile
```

-	Layers:
	-	`sha256:045d5e4d7f1b02b270f2b39f6cfdc49b5cb491134b55b9308ddaa4bf79f39391`  
		Last Modified: Thu, 15 May 2025 21:43:49 GMT  
		Size: 4.0 MB (3956177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53809675a1cc4de34fd12f811d8d666321a4623ebb988f23833edcee8fbc1ef`  
		Last Modified: Thu, 15 May 2025 21:43:48 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:868e7478c67c722493268ef41b4427522279fa6a35f66461fd7adb0bf9e2c4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363329795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8621a9920839bcfdc5e9493f7408dca1bba5d13e97372f25dcb2828d0cab627`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf4c9ebe75ad00b908f5c783b4815794956bf90232cc34953f0a5744f19b699`  
		Last Modified: Thu, 22 May 2025 03:36:09 GMT  
		Size: 336.4 MB (336446987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:7a4f9ef8212aa8a7d6456c13e712c2838ea2d37473e5dc052a89f5fde72edc28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6469567669efec36515c9f38ed52cb7510dea8dc20939991a8486e11898c4ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff31c08b679c1c5a077d7a557e36813d9be82c5bbc22efbc845d709dd07bfacf`  
		Last Modified: Thu, 22 May 2025 03:36:05 GMT  
		Size: 3.8 MB (3824766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a9a671478833eaf718e74615d4a29101183eeab0898f719807cd0c3a261e6d`  
		Last Modified: Thu, 22 May 2025 03:36:04 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:989095388527710c84035fb19f851eee7c1ef3280f20885afaa3f1ca40c132a0
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
$ docker pull rust@sha256:bb40fab9222e04479fcdd45dd897df82c6ce527f1be367d7af26b9d8b0ef6a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304047247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed37a08d4804ab8dc49d922940d98831dba0a9ab0d064517c16d3e8ebc61028`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfee91a65ac6ac51500a0ec06fef619ed43fb695781fb524461a5c4d2d637da`  
		Last Modified: Wed, 21 May 2025 23:30:50 GMT  
		Size: 275.8 MB (275821917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:efe02561cb166afdf2b5ceff7aa87559a0d4305e49b91aaf2b14ecea3dfac430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98fcfc56b3317ccdbefec9a1d8a372664b2c3fcb175e2a68692eb79b093238e`

```dockerfile
```

-	Layers:
	-	`sha256:8b0b25427736858183a7036091af78fd2db2d997da37facb6e4d05aaeae085ac`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 4.0 MB (3984195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d91ce431f3e8f53deb758af58dcf2d0d526914b7e949edc4a9194ad60d84b79`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:9e29ea2079cecf087bbda1c2fd2ad61236b36515fa51c6ff29828e8720467d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.1 MB (320057803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc73805e0130280f517428c036ce3ef1b66e23f5cfc530e79e9523fff52a2da`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2affe51206b495c552876f1361055b5ba2ba5c499a12dc799182e527f88fee8f`  
		Last Modified: Fri, 16 May 2025 00:47:33 GMT  
		Size: 296.1 MB (296119729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7f307223876a0415ebe98e4232538d19ba2dfd94a4587afd1b6625bc10411268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b85b7e64240d9a4922e80471ff1f6d7ddf3fa2df0e3d30083ee3421d6afb6f`

```dockerfile
```

-	Layers:
	-	`sha256:8533123b469cd2f37a235ff4ae7f91614ee1dd9a8b02d36fd1828d5275843a82`  
		Last Modified: Fri, 16 May 2025 00:47:27 GMT  
		Size: 3.8 MB (3798367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3d2d35d257570cf330e2e8c1696e66fc0e1c593229df7b7735be317bae3977`  
		Last Modified: Fri, 16 May 2025 00:47:26 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:e42c600982c6907c6953b3067f6c48033e395f4d10181943c51ebac2f7f23bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267996219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3084e189f23691ae93614b7982a7e2cac388bca91738c5669989e7d8b796f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed633d6741d291fe9a1763e68d2cccb161b0647cba3b92db34f2082a23b9e0e5`  
		Last Modified: Thu, 15 May 2025 21:25:02 GMT  
		Size: 239.9 MB (239929597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:49d4587422ab4bfcf0173cab06c43b80c8984a7ab4c06e5735771535306cbd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4019635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ed220b85632009846640d2295c2f4ab23f854fa0b42e0c3243b5cefdd747ae`

```dockerfile
```

-	Layers:
	-	`sha256:3554280116bde06c2a965fd24a497d66881cd9d1aa281871d1b73769d8a2094d`  
		Last Modified: Thu, 15 May 2025 21:24:57 GMT  
		Size: 4.0 MB (4006212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec9148c526a826a45ec9302a772ebcdbad438372587030aeb75898a207f5529`  
		Last Modified: Thu, 15 May 2025 21:24:56 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:ba53dc2028f64403c6bd2a89614ec2e82ac8573537c865976e2cc6374ec2029b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325373122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2b704e3adfa1d07aa1cbc2987edbfeecfa1944de3fb2c3a968bd74c02ec417`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814ea34b52869e575de48c99d2f39a24d0e4d29694d8f3a01507831f57c2b06d`  
		Last Modified: Wed, 21 May 2025 23:24:41 GMT  
		Size: 296.2 MB (296165635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:889b0b25c9982cd5fd0571c6b2e686ec647c319ecab6c6d5a7adb6d0d6435a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3976779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8904643b41a0647ba565c4644b3392f328605ea998f3baade734ba5d2aacb870`

```dockerfile
```

-	Layers:
	-	`sha256:b1c6f53dcb1207b295e2a9b9c928c3d427f03fff1cda3c59d8cb153c959edd63`  
		Last Modified: Wed, 21 May 2025 23:24:35 GMT  
		Size: 4.0 MB (3963560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f37c60466f2e78fb30d52c14fbff69ffd5e0acccfafbf0eeb4d5f39c371cb4`  
		Last Modified: Wed, 21 May 2025 23:24:34 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:73839fb86f1fecdfa502eed34acc218fa19ea5b56c0c32411ea7a21108c4cd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377784662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3902494a5ed4edbc6b7649c8b67f6216b185ab73ac30aeb3191240f8c20079b2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf472daa2685f63de3e031e0501577d5082ab01e4cd68a594850d5b117971ab4`  
		Last Modified: Thu, 15 May 2025 21:44:03 GMT  
		Size: 345.7 MB (345716219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b15ebebde5337a1f5f6d3035e50b978c23924c91ade52b89e87fb0ea78553cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38b8f6da58da02263499e3598466193030911e6f0ffd21726d6f52111dd4a5c`

```dockerfile
```

-	Layers:
	-	`sha256:045d5e4d7f1b02b270f2b39f6cfdc49b5cb491134b55b9308ddaa4bf79f39391`  
		Last Modified: Thu, 15 May 2025 21:43:49 GMT  
		Size: 4.0 MB (3956177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53809675a1cc4de34fd12f811d8d666321a4623ebb988f23833edcee8fbc1ef`  
		Last Modified: Thu, 15 May 2025 21:43:48 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:868e7478c67c722493268ef41b4427522279fa6a35f66461fd7adb0bf9e2c4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363329795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8621a9920839bcfdc5e9493f7408dca1bba5d13e97372f25dcb2828d0cab627`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf4c9ebe75ad00b908f5c783b4815794956bf90232cc34953f0a5744f19b699`  
		Last Modified: Thu, 22 May 2025 03:36:09 GMT  
		Size: 336.4 MB (336446987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7a4f9ef8212aa8a7d6456c13e712c2838ea2d37473e5dc052a89f5fde72edc28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6469567669efec36515c9f38ed52cb7510dea8dc20939991a8486e11898c4ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff31c08b679c1c5a077d7a557e36813d9be82c5bbc22efbc845d709dd07bfacf`  
		Last Modified: Thu, 22 May 2025 03:36:05 GMT  
		Size: 3.8 MB (3824766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a9a671478833eaf718e74615d4a29101183eeab0898f719807cd0c3a261e6d`  
		Last Modified: Thu, 22 May 2025 03:36:04 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:7b85733174e7e5bb18d04389fe4f44c0a2421001c0fac80e9b25856fa5b077e1
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
$ docker pull rust@sha256:97b80590a20d5c2eb07da85188192a7adef3f4f312522cbfd475c7de7bd82c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295463417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d550ef0b540bad33bf2ec9fb03f2c8e364e5380cd6213c65d4878abf01f3cf67`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf3b96d50315a23a39f84e3081e1253eab321a691d742d8baa3fc48a80f9ad0`  
		Last Modified: Wed, 21 May 2025 23:30:17 GMT  
		Size: 265.2 MB (265207477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7654398afe6d9c2ada6a00ed784165dda7ea2364aeee0713ceae8da91147f90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4213039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2e800891f1055bb4074ed0d02441fe6240edc04c0a2722808deb75b744d97b`

```dockerfile
```

-	Layers:
	-	`sha256:b8eb46c3c2dba7b7825cb14a2f20554b65d85f1b7982e36530088fe6645b473f`  
		Last Modified: Wed, 21 May 2025 23:30:13 GMT  
		Size: 4.2 MB (4201683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43919c7995c8288c67859032aefa9df80e945eb0051bf122fab252d5ab8603e8`  
		Last Modified: Wed, 21 May 2025 23:30:13 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:fb46a8886b184e63725f71cecc5b4447baf825554560e49a902be80aa0be12be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.9 MB (319898121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3c8bf9b7293d122263ddcf92e437f269123360707572d092aa873ff6acfe5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a398f3fb2a84d2f55ccffe98cc554e8b7b0e593b06e480a45942a14035707d5`  
		Last Modified: Fri, 16 May 2025 00:42:53 GMT  
		Size: 294.4 MB (294355694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ddb6be6bc9d103419637c3e37d63eca143fe0f3cbc083278b2c2ab7ab1ab2feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4022345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e3a4cd59da45b8ce03653bea73bd63dac2476592a9e36a5493e1fa31d8757`

```dockerfile
```

-	Layers:
	-	`sha256:902f97b8ad9a51f2adb68f88d234da7cd55c1af152e2cbb9dd297c05ffbb61c4`  
		Last Modified: Fri, 16 May 2025 00:42:47 GMT  
		Size: 4.0 MB (4010914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f026c959c784b691edc6db6bbf65f8700a3a83d8366c5c3a5b605c9a235852`  
		Last Modified: Fri, 16 May 2025 00:42:46 GMT  
		Size: 11.4 KB (11431 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be38bf3c2d6e3a2b47825e6dd4d77cf20583eb6206683ed3b21b29a77b4da50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262677882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8f9f1aa711538c6de6c47c0267af7d5e46c3d9bdd4a57a7830ca2df5328f55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4830ced46110e2a304d2fa24aff7c40cee44a64b15cbd1602175d7528ba9dca9`  
		Last Modified: Thu, 15 May 2025 21:22:59 GMT  
		Size: 233.9 MB (233933237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7b7be60ffc119e22194697635f39ef3ecb1d40d4dcedd25ef4229bc08a999188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4210772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8fc5e814cbb7c4a39f70f39dbce6ebb5f6779ca231d8f1eb11d75367bfdd9b`

```dockerfile
```

-	Layers:
	-	`sha256:68e804f29c4c1759df1a8c3a9dcdc215b964624a74e91345ccf86bb1fa7d61de`  
		Last Modified: Thu, 15 May 2025 21:22:54 GMT  
		Size: 4.2 MB (4199312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fba59bcde4cb014edb46b31d61e90b7ae6a1d420dba63e342fab2115e5f4640`  
		Last Modified: Thu, 15 May 2025 21:22:53 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:6c6e66e31919c82fe7ea1b63e8d37f1b3b89a184a6c95c9c4a1433e39d84c8d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 MB (320512888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8dae71aa0ae8520f4e956746adc671bfb485dca203c82aa62b3d1a6a45d00c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452460d1c227bf7acc8aeb01051d54bfe06fb359bfc4c6ae3535ea37ea6e2d12`  
		Last Modified: Wed, 21 May 2025 23:24:38 GMT  
		Size: 289.3 MB (289323688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5d135ffd369ba51d29a1c421aeea4320644446c924c37fb843458a4188caca00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4202751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbdf2ab316bec0455185f0aa859a9e62785b877b4f0e81754f1f65734dc86a6`

```dockerfile
```

-	Layers:
	-	`sha256:46da1a092528e79eb79c8dfaac9bdc3cc88154152aa2ad577f97f5eedcea6360`  
		Last Modified: Wed, 21 May 2025 23:24:32 GMT  
		Size: 4.2 MB (4191427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270cf5ab3f0a6904e359a5f16f1ab8ffc19021fe328a31afce493aae98aa5bdd`  
		Last Modified: Wed, 21 May 2025 23:24:31 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87`

```console
$ docker pull rust@sha256:893a03d96de2c0e6eb8b73e24b2266264b6dee244ce997d1bae246901093ba23
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

### `rust:1.87` - linux; amd64

```console
$ docker pull rust@sha256:3d4a2ab199238d07982c4b2bd663ed9e54d135eeecbfa326a8cc73d6659a57ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553331383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed12ea880e03238fe4e68bc7e19b72fe31649a20a35874431e0e3b9ee37bfcfe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f099911d692f62b851cf49a1e93294288a115f5cd2d014180e4d3684d34ab`  
		Last Modified: Thu, 22 May 2025 00:12:38 GMT  
		Size: 211.4 MB (211362119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60122453ea09122539d0bff9dd2ace9ad0fb5f94f28106482345e871b8776f`  
		Last Modified: Thu, 22 May 2025 01:22:53 GMT  
		Size: 205.1 MB (205065526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87` - unknown; unknown

```console
$ docker pull rust@sha256:c22e4e30bdb5ca31034eb63aa448f9c77a1102d1c161ad253c2925c9fb5de7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15583659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f90206053d1f253e46155a79fb7bb6966620d44bd8a39970cae527f1f819a1f`

```dockerfile
```

-	Layers:
	-	`sha256:6353069eb27b9defe4c9f76cfe25f6f0812b36dbd10a091e3f05bc17d5e07939`  
		Last Modified: Thu, 22 May 2025 01:22:51 GMT  
		Size: 15.6 MB (15570520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36489b5c50efe5ec3b3b1a288cc4d0a9ec10bd1986b2a4bed6d14eeb6f342209`  
		Last Modified: Thu, 22 May 2025 01:22:50 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87` - linux; arm variant v7

```console
$ docker pull rust@sha256:a717a4a677877e4c90506d6094ba956c65c8acbb675322e10051e026b84ac7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549353893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c15507a70a72169329e3fb52a9e9f8e6fda428fc8a10c673722a27ad87d7517`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Mon, 28 Apr 2025 21:15:27 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Tue, 29 Apr 2025 03:37:10 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3553b1499305feec4f182c1e2562e06daaecb3dc337d83b89b8c909f46c0a1`  
		Last Modified: Tue, 29 Apr 2025 13:22:56 GMT  
		Size: 59.6 MB (59640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d55cc6c59023a65c15579520e32553ab9f1e2d6377e8e4dd69393e113713d3`  
		Last Modified: Tue, 29 Apr 2025 16:44:12 GMT  
		Size: 175.3 MB (175316182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae6506bd78c8b0409ae60f919fcf0308fadded07bb677e52eaca831e32f27e4`  
		Last Modified: Fri, 16 May 2025 00:45:12 GMT  
		Size: 248.3 MB (248282041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87` - unknown; unknown

```console
$ docker pull rust@sha256:704762edf7170410c4143b57dc2c2592340918185bbd978e992015426067433c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15387590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118ae28de64f563725129ee9df3f3efdfd56f98689b846a2020a59babcd3a5a3`

```dockerfile
```

-	Layers:
	-	`sha256:0ed13d7d744dbbbcbf9675297a7a1707dc0b984f5b19f5a792be6856c23b4237`  
		Last Modified: Fri, 16 May 2025 00:45:09 GMT  
		Size: 15.4 MB (15374344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cc69fc971f6f9022f452d055c879d015b21e562a7728564f74f09f10c9bf7f`  
		Last Modified: Fri, 16 May 2025 00:45:06 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:79638f277b74a79352c910c6479b5cb8c25b0f2ef2b11af4b7f2d63a04bbe78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513058250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facc597070c63677b4fc7121846c580a1ee5f055d749af0856a73fc113dc99e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Tue, 29 Apr 2025 18:37:11 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d41c7623f41e51939686bf861fe89538ae4dc84481ff4136b55524e770d2603`  
		Last Modified: Wed, 30 Apr 2025 02:16:31 GMT  
		Size: 202.7 MB (202748227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2789ce74abfb6ada85cef976765f28a31f0d76101d35d89fe6f30e6a160f5cf7`  
		Last Modified: Thu, 15 May 2025 21:23:55 GMT  
		Size: 174.1 MB (174082434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87` - unknown; unknown

```console
$ docker pull rust@sha256:f7f0b6b46806bffe1c5d2161f9299dc0a9238fefa3183278ae6109c67595d89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15613623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79ce7216bf86b5ea593af61df25f8acf8b9a077a234befe5f780ee67da136ae`

```dockerfile
```

-	Layers:
	-	`sha256:00c23c1dc907f8d220ac1ef9c18b98380d358000cb5edabb21556f1ece3cc7ec`  
		Last Modified: Thu, 15 May 2025 21:23:51 GMT  
		Size: 15.6 MB (15600332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e5ccf8415d9f8e96f788c503d732dfce14045f3ba24d8366c936bf8762ef8`  
		Last Modified: Thu, 15 May 2025 21:23:50 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87` - linux; 386

```console
$ docker pull rust@sha256:d1548c29f4a54233ce3663dbf31e24697f803f2eaa51dc48517fc374e605cd53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579410243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599b9672494cb7a24c90726f5649fd8bb62e266686d6c92c3a70db98df8fb36a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Wed, 21 May 2025 23:20:06 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8c7f8292580c2c70e8cb47ec957249f0882ee6ee3737bf3250e44650a38db`  
		Last Modified: Wed, 21 May 2025 23:37:30 GMT  
		Size: 66.2 MB (66224115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e426a3a2617e34e93d75e9b5c79113e976623e3633255f578a7087d4221ba47`  
		Last Modified: Thu, 22 May 2025 00:12:45 GMT  
		Size: 210.3 MB (210303724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e15432acb4bbafe1b177dc4d3a8a7616460a38e03b58bf34ad9f8a4e54f229`  
		Last Modified: Thu, 22 May 2025 01:21:36 GMT  
		Size: 228.6 MB (228555174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87` - unknown; unknown

```console
$ docker pull rust@sha256:626889100874bfa993f52c41bf9e48649fc7b964c1dd889884eb3b1f106ed47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a19fecc316543561006e19323c1d5f88ff6b410323def3f15d858f5152634a`

```dockerfile
```

-	Layers:
	-	`sha256:d5613f30992ef58d04da59a0c3fc9df18e23a6aea5ddc9094597440de2585099`  
		Last Modified: Thu, 22 May 2025 01:21:31 GMT  
		Size: 15.5 MB (15547420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ffe58d9c1f399bf6345b1eae0a9b2681b28358b08f9b7a3333ff32c090bcda`  
		Last Modified: Thu, 22 May 2025 01:21:30 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87` - linux; ppc64le

```console
$ docker pull rust@sha256:edad25bbea95469efae8b7575e3621376e99cdac3e8dc847e12990d79ffa15e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639187573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf09d1faa6098d8816d94f3129d858a3c9895d7ccb9d5f8c7510120d86649501`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Tue, 29 Apr 2025 07:46:58 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Tue, 29 Apr 2025 08:29:00 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f7f895e65e8530bee082db2e14aefaa34547b4753e60990faca2b691714e63`  
		Last Modified: Tue, 29 Apr 2025 09:10:46 GMT  
		Size: 214.4 MB (214409240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f771a754d3f6d9880020eef886dee95dbbc411da896e8d6188ce4b35d1ccea1`  
		Last Modified: Thu, 15 May 2025 21:41:17 GMT  
		Size: 277.0 MB (276955667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87` - unknown; unknown

```console
$ docker pull rust@sha256:25e42159bf1ae8fed15f948468f0850e56728c647b8dc63fc1178c7946f65a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b8b744207f149e1825389c70977eaaa027331392f4bb1af2cf53edda9e7348`

```dockerfile
```

-	Layers:
	-	`sha256:1261dadc28c70b94878106245907b72b29ecaecd634cf88ba53927741da602e3`  
		Last Modified: Thu, 15 May 2025 21:40:56 GMT  
		Size: 15.5 MB (15546986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43db0b6c0fb41e034652a717f321ad57ef840725dc6ecbddbb455e4ba85b36da`  
		Last Modified: Thu, 15 May 2025 21:40:55 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87` - linux; s390x

```console
$ docker pull rust@sha256:a46b263c2cce2b762d073f453a72c33eb474d71183208ed22ebccb7841b9309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604372811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cc62b570c4d03e5e28a7b9abaeec07a8d1a0681c67877cdd087f829e8b5543`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Tue, 29 Apr 2025 00:01:21 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Tue, 29 Apr 2025 02:58:48 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfe8bd3e826ba76e4ad73b0a5ce638276af95b860bec9b25c2754c5600c5a61`  
		Last Modified: Tue, 29 Apr 2025 05:34:00 GMT  
		Size: 183.4 MB (183405963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589f590c508c398e3740adc2dd1d0915bdc9a36f36693dacb7d2cb83012bcca1`  
		Last Modified: Thu, 15 May 2025 23:34:36 GMT  
		Size: 286.3 MB (286310328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87` - unknown; unknown

```console
$ docker pull rust@sha256:0bb2f2b59196707a888cfccbc092b473f6e382739d12c2db5d9117cd4f490b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15395439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61693f885fe5810811eb46994aa1af308f091912dc96214dad8fd6651bc00831`

```dockerfile
```

-	Layers:
	-	`sha256:011ca34cbff4dd90ea475c3878d26371312698ea04d43f7886f8598f7f924610`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 15.4 MB (15382300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4311afc8d95a09e62d7f51e2603140152c818532e8aa83db3b1545ef3d7a15`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87-alpine`

```console
$ docker pull rust@sha256:fa7c28576553c431224a85c897c38f3a6443bd831be37061ab3560d9e797dc82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.87-alpine` - linux; amd64

```console
$ docker pull rust@sha256:77b6339cdb0832ad483e0d6389c4c6df605568e9c2f1a14fe76dd3b3cd3cd023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324247403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ffcf6a0b7e66d9cf8d858d524ebcd49bb36208a8c8d449ab6a1927df31f7b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b343ca42d769a088aad30a06435916be946b7bd77c275c4c48aa9c02d07ebc6`  
		Last Modified: Thu, 15 May 2025 18:37:40 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0312ddedcb8a05877b03a2214ddd4942d87d6bd8684a5f5bc0353f72d76def`  
		Last Modified: Thu, 15 May 2025 18:37:44 GMT  
		Size: 259.0 MB (259040344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:4e64c00b2317960a70850f4400db745c6cfb2bdd9f3d125aa41eae29aa6db0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.7 KB (795741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60b54f74613b5e61b7293457c23a015874a512e095a95d91dfbad52ebb043b4`

```dockerfile
```

-	Layers:
	-	`sha256:a5a1184050fab9829a713a4d20d0725d4538c6e742e9839d6591249330d5359e`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 783.8 KB (783823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05e06b11fae76f35a913f94980f7b264abfa081dffa29929dd773c6969a089d`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c46257a5086c247e6cf7f47f0b1bfd6829b0487f60ba421e09dc869a1cf8854e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 MB (326998595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4173638e4c107fec82a3872cebbc9896730ad56739846f1cab5b2d2a6662d444`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a8d04fc53dbb480e66cf7321229cda858c75a9bfa488474aabc6a3fbc3423`  
		Last Modified: Mon, 05 May 2025 22:59:43 GMT  
		Size: 59.1 MB (59101363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd10981d51d5c4342a74b76870500712f6977bafb0891f69b5b725cd3f83575b`  
		Last Modified: Thu, 15 May 2025 21:52:00 GMT  
		Size: 263.9 MB (263904203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:34672929840929fdaeda033ca2f79184da7ad0a5f4ca4c5afc3d17ab43dceceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.5 KB (875494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c7d1faabdd527c0adb51cec9eac15ffbf9a2ad32dd7bad9fd10768aef390ae`

```dockerfile
```

-	Layers:
	-	`sha256:5fad1a9258bc9e5e8818e557ec0496368c72e4184380ef235dc4bb26a03a6e03`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 863.4 KB (863409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4799a729390389da9955e76bdba397218c8fff4138d88735449c1364a6120788`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87-alpine3.20`

```console
$ docker pull rust@sha256:126b44382fa926ce41eecac3ef4628de508f0df8556fe43e8d64cdcd1cbbe40b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.87-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:a6e21abdf25464282e9ebe77b75a597cbd0b21d375eafa86c38af1e1cb8a2d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.0 MB (317984256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69198b701be7dc50b960f31ef7f4fd2764b266e2d8adaa0bab88ab59ce2b2bf6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718715b3cbe3b4fd9094909206504e5958585bd739a34dc4fb5b7f6ed2131b8`  
		Last Modified: Thu, 15 May 2025 18:37:42 GMT  
		Size: 55.3 MB (55315586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeb4a9d8a98d7b7dadf2be0b1943267d81b081cb2fb12a85484c6aaadf235fb`  
		Last Modified: Thu, 15 May 2025 18:37:48 GMT  
		Size: 259.0 MB (259041773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:279079ce7141a696c62912e2b546d3b1db80da36385b8291b96bd87b06a333ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.5 KB (722503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f9514c3a9ca96fa531c453a6086450f8357d88a8602759b77fade775484d62`

```dockerfile
```

-	Layers:
	-	`sha256:7ef4df00128cf574a18437ccce5e6d348c5ac96f9e656076475640bc336b72b8`  
		Last Modified: Thu, 15 May 2025 18:37:41 GMT  
		Size: 711.8 KB (711789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a9394ddea85fc3e016d5927f8ce6a38638e7c7eeea1996460a0e68f6915e5c6`  
		Last Modified: Thu, 15 May 2025 18:37:40 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2881015e0b8d0d3e45e40cf26cedbea750dc4e4bae1f9492ea6ea20c3c478296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320946007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f9aeec89829426e53d9ec2993f49c4e8add3c62bbb31e1a8833ca8f6bba7b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c6aa5430354637d99185e3c6f997bb89b34d0340d714c59489470f3b28fb00`  
		Last Modified: Mon, 05 May 2025 22:58:37 GMT  
		Size: 53.0 MB (52950277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d7b743d7f5864c65b2894547a9334b33385928622ae90e6a32c6e8856c668`  
		Last Modified: Thu, 15 May 2025 21:26:08 GMT  
		Size: 263.9 MB (263904565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:b8cb278c3d3464f502ef0c4e303cc516cf61210f397481f3f916b0efd803552e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0465991995a77f18ceff0792501f873542ee79e340b0bc4e6a168e2d55cf0cfb`

```dockerfile
```

-	Layers:
	-	`sha256:13318289bd5cbf3b293bd9e48b8d9dfb9679941c1b10fefc888f757d08695f98`  
		Last Modified: Thu, 15 May 2025 21:26:00 GMT  
		Size: 747.7 KB (747721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5df0c715639e649fb2f087e25e05ab1d51803c9e80193b7ded83d66aa0f06e`  
		Last Modified: Thu, 15 May 2025 21:25:59 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87-alpine3.21`

```console
$ docker pull rust@sha256:fa7c28576553c431224a85c897c38f3a6443bd831be37061ab3560d9e797dc82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.87-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:77b6339cdb0832ad483e0d6389c4c6df605568e9c2f1a14fe76dd3b3cd3cd023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324247403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ffcf6a0b7e66d9cf8d858d524ebcd49bb36208a8c8d449ab6a1927df31f7b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b343ca42d769a088aad30a06435916be946b7bd77c275c4c48aa9c02d07ebc6`  
		Last Modified: Thu, 15 May 2025 18:37:40 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0312ddedcb8a05877b03a2214ddd4942d87d6bd8684a5f5bc0353f72d76def`  
		Last Modified: Thu, 15 May 2025 18:37:44 GMT  
		Size: 259.0 MB (259040344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:4e64c00b2317960a70850f4400db745c6cfb2bdd9f3d125aa41eae29aa6db0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.7 KB (795741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60b54f74613b5e61b7293457c23a015874a512e095a95d91dfbad52ebb043b4`

```dockerfile
```

-	Layers:
	-	`sha256:a5a1184050fab9829a713a4d20d0725d4538c6e742e9839d6591249330d5359e`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 783.8 KB (783823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05e06b11fae76f35a913f94980f7b264abfa081dffa29929dd773c6969a089d`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c46257a5086c247e6cf7f47f0b1bfd6829b0487f60ba421e09dc869a1cf8854e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 MB (326998595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4173638e4c107fec82a3872cebbc9896730ad56739846f1cab5b2d2a6662d444`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a8d04fc53dbb480e66cf7321229cda858c75a9bfa488474aabc6a3fbc3423`  
		Last Modified: Mon, 05 May 2025 22:59:43 GMT  
		Size: 59.1 MB (59101363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd10981d51d5c4342a74b76870500712f6977bafb0891f69b5b725cd3f83575b`  
		Last Modified: Thu, 15 May 2025 21:52:00 GMT  
		Size: 263.9 MB (263904203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:34672929840929fdaeda033ca2f79184da7ad0a5f4ca4c5afc3d17ab43dceceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.5 KB (875494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c7d1faabdd527c0adb51cec9eac15ffbf9a2ad32dd7bad9fd10768aef390ae`

```dockerfile
```

-	Layers:
	-	`sha256:5fad1a9258bc9e5e8818e557ec0496368c72e4184380ef235dc4bb26a03a6e03`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 863.4 KB (863409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4799a729390389da9955e76bdba397218c8fff4138d88735449c1364a6120788`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87-bookworm`

```console
$ docker pull rust@sha256:893a03d96de2c0e6eb8b73e24b2266264b6dee244ce997d1bae246901093ba23
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

### `rust:1.87-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:3d4a2ab199238d07982c4b2bd663ed9e54d135eeecbfa326a8cc73d6659a57ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553331383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed12ea880e03238fe4e68bc7e19b72fe31649a20a35874431e0e3b9ee37bfcfe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f099911d692f62b851cf49a1e93294288a115f5cd2d014180e4d3684d34ab`  
		Last Modified: Thu, 22 May 2025 00:12:38 GMT  
		Size: 211.4 MB (211362119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60122453ea09122539d0bff9dd2ace9ad0fb5f94f28106482345e871b8776f`  
		Last Modified: Thu, 22 May 2025 01:22:53 GMT  
		Size: 205.1 MB (205065526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c22e4e30bdb5ca31034eb63aa448f9c77a1102d1c161ad253c2925c9fb5de7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15583659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f90206053d1f253e46155a79fb7bb6966620d44bd8a39970cae527f1f819a1f`

```dockerfile
```

-	Layers:
	-	`sha256:6353069eb27b9defe4c9f76cfe25f6f0812b36dbd10a091e3f05bc17d5e07939`  
		Last Modified: Thu, 22 May 2025 01:22:51 GMT  
		Size: 15.6 MB (15570520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36489b5c50efe5ec3b3b1a288cc4d0a9ec10bd1986b2a4bed6d14eeb6f342209`  
		Last Modified: Thu, 22 May 2025 01:22:50 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:a717a4a677877e4c90506d6094ba956c65c8acbb675322e10051e026b84ac7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549353893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c15507a70a72169329e3fb52a9e9f8e6fda428fc8a10c673722a27ad87d7517`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Mon, 28 Apr 2025 21:15:27 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Tue, 29 Apr 2025 03:37:10 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3553b1499305feec4f182c1e2562e06daaecb3dc337d83b89b8c909f46c0a1`  
		Last Modified: Tue, 29 Apr 2025 13:22:56 GMT  
		Size: 59.6 MB (59640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d55cc6c59023a65c15579520e32553ab9f1e2d6377e8e4dd69393e113713d3`  
		Last Modified: Tue, 29 Apr 2025 16:44:12 GMT  
		Size: 175.3 MB (175316182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae6506bd78c8b0409ae60f919fcf0308fadded07bb677e52eaca831e32f27e4`  
		Last Modified: Fri, 16 May 2025 00:45:12 GMT  
		Size: 248.3 MB (248282041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:704762edf7170410c4143b57dc2c2592340918185bbd978e992015426067433c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15387590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118ae28de64f563725129ee9df3f3efdfd56f98689b846a2020a59babcd3a5a3`

```dockerfile
```

-	Layers:
	-	`sha256:0ed13d7d744dbbbcbf9675297a7a1707dc0b984f5b19f5a792be6856c23b4237`  
		Last Modified: Fri, 16 May 2025 00:45:09 GMT  
		Size: 15.4 MB (15374344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cc69fc971f6f9022f452d055c879d015b21e562a7728564f74f09f10c9bf7f`  
		Last Modified: Fri, 16 May 2025 00:45:06 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:79638f277b74a79352c910c6479b5cb8c25b0f2ef2b11af4b7f2d63a04bbe78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513058250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facc597070c63677b4fc7121846c580a1ee5f055d749af0856a73fc113dc99e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Tue, 29 Apr 2025 18:37:11 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d41c7623f41e51939686bf861fe89538ae4dc84481ff4136b55524e770d2603`  
		Last Modified: Wed, 30 Apr 2025 02:16:31 GMT  
		Size: 202.7 MB (202748227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2789ce74abfb6ada85cef976765f28a31f0d76101d35d89fe6f30e6a160f5cf7`  
		Last Modified: Thu, 15 May 2025 21:23:55 GMT  
		Size: 174.1 MB (174082434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f7f0b6b46806bffe1c5d2161f9299dc0a9238fefa3183278ae6109c67595d89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15613623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79ce7216bf86b5ea593af61df25f8acf8b9a077a234befe5f780ee67da136ae`

```dockerfile
```

-	Layers:
	-	`sha256:00c23c1dc907f8d220ac1ef9c18b98380d358000cb5edabb21556f1ece3cc7ec`  
		Last Modified: Thu, 15 May 2025 21:23:51 GMT  
		Size: 15.6 MB (15600332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e5ccf8415d9f8e96f788c503d732dfce14045f3ba24d8366c936bf8762ef8`  
		Last Modified: Thu, 15 May 2025 21:23:50 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bookworm` - linux; 386

```console
$ docker pull rust@sha256:d1548c29f4a54233ce3663dbf31e24697f803f2eaa51dc48517fc374e605cd53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579410243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599b9672494cb7a24c90726f5649fd8bb62e266686d6c92c3a70db98df8fb36a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Wed, 21 May 2025 23:20:06 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8c7f8292580c2c70e8cb47ec957249f0882ee6ee3737bf3250e44650a38db`  
		Last Modified: Wed, 21 May 2025 23:37:30 GMT  
		Size: 66.2 MB (66224115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e426a3a2617e34e93d75e9b5c79113e976623e3633255f578a7087d4221ba47`  
		Last Modified: Thu, 22 May 2025 00:12:45 GMT  
		Size: 210.3 MB (210303724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e15432acb4bbafe1b177dc4d3a8a7616460a38e03b58bf34ad9f8a4e54f229`  
		Last Modified: Thu, 22 May 2025 01:21:36 GMT  
		Size: 228.6 MB (228555174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:626889100874bfa993f52c41bf9e48649fc7b964c1dd889884eb3b1f106ed47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a19fecc316543561006e19323c1d5f88ff6b410323def3f15d858f5152634a`

```dockerfile
```

-	Layers:
	-	`sha256:d5613f30992ef58d04da59a0c3fc9df18e23a6aea5ddc9094597440de2585099`  
		Last Modified: Thu, 22 May 2025 01:21:31 GMT  
		Size: 15.5 MB (15547420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ffe58d9c1f399bf6345b1eae0a9b2681b28358b08f9b7a3333ff32c090bcda`  
		Last Modified: Thu, 22 May 2025 01:21:30 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:edad25bbea95469efae8b7575e3621376e99cdac3e8dc847e12990d79ffa15e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639187573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf09d1faa6098d8816d94f3129d858a3c9895d7ccb9d5f8c7510120d86649501`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Tue, 29 Apr 2025 07:46:58 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Tue, 29 Apr 2025 08:29:00 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f7f895e65e8530bee082db2e14aefaa34547b4753e60990faca2b691714e63`  
		Last Modified: Tue, 29 Apr 2025 09:10:46 GMT  
		Size: 214.4 MB (214409240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f771a754d3f6d9880020eef886dee95dbbc411da896e8d6188ce4b35d1ccea1`  
		Last Modified: Thu, 15 May 2025 21:41:17 GMT  
		Size: 277.0 MB (276955667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:25e42159bf1ae8fed15f948468f0850e56728c647b8dc63fc1178c7946f65a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b8b744207f149e1825389c70977eaaa027331392f4bb1af2cf53edda9e7348`

```dockerfile
```

-	Layers:
	-	`sha256:1261dadc28c70b94878106245907b72b29ecaecd634cf88ba53927741da602e3`  
		Last Modified: Thu, 15 May 2025 21:40:56 GMT  
		Size: 15.5 MB (15546986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43db0b6c0fb41e034652a717f321ad57ef840725dc6ecbddbb455e4ba85b36da`  
		Last Modified: Thu, 15 May 2025 21:40:55 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:a46b263c2cce2b762d073f453a72c33eb474d71183208ed22ebccb7841b9309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604372811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cc62b570c4d03e5e28a7b9abaeec07a8d1a0681c67877cdd087f829e8b5543`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Tue, 29 Apr 2025 00:01:21 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Tue, 29 Apr 2025 02:58:48 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfe8bd3e826ba76e4ad73b0a5ce638276af95b860bec9b25c2754c5600c5a61`  
		Last Modified: Tue, 29 Apr 2025 05:34:00 GMT  
		Size: 183.4 MB (183405963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589f590c508c398e3740adc2dd1d0915bdc9a36f36693dacb7d2cb83012bcca1`  
		Last Modified: Thu, 15 May 2025 23:34:36 GMT  
		Size: 286.3 MB (286310328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0bb2f2b59196707a888cfccbc092b473f6e382739d12c2db5d9117cd4f490b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15395439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61693f885fe5810811eb46994aa1af308f091912dc96214dad8fd6651bc00831`

```dockerfile
```

-	Layers:
	-	`sha256:011ca34cbff4dd90ea475c3878d26371312698ea04d43f7886f8598f7f924610`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 15.4 MB (15382300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4311afc8d95a09e62d7f51e2603140152c818532e8aa83db3b1545ef3d7a15`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87-bullseye`

```console
$ docker pull rust@sha256:51f2d8c9d5c6c2506765a1f9e17c8ebc33aded193deffa72356a337ca396255a
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

### `rust:1.87-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:0b451f05a606a3b41c9a864500a9c50f9886a9aeb8c563d1b7ce1cf1bda5e56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526472326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bf6dd7679501c4f32309849fca9c4030a99afef60deb99454ca0ec09b18262`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Wed, 21 May 2025 23:20:29 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69a02035012d2783a66ac7ecc549af09c1718d81affa5f9c39abcf969da971`  
		Last Modified: Wed, 21 May 2025 23:37:39 GMT  
		Size: 54.8 MB (54757308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94932625c5ab18ebb7640ecd70dd33061ba90cc7666b7ff06042a8bd7cf63fb`  
		Last Modified: Thu, 22 May 2025 00:12:38 GMT  
		Size: 197.1 MB (197133895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f7643072d1ada9eba65bdb4a38d74d4c1a9411d53739374cd72e0419954af6`  
		Last Modified: Thu, 22 May 2025 01:22:46 GMT  
		Size: 205.1 MB (205066054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:73be1b1016ce85742cea899179b3476659dae35179498a4a4c22bda005e6fd13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15186206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dd4e66e59d674615efab4283c43eb93a71f55d7f04c60a4770da8c927e6a7a`

```dockerfile
```

-	Layers:
	-	`sha256:42e2775ff89b0e1ca092e8b334f36270b1c16e46d0b4457d9bd59a09a0b61499`  
		Last Modified: Thu, 22 May 2025 01:22:43 GMT  
		Size: 15.2 MB (15174957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954ef5cd1b91201a29c71b2b2d32806e4c10fcfd2bacb9671a09bf86b7820f49`  
		Last Modified: Thu, 22 May 2025 01:22:43 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:d7d4f233403022183f2af37fd51898a1d97b78dbed910fe576277af94e82d87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.4 MB (530385150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd03e62aeebdd1f83bdc094079d1c37453a5be372a0b838c1aecb8029ef3654`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Mon, 28 Apr 2025 21:16:06 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Tue, 29 Apr 2025 03:37:44 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4cecedb434598f97e33a3320b6af6e1676388e6c13b31f0aab4b7c9372012`  
		Last Modified: Tue, 29 Apr 2025 13:23:50 GMT  
		Size: 50.6 MB (50625161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce34362265f33a06975f249d19b3ebf3e131e052b1333868e863a53ee816bc45`  
		Last Modified: Tue, 29 Apr 2025 16:46:09 GMT  
		Size: 167.6 MB (167558886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9539bd9006e9f246574a8c2d9f897d10b5c6813afbfee941acec16d2754a253`  
		Last Modified: Fri, 16 May 2025 00:40:56 GMT  
		Size: 248.3 MB (248282029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:132febdf611c5e84d3d37871ca0910429259ce6b4d1deae9b87f53877127b12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14985623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c231e250c4ae7852218bf793df0bff4ce8abb50ba96b3716aea288f555f2b9a5`

```dockerfile
```

-	Layers:
	-	`sha256:abc988d1691a81eb6a0aa6a62af1d62907119d597c4ba544006f95b4fbf04e4c`  
		Last Modified: Fri, 16 May 2025 00:40:50 GMT  
		Size: 15.0 MB (14974298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d8d1c4bd3d1fa595a076fd516f16ff496c0d1db3b0bcf0e1585088e674aebf9`  
		Last Modified: Fri, 16 May 2025 00:40:50 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:237790655bcd54abab4c49c48259af2dd699173335de4e955048c62ddb2a3146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486950939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172df5659cc3f650a81e372d4074c690126a29a4b8873fdab84f99d05ddb3b6f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Tue, 29 Apr 2025 01:47:13 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Tue, 29 Apr 2025 18:37:49 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356545a2ed16b26897f2a271b3f4a7d7e64a9bf9bc0c78fdf4f1386401e37428`  
		Last Modified: Wed, 30 Apr 2025 02:18:06 GMT  
		Size: 190.0 MB (190024328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98136a9af2cf6c7fbc2743af98d832e725438a68b83e340d2dae7eaf7e34c4b4`  
		Last Modified: Thu, 15 May 2025 21:21:52 GMT  
		Size: 174.1 MB (174081523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:837bb4c602d1047b0f2f89e25c244920e3bae19537f888475e7494b23b57334a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce05b2083a6cd6c1338f72b13b1b2f39104bb810013782bd93110d997e51a630`

```dockerfile
```

-	Layers:
	-	`sha256:928ea9471f7f3720e5182302bc720fcc69c8958c677a45ae48ee625d81f5a9cb`  
		Last Modified: Thu, 15 May 2025 21:21:44 GMT  
		Size: 15.2 MB (15176927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fad39b7b7530b615cc7f2c4f42a809573b4e4e41b9423f8b02afdc2f31d3495a`  
		Last Modified: Thu, 15 May 2025 21:21:43 GMT  
		Size: 11.4 KB (11352 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bullseye` - linux; 386

```console
$ docker pull rust@sha256:ae9554cbdf2ce6d8c237cf2e62fd8da4d3e7df981bf95d72dfb02636102a0223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555598704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7804a77f872b7bebd7c0c219c30213b20ee8e554d9e5fac9bb4cbb19e7738672`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde5c2ebb13d7ca154f5cc8b4e26e7e3a669b8bac689ec15851b65e299a0fd6`  
		Last Modified: Wed, 21 May 2025 23:19:38 GMT  
		Size: 16.3 MB (16268487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e052669a7dd77fed659f1b6d3fcf5171929214e8821aaf28744160fb71f4f1`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 56.0 MB (56049779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f06bdedcf2f8fa5a0d52d346902f8aceec74013af364956265940521230002`  
		Last Modified: Thu, 22 May 2025 00:13:14 GMT  
		Size: 200.0 MB (200039337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fee6831b1ed84af5ee781297e8478225fc1f1ccd5f724ec9187d1041829c86f`  
		Last Modified: Thu, 22 May 2025 01:21:26 GMT  
		Size: 228.6 MB (228555319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:99cd576357e873f7fc20c2b9a3a22e4305a969e9fc11165246cc866b8ddb5140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15172877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c047e879fdd094e6ee7ea60daeadb0ab59443f0c260184750cf5bb5a7c5c6022`

```dockerfile
```

-	Layers:
	-	`sha256:598d23bd2066f74b5b66e8e4d84a9eed0971a6998849692f35e8eb929c9570ec`  
		Last Modified: Thu, 22 May 2025 01:21:21 GMT  
		Size: 15.2 MB (15161661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f759815be291285c72b5589321a35711ca79f0ac7a669df83b713ceef6a54b26`  
		Last Modified: Thu, 22 May 2025 01:21:21 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87-slim`

```console
$ docker pull rust@sha256:989095388527710c84035fb19f851eee7c1ef3280f20885afaa3f1ca40c132a0
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

### `rust:1.87-slim` - linux; amd64

```console
$ docker pull rust@sha256:bb40fab9222e04479fcdd45dd897df82c6ce527f1be367d7af26b9d8b0ef6a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304047247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed37a08d4804ab8dc49d922940d98831dba0a9ab0d064517c16d3e8ebc61028`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfee91a65ac6ac51500a0ec06fef619ed43fb695781fb524461a5c4d2d637da`  
		Last Modified: Wed, 21 May 2025 23:30:50 GMT  
		Size: 275.8 MB (275821917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim` - unknown; unknown

```console
$ docker pull rust@sha256:efe02561cb166afdf2b5ceff7aa87559a0d4305e49b91aaf2b14ecea3dfac430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98fcfc56b3317ccdbefec9a1d8a372664b2c3fcb175e2a68692eb79b093238e`

```dockerfile
```

-	Layers:
	-	`sha256:8b0b25427736858183a7036091af78fd2db2d997da37facb6e4d05aaeae085ac`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 4.0 MB (3984195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d91ce431f3e8f53deb758af58dcf2d0d526914b7e949edc4a9194ad60d84b79`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:9e29ea2079cecf087bbda1c2fd2ad61236b36515fa51c6ff29828e8720467d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.1 MB (320057803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc73805e0130280f517428c036ce3ef1b66e23f5cfc530e79e9523fff52a2da`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2affe51206b495c552876f1361055b5ba2ba5c499a12dc799182e527f88fee8f`  
		Last Modified: Fri, 16 May 2025 00:47:33 GMT  
		Size: 296.1 MB (296119729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim` - unknown; unknown

```console
$ docker pull rust@sha256:7f307223876a0415ebe98e4232538d19ba2dfd94a4587afd1b6625bc10411268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b85b7e64240d9a4922e80471ff1f6d7ddf3fa2df0e3d30083ee3421d6afb6f`

```dockerfile
```

-	Layers:
	-	`sha256:8533123b469cd2f37a235ff4ae7f91614ee1dd9a8b02d36fd1828d5275843a82`  
		Last Modified: Fri, 16 May 2025 00:47:27 GMT  
		Size: 3.8 MB (3798367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3d2d35d257570cf330e2e8c1696e66fc0e1c593229df7b7735be317bae3977`  
		Last Modified: Fri, 16 May 2025 00:47:26 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:e42c600982c6907c6953b3067f6c48033e395f4d10181943c51ebac2f7f23bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267996219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3084e189f23691ae93614b7982a7e2cac388bca91738c5669989e7d8b796f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed633d6741d291fe9a1763e68d2cccb161b0647cba3b92db34f2082a23b9e0e5`  
		Last Modified: Thu, 15 May 2025 21:25:02 GMT  
		Size: 239.9 MB (239929597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim` - unknown; unknown

```console
$ docker pull rust@sha256:49d4587422ab4bfcf0173cab06c43b80c8984a7ab4c06e5735771535306cbd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4019635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ed220b85632009846640d2295c2f4ab23f854fa0b42e0c3243b5cefdd747ae`

```dockerfile
```

-	Layers:
	-	`sha256:3554280116bde06c2a965fd24a497d66881cd9d1aa281871d1b73769d8a2094d`  
		Last Modified: Thu, 15 May 2025 21:24:57 GMT  
		Size: 4.0 MB (4006212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec9148c526a826a45ec9302a772ebcdbad438372587030aeb75898a207f5529`  
		Last Modified: Thu, 15 May 2025 21:24:56 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim` - linux; 386

```console
$ docker pull rust@sha256:ba53dc2028f64403c6bd2a89614ec2e82ac8573537c865976e2cc6374ec2029b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325373122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2b704e3adfa1d07aa1cbc2987edbfeecfa1944de3fb2c3a968bd74c02ec417`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814ea34b52869e575de48c99d2f39a24d0e4d29694d8f3a01507831f57c2b06d`  
		Last Modified: Wed, 21 May 2025 23:24:41 GMT  
		Size: 296.2 MB (296165635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim` - unknown; unknown

```console
$ docker pull rust@sha256:889b0b25c9982cd5fd0571c6b2e686ec647c319ecab6c6d5a7adb6d0d6435a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3976779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8904643b41a0647ba565c4644b3392f328605ea998f3baade734ba5d2aacb870`

```dockerfile
```

-	Layers:
	-	`sha256:b1c6f53dcb1207b295e2a9b9c928c3d427f03fff1cda3c59d8cb153c959edd63`  
		Last Modified: Wed, 21 May 2025 23:24:35 GMT  
		Size: 4.0 MB (3963560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f37c60466f2e78fb30d52c14fbff69ffd5e0acccfafbf0eeb4d5f39c371cb4`  
		Last Modified: Wed, 21 May 2025 23:24:34 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:73839fb86f1fecdfa502eed34acc218fa19ea5b56c0c32411ea7a21108c4cd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377784662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3902494a5ed4edbc6b7649c8b67f6216b185ab73ac30aeb3191240f8c20079b2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf472daa2685f63de3e031e0501577d5082ab01e4cd68a594850d5b117971ab4`  
		Last Modified: Thu, 15 May 2025 21:44:03 GMT  
		Size: 345.7 MB (345716219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b15ebebde5337a1f5f6d3035e50b978c23924c91ade52b89e87fb0ea78553cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38b8f6da58da02263499e3598466193030911e6f0ffd21726d6f52111dd4a5c`

```dockerfile
```

-	Layers:
	-	`sha256:045d5e4d7f1b02b270f2b39f6cfdc49b5cb491134b55b9308ddaa4bf79f39391`  
		Last Modified: Thu, 15 May 2025 21:43:49 GMT  
		Size: 4.0 MB (3956177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53809675a1cc4de34fd12f811d8d666321a4623ebb988f23833edcee8fbc1ef`  
		Last Modified: Thu, 15 May 2025 21:43:48 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim` - linux; s390x

```console
$ docker pull rust@sha256:868e7478c67c722493268ef41b4427522279fa6a35f66461fd7adb0bf9e2c4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363329795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8621a9920839bcfdc5e9493f7408dca1bba5d13e97372f25dcb2828d0cab627`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf4c9ebe75ad00b908f5c783b4815794956bf90232cc34953f0a5744f19b699`  
		Last Modified: Thu, 22 May 2025 03:36:09 GMT  
		Size: 336.4 MB (336446987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim` - unknown; unknown

```console
$ docker pull rust@sha256:7a4f9ef8212aa8a7d6456c13e712c2838ea2d37473e5dc052a89f5fde72edc28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6469567669efec36515c9f38ed52cb7510dea8dc20939991a8486e11898c4ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff31c08b679c1c5a077d7a557e36813d9be82c5bbc22efbc845d709dd07bfacf`  
		Last Modified: Thu, 22 May 2025 03:36:05 GMT  
		Size: 3.8 MB (3824766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a9a671478833eaf718e74615d4a29101183eeab0898f719807cd0c3a261e6d`  
		Last Modified: Thu, 22 May 2025 03:36:04 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87-slim-bookworm`

```console
$ docker pull rust@sha256:989095388527710c84035fb19f851eee7c1ef3280f20885afaa3f1ca40c132a0
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

### `rust:1.87-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:bb40fab9222e04479fcdd45dd897df82c6ce527f1be367d7af26b9d8b0ef6a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304047247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed37a08d4804ab8dc49d922940d98831dba0a9ab0d064517c16d3e8ebc61028`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfee91a65ac6ac51500a0ec06fef619ed43fb695781fb524461a5c4d2d637da`  
		Last Modified: Wed, 21 May 2025 23:30:50 GMT  
		Size: 275.8 MB (275821917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:efe02561cb166afdf2b5ceff7aa87559a0d4305e49b91aaf2b14ecea3dfac430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98fcfc56b3317ccdbefec9a1d8a372664b2c3fcb175e2a68692eb79b093238e`

```dockerfile
```

-	Layers:
	-	`sha256:8b0b25427736858183a7036091af78fd2db2d997da37facb6e4d05aaeae085ac`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 4.0 MB (3984195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d91ce431f3e8f53deb758af58dcf2d0d526914b7e949edc4a9194ad60d84b79`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:9e29ea2079cecf087bbda1c2fd2ad61236b36515fa51c6ff29828e8720467d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.1 MB (320057803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc73805e0130280f517428c036ce3ef1b66e23f5cfc530e79e9523fff52a2da`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2affe51206b495c552876f1361055b5ba2ba5c499a12dc799182e527f88fee8f`  
		Last Modified: Fri, 16 May 2025 00:47:33 GMT  
		Size: 296.1 MB (296119729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7f307223876a0415ebe98e4232538d19ba2dfd94a4587afd1b6625bc10411268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b85b7e64240d9a4922e80471ff1f6d7ddf3fa2df0e3d30083ee3421d6afb6f`

```dockerfile
```

-	Layers:
	-	`sha256:8533123b469cd2f37a235ff4ae7f91614ee1dd9a8b02d36fd1828d5275843a82`  
		Last Modified: Fri, 16 May 2025 00:47:27 GMT  
		Size: 3.8 MB (3798367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3d2d35d257570cf330e2e8c1696e66fc0e1c593229df7b7735be317bae3977`  
		Last Modified: Fri, 16 May 2025 00:47:26 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:e42c600982c6907c6953b3067f6c48033e395f4d10181943c51ebac2f7f23bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267996219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3084e189f23691ae93614b7982a7e2cac388bca91738c5669989e7d8b796f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed633d6741d291fe9a1763e68d2cccb161b0647cba3b92db34f2082a23b9e0e5`  
		Last Modified: Thu, 15 May 2025 21:25:02 GMT  
		Size: 239.9 MB (239929597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:49d4587422ab4bfcf0173cab06c43b80c8984a7ab4c06e5735771535306cbd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4019635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ed220b85632009846640d2295c2f4ab23f854fa0b42e0c3243b5cefdd747ae`

```dockerfile
```

-	Layers:
	-	`sha256:3554280116bde06c2a965fd24a497d66881cd9d1aa281871d1b73769d8a2094d`  
		Last Modified: Thu, 15 May 2025 21:24:57 GMT  
		Size: 4.0 MB (4006212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec9148c526a826a45ec9302a772ebcdbad438372587030aeb75898a207f5529`  
		Last Modified: Thu, 15 May 2025 21:24:56 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:ba53dc2028f64403c6bd2a89614ec2e82ac8573537c865976e2cc6374ec2029b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325373122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2b704e3adfa1d07aa1cbc2987edbfeecfa1944de3fb2c3a968bd74c02ec417`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814ea34b52869e575de48c99d2f39a24d0e4d29694d8f3a01507831f57c2b06d`  
		Last Modified: Wed, 21 May 2025 23:24:41 GMT  
		Size: 296.2 MB (296165635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:889b0b25c9982cd5fd0571c6b2e686ec647c319ecab6c6d5a7adb6d0d6435a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3976779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8904643b41a0647ba565c4644b3392f328605ea998f3baade734ba5d2aacb870`

```dockerfile
```

-	Layers:
	-	`sha256:b1c6f53dcb1207b295e2a9b9c928c3d427f03fff1cda3c59d8cb153c959edd63`  
		Last Modified: Wed, 21 May 2025 23:24:35 GMT  
		Size: 4.0 MB (3963560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f37c60466f2e78fb30d52c14fbff69ffd5e0acccfafbf0eeb4d5f39c371cb4`  
		Last Modified: Wed, 21 May 2025 23:24:34 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:73839fb86f1fecdfa502eed34acc218fa19ea5b56c0c32411ea7a21108c4cd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377784662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3902494a5ed4edbc6b7649c8b67f6216b185ab73ac30aeb3191240f8c20079b2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf472daa2685f63de3e031e0501577d5082ab01e4cd68a594850d5b117971ab4`  
		Last Modified: Thu, 15 May 2025 21:44:03 GMT  
		Size: 345.7 MB (345716219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b15ebebde5337a1f5f6d3035e50b978c23924c91ade52b89e87fb0ea78553cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38b8f6da58da02263499e3598466193030911e6f0ffd21726d6f52111dd4a5c`

```dockerfile
```

-	Layers:
	-	`sha256:045d5e4d7f1b02b270f2b39f6cfdc49b5cb491134b55b9308ddaa4bf79f39391`  
		Last Modified: Thu, 15 May 2025 21:43:49 GMT  
		Size: 4.0 MB (3956177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53809675a1cc4de34fd12f811d8d666321a4623ebb988f23833edcee8fbc1ef`  
		Last Modified: Thu, 15 May 2025 21:43:48 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:868e7478c67c722493268ef41b4427522279fa6a35f66461fd7adb0bf9e2c4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363329795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8621a9920839bcfdc5e9493f7408dca1bba5d13e97372f25dcb2828d0cab627`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf4c9ebe75ad00b908f5c783b4815794956bf90232cc34953f0a5744f19b699`  
		Last Modified: Thu, 22 May 2025 03:36:09 GMT  
		Size: 336.4 MB (336446987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7a4f9ef8212aa8a7d6456c13e712c2838ea2d37473e5dc052a89f5fde72edc28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6469567669efec36515c9f38ed52cb7510dea8dc20939991a8486e11898c4ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff31c08b679c1c5a077d7a557e36813d9be82c5bbc22efbc845d709dd07bfacf`  
		Last Modified: Thu, 22 May 2025 03:36:05 GMT  
		Size: 3.8 MB (3824766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a9a671478833eaf718e74615d4a29101183eeab0898f719807cd0c3a261e6d`  
		Last Modified: Thu, 22 May 2025 03:36:04 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87-slim-bullseye`

```console
$ docker pull rust@sha256:7b85733174e7e5bb18d04389fe4f44c0a2421001c0fac80e9b25856fa5b077e1
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

### `rust:1.87-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:97b80590a20d5c2eb07da85188192a7adef3f4f312522cbfd475c7de7bd82c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295463417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d550ef0b540bad33bf2ec9fb03f2c8e364e5380cd6213c65d4878abf01f3cf67`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf3b96d50315a23a39f84e3081e1253eab321a691d742d8baa3fc48a80f9ad0`  
		Last Modified: Wed, 21 May 2025 23:30:17 GMT  
		Size: 265.2 MB (265207477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7654398afe6d9c2ada6a00ed784165dda7ea2364aeee0713ceae8da91147f90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4213039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2e800891f1055bb4074ed0d02441fe6240edc04c0a2722808deb75b744d97b`

```dockerfile
```

-	Layers:
	-	`sha256:b8eb46c3c2dba7b7825cb14a2f20554b65d85f1b7982e36530088fe6645b473f`  
		Last Modified: Wed, 21 May 2025 23:30:13 GMT  
		Size: 4.2 MB (4201683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43919c7995c8288c67859032aefa9df80e945eb0051bf122fab252d5ab8603e8`  
		Last Modified: Wed, 21 May 2025 23:30:13 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:fb46a8886b184e63725f71cecc5b4447baf825554560e49a902be80aa0be12be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.9 MB (319898121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3c8bf9b7293d122263ddcf92e437f269123360707572d092aa873ff6acfe5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a398f3fb2a84d2f55ccffe98cc554e8b7b0e593b06e480a45942a14035707d5`  
		Last Modified: Fri, 16 May 2025 00:42:53 GMT  
		Size: 294.4 MB (294355694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ddb6be6bc9d103419637c3e37d63eca143fe0f3cbc083278b2c2ab7ab1ab2feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4022345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e3a4cd59da45b8ce03653bea73bd63dac2476592a9e36a5493e1fa31d8757`

```dockerfile
```

-	Layers:
	-	`sha256:902f97b8ad9a51f2adb68f88d234da7cd55c1af152e2cbb9dd297c05ffbb61c4`  
		Last Modified: Fri, 16 May 2025 00:42:47 GMT  
		Size: 4.0 MB (4010914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f026c959c784b691edc6db6bbf65f8700a3a83d8366c5c3a5b605c9a235852`  
		Last Modified: Fri, 16 May 2025 00:42:46 GMT  
		Size: 11.4 KB (11431 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be38bf3c2d6e3a2b47825e6dd4d77cf20583eb6206683ed3b21b29a77b4da50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262677882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8f9f1aa711538c6de6c47c0267af7d5e46c3d9bdd4a57a7830ca2df5328f55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4830ced46110e2a304d2fa24aff7c40cee44a64b15cbd1602175d7528ba9dca9`  
		Last Modified: Thu, 15 May 2025 21:22:59 GMT  
		Size: 233.9 MB (233933237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7b7be60ffc119e22194697635f39ef3ecb1d40d4dcedd25ef4229bc08a999188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4210772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8fc5e814cbb7c4a39f70f39dbce6ebb5f6779ca231d8f1eb11d75367bfdd9b`

```dockerfile
```

-	Layers:
	-	`sha256:68e804f29c4c1759df1a8c3a9dcdc215b964624a74e91345ccf86bb1fa7d61de`  
		Last Modified: Thu, 15 May 2025 21:22:54 GMT  
		Size: 4.2 MB (4199312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fba59bcde4cb014edb46b31d61e90b7ae6a1d420dba63e342fab2115e5f4640`  
		Last Modified: Thu, 15 May 2025 21:22:53 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:6c6e66e31919c82fe7ea1b63e8d37f1b3b89a184a6c95c9c4a1433e39d84c8d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 MB (320512888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8dae71aa0ae8520f4e956746adc671bfb485dca203c82aa62b3d1a6a45d00c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452460d1c227bf7acc8aeb01051d54bfe06fb359bfc4c6ae3535ea37ea6e2d12`  
		Last Modified: Wed, 21 May 2025 23:24:38 GMT  
		Size: 289.3 MB (289323688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5d135ffd369ba51d29a1c421aeea4320644446c924c37fb843458a4188caca00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4202751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbdf2ab316bec0455185f0aa859a9e62785b877b4f0e81754f1f65734dc86a6`

```dockerfile
```

-	Layers:
	-	`sha256:46da1a092528e79eb79c8dfaac9bdc3cc88154152aa2ad577f97f5eedcea6360`  
		Last Modified: Wed, 21 May 2025 23:24:32 GMT  
		Size: 4.2 MB (4191427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270cf5ab3f0a6904e359a5f16f1ab8ffc19021fe328a31afce493aae98aa5bdd`  
		Last Modified: Wed, 21 May 2025 23:24:31 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0`

```console
$ docker pull rust@sha256:893a03d96de2c0e6eb8b73e24b2266264b6dee244ce997d1bae246901093ba23
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

### `rust:1.87.0` - linux; amd64

```console
$ docker pull rust@sha256:3d4a2ab199238d07982c4b2bd663ed9e54d135eeecbfa326a8cc73d6659a57ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553331383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed12ea880e03238fe4e68bc7e19b72fe31649a20a35874431e0e3b9ee37bfcfe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f099911d692f62b851cf49a1e93294288a115f5cd2d014180e4d3684d34ab`  
		Last Modified: Thu, 22 May 2025 00:12:38 GMT  
		Size: 211.4 MB (211362119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60122453ea09122539d0bff9dd2ace9ad0fb5f94f28106482345e871b8776f`  
		Last Modified: Thu, 22 May 2025 01:22:53 GMT  
		Size: 205.1 MB (205065526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0` - unknown; unknown

```console
$ docker pull rust@sha256:c22e4e30bdb5ca31034eb63aa448f9c77a1102d1c161ad253c2925c9fb5de7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15583659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f90206053d1f253e46155a79fb7bb6966620d44bd8a39970cae527f1f819a1f`

```dockerfile
```

-	Layers:
	-	`sha256:6353069eb27b9defe4c9f76cfe25f6f0812b36dbd10a091e3f05bc17d5e07939`  
		Last Modified: Thu, 22 May 2025 01:22:51 GMT  
		Size: 15.6 MB (15570520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36489b5c50efe5ec3b3b1a288cc4d0a9ec10bd1986b2a4bed6d14eeb6f342209`  
		Last Modified: Thu, 22 May 2025 01:22:50 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0` - linux; arm variant v7

```console
$ docker pull rust@sha256:a717a4a677877e4c90506d6094ba956c65c8acbb675322e10051e026b84ac7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549353893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c15507a70a72169329e3fb52a9e9f8e6fda428fc8a10c673722a27ad87d7517`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Mon, 28 Apr 2025 21:15:27 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Tue, 29 Apr 2025 03:37:10 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3553b1499305feec4f182c1e2562e06daaecb3dc337d83b89b8c909f46c0a1`  
		Last Modified: Tue, 29 Apr 2025 13:22:56 GMT  
		Size: 59.6 MB (59640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d55cc6c59023a65c15579520e32553ab9f1e2d6377e8e4dd69393e113713d3`  
		Last Modified: Tue, 29 Apr 2025 16:44:12 GMT  
		Size: 175.3 MB (175316182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae6506bd78c8b0409ae60f919fcf0308fadded07bb677e52eaca831e32f27e4`  
		Last Modified: Fri, 16 May 2025 00:45:12 GMT  
		Size: 248.3 MB (248282041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0` - unknown; unknown

```console
$ docker pull rust@sha256:704762edf7170410c4143b57dc2c2592340918185bbd978e992015426067433c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15387590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118ae28de64f563725129ee9df3f3efdfd56f98689b846a2020a59babcd3a5a3`

```dockerfile
```

-	Layers:
	-	`sha256:0ed13d7d744dbbbcbf9675297a7a1707dc0b984f5b19f5a792be6856c23b4237`  
		Last Modified: Fri, 16 May 2025 00:45:09 GMT  
		Size: 15.4 MB (15374344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cc69fc971f6f9022f452d055c879d015b21e562a7728564f74f09f10c9bf7f`  
		Last Modified: Fri, 16 May 2025 00:45:06 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:79638f277b74a79352c910c6479b5cb8c25b0f2ef2b11af4b7f2d63a04bbe78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513058250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facc597070c63677b4fc7121846c580a1ee5f055d749af0856a73fc113dc99e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Tue, 29 Apr 2025 18:37:11 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d41c7623f41e51939686bf861fe89538ae4dc84481ff4136b55524e770d2603`  
		Last Modified: Wed, 30 Apr 2025 02:16:31 GMT  
		Size: 202.7 MB (202748227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2789ce74abfb6ada85cef976765f28a31f0d76101d35d89fe6f30e6a160f5cf7`  
		Last Modified: Thu, 15 May 2025 21:23:55 GMT  
		Size: 174.1 MB (174082434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0` - unknown; unknown

```console
$ docker pull rust@sha256:f7f0b6b46806bffe1c5d2161f9299dc0a9238fefa3183278ae6109c67595d89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15613623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79ce7216bf86b5ea593af61df25f8acf8b9a077a234befe5f780ee67da136ae`

```dockerfile
```

-	Layers:
	-	`sha256:00c23c1dc907f8d220ac1ef9c18b98380d358000cb5edabb21556f1ece3cc7ec`  
		Last Modified: Thu, 15 May 2025 21:23:51 GMT  
		Size: 15.6 MB (15600332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e5ccf8415d9f8e96f788c503d732dfce14045f3ba24d8366c936bf8762ef8`  
		Last Modified: Thu, 15 May 2025 21:23:50 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0` - linux; 386

```console
$ docker pull rust@sha256:d1548c29f4a54233ce3663dbf31e24697f803f2eaa51dc48517fc374e605cd53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579410243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599b9672494cb7a24c90726f5649fd8bb62e266686d6c92c3a70db98df8fb36a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Wed, 21 May 2025 23:20:06 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8c7f8292580c2c70e8cb47ec957249f0882ee6ee3737bf3250e44650a38db`  
		Last Modified: Wed, 21 May 2025 23:37:30 GMT  
		Size: 66.2 MB (66224115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e426a3a2617e34e93d75e9b5c79113e976623e3633255f578a7087d4221ba47`  
		Last Modified: Thu, 22 May 2025 00:12:45 GMT  
		Size: 210.3 MB (210303724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e15432acb4bbafe1b177dc4d3a8a7616460a38e03b58bf34ad9f8a4e54f229`  
		Last Modified: Thu, 22 May 2025 01:21:36 GMT  
		Size: 228.6 MB (228555174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0` - unknown; unknown

```console
$ docker pull rust@sha256:626889100874bfa993f52c41bf9e48649fc7b964c1dd889884eb3b1f106ed47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a19fecc316543561006e19323c1d5f88ff6b410323def3f15d858f5152634a`

```dockerfile
```

-	Layers:
	-	`sha256:d5613f30992ef58d04da59a0c3fc9df18e23a6aea5ddc9094597440de2585099`  
		Last Modified: Thu, 22 May 2025 01:21:31 GMT  
		Size: 15.5 MB (15547420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ffe58d9c1f399bf6345b1eae0a9b2681b28358b08f9b7a3333ff32c090bcda`  
		Last Modified: Thu, 22 May 2025 01:21:30 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0` - linux; ppc64le

```console
$ docker pull rust@sha256:edad25bbea95469efae8b7575e3621376e99cdac3e8dc847e12990d79ffa15e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639187573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf09d1faa6098d8816d94f3129d858a3c9895d7ccb9d5f8c7510120d86649501`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Tue, 29 Apr 2025 07:46:58 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Tue, 29 Apr 2025 08:29:00 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f7f895e65e8530bee082db2e14aefaa34547b4753e60990faca2b691714e63`  
		Last Modified: Tue, 29 Apr 2025 09:10:46 GMT  
		Size: 214.4 MB (214409240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f771a754d3f6d9880020eef886dee95dbbc411da896e8d6188ce4b35d1ccea1`  
		Last Modified: Thu, 15 May 2025 21:41:17 GMT  
		Size: 277.0 MB (276955667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0` - unknown; unknown

```console
$ docker pull rust@sha256:25e42159bf1ae8fed15f948468f0850e56728c647b8dc63fc1178c7946f65a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b8b744207f149e1825389c70977eaaa027331392f4bb1af2cf53edda9e7348`

```dockerfile
```

-	Layers:
	-	`sha256:1261dadc28c70b94878106245907b72b29ecaecd634cf88ba53927741da602e3`  
		Last Modified: Thu, 15 May 2025 21:40:56 GMT  
		Size: 15.5 MB (15546986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43db0b6c0fb41e034652a717f321ad57ef840725dc6ecbddbb455e4ba85b36da`  
		Last Modified: Thu, 15 May 2025 21:40:55 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0` - linux; s390x

```console
$ docker pull rust@sha256:a46b263c2cce2b762d073f453a72c33eb474d71183208ed22ebccb7841b9309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604372811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cc62b570c4d03e5e28a7b9abaeec07a8d1a0681c67877cdd087f829e8b5543`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Tue, 29 Apr 2025 00:01:21 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Tue, 29 Apr 2025 02:58:48 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfe8bd3e826ba76e4ad73b0a5ce638276af95b860bec9b25c2754c5600c5a61`  
		Last Modified: Tue, 29 Apr 2025 05:34:00 GMT  
		Size: 183.4 MB (183405963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589f590c508c398e3740adc2dd1d0915bdc9a36f36693dacb7d2cb83012bcca1`  
		Last Modified: Thu, 15 May 2025 23:34:36 GMT  
		Size: 286.3 MB (286310328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0` - unknown; unknown

```console
$ docker pull rust@sha256:0bb2f2b59196707a888cfccbc092b473f6e382739d12c2db5d9117cd4f490b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15395439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61693f885fe5810811eb46994aa1af308f091912dc96214dad8fd6651bc00831`

```dockerfile
```

-	Layers:
	-	`sha256:011ca34cbff4dd90ea475c3878d26371312698ea04d43f7886f8598f7f924610`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 15.4 MB (15382300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4311afc8d95a09e62d7f51e2603140152c818532e8aa83db3b1545ef3d7a15`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0-alpine`

```console
$ docker pull rust@sha256:fa7c28576553c431224a85c897c38f3a6443bd831be37061ab3560d9e797dc82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.87.0-alpine` - linux; amd64

```console
$ docker pull rust@sha256:77b6339cdb0832ad483e0d6389c4c6df605568e9c2f1a14fe76dd3b3cd3cd023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324247403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ffcf6a0b7e66d9cf8d858d524ebcd49bb36208a8c8d449ab6a1927df31f7b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b343ca42d769a088aad30a06435916be946b7bd77c275c4c48aa9c02d07ebc6`  
		Last Modified: Thu, 15 May 2025 18:37:40 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0312ddedcb8a05877b03a2214ddd4942d87d6bd8684a5f5bc0353f72d76def`  
		Last Modified: Thu, 15 May 2025 18:37:44 GMT  
		Size: 259.0 MB (259040344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:4e64c00b2317960a70850f4400db745c6cfb2bdd9f3d125aa41eae29aa6db0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.7 KB (795741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60b54f74613b5e61b7293457c23a015874a512e095a95d91dfbad52ebb043b4`

```dockerfile
```

-	Layers:
	-	`sha256:a5a1184050fab9829a713a4d20d0725d4538c6e742e9839d6591249330d5359e`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 783.8 KB (783823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05e06b11fae76f35a913f94980f7b264abfa081dffa29929dd773c6969a089d`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c46257a5086c247e6cf7f47f0b1bfd6829b0487f60ba421e09dc869a1cf8854e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 MB (326998595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4173638e4c107fec82a3872cebbc9896730ad56739846f1cab5b2d2a6662d444`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a8d04fc53dbb480e66cf7321229cda858c75a9bfa488474aabc6a3fbc3423`  
		Last Modified: Mon, 05 May 2025 22:59:43 GMT  
		Size: 59.1 MB (59101363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd10981d51d5c4342a74b76870500712f6977bafb0891f69b5b725cd3f83575b`  
		Last Modified: Thu, 15 May 2025 21:52:00 GMT  
		Size: 263.9 MB (263904203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:34672929840929fdaeda033ca2f79184da7ad0a5f4ca4c5afc3d17ab43dceceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.5 KB (875494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c7d1faabdd527c0adb51cec9eac15ffbf9a2ad32dd7bad9fd10768aef390ae`

```dockerfile
```

-	Layers:
	-	`sha256:5fad1a9258bc9e5e8818e557ec0496368c72e4184380ef235dc4bb26a03a6e03`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 863.4 KB (863409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4799a729390389da9955e76bdba397218c8fff4138d88735449c1364a6120788`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0-alpine3.20`

```console
$ docker pull rust@sha256:126b44382fa926ce41eecac3ef4628de508f0df8556fe43e8d64cdcd1cbbe40b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.87.0-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:a6e21abdf25464282e9ebe77b75a597cbd0b21d375eafa86c38af1e1cb8a2d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.0 MB (317984256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69198b701be7dc50b960f31ef7f4fd2764b266e2d8adaa0bab88ab59ce2b2bf6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718715b3cbe3b4fd9094909206504e5958585bd739a34dc4fb5b7f6ed2131b8`  
		Last Modified: Thu, 15 May 2025 18:37:42 GMT  
		Size: 55.3 MB (55315586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeb4a9d8a98d7b7dadf2be0b1943267d81b081cb2fb12a85484c6aaadf235fb`  
		Last Modified: Thu, 15 May 2025 18:37:48 GMT  
		Size: 259.0 MB (259041773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:279079ce7141a696c62912e2b546d3b1db80da36385b8291b96bd87b06a333ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.5 KB (722503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f9514c3a9ca96fa531c453a6086450f8357d88a8602759b77fade775484d62`

```dockerfile
```

-	Layers:
	-	`sha256:7ef4df00128cf574a18437ccce5e6d348c5ac96f9e656076475640bc336b72b8`  
		Last Modified: Thu, 15 May 2025 18:37:41 GMT  
		Size: 711.8 KB (711789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a9394ddea85fc3e016d5927f8ce6a38638e7c7eeea1996460a0e68f6915e5c6`  
		Last Modified: Thu, 15 May 2025 18:37:40 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2881015e0b8d0d3e45e40cf26cedbea750dc4e4bae1f9492ea6ea20c3c478296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320946007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f9aeec89829426e53d9ec2993f49c4e8add3c62bbb31e1a8833ca8f6bba7b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c6aa5430354637d99185e3c6f997bb89b34d0340d714c59489470f3b28fb00`  
		Last Modified: Mon, 05 May 2025 22:58:37 GMT  
		Size: 53.0 MB (52950277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d7b743d7f5864c65b2894547a9334b33385928622ae90e6a32c6e8856c668`  
		Last Modified: Thu, 15 May 2025 21:26:08 GMT  
		Size: 263.9 MB (263904565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:b8cb278c3d3464f502ef0c4e303cc516cf61210f397481f3f916b0efd803552e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0465991995a77f18ceff0792501f873542ee79e340b0bc4e6a168e2d55cf0cfb`

```dockerfile
```

-	Layers:
	-	`sha256:13318289bd5cbf3b293bd9e48b8d9dfb9679941c1b10fefc888f757d08695f98`  
		Last Modified: Thu, 15 May 2025 21:26:00 GMT  
		Size: 747.7 KB (747721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5df0c715639e649fb2f087e25e05ab1d51803c9e80193b7ded83d66aa0f06e`  
		Last Modified: Thu, 15 May 2025 21:25:59 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0-alpine3.21`

```console
$ docker pull rust@sha256:fa7c28576553c431224a85c897c38f3a6443bd831be37061ab3560d9e797dc82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.87.0-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:77b6339cdb0832ad483e0d6389c4c6df605568e9c2f1a14fe76dd3b3cd3cd023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324247403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ffcf6a0b7e66d9cf8d858d524ebcd49bb36208a8c8d449ab6a1927df31f7b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b343ca42d769a088aad30a06435916be946b7bd77c275c4c48aa9c02d07ebc6`  
		Last Modified: Thu, 15 May 2025 18:37:40 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0312ddedcb8a05877b03a2214ddd4942d87d6bd8684a5f5bc0353f72d76def`  
		Last Modified: Thu, 15 May 2025 18:37:44 GMT  
		Size: 259.0 MB (259040344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:4e64c00b2317960a70850f4400db745c6cfb2bdd9f3d125aa41eae29aa6db0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.7 KB (795741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60b54f74613b5e61b7293457c23a015874a512e095a95d91dfbad52ebb043b4`

```dockerfile
```

-	Layers:
	-	`sha256:a5a1184050fab9829a713a4d20d0725d4538c6e742e9839d6591249330d5359e`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 783.8 KB (783823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05e06b11fae76f35a913f94980f7b264abfa081dffa29929dd773c6969a089d`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c46257a5086c247e6cf7f47f0b1bfd6829b0487f60ba421e09dc869a1cf8854e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 MB (326998595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4173638e4c107fec82a3872cebbc9896730ad56739846f1cab5b2d2a6662d444`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a8d04fc53dbb480e66cf7321229cda858c75a9bfa488474aabc6a3fbc3423`  
		Last Modified: Mon, 05 May 2025 22:59:43 GMT  
		Size: 59.1 MB (59101363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd10981d51d5c4342a74b76870500712f6977bafb0891f69b5b725cd3f83575b`  
		Last Modified: Thu, 15 May 2025 21:52:00 GMT  
		Size: 263.9 MB (263904203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:34672929840929fdaeda033ca2f79184da7ad0a5f4ca4c5afc3d17ab43dceceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.5 KB (875494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c7d1faabdd527c0adb51cec9eac15ffbf9a2ad32dd7bad9fd10768aef390ae`

```dockerfile
```

-	Layers:
	-	`sha256:5fad1a9258bc9e5e8818e557ec0496368c72e4184380ef235dc4bb26a03a6e03`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 863.4 KB (863409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4799a729390389da9955e76bdba397218c8fff4138d88735449c1364a6120788`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0-bookworm`

```console
$ docker pull rust@sha256:893a03d96de2c0e6eb8b73e24b2266264b6dee244ce997d1bae246901093ba23
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

### `rust:1.87.0-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:3d4a2ab199238d07982c4b2bd663ed9e54d135eeecbfa326a8cc73d6659a57ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553331383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed12ea880e03238fe4e68bc7e19b72fe31649a20a35874431e0e3b9ee37bfcfe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f099911d692f62b851cf49a1e93294288a115f5cd2d014180e4d3684d34ab`  
		Last Modified: Thu, 22 May 2025 00:12:38 GMT  
		Size: 211.4 MB (211362119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60122453ea09122539d0bff9dd2ace9ad0fb5f94f28106482345e871b8776f`  
		Last Modified: Thu, 22 May 2025 01:22:53 GMT  
		Size: 205.1 MB (205065526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c22e4e30bdb5ca31034eb63aa448f9c77a1102d1c161ad253c2925c9fb5de7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15583659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f90206053d1f253e46155a79fb7bb6966620d44bd8a39970cae527f1f819a1f`

```dockerfile
```

-	Layers:
	-	`sha256:6353069eb27b9defe4c9f76cfe25f6f0812b36dbd10a091e3f05bc17d5e07939`  
		Last Modified: Thu, 22 May 2025 01:22:51 GMT  
		Size: 15.6 MB (15570520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36489b5c50efe5ec3b3b1a288cc4d0a9ec10bd1986b2a4bed6d14eeb6f342209`  
		Last Modified: Thu, 22 May 2025 01:22:50 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:a717a4a677877e4c90506d6094ba956c65c8acbb675322e10051e026b84ac7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549353893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c15507a70a72169329e3fb52a9e9f8e6fda428fc8a10c673722a27ad87d7517`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Mon, 28 Apr 2025 21:15:27 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Tue, 29 Apr 2025 03:37:10 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3553b1499305feec4f182c1e2562e06daaecb3dc337d83b89b8c909f46c0a1`  
		Last Modified: Tue, 29 Apr 2025 13:22:56 GMT  
		Size: 59.6 MB (59640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d55cc6c59023a65c15579520e32553ab9f1e2d6377e8e4dd69393e113713d3`  
		Last Modified: Tue, 29 Apr 2025 16:44:12 GMT  
		Size: 175.3 MB (175316182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae6506bd78c8b0409ae60f919fcf0308fadded07bb677e52eaca831e32f27e4`  
		Last Modified: Fri, 16 May 2025 00:45:12 GMT  
		Size: 248.3 MB (248282041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:704762edf7170410c4143b57dc2c2592340918185bbd978e992015426067433c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15387590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118ae28de64f563725129ee9df3f3efdfd56f98689b846a2020a59babcd3a5a3`

```dockerfile
```

-	Layers:
	-	`sha256:0ed13d7d744dbbbcbf9675297a7a1707dc0b984f5b19f5a792be6856c23b4237`  
		Last Modified: Fri, 16 May 2025 00:45:09 GMT  
		Size: 15.4 MB (15374344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cc69fc971f6f9022f452d055c879d015b21e562a7728564f74f09f10c9bf7f`  
		Last Modified: Fri, 16 May 2025 00:45:06 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:79638f277b74a79352c910c6479b5cb8c25b0f2ef2b11af4b7f2d63a04bbe78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513058250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facc597070c63677b4fc7121846c580a1ee5f055d749af0856a73fc113dc99e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Tue, 29 Apr 2025 18:37:11 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d41c7623f41e51939686bf861fe89538ae4dc84481ff4136b55524e770d2603`  
		Last Modified: Wed, 30 Apr 2025 02:16:31 GMT  
		Size: 202.7 MB (202748227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2789ce74abfb6ada85cef976765f28a31f0d76101d35d89fe6f30e6a160f5cf7`  
		Last Modified: Thu, 15 May 2025 21:23:55 GMT  
		Size: 174.1 MB (174082434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f7f0b6b46806bffe1c5d2161f9299dc0a9238fefa3183278ae6109c67595d89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15613623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79ce7216bf86b5ea593af61df25f8acf8b9a077a234befe5f780ee67da136ae`

```dockerfile
```

-	Layers:
	-	`sha256:00c23c1dc907f8d220ac1ef9c18b98380d358000cb5edabb21556f1ece3cc7ec`  
		Last Modified: Thu, 15 May 2025 21:23:51 GMT  
		Size: 15.6 MB (15600332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e5ccf8415d9f8e96f788c503d732dfce14045f3ba24d8366c936bf8762ef8`  
		Last Modified: Thu, 15 May 2025 21:23:50 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bookworm` - linux; 386

```console
$ docker pull rust@sha256:d1548c29f4a54233ce3663dbf31e24697f803f2eaa51dc48517fc374e605cd53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579410243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599b9672494cb7a24c90726f5649fd8bb62e266686d6c92c3a70db98df8fb36a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Wed, 21 May 2025 23:20:06 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8c7f8292580c2c70e8cb47ec957249f0882ee6ee3737bf3250e44650a38db`  
		Last Modified: Wed, 21 May 2025 23:37:30 GMT  
		Size: 66.2 MB (66224115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e426a3a2617e34e93d75e9b5c79113e976623e3633255f578a7087d4221ba47`  
		Last Modified: Thu, 22 May 2025 00:12:45 GMT  
		Size: 210.3 MB (210303724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e15432acb4bbafe1b177dc4d3a8a7616460a38e03b58bf34ad9f8a4e54f229`  
		Last Modified: Thu, 22 May 2025 01:21:36 GMT  
		Size: 228.6 MB (228555174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:626889100874bfa993f52c41bf9e48649fc7b964c1dd889884eb3b1f106ed47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a19fecc316543561006e19323c1d5f88ff6b410323def3f15d858f5152634a`

```dockerfile
```

-	Layers:
	-	`sha256:d5613f30992ef58d04da59a0c3fc9df18e23a6aea5ddc9094597440de2585099`  
		Last Modified: Thu, 22 May 2025 01:21:31 GMT  
		Size: 15.5 MB (15547420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ffe58d9c1f399bf6345b1eae0a9b2681b28358b08f9b7a3333ff32c090bcda`  
		Last Modified: Thu, 22 May 2025 01:21:30 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:edad25bbea95469efae8b7575e3621376e99cdac3e8dc847e12990d79ffa15e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639187573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf09d1faa6098d8816d94f3129d858a3c9895d7ccb9d5f8c7510120d86649501`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Tue, 29 Apr 2025 07:46:58 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Tue, 29 Apr 2025 08:29:00 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f7f895e65e8530bee082db2e14aefaa34547b4753e60990faca2b691714e63`  
		Last Modified: Tue, 29 Apr 2025 09:10:46 GMT  
		Size: 214.4 MB (214409240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f771a754d3f6d9880020eef886dee95dbbc411da896e8d6188ce4b35d1ccea1`  
		Last Modified: Thu, 15 May 2025 21:41:17 GMT  
		Size: 277.0 MB (276955667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:25e42159bf1ae8fed15f948468f0850e56728c647b8dc63fc1178c7946f65a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b8b744207f149e1825389c70977eaaa027331392f4bb1af2cf53edda9e7348`

```dockerfile
```

-	Layers:
	-	`sha256:1261dadc28c70b94878106245907b72b29ecaecd634cf88ba53927741da602e3`  
		Last Modified: Thu, 15 May 2025 21:40:56 GMT  
		Size: 15.5 MB (15546986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43db0b6c0fb41e034652a717f321ad57ef840725dc6ecbddbb455e4ba85b36da`  
		Last Modified: Thu, 15 May 2025 21:40:55 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:a46b263c2cce2b762d073f453a72c33eb474d71183208ed22ebccb7841b9309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604372811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cc62b570c4d03e5e28a7b9abaeec07a8d1a0681c67877cdd087f829e8b5543`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Tue, 29 Apr 2025 00:01:21 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Tue, 29 Apr 2025 02:58:48 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfe8bd3e826ba76e4ad73b0a5ce638276af95b860bec9b25c2754c5600c5a61`  
		Last Modified: Tue, 29 Apr 2025 05:34:00 GMT  
		Size: 183.4 MB (183405963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589f590c508c398e3740adc2dd1d0915bdc9a36f36693dacb7d2cb83012bcca1`  
		Last Modified: Thu, 15 May 2025 23:34:36 GMT  
		Size: 286.3 MB (286310328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0bb2f2b59196707a888cfccbc092b473f6e382739d12c2db5d9117cd4f490b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15395439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61693f885fe5810811eb46994aa1af308f091912dc96214dad8fd6651bc00831`

```dockerfile
```

-	Layers:
	-	`sha256:011ca34cbff4dd90ea475c3878d26371312698ea04d43f7886f8598f7f924610`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 15.4 MB (15382300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4311afc8d95a09e62d7f51e2603140152c818532e8aa83db3b1545ef3d7a15`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0-bullseye`

```console
$ docker pull rust@sha256:51f2d8c9d5c6c2506765a1f9e17c8ebc33aded193deffa72356a337ca396255a
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

### `rust:1.87.0-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:0b451f05a606a3b41c9a864500a9c50f9886a9aeb8c563d1b7ce1cf1bda5e56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526472326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bf6dd7679501c4f32309849fca9c4030a99afef60deb99454ca0ec09b18262`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Wed, 21 May 2025 23:20:29 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69a02035012d2783a66ac7ecc549af09c1718d81affa5f9c39abcf969da971`  
		Last Modified: Wed, 21 May 2025 23:37:39 GMT  
		Size: 54.8 MB (54757308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94932625c5ab18ebb7640ecd70dd33061ba90cc7666b7ff06042a8bd7cf63fb`  
		Last Modified: Thu, 22 May 2025 00:12:38 GMT  
		Size: 197.1 MB (197133895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f7643072d1ada9eba65bdb4a38d74d4c1a9411d53739374cd72e0419954af6`  
		Last Modified: Thu, 22 May 2025 01:22:46 GMT  
		Size: 205.1 MB (205066054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:73be1b1016ce85742cea899179b3476659dae35179498a4a4c22bda005e6fd13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15186206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dd4e66e59d674615efab4283c43eb93a71f55d7f04c60a4770da8c927e6a7a`

```dockerfile
```

-	Layers:
	-	`sha256:42e2775ff89b0e1ca092e8b334f36270b1c16e46d0b4457d9bd59a09a0b61499`  
		Last Modified: Thu, 22 May 2025 01:22:43 GMT  
		Size: 15.2 MB (15174957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954ef5cd1b91201a29c71b2b2d32806e4c10fcfd2bacb9671a09bf86b7820f49`  
		Last Modified: Thu, 22 May 2025 01:22:43 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:d7d4f233403022183f2af37fd51898a1d97b78dbed910fe576277af94e82d87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.4 MB (530385150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd03e62aeebdd1f83bdc094079d1c37453a5be372a0b838c1aecb8029ef3654`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Mon, 28 Apr 2025 21:16:06 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Tue, 29 Apr 2025 03:37:44 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4cecedb434598f97e33a3320b6af6e1676388e6c13b31f0aab4b7c9372012`  
		Last Modified: Tue, 29 Apr 2025 13:23:50 GMT  
		Size: 50.6 MB (50625161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce34362265f33a06975f249d19b3ebf3e131e052b1333868e863a53ee816bc45`  
		Last Modified: Tue, 29 Apr 2025 16:46:09 GMT  
		Size: 167.6 MB (167558886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9539bd9006e9f246574a8c2d9f897d10b5c6813afbfee941acec16d2754a253`  
		Last Modified: Fri, 16 May 2025 00:40:56 GMT  
		Size: 248.3 MB (248282029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:132febdf611c5e84d3d37871ca0910429259ce6b4d1deae9b87f53877127b12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14985623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c231e250c4ae7852218bf793df0bff4ce8abb50ba96b3716aea288f555f2b9a5`

```dockerfile
```

-	Layers:
	-	`sha256:abc988d1691a81eb6a0aa6a62af1d62907119d597c4ba544006f95b4fbf04e4c`  
		Last Modified: Fri, 16 May 2025 00:40:50 GMT  
		Size: 15.0 MB (14974298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d8d1c4bd3d1fa595a076fd516f16ff496c0d1db3b0bcf0e1585088e674aebf9`  
		Last Modified: Fri, 16 May 2025 00:40:50 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:237790655bcd54abab4c49c48259af2dd699173335de4e955048c62ddb2a3146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486950939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172df5659cc3f650a81e372d4074c690126a29a4b8873fdab84f99d05ddb3b6f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Tue, 29 Apr 2025 01:47:13 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Tue, 29 Apr 2025 18:37:49 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356545a2ed16b26897f2a271b3f4a7d7e64a9bf9bc0c78fdf4f1386401e37428`  
		Last Modified: Wed, 30 Apr 2025 02:18:06 GMT  
		Size: 190.0 MB (190024328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98136a9af2cf6c7fbc2743af98d832e725438a68b83e340d2dae7eaf7e34c4b4`  
		Last Modified: Thu, 15 May 2025 21:21:52 GMT  
		Size: 174.1 MB (174081523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:837bb4c602d1047b0f2f89e25c244920e3bae19537f888475e7494b23b57334a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce05b2083a6cd6c1338f72b13b1b2f39104bb810013782bd93110d997e51a630`

```dockerfile
```

-	Layers:
	-	`sha256:928ea9471f7f3720e5182302bc720fcc69c8958c677a45ae48ee625d81f5a9cb`  
		Last Modified: Thu, 15 May 2025 21:21:44 GMT  
		Size: 15.2 MB (15176927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fad39b7b7530b615cc7f2c4f42a809573b4e4e41b9423f8b02afdc2f31d3495a`  
		Last Modified: Thu, 15 May 2025 21:21:43 GMT  
		Size: 11.4 KB (11352 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bullseye` - linux; 386

```console
$ docker pull rust@sha256:ae9554cbdf2ce6d8c237cf2e62fd8da4d3e7df981bf95d72dfb02636102a0223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555598704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7804a77f872b7bebd7c0c219c30213b20ee8e554d9e5fac9bb4cbb19e7738672`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde5c2ebb13d7ca154f5cc8b4e26e7e3a669b8bac689ec15851b65e299a0fd6`  
		Last Modified: Wed, 21 May 2025 23:19:38 GMT  
		Size: 16.3 MB (16268487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e052669a7dd77fed659f1b6d3fcf5171929214e8821aaf28744160fb71f4f1`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 56.0 MB (56049779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f06bdedcf2f8fa5a0d52d346902f8aceec74013af364956265940521230002`  
		Last Modified: Thu, 22 May 2025 00:13:14 GMT  
		Size: 200.0 MB (200039337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fee6831b1ed84af5ee781297e8478225fc1f1ccd5f724ec9187d1041829c86f`  
		Last Modified: Thu, 22 May 2025 01:21:26 GMT  
		Size: 228.6 MB (228555319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:99cd576357e873f7fc20c2b9a3a22e4305a969e9fc11165246cc866b8ddb5140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15172877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c047e879fdd094e6ee7ea60daeadb0ab59443f0c260184750cf5bb5a7c5c6022`

```dockerfile
```

-	Layers:
	-	`sha256:598d23bd2066f74b5b66e8e4d84a9eed0971a6998849692f35e8eb929c9570ec`  
		Last Modified: Thu, 22 May 2025 01:21:21 GMT  
		Size: 15.2 MB (15161661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f759815be291285c72b5589321a35711ca79f0ac7a669df83b713ceef6a54b26`  
		Last Modified: Thu, 22 May 2025 01:21:21 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0-slim`

```console
$ docker pull rust@sha256:989095388527710c84035fb19f851eee7c1ef3280f20885afaa3f1ca40c132a0
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

### `rust:1.87.0-slim` - linux; amd64

```console
$ docker pull rust@sha256:bb40fab9222e04479fcdd45dd897df82c6ce527f1be367d7af26b9d8b0ef6a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304047247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed37a08d4804ab8dc49d922940d98831dba0a9ab0d064517c16d3e8ebc61028`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfee91a65ac6ac51500a0ec06fef619ed43fb695781fb524461a5c4d2d637da`  
		Last Modified: Wed, 21 May 2025 23:30:50 GMT  
		Size: 275.8 MB (275821917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:efe02561cb166afdf2b5ceff7aa87559a0d4305e49b91aaf2b14ecea3dfac430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98fcfc56b3317ccdbefec9a1d8a372664b2c3fcb175e2a68692eb79b093238e`

```dockerfile
```

-	Layers:
	-	`sha256:8b0b25427736858183a7036091af78fd2db2d997da37facb6e4d05aaeae085ac`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 4.0 MB (3984195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d91ce431f3e8f53deb758af58dcf2d0d526914b7e949edc4a9194ad60d84b79`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:9e29ea2079cecf087bbda1c2fd2ad61236b36515fa51c6ff29828e8720467d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.1 MB (320057803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc73805e0130280f517428c036ce3ef1b66e23f5cfc530e79e9523fff52a2da`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2affe51206b495c552876f1361055b5ba2ba5c499a12dc799182e527f88fee8f`  
		Last Modified: Fri, 16 May 2025 00:47:33 GMT  
		Size: 296.1 MB (296119729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:7f307223876a0415ebe98e4232538d19ba2dfd94a4587afd1b6625bc10411268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b85b7e64240d9a4922e80471ff1f6d7ddf3fa2df0e3d30083ee3421d6afb6f`

```dockerfile
```

-	Layers:
	-	`sha256:8533123b469cd2f37a235ff4ae7f91614ee1dd9a8b02d36fd1828d5275843a82`  
		Last Modified: Fri, 16 May 2025 00:47:27 GMT  
		Size: 3.8 MB (3798367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3d2d35d257570cf330e2e8c1696e66fc0e1c593229df7b7735be317bae3977`  
		Last Modified: Fri, 16 May 2025 00:47:26 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:e42c600982c6907c6953b3067f6c48033e395f4d10181943c51ebac2f7f23bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267996219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3084e189f23691ae93614b7982a7e2cac388bca91738c5669989e7d8b796f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed633d6741d291fe9a1763e68d2cccb161b0647cba3b92db34f2082a23b9e0e5`  
		Last Modified: Thu, 15 May 2025 21:25:02 GMT  
		Size: 239.9 MB (239929597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:49d4587422ab4bfcf0173cab06c43b80c8984a7ab4c06e5735771535306cbd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4019635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ed220b85632009846640d2295c2f4ab23f854fa0b42e0c3243b5cefdd747ae`

```dockerfile
```

-	Layers:
	-	`sha256:3554280116bde06c2a965fd24a497d66881cd9d1aa281871d1b73769d8a2094d`  
		Last Modified: Thu, 15 May 2025 21:24:57 GMT  
		Size: 4.0 MB (4006212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec9148c526a826a45ec9302a772ebcdbad438372587030aeb75898a207f5529`  
		Last Modified: Thu, 15 May 2025 21:24:56 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim` - linux; 386

```console
$ docker pull rust@sha256:ba53dc2028f64403c6bd2a89614ec2e82ac8573537c865976e2cc6374ec2029b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325373122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2b704e3adfa1d07aa1cbc2987edbfeecfa1944de3fb2c3a968bd74c02ec417`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814ea34b52869e575de48c99d2f39a24d0e4d29694d8f3a01507831f57c2b06d`  
		Last Modified: Wed, 21 May 2025 23:24:41 GMT  
		Size: 296.2 MB (296165635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:889b0b25c9982cd5fd0571c6b2e686ec647c319ecab6c6d5a7adb6d0d6435a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3976779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8904643b41a0647ba565c4644b3392f328605ea998f3baade734ba5d2aacb870`

```dockerfile
```

-	Layers:
	-	`sha256:b1c6f53dcb1207b295e2a9b9c928c3d427f03fff1cda3c59d8cb153c959edd63`  
		Last Modified: Wed, 21 May 2025 23:24:35 GMT  
		Size: 4.0 MB (3963560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f37c60466f2e78fb30d52c14fbff69ffd5e0acccfafbf0eeb4d5f39c371cb4`  
		Last Modified: Wed, 21 May 2025 23:24:34 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:73839fb86f1fecdfa502eed34acc218fa19ea5b56c0c32411ea7a21108c4cd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377784662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3902494a5ed4edbc6b7649c8b67f6216b185ab73ac30aeb3191240f8c20079b2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf472daa2685f63de3e031e0501577d5082ab01e4cd68a594850d5b117971ab4`  
		Last Modified: Thu, 15 May 2025 21:44:03 GMT  
		Size: 345.7 MB (345716219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b15ebebde5337a1f5f6d3035e50b978c23924c91ade52b89e87fb0ea78553cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38b8f6da58da02263499e3598466193030911e6f0ffd21726d6f52111dd4a5c`

```dockerfile
```

-	Layers:
	-	`sha256:045d5e4d7f1b02b270f2b39f6cfdc49b5cb491134b55b9308ddaa4bf79f39391`  
		Last Modified: Thu, 15 May 2025 21:43:49 GMT  
		Size: 4.0 MB (3956177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53809675a1cc4de34fd12f811d8d666321a4623ebb988f23833edcee8fbc1ef`  
		Last Modified: Thu, 15 May 2025 21:43:48 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim` - linux; s390x

```console
$ docker pull rust@sha256:868e7478c67c722493268ef41b4427522279fa6a35f66461fd7adb0bf9e2c4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363329795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8621a9920839bcfdc5e9493f7408dca1bba5d13e97372f25dcb2828d0cab627`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf4c9ebe75ad00b908f5c783b4815794956bf90232cc34953f0a5744f19b699`  
		Last Modified: Thu, 22 May 2025 03:36:09 GMT  
		Size: 336.4 MB (336446987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:7a4f9ef8212aa8a7d6456c13e712c2838ea2d37473e5dc052a89f5fde72edc28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6469567669efec36515c9f38ed52cb7510dea8dc20939991a8486e11898c4ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff31c08b679c1c5a077d7a557e36813d9be82c5bbc22efbc845d709dd07bfacf`  
		Last Modified: Thu, 22 May 2025 03:36:05 GMT  
		Size: 3.8 MB (3824766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a9a671478833eaf718e74615d4a29101183eeab0898f719807cd0c3a261e6d`  
		Last Modified: Thu, 22 May 2025 03:36:04 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0-slim-bookworm`

```console
$ docker pull rust@sha256:989095388527710c84035fb19f851eee7c1ef3280f20885afaa3f1ca40c132a0
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

### `rust:1.87.0-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:bb40fab9222e04479fcdd45dd897df82c6ce527f1be367d7af26b9d8b0ef6a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304047247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed37a08d4804ab8dc49d922940d98831dba0a9ab0d064517c16d3e8ebc61028`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfee91a65ac6ac51500a0ec06fef619ed43fb695781fb524461a5c4d2d637da`  
		Last Modified: Wed, 21 May 2025 23:30:50 GMT  
		Size: 275.8 MB (275821917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:efe02561cb166afdf2b5ceff7aa87559a0d4305e49b91aaf2b14ecea3dfac430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98fcfc56b3317ccdbefec9a1d8a372664b2c3fcb175e2a68692eb79b093238e`

```dockerfile
```

-	Layers:
	-	`sha256:8b0b25427736858183a7036091af78fd2db2d997da37facb6e4d05aaeae085ac`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 4.0 MB (3984195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d91ce431f3e8f53deb758af58dcf2d0d526914b7e949edc4a9194ad60d84b79`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:9e29ea2079cecf087bbda1c2fd2ad61236b36515fa51c6ff29828e8720467d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.1 MB (320057803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc73805e0130280f517428c036ce3ef1b66e23f5cfc530e79e9523fff52a2da`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2affe51206b495c552876f1361055b5ba2ba5c499a12dc799182e527f88fee8f`  
		Last Modified: Fri, 16 May 2025 00:47:33 GMT  
		Size: 296.1 MB (296119729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7f307223876a0415ebe98e4232538d19ba2dfd94a4587afd1b6625bc10411268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b85b7e64240d9a4922e80471ff1f6d7ddf3fa2df0e3d30083ee3421d6afb6f`

```dockerfile
```

-	Layers:
	-	`sha256:8533123b469cd2f37a235ff4ae7f91614ee1dd9a8b02d36fd1828d5275843a82`  
		Last Modified: Fri, 16 May 2025 00:47:27 GMT  
		Size: 3.8 MB (3798367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3d2d35d257570cf330e2e8c1696e66fc0e1c593229df7b7735be317bae3977`  
		Last Modified: Fri, 16 May 2025 00:47:26 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:e42c600982c6907c6953b3067f6c48033e395f4d10181943c51ebac2f7f23bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267996219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3084e189f23691ae93614b7982a7e2cac388bca91738c5669989e7d8b796f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed633d6741d291fe9a1763e68d2cccb161b0647cba3b92db34f2082a23b9e0e5`  
		Last Modified: Thu, 15 May 2025 21:25:02 GMT  
		Size: 239.9 MB (239929597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:49d4587422ab4bfcf0173cab06c43b80c8984a7ab4c06e5735771535306cbd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4019635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ed220b85632009846640d2295c2f4ab23f854fa0b42e0c3243b5cefdd747ae`

```dockerfile
```

-	Layers:
	-	`sha256:3554280116bde06c2a965fd24a497d66881cd9d1aa281871d1b73769d8a2094d`  
		Last Modified: Thu, 15 May 2025 21:24:57 GMT  
		Size: 4.0 MB (4006212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec9148c526a826a45ec9302a772ebcdbad438372587030aeb75898a207f5529`  
		Last Modified: Thu, 15 May 2025 21:24:56 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:ba53dc2028f64403c6bd2a89614ec2e82ac8573537c865976e2cc6374ec2029b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325373122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2b704e3adfa1d07aa1cbc2987edbfeecfa1944de3fb2c3a968bd74c02ec417`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814ea34b52869e575de48c99d2f39a24d0e4d29694d8f3a01507831f57c2b06d`  
		Last Modified: Wed, 21 May 2025 23:24:41 GMT  
		Size: 296.2 MB (296165635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:889b0b25c9982cd5fd0571c6b2e686ec647c319ecab6c6d5a7adb6d0d6435a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3976779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8904643b41a0647ba565c4644b3392f328605ea998f3baade734ba5d2aacb870`

```dockerfile
```

-	Layers:
	-	`sha256:b1c6f53dcb1207b295e2a9b9c928c3d427f03fff1cda3c59d8cb153c959edd63`  
		Last Modified: Wed, 21 May 2025 23:24:35 GMT  
		Size: 4.0 MB (3963560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f37c60466f2e78fb30d52c14fbff69ffd5e0acccfafbf0eeb4d5f39c371cb4`  
		Last Modified: Wed, 21 May 2025 23:24:34 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:73839fb86f1fecdfa502eed34acc218fa19ea5b56c0c32411ea7a21108c4cd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377784662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3902494a5ed4edbc6b7649c8b67f6216b185ab73ac30aeb3191240f8c20079b2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf472daa2685f63de3e031e0501577d5082ab01e4cd68a594850d5b117971ab4`  
		Last Modified: Thu, 15 May 2025 21:44:03 GMT  
		Size: 345.7 MB (345716219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b15ebebde5337a1f5f6d3035e50b978c23924c91ade52b89e87fb0ea78553cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38b8f6da58da02263499e3598466193030911e6f0ffd21726d6f52111dd4a5c`

```dockerfile
```

-	Layers:
	-	`sha256:045d5e4d7f1b02b270f2b39f6cfdc49b5cb491134b55b9308ddaa4bf79f39391`  
		Last Modified: Thu, 15 May 2025 21:43:49 GMT  
		Size: 4.0 MB (3956177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53809675a1cc4de34fd12f811d8d666321a4623ebb988f23833edcee8fbc1ef`  
		Last Modified: Thu, 15 May 2025 21:43:48 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:868e7478c67c722493268ef41b4427522279fa6a35f66461fd7adb0bf9e2c4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363329795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8621a9920839bcfdc5e9493f7408dca1bba5d13e97372f25dcb2828d0cab627`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf4c9ebe75ad00b908f5c783b4815794956bf90232cc34953f0a5744f19b699`  
		Last Modified: Thu, 22 May 2025 03:36:09 GMT  
		Size: 336.4 MB (336446987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7a4f9ef8212aa8a7d6456c13e712c2838ea2d37473e5dc052a89f5fde72edc28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6469567669efec36515c9f38ed52cb7510dea8dc20939991a8486e11898c4ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff31c08b679c1c5a077d7a557e36813d9be82c5bbc22efbc845d709dd07bfacf`  
		Last Modified: Thu, 22 May 2025 03:36:05 GMT  
		Size: 3.8 MB (3824766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a9a671478833eaf718e74615d4a29101183eeab0898f719807cd0c3a261e6d`  
		Last Modified: Thu, 22 May 2025 03:36:04 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0-slim-bullseye`

```console
$ docker pull rust@sha256:7b85733174e7e5bb18d04389fe4f44c0a2421001c0fac80e9b25856fa5b077e1
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

### `rust:1.87.0-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:97b80590a20d5c2eb07da85188192a7adef3f4f312522cbfd475c7de7bd82c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295463417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d550ef0b540bad33bf2ec9fb03f2c8e364e5380cd6213c65d4878abf01f3cf67`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf3b96d50315a23a39f84e3081e1253eab321a691d742d8baa3fc48a80f9ad0`  
		Last Modified: Wed, 21 May 2025 23:30:17 GMT  
		Size: 265.2 MB (265207477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7654398afe6d9c2ada6a00ed784165dda7ea2364aeee0713ceae8da91147f90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4213039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2e800891f1055bb4074ed0d02441fe6240edc04c0a2722808deb75b744d97b`

```dockerfile
```

-	Layers:
	-	`sha256:b8eb46c3c2dba7b7825cb14a2f20554b65d85f1b7982e36530088fe6645b473f`  
		Last Modified: Wed, 21 May 2025 23:30:13 GMT  
		Size: 4.2 MB (4201683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43919c7995c8288c67859032aefa9df80e945eb0051bf122fab252d5ab8603e8`  
		Last Modified: Wed, 21 May 2025 23:30:13 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:fb46a8886b184e63725f71cecc5b4447baf825554560e49a902be80aa0be12be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.9 MB (319898121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3c8bf9b7293d122263ddcf92e437f269123360707572d092aa873ff6acfe5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a398f3fb2a84d2f55ccffe98cc554e8b7b0e593b06e480a45942a14035707d5`  
		Last Modified: Fri, 16 May 2025 00:42:53 GMT  
		Size: 294.4 MB (294355694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ddb6be6bc9d103419637c3e37d63eca143fe0f3cbc083278b2c2ab7ab1ab2feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4022345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e3a4cd59da45b8ce03653bea73bd63dac2476592a9e36a5493e1fa31d8757`

```dockerfile
```

-	Layers:
	-	`sha256:902f97b8ad9a51f2adb68f88d234da7cd55c1af152e2cbb9dd297c05ffbb61c4`  
		Last Modified: Fri, 16 May 2025 00:42:47 GMT  
		Size: 4.0 MB (4010914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f026c959c784b691edc6db6bbf65f8700a3a83d8366c5c3a5b605c9a235852`  
		Last Modified: Fri, 16 May 2025 00:42:46 GMT  
		Size: 11.4 KB (11431 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be38bf3c2d6e3a2b47825e6dd4d77cf20583eb6206683ed3b21b29a77b4da50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262677882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8f9f1aa711538c6de6c47c0267af7d5e46c3d9bdd4a57a7830ca2df5328f55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4830ced46110e2a304d2fa24aff7c40cee44a64b15cbd1602175d7528ba9dca9`  
		Last Modified: Thu, 15 May 2025 21:22:59 GMT  
		Size: 233.9 MB (233933237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7b7be60ffc119e22194697635f39ef3ecb1d40d4dcedd25ef4229bc08a999188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4210772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8fc5e814cbb7c4a39f70f39dbce6ebb5f6779ca231d8f1eb11d75367bfdd9b`

```dockerfile
```

-	Layers:
	-	`sha256:68e804f29c4c1759df1a8c3a9dcdc215b964624a74e91345ccf86bb1fa7d61de`  
		Last Modified: Thu, 15 May 2025 21:22:54 GMT  
		Size: 4.2 MB (4199312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fba59bcde4cb014edb46b31d61e90b7ae6a1d420dba63e342fab2115e5f4640`  
		Last Modified: Thu, 15 May 2025 21:22:53 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:6c6e66e31919c82fe7ea1b63e8d37f1b3b89a184a6c95c9c4a1433e39d84c8d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 MB (320512888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8dae71aa0ae8520f4e956746adc671bfb485dca203c82aa62b3d1a6a45d00c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452460d1c227bf7acc8aeb01051d54bfe06fb359bfc4c6ae3535ea37ea6e2d12`  
		Last Modified: Wed, 21 May 2025 23:24:38 GMT  
		Size: 289.3 MB (289323688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5d135ffd369ba51d29a1c421aeea4320644446c924c37fb843458a4188caca00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4202751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbdf2ab316bec0455185f0aa859a9e62785b877b4f0e81754f1f65734dc86a6`

```dockerfile
```

-	Layers:
	-	`sha256:46da1a092528e79eb79c8dfaac9bdc3cc88154152aa2ad577f97f5eedcea6360`  
		Last Modified: Wed, 21 May 2025 23:24:32 GMT  
		Size: 4.2 MB (4191427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270cf5ab3f0a6904e359a5f16f1ab8ffc19021fe328a31afce493aae98aa5bdd`  
		Last Modified: Wed, 21 May 2025 23:24:31 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:fa7c28576553c431224a85c897c38f3a6443bd831be37061ab3560d9e797dc82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:77b6339cdb0832ad483e0d6389c4c6df605568e9c2f1a14fe76dd3b3cd3cd023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324247403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ffcf6a0b7e66d9cf8d858d524ebcd49bb36208a8c8d449ab6a1927df31f7b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b343ca42d769a088aad30a06435916be946b7bd77c275c4c48aa9c02d07ebc6`  
		Last Modified: Thu, 15 May 2025 18:37:40 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0312ddedcb8a05877b03a2214ddd4942d87d6bd8684a5f5bc0353f72d76def`  
		Last Modified: Thu, 15 May 2025 18:37:44 GMT  
		Size: 259.0 MB (259040344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:4e64c00b2317960a70850f4400db745c6cfb2bdd9f3d125aa41eae29aa6db0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.7 KB (795741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60b54f74613b5e61b7293457c23a015874a512e095a95d91dfbad52ebb043b4`

```dockerfile
```

-	Layers:
	-	`sha256:a5a1184050fab9829a713a4d20d0725d4538c6e742e9839d6591249330d5359e`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 783.8 KB (783823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05e06b11fae76f35a913f94980f7b264abfa081dffa29929dd773c6969a089d`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c46257a5086c247e6cf7f47f0b1bfd6829b0487f60ba421e09dc869a1cf8854e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 MB (326998595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4173638e4c107fec82a3872cebbc9896730ad56739846f1cab5b2d2a6662d444`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a8d04fc53dbb480e66cf7321229cda858c75a9bfa488474aabc6a3fbc3423`  
		Last Modified: Mon, 05 May 2025 22:59:43 GMT  
		Size: 59.1 MB (59101363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd10981d51d5c4342a74b76870500712f6977bafb0891f69b5b725cd3f83575b`  
		Last Modified: Thu, 15 May 2025 21:52:00 GMT  
		Size: 263.9 MB (263904203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:34672929840929fdaeda033ca2f79184da7ad0a5f4ca4c5afc3d17ab43dceceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.5 KB (875494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c7d1faabdd527c0adb51cec9eac15ffbf9a2ad32dd7bad9fd10768aef390ae`

```dockerfile
```

-	Layers:
	-	`sha256:5fad1a9258bc9e5e8818e557ec0496368c72e4184380ef235dc4bb26a03a6e03`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 863.4 KB (863409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4799a729390389da9955e76bdba397218c8fff4138d88735449c1364a6120788`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.20`

```console
$ docker pull rust@sha256:126b44382fa926ce41eecac3ef4628de508f0df8556fe43e8d64cdcd1cbbe40b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:a6e21abdf25464282e9ebe77b75a597cbd0b21d375eafa86c38af1e1cb8a2d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.0 MB (317984256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69198b701be7dc50b960f31ef7f4fd2764b266e2d8adaa0bab88ab59ce2b2bf6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718715b3cbe3b4fd9094909206504e5958585bd739a34dc4fb5b7f6ed2131b8`  
		Last Modified: Thu, 15 May 2025 18:37:42 GMT  
		Size: 55.3 MB (55315586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeb4a9d8a98d7b7dadf2be0b1943267d81b081cb2fb12a85484c6aaadf235fb`  
		Last Modified: Thu, 15 May 2025 18:37:48 GMT  
		Size: 259.0 MB (259041773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:279079ce7141a696c62912e2b546d3b1db80da36385b8291b96bd87b06a333ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.5 KB (722503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f9514c3a9ca96fa531c453a6086450f8357d88a8602759b77fade775484d62`

```dockerfile
```

-	Layers:
	-	`sha256:7ef4df00128cf574a18437ccce5e6d348c5ac96f9e656076475640bc336b72b8`  
		Last Modified: Thu, 15 May 2025 18:37:41 GMT  
		Size: 711.8 KB (711789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a9394ddea85fc3e016d5927f8ce6a38638e7c7eeea1996460a0e68f6915e5c6`  
		Last Modified: Thu, 15 May 2025 18:37:40 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2881015e0b8d0d3e45e40cf26cedbea750dc4e4bae1f9492ea6ea20c3c478296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320946007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f9aeec89829426e53d9ec2993f49c4e8add3c62bbb31e1a8833ca8f6bba7b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c6aa5430354637d99185e3c6f997bb89b34d0340d714c59489470f3b28fb00`  
		Last Modified: Mon, 05 May 2025 22:58:37 GMT  
		Size: 53.0 MB (52950277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d7b743d7f5864c65b2894547a9334b33385928622ae90e6a32c6e8856c668`  
		Last Modified: Thu, 15 May 2025 21:26:08 GMT  
		Size: 263.9 MB (263904565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:b8cb278c3d3464f502ef0c4e303cc516cf61210f397481f3f916b0efd803552e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.6 KB (758554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0465991995a77f18ceff0792501f873542ee79e340b0bc4e6a168e2d55cf0cfb`

```dockerfile
```

-	Layers:
	-	`sha256:13318289bd5cbf3b293bd9e48b8d9dfb9679941c1b10fefc888f757d08695f98`  
		Last Modified: Thu, 15 May 2025 21:26:00 GMT  
		Size: 747.7 KB (747721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5df0c715639e649fb2f087e25e05ab1d51803c9e80193b7ded83d66aa0f06e`  
		Last Modified: Thu, 15 May 2025 21:25:59 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.21`

```console
$ docker pull rust@sha256:fa7c28576553c431224a85c897c38f3a6443bd831be37061ab3560d9e797dc82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:77b6339cdb0832ad483e0d6389c4c6df605568e9c2f1a14fe76dd3b3cd3cd023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324247403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ffcf6a0b7e66d9cf8d858d524ebcd49bb36208a8c8d449ab6a1927df31f7b2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b343ca42d769a088aad30a06435916be946b7bd77c275c4c48aa9c02d07ebc6`  
		Last Modified: Thu, 15 May 2025 18:37:40 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0312ddedcb8a05877b03a2214ddd4942d87d6bd8684a5f5bc0353f72d76def`  
		Last Modified: Thu, 15 May 2025 18:37:44 GMT  
		Size: 259.0 MB (259040344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:4e64c00b2317960a70850f4400db745c6cfb2bdd9f3d125aa41eae29aa6db0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.7 KB (795741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60b54f74613b5e61b7293457c23a015874a512e095a95d91dfbad52ebb043b4`

```dockerfile
```

-	Layers:
	-	`sha256:a5a1184050fab9829a713a4d20d0725d4538c6e742e9839d6591249330d5359e`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 783.8 KB (783823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05e06b11fae76f35a913f94980f7b264abfa081dffa29929dd773c6969a089d`  
		Last Modified: Thu, 15 May 2025 18:37:37 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:c46257a5086c247e6cf7f47f0b1bfd6829b0487f60ba421e09dc869a1cf8854e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 MB (326998595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4173638e4c107fec82a3872cebbc9896730ad56739846f1cab5b2d2a6662d444`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a8d04fc53dbb480e66cf7321229cda858c75a9bfa488474aabc6a3fbc3423`  
		Last Modified: Mon, 05 May 2025 22:59:43 GMT  
		Size: 59.1 MB (59101363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd10981d51d5c4342a74b76870500712f6977bafb0891f69b5b725cd3f83575b`  
		Last Modified: Thu, 15 May 2025 21:52:00 GMT  
		Size: 263.9 MB (263904203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:34672929840929fdaeda033ca2f79184da7ad0a5f4ca4c5afc3d17ab43dceceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.5 KB (875494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c7d1faabdd527c0adb51cec9eac15ffbf9a2ad32dd7bad9fd10768aef390ae`

```dockerfile
```

-	Layers:
	-	`sha256:5fad1a9258bc9e5e8818e557ec0496368c72e4184380ef235dc4bb26a03a6e03`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 863.4 KB (863409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4799a729390389da9955e76bdba397218c8fff4138d88735449c1364a6120788`  
		Last Modified: Thu, 15 May 2025 21:51:55 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:893a03d96de2c0e6eb8b73e24b2266264b6dee244ce997d1bae246901093ba23
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
$ docker pull rust@sha256:3d4a2ab199238d07982c4b2bd663ed9e54d135eeecbfa326a8cc73d6659a57ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553331383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed12ea880e03238fe4e68bc7e19b72fe31649a20a35874431e0e3b9ee37bfcfe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f099911d692f62b851cf49a1e93294288a115f5cd2d014180e4d3684d34ab`  
		Last Modified: Thu, 22 May 2025 00:12:38 GMT  
		Size: 211.4 MB (211362119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60122453ea09122539d0bff9dd2ace9ad0fb5f94f28106482345e871b8776f`  
		Last Modified: Thu, 22 May 2025 01:22:53 GMT  
		Size: 205.1 MB (205065526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c22e4e30bdb5ca31034eb63aa448f9c77a1102d1c161ad253c2925c9fb5de7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15583659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f90206053d1f253e46155a79fb7bb6966620d44bd8a39970cae527f1f819a1f`

```dockerfile
```

-	Layers:
	-	`sha256:6353069eb27b9defe4c9f76cfe25f6f0812b36dbd10a091e3f05bc17d5e07939`  
		Last Modified: Thu, 22 May 2025 01:22:51 GMT  
		Size: 15.6 MB (15570520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36489b5c50efe5ec3b3b1a288cc4d0a9ec10bd1986b2a4bed6d14eeb6f342209`  
		Last Modified: Thu, 22 May 2025 01:22:50 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:a717a4a677877e4c90506d6094ba956c65c8acbb675322e10051e026b84ac7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549353893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c15507a70a72169329e3fb52a9e9f8e6fda428fc8a10c673722a27ad87d7517`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Mon, 28 Apr 2025 21:15:27 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Tue, 29 Apr 2025 03:37:10 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3553b1499305feec4f182c1e2562e06daaecb3dc337d83b89b8c909f46c0a1`  
		Last Modified: Tue, 29 Apr 2025 13:22:56 GMT  
		Size: 59.6 MB (59640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d55cc6c59023a65c15579520e32553ab9f1e2d6377e8e4dd69393e113713d3`  
		Last Modified: Tue, 29 Apr 2025 16:44:12 GMT  
		Size: 175.3 MB (175316182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae6506bd78c8b0409ae60f919fcf0308fadded07bb677e52eaca831e32f27e4`  
		Last Modified: Fri, 16 May 2025 00:45:12 GMT  
		Size: 248.3 MB (248282041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:704762edf7170410c4143b57dc2c2592340918185bbd978e992015426067433c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15387590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118ae28de64f563725129ee9df3f3efdfd56f98689b846a2020a59babcd3a5a3`

```dockerfile
```

-	Layers:
	-	`sha256:0ed13d7d744dbbbcbf9675297a7a1707dc0b984f5b19f5a792be6856c23b4237`  
		Last Modified: Fri, 16 May 2025 00:45:09 GMT  
		Size: 15.4 MB (15374344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cc69fc971f6f9022f452d055c879d015b21e562a7728564f74f09f10c9bf7f`  
		Last Modified: Fri, 16 May 2025 00:45:06 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:79638f277b74a79352c910c6479b5cb8c25b0f2ef2b11af4b7f2d63a04bbe78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513058250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facc597070c63677b4fc7121846c580a1ee5f055d749af0856a73fc113dc99e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Tue, 29 Apr 2025 18:37:11 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d41c7623f41e51939686bf861fe89538ae4dc84481ff4136b55524e770d2603`  
		Last Modified: Wed, 30 Apr 2025 02:16:31 GMT  
		Size: 202.7 MB (202748227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2789ce74abfb6ada85cef976765f28a31f0d76101d35d89fe6f30e6a160f5cf7`  
		Last Modified: Thu, 15 May 2025 21:23:55 GMT  
		Size: 174.1 MB (174082434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f7f0b6b46806bffe1c5d2161f9299dc0a9238fefa3183278ae6109c67595d89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15613623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79ce7216bf86b5ea593af61df25f8acf8b9a077a234befe5f780ee67da136ae`

```dockerfile
```

-	Layers:
	-	`sha256:00c23c1dc907f8d220ac1ef9c18b98380d358000cb5edabb21556f1ece3cc7ec`  
		Last Modified: Thu, 15 May 2025 21:23:51 GMT  
		Size: 15.6 MB (15600332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e5ccf8415d9f8e96f788c503d732dfce14045f3ba24d8366c936bf8762ef8`  
		Last Modified: Thu, 15 May 2025 21:23:50 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:d1548c29f4a54233ce3663dbf31e24697f803f2eaa51dc48517fc374e605cd53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579410243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599b9672494cb7a24c90726f5649fd8bb62e266686d6c92c3a70db98df8fb36a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Wed, 21 May 2025 23:20:06 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8c7f8292580c2c70e8cb47ec957249f0882ee6ee3737bf3250e44650a38db`  
		Last Modified: Wed, 21 May 2025 23:37:30 GMT  
		Size: 66.2 MB (66224115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e426a3a2617e34e93d75e9b5c79113e976623e3633255f578a7087d4221ba47`  
		Last Modified: Thu, 22 May 2025 00:12:45 GMT  
		Size: 210.3 MB (210303724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e15432acb4bbafe1b177dc4d3a8a7616460a38e03b58bf34ad9f8a4e54f229`  
		Last Modified: Thu, 22 May 2025 01:21:36 GMT  
		Size: 228.6 MB (228555174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:626889100874bfa993f52c41bf9e48649fc7b964c1dd889884eb3b1f106ed47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a19fecc316543561006e19323c1d5f88ff6b410323def3f15d858f5152634a`

```dockerfile
```

-	Layers:
	-	`sha256:d5613f30992ef58d04da59a0c3fc9df18e23a6aea5ddc9094597440de2585099`  
		Last Modified: Thu, 22 May 2025 01:21:31 GMT  
		Size: 15.5 MB (15547420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ffe58d9c1f399bf6345b1eae0a9b2681b28358b08f9b7a3333ff32c090bcda`  
		Last Modified: Thu, 22 May 2025 01:21:30 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:edad25bbea95469efae8b7575e3621376e99cdac3e8dc847e12990d79ffa15e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639187573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf09d1faa6098d8816d94f3129d858a3c9895d7ccb9d5f8c7510120d86649501`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Tue, 29 Apr 2025 07:46:58 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Tue, 29 Apr 2025 08:29:00 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f7f895e65e8530bee082db2e14aefaa34547b4753e60990faca2b691714e63`  
		Last Modified: Tue, 29 Apr 2025 09:10:46 GMT  
		Size: 214.4 MB (214409240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f771a754d3f6d9880020eef886dee95dbbc411da896e8d6188ce4b35d1ccea1`  
		Last Modified: Thu, 15 May 2025 21:41:17 GMT  
		Size: 277.0 MB (276955667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:25e42159bf1ae8fed15f948468f0850e56728c647b8dc63fc1178c7946f65a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b8b744207f149e1825389c70977eaaa027331392f4bb1af2cf53edda9e7348`

```dockerfile
```

-	Layers:
	-	`sha256:1261dadc28c70b94878106245907b72b29ecaecd634cf88ba53927741da602e3`  
		Last Modified: Thu, 15 May 2025 21:40:56 GMT  
		Size: 15.5 MB (15546986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43db0b6c0fb41e034652a717f321ad57ef840725dc6ecbddbb455e4ba85b36da`  
		Last Modified: Thu, 15 May 2025 21:40:55 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:a46b263c2cce2b762d073f453a72c33eb474d71183208ed22ebccb7841b9309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604372811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cc62b570c4d03e5e28a7b9abaeec07a8d1a0681c67877cdd087f829e8b5543`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Tue, 29 Apr 2025 00:01:21 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Tue, 29 Apr 2025 02:58:48 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfe8bd3e826ba76e4ad73b0a5ce638276af95b860bec9b25c2754c5600c5a61`  
		Last Modified: Tue, 29 Apr 2025 05:34:00 GMT  
		Size: 183.4 MB (183405963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589f590c508c398e3740adc2dd1d0915bdc9a36f36693dacb7d2cb83012bcca1`  
		Last Modified: Thu, 15 May 2025 23:34:36 GMT  
		Size: 286.3 MB (286310328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0bb2f2b59196707a888cfccbc092b473f6e382739d12c2db5d9117cd4f490b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15395439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61693f885fe5810811eb46994aa1af308f091912dc96214dad8fd6651bc00831`

```dockerfile
```

-	Layers:
	-	`sha256:011ca34cbff4dd90ea475c3878d26371312698ea04d43f7886f8598f7f924610`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 15.4 MB (15382300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4311afc8d95a09e62d7f51e2603140152c818532e8aa83db3b1545ef3d7a15`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:51f2d8c9d5c6c2506765a1f9e17c8ebc33aded193deffa72356a337ca396255a
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
$ docker pull rust@sha256:0b451f05a606a3b41c9a864500a9c50f9886a9aeb8c563d1b7ce1cf1bda5e56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526472326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bf6dd7679501c4f32309849fca9c4030a99afef60deb99454ca0ec09b18262`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Wed, 21 May 2025 23:20:29 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69a02035012d2783a66ac7ecc549af09c1718d81affa5f9c39abcf969da971`  
		Last Modified: Wed, 21 May 2025 23:37:39 GMT  
		Size: 54.8 MB (54757308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94932625c5ab18ebb7640ecd70dd33061ba90cc7666b7ff06042a8bd7cf63fb`  
		Last Modified: Thu, 22 May 2025 00:12:38 GMT  
		Size: 197.1 MB (197133895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f7643072d1ada9eba65bdb4a38d74d4c1a9411d53739374cd72e0419954af6`  
		Last Modified: Thu, 22 May 2025 01:22:46 GMT  
		Size: 205.1 MB (205066054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:73be1b1016ce85742cea899179b3476659dae35179498a4a4c22bda005e6fd13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15186206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dd4e66e59d674615efab4283c43eb93a71f55d7f04c60a4770da8c927e6a7a`

```dockerfile
```

-	Layers:
	-	`sha256:42e2775ff89b0e1ca092e8b334f36270b1c16e46d0b4457d9bd59a09a0b61499`  
		Last Modified: Thu, 22 May 2025 01:22:43 GMT  
		Size: 15.2 MB (15174957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954ef5cd1b91201a29c71b2b2d32806e4c10fcfd2bacb9671a09bf86b7820f49`  
		Last Modified: Thu, 22 May 2025 01:22:43 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:d7d4f233403022183f2af37fd51898a1d97b78dbed910fe576277af94e82d87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.4 MB (530385150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd03e62aeebdd1f83bdc094079d1c37453a5be372a0b838c1aecb8029ef3654`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Mon, 28 Apr 2025 21:16:06 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Tue, 29 Apr 2025 03:37:44 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4cecedb434598f97e33a3320b6af6e1676388e6c13b31f0aab4b7c9372012`  
		Last Modified: Tue, 29 Apr 2025 13:23:50 GMT  
		Size: 50.6 MB (50625161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce34362265f33a06975f249d19b3ebf3e131e052b1333868e863a53ee816bc45`  
		Last Modified: Tue, 29 Apr 2025 16:46:09 GMT  
		Size: 167.6 MB (167558886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9539bd9006e9f246574a8c2d9f897d10b5c6813afbfee941acec16d2754a253`  
		Last Modified: Fri, 16 May 2025 00:40:56 GMT  
		Size: 248.3 MB (248282029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:132febdf611c5e84d3d37871ca0910429259ce6b4d1deae9b87f53877127b12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14985623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c231e250c4ae7852218bf793df0bff4ce8abb50ba96b3716aea288f555f2b9a5`

```dockerfile
```

-	Layers:
	-	`sha256:abc988d1691a81eb6a0aa6a62af1d62907119d597c4ba544006f95b4fbf04e4c`  
		Last Modified: Fri, 16 May 2025 00:40:50 GMT  
		Size: 15.0 MB (14974298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d8d1c4bd3d1fa595a076fd516f16ff496c0d1db3b0bcf0e1585088e674aebf9`  
		Last Modified: Fri, 16 May 2025 00:40:50 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:237790655bcd54abab4c49c48259af2dd699173335de4e955048c62ddb2a3146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486950939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172df5659cc3f650a81e372d4074c690126a29a4b8873fdab84f99d05ddb3b6f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Tue, 29 Apr 2025 01:47:13 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Tue, 29 Apr 2025 18:37:49 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356545a2ed16b26897f2a271b3f4a7d7e64a9bf9bc0c78fdf4f1386401e37428`  
		Last Modified: Wed, 30 Apr 2025 02:18:06 GMT  
		Size: 190.0 MB (190024328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98136a9af2cf6c7fbc2743af98d832e725438a68b83e340d2dae7eaf7e34c4b4`  
		Last Modified: Thu, 15 May 2025 21:21:52 GMT  
		Size: 174.1 MB (174081523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:837bb4c602d1047b0f2f89e25c244920e3bae19537f888475e7494b23b57334a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce05b2083a6cd6c1338f72b13b1b2f39104bb810013782bd93110d997e51a630`

```dockerfile
```

-	Layers:
	-	`sha256:928ea9471f7f3720e5182302bc720fcc69c8958c677a45ae48ee625d81f5a9cb`  
		Last Modified: Thu, 15 May 2025 21:21:44 GMT  
		Size: 15.2 MB (15176927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fad39b7b7530b615cc7f2c4f42a809573b4e4e41b9423f8b02afdc2f31d3495a`  
		Last Modified: Thu, 15 May 2025 21:21:43 GMT  
		Size: 11.4 KB (11352 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:ae9554cbdf2ce6d8c237cf2e62fd8da4d3e7df981bf95d72dfb02636102a0223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555598704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7804a77f872b7bebd7c0c219c30213b20ee8e554d9e5fac9bb4cbb19e7738672`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde5c2ebb13d7ca154f5cc8b4e26e7e3a669b8bac689ec15851b65e299a0fd6`  
		Last Modified: Wed, 21 May 2025 23:19:38 GMT  
		Size: 16.3 MB (16268487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e052669a7dd77fed659f1b6d3fcf5171929214e8821aaf28744160fb71f4f1`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 56.0 MB (56049779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f06bdedcf2f8fa5a0d52d346902f8aceec74013af364956265940521230002`  
		Last Modified: Thu, 22 May 2025 00:13:14 GMT  
		Size: 200.0 MB (200039337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fee6831b1ed84af5ee781297e8478225fc1f1ccd5f724ec9187d1041829c86f`  
		Last Modified: Thu, 22 May 2025 01:21:26 GMT  
		Size: 228.6 MB (228555319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:99cd576357e873f7fc20c2b9a3a22e4305a969e9fc11165246cc866b8ddb5140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15172877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c047e879fdd094e6ee7ea60daeadb0ab59443f0c260184750cf5bb5a7c5c6022`

```dockerfile
```

-	Layers:
	-	`sha256:598d23bd2066f74b5b66e8e4d84a9eed0971a6998849692f35e8eb929c9570ec`  
		Last Modified: Thu, 22 May 2025 01:21:21 GMT  
		Size: 15.2 MB (15161661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f759815be291285c72b5589321a35711ca79f0ac7a669df83b713ceef6a54b26`  
		Last Modified: Thu, 22 May 2025 01:21:21 GMT  
		Size: 11.2 KB (11216 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:893a03d96de2c0e6eb8b73e24b2266264b6dee244ce997d1bae246901093ba23
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
$ docker pull rust@sha256:3d4a2ab199238d07982c4b2bd663ed9e54d135eeecbfa326a8cc73d6659a57ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553331383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed12ea880e03238fe4e68bc7e19b72fe31649a20a35874431e0e3b9ee37bfcfe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f099911d692f62b851cf49a1e93294288a115f5cd2d014180e4d3684d34ab`  
		Last Modified: Thu, 22 May 2025 00:12:38 GMT  
		Size: 211.4 MB (211362119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60122453ea09122539d0bff9dd2ace9ad0fb5f94f28106482345e871b8776f`  
		Last Modified: Thu, 22 May 2025 01:22:53 GMT  
		Size: 205.1 MB (205065526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:c22e4e30bdb5ca31034eb63aa448f9c77a1102d1c161ad253c2925c9fb5de7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15583659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f90206053d1f253e46155a79fb7bb6966620d44bd8a39970cae527f1f819a1f`

```dockerfile
```

-	Layers:
	-	`sha256:6353069eb27b9defe4c9f76cfe25f6f0812b36dbd10a091e3f05bc17d5e07939`  
		Last Modified: Thu, 22 May 2025 01:22:51 GMT  
		Size: 15.6 MB (15570520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36489b5c50efe5ec3b3b1a288cc4d0a9ec10bd1986b2a4bed6d14eeb6f342209`  
		Last Modified: Thu, 22 May 2025 01:22:50 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:a717a4a677877e4c90506d6094ba956c65c8acbb675322e10051e026b84ac7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549353893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c15507a70a72169329e3fb52a9e9f8e6fda428fc8a10c673722a27ad87d7517`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Mon, 28 Apr 2025 21:15:27 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Tue, 29 Apr 2025 03:37:10 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3553b1499305feec4f182c1e2562e06daaecb3dc337d83b89b8c909f46c0a1`  
		Last Modified: Tue, 29 Apr 2025 13:22:56 GMT  
		Size: 59.6 MB (59640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d55cc6c59023a65c15579520e32553ab9f1e2d6377e8e4dd69393e113713d3`  
		Last Modified: Tue, 29 Apr 2025 16:44:12 GMT  
		Size: 175.3 MB (175316182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae6506bd78c8b0409ae60f919fcf0308fadded07bb677e52eaca831e32f27e4`  
		Last Modified: Fri, 16 May 2025 00:45:12 GMT  
		Size: 248.3 MB (248282041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:704762edf7170410c4143b57dc2c2592340918185bbd978e992015426067433c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15387590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118ae28de64f563725129ee9df3f3efdfd56f98689b846a2020a59babcd3a5a3`

```dockerfile
```

-	Layers:
	-	`sha256:0ed13d7d744dbbbcbf9675297a7a1707dc0b984f5b19f5a792be6856c23b4237`  
		Last Modified: Fri, 16 May 2025 00:45:09 GMT  
		Size: 15.4 MB (15374344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cc69fc971f6f9022f452d055c879d015b21e562a7728564f74f09f10c9bf7f`  
		Last Modified: Fri, 16 May 2025 00:45:06 GMT  
		Size: 13.2 KB (13246 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:79638f277b74a79352c910c6479b5cb8c25b0f2ef2b11af4b7f2d63a04bbe78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513058250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facc597070c63677b4fc7121846c580a1ee5f055d749af0856a73fc113dc99e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Tue, 29 Apr 2025 18:37:11 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d41c7623f41e51939686bf861fe89538ae4dc84481ff4136b55524e770d2603`  
		Last Modified: Wed, 30 Apr 2025 02:16:31 GMT  
		Size: 202.7 MB (202748227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2789ce74abfb6ada85cef976765f28a31f0d76101d35d89fe6f30e6a160f5cf7`  
		Last Modified: Thu, 15 May 2025 21:23:55 GMT  
		Size: 174.1 MB (174082434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:f7f0b6b46806bffe1c5d2161f9299dc0a9238fefa3183278ae6109c67595d89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15613623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79ce7216bf86b5ea593af61df25f8acf8b9a077a234befe5f780ee67da136ae`

```dockerfile
```

-	Layers:
	-	`sha256:00c23c1dc907f8d220ac1ef9c18b98380d358000cb5edabb21556f1ece3cc7ec`  
		Last Modified: Thu, 15 May 2025 21:23:51 GMT  
		Size: 15.6 MB (15600332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3e5ccf8415d9f8e96f788c503d732dfce14045f3ba24d8366c936bf8762ef8`  
		Last Modified: Thu, 15 May 2025 21:23:50 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:d1548c29f4a54233ce3663dbf31e24697f803f2eaa51dc48517fc374e605cd53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579410243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599b9672494cb7a24c90726f5649fd8bb62e266686d6c92c3a70db98df8fb36a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Wed, 21 May 2025 23:20:06 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8c7f8292580c2c70e8cb47ec957249f0882ee6ee3737bf3250e44650a38db`  
		Last Modified: Wed, 21 May 2025 23:37:30 GMT  
		Size: 66.2 MB (66224115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e426a3a2617e34e93d75e9b5c79113e976623e3633255f578a7087d4221ba47`  
		Last Modified: Thu, 22 May 2025 00:12:45 GMT  
		Size: 210.3 MB (210303724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e15432acb4bbafe1b177dc4d3a8a7616460a38e03b58bf34ad9f8a4e54f229`  
		Last Modified: Thu, 22 May 2025 01:21:36 GMT  
		Size: 228.6 MB (228555174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:626889100874bfa993f52c41bf9e48649fc7b964c1dd889884eb3b1f106ed47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a19fecc316543561006e19323c1d5f88ff6b410323def3f15d858f5152634a`

```dockerfile
```

-	Layers:
	-	`sha256:d5613f30992ef58d04da59a0c3fc9df18e23a6aea5ddc9094597440de2585099`  
		Last Modified: Thu, 22 May 2025 01:21:31 GMT  
		Size: 15.5 MB (15547420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ffe58d9c1f399bf6345b1eae0a9b2681b28358b08f9b7a3333ff32c090bcda`  
		Last Modified: Thu, 22 May 2025 01:21:30 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:edad25bbea95469efae8b7575e3621376e99cdac3e8dc847e12990d79ffa15e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639187573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf09d1faa6098d8816d94f3129d858a3c9895d7ccb9d5f8c7510120d86649501`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Tue, 29 Apr 2025 07:46:58 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Tue, 29 Apr 2025 08:29:00 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f7f895e65e8530bee082db2e14aefaa34547b4753e60990faca2b691714e63`  
		Last Modified: Tue, 29 Apr 2025 09:10:46 GMT  
		Size: 214.4 MB (214409240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f771a754d3f6d9880020eef886dee95dbbc411da896e8d6188ce4b35d1ccea1`  
		Last Modified: Thu, 15 May 2025 21:41:17 GMT  
		Size: 277.0 MB (276955667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:25e42159bf1ae8fed15f948468f0850e56728c647b8dc63fc1178c7946f65a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15560193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b8b744207f149e1825389c70977eaaa027331392f4bb1af2cf53edda9e7348`

```dockerfile
```

-	Layers:
	-	`sha256:1261dadc28c70b94878106245907b72b29ecaecd634cf88ba53927741da602e3`  
		Last Modified: Thu, 15 May 2025 21:40:56 GMT  
		Size: 15.5 MB (15546986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43db0b6c0fb41e034652a717f321ad57ef840725dc6ecbddbb455e4ba85b36da`  
		Last Modified: Thu, 15 May 2025 21:40:55 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:a46b263c2cce2b762d073f453a72c33eb474d71183208ed22ebccb7841b9309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604372811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cc62b570c4d03e5e28a7b9abaeec07a8d1a0681c67877cdd087f829e8b5543`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Tue, 29 Apr 2025 00:01:21 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Tue, 29 Apr 2025 02:58:48 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfe8bd3e826ba76e4ad73b0a5ce638276af95b860bec9b25c2754c5600c5a61`  
		Last Modified: Tue, 29 Apr 2025 05:34:00 GMT  
		Size: 183.4 MB (183405963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589f590c508c398e3740adc2dd1d0915bdc9a36f36693dacb7d2cb83012bcca1`  
		Last Modified: Thu, 15 May 2025 23:34:36 GMT  
		Size: 286.3 MB (286310328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:0bb2f2b59196707a888cfccbc092b473f6e382739d12c2db5d9117cd4f490b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15395439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61693f885fe5810811eb46994aa1af308f091912dc96214dad8fd6651bc00831`

```dockerfile
```

-	Layers:
	-	`sha256:011ca34cbff4dd90ea475c3878d26371312698ea04d43f7886f8598f7f924610`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 15.4 MB (15382300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4311afc8d95a09e62d7f51e2603140152c818532e8aa83db3b1545ef3d7a15`  
		Last Modified: Thu, 15 May 2025 23:34:30 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:989095388527710c84035fb19f851eee7c1ef3280f20885afaa3f1ca40c132a0
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
$ docker pull rust@sha256:bb40fab9222e04479fcdd45dd897df82c6ce527f1be367d7af26b9d8b0ef6a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304047247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed37a08d4804ab8dc49d922940d98831dba0a9ab0d064517c16d3e8ebc61028`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfee91a65ac6ac51500a0ec06fef619ed43fb695781fb524461a5c4d2d637da`  
		Last Modified: Wed, 21 May 2025 23:30:50 GMT  
		Size: 275.8 MB (275821917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:efe02561cb166afdf2b5ceff7aa87559a0d4305e49b91aaf2b14ecea3dfac430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98fcfc56b3317ccdbefec9a1d8a372664b2c3fcb175e2a68692eb79b093238e`

```dockerfile
```

-	Layers:
	-	`sha256:8b0b25427736858183a7036091af78fd2db2d997da37facb6e4d05aaeae085ac`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 4.0 MB (3984195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d91ce431f3e8f53deb758af58dcf2d0d526914b7e949edc4a9194ad60d84b79`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:9e29ea2079cecf087bbda1c2fd2ad61236b36515fa51c6ff29828e8720467d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.1 MB (320057803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc73805e0130280f517428c036ce3ef1b66e23f5cfc530e79e9523fff52a2da`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2affe51206b495c552876f1361055b5ba2ba5c499a12dc799182e527f88fee8f`  
		Last Modified: Fri, 16 May 2025 00:47:33 GMT  
		Size: 296.1 MB (296119729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:7f307223876a0415ebe98e4232538d19ba2dfd94a4587afd1b6625bc10411268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b85b7e64240d9a4922e80471ff1f6d7ddf3fa2df0e3d30083ee3421d6afb6f`

```dockerfile
```

-	Layers:
	-	`sha256:8533123b469cd2f37a235ff4ae7f91614ee1dd9a8b02d36fd1828d5275843a82`  
		Last Modified: Fri, 16 May 2025 00:47:27 GMT  
		Size: 3.8 MB (3798367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3d2d35d257570cf330e2e8c1696e66fc0e1c593229df7b7735be317bae3977`  
		Last Modified: Fri, 16 May 2025 00:47:26 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:e42c600982c6907c6953b3067f6c48033e395f4d10181943c51ebac2f7f23bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267996219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3084e189f23691ae93614b7982a7e2cac388bca91738c5669989e7d8b796f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed633d6741d291fe9a1763e68d2cccb161b0647cba3b92db34f2082a23b9e0e5`  
		Last Modified: Thu, 15 May 2025 21:25:02 GMT  
		Size: 239.9 MB (239929597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:49d4587422ab4bfcf0173cab06c43b80c8984a7ab4c06e5735771535306cbd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4019635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ed220b85632009846640d2295c2f4ab23f854fa0b42e0c3243b5cefdd747ae`

```dockerfile
```

-	Layers:
	-	`sha256:3554280116bde06c2a965fd24a497d66881cd9d1aa281871d1b73769d8a2094d`  
		Last Modified: Thu, 15 May 2025 21:24:57 GMT  
		Size: 4.0 MB (4006212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec9148c526a826a45ec9302a772ebcdbad438372587030aeb75898a207f5529`  
		Last Modified: Thu, 15 May 2025 21:24:56 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:ba53dc2028f64403c6bd2a89614ec2e82ac8573537c865976e2cc6374ec2029b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325373122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2b704e3adfa1d07aa1cbc2987edbfeecfa1944de3fb2c3a968bd74c02ec417`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814ea34b52869e575de48c99d2f39a24d0e4d29694d8f3a01507831f57c2b06d`  
		Last Modified: Wed, 21 May 2025 23:24:41 GMT  
		Size: 296.2 MB (296165635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:889b0b25c9982cd5fd0571c6b2e686ec647c319ecab6c6d5a7adb6d0d6435a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3976779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8904643b41a0647ba565c4644b3392f328605ea998f3baade734ba5d2aacb870`

```dockerfile
```

-	Layers:
	-	`sha256:b1c6f53dcb1207b295e2a9b9c928c3d427f03fff1cda3c59d8cb153c959edd63`  
		Last Modified: Wed, 21 May 2025 23:24:35 GMT  
		Size: 4.0 MB (3963560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f37c60466f2e78fb30d52c14fbff69ffd5e0acccfafbf0eeb4d5f39c371cb4`  
		Last Modified: Wed, 21 May 2025 23:24:34 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:73839fb86f1fecdfa502eed34acc218fa19ea5b56c0c32411ea7a21108c4cd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377784662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3902494a5ed4edbc6b7649c8b67f6216b185ab73ac30aeb3191240f8c20079b2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf472daa2685f63de3e031e0501577d5082ab01e4cd68a594850d5b117971ab4`  
		Last Modified: Thu, 15 May 2025 21:44:03 GMT  
		Size: 345.7 MB (345716219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:b15ebebde5337a1f5f6d3035e50b978c23924c91ade52b89e87fb0ea78553cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38b8f6da58da02263499e3598466193030911e6f0ffd21726d6f52111dd4a5c`

```dockerfile
```

-	Layers:
	-	`sha256:045d5e4d7f1b02b270f2b39f6cfdc49b5cb491134b55b9308ddaa4bf79f39391`  
		Last Modified: Thu, 15 May 2025 21:43:49 GMT  
		Size: 4.0 MB (3956177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53809675a1cc4de34fd12f811d8d666321a4623ebb988f23833edcee8fbc1ef`  
		Last Modified: Thu, 15 May 2025 21:43:48 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:868e7478c67c722493268ef41b4427522279fa6a35f66461fd7adb0bf9e2c4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363329795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8621a9920839bcfdc5e9493f7408dca1bba5d13e97372f25dcb2828d0cab627`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf4c9ebe75ad00b908f5c783b4815794956bf90232cc34953f0a5744f19b699`  
		Last Modified: Thu, 22 May 2025 03:36:09 GMT  
		Size: 336.4 MB (336446987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:7a4f9ef8212aa8a7d6456c13e712c2838ea2d37473e5dc052a89f5fde72edc28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6469567669efec36515c9f38ed52cb7510dea8dc20939991a8486e11898c4ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff31c08b679c1c5a077d7a557e36813d9be82c5bbc22efbc845d709dd07bfacf`  
		Last Modified: Thu, 22 May 2025 03:36:05 GMT  
		Size: 3.8 MB (3824766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a9a671478833eaf718e74615d4a29101183eeab0898f719807cd0c3a261e6d`  
		Last Modified: Thu, 22 May 2025 03:36:04 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:989095388527710c84035fb19f851eee7c1ef3280f20885afaa3f1ca40c132a0
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
$ docker pull rust@sha256:bb40fab9222e04479fcdd45dd897df82c6ce527f1be367d7af26b9d8b0ef6a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304047247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed37a08d4804ab8dc49d922940d98831dba0a9ab0d064517c16d3e8ebc61028`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfee91a65ac6ac51500a0ec06fef619ed43fb695781fb524461a5c4d2d637da`  
		Last Modified: Wed, 21 May 2025 23:30:50 GMT  
		Size: 275.8 MB (275821917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:efe02561cb166afdf2b5ceff7aa87559a0d4305e49b91aaf2b14ecea3dfac430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98fcfc56b3317ccdbefec9a1d8a372664b2c3fcb175e2a68692eb79b093238e`

```dockerfile
```

-	Layers:
	-	`sha256:8b0b25427736858183a7036091af78fd2db2d997da37facb6e4d05aaeae085ac`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 4.0 MB (3984195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d91ce431f3e8f53deb758af58dcf2d0d526914b7e949edc4a9194ad60d84b79`  
		Last Modified: Wed, 21 May 2025 23:30:44 GMT  
		Size: 13.3 KB (13271 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:9e29ea2079cecf087bbda1c2fd2ad61236b36515fa51c6ff29828e8720467d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.1 MB (320057803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc73805e0130280f517428c036ce3ef1b66e23f5cfc530e79e9523fff52a2da`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2affe51206b495c552876f1361055b5ba2ba5c499a12dc799182e527f88fee8f`  
		Last Modified: Fri, 16 May 2025 00:47:33 GMT  
		Size: 296.1 MB (296119729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7f307223876a0415ebe98e4232538d19ba2dfd94a4587afd1b6625bc10411268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b85b7e64240d9a4922e80471ff1f6d7ddf3fa2df0e3d30083ee3421d6afb6f`

```dockerfile
```

-	Layers:
	-	`sha256:8533123b469cd2f37a235ff4ae7f91614ee1dd9a8b02d36fd1828d5275843a82`  
		Last Modified: Fri, 16 May 2025 00:47:27 GMT  
		Size: 3.8 MB (3798367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3d2d35d257570cf330e2e8c1696e66fc0e1c593229df7b7735be317bae3977`  
		Last Modified: Fri, 16 May 2025 00:47:26 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:e42c600982c6907c6953b3067f6c48033e395f4d10181943c51ebac2f7f23bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267996219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3084e189f23691ae93614b7982a7e2cac388bca91738c5669989e7d8b796f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed633d6741d291fe9a1763e68d2cccb161b0647cba3b92db34f2082a23b9e0e5`  
		Last Modified: Thu, 15 May 2025 21:25:02 GMT  
		Size: 239.9 MB (239929597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:49d4587422ab4bfcf0173cab06c43b80c8984a7ab4c06e5735771535306cbd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4019635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ed220b85632009846640d2295c2f4ab23f854fa0b42e0c3243b5cefdd747ae`

```dockerfile
```

-	Layers:
	-	`sha256:3554280116bde06c2a965fd24a497d66881cd9d1aa281871d1b73769d8a2094d`  
		Last Modified: Thu, 15 May 2025 21:24:57 GMT  
		Size: 4.0 MB (4006212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec9148c526a826a45ec9302a772ebcdbad438372587030aeb75898a207f5529`  
		Last Modified: Thu, 15 May 2025 21:24:56 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:ba53dc2028f64403c6bd2a89614ec2e82ac8573537c865976e2cc6374ec2029b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325373122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2b704e3adfa1d07aa1cbc2987edbfeecfa1944de3fb2c3a968bd74c02ec417`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814ea34b52869e575de48c99d2f39a24d0e4d29694d8f3a01507831f57c2b06d`  
		Last Modified: Wed, 21 May 2025 23:24:41 GMT  
		Size: 296.2 MB (296165635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:889b0b25c9982cd5fd0571c6b2e686ec647c319ecab6c6d5a7adb6d0d6435a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3976779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8904643b41a0647ba565c4644b3392f328605ea998f3baade734ba5d2aacb870`

```dockerfile
```

-	Layers:
	-	`sha256:b1c6f53dcb1207b295e2a9b9c928c3d427f03fff1cda3c59d8cb153c959edd63`  
		Last Modified: Wed, 21 May 2025 23:24:35 GMT  
		Size: 4.0 MB (3963560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f37c60466f2e78fb30d52c14fbff69ffd5e0acccfafbf0eeb4d5f39c371cb4`  
		Last Modified: Wed, 21 May 2025 23:24:34 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:73839fb86f1fecdfa502eed34acc218fa19ea5b56c0c32411ea7a21108c4cd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377784662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3902494a5ed4edbc6b7649c8b67f6216b185ab73ac30aeb3191240f8c20079b2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf472daa2685f63de3e031e0501577d5082ab01e4cd68a594850d5b117971ab4`  
		Last Modified: Thu, 15 May 2025 21:44:03 GMT  
		Size: 345.7 MB (345716219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b15ebebde5337a1f5f6d3035e50b978c23924c91ade52b89e87fb0ea78553cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38b8f6da58da02263499e3598466193030911e6f0ffd21726d6f52111dd4a5c`

```dockerfile
```

-	Layers:
	-	`sha256:045d5e4d7f1b02b270f2b39f6cfdc49b5cb491134b55b9308ddaa4bf79f39391`  
		Last Modified: Thu, 15 May 2025 21:43:49 GMT  
		Size: 4.0 MB (3956177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53809675a1cc4de34fd12f811d8d666321a4623ebb988f23833edcee8fbc1ef`  
		Last Modified: Thu, 15 May 2025 21:43:48 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:868e7478c67c722493268ef41b4427522279fa6a35f66461fd7adb0bf9e2c4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363329795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8621a9920839bcfdc5e9493f7408dca1bba5d13e97372f25dcb2828d0cab627`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf4c9ebe75ad00b908f5c783b4815794956bf90232cc34953f0a5744f19b699`  
		Last Modified: Thu, 22 May 2025 03:36:09 GMT  
		Size: 336.4 MB (336446987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7a4f9ef8212aa8a7d6456c13e712c2838ea2d37473e5dc052a89f5fde72edc28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6469567669efec36515c9f38ed52cb7510dea8dc20939991a8486e11898c4ba`

```dockerfile
```

-	Layers:
	-	`sha256:ff31c08b679c1c5a077d7a557e36813d9be82c5bbc22efbc845d709dd07bfacf`  
		Last Modified: Thu, 22 May 2025 03:36:05 GMT  
		Size: 3.8 MB (3824766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a9a671478833eaf718e74615d4a29101183eeab0898f719807cd0c3a261e6d`  
		Last Modified: Thu, 22 May 2025 03:36:04 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:7b85733174e7e5bb18d04389fe4f44c0a2421001c0fac80e9b25856fa5b077e1
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
$ docker pull rust@sha256:97b80590a20d5c2eb07da85188192a7adef3f4f312522cbfd475c7de7bd82c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295463417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d550ef0b540bad33bf2ec9fb03f2c8e364e5380cd6213c65d4878abf01f3cf67`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf3b96d50315a23a39f84e3081e1253eab321a691d742d8baa3fc48a80f9ad0`  
		Last Modified: Wed, 21 May 2025 23:30:17 GMT  
		Size: 265.2 MB (265207477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7654398afe6d9c2ada6a00ed784165dda7ea2364aeee0713ceae8da91147f90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4213039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2e800891f1055bb4074ed0d02441fe6240edc04c0a2722808deb75b744d97b`

```dockerfile
```

-	Layers:
	-	`sha256:b8eb46c3c2dba7b7825cb14a2f20554b65d85f1b7982e36530088fe6645b473f`  
		Last Modified: Wed, 21 May 2025 23:30:13 GMT  
		Size: 4.2 MB (4201683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43919c7995c8288c67859032aefa9df80e945eb0051bf122fab252d5ab8603e8`  
		Last Modified: Wed, 21 May 2025 23:30:13 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:fb46a8886b184e63725f71cecc5b4447baf825554560e49a902be80aa0be12be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.9 MB (319898121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3c8bf9b7293d122263ddcf92e437f269123360707572d092aa873ff6acfe5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a398f3fb2a84d2f55ccffe98cc554e8b7b0e593b06e480a45942a14035707d5`  
		Last Modified: Fri, 16 May 2025 00:42:53 GMT  
		Size: 294.4 MB (294355694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ddb6be6bc9d103419637c3e37d63eca143fe0f3cbc083278b2c2ab7ab1ab2feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4022345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e3a4cd59da45b8ce03653bea73bd63dac2476592a9e36a5493e1fa31d8757`

```dockerfile
```

-	Layers:
	-	`sha256:902f97b8ad9a51f2adb68f88d234da7cd55c1af152e2cbb9dd297c05ffbb61c4`  
		Last Modified: Fri, 16 May 2025 00:42:47 GMT  
		Size: 4.0 MB (4010914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f026c959c784b691edc6db6bbf65f8700a3a83d8366c5c3a5b605c9a235852`  
		Last Modified: Fri, 16 May 2025 00:42:46 GMT  
		Size: 11.4 KB (11431 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:be38bf3c2d6e3a2b47825e6dd4d77cf20583eb6206683ed3b21b29a77b4da50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262677882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8f9f1aa711538c6de6c47c0267af7d5e46c3d9bdd4a57a7830ca2df5328f55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4830ced46110e2a304d2fa24aff7c40cee44a64b15cbd1602175d7528ba9dca9`  
		Last Modified: Thu, 15 May 2025 21:22:59 GMT  
		Size: 233.9 MB (233933237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7b7be60ffc119e22194697635f39ef3ecb1d40d4dcedd25ef4229bc08a999188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4210772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8fc5e814cbb7c4a39f70f39dbce6ebb5f6779ca231d8f1eb11d75367bfdd9b`

```dockerfile
```

-	Layers:
	-	`sha256:68e804f29c4c1759df1a8c3a9dcdc215b964624a74e91345ccf86bb1fa7d61de`  
		Last Modified: Thu, 15 May 2025 21:22:54 GMT  
		Size: 4.2 MB (4199312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fba59bcde4cb014edb46b31d61e90b7ae6a1d420dba63e342fab2115e5f4640`  
		Last Modified: Thu, 15 May 2025 21:22:53 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:6c6e66e31919c82fe7ea1b63e8d37f1b3b89a184a6c95c9c4a1433e39d84c8d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 MB (320512888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8dae71aa0ae8520f4e956746adc671bfb485dca203c82aa62b3d1a6a45d00c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452460d1c227bf7acc8aeb01051d54bfe06fb359bfc4c6ae3535ea37ea6e2d12`  
		Last Modified: Wed, 21 May 2025 23:24:38 GMT  
		Size: 289.3 MB (289323688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5d135ffd369ba51d29a1c421aeea4320644446c924c37fb843458a4188caca00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4202751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbdf2ab316bec0455185f0aa859a9e62785b877b4f0e81754f1f65734dc86a6`

```dockerfile
```

-	Layers:
	-	`sha256:46da1a092528e79eb79c8dfaac9bdc3cc88154152aa2ad577f97f5eedcea6360`  
		Last Modified: Wed, 21 May 2025 23:24:32 GMT  
		Size: 4.2 MB (4191427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270cf5ab3f0a6904e359a5f16f1ab8ffc19021fe328a31afce493aae98aa5bdd`  
		Last Modified: Wed, 21 May 2025 23:24:31 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json
