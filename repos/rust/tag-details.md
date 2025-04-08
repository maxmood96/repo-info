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
-	[`rust:1.86`](#rust186)
-	[`rust:1.86-alpine`](#rust186-alpine)
-	[`rust:1.86-alpine3.20`](#rust186-alpine320)
-	[`rust:1.86-alpine3.21`](#rust186-alpine321)
-	[`rust:1.86-bookworm`](#rust186-bookworm)
-	[`rust:1.86-bullseye`](#rust186-bullseye)
-	[`rust:1.86-slim`](#rust186-slim)
-	[`rust:1.86-slim-bookworm`](#rust186-slim-bookworm)
-	[`rust:1.86-slim-bullseye`](#rust186-slim-bullseye)
-	[`rust:1.86.0`](#rust1860)
-	[`rust:1.86.0-alpine`](#rust1860-alpine)
-	[`rust:1.86.0-alpine3.20`](#rust1860-alpine320)
-	[`rust:1.86.0-alpine3.21`](#rust1860-alpine321)
-	[`rust:1.86.0-bookworm`](#rust1860-bookworm)
-	[`rust:1.86.0-bullseye`](#rust1860-bullseye)
-	[`rust:1.86.0-slim`](#rust1860-slim)
-	[`rust:1.86.0-slim-bookworm`](#rust1860-slim-bookworm)
-	[`rust:1.86.0-slim-bullseye`](#rust1860-slim-bullseye)
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
$ docker pull rust@sha256:6a6dda669f020fa1fcb0903e37a049484fbf4b4699c8cb89db26ca030f475259
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
$ docker pull rust@sha256:e2c3cc250468c6290044b6f8b8254ac79219b17c3232804e4a79b651d0c031a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547073889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dee95e9b67a7bb176a7084f8e543e0ec50c67fee8c69770f9a8e20c659bca81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b617a119f8a27982374d94ec6eb3738ae3d38d6fc2c34c865813926cf596a621`  
		Last Modified: Tue, 08 Apr 2025 03:16:47 GMT  
		Size: 211.3 MB (211331550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74a39eb585dbe3732f07ffb8ce7351ff0725ce605cd0585470613834f464774`  
		Last Modified: Tue, 08 Apr 2025 04:21:31 GMT  
		Size: 198.8 MB (198844240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:3509ec4e64b314235325eee7ebafc7f34e2f3ed18cdd2db1ee62e45e56c88418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb7ce20ad7522cd62fcddacdcd2610e03d6632563b739d9cbb6971a476918e6`

```dockerfile
```

-	Layers:
	-	`sha256:769f4e29352c2ec152cb9cb46918f0fb247e33b661cc190886c060f1b9bb5662`  
		Last Modified: Tue, 08 Apr 2025 04:21:26 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f071db2499bcd484721f1239e87ae438c36ca8d5af3bb29b6b8c7758232701`  
		Last Modified: Tue, 08 Apr 2025 04:21:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:e2f34964c241e7ea71a854eb91e0b225a2418936648499283d14c73abae98a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542260031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16535fe936f9919d4b6beff652f4c5e4d3e625c13bfff7fa4247510f19399638`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a319072ea86a8c9aa06075cbf6677da28654a48a38fc6adb52aa04f271ddd06`  
		Last Modified: Tue, 18 Mar 2025 07:30:13 GMT  
		Size: 21.9 MB (21918018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f325c93a6cb0439e3bf485f3a1ca5c31cca2f6b205d5c37e15890e18b5fe0`  
		Last Modified: Tue, 18 Mar 2025 15:26:53 GMT  
		Size: 59.6 MB (59639263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407c08ebab5377348ed14160a63d8d957a380f355e742fcec3755c68baf9c20d`  
		Last Modified: Tue, 18 Mar 2025 16:12:56 GMT  
		Size: 175.3 MB (175309168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dd9c885e006c5ba163c1af9605526e79f2905da43c9de3a5037b5f4a902ee5`  
		Last Modified: Thu, 03 Apr 2025 17:15:51 GMT  
		Size: 241.2 MB (241215579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:dfebee42501bc9ae716db67f70571ab1c43cae2aa84b8465558968c336c7bb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15287641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea10ffe1f6ecb4c95a552c05741fc7bbfa6e7501c663039937ea61b2f769b014`

```dockerfile
```

-	Layers:
	-	`sha256:721c7e73d5bf649a41efdad2260e00c896508c024f704b6dc26802980b057621`  
		Last Modified: Thu, 03 Apr 2025 17:15:45 GMT  
		Size: 15.3 MB (15274394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771ebeb25304716d614718f27531976702dafcdae3ae12e4f819037aa9509b53`  
		Last Modified: Thu, 03 Apr 2025 17:15:44 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8489b54bc057a93babd8906b056fe4c67f0e77e1d19fc18eb8fca8305067ae26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506607013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead27b748614e277ca15ac3636b936d4e471ad7ecf24da4587ddf7ac3cd9f419`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9d474cce081e468bc6f85727459852112ba732fbbfe3236fae66c5fa8a5ed5`  
		Last Modified: Tue, 18 Mar 2025 14:10:35 GMT  
		Size: 202.8 MB (202753988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadb53c2ea73a273e0e6fe4e18341f4291c24756dcbee8ad109038b067c0f8f4`  
		Last Modified: Thu, 03 Apr 2025 17:13:37 GMT  
		Size: 167.6 MB (167648030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:a48df1ec2a1e0ba16e84f7bb2189beb15a1aa86dd28a81bd65acba1470f9482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a632aa94d376b315058678dfd1194d1f04a4d851360ec98e10a5ab1f8239f18e`

```dockerfile
```

-	Layers:
	-	`sha256:86d2e91568072d7cf8f5f4aae6ec90b5a8825cb28ef55a1a29fe724454047aa2`  
		Last Modified: Thu, 03 Apr 2025 17:13:34 GMT  
		Size: 15.5 MB (15498527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fe3ef790dced91066659ab58e76acdd4fdd0f583148f161765e84ac8014bc2`  
		Last Modified: Thu, 03 Apr 2025 17:13:33 GMT  
		Size: 13.3 KB (13289 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:b06f5a923b052f2fbce21856fac2a8cbd4526310f9a22fae41a0b52388579188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572973806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cbc7d1b2a98309adc0f9f209d81640bd7a80c92e6bb5f5d4cda79343bea281`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7cbed080b4cdef804ca7e1b5bf4f3bc870dbef54cd5c74053fef6b147056`  
		Last Modified: Tue, 08 Apr 2025 01:23:54 GMT  
		Size: 24.8 MB (24847203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ffc3e6085548412ccbe96cfa7c6e138ccc7724d5a764a6a99e732fca48b289`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 66.2 MB (66237424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8471ab4232bc51e32c08f3c8fae6e33670c6c77fa4a3359a48d05453051f93e`  
		Last Modified: Tue, 08 Apr 2025 03:17:21 GMT  
		Size: 210.3 MB (210267336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ab54bb87b446c157a467a30d193edfb918d405722cf4c7b60d8f93b3a06b1a`  
		Last Modified: Tue, 08 Apr 2025 04:21:02 GMT  
		Size: 222.1 MB (222143712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:efc9f3a3297418eaf506f8ea51750f360027cbb3201e9a77d7ca1e1baaf7dc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da045b658f2b336a573f002e616b2fc8c51911ed0e2cb15e088c1c739a37e94d`

```dockerfile
```

-	Layers:
	-	`sha256:41bae4c1c5e052f6bdf0a312634e204ce48fb5ed8ab4309743503426c887ad5b`  
		Last Modified: Tue, 08 Apr 2025 04:20:57 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85eac65f6e9308480c58b3d5c215045ff30d0e9566710981c869dfa18a5f49a`  
		Last Modified: Tue, 08 Apr 2025 04:20:56 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:0b20be231028bfd49a688c56aea6e25cf138c49012ce5addadc5bf68ad029674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628711168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c542d6616e2ce45fb4557eb923016df6ded64d6756d6212a69bbfdbfa2aeaf3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c3d0039c25f88e5b7c3da861e5a41bc617f045eff9521b410ceced36c47c971`  
		Last Modified: Mon, 17 Mar 2025 22:17:38 GMT  
		Size: 52.3 MB (52306033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b570e1ccee8c153bcd6622cbc7c9c8f1150932eca72b58d0e1d93a81c2d4b`  
		Last Modified: Tue, 18 Mar 2025 00:06:46 GMT  
		Size: 25.7 MB (25650089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3219f8cada3f1c641a91887b1112d0699cc708ea02d9c8f85a77e08659008bf`  
		Last Modified: Tue, 18 Mar 2025 07:04:49 GMT  
		Size: 69.8 MB (69844086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4c6aa27e302a908ce45a312c9a7c6eab49c831e12f24c5b4c29145d2d6ab77`  
		Last Modified: Tue, 18 Mar 2025 13:50:48 GMT  
		Size: 214.4 MB (214407742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794fac3bd448ad09edaa36a6cde07f66551a607b885eb53d5f2021f315d4f3a1`  
		Last Modified: Thu, 03 Apr 2025 17:12:22 GMT  
		Size: 266.5 MB (266503218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:bdcd78b6c3e9fe62dc32903e0e40321ad1dcb75565546a46b7fcb80c80d051a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b2473977886e04bd3f2fa7f647e75326f6f9692e51ddd99b58f5b6a3f33ce4`

```dockerfile
```

-	Layers:
	-	`sha256:285e9d5c95682b386fd734af5f45355fd2b768e4de10b666c7928c0865c17115`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 15.4 MB (15445052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2784c65f478f48009daf0d9be5e9eb15f877c29df9a514d10ae1f463b05d5abe`  
		Last Modified: Thu, 03 Apr 2025 17:12:02 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:f48c071cd1dbf6e7f913bd6786412be97c82f25dc7e07ec327777838a47a15ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611934465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7d2d1236345049aad144c2d5ba643f4117f44e14bc7d7a4cd83c3ec56235d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea48981a9fc9115877d4666b28ace59b31b650cc30850dc9dbcd586ba0a496cb`  
		Last Modified: Mon, 17 Mar 2025 22:26:07 GMT  
		Size: 47.1 MB (47127836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d2fcabaa2191a259a1c138c1eae49463f7916a91e0b0f61fdbaa5dba7f4e2`  
		Last Modified: Tue, 18 Mar 2025 02:53:59 GMT  
		Size: 24.0 MB (24007981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e4163fc9bb4b1cfe20bf3ee0f067c3cb219407f1ed0b91eb04a5759f702712`  
		Last Modified: Tue, 18 Mar 2025 05:55:51 GMT  
		Size: 63.5 MB (63498480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f2a6b02b0e41028d194dbcc5b64d0cad2bdb30fa6390057978ddcf6ef155f8`  
		Last Modified: Tue, 18 Mar 2025 09:15:15 GMT  
		Size: 183.4 MB (183397092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15db11f7134bcabfcadf4efd6f83b0adb817278124e7abf84c09e8f2ace4d0e`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 293.9 MB (293903076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:24e6102ed3718659338647ed86c5ef77a3aed787e69c279a8b5a161b2dcee7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15295779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d32f0eae7397ef0bb4dc33fd8d1fd800859d56d4071a54e533f4f5da705fdf`

```dockerfile
```

-	Layers:
	-	`sha256:3bc6a1475676787f936efb971e18c1fd827cc2e06dde956322e7e95e32062df1`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 15.3 MB (15282640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f55e26963096390aa8b80788e20cf1bfd491126b210047525a73c44588be51`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:541a1720c1cedddae9e17b4214075bf57c20bc7b176b4bba6bce3437c44d51ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:ce413e392ed6c282a76beb447bfccc104136a46f2655df2df41fc0f04654c309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316237247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61d786d9f9c5cca0ab287fa99b7679ad755421530a8e95a8bd2cda19a69b856`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5c777dc8267f16eea52cc33c64c7b185aefaaaa260043622010c6e05333fd7`  
		Last Modified: Thu, 03 Apr 2025 17:12:15 GMT  
		Size: 61.6 MB (61564834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e319873236c572a5816c152bdb5011118b8ae9c672790e2ec264fbaafa4ddf`  
		Last Modified: Thu, 03 Apr 2025 17:12:18 GMT  
		Size: 251.0 MB (251030166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:dec7a5b5c43f2a69e7e1cd89b74f027b8ba4ac636e6654f30374a8143acce18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f0eca96243ca4fe82ac8c256aa685c9ed10eac95db72e1b176381f13e144e2`

```dockerfile
```

-	Layers:
	-	`sha256:cbd99f0e8b79ec516d96f3aee08b442562fc75cac2649bcb0a800ea915a0714a`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfec6d6b7554872ae59d5b3dc085d0c9287383d5bcb072f16cb8ac7fb44efbc3`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:45e626fcf2ef7f58c8b112b01657060691996ab4b4b3432a3f119afc93dd3875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (319016934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e2d039a6466c76b77a98bc81bba79858b86a3e5ab8a7c040094a491246270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63214d4c52deb7cd72dfb7b8ee63339ab9ba46086f6c52f3fc22c42a4cc6354c`  
		Last Modified: Wed, 19 Mar 2025 01:06:39 GMT  
		Size: 59.1 MB (59101227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa19e22237227dd4aba81e7f9e8743ac6f1828d92265e2ab9769fc3af195e04`  
		Last Modified: Thu, 03 Apr 2025 17:17:12 GMT  
		Size: 255.9 MB (255922678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:632262d43e3f35ced6b1ab847cc01838d21e8088bcd90a00889666a132b432b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37903037391a8658de906154ce8a47191fa1a8bf38f2a28471f7947cbf39b9b0`

```dockerfile
```

-	Layers:
	-	`sha256:1b5a4bc32a00e922f7028b1c3560d72456d27fdbc45f6525d545f9f313f21c09`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0fbb2e69c51339ac830b15829e85032b03271d892d1327f0628435616478b9c`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:2ee35275aeaa2e438f34a0563f7931988f5c5254e2eeec562f95a60ca2a2e7c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:b07e0b6e63438f28b28ab8976881ae0a926af4da9fbe9288ed0fe69138690c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.0 MB (309972637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86009d33dc0da7a31e9d46f4f6954d7e7b0166da8ebbbdf47d6cbd1c09829847`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda11a1c7cdfc868caa20205c5191c9e175af463da2d48ab5c74561819b4cbea`  
		Last Modified: Thu, 03 Apr 2025 17:11:17 GMT  
		Size: 55.3 MB (55315639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55f3dceec5bf9dd5986d21f22e336fc8efccac71e961895a64688eb12863f3c`  
		Last Modified: Thu, 03 Apr 2025 17:11:22 GMT  
		Size: 251.0 MB (251030101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:c9ce1958f067088ab558b7b6319833afff6b777d67358dbcfe70b9da0efb7ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a217f7fcce5e6762e7f71ad217556d3f4a942e64e66b12b91b30c51c8734ffc`

```dockerfile
```

-	Layers:
	-	`sha256:fbf4d52494216492b9e0cbcae0e1ad2eb0b2153e57c111b027c08f966da96c79`  
		Last Modified: Thu, 03 Apr 2025 17:11:15 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d67dd3f9a37cf39335b9f2e242627d47bd6a5b1b6fcd8474b54957de8f8fd84`  
		Last Modified: Thu, 03 Apr 2025 17:11:14 GMT  
		Size: 10.7 KB (10713 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:28b8265454853aeb6fd5b4dfd02b0223f6349204f348663e2c7551fc9a984541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312964800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272469f2176bd29846696edd36f27ed458dcddadb03bd9b7967197df0e6d94e2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7362932bfc33faed0c84d60ed0d4aefe9e34b5b9366cfa2015a14c01e2604`  
		Last Modified: Wed, 19 Mar 2025 04:51:19 GMT  
		Size: 53.0 MB (52950559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da216a1abe7d23357c54f3c639e81a67652f254c496e34ca5ed47c3a49b9582`  
		Last Modified: Thu, 03 Apr 2025 17:16:01 GMT  
		Size: 255.9 MB (255923076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:be732f17ad9e5e6e7cf13ee3a78836ae6ffae078de73425995fd283f4a6f1e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8093eb3b99a9036476b177c449878affb005e2ea60bd33c51dfbba375427b1f`

```dockerfile
```

-	Layers:
	-	`sha256:8d233587293019133f0bd1ba7d43eb76c4ec6b3e670421c4e41787189d73c449`  
		Last Modified: Thu, 03 Apr 2025 17:15:55 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce0e73bdd8ebfaaec68f238d168a0405459eead3889f55c922f39f2bba99938`  
		Last Modified: Thu, 03 Apr 2025 17:15:55 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.21`

```console
$ docker pull rust@sha256:541a1720c1cedddae9e17b4214075bf57c20bc7b176b4bba6bce3437c44d51ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:ce413e392ed6c282a76beb447bfccc104136a46f2655df2df41fc0f04654c309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316237247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61d786d9f9c5cca0ab287fa99b7679ad755421530a8e95a8bd2cda19a69b856`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5c777dc8267f16eea52cc33c64c7b185aefaaaa260043622010c6e05333fd7`  
		Last Modified: Thu, 03 Apr 2025 17:12:15 GMT  
		Size: 61.6 MB (61564834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e319873236c572a5816c152bdb5011118b8ae9c672790e2ec264fbaafa4ddf`  
		Last Modified: Thu, 03 Apr 2025 17:12:18 GMT  
		Size: 251.0 MB (251030166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:dec7a5b5c43f2a69e7e1cd89b74f027b8ba4ac636e6654f30374a8143acce18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f0eca96243ca4fe82ac8c256aa685c9ed10eac95db72e1b176381f13e144e2`

```dockerfile
```

-	Layers:
	-	`sha256:cbd99f0e8b79ec516d96f3aee08b442562fc75cac2649bcb0a800ea915a0714a`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfec6d6b7554872ae59d5b3dc085d0c9287383d5bcb072f16cb8ac7fb44efbc3`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:45e626fcf2ef7f58c8b112b01657060691996ab4b4b3432a3f119afc93dd3875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (319016934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e2d039a6466c76b77a98bc81bba79858b86a3e5ab8a7c040094a491246270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63214d4c52deb7cd72dfb7b8ee63339ab9ba46086f6c52f3fc22c42a4cc6354c`  
		Last Modified: Wed, 19 Mar 2025 01:06:39 GMT  
		Size: 59.1 MB (59101227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa19e22237227dd4aba81e7f9e8743ac6f1828d92265e2ab9769fc3af195e04`  
		Last Modified: Thu, 03 Apr 2025 17:17:12 GMT  
		Size: 255.9 MB (255922678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:632262d43e3f35ced6b1ab847cc01838d21e8088bcd90a00889666a132b432b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37903037391a8658de906154ce8a47191fa1a8bf38f2a28471f7947cbf39b9b0`

```dockerfile
```

-	Layers:
	-	`sha256:1b5a4bc32a00e922f7028b1c3560d72456d27fdbc45f6525d545f9f313f21c09`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0fbb2e69c51339ac830b15829e85032b03271d892d1327f0628435616478b9c`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:6a6dda669f020fa1fcb0903e37a049484fbf4b4699c8cb89db26ca030f475259
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
$ docker pull rust@sha256:e2c3cc250468c6290044b6f8b8254ac79219b17c3232804e4a79b651d0c031a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547073889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dee95e9b67a7bb176a7084f8e543e0ec50c67fee8c69770f9a8e20c659bca81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b617a119f8a27982374d94ec6eb3738ae3d38d6fc2c34c865813926cf596a621`  
		Last Modified: Tue, 08 Apr 2025 03:16:47 GMT  
		Size: 211.3 MB (211331550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74a39eb585dbe3732f07ffb8ce7351ff0725ce605cd0585470613834f464774`  
		Last Modified: Tue, 08 Apr 2025 04:21:31 GMT  
		Size: 198.8 MB (198844240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3509ec4e64b314235325eee7ebafc7f34e2f3ed18cdd2db1ee62e45e56c88418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb7ce20ad7522cd62fcddacdcd2610e03d6632563b739d9cbb6971a476918e6`

```dockerfile
```

-	Layers:
	-	`sha256:769f4e29352c2ec152cb9cb46918f0fb247e33b661cc190886c060f1b9bb5662`  
		Last Modified: Tue, 08 Apr 2025 04:21:26 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f071db2499bcd484721f1239e87ae438c36ca8d5af3bb29b6b8c7758232701`  
		Last Modified: Tue, 08 Apr 2025 04:21:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:e2f34964c241e7ea71a854eb91e0b225a2418936648499283d14c73abae98a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542260031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16535fe936f9919d4b6beff652f4c5e4d3e625c13bfff7fa4247510f19399638`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a319072ea86a8c9aa06075cbf6677da28654a48a38fc6adb52aa04f271ddd06`  
		Last Modified: Tue, 18 Mar 2025 07:30:13 GMT  
		Size: 21.9 MB (21918018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f325c93a6cb0439e3bf485f3a1ca5c31cca2f6b205d5c37e15890e18b5fe0`  
		Last Modified: Tue, 18 Mar 2025 15:26:53 GMT  
		Size: 59.6 MB (59639263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407c08ebab5377348ed14160a63d8d957a380f355e742fcec3755c68baf9c20d`  
		Last Modified: Tue, 18 Mar 2025 16:12:56 GMT  
		Size: 175.3 MB (175309168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dd9c885e006c5ba163c1af9605526e79f2905da43c9de3a5037b5f4a902ee5`  
		Last Modified: Thu, 03 Apr 2025 17:15:51 GMT  
		Size: 241.2 MB (241215579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:dfebee42501bc9ae716db67f70571ab1c43cae2aa84b8465558968c336c7bb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15287641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea10ffe1f6ecb4c95a552c05741fc7bbfa6e7501c663039937ea61b2f769b014`

```dockerfile
```

-	Layers:
	-	`sha256:721c7e73d5bf649a41efdad2260e00c896508c024f704b6dc26802980b057621`  
		Last Modified: Thu, 03 Apr 2025 17:15:45 GMT  
		Size: 15.3 MB (15274394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771ebeb25304716d614718f27531976702dafcdae3ae12e4f819037aa9509b53`  
		Last Modified: Thu, 03 Apr 2025 17:15:44 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8489b54bc057a93babd8906b056fe4c67f0e77e1d19fc18eb8fca8305067ae26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506607013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead27b748614e277ca15ac3636b936d4e471ad7ecf24da4587ddf7ac3cd9f419`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9d474cce081e468bc6f85727459852112ba732fbbfe3236fae66c5fa8a5ed5`  
		Last Modified: Tue, 18 Mar 2025 14:10:35 GMT  
		Size: 202.8 MB (202753988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadb53c2ea73a273e0e6fe4e18341f4291c24756dcbee8ad109038b067c0f8f4`  
		Last Modified: Thu, 03 Apr 2025 17:13:37 GMT  
		Size: 167.6 MB (167648030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a48df1ec2a1e0ba16e84f7bb2189beb15a1aa86dd28a81bd65acba1470f9482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a632aa94d376b315058678dfd1194d1f04a4d851360ec98e10a5ab1f8239f18e`

```dockerfile
```

-	Layers:
	-	`sha256:86d2e91568072d7cf8f5f4aae6ec90b5a8825cb28ef55a1a29fe724454047aa2`  
		Last Modified: Thu, 03 Apr 2025 17:13:34 GMT  
		Size: 15.5 MB (15498527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fe3ef790dced91066659ab58e76acdd4fdd0f583148f161765e84ac8014bc2`  
		Last Modified: Thu, 03 Apr 2025 17:13:33 GMT  
		Size: 13.3 KB (13289 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:b06f5a923b052f2fbce21856fac2a8cbd4526310f9a22fae41a0b52388579188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572973806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cbc7d1b2a98309adc0f9f209d81640bd7a80c92e6bb5f5d4cda79343bea281`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7cbed080b4cdef804ca7e1b5bf4f3bc870dbef54cd5c74053fef6b147056`  
		Last Modified: Tue, 08 Apr 2025 01:23:54 GMT  
		Size: 24.8 MB (24847203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ffc3e6085548412ccbe96cfa7c6e138ccc7724d5a764a6a99e732fca48b289`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 66.2 MB (66237424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8471ab4232bc51e32c08f3c8fae6e33670c6c77fa4a3359a48d05453051f93e`  
		Last Modified: Tue, 08 Apr 2025 03:17:21 GMT  
		Size: 210.3 MB (210267336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ab54bb87b446c157a467a30d193edfb918d405722cf4c7b60d8f93b3a06b1a`  
		Last Modified: Tue, 08 Apr 2025 04:21:02 GMT  
		Size: 222.1 MB (222143712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:efc9f3a3297418eaf506f8ea51750f360027cbb3201e9a77d7ca1e1baaf7dc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da045b658f2b336a573f002e616b2fc8c51911ed0e2cb15e088c1c739a37e94d`

```dockerfile
```

-	Layers:
	-	`sha256:41bae4c1c5e052f6bdf0a312634e204ce48fb5ed8ab4309743503426c887ad5b`  
		Last Modified: Tue, 08 Apr 2025 04:20:57 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85eac65f6e9308480c58b3d5c215045ff30d0e9566710981c869dfa18a5f49a`  
		Last Modified: Tue, 08 Apr 2025 04:20:56 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:0b20be231028bfd49a688c56aea6e25cf138c49012ce5addadc5bf68ad029674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628711168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c542d6616e2ce45fb4557eb923016df6ded64d6756d6212a69bbfdbfa2aeaf3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c3d0039c25f88e5b7c3da861e5a41bc617f045eff9521b410ceced36c47c971`  
		Last Modified: Mon, 17 Mar 2025 22:17:38 GMT  
		Size: 52.3 MB (52306033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b570e1ccee8c153bcd6622cbc7c9c8f1150932eca72b58d0e1d93a81c2d4b`  
		Last Modified: Tue, 18 Mar 2025 00:06:46 GMT  
		Size: 25.7 MB (25650089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3219f8cada3f1c641a91887b1112d0699cc708ea02d9c8f85a77e08659008bf`  
		Last Modified: Tue, 18 Mar 2025 07:04:49 GMT  
		Size: 69.8 MB (69844086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4c6aa27e302a908ce45a312c9a7c6eab49c831e12f24c5b4c29145d2d6ab77`  
		Last Modified: Tue, 18 Mar 2025 13:50:48 GMT  
		Size: 214.4 MB (214407742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794fac3bd448ad09edaa36a6cde07f66551a607b885eb53d5f2021f315d4f3a1`  
		Last Modified: Thu, 03 Apr 2025 17:12:22 GMT  
		Size: 266.5 MB (266503218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bdcd78b6c3e9fe62dc32903e0e40321ad1dcb75565546a46b7fcb80c80d051a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b2473977886e04bd3f2fa7f647e75326f6f9692e51ddd99b58f5b6a3f33ce4`

```dockerfile
```

-	Layers:
	-	`sha256:285e9d5c95682b386fd734af5f45355fd2b768e4de10b666c7928c0865c17115`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 15.4 MB (15445052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2784c65f478f48009daf0d9be5e9eb15f877c29df9a514d10ae1f463b05d5abe`  
		Last Modified: Thu, 03 Apr 2025 17:12:02 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:f48c071cd1dbf6e7f913bd6786412be97c82f25dc7e07ec327777838a47a15ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611934465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7d2d1236345049aad144c2d5ba643f4117f44e14bc7d7a4cd83c3ec56235d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea48981a9fc9115877d4666b28ace59b31b650cc30850dc9dbcd586ba0a496cb`  
		Last Modified: Mon, 17 Mar 2025 22:26:07 GMT  
		Size: 47.1 MB (47127836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d2fcabaa2191a259a1c138c1eae49463f7916a91e0b0f61fdbaa5dba7f4e2`  
		Last Modified: Tue, 18 Mar 2025 02:53:59 GMT  
		Size: 24.0 MB (24007981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e4163fc9bb4b1cfe20bf3ee0f067c3cb219407f1ed0b91eb04a5759f702712`  
		Last Modified: Tue, 18 Mar 2025 05:55:51 GMT  
		Size: 63.5 MB (63498480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f2a6b02b0e41028d194dbcc5b64d0cad2bdb30fa6390057978ddcf6ef155f8`  
		Last Modified: Tue, 18 Mar 2025 09:15:15 GMT  
		Size: 183.4 MB (183397092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15db11f7134bcabfcadf4efd6f83b0adb817278124e7abf84c09e8f2ace4d0e`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 293.9 MB (293903076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:24e6102ed3718659338647ed86c5ef77a3aed787e69c279a8b5a161b2dcee7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15295779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d32f0eae7397ef0bb4dc33fd8d1fd800859d56d4071a54e533f4f5da705fdf`

```dockerfile
```

-	Layers:
	-	`sha256:3bc6a1475676787f936efb971e18c1fd827cc2e06dde956322e7e95e32062df1`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 15.3 MB (15282640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f55e26963096390aa8b80788e20cf1bfd491126b210047525a73c44588be51`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:7a8c32ed3e4407a50d35985e0602f42c1f78ea6ae13930e3ace8205d573fd43f
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
$ docker pull rust@sha256:19c3a05a2f4be47ee8cbce22c200f09a16a378a1150bd4019fa5f0ac630e609b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.2 MB (520218264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b03f8c11be37e006c1e9735f2cf80ff0be92fcb7662a408c1e380365e6fa1bb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7819131060d3c79e48555fb5b04fa584b86d2fb80e3ede0864c7e6bba7d87`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 15.8 MB (15763510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f843b455b9b7bececb5cfeb4ba5839d4aa47845ded1258734c375304df3d0`  
		Last Modified: Tue, 08 Apr 2025 02:13:52 GMT  
		Size: 54.8 MB (54755152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b731139994e4dbd527b938ba04d372fec4d9d7302e7f454003dc0b3485c05bb1`  
		Last Modified: Tue, 08 Apr 2025 03:17:23 GMT  
		Size: 197.1 MB (197105555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056d1ad25ed6f278ed43ffa359808bab69a55df6afc883e564cb8c8768160524`  
		Last Modified: Tue, 08 Apr 2025 04:21:23 GMT  
		Size: 198.8 MB (198845518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6eaea83e5ca843f5257ac5886c846ed9d2607868f4d96b02bb4d6dc390341595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15086810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf77a97c2724f28d4b6a8a0ba1ac79caafacb92bc07435739b9410c5315274d`

```dockerfile
```

-	Layers:
	-	`sha256:1f6c5eb822984d31b2a2285ca0d64cd1827a12c9a40dc33817afa4bb7094f578`  
		Last Modified: Tue, 08 Apr 2025 04:21:19 GMT  
		Size: 15.1 MB (15075561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70368749ca14fffe47e32e606e5c77ad9e0468cf7cd92010ccd9218052806e8c`  
		Last Modified: Tue, 08 Apr 2025 04:21:19 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:2355887e87ec08c9db4665d5856f0e5dde1a1b436d7ef1ebedbc71f6aa4288b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.1 MB (523115497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956da94b04af8a4f1ba79acfd8f8f637cb0251bd8292b6e013d0607a18f48f0a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c0fd1793bf8bc1764ff6503ad6f86ae0f1151de2bd8b7285b28dc6f5cc6001c3`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 49.0 MB (49026561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fd5d78189f9a0219a8d445519fe59067dcfa82b8799cf047c0b783ffa33a78`  
		Last Modified: Tue, 18 Mar 2025 07:26:06 GMT  
		Size: 14.7 MB (14674012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31183489ce2b77443c42eee08badb4a4fcf8ad4cef9299e71603f2239cb4064`  
		Last Modified: Tue, 18 Mar 2025 15:29:13 GMT  
		Size: 50.6 MB (50640225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6676c7b3b77e9e71cb741c5c04bfd9a595560092d9024884d0ce64c66f48bc6`  
		Last Modified: Tue, 18 Mar 2025 16:15:00 GMT  
		Size: 167.6 MB (167559857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b86ba427e0fae57b323d1a94b5942db3ef6663580549d5abeeaff2e6671eeb7`  
		Last Modified: Thu, 03 Apr 2025 17:11:34 GMT  
		Size: 241.2 MB (241214842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:02ad46142f4af7ad1d5deb91011c07cef40aa34ba654a2afff289dcec3b5edd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e693efb626079c5d179344964747f1db704955b930abdc9372eb60dd7d37b2`

```dockerfile
```

-	Layers:
	-	`sha256:fbf9e4eabc83ab73bf1172bd3b0216ea0257bad4e2bb7e7d735d5ad5ef2bccec`  
		Last Modified: Thu, 03 Apr 2025 17:11:29 GMT  
		Size: 14.9 MB (14874384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:897e8e84b1d8543de6c676fd27fe8bb89d0448b16d6464b9966887246a0ba0d4`  
		Last Modified: Thu, 03 Apr 2025 17:11:28 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:69d48decb7216958492661cea62057f649e080c0cd37360d4b74324867db6d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.3 MB (480316197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5114f900c5aa75bfd01846f195f411d4ccb4a7b272ad186738d04b0776e6a11`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645bc92dcf4a3c806f112acf0724041051eab86b13816f8d7286950facb47ec3`  
		Last Modified: Tue, 18 Mar 2025 05:00:00 GMT  
		Size: 15.5 MB (15544004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96fedce3b84d801b5eec66fa2ddb4a4653be64f8e04188e6e7ab37b6566bd34`  
		Last Modified: Tue, 18 Mar 2025 13:15:20 GMT  
		Size: 54.9 MB (54855429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15780e9924523e788780ac991f29afa248c22b09abb68f8a9945cf272b3dc84e`  
		Last Modified: Tue, 18 Mar 2025 14:12:21 GMT  
		Size: 190.0 MB (190020786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b53efaeee4c92c572f617852fe5add72eed90d7c8f3416dcaff2bdaf40c47af`  
		Last Modified: Thu, 03 Apr 2025 17:10:56 GMT  
		Size: 167.6 MB (167647584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d0b352a4def49f1720c30632fc5dd136d73b3e2f9b904e02471089d27a3d2497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d14e3af14e7f5e5a1d29988d0c4bcb918ce2cb76c209f37cf16cf8ab2a83f3d`

```dockerfile
```

-	Layers:
	-	`sha256:70f71d6a962c6cd40615d935896c2467b5730056acbdcc9132c27fde862a3401`  
		Last Modified: Thu, 03 Apr 2025 17:10:55 GMT  
		Size: 15.1 MB (15075853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90c75b489dac3fed9aabb83068b4b8336b7ed3e8eb253a534ae509cc7ed1ec2b`  
		Last Modified: Thu, 03 Apr 2025 17:10:52 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:3a72bca02f43cd0d9f449b127103aadd427ff987a9613b3bc088eeb699fee0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549154273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c1a99516c42e56ce0d8c4e9108af14a30bf714c00ba497fe5b0818adb0458`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ffef4e17cbc252fc170472ff3910647beec8b91ac9abe188d6595b2087a0dc`  
		Last Modified: Tue, 08 Apr 2025 01:24:12 GMT  
		Size: 16.3 MB (16267037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684d7ac3a47d27aefe42d135394e4d8b703fb530ab3bd2ad6ef78b8c9beaf885`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 56.0 MB (56047217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f57b5c68cdb07f2657d3893b6b23c64ea31a47747ad68a064ff80bc616fdb51`  
		Last Modified: Tue, 08 Apr 2025 03:26:01 GMT  
		Size: 200.0 MB (200010627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9965d6680dd77db10541dab74f8fa0b74081c35a96fba815ca735a5bdba30db6`  
		Last Modified: Tue, 08 Apr 2025 04:20:42 GMT  
		Size: 222.1 MB (222144927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3f64b6b5e44466afdb2e0b9bc6fc4d01da31c626355b88f65650f57c3c2b176f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15073805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f9a17691493fcbefe1257efebd05e75f9d2247b27d8e4c2f0787e67400b081`

```dockerfile
```

-	Layers:
	-	`sha256:70606c1f443921a19b7f1ccd2601da80840aab493bd5fe9990c855778aa67324`  
		Last Modified: Tue, 08 Apr 2025 04:20:38 GMT  
		Size: 15.1 MB (15062588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760624857aafbce57f9c110b4cd55c6efb77f9b6f390378e3518a694baed7386`  
		Last Modified: Tue, 08 Apr 2025 04:20:37 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:3f391b0678a6e0c88fd26f13e399c9c515ac47354e3cadfee7daee3b21651a4f
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
$ docker pull rust@sha256:41b809ac8846aeacb14ccb5dd79734dc6336b1e8888529c1e0a6d26931443b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297829415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b78d2068c9472719a39cfbd28a9e0133db41638ba76fb051d4920fd18f6357`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210bb45fea98f7e6faa766c3c761469f156896c67811f25bec9d45f29b1dcbf0`  
		Last Modified: Tue, 08 Apr 2025 01:35:04 GMT  
		Size: 269.6 MB (269602156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:dcbbf8a097555fecc6ee6d280575383a22bc6a9ab9d7c62b65bce2c5ac8b95b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4053ef871c854e51688a9e9d237bc0def61479d6a5e3fb1a875747ca86268418`

```dockerfile
```

-	Layers:
	-	`sha256:3a8e6fbc9faed90473194037bdf9c636eecebcd8b7aa883b8ce27862a1779d1c`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d055c2481171ed38a99a22ae56c4e7c2b1bd465a4daf50f1676878fc24ef3643`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:f2147dce0408c155cafde8cea27150a5716e908161387aa42d3d5cd5cc276e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313009317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfd2341a89215716ee5a10bd8b6d887794af904f07446e83403c73d9dc11c9a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f48bc660f38990c9b1a99eef7221c43c0941e46d2c77adb1059dcf83e133720`  
		Last Modified: Tue, 08 Apr 2025 16:49:54 GMT  
		Size: 289.1 MB (289071450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:d03db0f51b3c203366e2d84c10c12ecefa338936f585b5e4493d144c0dd27b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d1df47ee7b8d27a616f617be86cd4d2c4bf9e6bacc9d6fac6c37bd6e2f6dd3`

```dockerfile
```

-	Layers:
	-	`sha256:6390c2b58d4d8b999d967a77f6c60f6e39fb1edcc78af868a9d39f02ea9c65cf`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 3.8 MB (3772732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89d90b466102965ae43f68698343d7a6deca9a2fa42f42bbab5b189ff921d00`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea3f5851799ee3e8f16ab003ef563ccfb590e287eb7960ff91fe44688a3e587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261543175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f316977191bca409dac97a0cd223be43a03fac7acb153bafc4c857382a8ae29e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be93040355bf29c5c23f25725fbace42a8c4e87149f54781b767539dc20cf504`  
		Last Modified: Tue, 08 Apr 2025 10:49:02 GMT  
		Size: 233.5 MB (233476855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:7f6e5cdeadc7696bb55921e2a30219a5d48b483e09f9d698dd934b28bfa15ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4802987aca1475d13fc58155ab1989d5789510e7961ad326ff3f0c7a05e6fb99`

```dockerfile
```

-	Layers:
	-	`sha256:253b9ae3ce5e09b9e82ca1ac3fcbe67e8bd9332025c8e18c1badd9df3085b13c`  
		Last Modified: Tue, 08 Apr 2025 10:48:57 GMT  
		Size: 4.0 MB (3979012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd310d7f0f093aa881f6d6beb86fedbafca89eba3eabe30fe233daf93087a8c`  
		Last Modified: Tue, 08 Apr 2025 10:48:56 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:bb5180ab836d2b9765e970861a734726951e55b490d86045511c69cffe5dcd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318921500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1379b48bf43ced6ff1dc1e0bc7150af59edb7c1cdf3e52a2b612cb94b64bb124`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5717094e375a7a30cbfd95d79b71ae2e1e438a9b730fb27e48eb343d0b981a1`  
		Last Modified: Tue, 08 Apr 2025 01:29:40 GMT  
		Size: 289.7 MB (289710769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b34dca3bdc3700658baef2ef87246f01f1276f019a270f7d6651094d9ef5bd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58e87bde78e6421ad5701ed6e1895b2146e37f9ddbb710e6c3564c5aeaa912d`

```dockerfile
```

-	Layers:
	-	`sha256:3a5f365726ead50a517bb7a1e0a66f89be048dd83aa40e156c91402f469e650f`  
		Last Modified: Tue, 08 Apr 2025 01:29:33 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48c9848cb48320622ba069df1d248315014d723047a5ad2fe5c0984f63b29b4`  
		Last Modified: Tue, 08 Apr 2025 01:29:32 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:7c698b86ae28c62f50194162e6ce3ccb20929b7e102dcc9451daae302a190c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367337074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583a28a59a2f362110c00233e30bd9cbe585d26d44f01bae200b8bfcacbc3dd4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b1b3a088ca3ea201af18986b7436e4aec60625258327e913df52ff8591370`  
		Last Modified: Tue, 08 Apr 2025 07:30:39 GMT  
		Size: 335.3 MB (335268843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:053e7e4791aacc14950e3e3fd33978f493690d41cf4a6ce384c31f8a6b28e790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de63ee76d9cad60f0ede2a9ebfa9ceaa8033826728ff25b231320f60c2a513e`

```dockerfile
```

-	Layers:
	-	`sha256:cb9a48cc982aca824da80a9466474cea0ca2889c619a740a0966fefe497cfeab`  
		Last Modified: Tue, 08 Apr 2025 07:30:30 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae8c4b9df6ac332d20cd1be109d998ae230fe05ebf9b7f6ee2cfb308c2bcb6d3`  
		Last Modified: Tue, 08 Apr 2025 07:30:29 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:6fbc766b1eba2d9ee4174bf5728c3d5cdfa04d6bd77051944c5c0fd8bff0295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5e6a02c07dc29b10ca722271c932c061c30824d57f634c336d1ea35d41f4cf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37b16f2d003c1f9e67bd6dfda070e17bd22a162101f28a4396a958280daf695`  
		Last Modified: Tue, 08 Apr 2025 06:20:23 GMT  
		Size: 344.0 MB (344011347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:8547ff21e07816223e9f6766d42bea2cb69c579334e2ac18d625ac04749bb5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146d2be439c484209ca809cc8ce80871138fe27edf39a29a708fa317e8175305`

```dockerfile
```

-	Layers:
	-	`sha256:0b77fa511d03b0701d0ef55560b74a78f3f6e64e484e0095d3be54b544545131`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2add6570625fb08371b11c1a0bc8716a08b4fdd1ad3706bde7cf21f4d9323ff4`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:3f391b0678a6e0c88fd26f13e399c9c515ac47354e3cadfee7daee3b21651a4f
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
$ docker pull rust@sha256:41b809ac8846aeacb14ccb5dd79734dc6336b1e8888529c1e0a6d26931443b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297829415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b78d2068c9472719a39cfbd28a9e0133db41638ba76fb051d4920fd18f6357`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210bb45fea98f7e6faa766c3c761469f156896c67811f25bec9d45f29b1dcbf0`  
		Last Modified: Tue, 08 Apr 2025 01:35:04 GMT  
		Size: 269.6 MB (269602156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:dcbbf8a097555fecc6ee6d280575383a22bc6a9ab9d7c62b65bce2c5ac8b95b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4053ef871c854e51688a9e9d237bc0def61479d6a5e3fb1a875747ca86268418`

```dockerfile
```

-	Layers:
	-	`sha256:3a8e6fbc9faed90473194037bdf9c636eecebcd8b7aa883b8ce27862a1779d1c`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d055c2481171ed38a99a22ae56c4e7c2b1bd465a4daf50f1676878fc24ef3643`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:f2147dce0408c155cafde8cea27150a5716e908161387aa42d3d5cd5cc276e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313009317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfd2341a89215716ee5a10bd8b6d887794af904f07446e83403c73d9dc11c9a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f48bc660f38990c9b1a99eef7221c43c0941e46d2c77adb1059dcf83e133720`  
		Last Modified: Tue, 08 Apr 2025 16:49:54 GMT  
		Size: 289.1 MB (289071450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d03db0f51b3c203366e2d84c10c12ecefa338936f585b5e4493d144c0dd27b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d1df47ee7b8d27a616f617be86cd4d2c4bf9e6bacc9d6fac6c37bd6e2f6dd3`

```dockerfile
```

-	Layers:
	-	`sha256:6390c2b58d4d8b999d967a77f6c60f6e39fb1edcc78af868a9d39f02ea9c65cf`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 3.8 MB (3772732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89d90b466102965ae43f68698343d7a6deca9a2fa42f42bbab5b189ff921d00`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea3f5851799ee3e8f16ab003ef563ccfb590e287eb7960ff91fe44688a3e587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261543175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f316977191bca409dac97a0cd223be43a03fac7acb153bafc4c857382a8ae29e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be93040355bf29c5c23f25725fbace42a8c4e87149f54781b767539dc20cf504`  
		Last Modified: Tue, 08 Apr 2025 10:49:02 GMT  
		Size: 233.5 MB (233476855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7f6e5cdeadc7696bb55921e2a30219a5d48b483e09f9d698dd934b28bfa15ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4802987aca1475d13fc58155ab1989d5789510e7961ad326ff3f0c7a05e6fb99`

```dockerfile
```

-	Layers:
	-	`sha256:253b9ae3ce5e09b9e82ca1ac3fcbe67e8bd9332025c8e18c1badd9df3085b13c`  
		Last Modified: Tue, 08 Apr 2025 10:48:57 GMT  
		Size: 4.0 MB (3979012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd310d7f0f093aa881f6d6beb86fedbafca89eba3eabe30fe233daf93087a8c`  
		Last Modified: Tue, 08 Apr 2025 10:48:56 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:bb5180ab836d2b9765e970861a734726951e55b490d86045511c69cffe5dcd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318921500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1379b48bf43ced6ff1dc1e0bc7150af59edb7c1cdf3e52a2b612cb94b64bb124`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5717094e375a7a30cbfd95d79b71ae2e1e438a9b730fb27e48eb343d0b981a1`  
		Last Modified: Tue, 08 Apr 2025 01:29:40 GMT  
		Size: 289.7 MB (289710769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b34dca3bdc3700658baef2ef87246f01f1276f019a270f7d6651094d9ef5bd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58e87bde78e6421ad5701ed6e1895b2146e37f9ddbb710e6c3564c5aeaa912d`

```dockerfile
```

-	Layers:
	-	`sha256:3a5f365726ead50a517bb7a1e0a66f89be048dd83aa40e156c91402f469e650f`  
		Last Modified: Tue, 08 Apr 2025 01:29:33 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48c9848cb48320622ba069df1d248315014d723047a5ad2fe5c0984f63b29b4`  
		Last Modified: Tue, 08 Apr 2025 01:29:32 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:7c698b86ae28c62f50194162e6ce3ccb20929b7e102dcc9451daae302a190c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367337074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583a28a59a2f362110c00233e30bd9cbe585d26d44f01bae200b8bfcacbc3dd4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b1b3a088ca3ea201af18986b7436e4aec60625258327e913df52ff8591370`  
		Last Modified: Tue, 08 Apr 2025 07:30:39 GMT  
		Size: 335.3 MB (335268843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:053e7e4791aacc14950e3e3fd33978f493690d41cf4a6ce384c31f8a6b28e790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de63ee76d9cad60f0ede2a9ebfa9ceaa8033826728ff25b231320f60c2a513e`

```dockerfile
```

-	Layers:
	-	`sha256:cb9a48cc982aca824da80a9466474cea0ca2889c619a740a0966fefe497cfeab`  
		Last Modified: Tue, 08 Apr 2025 07:30:30 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae8c4b9df6ac332d20cd1be109d998ae230fe05ebf9b7f6ee2cfb308c2bcb6d3`  
		Last Modified: Tue, 08 Apr 2025 07:30:29 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:6fbc766b1eba2d9ee4174bf5728c3d5cdfa04d6bd77051944c5c0fd8bff0295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5e6a02c07dc29b10ca722271c932c061c30824d57f634c336d1ea35d41f4cf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37b16f2d003c1f9e67bd6dfda070e17bd22a162101f28a4396a958280daf695`  
		Last Modified: Tue, 08 Apr 2025 06:20:23 GMT  
		Size: 344.0 MB (344011347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8547ff21e07816223e9f6766d42bea2cb69c579334e2ac18d625ac04749bb5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146d2be439c484209ca809cc8ce80871138fe27edf39a29a708fa317e8175305`

```dockerfile
```

-	Layers:
	-	`sha256:0b77fa511d03b0701d0ef55560b74a78f3f6e64e484e0095d3be54b544545131`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2add6570625fb08371b11c1a0bc8716a08b4fdd1ad3706bde7cf21f4d9323ff4`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:405e5b0fe9f74098d19f3a7b65368c9cd4323758dd6b2d6305a35df8d2cc0a2a
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
$ docker pull rust@sha256:f8c0bb10d0e408141ae1ce9db3906933d04044014b81315956bb8babefdb4538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289245429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701ed3fc33b113775a941d354adccbf40b6a225401b883ee5966de1c83f41b2b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88fad72c2506246ffe6396d482cf40fced3dbdcef8f4356795a7cac8ff6b2ef`  
		Last Modified: Tue, 08 Apr 2025 01:35:00 GMT  
		Size: 259.0 MB (258988010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4741338f8e175f2156ac1827a7e205ed3ea2f97dab9e129c70963ec485678779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0edf37b8243573464db9fa035308a4066da5453afcc99b305823cb05f7a7437`

```dockerfile
```

-	Layers:
	-	`sha256:9eb94d3eacd1815973a9e0b2b8d9ea7e1aba5c23b593f6bc9dcc7afb1bdd484c`  
		Last Modified: Tue, 08 Apr 2025 01:34:55 GMT  
		Size: 4.2 MB (4175124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ba3cecfcf1347fea0549f31ad4367cab149129294dc8dfc57ccf6d6f0813fff`  
		Last Modified: Tue, 08 Apr 2025 01:34:55 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:64862b5819093237df39378fbaa1b43498424fab0bec03cae5733be1b24142b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.0 MB (309037855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6173382e6c055035ab42b01f20d2e1159bc44baf086271255b1ca3daf44909`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fabdae83abb8c4e7989a8005a7a92a8535e6ab6c0bd633442c316443e6f2bab`  
		Last Modified: Tue, 08 Apr 2025 16:53:16 GMT  
		Size: 283.5 MB (283498720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a1e648062c749afa43013786ee2772e71053aae03cb4782bbc4537e21bc45a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3995706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80946ceab5e2263d6a3d2080648d12b9fa299c11ee188d9f752f9d87cf949f4e`

```dockerfile
```

-	Layers:
	-	`sha256:82474d826cb3957f1fe6d11964dabb805591e256095862418b74e61335f2d2bb`  
		Last Modified: Tue, 08 Apr 2025 16:53:10 GMT  
		Size: 4.0 MB (3984274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c1e96c51cd14f17a15a43d875ce615aeb964e08b5edb459ce6c20c3722eb049`  
		Last Modified: Tue, 08 Apr 2025 16:53:09 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:663387b95b7c33a5430b967b31ff194fcdda0a1ce99f5b57701067a097d7790e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252089618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714f3327734efe4ca704111ca38e47742d41d1d6dbf7fd5f688890f0d51b0358`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae574b04e648f49bc601b389c9fe05b55820b884d921b0be2237f6bcbe8a3f94`  
		Last Modified: Tue, 08 Apr 2025 10:47:57 GMT  
		Size: 223.3 MB (223340120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:82d09db72e41c93ab2119868ef3741a813878f94117b474e06283adb390fbeab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4183262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544589af526ae2c336c2f08de66d4d92a1e44abc4a3bc1dc03656c481d5d7819`

```dockerfile
```

-	Layers:
	-	`sha256:b88826ea138c560bd03b90c875666115d0b79433cb4be2921f0d1aa605f9dc33`  
		Last Modified: Tue, 08 Apr 2025 10:47:52 GMT  
		Size: 4.2 MB (4171802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1ef1d405fbb2d4f000818000750480dae3e874eb9e5dd56ae60396665119ffe`  
		Last Modified: Tue, 08 Apr 2025 10:47:51 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:43df35999046bea8233d1a5fdfcd2356fba15a793fbeb9fa5224d1262adf2960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314097491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d34f303281cbb2b93f669a37283d0e2d6c0068957020ef6fa5232b882c63638`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c7f226a3ed9e3a783e859dc8479e50da2694130147ffb4885645e02664eedbec`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 31.2 MB (31184573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b380f9c572c29705a08754c4980a85f7915a4d9cd340d7f3c36e3926cba3001`  
		Last Modified: Tue, 08 Apr 2025 01:29:00 GMT  
		Size: 282.9 MB (282912918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:19d00c62057a0ddf1ba7ff04c110803c0702d91dcdad6a4eed7e9ff8f85cc8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80ca8b84c676afa150db9ce38fd1bfaca44431b98cdac4af32efe184523a8ca`

```dockerfile
```

-	Layers:
	-	`sha256:80703f1c4e5c8b72cdde3f31569d00b27ba521369410893b3e2dbc529daa0b19`  
		Last Modified: Tue, 08 Apr 2025 01:28:53 GMT  
		Size: 4.2 MB (4165381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1fd41d56f3f22ed5780318a7bc49397260241142ba692570d227a36598e668b`  
		Last Modified: Tue, 08 Apr 2025 01:28:53 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86`

```console
$ docker pull rust@sha256:6a6dda669f020fa1fcb0903e37a049484fbf4b4699c8cb89db26ca030f475259
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

### `rust:1.86` - linux; amd64

```console
$ docker pull rust@sha256:e2c3cc250468c6290044b6f8b8254ac79219b17c3232804e4a79b651d0c031a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547073889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dee95e9b67a7bb176a7084f8e543e0ec50c67fee8c69770f9a8e20c659bca81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b617a119f8a27982374d94ec6eb3738ae3d38d6fc2c34c865813926cf596a621`  
		Last Modified: Tue, 08 Apr 2025 03:16:47 GMT  
		Size: 211.3 MB (211331550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74a39eb585dbe3732f07ffb8ce7351ff0725ce605cd0585470613834f464774`  
		Last Modified: Tue, 08 Apr 2025 04:21:31 GMT  
		Size: 198.8 MB (198844240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86` - unknown; unknown

```console
$ docker pull rust@sha256:3509ec4e64b314235325eee7ebafc7f34e2f3ed18cdd2db1ee62e45e56c88418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb7ce20ad7522cd62fcddacdcd2610e03d6632563b739d9cbb6971a476918e6`

```dockerfile
```

-	Layers:
	-	`sha256:769f4e29352c2ec152cb9cb46918f0fb247e33b661cc190886c060f1b9bb5662`  
		Last Modified: Tue, 08 Apr 2025 04:21:26 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f071db2499bcd484721f1239e87ae438c36ca8d5af3bb29b6b8c7758232701`  
		Last Modified: Tue, 08 Apr 2025 04:21:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86` - linux; arm variant v7

```console
$ docker pull rust@sha256:e2f34964c241e7ea71a854eb91e0b225a2418936648499283d14c73abae98a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542260031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16535fe936f9919d4b6beff652f4c5e4d3e625c13bfff7fa4247510f19399638`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a319072ea86a8c9aa06075cbf6677da28654a48a38fc6adb52aa04f271ddd06`  
		Last Modified: Tue, 18 Mar 2025 07:30:13 GMT  
		Size: 21.9 MB (21918018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f325c93a6cb0439e3bf485f3a1ca5c31cca2f6b205d5c37e15890e18b5fe0`  
		Last Modified: Tue, 18 Mar 2025 15:26:53 GMT  
		Size: 59.6 MB (59639263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407c08ebab5377348ed14160a63d8d957a380f355e742fcec3755c68baf9c20d`  
		Last Modified: Tue, 18 Mar 2025 16:12:56 GMT  
		Size: 175.3 MB (175309168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dd9c885e006c5ba163c1af9605526e79f2905da43c9de3a5037b5f4a902ee5`  
		Last Modified: Thu, 03 Apr 2025 17:15:51 GMT  
		Size: 241.2 MB (241215579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86` - unknown; unknown

```console
$ docker pull rust@sha256:dfebee42501bc9ae716db67f70571ab1c43cae2aa84b8465558968c336c7bb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15287641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea10ffe1f6ecb4c95a552c05741fc7bbfa6e7501c663039937ea61b2f769b014`

```dockerfile
```

-	Layers:
	-	`sha256:721c7e73d5bf649a41efdad2260e00c896508c024f704b6dc26802980b057621`  
		Last Modified: Thu, 03 Apr 2025 17:15:45 GMT  
		Size: 15.3 MB (15274394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771ebeb25304716d614718f27531976702dafcdae3ae12e4f819037aa9509b53`  
		Last Modified: Thu, 03 Apr 2025 17:15:44 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8489b54bc057a93babd8906b056fe4c67f0e77e1d19fc18eb8fca8305067ae26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506607013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead27b748614e277ca15ac3636b936d4e471ad7ecf24da4587ddf7ac3cd9f419`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9d474cce081e468bc6f85727459852112ba732fbbfe3236fae66c5fa8a5ed5`  
		Last Modified: Tue, 18 Mar 2025 14:10:35 GMT  
		Size: 202.8 MB (202753988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadb53c2ea73a273e0e6fe4e18341f4291c24756dcbee8ad109038b067c0f8f4`  
		Last Modified: Thu, 03 Apr 2025 17:13:37 GMT  
		Size: 167.6 MB (167648030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86` - unknown; unknown

```console
$ docker pull rust@sha256:a48df1ec2a1e0ba16e84f7bb2189beb15a1aa86dd28a81bd65acba1470f9482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a632aa94d376b315058678dfd1194d1f04a4d851360ec98e10a5ab1f8239f18e`

```dockerfile
```

-	Layers:
	-	`sha256:86d2e91568072d7cf8f5f4aae6ec90b5a8825cb28ef55a1a29fe724454047aa2`  
		Last Modified: Thu, 03 Apr 2025 17:13:34 GMT  
		Size: 15.5 MB (15498527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fe3ef790dced91066659ab58e76acdd4fdd0f583148f161765e84ac8014bc2`  
		Last Modified: Thu, 03 Apr 2025 17:13:33 GMT  
		Size: 13.3 KB (13289 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86` - linux; 386

```console
$ docker pull rust@sha256:b06f5a923b052f2fbce21856fac2a8cbd4526310f9a22fae41a0b52388579188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572973806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cbc7d1b2a98309adc0f9f209d81640bd7a80c92e6bb5f5d4cda79343bea281`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7cbed080b4cdef804ca7e1b5bf4f3bc870dbef54cd5c74053fef6b147056`  
		Last Modified: Tue, 08 Apr 2025 01:23:54 GMT  
		Size: 24.8 MB (24847203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ffc3e6085548412ccbe96cfa7c6e138ccc7724d5a764a6a99e732fca48b289`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 66.2 MB (66237424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8471ab4232bc51e32c08f3c8fae6e33670c6c77fa4a3359a48d05453051f93e`  
		Last Modified: Tue, 08 Apr 2025 03:17:21 GMT  
		Size: 210.3 MB (210267336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ab54bb87b446c157a467a30d193edfb918d405722cf4c7b60d8f93b3a06b1a`  
		Last Modified: Tue, 08 Apr 2025 04:21:02 GMT  
		Size: 222.1 MB (222143712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86` - unknown; unknown

```console
$ docker pull rust@sha256:efc9f3a3297418eaf506f8ea51750f360027cbb3201e9a77d7ca1e1baaf7dc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da045b658f2b336a573f002e616b2fc8c51911ed0e2cb15e088c1c739a37e94d`

```dockerfile
```

-	Layers:
	-	`sha256:41bae4c1c5e052f6bdf0a312634e204ce48fb5ed8ab4309743503426c887ad5b`  
		Last Modified: Tue, 08 Apr 2025 04:20:57 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85eac65f6e9308480c58b3d5c215045ff30d0e9566710981c869dfa18a5f49a`  
		Last Modified: Tue, 08 Apr 2025 04:20:56 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86` - linux; ppc64le

```console
$ docker pull rust@sha256:0b20be231028bfd49a688c56aea6e25cf138c49012ce5addadc5bf68ad029674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628711168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c542d6616e2ce45fb4557eb923016df6ded64d6756d6212a69bbfdbfa2aeaf3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c3d0039c25f88e5b7c3da861e5a41bc617f045eff9521b410ceced36c47c971`  
		Last Modified: Mon, 17 Mar 2025 22:17:38 GMT  
		Size: 52.3 MB (52306033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b570e1ccee8c153bcd6622cbc7c9c8f1150932eca72b58d0e1d93a81c2d4b`  
		Last Modified: Tue, 18 Mar 2025 00:06:46 GMT  
		Size: 25.7 MB (25650089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3219f8cada3f1c641a91887b1112d0699cc708ea02d9c8f85a77e08659008bf`  
		Last Modified: Tue, 18 Mar 2025 07:04:49 GMT  
		Size: 69.8 MB (69844086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4c6aa27e302a908ce45a312c9a7c6eab49c831e12f24c5b4c29145d2d6ab77`  
		Last Modified: Tue, 18 Mar 2025 13:50:48 GMT  
		Size: 214.4 MB (214407742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794fac3bd448ad09edaa36a6cde07f66551a607b885eb53d5f2021f315d4f3a1`  
		Last Modified: Thu, 03 Apr 2025 17:12:22 GMT  
		Size: 266.5 MB (266503218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86` - unknown; unknown

```console
$ docker pull rust@sha256:bdcd78b6c3e9fe62dc32903e0e40321ad1dcb75565546a46b7fcb80c80d051a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b2473977886e04bd3f2fa7f647e75326f6f9692e51ddd99b58f5b6a3f33ce4`

```dockerfile
```

-	Layers:
	-	`sha256:285e9d5c95682b386fd734af5f45355fd2b768e4de10b666c7928c0865c17115`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 15.4 MB (15445052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2784c65f478f48009daf0d9be5e9eb15f877c29df9a514d10ae1f463b05d5abe`  
		Last Modified: Thu, 03 Apr 2025 17:12:02 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86` - linux; s390x

```console
$ docker pull rust@sha256:f48c071cd1dbf6e7f913bd6786412be97c82f25dc7e07ec327777838a47a15ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611934465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7d2d1236345049aad144c2d5ba643f4117f44e14bc7d7a4cd83c3ec56235d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea48981a9fc9115877d4666b28ace59b31b650cc30850dc9dbcd586ba0a496cb`  
		Last Modified: Mon, 17 Mar 2025 22:26:07 GMT  
		Size: 47.1 MB (47127836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d2fcabaa2191a259a1c138c1eae49463f7916a91e0b0f61fdbaa5dba7f4e2`  
		Last Modified: Tue, 18 Mar 2025 02:53:59 GMT  
		Size: 24.0 MB (24007981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e4163fc9bb4b1cfe20bf3ee0f067c3cb219407f1ed0b91eb04a5759f702712`  
		Last Modified: Tue, 18 Mar 2025 05:55:51 GMT  
		Size: 63.5 MB (63498480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f2a6b02b0e41028d194dbcc5b64d0cad2bdb30fa6390057978ddcf6ef155f8`  
		Last Modified: Tue, 18 Mar 2025 09:15:15 GMT  
		Size: 183.4 MB (183397092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15db11f7134bcabfcadf4efd6f83b0adb817278124e7abf84c09e8f2ace4d0e`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 293.9 MB (293903076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86` - unknown; unknown

```console
$ docker pull rust@sha256:24e6102ed3718659338647ed86c5ef77a3aed787e69c279a8b5a161b2dcee7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15295779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d32f0eae7397ef0bb4dc33fd8d1fd800859d56d4071a54e533f4f5da705fdf`

```dockerfile
```

-	Layers:
	-	`sha256:3bc6a1475676787f936efb971e18c1fd827cc2e06dde956322e7e95e32062df1`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 15.3 MB (15282640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f55e26963096390aa8b80788e20cf1bfd491126b210047525a73c44588be51`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86-alpine`

```console
$ docker pull rust@sha256:541a1720c1cedddae9e17b4214075bf57c20bc7b176b4bba6bce3437c44d51ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.86-alpine` - linux; amd64

```console
$ docker pull rust@sha256:ce413e392ed6c282a76beb447bfccc104136a46f2655df2df41fc0f04654c309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316237247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61d786d9f9c5cca0ab287fa99b7679ad755421530a8e95a8bd2cda19a69b856`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5c777dc8267f16eea52cc33c64c7b185aefaaaa260043622010c6e05333fd7`  
		Last Modified: Thu, 03 Apr 2025 17:12:15 GMT  
		Size: 61.6 MB (61564834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e319873236c572a5816c152bdb5011118b8ae9c672790e2ec264fbaafa4ddf`  
		Last Modified: Thu, 03 Apr 2025 17:12:18 GMT  
		Size: 251.0 MB (251030166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:dec7a5b5c43f2a69e7e1cd89b74f027b8ba4ac636e6654f30374a8143acce18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f0eca96243ca4fe82ac8c256aa685c9ed10eac95db72e1b176381f13e144e2`

```dockerfile
```

-	Layers:
	-	`sha256:cbd99f0e8b79ec516d96f3aee08b442562fc75cac2649bcb0a800ea915a0714a`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfec6d6b7554872ae59d5b3dc085d0c9287383d5bcb072f16cb8ac7fb44efbc3`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:45e626fcf2ef7f58c8b112b01657060691996ab4b4b3432a3f119afc93dd3875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (319016934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e2d039a6466c76b77a98bc81bba79858b86a3e5ab8a7c040094a491246270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63214d4c52deb7cd72dfb7b8ee63339ab9ba46086f6c52f3fc22c42a4cc6354c`  
		Last Modified: Wed, 19 Mar 2025 01:06:39 GMT  
		Size: 59.1 MB (59101227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa19e22237227dd4aba81e7f9e8743ac6f1828d92265e2ab9769fc3af195e04`  
		Last Modified: Thu, 03 Apr 2025 17:17:12 GMT  
		Size: 255.9 MB (255922678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:632262d43e3f35ced6b1ab847cc01838d21e8088bcd90a00889666a132b432b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37903037391a8658de906154ce8a47191fa1a8bf38f2a28471f7947cbf39b9b0`

```dockerfile
```

-	Layers:
	-	`sha256:1b5a4bc32a00e922f7028b1c3560d72456d27fdbc45f6525d545f9f313f21c09`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0fbb2e69c51339ac830b15829e85032b03271d892d1327f0628435616478b9c`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86-alpine3.20`

```console
$ docker pull rust@sha256:2ee35275aeaa2e438f34a0563f7931988f5c5254e2eeec562f95a60ca2a2e7c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.86-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:b07e0b6e63438f28b28ab8976881ae0a926af4da9fbe9288ed0fe69138690c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.0 MB (309972637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86009d33dc0da7a31e9d46f4f6954d7e7b0166da8ebbbdf47d6cbd1c09829847`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda11a1c7cdfc868caa20205c5191c9e175af463da2d48ab5c74561819b4cbea`  
		Last Modified: Thu, 03 Apr 2025 17:11:17 GMT  
		Size: 55.3 MB (55315639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55f3dceec5bf9dd5986d21f22e336fc8efccac71e961895a64688eb12863f3c`  
		Last Modified: Thu, 03 Apr 2025 17:11:22 GMT  
		Size: 251.0 MB (251030101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:c9ce1958f067088ab558b7b6319833afff6b777d67358dbcfe70b9da0efb7ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a217f7fcce5e6762e7f71ad217556d3f4a942e64e66b12b91b30c51c8734ffc`

```dockerfile
```

-	Layers:
	-	`sha256:fbf4d52494216492b9e0cbcae0e1ad2eb0b2153e57c111b027c08f966da96c79`  
		Last Modified: Thu, 03 Apr 2025 17:11:15 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d67dd3f9a37cf39335b9f2e242627d47bd6a5b1b6fcd8474b54957de8f8fd84`  
		Last Modified: Thu, 03 Apr 2025 17:11:14 GMT  
		Size: 10.7 KB (10713 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:28b8265454853aeb6fd5b4dfd02b0223f6349204f348663e2c7551fc9a984541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312964800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272469f2176bd29846696edd36f27ed458dcddadb03bd9b7967197df0e6d94e2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7362932bfc33faed0c84d60ed0d4aefe9e34b5b9366cfa2015a14c01e2604`  
		Last Modified: Wed, 19 Mar 2025 04:51:19 GMT  
		Size: 53.0 MB (52950559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da216a1abe7d23357c54f3c639e81a67652f254c496e34ca5ed47c3a49b9582`  
		Last Modified: Thu, 03 Apr 2025 17:16:01 GMT  
		Size: 255.9 MB (255923076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:be732f17ad9e5e6e7cf13ee3a78836ae6ffae078de73425995fd283f4a6f1e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8093eb3b99a9036476b177c449878affb005e2ea60bd33c51dfbba375427b1f`

```dockerfile
```

-	Layers:
	-	`sha256:8d233587293019133f0bd1ba7d43eb76c4ec6b3e670421c4e41787189d73c449`  
		Last Modified: Thu, 03 Apr 2025 17:15:55 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce0e73bdd8ebfaaec68f238d168a0405459eead3889f55c922f39f2bba99938`  
		Last Modified: Thu, 03 Apr 2025 17:15:55 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86-alpine3.21`

```console
$ docker pull rust@sha256:541a1720c1cedddae9e17b4214075bf57c20bc7b176b4bba6bce3437c44d51ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.86-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:ce413e392ed6c282a76beb447bfccc104136a46f2655df2df41fc0f04654c309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316237247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61d786d9f9c5cca0ab287fa99b7679ad755421530a8e95a8bd2cda19a69b856`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5c777dc8267f16eea52cc33c64c7b185aefaaaa260043622010c6e05333fd7`  
		Last Modified: Thu, 03 Apr 2025 17:12:15 GMT  
		Size: 61.6 MB (61564834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e319873236c572a5816c152bdb5011118b8ae9c672790e2ec264fbaafa4ddf`  
		Last Modified: Thu, 03 Apr 2025 17:12:18 GMT  
		Size: 251.0 MB (251030166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:dec7a5b5c43f2a69e7e1cd89b74f027b8ba4ac636e6654f30374a8143acce18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f0eca96243ca4fe82ac8c256aa685c9ed10eac95db72e1b176381f13e144e2`

```dockerfile
```

-	Layers:
	-	`sha256:cbd99f0e8b79ec516d96f3aee08b442562fc75cac2649bcb0a800ea915a0714a`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfec6d6b7554872ae59d5b3dc085d0c9287383d5bcb072f16cb8ac7fb44efbc3`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:45e626fcf2ef7f58c8b112b01657060691996ab4b4b3432a3f119afc93dd3875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (319016934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e2d039a6466c76b77a98bc81bba79858b86a3e5ab8a7c040094a491246270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63214d4c52deb7cd72dfb7b8ee63339ab9ba46086f6c52f3fc22c42a4cc6354c`  
		Last Modified: Wed, 19 Mar 2025 01:06:39 GMT  
		Size: 59.1 MB (59101227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa19e22237227dd4aba81e7f9e8743ac6f1828d92265e2ab9769fc3af195e04`  
		Last Modified: Thu, 03 Apr 2025 17:17:12 GMT  
		Size: 255.9 MB (255922678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:632262d43e3f35ced6b1ab847cc01838d21e8088bcd90a00889666a132b432b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37903037391a8658de906154ce8a47191fa1a8bf38f2a28471f7947cbf39b9b0`

```dockerfile
```

-	Layers:
	-	`sha256:1b5a4bc32a00e922f7028b1c3560d72456d27fdbc45f6525d545f9f313f21c09`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0fbb2e69c51339ac830b15829e85032b03271d892d1327f0628435616478b9c`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86-bookworm`

```console
$ docker pull rust@sha256:6a6dda669f020fa1fcb0903e37a049484fbf4b4699c8cb89db26ca030f475259
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

### `rust:1.86-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:e2c3cc250468c6290044b6f8b8254ac79219b17c3232804e4a79b651d0c031a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547073889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dee95e9b67a7bb176a7084f8e543e0ec50c67fee8c69770f9a8e20c659bca81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b617a119f8a27982374d94ec6eb3738ae3d38d6fc2c34c865813926cf596a621`  
		Last Modified: Tue, 08 Apr 2025 03:16:47 GMT  
		Size: 211.3 MB (211331550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74a39eb585dbe3732f07ffb8ce7351ff0725ce605cd0585470613834f464774`  
		Last Modified: Tue, 08 Apr 2025 04:21:31 GMT  
		Size: 198.8 MB (198844240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3509ec4e64b314235325eee7ebafc7f34e2f3ed18cdd2db1ee62e45e56c88418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb7ce20ad7522cd62fcddacdcd2610e03d6632563b739d9cbb6971a476918e6`

```dockerfile
```

-	Layers:
	-	`sha256:769f4e29352c2ec152cb9cb46918f0fb247e33b661cc190886c060f1b9bb5662`  
		Last Modified: Tue, 08 Apr 2025 04:21:26 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f071db2499bcd484721f1239e87ae438c36ca8d5af3bb29b6b8c7758232701`  
		Last Modified: Tue, 08 Apr 2025 04:21:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:e2f34964c241e7ea71a854eb91e0b225a2418936648499283d14c73abae98a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542260031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16535fe936f9919d4b6beff652f4c5e4d3e625c13bfff7fa4247510f19399638`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a319072ea86a8c9aa06075cbf6677da28654a48a38fc6adb52aa04f271ddd06`  
		Last Modified: Tue, 18 Mar 2025 07:30:13 GMT  
		Size: 21.9 MB (21918018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f325c93a6cb0439e3bf485f3a1ca5c31cca2f6b205d5c37e15890e18b5fe0`  
		Last Modified: Tue, 18 Mar 2025 15:26:53 GMT  
		Size: 59.6 MB (59639263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407c08ebab5377348ed14160a63d8d957a380f355e742fcec3755c68baf9c20d`  
		Last Modified: Tue, 18 Mar 2025 16:12:56 GMT  
		Size: 175.3 MB (175309168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dd9c885e006c5ba163c1af9605526e79f2905da43c9de3a5037b5f4a902ee5`  
		Last Modified: Thu, 03 Apr 2025 17:15:51 GMT  
		Size: 241.2 MB (241215579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:dfebee42501bc9ae716db67f70571ab1c43cae2aa84b8465558968c336c7bb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15287641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea10ffe1f6ecb4c95a552c05741fc7bbfa6e7501c663039937ea61b2f769b014`

```dockerfile
```

-	Layers:
	-	`sha256:721c7e73d5bf649a41efdad2260e00c896508c024f704b6dc26802980b057621`  
		Last Modified: Thu, 03 Apr 2025 17:15:45 GMT  
		Size: 15.3 MB (15274394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771ebeb25304716d614718f27531976702dafcdae3ae12e4f819037aa9509b53`  
		Last Modified: Thu, 03 Apr 2025 17:15:44 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8489b54bc057a93babd8906b056fe4c67f0e77e1d19fc18eb8fca8305067ae26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506607013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead27b748614e277ca15ac3636b936d4e471ad7ecf24da4587ddf7ac3cd9f419`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9d474cce081e468bc6f85727459852112ba732fbbfe3236fae66c5fa8a5ed5`  
		Last Modified: Tue, 18 Mar 2025 14:10:35 GMT  
		Size: 202.8 MB (202753988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadb53c2ea73a273e0e6fe4e18341f4291c24756dcbee8ad109038b067c0f8f4`  
		Last Modified: Thu, 03 Apr 2025 17:13:37 GMT  
		Size: 167.6 MB (167648030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a48df1ec2a1e0ba16e84f7bb2189beb15a1aa86dd28a81bd65acba1470f9482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a632aa94d376b315058678dfd1194d1f04a4d851360ec98e10a5ab1f8239f18e`

```dockerfile
```

-	Layers:
	-	`sha256:86d2e91568072d7cf8f5f4aae6ec90b5a8825cb28ef55a1a29fe724454047aa2`  
		Last Modified: Thu, 03 Apr 2025 17:13:34 GMT  
		Size: 15.5 MB (15498527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fe3ef790dced91066659ab58e76acdd4fdd0f583148f161765e84ac8014bc2`  
		Last Modified: Thu, 03 Apr 2025 17:13:33 GMT  
		Size: 13.3 KB (13289 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bookworm` - linux; 386

```console
$ docker pull rust@sha256:b06f5a923b052f2fbce21856fac2a8cbd4526310f9a22fae41a0b52388579188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572973806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cbc7d1b2a98309adc0f9f209d81640bd7a80c92e6bb5f5d4cda79343bea281`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7cbed080b4cdef804ca7e1b5bf4f3bc870dbef54cd5c74053fef6b147056`  
		Last Modified: Tue, 08 Apr 2025 01:23:54 GMT  
		Size: 24.8 MB (24847203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ffc3e6085548412ccbe96cfa7c6e138ccc7724d5a764a6a99e732fca48b289`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 66.2 MB (66237424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8471ab4232bc51e32c08f3c8fae6e33670c6c77fa4a3359a48d05453051f93e`  
		Last Modified: Tue, 08 Apr 2025 03:17:21 GMT  
		Size: 210.3 MB (210267336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ab54bb87b446c157a467a30d193edfb918d405722cf4c7b60d8f93b3a06b1a`  
		Last Modified: Tue, 08 Apr 2025 04:21:02 GMT  
		Size: 222.1 MB (222143712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:efc9f3a3297418eaf506f8ea51750f360027cbb3201e9a77d7ca1e1baaf7dc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da045b658f2b336a573f002e616b2fc8c51911ed0e2cb15e088c1c739a37e94d`

```dockerfile
```

-	Layers:
	-	`sha256:41bae4c1c5e052f6bdf0a312634e204ce48fb5ed8ab4309743503426c887ad5b`  
		Last Modified: Tue, 08 Apr 2025 04:20:57 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85eac65f6e9308480c58b3d5c215045ff30d0e9566710981c869dfa18a5f49a`  
		Last Modified: Tue, 08 Apr 2025 04:20:56 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:0b20be231028bfd49a688c56aea6e25cf138c49012ce5addadc5bf68ad029674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628711168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c542d6616e2ce45fb4557eb923016df6ded64d6756d6212a69bbfdbfa2aeaf3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c3d0039c25f88e5b7c3da861e5a41bc617f045eff9521b410ceced36c47c971`  
		Last Modified: Mon, 17 Mar 2025 22:17:38 GMT  
		Size: 52.3 MB (52306033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b570e1ccee8c153bcd6622cbc7c9c8f1150932eca72b58d0e1d93a81c2d4b`  
		Last Modified: Tue, 18 Mar 2025 00:06:46 GMT  
		Size: 25.7 MB (25650089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3219f8cada3f1c641a91887b1112d0699cc708ea02d9c8f85a77e08659008bf`  
		Last Modified: Tue, 18 Mar 2025 07:04:49 GMT  
		Size: 69.8 MB (69844086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4c6aa27e302a908ce45a312c9a7c6eab49c831e12f24c5b4c29145d2d6ab77`  
		Last Modified: Tue, 18 Mar 2025 13:50:48 GMT  
		Size: 214.4 MB (214407742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794fac3bd448ad09edaa36a6cde07f66551a607b885eb53d5f2021f315d4f3a1`  
		Last Modified: Thu, 03 Apr 2025 17:12:22 GMT  
		Size: 266.5 MB (266503218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bdcd78b6c3e9fe62dc32903e0e40321ad1dcb75565546a46b7fcb80c80d051a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b2473977886e04bd3f2fa7f647e75326f6f9692e51ddd99b58f5b6a3f33ce4`

```dockerfile
```

-	Layers:
	-	`sha256:285e9d5c95682b386fd734af5f45355fd2b768e4de10b666c7928c0865c17115`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 15.4 MB (15445052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2784c65f478f48009daf0d9be5e9eb15f877c29df9a514d10ae1f463b05d5abe`  
		Last Modified: Thu, 03 Apr 2025 17:12:02 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:f48c071cd1dbf6e7f913bd6786412be97c82f25dc7e07ec327777838a47a15ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611934465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7d2d1236345049aad144c2d5ba643f4117f44e14bc7d7a4cd83c3ec56235d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea48981a9fc9115877d4666b28ace59b31b650cc30850dc9dbcd586ba0a496cb`  
		Last Modified: Mon, 17 Mar 2025 22:26:07 GMT  
		Size: 47.1 MB (47127836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d2fcabaa2191a259a1c138c1eae49463f7916a91e0b0f61fdbaa5dba7f4e2`  
		Last Modified: Tue, 18 Mar 2025 02:53:59 GMT  
		Size: 24.0 MB (24007981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e4163fc9bb4b1cfe20bf3ee0f067c3cb219407f1ed0b91eb04a5759f702712`  
		Last Modified: Tue, 18 Mar 2025 05:55:51 GMT  
		Size: 63.5 MB (63498480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f2a6b02b0e41028d194dbcc5b64d0cad2bdb30fa6390057978ddcf6ef155f8`  
		Last Modified: Tue, 18 Mar 2025 09:15:15 GMT  
		Size: 183.4 MB (183397092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15db11f7134bcabfcadf4efd6f83b0adb817278124e7abf84c09e8f2ace4d0e`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 293.9 MB (293903076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:24e6102ed3718659338647ed86c5ef77a3aed787e69c279a8b5a161b2dcee7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15295779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d32f0eae7397ef0bb4dc33fd8d1fd800859d56d4071a54e533f4f5da705fdf`

```dockerfile
```

-	Layers:
	-	`sha256:3bc6a1475676787f936efb971e18c1fd827cc2e06dde956322e7e95e32062df1`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 15.3 MB (15282640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f55e26963096390aa8b80788e20cf1bfd491126b210047525a73c44588be51`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86-bullseye`

```console
$ docker pull rust@sha256:7a8c32ed3e4407a50d35985e0602f42c1f78ea6ae13930e3ace8205d573fd43f
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

### `rust:1.86-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:19c3a05a2f4be47ee8cbce22c200f09a16a378a1150bd4019fa5f0ac630e609b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.2 MB (520218264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b03f8c11be37e006c1e9735f2cf80ff0be92fcb7662a408c1e380365e6fa1bb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7819131060d3c79e48555fb5b04fa584b86d2fb80e3ede0864c7e6bba7d87`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 15.8 MB (15763510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f843b455b9b7bececb5cfeb4ba5839d4aa47845ded1258734c375304df3d0`  
		Last Modified: Tue, 08 Apr 2025 02:13:52 GMT  
		Size: 54.8 MB (54755152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b731139994e4dbd527b938ba04d372fec4d9d7302e7f454003dc0b3485c05bb1`  
		Last Modified: Tue, 08 Apr 2025 03:17:23 GMT  
		Size: 197.1 MB (197105555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056d1ad25ed6f278ed43ffa359808bab69a55df6afc883e564cb8c8768160524`  
		Last Modified: Tue, 08 Apr 2025 04:21:23 GMT  
		Size: 198.8 MB (198845518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6eaea83e5ca843f5257ac5886c846ed9d2607868f4d96b02bb4d6dc390341595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15086810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf77a97c2724f28d4b6a8a0ba1ac79caafacb92bc07435739b9410c5315274d`

```dockerfile
```

-	Layers:
	-	`sha256:1f6c5eb822984d31b2a2285ca0d64cd1827a12c9a40dc33817afa4bb7094f578`  
		Last Modified: Tue, 08 Apr 2025 04:21:19 GMT  
		Size: 15.1 MB (15075561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70368749ca14fffe47e32e606e5c77ad9e0468cf7cd92010ccd9218052806e8c`  
		Last Modified: Tue, 08 Apr 2025 04:21:19 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:2355887e87ec08c9db4665d5856f0e5dde1a1b436d7ef1ebedbc71f6aa4288b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.1 MB (523115497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956da94b04af8a4f1ba79acfd8f8f637cb0251bd8292b6e013d0607a18f48f0a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c0fd1793bf8bc1764ff6503ad6f86ae0f1151de2bd8b7285b28dc6f5cc6001c3`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 49.0 MB (49026561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fd5d78189f9a0219a8d445519fe59067dcfa82b8799cf047c0b783ffa33a78`  
		Last Modified: Tue, 18 Mar 2025 07:26:06 GMT  
		Size: 14.7 MB (14674012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31183489ce2b77443c42eee08badb4a4fcf8ad4cef9299e71603f2239cb4064`  
		Last Modified: Tue, 18 Mar 2025 15:29:13 GMT  
		Size: 50.6 MB (50640225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6676c7b3b77e9e71cb741c5c04bfd9a595560092d9024884d0ce64c66f48bc6`  
		Last Modified: Tue, 18 Mar 2025 16:15:00 GMT  
		Size: 167.6 MB (167559857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b86ba427e0fae57b323d1a94b5942db3ef6663580549d5abeeaff2e6671eeb7`  
		Last Modified: Thu, 03 Apr 2025 17:11:34 GMT  
		Size: 241.2 MB (241214842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:02ad46142f4af7ad1d5deb91011c07cef40aa34ba654a2afff289dcec3b5edd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e693efb626079c5d179344964747f1db704955b930abdc9372eb60dd7d37b2`

```dockerfile
```

-	Layers:
	-	`sha256:fbf9e4eabc83ab73bf1172bd3b0216ea0257bad4e2bb7e7d735d5ad5ef2bccec`  
		Last Modified: Thu, 03 Apr 2025 17:11:29 GMT  
		Size: 14.9 MB (14874384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:897e8e84b1d8543de6c676fd27fe8bb89d0448b16d6464b9966887246a0ba0d4`  
		Last Modified: Thu, 03 Apr 2025 17:11:28 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:69d48decb7216958492661cea62057f649e080c0cd37360d4b74324867db6d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.3 MB (480316197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5114f900c5aa75bfd01846f195f411d4ccb4a7b272ad186738d04b0776e6a11`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645bc92dcf4a3c806f112acf0724041051eab86b13816f8d7286950facb47ec3`  
		Last Modified: Tue, 18 Mar 2025 05:00:00 GMT  
		Size: 15.5 MB (15544004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96fedce3b84d801b5eec66fa2ddb4a4653be64f8e04188e6e7ab37b6566bd34`  
		Last Modified: Tue, 18 Mar 2025 13:15:20 GMT  
		Size: 54.9 MB (54855429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15780e9924523e788780ac991f29afa248c22b09abb68f8a9945cf272b3dc84e`  
		Last Modified: Tue, 18 Mar 2025 14:12:21 GMT  
		Size: 190.0 MB (190020786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b53efaeee4c92c572f617852fe5add72eed90d7c8f3416dcaff2bdaf40c47af`  
		Last Modified: Thu, 03 Apr 2025 17:10:56 GMT  
		Size: 167.6 MB (167647584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d0b352a4def49f1720c30632fc5dd136d73b3e2f9b904e02471089d27a3d2497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d14e3af14e7f5e5a1d29988d0c4bcb918ce2cb76c209f37cf16cf8ab2a83f3d`

```dockerfile
```

-	Layers:
	-	`sha256:70f71d6a962c6cd40615d935896c2467b5730056acbdcc9132c27fde862a3401`  
		Last Modified: Thu, 03 Apr 2025 17:10:55 GMT  
		Size: 15.1 MB (15075853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90c75b489dac3fed9aabb83068b4b8336b7ed3e8eb253a534ae509cc7ed1ec2b`  
		Last Modified: Thu, 03 Apr 2025 17:10:52 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bullseye` - linux; 386

```console
$ docker pull rust@sha256:3a72bca02f43cd0d9f449b127103aadd427ff987a9613b3bc088eeb699fee0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549154273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c1a99516c42e56ce0d8c4e9108af14a30bf714c00ba497fe5b0818adb0458`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ffef4e17cbc252fc170472ff3910647beec8b91ac9abe188d6595b2087a0dc`  
		Last Modified: Tue, 08 Apr 2025 01:24:12 GMT  
		Size: 16.3 MB (16267037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684d7ac3a47d27aefe42d135394e4d8b703fb530ab3bd2ad6ef78b8c9beaf885`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 56.0 MB (56047217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f57b5c68cdb07f2657d3893b6b23c64ea31a47747ad68a064ff80bc616fdb51`  
		Last Modified: Tue, 08 Apr 2025 03:26:01 GMT  
		Size: 200.0 MB (200010627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9965d6680dd77db10541dab74f8fa0b74081c35a96fba815ca735a5bdba30db6`  
		Last Modified: Tue, 08 Apr 2025 04:20:42 GMT  
		Size: 222.1 MB (222144927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3f64b6b5e44466afdb2e0b9bc6fc4d01da31c626355b88f65650f57c3c2b176f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15073805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f9a17691493fcbefe1257efebd05e75f9d2247b27d8e4c2f0787e67400b081`

```dockerfile
```

-	Layers:
	-	`sha256:70606c1f443921a19b7f1ccd2601da80840aab493bd5fe9990c855778aa67324`  
		Last Modified: Tue, 08 Apr 2025 04:20:38 GMT  
		Size: 15.1 MB (15062588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760624857aafbce57f9c110b4cd55c6efb77f9b6f390378e3518a694baed7386`  
		Last Modified: Tue, 08 Apr 2025 04:20:37 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86-slim`

```console
$ docker pull rust@sha256:3f391b0678a6e0c88fd26f13e399c9c515ac47354e3cadfee7daee3b21651a4f
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

### `rust:1.86-slim` - linux; amd64

```console
$ docker pull rust@sha256:41b809ac8846aeacb14ccb5dd79734dc6336b1e8888529c1e0a6d26931443b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297829415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b78d2068c9472719a39cfbd28a9e0133db41638ba76fb051d4920fd18f6357`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210bb45fea98f7e6faa766c3c761469f156896c67811f25bec9d45f29b1dcbf0`  
		Last Modified: Tue, 08 Apr 2025 01:35:04 GMT  
		Size: 269.6 MB (269602156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim` - unknown; unknown

```console
$ docker pull rust@sha256:dcbbf8a097555fecc6ee6d280575383a22bc6a9ab9d7c62b65bce2c5ac8b95b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4053ef871c854e51688a9e9d237bc0def61479d6a5e3fb1a875747ca86268418`

```dockerfile
```

-	Layers:
	-	`sha256:3a8e6fbc9faed90473194037bdf9c636eecebcd8b7aa883b8ce27862a1779d1c`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d055c2481171ed38a99a22ae56c4e7c2b1bd465a4daf50f1676878fc24ef3643`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:f2147dce0408c155cafde8cea27150a5716e908161387aa42d3d5cd5cc276e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313009317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfd2341a89215716ee5a10bd8b6d887794af904f07446e83403c73d9dc11c9a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f48bc660f38990c9b1a99eef7221c43c0941e46d2c77adb1059dcf83e133720`  
		Last Modified: Tue, 08 Apr 2025 16:49:54 GMT  
		Size: 289.1 MB (289071450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim` - unknown; unknown

```console
$ docker pull rust@sha256:d03db0f51b3c203366e2d84c10c12ecefa338936f585b5e4493d144c0dd27b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d1df47ee7b8d27a616f617be86cd4d2c4bf9e6bacc9d6fac6c37bd6e2f6dd3`

```dockerfile
```

-	Layers:
	-	`sha256:6390c2b58d4d8b999d967a77f6c60f6e39fb1edcc78af868a9d39f02ea9c65cf`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 3.8 MB (3772732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89d90b466102965ae43f68698343d7a6deca9a2fa42f42bbab5b189ff921d00`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea3f5851799ee3e8f16ab003ef563ccfb590e287eb7960ff91fe44688a3e587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261543175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f316977191bca409dac97a0cd223be43a03fac7acb153bafc4c857382a8ae29e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be93040355bf29c5c23f25725fbace42a8c4e87149f54781b767539dc20cf504`  
		Last Modified: Tue, 08 Apr 2025 10:49:02 GMT  
		Size: 233.5 MB (233476855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim` - unknown; unknown

```console
$ docker pull rust@sha256:7f6e5cdeadc7696bb55921e2a30219a5d48b483e09f9d698dd934b28bfa15ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4802987aca1475d13fc58155ab1989d5789510e7961ad326ff3f0c7a05e6fb99`

```dockerfile
```

-	Layers:
	-	`sha256:253b9ae3ce5e09b9e82ca1ac3fcbe67e8bd9332025c8e18c1badd9df3085b13c`  
		Last Modified: Tue, 08 Apr 2025 10:48:57 GMT  
		Size: 4.0 MB (3979012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd310d7f0f093aa881f6d6beb86fedbafca89eba3eabe30fe233daf93087a8c`  
		Last Modified: Tue, 08 Apr 2025 10:48:56 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim` - linux; 386

```console
$ docker pull rust@sha256:bb5180ab836d2b9765e970861a734726951e55b490d86045511c69cffe5dcd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318921500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1379b48bf43ced6ff1dc1e0bc7150af59edb7c1cdf3e52a2b612cb94b64bb124`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5717094e375a7a30cbfd95d79b71ae2e1e438a9b730fb27e48eb343d0b981a1`  
		Last Modified: Tue, 08 Apr 2025 01:29:40 GMT  
		Size: 289.7 MB (289710769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b34dca3bdc3700658baef2ef87246f01f1276f019a270f7d6651094d9ef5bd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58e87bde78e6421ad5701ed6e1895b2146e37f9ddbb710e6c3564c5aeaa912d`

```dockerfile
```

-	Layers:
	-	`sha256:3a5f365726ead50a517bb7a1e0a66f89be048dd83aa40e156c91402f469e650f`  
		Last Modified: Tue, 08 Apr 2025 01:29:33 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48c9848cb48320622ba069df1d248315014d723047a5ad2fe5c0984f63b29b4`  
		Last Modified: Tue, 08 Apr 2025 01:29:32 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:7c698b86ae28c62f50194162e6ce3ccb20929b7e102dcc9451daae302a190c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367337074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583a28a59a2f362110c00233e30bd9cbe585d26d44f01bae200b8bfcacbc3dd4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b1b3a088ca3ea201af18986b7436e4aec60625258327e913df52ff8591370`  
		Last Modified: Tue, 08 Apr 2025 07:30:39 GMT  
		Size: 335.3 MB (335268843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim` - unknown; unknown

```console
$ docker pull rust@sha256:053e7e4791aacc14950e3e3fd33978f493690d41cf4a6ce384c31f8a6b28e790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de63ee76d9cad60f0ede2a9ebfa9ceaa8033826728ff25b231320f60c2a513e`

```dockerfile
```

-	Layers:
	-	`sha256:cb9a48cc982aca824da80a9466474cea0ca2889c619a740a0966fefe497cfeab`  
		Last Modified: Tue, 08 Apr 2025 07:30:30 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae8c4b9df6ac332d20cd1be109d998ae230fe05ebf9b7f6ee2cfb308c2bcb6d3`  
		Last Modified: Tue, 08 Apr 2025 07:30:29 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim` - linux; s390x

```console
$ docker pull rust@sha256:6fbc766b1eba2d9ee4174bf5728c3d5cdfa04d6bd77051944c5c0fd8bff0295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5e6a02c07dc29b10ca722271c932c061c30824d57f634c336d1ea35d41f4cf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37b16f2d003c1f9e67bd6dfda070e17bd22a162101f28a4396a958280daf695`  
		Last Modified: Tue, 08 Apr 2025 06:20:23 GMT  
		Size: 344.0 MB (344011347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim` - unknown; unknown

```console
$ docker pull rust@sha256:8547ff21e07816223e9f6766d42bea2cb69c579334e2ac18d625ac04749bb5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146d2be439c484209ca809cc8ce80871138fe27edf39a29a708fa317e8175305`

```dockerfile
```

-	Layers:
	-	`sha256:0b77fa511d03b0701d0ef55560b74a78f3f6e64e484e0095d3be54b544545131`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2add6570625fb08371b11c1a0bc8716a08b4fdd1ad3706bde7cf21f4d9323ff4`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86-slim-bookworm`

```console
$ docker pull rust@sha256:3f391b0678a6e0c88fd26f13e399c9c515ac47354e3cadfee7daee3b21651a4f
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

### `rust:1.86-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:41b809ac8846aeacb14ccb5dd79734dc6336b1e8888529c1e0a6d26931443b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297829415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b78d2068c9472719a39cfbd28a9e0133db41638ba76fb051d4920fd18f6357`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210bb45fea98f7e6faa766c3c761469f156896c67811f25bec9d45f29b1dcbf0`  
		Last Modified: Tue, 08 Apr 2025 01:35:04 GMT  
		Size: 269.6 MB (269602156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:dcbbf8a097555fecc6ee6d280575383a22bc6a9ab9d7c62b65bce2c5ac8b95b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4053ef871c854e51688a9e9d237bc0def61479d6a5e3fb1a875747ca86268418`

```dockerfile
```

-	Layers:
	-	`sha256:3a8e6fbc9faed90473194037bdf9c636eecebcd8b7aa883b8ce27862a1779d1c`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d055c2481171ed38a99a22ae56c4e7c2b1bd465a4daf50f1676878fc24ef3643`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:f2147dce0408c155cafde8cea27150a5716e908161387aa42d3d5cd5cc276e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313009317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfd2341a89215716ee5a10bd8b6d887794af904f07446e83403c73d9dc11c9a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f48bc660f38990c9b1a99eef7221c43c0941e46d2c77adb1059dcf83e133720`  
		Last Modified: Tue, 08 Apr 2025 16:49:54 GMT  
		Size: 289.1 MB (289071450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d03db0f51b3c203366e2d84c10c12ecefa338936f585b5e4493d144c0dd27b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d1df47ee7b8d27a616f617be86cd4d2c4bf9e6bacc9d6fac6c37bd6e2f6dd3`

```dockerfile
```

-	Layers:
	-	`sha256:6390c2b58d4d8b999d967a77f6c60f6e39fb1edcc78af868a9d39f02ea9c65cf`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 3.8 MB (3772732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89d90b466102965ae43f68698343d7a6deca9a2fa42f42bbab5b189ff921d00`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea3f5851799ee3e8f16ab003ef563ccfb590e287eb7960ff91fe44688a3e587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261543175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f316977191bca409dac97a0cd223be43a03fac7acb153bafc4c857382a8ae29e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be93040355bf29c5c23f25725fbace42a8c4e87149f54781b767539dc20cf504`  
		Last Modified: Tue, 08 Apr 2025 10:49:02 GMT  
		Size: 233.5 MB (233476855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7f6e5cdeadc7696bb55921e2a30219a5d48b483e09f9d698dd934b28bfa15ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4802987aca1475d13fc58155ab1989d5789510e7961ad326ff3f0c7a05e6fb99`

```dockerfile
```

-	Layers:
	-	`sha256:253b9ae3ce5e09b9e82ca1ac3fcbe67e8bd9332025c8e18c1badd9df3085b13c`  
		Last Modified: Tue, 08 Apr 2025 10:48:57 GMT  
		Size: 4.0 MB (3979012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd310d7f0f093aa881f6d6beb86fedbafca89eba3eabe30fe233daf93087a8c`  
		Last Modified: Tue, 08 Apr 2025 10:48:56 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:bb5180ab836d2b9765e970861a734726951e55b490d86045511c69cffe5dcd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318921500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1379b48bf43ced6ff1dc1e0bc7150af59edb7c1cdf3e52a2b612cb94b64bb124`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5717094e375a7a30cbfd95d79b71ae2e1e438a9b730fb27e48eb343d0b981a1`  
		Last Modified: Tue, 08 Apr 2025 01:29:40 GMT  
		Size: 289.7 MB (289710769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b34dca3bdc3700658baef2ef87246f01f1276f019a270f7d6651094d9ef5bd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58e87bde78e6421ad5701ed6e1895b2146e37f9ddbb710e6c3564c5aeaa912d`

```dockerfile
```

-	Layers:
	-	`sha256:3a5f365726ead50a517bb7a1e0a66f89be048dd83aa40e156c91402f469e650f`  
		Last Modified: Tue, 08 Apr 2025 01:29:33 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48c9848cb48320622ba069df1d248315014d723047a5ad2fe5c0984f63b29b4`  
		Last Modified: Tue, 08 Apr 2025 01:29:32 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:7c698b86ae28c62f50194162e6ce3ccb20929b7e102dcc9451daae302a190c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367337074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583a28a59a2f362110c00233e30bd9cbe585d26d44f01bae200b8bfcacbc3dd4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b1b3a088ca3ea201af18986b7436e4aec60625258327e913df52ff8591370`  
		Last Modified: Tue, 08 Apr 2025 07:30:39 GMT  
		Size: 335.3 MB (335268843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:053e7e4791aacc14950e3e3fd33978f493690d41cf4a6ce384c31f8a6b28e790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de63ee76d9cad60f0ede2a9ebfa9ceaa8033826728ff25b231320f60c2a513e`

```dockerfile
```

-	Layers:
	-	`sha256:cb9a48cc982aca824da80a9466474cea0ca2889c619a740a0966fefe497cfeab`  
		Last Modified: Tue, 08 Apr 2025 07:30:30 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae8c4b9df6ac332d20cd1be109d998ae230fe05ebf9b7f6ee2cfb308c2bcb6d3`  
		Last Modified: Tue, 08 Apr 2025 07:30:29 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:6fbc766b1eba2d9ee4174bf5728c3d5cdfa04d6bd77051944c5c0fd8bff0295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5e6a02c07dc29b10ca722271c932c061c30824d57f634c336d1ea35d41f4cf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37b16f2d003c1f9e67bd6dfda070e17bd22a162101f28a4396a958280daf695`  
		Last Modified: Tue, 08 Apr 2025 06:20:23 GMT  
		Size: 344.0 MB (344011347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8547ff21e07816223e9f6766d42bea2cb69c579334e2ac18d625ac04749bb5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146d2be439c484209ca809cc8ce80871138fe27edf39a29a708fa317e8175305`

```dockerfile
```

-	Layers:
	-	`sha256:0b77fa511d03b0701d0ef55560b74a78f3f6e64e484e0095d3be54b544545131`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2add6570625fb08371b11c1a0bc8716a08b4fdd1ad3706bde7cf21f4d9323ff4`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86-slim-bullseye`

```console
$ docker pull rust@sha256:405e5b0fe9f74098d19f3a7b65368c9cd4323758dd6b2d6305a35df8d2cc0a2a
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

### `rust:1.86-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:f8c0bb10d0e408141ae1ce9db3906933d04044014b81315956bb8babefdb4538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289245429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701ed3fc33b113775a941d354adccbf40b6a225401b883ee5966de1c83f41b2b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88fad72c2506246ffe6396d482cf40fced3dbdcef8f4356795a7cac8ff6b2ef`  
		Last Modified: Tue, 08 Apr 2025 01:35:00 GMT  
		Size: 259.0 MB (258988010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4741338f8e175f2156ac1827a7e205ed3ea2f97dab9e129c70963ec485678779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0edf37b8243573464db9fa035308a4066da5453afcc99b305823cb05f7a7437`

```dockerfile
```

-	Layers:
	-	`sha256:9eb94d3eacd1815973a9e0b2b8d9ea7e1aba5c23b593f6bc9dcc7afb1bdd484c`  
		Last Modified: Tue, 08 Apr 2025 01:34:55 GMT  
		Size: 4.2 MB (4175124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ba3cecfcf1347fea0549f31ad4367cab149129294dc8dfc57ccf6d6f0813fff`  
		Last Modified: Tue, 08 Apr 2025 01:34:55 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:64862b5819093237df39378fbaa1b43498424fab0bec03cae5733be1b24142b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.0 MB (309037855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6173382e6c055035ab42b01f20d2e1159bc44baf086271255b1ca3daf44909`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fabdae83abb8c4e7989a8005a7a92a8535e6ab6c0bd633442c316443e6f2bab`  
		Last Modified: Tue, 08 Apr 2025 16:53:16 GMT  
		Size: 283.5 MB (283498720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a1e648062c749afa43013786ee2772e71053aae03cb4782bbc4537e21bc45a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3995706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80946ceab5e2263d6a3d2080648d12b9fa299c11ee188d9f752f9d87cf949f4e`

```dockerfile
```

-	Layers:
	-	`sha256:82474d826cb3957f1fe6d11964dabb805591e256095862418b74e61335f2d2bb`  
		Last Modified: Tue, 08 Apr 2025 16:53:10 GMT  
		Size: 4.0 MB (3984274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c1e96c51cd14f17a15a43d875ce615aeb964e08b5edb459ce6c20c3722eb049`  
		Last Modified: Tue, 08 Apr 2025 16:53:09 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:663387b95b7c33a5430b967b31ff194fcdda0a1ce99f5b57701067a097d7790e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252089618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714f3327734efe4ca704111ca38e47742d41d1d6dbf7fd5f688890f0d51b0358`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae574b04e648f49bc601b389c9fe05b55820b884d921b0be2237f6bcbe8a3f94`  
		Last Modified: Tue, 08 Apr 2025 10:47:57 GMT  
		Size: 223.3 MB (223340120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:82d09db72e41c93ab2119868ef3741a813878f94117b474e06283adb390fbeab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4183262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544589af526ae2c336c2f08de66d4d92a1e44abc4a3bc1dc03656c481d5d7819`

```dockerfile
```

-	Layers:
	-	`sha256:b88826ea138c560bd03b90c875666115d0b79433cb4be2921f0d1aa605f9dc33`  
		Last Modified: Tue, 08 Apr 2025 10:47:52 GMT  
		Size: 4.2 MB (4171802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1ef1d405fbb2d4f000818000750480dae3e874eb9e5dd56ae60396665119ffe`  
		Last Modified: Tue, 08 Apr 2025 10:47:51 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:43df35999046bea8233d1a5fdfcd2356fba15a793fbeb9fa5224d1262adf2960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314097491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d34f303281cbb2b93f669a37283d0e2d6c0068957020ef6fa5232b882c63638`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c7f226a3ed9e3a783e859dc8479e50da2694130147ffb4885645e02664eedbec`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 31.2 MB (31184573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b380f9c572c29705a08754c4980a85f7915a4d9cd340d7f3c36e3926cba3001`  
		Last Modified: Tue, 08 Apr 2025 01:29:00 GMT  
		Size: 282.9 MB (282912918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:19d00c62057a0ddf1ba7ff04c110803c0702d91dcdad6a4eed7e9ff8f85cc8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80ca8b84c676afa150db9ce38fd1bfaca44431b98cdac4af32efe184523a8ca`

```dockerfile
```

-	Layers:
	-	`sha256:80703f1c4e5c8b72cdde3f31569d00b27ba521369410893b3e2dbc529daa0b19`  
		Last Modified: Tue, 08 Apr 2025 01:28:53 GMT  
		Size: 4.2 MB (4165381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1fd41d56f3f22ed5780318a7bc49397260241142ba692570d227a36598e668b`  
		Last Modified: Tue, 08 Apr 2025 01:28:53 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0`

```console
$ docker pull rust@sha256:6a6dda669f020fa1fcb0903e37a049484fbf4b4699c8cb89db26ca030f475259
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

### `rust:1.86.0` - linux; amd64

```console
$ docker pull rust@sha256:e2c3cc250468c6290044b6f8b8254ac79219b17c3232804e4a79b651d0c031a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547073889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dee95e9b67a7bb176a7084f8e543e0ec50c67fee8c69770f9a8e20c659bca81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b617a119f8a27982374d94ec6eb3738ae3d38d6fc2c34c865813926cf596a621`  
		Last Modified: Tue, 08 Apr 2025 03:16:47 GMT  
		Size: 211.3 MB (211331550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74a39eb585dbe3732f07ffb8ce7351ff0725ce605cd0585470613834f464774`  
		Last Modified: Tue, 08 Apr 2025 04:21:31 GMT  
		Size: 198.8 MB (198844240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0` - unknown; unknown

```console
$ docker pull rust@sha256:3509ec4e64b314235325eee7ebafc7f34e2f3ed18cdd2db1ee62e45e56c88418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb7ce20ad7522cd62fcddacdcd2610e03d6632563b739d9cbb6971a476918e6`

```dockerfile
```

-	Layers:
	-	`sha256:769f4e29352c2ec152cb9cb46918f0fb247e33b661cc190886c060f1b9bb5662`  
		Last Modified: Tue, 08 Apr 2025 04:21:26 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f071db2499bcd484721f1239e87ae438c36ca8d5af3bb29b6b8c7758232701`  
		Last Modified: Tue, 08 Apr 2025 04:21:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0` - linux; arm variant v7

```console
$ docker pull rust@sha256:e2f34964c241e7ea71a854eb91e0b225a2418936648499283d14c73abae98a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542260031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16535fe936f9919d4b6beff652f4c5e4d3e625c13bfff7fa4247510f19399638`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a319072ea86a8c9aa06075cbf6677da28654a48a38fc6adb52aa04f271ddd06`  
		Last Modified: Tue, 18 Mar 2025 07:30:13 GMT  
		Size: 21.9 MB (21918018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f325c93a6cb0439e3bf485f3a1ca5c31cca2f6b205d5c37e15890e18b5fe0`  
		Last Modified: Tue, 18 Mar 2025 15:26:53 GMT  
		Size: 59.6 MB (59639263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407c08ebab5377348ed14160a63d8d957a380f355e742fcec3755c68baf9c20d`  
		Last Modified: Tue, 18 Mar 2025 16:12:56 GMT  
		Size: 175.3 MB (175309168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dd9c885e006c5ba163c1af9605526e79f2905da43c9de3a5037b5f4a902ee5`  
		Last Modified: Thu, 03 Apr 2025 17:15:51 GMT  
		Size: 241.2 MB (241215579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0` - unknown; unknown

```console
$ docker pull rust@sha256:dfebee42501bc9ae716db67f70571ab1c43cae2aa84b8465558968c336c7bb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15287641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea10ffe1f6ecb4c95a552c05741fc7bbfa6e7501c663039937ea61b2f769b014`

```dockerfile
```

-	Layers:
	-	`sha256:721c7e73d5bf649a41efdad2260e00c896508c024f704b6dc26802980b057621`  
		Last Modified: Thu, 03 Apr 2025 17:15:45 GMT  
		Size: 15.3 MB (15274394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771ebeb25304716d614718f27531976702dafcdae3ae12e4f819037aa9509b53`  
		Last Modified: Thu, 03 Apr 2025 17:15:44 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8489b54bc057a93babd8906b056fe4c67f0e77e1d19fc18eb8fca8305067ae26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506607013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead27b748614e277ca15ac3636b936d4e471ad7ecf24da4587ddf7ac3cd9f419`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9d474cce081e468bc6f85727459852112ba732fbbfe3236fae66c5fa8a5ed5`  
		Last Modified: Tue, 18 Mar 2025 14:10:35 GMT  
		Size: 202.8 MB (202753988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadb53c2ea73a273e0e6fe4e18341f4291c24756dcbee8ad109038b067c0f8f4`  
		Last Modified: Thu, 03 Apr 2025 17:13:37 GMT  
		Size: 167.6 MB (167648030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0` - unknown; unknown

```console
$ docker pull rust@sha256:a48df1ec2a1e0ba16e84f7bb2189beb15a1aa86dd28a81bd65acba1470f9482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a632aa94d376b315058678dfd1194d1f04a4d851360ec98e10a5ab1f8239f18e`

```dockerfile
```

-	Layers:
	-	`sha256:86d2e91568072d7cf8f5f4aae6ec90b5a8825cb28ef55a1a29fe724454047aa2`  
		Last Modified: Thu, 03 Apr 2025 17:13:34 GMT  
		Size: 15.5 MB (15498527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fe3ef790dced91066659ab58e76acdd4fdd0f583148f161765e84ac8014bc2`  
		Last Modified: Thu, 03 Apr 2025 17:13:33 GMT  
		Size: 13.3 KB (13289 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0` - linux; 386

```console
$ docker pull rust@sha256:b06f5a923b052f2fbce21856fac2a8cbd4526310f9a22fae41a0b52388579188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572973806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cbc7d1b2a98309adc0f9f209d81640bd7a80c92e6bb5f5d4cda79343bea281`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7cbed080b4cdef804ca7e1b5bf4f3bc870dbef54cd5c74053fef6b147056`  
		Last Modified: Tue, 08 Apr 2025 01:23:54 GMT  
		Size: 24.8 MB (24847203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ffc3e6085548412ccbe96cfa7c6e138ccc7724d5a764a6a99e732fca48b289`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 66.2 MB (66237424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8471ab4232bc51e32c08f3c8fae6e33670c6c77fa4a3359a48d05453051f93e`  
		Last Modified: Tue, 08 Apr 2025 03:17:21 GMT  
		Size: 210.3 MB (210267336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ab54bb87b446c157a467a30d193edfb918d405722cf4c7b60d8f93b3a06b1a`  
		Last Modified: Tue, 08 Apr 2025 04:21:02 GMT  
		Size: 222.1 MB (222143712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0` - unknown; unknown

```console
$ docker pull rust@sha256:efc9f3a3297418eaf506f8ea51750f360027cbb3201e9a77d7ca1e1baaf7dc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da045b658f2b336a573f002e616b2fc8c51911ed0e2cb15e088c1c739a37e94d`

```dockerfile
```

-	Layers:
	-	`sha256:41bae4c1c5e052f6bdf0a312634e204ce48fb5ed8ab4309743503426c887ad5b`  
		Last Modified: Tue, 08 Apr 2025 04:20:57 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85eac65f6e9308480c58b3d5c215045ff30d0e9566710981c869dfa18a5f49a`  
		Last Modified: Tue, 08 Apr 2025 04:20:56 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0` - linux; ppc64le

```console
$ docker pull rust@sha256:0b20be231028bfd49a688c56aea6e25cf138c49012ce5addadc5bf68ad029674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628711168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c542d6616e2ce45fb4557eb923016df6ded64d6756d6212a69bbfdbfa2aeaf3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c3d0039c25f88e5b7c3da861e5a41bc617f045eff9521b410ceced36c47c971`  
		Last Modified: Mon, 17 Mar 2025 22:17:38 GMT  
		Size: 52.3 MB (52306033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b570e1ccee8c153bcd6622cbc7c9c8f1150932eca72b58d0e1d93a81c2d4b`  
		Last Modified: Tue, 18 Mar 2025 00:06:46 GMT  
		Size: 25.7 MB (25650089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3219f8cada3f1c641a91887b1112d0699cc708ea02d9c8f85a77e08659008bf`  
		Last Modified: Tue, 18 Mar 2025 07:04:49 GMT  
		Size: 69.8 MB (69844086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4c6aa27e302a908ce45a312c9a7c6eab49c831e12f24c5b4c29145d2d6ab77`  
		Last Modified: Tue, 18 Mar 2025 13:50:48 GMT  
		Size: 214.4 MB (214407742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794fac3bd448ad09edaa36a6cde07f66551a607b885eb53d5f2021f315d4f3a1`  
		Last Modified: Thu, 03 Apr 2025 17:12:22 GMT  
		Size: 266.5 MB (266503218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0` - unknown; unknown

```console
$ docker pull rust@sha256:bdcd78b6c3e9fe62dc32903e0e40321ad1dcb75565546a46b7fcb80c80d051a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b2473977886e04bd3f2fa7f647e75326f6f9692e51ddd99b58f5b6a3f33ce4`

```dockerfile
```

-	Layers:
	-	`sha256:285e9d5c95682b386fd734af5f45355fd2b768e4de10b666c7928c0865c17115`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 15.4 MB (15445052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2784c65f478f48009daf0d9be5e9eb15f877c29df9a514d10ae1f463b05d5abe`  
		Last Modified: Thu, 03 Apr 2025 17:12:02 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0` - linux; s390x

```console
$ docker pull rust@sha256:f48c071cd1dbf6e7f913bd6786412be97c82f25dc7e07ec327777838a47a15ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611934465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7d2d1236345049aad144c2d5ba643f4117f44e14bc7d7a4cd83c3ec56235d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea48981a9fc9115877d4666b28ace59b31b650cc30850dc9dbcd586ba0a496cb`  
		Last Modified: Mon, 17 Mar 2025 22:26:07 GMT  
		Size: 47.1 MB (47127836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d2fcabaa2191a259a1c138c1eae49463f7916a91e0b0f61fdbaa5dba7f4e2`  
		Last Modified: Tue, 18 Mar 2025 02:53:59 GMT  
		Size: 24.0 MB (24007981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e4163fc9bb4b1cfe20bf3ee0f067c3cb219407f1ed0b91eb04a5759f702712`  
		Last Modified: Tue, 18 Mar 2025 05:55:51 GMT  
		Size: 63.5 MB (63498480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f2a6b02b0e41028d194dbcc5b64d0cad2bdb30fa6390057978ddcf6ef155f8`  
		Last Modified: Tue, 18 Mar 2025 09:15:15 GMT  
		Size: 183.4 MB (183397092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15db11f7134bcabfcadf4efd6f83b0adb817278124e7abf84c09e8f2ace4d0e`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 293.9 MB (293903076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0` - unknown; unknown

```console
$ docker pull rust@sha256:24e6102ed3718659338647ed86c5ef77a3aed787e69c279a8b5a161b2dcee7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15295779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d32f0eae7397ef0bb4dc33fd8d1fd800859d56d4071a54e533f4f5da705fdf`

```dockerfile
```

-	Layers:
	-	`sha256:3bc6a1475676787f936efb971e18c1fd827cc2e06dde956322e7e95e32062df1`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 15.3 MB (15282640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f55e26963096390aa8b80788e20cf1bfd491126b210047525a73c44588be51`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0-alpine`

```console
$ docker pull rust@sha256:541a1720c1cedddae9e17b4214075bf57c20bc7b176b4bba6bce3437c44d51ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.86.0-alpine` - linux; amd64

```console
$ docker pull rust@sha256:ce413e392ed6c282a76beb447bfccc104136a46f2655df2df41fc0f04654c309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316237247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61d786d9f9c5cca0ab287fa99b7679ad755421530a8e95a8bd2cda19a69b856`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5c777dc8267f16eea52cc33c64c7b185aefaaaa260043622010c6e05333fd7`  
		Last Modified: Thu, 03 Apr 2025 17:12:15 GMT  
		Size: 61.6 MB (61564834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e319873236c572a5816c152bdb5011118b8ae9c672790e2ec264fbaafa4ddf`  
		Last Modified: Thu, 03 Apr 2025 17:12:18 GMT  
		Size: 251.0 MB (251030166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:dec7a5b5c43f2a69e7e1cd89b74f027b8ba4ac636e6654f30374a8143acce18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f0eca96243ca4fe82ac8c256aa685c9ed10eac95db72e1b176381f13e144e2`

```dockerfile
```

-	Layers:
	-	`sha256:cbd99f0e8b79ec516d96f3aee08b442562fc75cac2649bcb0a800ea915a0714a`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfec6d6b7554872ae59d5b3dc085d0c9287383d5bcb072f16cb8ac7fb44efbc3`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:45e626fcf2ef7f58c8b112b01657060691996ab4b4b3432a3f119afc93dd3875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (319016934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e2d039a6466c76b77a98bc81bba79858b86a3e5ab8a7c040094a491246270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63214d4c52deb7cd72dfb7b8ee63339ab9ba46086f6c52f3fc22c42a4cc6354c`  
		Last Modified: Wed, 19 Mar 2025 01:06:39 GMT  
		Size: 59.1 MB (59101227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa19e22237227dd4aba81e7f9e8743ac6f1828d92265e2ab9769fc3af195e04`  
		Last Modified: Thu, 03 Apr 2025 17:17:12 GMT  
		Size: 255.9 MB (255922678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:632262d43e3f35ced6b1ab847cc01838d21e8088bcd90a00889666a132b432b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37903037391a8658de906154ce8a47191fa1a8bf38f2a28471f7947cbf39b9b0`

```dockerfile
```

-	Layers:
	-	`sha256:1b5a4bc32a00e922f7028b1c3560d72456d27fdbc45f6525d545f9f313f21c09`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0fbb2e69c51339ac830b15829e85032b03271d892d1327f0628435616478b9c`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0-alpine3.20`

```console
$ docker pull rust@sha256:2ee35275aeaa2e438f34a0563f7931988f5c5254e2eeec562f95a60ca2a2e7c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.86.0-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:b07e0b6e63438f28b28ab8976881ae0a926af4da9fbe9288ed0fe69138690c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.0 MB (309972637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86009d33dc0da7a31e9d46f4f6954d7e7b0166da8ebbbdf47d6cbd1c09829847`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda11a1c7cdfc868caa20205c5191c9e175af463da2d48ab5c74561819b4cbea`  
		Last Modified: Thu, 03 Apr 2025 17:11:17 GMT  
		Size: 55.3 MB (55315639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55f3dceec5bf9dd5986d21f22e336fc8efccac71e961895a64688eb12863f3c`  
		Last Modified: Thu, 03 Apr 2025 17:11:22 GMT  
		Size: 251.0 MB (251030101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:c9ce1958f067088ab558b7b6319833afff6b777d67358dbcfe70b9da0efb7ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a217f7fcce5e6762e7f71ad217556d3f4a942e64e66b12b91b30c51c8734ffc`

```dockerfile
```

-	Layers:
	-	`sha256:fbf4d52494216492b9e0cbcae0e1ad2eb0b2153e57c111b027c08f966da96c79`  
		Last Modified: Thu, 03 Apr 2025 17:11:15 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d67dd3f9a37cf39335b9f2e242627d47bd6a5b1b6fcd8474b54957de8f8fd84`  
		Last Modified: Thu, 03 Apr 2025 17:11:14 GMT  
		Size: 10.7 KB (10713 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:28b8265454853aeb6fd5b4dfd02b0223f6349204f348663e2c7551fc9a984541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312964800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272469f2176bd29846696edd36f27ed458dcddadb03bd9b7967197df0e6d94e2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7362932bfc33faed0c84d60ed0d4aefe9e34b5b9366cfa2015a14c01e2604`  
		Last Modified: Wed, 19 Mar 2025 04:51:19 GMT  
		Size: 53.0 MB (52950559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da216a1abe7d23357c54f3c639e81a67652f254c496e34ca5ed47c3a49b9582`  
		Last Modified: Thu, 03 Apr 2025 17:16:01 GMT  
		Size: 255.9 MB (255923076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:be732f17ad9e5e6e7cf13ee3a78836ae6ffae078de73425995fd283f4a6f1e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8093eb3b99a9036476b177c449878affb005e2ea60bd33c51dfbba375427b1f`

```dockerfile
```

-	Layers:
	-	`sha256:8d233587293019133f0bd1ba7d43eb76c4ec6b3e670421c4e41787189d73c449`  
		Last Modified: Thu, 03 Apr 2025 17:15:55 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce0e73bdd8ebfaaec68f238d168a0405459eead3889f55c922f39f2bba99938`  
		Last Modified: Thu, 03 Apr 2025 17:15:55 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0-alpine3.21`

```console
$ docker pull rust@sha256:541a1720c1cedddae9e17b4214075bf57c20bc7b176b4bba6bce3437c44d51ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.86.0-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:ce413e392ed6c282a76beb447bfccc104136a46f2655df2df41fc0f04654c309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316237247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61d786d9f9c5cca0ab287fa99b7679ad755421530a8e95a8bd2cda19a69b856`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5c777dc8267f16eea52cc33c64c7b185aefaaaa260043622010c6e05333fd7`  
		Last Modified: Thu, 03 Apr 2025 17:12:15 GMT  
		Size: 61.6 MB (61564834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e319873236c572a5816c152bdb5011118b8ae9c672790e2ec264fbaafa4ddf`  
		Last Modified: Thu, 03 Apr 2025 17:12:18 GMT  
		Size: 251.0 MB (251030166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:dec7a5b5c43f2a69e7e1cd89b74f027b8ba4ac636e6654f30374a8143acce18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f0eca96243ca4fe82ac8c256aa685c9ed10eac95db72e1b176381f13e144e2`

```dockerfile
```

-	Layers:
	-	`sha256:cbd99f0e8b79ec516d96f3aee08b442562fc75cac2649bcb0a800ea915a0714a`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfec6d6b7554872ae59d5b3dc085d0c9287383d5bcb072f16cb8ac7fb44efbc3`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:45e626fcf2ef7f58c8b112b01657060691996ab4b4b3432a3f119afc93dd3875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (319016934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e2d039a6466c76b77a98bc81bba79858b86a3e5ab8a7c040094a491246270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63214d4c52deb7cd72dfb7b8ee63339ab9ba46086f6c52f3fc22c42a4cc6354c`  
		Last Modified: Wed, 19 Mar 2025 01:06:39 GMT  
		Size: 59.1 MB (59101227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa19e22237227dd4aba81e7f9e8743ac6f1828d92265e2ab9769fc3af195e04`  
		Last Modified: Thu, 03 Apr 2025 17:17:12 GMT  
		Size: 255.9 MB (255922678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:632262d43e3f35ced6b1ab847cc01838d21e8088bcd90a00889666a132b432b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37903037391a8658de906154ce8a47191fa1a8bf38f2a28471f7947cbf39b9b0`

```dockerfile
```

-	Layers:
	-	`sha256:1b5a4bc32a00e922f7028b1c3560d72456d27fdbc45f6525d545f9f313f21c09`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0fbb2e69c51339ac830b15829e85032b03271d892d1327f0628435616478b9c`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0-bookworm`

```console
$ docker pull rust@sha256:6a6dda669f020fa1fcb0903e37a049484fbf4b4699c8cb89db26ca030f475259
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

### `rust:1.86.0-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:e2c3cc250468c6290044b6f8b8254ac79219b17c3232804e4a79b651d0c031a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547073889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dee95e9b67a7bb176a7084f8e543e0ec50c67fee8c69770f9a8e20c659bca81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b617a119f8a27982374d94ec6eb3738ae3d38d6fc2c34c865813926cf596a621`  
		Last Modified: Tue, 08 Apr 2025 03:16:47 GMT  
		Size: 211.3 MB (211331550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74a39eb585dbe3732f07ffb8ce7351ff0725ce605cd0585470613834f464774`  
		Last Modified: Tue, 08 Apr 2025 04:21:31 GMT  
		Size: 198.8 MB (198844240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3509ec4e64b314235325eee7ebafc7f34e2f3ed18cdd2db1ee62e45e56c88418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb7ce20ad7522cd62fcddacdcd2610e03d6632563b739d9cbb6971a476918e6`

```dockerfile
```

-	Layers:
	-	`sha256:769f4e29352c2ec152cb9cb46918f0fb247e33b661cc190886c060f1b9bb5662`  
		Last Modified: Tue, 08 Apr 2025 04:21:26 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f071db2499bcd484721f1239e87ae438c36ca8d5af3bb29b6b8c7758232701`  
		Last Modified: Tue, 08 Apr 2025 04:21:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:e2f34964c241e7ea71a854eb91e0b225a2418936648499283d14c73abae98a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542260031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16535fe936f9919d4b6beff652f4c5e4d3e625c13bfff7fa4247510f19399638`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a319072ea86a8c9aa06075cbf6677da28654a48a38fc6adb52aa04f271ddd06`  
		Last Modified: Tue, 18 Mar 2025 07:30:13 GMT  
		Size: 21.9 MB (21918018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f325c93a6cb0439e3bf485f3a1ca5c31cca2f6b205d5c37e15890e18b5fe0`  
		Last Modified: Tue, 18 Mar 2025 15:26:53 GMT  
		Size: 59.6 MB (59639263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407c08ebab5377348ed14160a63d8d957a380f355e742fcec3755c68baf9c20d`  
		Last Modified: Tue, 18 Mar 2025 16:12:56 GMT  
		Size: 175.3 MB (175309168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dd9c885e006c5ba163c1af9605526e79f2905da43c9de3a5037b5f4a902ee5`  
		Last Modified: Thu, 03 Apr 2025 17:15:51 GMT  
		Size: 241.2 MB (241215579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:dfebee42501bc9ae716db67f70571ab1c43cae2aa84b8465558968c336c7bb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15287641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea10ffe1f6ecb4c95a552c05741fc7bbfa6e7501c663039937ea61b2f769b014`

```dockerfile
```

-	Layers:
	-	`sha256:721c7e73d5bf649a41efdad2260e00c896508c024f704b6dc26802980b057621`  
		Last Modified: Thu, 03 Apr 2025 17:15:45 GMT  
		Size: 15.3 MB (15274394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771ebeb25304716d614718f27531976702dafcdae3ae12e4f819037aa9509b53`  
		Last Modified: Thu, 03 Apr 2025 17:15:44 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8489b54bc057a93babd8906b056fe4c67f0e77e1d19fc18eb8fca8305067ae26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506607013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead27b748614e277ca15ac3636b936d4e471ad7ecf24da4587ddf7ac3cd9f419`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9d474cce081e468bc6f85727459852112ba732fbbfe3236fae66c5fa8a5ed5`  
		Last Modified: Tue, 18 Mar 2025 14:10:35 GMT  
		Size: 202.8 MB (202753988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadb53c2ea73a273e0e6fe4e18341f4291c24756dcbee8ad109038b067c0f8f4`  
		Last Modified: Thu, 03 Apr 2025 17:13:37 GMT  
		Size: 167.6 MB (167648030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a48df1ec2a1e0ba16e84f7bb2189beb15a1aa86dd28a81bd65acba1470f9482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a632aa94d376b315058678dfd1194d1f04a4d851360ec98e10a5ab1f8239f18e`

```dockerfile
```

-	Layers:
	-	`sha256:86d2e91568072d7cf8f5f4aae6ec90b5a8825cb28ef55a1a29fe724454047aa2`  
		Last Modified: Thu, 03 Apr 2025 17:13:34 GMT  
		Size: 15.5 MB (15498527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fe3ef790dced91066659ab58e76acdd4fdd0f583148f161765e84ac8014bc2`  
		Last Modified: Thu, 03 Apr 2025 17:13:33 GMT  
		Size: 13.3 KB (13289 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bookworm` - linux; 386

```console
$ docker pull rust@sha256:b06f5a923b052f2fbce21856fac2a8cbd4526310f9a22fae41a0b52388579188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572973806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cbc7d1b2a98309adc0f9f209d81640bd7a80c92e6bb5f5d4cda79343bea281`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7cbed080b4cdef804ca7e1b5bf4f3bc870dbef54cd5c74053fef6b147056`  
		Last Modified: Tue, 08 Apr 2025 01:23:54 GMT  
		Size: 24.8 MB (24847203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ffc3e6085548412ccbe96cfa7c6e138ccc7724d5a764a6a99e732fca48b289`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 66.2 MB (66237424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8471ab4232bc51e32c08f3c8fae6e33670c6c77fa4a3359a48d05453051f93e`  
		Last Modified: Tue, 08 Apr 2025 03:17:21 GMT  
		Size: 210.3 MB (210267336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ab54bb87b446c157a467a30d193edfb918d405722cf4c7b60d8f93b3a06b1a`  
		Last Modified: Tue, 08 Apr 2025 04:21:02 GMT  
		Size: 222.1 MB (222143712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:efc9f3a3297418eaf506f8ea51750f360027cbb3201e9a77d7ca1e1baaf7dc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da045b658f2b336a573f002e616b2fc8c51911ed0e2cb15e088c1c739a37e94d`

```dockerfile
```

-	Layers:
	-	`sha256:41bae4c1c5e052f6bdf0a312634e204ce48fb5ed8ab4309743503426c887ad5b`  
		Last Modified: Tue, 08 Apr 2025 04:20:57 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85eac65f6e9308480c58b3d5c215045ff30d0e9566710981c869dfa18a5f49a`  
		Last Modified: Tue, 08 Apr 2025 04:20:56 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:0b20be231028bfd49a688c56aea6e25cf138c49012ce5addadc5bf68ad029674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628711168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c542d6616e2ce45fb4557eb923016df6ded64d6756d6212a69bbfdbfa2aeaf3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c3d0039c25f88e5b7c3da861e5a41bc617f045eff9521b410ceced36c47c971`  
		Last Modified: Mon, 17 Mar 2025 22:17:38 GMT  
		Size: 52.3 MB (52306033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b570e1ccee8c153bcd6622cbc7c9c8f1150932eca72b58d0e1d93a81c2d4b`  
		Last Modified: Tue, 18 Mar 2025 00:06:46 GMT  
		Size: 25.7 MB (25650089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3219f8cada3f1c641a91887b1112d0699cc708ea02d9c8f85a77e08659008bf`  
		Last Modified: Tue, 18 Mar 2025 07:04:49 GMT  
		Size: 69.8 MB (69844086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4c6aa27e302a908ce45a312c9a7c6eab49c831e12f24c5b4c29145d2d6ab77`  
		Last Modified: Tue, 18 Mar 2025 13:50:48 GMT  
		Size: 214.4 MB (214407742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794fac3bd448ad09edaa36a6cde07f66551a607b885eb53d5f2021f315d4f3a1`  
		Last Modified: Thu, 03 Apr 2025 17:12:22 GMT  
		Size: 266.5 MB (266503218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bdcd78b6c3e9fe62dc32903e0e40321ad1dcb75565546a46b7fcb80c80d051a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b2473977886e04bd3f2fa7f647e75326f6f9692e51ddd99b58f5b6a3f33ce4`

```dockerfile
```

-	Layers:
	-	`sha256:285e9d5c95682b386fd734af5f45355fd2b768e4de10b666c7928c0865c17115`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 15.4 MB (15445052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2784c65f478f48009daf0d9be5e9eb15f877c29df9a514d10ae1f463b05d5abe`  
		Last Modified: Thu, 03 Apr 2025 17:12:02 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:f48c071cd1dbf6e7f913bd6786412be97c82f25dc7e07ec327777838a47a15ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611934465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7d2d1236345049aad144c2d5ba643f4117f44e14bc7d7a4cd83c3ec56235d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea48981a9fc9115877d4666b28ace59b31b650cc30850dc9dbcd586ba0a496cb`  
		Last Modified: Mon, 17 Mar 2025 22:26:07 GMT  
		Size: 47.1 MB (47127836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d2fcabaa2191a259a1c138c1eae49463f7916a91e0b0f61fdbaa5dba7f4e2`  
		Last Modified: Tue, 18 Mar 2025 02:53:59 GMT  
		Size: 24.0 MB (24007981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e4163fc9bb4b1cfe20bf3ee0f067c3cb219407f1ed0b91eb04a5759f702712`  
		Last Modified: Tue, 18 Mar 2025 05:55:51 GMT  
		Size: 63.5 MB (63498480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f2a6b02b0e41028d194dbcc5b64d0cad2bdb30fa6390057978ddcf6ef155f8`  
		Last Modified: Tue, 18 Mar 2025 09:15:15 GMT  
		Size: 183.4 MB (183397092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15db11f7134bcabfcadf4efd6f83b0adb817278124e7abf84c09e8f2ace4d0e`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 293.9 MB (293903076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:24e6102ed3718659338647ed86c5ef77a3aed787e69c279a8b5a161b2dcee7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15295779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d32f0eae7397ef0bb4dc33fd8d1fd800859d56d4071a54e533f4f5da705fdf`

```dockerfile
```

-	Layers:
	-	`sha256:3bc6a1475676787f936efb971e18c1fd827cc2e06dde956322e7e95e32062df1`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 15.3 MB (15282640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f55e26963096390aa8b80788e20cf1bfd491126b210047525a73c44588be51`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0-bullseye`

```console
$ docker pull rust@sha256:7a8c32ed3e4407a50d35985e0602f42c1f78ea6ae13930e3ace8205d573fd43f
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

### `rust:1.86.0-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:19c3a05a2f4be47ee8cbce22c200f09a16a378a1150bd4019fa5f0ac630e609b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.2 MB (520218264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b03f8c11be37e006c1e9735f2cf80ff0be92fcb7662a408c1e380365e6fa1bb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7819131060d3c79e48555fb5b04fa584b86d2fb80e3ede0864c7e6bba7d87`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 15.8 MB (15763510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f843b455b9b7bececb5cfeb4ba5839d4aa47845ded1258734c375304df3d0`  
		Last Modified: Tue, 08 Apr 2025 02:13:52 GMT  
		Size: 54.8 MB (54755152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b731139994e4dbd527b938ba04d372fec4d9d7302e7f454003dc0b3485c05bb1`  
		Last Modified: Tue, 08 Apr 2025 03:17:23 GMT  
		Size: 197.1 MB (197105555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056d1ad25ed6f278ed43ffa359808bab69a55df6afc883e564cb8c8768160524`  
		Last Modified: Tue, 08 Apr 2025 04:21:23 GMT  
		Size: 198.8 MB (198845518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6eaea83e5ca843f5257ac5886c846ed9d2607868f4d96b02bb4d6dc390341595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15086810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf77a97c2724f28d4b6a8a0ba1ac79caafacb92bc07435739b9410c5315274d`

```dockerfile
```

-	Layers:
	-	`sha256:1f6c5eb822984d31b2a2285ca0d64cd1827a12c9a40dc33817afa4bb7094f578`  
		Last Modified: Tue, 08 Apr 2025 04:21:19 GMT  
		Size: 15.1 MB (15075561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70368749ca14fffe47e32e606e5c77ad9e0468cf7cd92010ccd9218052806e8c`  
		Last Modified: Tue, 08 Apr 2025 04:21:19 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:2355887e87ec08c9db4665d5856f0e5dde1a1b436d7ef1ebedbc71f6aa4288b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.1 MB (523115497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956da94b04af8a4f1ba79acfd8f8f637cb0251bd8292b6e013d0607a18f48f0a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c0fd1793bf8bc1764ff6503ad6f86ae0f1151de2bd8b7285b28dc6f5cc6001c3`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 49.0 MB (49026561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fd5d78189f9a0219a8d445519fe59067dcfa82b8799cf047c0b783ffa33a78`  
		Last Modified: Tue, 18 Mar 2025 07:26:06 GMT  
		Size: 14.7 MB (14674012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31183489ce2b77443c42eee08badb4a4fcf8ad4cef9299e71603f2239cb4064`  
		Last Modified: Tue, 18 Mar 2025 15:29:13 GMT  
		Size: 50.6 MB (50640225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6676c7b3b77e9e71cb741c5c04bfd9a595560092d9024884d0ce64c66f48bc6`  
		Last Modified: Tue, 18 Mar 2025 16:15:00 GMT  
		Size: 167.6 MB (167559857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b86ba427e0fae57b323d1a94b5942db3ef6663580549d5abeeaff2e6671eeb7`  
		Last Modified: Thu, 03 Apr 2025 17:11:34 GMT  
		Size: 241.2 MB (241214842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:02ad46142f4af7ad1d5deb91011c07cef40aa34ba654a2afff289dcec3b5edd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e693efb626079c5d179344964747f1db704955b930abdc9372eb60dd7d37b2`

```dockerfile
```

-	Layers:
	-	`sha256:fbf9e4eabc83ab73bf1172bd3b0216ea0257bad4e2bb7e7d735d5ad5ef2bccec`  
		Last Modified: Thu, 03 Apr 2025 17:11:29 GMT  
		Size: 14.9 MB (14874384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:897e8e84b1d8543de6c676fd27fe8bb89d0448b16d6464b9966887246a0ba0d4`  
		Last Modified: Thu, 03 Apr 2025 17:11:28 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:69d48decb7216958492661cea62057f649e080c0cd37360d4b74324867db6d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.3 MB (480316197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5114f900c5aa75bfd01846f195f411d4ccb4a7b272ad186738d04b0776e6a11`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645bc92dcf4a3c806f112acf0724041051eab86b13816f8d7286950facb47ec3`  
		Last Modified: Tue, 18 Mar 2025 05:00:00 GMT  
		Size: 15.5 MB (15544004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96fedce3b84d801b5eec66fa2ddb4a4653be64f8e04188e6e7ab37b6566bd34`  
		Last Modified: Tue, 18 Mar 2025 13:15:20 GMT  
		Size: 54.9 MB (54855429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15780e9924523e788780ac991f29afa248c22b09abb68f8a9945cf272b3dc84e`  
		Last Modified: Tue, 18 Mar 2025 14:12:21 GMT  
		Size: 190.0 MB (190020786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b53efaeee4c92c572f617852fe5add72eed90d7c8f3416dcaff2bdaf40c47af`  
		Last Modified: Thu, 03 Apr 2025 17:10:56 GMT  
		Size: 167.6 MB (167647584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d0b352a4def49f1720c30632fc5dd136d73b3e2f9b904e02471089d27a3d2497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d14e3af14e7f5e5a1d29988d0c4bcb918ce2cb76c209f37cf16cf8ab2a83f3d`

```dockerfile
```

-	Layers:
	-	`sha256:70f71d6a962c6cd40615d935896c2467b5730056acbdcc9132c27fde862a3401`  
		Last Modified: Thu, 03 Apr 2025 17:10:55 GMT  
		Size: 15.1 MB (15075853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90c75b489dac3fed9aabb83068b4b8336b7ed3e8eb253a534ae509cc7ed1ec2b`  
		Last Modified: Thu, 03 Apr 2025 17:10:52 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bullseye` - linux; 386

```console
$ docker pull rust@sha256:3a72bca02f43cd0d9f449b127103aadd427ff987a9613b3bc088eeb699fee0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549154273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c1a99516c42e56ce0d8c4e9108af14a30bf714c00ba497fe5b0818adb0458`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ffef4e17cbc252fc170472ff3910647beec8b91ac9abe188d6595b2087a0dc`  
		Last Modified: Tue, 08 Apr 2025 01:24:12 GMT  
		Size: 16.3 MB (16267037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684d7ac3a47d27aefe42d135394e4d8b703fb530ab3bd2ad6ef78b8c9beaf885`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 56.0 MB (56047217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f57b5c68cdb07f2657d3893b6b23c64ea31a47747ad68a064ff80bc616fdb51`  
		Last Modified: Tue, 08 Apr 2025 03:26:01 GMT  
		Size: 200.0 MB (200010627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9965d6680dd77db10541dab74f8fa0b74081c35a96fba815ca735a5bdba30db6`  
		Last Modified: Tue, 08 Apr 2025 04:20:42 GMT  
		Size: 222.1 MB (222144927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3f64b6b5e44466afdb2e0b9bc6fc4d01da31c626355b88f65650f57c3c2b176f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15073805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f9a17691493fcbefe1257efebd05e75f9d2247b27d8e4c2f0787e67400b081`

```dockerfile
```

-	Layers:
	-	`sha256:70606c1f443921a19b7f1ccd2601da80840aab493bd5fe9990c855778aa67324`  
		Last Modified: Tue, 08 Apr 2025 04:20:38 GMT  
		Size: 15.1 MB (15062588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760624857aafbce57f9c110b4cd55c6efb77f9b6f390378e3518a694baed7386`  
		Last Modified: Tue, 08 Apr 2025 04:20:37 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0-slim`

```console
$ docker pull rust@sha256:3f391b0678a6e0c88fd26f13e399c9c515ac47354e3cadfee7daee3b21651a4f
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

### `rust:1.86.0-slim` - linux; amd64

```console
$ docker pull rust@sha256:41b809ac8846aeacb14ccb5dd79734dc6336b1e8888529c1e0a6d26931443b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297829415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b78d2068c9472719a39cfbd28a9e0133db41638ba76fb051d4920fd18f6357`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210bb45fea98f7e6faa766c3c761469f156896c67811f25bec9d45f29b1dcbf0`  
		Last Modified: Tue, 08 Apr 2025 01:35:04 GMT  
		Size: 269.6 MB (269602156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:dcbbf8a097555fecc6ee6d280575383a22bc6a9ab9d7c62b65bce2c5ac8b95b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4053ef871c854e51688a9e9d237bc0def61479d6a5e3fb1a875747ca86268418`

```dockerfile
```

-	Layers:
	-	`sha256:3a8e6fbc9faed90473194037bdf9c636eecebcd8b7aa883b8ce27862a1779d1c`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d055c2481171ed38a99a22ae56c4e7c2b1bd465a4daf50f1676878fc24ef3643`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:f2147dce0408c155cafde8cea27150a5716e908161387aa42d3d5cd5cc276e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313009317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfd2341a89215716ee5a10bd8b6d887794af904f07446e83403c73d9dc11c9a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f48bc660f38990c9b1a99eef7221c43c0941e46d2c77adb1059dcf83e133720`  
		Last Modified: Tue, 08 Apr 2025 16:49:54 GMT  
		Size: 289.1 MB (289071450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:d03db0f51b3c203366e2d84c10c12ecefa338936f585b5e4493d144c0dd27b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d1df47ee7b8d27a616f617be86cd4d2c4bf9e6bacc9d6fac6c37bd6e2f6dd3`

```dockerfile
```

-	Layers:
	-	`sha256:6390c2b58d4d8b999d967a77f6c60f6e39fb1edcc78af868a9d39f02ea9c65cf`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 3.8 MB (3772732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89d90b466102965ae43f68698343d7a6deca9a2fa42f42bbab5b189ff921d00`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea3f5851799ee3e8f16ab003ef563ccfb590e287eb7960ff91fe44688a3e587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261543175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f316977191bca409dac97a0cd223be43a03fac7acb153bafc4c857382a8ae29e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be93040355bf29c5c23f25725fbace42a8c4e87149f54781b767539dc20cf504`  
		Last Modified: Tue, 08 Apr 2025 10:49:02 GMT  
		Size: 233.5 MB (233476855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:7f6e5cdeadc7696bb55921e2a30219a5d48b483e09f9d698dd934b28bfa15ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4802987aca1475d13fc58155ab1989d5789510e7961ad326ff3f0c7a05e6fb99`

```dockerfile
```

-	Layers:
	-	`sha256:253b9ae3ce5e09b9e82ca1ac3fcbe67e8bd9332025c8e18c1badd9df3085b13c`  
		Last Modified: Tue, 08 Apr 2025 10:48:57 GMT  
		Size: 4.0 MB (3979012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd310d7f0f093aa881f6d6beb86fedbafca89eba3eabe30fe233daf93087a8c`  
		Last Modified: Tue, 08 Apr 2025 10:48:56 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim` - linux; 386

```console
$ docker pull rust@sha256:bb5180ab836d2b9765e970861a734726951e55b490d86045511c69cffe5dcd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318921500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1379b48bf43ced6ff1dc1e0bc7150af59edb7c1cdf3e52a2b612cb94b64bb124`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5717094e375a7a30cbfd95d79b71ae2e1e438a9b730fb27e48eb343d0b981a1`  
		Last Modified: Tue, 08 Apr 2025 01:29:40 GMT  
		Size: 289.7 MB (289710769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b34dca3bdc3700658baef2ef87246f01f1276f019a270f7d6651094d9ef5bd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58e87bde78e6421ad5701ed6e1895b2146e37f9ddbb710e6c3564c5aeaa912d`

```dockerfile
```

-	Layers:
	-	`sha256:3a5f365726ead50a517bb7a1e0a66f89be048dd83aa40e156c91402f469e650f`  
		Last Modified: Tue, 08 Apr 2025 01:29:33 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48c9848cb48320622ba069df1d248315014d723047a5ad2fe5c0984f63b29b4`  
		Last Modified: Tue, 08 Apr 2025 01:29:32 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:7c698b86ae28c62f50194162e6ce3ccb20929b7e102dcc9451daae302a190c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367337074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583a28a59a2f362110c00233e30bd9cbe585d26d44f01bae200b8bfcacbc3dd4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b1b3a088ca3ea201af18986b7436e4aec60625258327e913df52ff8591370`  
		Last Modified: Tue, 08 Apr 2025 07:30:39 GMT  
		Size: 335.3 MB (335268843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:053e7e4791aacc14950e3e3fd33978f493690d41cf4a6ce384c31f8a6b28e790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de63ee76d9cad60f0ede2a9ebfa9ceaa8033826728ff25b231320f60c2a513e`

```dockerfile
```

-	Layers:
	-	`sha256:cb9a48cc982aca824da80a9466474cea0ca2889c619a740a0966fefe497cfeab`  
		Last Modified: Tue, 08 Apr 2025 07:30:30 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae8c4b9df6ac332d20cd1be109d998ae230fe05ebf9b7f6ee2cfb308c2bcb6d3`  
		Last Modified: Tue, 08 Apr 2025 07:30:29 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim` - linux; s390x

```console
$ docker pull rust@sha256:6fbc766b1eba2d9ee4174bf5728c3d5cdfa04d6bd77051944c5c0fd8bff0295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5e6a02c07dc29b10ca722271c932c061c30824d57f634c336d1ea35d41f4cf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37b16f2d003c1f9e67bd6dfda070e17bd22a162101f28a4396a958280daf695`  
		Last Modified: Tue, 08 Apr 2025 06:20:23 GMT  
		Size: 344.0 MB (344011347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:8547ff21e07816223e9f6766d42bea2cb69c579334e2ac18d625ac04749bb5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146d2be439c484209ca809cc8ce80871138fe27edf39a29a708fa317e8175305`

```dockerfile
```

-	Layers:
	-	`sha256:0b77fa511d03b0701d0ef55560b74a78f3f6e64e484e0095d3be54b544545131`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2add6570625fb08371b11c1a0bc8716a08b4fdd1ad3706bde7cf21f4d9323ff4`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0-slim-bookworm`

```console
$ docker pull rust@sha256:3f391b0678a6e0c88fd26f13e399c9c515ac47354e3cadfee7daee3b21651a4f
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

### `rust:1.86.0-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:41b809ac8846aeacb14ccb5dd79734dc6336b1e8888529c1e0a6d26931443b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297829415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b78d2068c9472719a39cfbd28a9e0133db41638ba76fb051d4920fd18f6357`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210bb45fea98f7e6faa766c3c761469f156896c67811f25bec9d45f29b1dcbf0`  
		Last Modified: Tue, 08 Apr 2025 01:35:04 GMT  
		Size: 269.6 MB (269602156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:dcbbf8a097555fecc6ee6d280575383a22bc6a9ab9d7c62b65bce2c5ac8b95b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4053ef871c854e51688a9e9d237bc0def61479d6a5e3fb1a875747ca86268418`

```dockerfile
```

-	Layers:
	-	`sha256:3a8e6fbc9faed90473194037bdf9c636eecebcd8b7aa883b8ce27862a1779d1c`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d055c2481171ed38a99a22ae56c4e7c2b1bd465a4daf50f1676878fc24ef3643`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:f2147dce0408c155cafde8cea27150a5716e908161387aa42d3d5cd5cc276e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313009317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfd2341a89215716ee5a10bd8b6d887794af904f07446e83403c73d9dc11c9a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f48bc660f38990c9b1a99eef7221c43c0941e46d2c77adb1059dcf83e133720`  
		Last Modified: Tue, 08 Apr 2025 16:49:54 GMT  
		Size: 289.1 MB (289071450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d03db0f51b3c203366e2d84c10c12ecefa338936f585b5e4493d144c0dd27b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d1df47ee7b8d27a616f617be86cd4d2c4bf9e6bacc9d6fac6c37bd6e2f6dd3`

```dockerfile
```

-	Layers:
	-	`sha256:6390c2b58d4d8b999d967a77f6c60f6e39fb1edcc78af868a9d39f02ea9c65cf`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 3.8 MB (3772732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89d90b466102965ae43f68698343d7a6deca9a2fa42f42bbab5b189ff921d00`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea3f5851799ee3e8f16ab003ef563ccfb590e287eb7960ff91fe44688a3e587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261543175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f316977191bca409dac97a0cd223be43a03fac7acb153bafc4c857382a8ae29e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be93040355bf29c5c23f25725fbace42a8c4e87149f54781b767539dc20cf504`  
		Last Modified: Tue, 08 Apr 2025 10:49:02 GMT  
		Size: 233.5 MB (233476855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7f6e5cdeadc7696bb55921e2a30219a5d48b483e09f9d698dd934b28bfa15ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4802987aca1475d13fc58155ab1989d5789510e7961ad326ff3f0c7a05e6fb99`

```dockerfile
```

-	Layers:
	-	`sha256:253b9ae3ce5e09b9e82ca1ac3fcbe67e8bd9332025c8e18c1badd9df3085b13c`  
		Last Modified: Tue, 08 Apr 2025 10:48:57 GMT  
		Size: 4.0 MB (3979012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd310d7f0f093aa881f6d6beb86fedbafca89eba3eabe30fe233daf93087a8c`  
		Last Modified: Tue, 08 Apr 2025 10:48:56 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:bb5180ab836d2b9765e970861a734726951e55b490d86045511c69cffe5dcd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318921500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1379b48bf43ced6ff1dc1e0bc7150af59edb7c1cdf3e52a2b612cb94b64bb124`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5717094e375a7a30cbfd95d79b71ae2e1e438a9b730fb27e48eb343d0b981a1`  
		Last Modified: Tue, 08 Apr 2025 01:29:40 GMT  
		Size: 289.7 MB (289710769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b34dca3bdc3700658baef2ef87246f01f1276f019a270f7d6651094d9ef5bd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58e87bde78e6421ad5701ed6e1895b2146e37f9ddbb710e6c3564c5aeaa912d`

```dockerfile
```

-	Layers:
	-	`sha256:3a5f365726ead50a517bb7a1e0a66f89be048dd83aa40e156c91402f469e650f`  
		Last Modified: Tue, 08 Apr 2025 01:29:33 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48c9848cb48320622ba069df1d248315014d723047a5ad2fe5c0984f63b29b4`  
		Last Modified: Tue, 08 Apr 2025 01:29:32 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:7c698b86ae28c62f50194162e6ce3ccb20929b7e102dcc9451daae302a190c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367337074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583a28a59a2f362110c00233e30bd9cbe585d26d44f01bae200b8bfcacbc3dd4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b1b3a088ca3ea201af18986b7436e4aec60625258327e913df52ff8591370`  
		Last Modified: Tue, 08 Apr 2025 07:30:39 GMT  
		Size: 335.3 MB (335268843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:053e7e4791aacc14950e3e3fd33978f493690d41cf4a6ce384c31f8a6b28e790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de63ee76d9cad60f0ede2a9ebfa9ceaa8033826728ff25b231320f60c2a513e`

```dockerfile
```

-	Layers:
	-	`sha256:cb9a48cc982aca824da80a9466474cea0ca2889c619a740a0966fefe497cfeab`  
		Last Modified: Tue, 08 Apr 2025 07:30:30 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae8c4b9df6ac332d20cd1be109d998ae230fe05ebf9b7f6ee2cfb308c2bcb6d3`  
		Last Modified: Tue, 08 Apr 2025 07:30:29 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:6fbc766b1eba2d9ee4174bf5728c3d5cdfa04d6bd77051944c5c0fd8bff0295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5e6a02c07dc29b10ca722271c932c061c30824d57f634c336d1ea35d41f4cf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37b16f2d003c1f9e67bd6dfda070e17bd22a162101f28a4396a958280daf695`  
		Last Modified: Tue, 08 Apr 2025 06:20:23 GMT  
		Size: 344.0 MB (344011347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8547ff21e07816223e9f6766d42bea2cb69c579334e2ac18d625ac04749bb5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146d2be439c484209ca809cc8ce80871138fe27edf39a29a708fa317e8175305`

```dockerfile
```

-	Layers:
	-	`sha256:0b77fa511d03b0701d0ef55560b74a78f3f6e64e484e0095d3be54b544545131`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2add6570625fb08371b11c1a0bc8716a08b4fdd1ad3706bde7cf21f4d9323ff4`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0-slim-bullseye`

```console
$ docker pull rust@sha256:405e5b0fe9f74098d19f3a7b65368c9cd4323758dd6b2d6305a35df8d2cc0a2a
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

### `rust:1.86.0-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:f8c0bb10d0e408141ae1ce9db3906933d04044014b81315956bb8babefdb4538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289245429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701ed3fc33b113775a941d354adccbf40b6a225401b883ee5966de1c83f41b2b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88fad72c2506246ffe6396d482cf40fced3dbdcef8f4356795a7cac8ff6b2ef`  
		Last Modified: Tue, 08 Apr 2025 01:35:00 GMT  
		Size: 259.0 MB (258988010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4741338f8e175f2156ac1827a7e205ed3ea2f97dab9e129c70963ec485678779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0edf37b8243573464db9fa035308a4066da5453afcc99b305823cb05f7a7437`

```dockerfile
```

-	Layers:
	-	`sha256:9eb94d3eacd1815973a9e0b2b8d9ea7e1aba5c23b593f6bc9dcc7afb1bdd484c`  
		Last Modified: Tue, 08 Apr 2025 01:34:55 GMT  
		Size: 4.2 MB (4175124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ba3cecfcf1347fea0549f31ad4367cab149129294dc8dfc57ccf6d6f0813fff`  
		Last Modified: Tue, 08 Apr 2025 01:34:55 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:64862b5819093237df39378fbaa1b43498424fab0bec03cae5733be1b24142b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.0 MB (309037855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6173382e6c055035ab42b01f20d2e1159bc44baf086271255b1ca3daf44909`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fabdae83abb8c4e7989a8005a7a92a8535e6ab6c0bd633442c316443e6f2bab`  
		Last Modified: Tue, 08 Apr 2025 16:53:16 GMT  
		Size: 283.5 MB (283498720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a1e648062c749afa43013786ee2772e71053aae03cb4782bbc4537e21bc45a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3995706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80946ceab5e2263d6a3d2080648d12b9fa299c11ee188d9f752f9d87cf949f4e`

```dockerfile
```

-	Layers:
	-	`sha256:82474d826cb3957f1fe6d11964dabb805591e256095862418b74e61335f2d2bb`  
		Last Modified: Tue, 08 Apr 2025 16:53:10 GMT  
		Size: 4.0 MB (3984274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c1e96c51cd14f17a15a43d875ce615aeb964e08b5edb459ce6c20c3722eb049`  
		Last Modified: Tue, 08 Apr 2025 16:53:09 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:663387b95b7c33a5430b967b31ff194fcdda0a1ce99f5b57701067a097d7790e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252089618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714f3327734efe4ca704111ca38e47742d41d1d6dbf7fd5f688890f0d51b0358`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae574b04e648f49bc601b389c9fe05b55820b884d921b0be2237f6bcbe8a3f94`  
		Last Modified: Tue, 08 Apr 2025 10:47:57 GMT  
		Size: 223.3 MB (223340120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:82d09db72e41c93ab2119868ef3741a813878f94117b474e06283adb390fbeab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4183262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544589af526ae2c336c2f08de66d4d92a1e44abc4a3bc1dc03656c481d5d7819`

```dockerfile
```

-	Layers:
	-	`sha256:b88826ea138c560bd03b90c875666115d0b79433cb4be2921f0d1aa605f9dc33`  
		Last Modified: Tue, 08 Apr 2025 10:47:52 GMT  
		Size: 4.2 MB (4171802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1ef1d405fbb2d4f000818000750480dae3e874eb9e5dd56ae60396665119ffe`  
		Last Modified: Tue, 08 Apr 2025 10:47:51 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:43df35999046bea8233d1a5fdfcd2356fba15a793fbeb9fa5224d1262adf2960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314097491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d34f303281cbb2b93f669a37283d0e2d6c0068957020ef6fa5232b882c63638`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c7f226a3ed9e3a783e859dc8479e50da2694130147ffb4885645e02664eedbec`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 31.2 MB (31184573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b380f9c572c29705a08754c4980a85f7915a4d9cd340d7f3c36e3926cba3001`  
		Last Modified: Tue, 08 Apr 2025 01:29:00 GMT  
		Size: 282.9 MB (282912918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:19d00c62057a0ddf1ba7ff04c110803c0702d91dcdad6a4eed7e9ff8f85cc8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80ca8b84c676afa150db9ce38fd1bfaca44431b98cdac4af32efe184523a8ca`

```dockerfile
```

-	Layers:
	-	`sha256:80703f1c4e5c8b72cdde3f31569d00b27ba521369410893b3e2dbc529daa0b19`  
		Last Modified: Tue, 08 Apr 2025 01:28:53 GMT  
		Size: 4.2 MB (4165381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1fd41d56f3f22ed5780318a7bc49397260241142ba692570d227a36598e668b`  
		Last Modified: Tue, 08 Apr 2025 01:28:53 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:541a1720c1cedddae9e17b4214075bf57c20bc7b176b4bba6bce3437c44d51ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:ce413e392ed6c282a76beb447bfccc104136a46f2655df2df41fc0f04654c309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316237247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61d786d9f9c5cca0ab287fa99b7679ad755421530a8e95a8bd2cda19a69b856`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5c777dc8267f16eea52cc33c64c7b185aefaaaa260043622010c6e05333fd7`  
		Last Modified: Thu, 03 Apr 2025 17:12:15 GMT  
		Size: 61.6 MB (61564834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e319873236c572a5816c152bdb5011118b8ae9c672790e2ec264fbaafa4ddf`  
		Last Modified: Thu, 03 Apr 2025 17:12:18 GMT  
		Size: 251.0 MB (251030166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:dec7a5b5c43f2a69e7e1cd89b74f027b8ba4ac636e6654f30374a8143acce18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f0eca96243ca4fe82ac8c256aa685c9ed10eac95db72e1b176381f13e144e2`

```dockerfile
```

-	Layers:
	-	`sha256:cbd99f0e8b79ec516d96f3aee08b442562fc75cac2649bcb0a800ea915a0714a`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfec6d6b7554872ae59d5b3dc085d0c9287383d5bcb072f16cb8ac7fb44efbc3`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:45e626fcf2ef7f58c8b112b01657060691996ab4b4b3432a3f119afc93dd3875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (319016934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e2d039a6466c76b77a98bc81bba79858b86a3e5ab8a7c040094a491246270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63214d4c52deb7cd72dfb7b8ee63339ab9ba46086f6c52f3fc22c42a4cc6354c`  
		Last Modified: Wed, 19 Mar 2025 01:06:39 GMT  
		Size: 59.1 MB (59101227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa19e22237227dd4aba81e7f9e8743ac6f1828d92265e2ab9769fc3af195e04`  
		Last Modified: Thu, 03 Apr 2025 17:17:12 GMT  
		Size: 255.9 MB (255922678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:632262d43e3f35ced6b1ab847cc01838d21e8088bcd90a00889666a132b432b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37903037391a8658de906154ce8a47191fa1a8bf38f2a28471f7947cbf39b9b0`

```dockerfile
```

-	Layers:
	-	`sha256:1b5a4bc32a00e922f7028b1c3560d72456d27fdbc45f6525d545f9f313f21c09`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0fbb2e69c51339ac830b15829e85032b03271d892d1327f0628435616478b9c`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.20`

```console
$ docker pull rust@sha256:2ee35275aeaa2e438f34a0563f7931988f5c5254e2eeec562f95a60ca2a2e7c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:b07e0b6e63438f28b28ab8976881ae0a926af4da9fbe9288ed0fe69138690c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.0 MB (309972637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86009d33dc0da7a31e9d46f4f6954d7e7b0166da8ebbbdf47d6cbd1c09829847`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda11a1c7cdfc868caa20205c5191c9e175af463da2d48ab5c74561819b4cbea`  
		Last Modified: Thu, 03 Apr 2025 17:11:17 GMT  
		Size: 55.3 MB (55315639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55f3dceec5bf9dd5986d21f22e336fc8efccac71e961895a64688eb12863f3c`  
		Last Modified: Thu, 03 Apr 2025 17:11:22 GMT  
		Size: 251.0 MB (251030101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:c9ce1958f067088ab558b7b6319833afff6b777d67358dbcfe70b9da0efb7ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 KB (720201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a217f7fcce5e6762e7f71ad217556d3f4a942e64e66b12b91b30c51c8734ffc`

```dockerfile
```

-	Layers:
	-	`sha256:fbf4d52494216492b9e0cbcae0e1ad2eb0b2153e57c111b027c08f966da96c79`  
		Last Modified: Thu, 03 Apr 2025 17:11:15 GMT  
		Size: 709.5 KB (709488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d67dd3f9a37cf39335b9f2e242627d47bd6a5b1b6fcd8474b54957de8f8fd84`  
		Last Modified: Thu, 03 Apr 2025 17:11:14 GMT  
		Size: 10.7 KB (10713 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:28b8265454853aeb6fd5b4dfd02b0223f6349204f348663e2c7551fc9a984541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312964800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272469f2176bd29846696edd36f27ed458dcddadb03bd9b7967197df0e6d94e2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7362932bfc33faed0c84d60ed0d4aefe9e34b5b9366cfa2015a14c01e2604`  
		Last Modified: Wed, 19 Mar 2025 04:51:19 GMT  
		Size: 53.0 MB (52950559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da216a1abe7d23357c54f3c639e81a67652f254c496e34ca5ed47c3a49b9582`  
		Last Modified: Thu, 03 Apr 2025 17:16:01 GMT  
		Size: 255.9 MB (255923076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:be732f17ad9e5e6e7cf13ee3a78836ae6ffae078de73425995fd283f4a6f1e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 KB (756253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8093eb3b99a9036476b177c449878affb005e2ea60bd33c51dfbba375427b1f`

```dockerfile
```

-	Layers:
	-	`sha256:8d233587293019133f0bd1ba7d43eb76c4ec6b3e670421c4e41787189d73c449`  
		Last Modified: Thu, 03 Apr 2025 17:15:55 GMT  
		Size: 745.4 KB (745420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce0e73bdd8ebfaaec68f238d168a0405459eead3889f55c922f39f2bba99938`  
		Last Modified: Thu, 03 Apr 2025 17:15:55 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.21`

```console
$ docker pull rust@sha256:541a1720c1cedddae9e17b4214075bf57c20bc7b176b4bba6bce3437c44d51ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:ce413e392ed6c282a76beb447bfccc104136a46f2655df2df41fc0f04654c309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316237247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61d786d9f9c5cca0ab287fa99b7679ad755421530a8e95a8bd2cda19a69b856`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5c777dc8267f16eea52cc33c64c7b185aefaaaa260043622010c6e05333fd7`  
		Last Modified: Thu, 03 Apr 2025 17:12:15 GMT  
		Size: 61.6 MB (61564834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e319873236c572a5816c152bdb5011118b8ae9c672790e2ec264fbaafa4ddf`  
		Last Modified: Thu, 03 Apr 2025 17:12:18 GMT  
		Size: 251.0 MB (251030166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:dec7a5b5c43f2a69e7e1cd89b74f027b8ba4ac636e6654f30374a8143acce18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **793.3 KB (793263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f0eca96243ca4fe82ac8c256aa685c9ed10eac95db72e1b176381f13e144e2`

```dockerfile
```

-	Layers:
	-	`sha256:cbd99f0e8b79ec516d96f3aee08b442562fc75cac2649bcb0a800ea915a0714a`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 781.3 KB (781345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfec6d6b7554872ae59d5b3dc085d0c9287383d5bcb072f16cb8ac7fb44efbc3`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:45e626fcf2ef7f58c8b112b01657060691996ab4b4b3432a3f119afc93dd3875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (319016934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e2d039a6466c76b77a98bc81bba79858b86a3e5ab8a7c040094a491246270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='8e60c9157b7aa2bf32baab5c124b80a31dd24ba6c41b39b50645d354d381f831' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b3ceb9642150570b1cc43b279441dc98062a100b1974e9f6a518517c8b5900a8' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63214d4c52deb7cd72dfb7b8ee63339ab9ba46086f6c52f3fc22c42a4cc6354c`  
		Last Modified: Wed, 19 Mar 2025 01:06:39 GMT  
		Size: 59.1 MB (59101227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa19e22237227dd4aba81e7f9e8743ac6f1828d92265e2ab9769fc3af195e04`  
		Last Modified: Thu, 03 Apr 2025 17:17:12 GMT  
		Size: 255.9 MB (255922678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:632262d43e3f35ced6b1ab847cc01838d21e8088bcd90a00889666a132b432b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.0 KB (873016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37903037391a8658de906154ce8a47191fa1a8bf38f2a28471f7947cbf39b9b0`

```dockerfile
```

-	Layers:
	-	`sha256:1b5a4bc32a00e922f7028b1c3560d72456d27fdbc45f6525d545f9f313f21c09`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 860.9 KB (860931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0fbb2e69c51339ac830b15829e85032b03271d892d1327f0628435616478b9c`  
		Last Modified: Thu, 03 Apr 2025 17:17:06 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:6a6dda669f020fa1fcb0903e37a049484fbf4b4699c8cb89db26ca030f475259
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
$ docker pull rust@sha256:e2c3cc250468c6290044b6f8b8254ac79219b17c3232804e4a79b651d0c031a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547073889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dee95e9b67a7bb176a7084f8e543e0ec50c67fee8c69770f9a8e20c659bca81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b617a119f8a27982374d94ec6eb3738ae3d38d6fc2c34c865813926cf596a621`  
		Last Modified: Tue, 08 Apr 2025 03:16:47 GMT  
		Size: 211.3 MB (211331550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74a39eb585dbe3732f07ffb8ce7351ff0725ce605cd0585470613834f464774`  
		Last Modified: Tue, 08 Apr 2025 04:21:31 GMT  
		Size: 198.8 MB (198844240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3509ec4e64b314235325eee7ebafc7f34e2f3ed18cdd2db1ee62e45e56c88418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb7ce20ad7522cd62fcddacdcd2610e03d6632563b739d9cbb6971a476918e6`

```dockerfile
```

-	Layers:
	-	`sha256:769f4e29352c2ec152cb9cb46918f0fb247e33b661cc190886c060f1b9bb5662`  
		Last Modified: Tue, 08 Apr 2025 04:21:26 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f071db2499bcd484721f1239e87ae438c36ca8d5af3bb29b6b8c7758232701`  
		Last Modified: Tue, 08 Apr 2025 04:21:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:e2f34964c241e7ea71a854eb91e0b225a2418936648499283d14c73abae98a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542260031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16535fe936f9919d4b6beff652f4c5e4d3e625c13bfff7fa4247510f19399638`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a319072ea86a8c9aa06075cbf6677da28654a48a38fc6adb52aa04f271ddd06`  
		Last Modified: Tue, 18 Mar 2025 07:30:13 GMT  
		Size: 21.9 MB (21918018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f325c93a6cb0439e3bf485f3a1ca5c31cca2f6b205d5c37e15890e18b5fe0`  
		Last Modified: Tue, 18 Mar 2025 15:26:53 GMT  
		Size: 59.6 MB (59639263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407c08ebab5377348ed14160a63d8d957a380f355e742fcec3755c68baf9c20d`  
		Last Modified: Tue, 18 Mar 2025 16:12:56 GMT  
		Size: 175.3 MB (175309168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dd9c885e006c5ba163c1af9605526e79f2905da43c9de3a5037b5f4a902ee5`  
		Last Modified: Thu, 03 Apr 2025 17:15:51 GMT  
		Size: 241.2 MB (241215579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:dfebee42501bc9ae716db67f70571ab1c43cae2aa84b8465558968c336c7bb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15287641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea10ffe1f6ecb4c95a552c05741fc7bbfa6e7501c663039937ea61b2f769b014`

```dockerfile
```

-	Layers:
	-	`sha256:721c7e73d5bf649a41efdad2260e00c896508c024f704b6dc26802980b057621`  
		Last Modified: Thu, 03 Apr 2025 17:15:45 GMT  
		Size: 15.3 MB (15274394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771ebeb25304716d614718f27531976702dafcdae3ae12e4f819037aa9509b53`  
		Last Modified: Thu, 03 Apr 2025 17:15:44 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8489b54bc057a93babd8906b056fe4c67f0e77e1d19fc18eb8fca8305067ae26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506607013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead27b748614e277ca15ac3636b936d4e471ad7ecf24da4587ddf7ac3cd9f419`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9d474cce081e468bc6f85727459852112ba732fbbfe3236fae66c5fa8a5ed5`  
		Last Modified: Tue, 18 Mar 2025 14:10:35 GMT  
		Size: 202.8 MB (202753988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadb53c2ea73a273e0e6fe4e18341f4291c24756dcbee8ad109038b067c0f8f4`  
		Last Modified: Thu, 03 Apr 2025 17:13:37 GMT  
		Size: 167.6 MB (167648030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a48df1ec2a1e0ba16e84f7bb2189beb15a1aa86dd28a81bd65acba1470f9482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a632aa94d376b315058678dfd1194d1f04a4d851360ec98e10a5ab1f8239f18e`

```dockerfile
```

-	Layers:
	-	`sha256:86d2e91568072d7cf8f5f4aae6ec90b5a8825cb28ef55a1a29fe724454047aa2`  
		Last Modified: Thu, 03 Apr 2025 17:13:34 GMT  
		Size: 15.5 MB (15498527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fe3ef790dced91066659ab58e76acdd4fdd0f583148f161765e84ac8014bc2`  
		Last Modified: Thu, 03 Apr 2025 17:13:33 GMT  
		Size: 13.3 KB (13289 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:b06f5a923b052f2fbce21856fac2a8cbd4526310f9a22fae41a0b52388579188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572973806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cbc7d1b2a98309adc0f9f209d81640bd7a80c92e6bb5f5d4cda79343bea281`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7cbed080b4cdef804ca7e1b5bf4f3bc870dbef54cd5c74053fef6b147056`  
		Last Modified: Tue, 08 Apr 2025 01:23:54 GMT  
		Size: 24.8 MB (24847203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ffc3e6085548412ccbe96cfa7c6e138ccc7724d5a764a6a99e732fca48b289`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 66.2 MB (66237424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8471ab4232bc51e32c08f3c8fae6e33670c6c77fa4a3359a48d05453051f93e`  
		Last Modified: Tue, 08 Apr 2025 03:17:21 GMT  
		Size: 210.3 MB (210267336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ab54bb87b446c157a467a30d193edfb918d405722cf4c7b60d8f93b3a06b1a`  
		Last Modified: Tue, 08 Apr 2025 04:21:02 GMT  
		Size: 222.1 MB (222143712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:efc9f3a3297418eaf506f8ea51750f360027cbb3201e9a77d7ca1e1baaf7dc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da045b658f2b336a573f002e616b2fc8c51911ed0e2cb15e088c1c739a37e94d`

```dockerfile
```

-	Layers:
	-	`sha256:41bae4c1c5e052f6bdf0a312634e204ce48fb5ed8ab4309743503426c887ad5b`  
		Last Modified: Tue, 08 Apr 2025 04:20:57 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85eac65f6e9308480c58b3d5c215045ff30d0e9566710981c869dfa18a5f49a`  
		Last Modified: Tue, 08 Apr 2025 04:20:56 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:0b20be231028bfd49a688c56aea6e25cf138c49012ce5addadc5bf68ad029674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628711168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c542d6616e2ce45fb4557eb923016df6ded64d6756d6212a69bbfdbfa2aeaf3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c3d0039c25f88e5b7c3da861e5a41bc617f045eff9521b410ceced36c47c971`  
		Last Modified: Mon, 17 Mar 2025 22:17:38 GMT  
		Size: 52.3 MB (52306033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b570e1ccee8c153bcd6622cbc7c9c8f1150932eca72b58d0e1d93a81c2d4b`  
		Last Modified: Tue, 18 Mar 2025 00:06:46 GMT  
		Size: 25.7 MB (25650089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3219f8cada3f1c641a91887b1112d0699cc708ea02d9c8f85a77e08659008bf`  
		Last Modified: Tue, 18 Mar 2025 07:04:49 GMT  
		Size: 69.8 MB (69844086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4c6aa27e302a908ce45a312c9a7c6eab49c831e12f24c5b4c29145d2d6ab77`  
		Last Modified: Tue, 18 Mar 2025 13:50:48 GMT  
		Size: 214.4 MB (214407742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794fac3bd448ad09edaa36a6cde07f66551a607b885eb53d5f2021f315d4f3a1`  
		Last Modified: Thu, 03 Apr 2025 17:12:22 GMT  
		Size: 266.5 MB (266503218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bdcd78b6c3e9fe62dc32903e0e40321ad1dcb75565546a46b7fcb80c80d051a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b2473977886e04bd3f2fa7f647e75326f6f9692e51ddd99b58f5b6a3f33ce4`

```dockerfile
```

-	Layers:
	-	`sha256:285e9d5c95682b386fd734af5f45355fd2b768e4de10b666c7928c0865c17115`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 15.4 MB (15445052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2784c65f478f48009daf0d9be5e9eb15f877c29df9a514d10ae1f463b05d5abe`  
		Last Modified: Thu, 03 Apr 2025 17:12:02 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:f48c071cd1dbf6e7f913bd6786412be97c82f25dc7e07ec327777838a47a15ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611934465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7d2d1236345049aad144c2d5ba643f4117f44e14bc7d7a4cd83c3ec56235d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea48981a9fc9115877d4666b28ace59b31b650cc30850dc9dbcd586ba0a496cb`  
		Last Modified: Mon, 17 Mar 2025 22:26:07 GMT  
		Size: 47.1 MB (47127836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d2fcabaa2191a259a1c138c1eae49463f7916a91e0b0f61fdbaa5dba7f4e2`  
		Last Modified: Tue, 18 Mar 2025 02:53:59 GMT  
		Size: 24.0 MB (24007981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e4163fc9bb4b1cfe20bf3ee0f067c3cb219407f1ed0b91eb04a5759f702712`  
		Last Modified: Tue, 18 Mar 2025 05:55:51 GMT  
		Size: 63.5 MB (63498480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f2a6b02b0e41028d194dbcc5b64d0cad2bdb30fa6390057978ddcf6ef155f8`  
		Last Modified: Tue, 18 Mar 2025 09:15:15 GMT  
		Size: 183.4 MB (183397092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15db11f7134bcabfcadf4efd6f83b0adb817278124e7abf84c09e8f2ace4d0e`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 293.9 MB (293903076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:24e6102ed3718659338647ed86c5ef77a3aed787e69c279a8b5a161b2dcee7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15295779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d32f0eae7397ef0bb4dc33fd8d1fd800859d56d4071a54e533f4f5da705fdf`

```dockerfile
```

-	Layers:
	-	`sha256:3bc6a1475676787f936efb971e18c1fd827cc2e06dde956322e7e95e32062df1`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 15.3 MB (15282640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f55e26963096390aa8b80788e20cf1bfd491126b210047525a73c44588be51`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:7a8c32ed3e4407a50d35985e0602f42c1f78ea6ae13930e3ace8205d573fd43f
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
$ docker pull rust@sha256:19c3a05a2f4be47ee8cbce22c200f09a16a378a1150bd4019fa5f0ac630e609b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.2 MB (520218264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b03f8c11be37e006c1e9735f2cf80ff0be92fcb7662a408c1e380365e6fa1bb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7819131060d3c79e48555fb5b04fa584b86d2fb80e3ede0864c7e6bba7d87`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 15.8 MB (15763510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f843b455b9b7bececb5cfeb4ba5839d4aa47845ded1258734c375304df3d0`  
		Last Modified: Tue, 08 Apr 2025 02:13:52 GMT  
		Size: 54.8 MB (54755152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b731139994e4dbd527b938ba04d372fec4d9d7302e7f454003dc0b3485c05bb1`  
		Last Modified: Tue, 08 Apr 2025 03:17:23 GMT  
		Size: 197.1 MB (197105555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056d1ad25ed6f278ed43ffa359808bab69a55df6afc883e564cb8c8768160524`  
		Last Modified: Tue, 08 Apr 2025 04:21:23 GMT  
		Size: 198.8 MB (198845518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6eaea83e5ca843f5257ac5886c846ed9d2607868f4d96b02bb4d6dc390341595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15086810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf77a97c2724f28d4b6a8a0ba1ac79caafacb92bc07435739b9410c5315274d`

```dockerfile
```

-	Layers:
	-	`sha256:1f6c5eb822984d31b2a2285ca0d64cd1827a12c9a40dc33817afa4bb7094f578`  
		Last Modified: Tue, 08 Apr 2025 04:21:19 GMT  
		Size: 15.1 MB (15075561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70368749ca14fffe47e32e606e5c77ad9e0468cf7cd92010ccd9218052806e8c`  
		Last Modified: Tue, 08 Apr 2025 04:21:19 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:2355887e87ec08c9db4665d5856f0e5dde1a1b436d7ef1ebedbc71f6aa4288b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.1 MB (523115497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956da94b04af8a4f1ba79acfd8f8f637cb0251bd8292b6e013d0607a18f48f0a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c0fd1793bf8bc1764ff6503ad6f86ae0f1151de2bd8b7285b28dc6f5cc6001c3`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 49.0 MB (49026561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fd5d78189f9a0219a8d445519fe59067dcfa82b8799cf047c0b783ffa33a78`  
		Last Modified: Tue, 18 Mar 2025 07:26:06 GMT  
		Size: 14.7 MB (14674012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31183489ce2b77443c42eee08badb4a4fcf8ad4cef9299e71603f2239cb4064`  
		Last Modified: Tue, 18 Mar 2025 15:29:13 GMT  
		Size: 50.6 MB (50640225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6676c7b3b77e9e71cb741c5c04bfd9a595560092d9024884d0ce64c66f48bc6`  
		Last Modified: Tue, 18 Mar 2025 16:15:00 GMT  
		Size: 167.6 MB (167559857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b86ba427e0fae57b323d1a94b5942db3ef6663580549d5abeeaff2e6671eeb7`  
		Last Modified: Thu, 03 Apr 2025 17:11:34 GMT  
		Size: 241.2 MB (241214842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:02ad46142f4af7ad1d5deb91011c07cef40aa34ba654a2afff289dcec3b5edd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e693efb626079c5d179344964747f1db704955b930abdc9372eb60dd7d37b2`

```dockerfile
```

-	Layers:
	-	`sha256:fbf9e4eabc83ab73bf1172bd3b0216ea0257bad4e2bb7e7d735d5ad5ef2bccec`  
		Last Modified: Thu, 03 Apr 2025 17:11:29 GMT  
		Size: 14.9 MB (14874384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:897e8e84b1d8543de6c676fd27fe8bb89d0448b16d6464b9966887246a0ba0d4`  
		Last Modified: Thu, 03 Apr 2025 17:11:28 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:69d48decb7216958492661cea62057f649e080c0cd37360d4b74324867db6d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.3 MB (480316197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5114f900c5aa75bfd01846f195f411d4ccb4a7b272ad186738d04b0776e6a11`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645bc92dcf4a3c806f112acf0724041051eab86b13816f8d7286950facb47ec3`  
		Last Modified: Tue, 18 Mar 2025 05:00:00 GMT  
		Size: 15.5 MB (15544004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96fedce3b84d801b5eec66fa2ddb4a4653be64f8e04188e6e7ab37b6566bd34`  
		Last Modified: Tue, 18 Mar 2025 13:15:20 GMT  
		Size: 54.9 MB (54855429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15780e9924523e788780ac991f29afa248c22b09abb68f8a9945cf272b3dc84e`  
		Last Modified: Tue, 18 Mar 2025 14:12:21 GMT  
		Size: 190.0 MB (190020786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b53efaeee4c92c572f617852fe5add72eed90d7c8f3416dcaff2bdaf40c47af`  
		Last Modified: Thu, 03 Apr 2025 17:10:56 GMT  
		Size: 167.6 MB (167647584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d0b352a4def49f1720c30632fc5dd136d73b3e2f9b904e02471089d27a3d2497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15087206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d14e3af14e7f5e5a1d29988d0c4bcb918ce2cb76c209f37cf16cf8ab2a83f3d`

```dockerfile
```

-	Layers:
	-	`sha256:70f71d6a962c6cd40615d935896c2467b5730056acbdcc9132c27fde862a3401`  
		Last Modified: Thu, 03 Apr 2025 17:10:55 GMT  
		Size: 15.1 MB (15075853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90c75b489dac3fed9aabb83068b4b8336b7ed3e8eb253a534ae509cc7ed1ec2b`  
		Last Modified: Thu, 03 Apr 2025 17:10:52 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:3a72bca02f43cd0d9f449b127103aadd427ff987a9613b3bc088eeb699fee0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549154273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c1a99516c42e56ce0d8c4e9108af14a30bf714c00ba497fe5b0818adb0458`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ffef4e17cbc252fc170472ff3910647beec8b91ac9abe188d6595b2087a0dc`  
		Last Modified: Tue, 08 Apr 2025 01:24:12 GMT  
		Size: 16.3 MB (16267037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684d7ac3a47d27aefe42d135394e4d8b703fb530ab3bd2ad6ef78b8c9beaf885`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 56.0 MB (56047217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f57b5c68cdb07f2657d3893b6b23c64ea31a47747ad68a064ff80bc616fdb51`  
		Last Modified: Tue, 08 Apr 2025 03:26:01 GMT  
		Size: 200.0 MB (200010627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9965d6680dd77db10541dab74f8fa0b74081c35a96fba815ca735a5bdba30db6`  
		Last Modified: Tue, 08 Apr 2025 04:20:42 GMT  
		Size: 222.1 MB (222144927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3f64b6b5e44466afdb2e0b9bc6fc4d01da31c626355b88f65650f57c3c2b176f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15073805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f9a17691493fcbefe1257efebd05e75f9d2247b27d8e4c2f0787e67400b081`

```dockerfile
```

-	Layers:
	-	`sha256:70606c1f443921a19b7f1ccd2601da80840aab493bd5fe9990c855778aa67324`  
		Last Modified: Tue, 08 Apr 2025 04:20:38 GMT  
		Size: 15.1 MB (15062588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760624857aafbce57f9c110b4cd55c6efb77f9b6f390378e3518a694baed7386`  
		Last Modified: Tue, 08 Apr 2025 04:20:37 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:6a6dda669f020fa1fcb0903e37a049484fbf4b4699c8cb89db26ca030f475259
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
$ docker pull rust@sha256:e2c3cc250468c6290044b6f8b8254ac79219b17c3232804e4a79b651d0c031a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547073889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dee95e9b67a7bb176a7084f8e543e0ec50c67fee8c69770f9a8e20c659bca81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b617a119f8a27982374d94ec6eb3738ae3d38d6fc2c34c865813926cf596a621`  
		Last Modified: Tue, 08 Apr 2025 03:16:47 GMT  
		Size: 211.3 MB (211331550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74a39eb585dbe3732f07ffb8ce7351ff0725ce605cd0585470613834f464774`  
		Last Modified: Tue, 08 Apr 2025 04:21:31 GMT  
		Size: 198.8 MB (198844240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:3509ec4e64b314235325eee7ebafc7f34e2f3ed18cdd2db1ee62e45e56c88418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb7ce20ad7522cd62fcddacdcd2610e03d6632563b739d9cbb6971a476918e6`

```dockerfile
```

-	Layers:
	-	`sha256:769f4e29352c2ec152cb9cb46918f0fb247e33b661cc190886c060f1b9bb5662`  
		Last Modified: Tue, 08 Apr 2025 04:21:26 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f071db2499bcd484721f1239e87ae438c36ca8d5af3bb29b6b8c7758232701`  
		Last Modified: Tue, 08 Apr 2025 04:21:25 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:e2f34964c241e7ea71a854eb91e0b225a2418936648499283d14c73abae98a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542260031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16535fe936f9919d4b6beff652f4c5e4d3e625c13bfff7fa4247510f19399638`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a319072ea86a8c9aa06075cbf6677da28654a48a38fc6adb52aa04f271ddd06`  
		Last Modified: Tue, 18 Mar 2025 07:30:13 GMT  
		Size: 21.9 MB (21918018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f325c93a6cb0439e3bf485f3a1ca5c31cca2f6b205d5c37e15890e18b5fe0`  
		Last Modified: Tue, 18 Mar 2025 15:26:53 GMT  
		Size: 59.6 MB (59639263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407c08ebab5377348ed14160a63d8d957a380f355e742fcec3755c68baf9c20d`  
		Last Modified: Tue, 18 Mar 2025 16:12:56 GMT  
		Size: 175.3 MB (175309168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dd9c885e006c5ba163c1af9605526e79f2905da43c9de3a5037b5f4a902ee5`  
		Last Modified: Thu, 03 Apr 2025 17:15:51 GMT  
		Size: 241.2 MB (241215579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:dfebee42501bc9ae716db67f70571ab1c43cae2aa84b8465558968c336c7bb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15287641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea10ffe1f6ecb4c95a552c05741fc7bbfa6e7501c663039937ea61b2f769b014`

```dockerfile
```

-	Layers:
	-	`sha256:721c7e73d5bf649a41efdad2260e00c896508c024f704b6dc26802980b057621`  
		Last Modified: Thu, 03 Apr 2025 17:15:45 GMT  
		Size: 15.3 MB (15274394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771ebeb25304716d614718f27531976702dafcdae3ae12e4f819037aa9509b53`  
		Last Modified: Thu, 03 Apr 2025 17:15:44 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8489b54bc057a93babd8906b056fe4c67f0e77e1d19fc18eb8fca8305067ae26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506607013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead27b748614e277ca15ac3636b936d4e471ad7ecf24da4587ddf7ac3cd9f419`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9d474cce081e468bc6f85727459852112ba732fbbfe3236fae66c5fa8a5ed5`  
		Last Modified: Tue, 18 Mar 2025 14:10:35 GMT  
		Size: 202.8 MB (202753988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadb53c2ea73a273e0e6fe4e18341f4291c24756dcbee8ad109038b067c0f8f4`  
		Last Modified: Thu, 03 Apr 2025 17:13:37 GMT  
		Size: 167.6 MB (167648030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:a48df1ec2a1e0ba16e84f7bb2189beb15a1aa86dd28a81bd65acba1470f9482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a632aa94d376b315058678dfd1194d1f04a4d851360ec98e10a5ab1f8239f18e`

```dockerfile
```

-	Layers:
	-	`sha256:86d2e91568072d7cf8f5f4aae6ec90b5a8825cb28ef55a1a29fe724454047aa2`  
		Last Modified: Thu, 03 Apr 2025 17:13:34 GMT  
		Size: 15.5 MB (15498527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fe3ef790dced91066659ab58e76acdd4fdd0f583148f161765e84ac8014bc2`  
		Last Modified: Thu, 03 Apr 2025 17:13:33 GMT  
		Size: 13.3 KB (13289 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:b06f5a923b052f2fbce21856fac2a8cbd4526310f9a22fae41a0b52388579188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572973806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cbc7d1b2a98309adc0f9f209d81640bd7a80c92e6bb5f5d4cda79343bea281`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7cbed080b4cdef804ca7e1b5bf4f3bc870dbef54cd5c74053fef6b147056`  
		Last Modified: Tue, 08 Apr 2025 01:23:54 GMT  
		Size: 24.8 MB (24847203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ffc3e6085548412ccbe96cfa7c6e138ccc7724d5a764a6a99e732fca48b289`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 66.2 MB (66237424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8471ab4232bc51e32c08f3c8fae6e33670c6c77fa4a3359a48d05453051f93e`  
		Last Modified: Tue, 08 Apr 2025 03:17:21 GMT  
		Size: 210.3 MB (210267336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ab54bb87b446c157a467a30d193edfb918d405722cf4c7b60d8f93b3a06b1a`  
		Last Modified: Tue, 08 Apr 2025 04:21:02 GMT  
		Size: 222.1 MB (222143712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:efc9f3a3297418eaf506f8ea51750f360027cbb3201e9a77d7ca1e1baaf7dc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da045b658f2b336a573f002e616b2fc8c51911ed0e2cb15e088c1c739a37e94d`

```dockerfile
```

-	Layers:
	-	`sha256:41bae4c1c5e052f6bdf0a312634e204ce48fb5ed8ab4309743503426c887ad5b`  
		Last Modified: Tue, 08 Apr 2025 04:20:57 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85eac65f6e9308480c58b3d5c215045ff30d0e9566710981c869dfa18a5f49a`  
		Last Modified: Tue, 08 Apr 2025 04:20:56 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:0b20be231028bfd49a688c56aea6e25cf138c49012ce5addadc5bf68ad029674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628711168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c542d6616e2ce45fb4557eb923016df6ded64d6756d6212a69bbfdbfa2aeaf3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6c3d0039c25f88e5b7c3da861e5a41bc617f045eff9521b410ceced36c47c971`  
		Last Modified: Mon, 17 Mar 2025 22:17:38 GMT  
		Size: 52.3 MB (52306033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b570e1ccee8c153bcd6622cbc7c9c8f1150932eca72b58d0e1d93a81c2d4b`  
		Last Modified: Tue, 18 Mar 2025 00:06:46 GMT  
		Size: 25.7 MB (25650089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3219f8cada3f1c641a91887b1112d0699cc708ea02d9c8f85a77e08659008bf`  
		Last Modified: Tue, 18 Mar 2025 07:04:49 GMT  
		Size: 69.8 MB (69844086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4c6aa27e302a908ce45a312c9a7c6eab49c831e12f24c5b4c29145d2d6ab77`  
		Last Modified: Tue, 18 Mar 2025 13:50:48 GMT  
		Size: 214.4 MB (214407742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794fac3bd448ad09edaa36a6cde07f66551a607b885eb53d5f2021f315d4f3a1`  
		Last Modified: Thu, 03 Apr 2025 17:12:22 GMT  
		Size: 266.5 MB (266503218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:bdcd78b6c3e9fe62dc32903e0e40321ad1dcb75565546a46b7fcb80c80d051a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b2473977886e04bd3f2fa7f647e75326f6f9692e51ddd99b58f5b6a3f33ce4`

```dockerfile
```

-	Layers:
	-	`sha256:285e9d5c95682b386fd734af5f45355fd2b768e4de10b666c7928c0865c17115`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 15.4 MB (15445052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2784c65f478f48009daf0d9be5e9eb15f877c29df9a514d10ae1f463b05d5abe`  
		Last Modified: Thu, 03 Apr 2025 17:12:02 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:f48c071cd1dbf6e7f913bd6786412be97c82f25dc7e07ec327777838a47a15ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611934465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7d2d1236345049aad144c2d5ba643f4117f44e14bc7d7a4cd83c3ec56235d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea48981a9fc9115877d4666b28ace59b31b650cc30850dc9dbcd586ba0a496cb`  
		Last Modified: Mon, 17 Mar 2025 22:26:07 GMT  
		Size: 47.1 MB (47127836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d2fcabaa2191a259a1c138c1eae49463f7916a91e0b0f61fdbaa5dba7f4e2`  
		Last Modified: Tue, 18 Mar 2025 02:53:59 GMT  
		Size: 24.0 MB (24007981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e4163fc9bb4b1cfe20bf3ee0f067c3cb219407f1ed0b91eb04a5759f702712`  
		Last Modified: Tue, 18 Mar 2025 05:55:51 GMT  
		Size: 63.5 MB (63498480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f2a6b02b0e41028d194dbcc5b64d0cad2bdb30fa6390057978ddcf6ef155f8`  
		Last Modified: Tue, 18 Mar 2025 09:15:15 GMT  
		Size: 183.4 MB (183397092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15db11f7134bcabfcadf4efd6f83b0adb817278124e7abf84c09e8f2ace4d0e`  
		Last Modified: Thu, 03 Apr 2025 17:12:03 GMT  
		Size: 293.9 MB (293903076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:24e6102ed3718659338647ed86c5ef77a3aed787e69c279a8b5a161b2dcee7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15295779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d32f0eae7397ef0bb4dc33fd8d1fd800859d56d4071a54e533f4f5da705fdf`

```dockerfile
```

-	Layers:
	-	`sha256:3bc6a1475676787f936efb971e18c1fd827cc2e06dde956322e7e95e32062df1`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 15.3 MB (15282640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f55e26963096390aa8b80788e20cf1bfd491126b210047525a73c44588be51`  
		Last Modified: Thu, 03 Apr 2025 17:11:58 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:3f391b0678a6e0c88fd26f13e399c9c515ac47354e3cadfee7daee3b21651a4f
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
$ docker pull rust@sha256:41b809ac8846aeacb14ccb5dd79734dc6336b1e8888529c1e0a6d26931443b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297829415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b78d2068c9472719a39cfbd28a9e0133db41638ba76fb051d4920fd18f6357`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210bb45fea98f7e6faa766c3c761469f156896c67811f25bec9d45f29b1dcbf0`  
		Last Modified: Tue, 08 Apr 2025 01:35:04 GMT  
		Size: 269.6 MB (269602156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:dcbbf8a097555fecc6ee6d280575383a22bc6a9ab9d7c62b65bce2c5ac8b95b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4053ef871c854e51688a9e9d237bc0def61479d6a5e3fb1a875747ca86268418`

```dockerfile
```

-	Layers:
	-	`sha256:3a8e6fbc9faed90473194037bdf9c636eecebcd8b7aa883b8ce27862a1779d1c`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d055c2481171ed38a99a22ae56c4e7c2b1bd465a4daf50f1676878fc24ef3643`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:f2147dce0408c155cafde8cea27150a5716e908161387aa42d3d5cd5cc276e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313009317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfd2341a89215716ee5a10bd8b6d887794af904f07446e83403c73d9dc11c9a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f48bc660f38990c9b1a99eef7221c43c0941e46d2c77adb1059dcf83e133720`  
		Last Modified: Tue, 08 Apr 2025 16:49:54 GMT  
		Size: 289.1 MB (289071450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:d03db0f51b3c203366e2d84c10c12ecefa338936f585b5e4493d144c0dd27b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d1df47ee7b8d27a616f617be86cd4d2c4bf9e6bacc9d6fac6c37bd6e2f6dd3`

```dockerfile
```

-	Layers:
	-	`sha256:6390c2b58d4d8b999d967a77f6c60f6e39fb1edcc78af868a9d39f02ea9c65cf`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 3.8 MB (3772732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89d90b466102965ae43f68698343d7a6deca9a2fa42f42bbab5b189ff921d00`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea3f5851799ee3e8f16ab003ef563ccfb590e287eb7960ff91fe44688a3e587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261543175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f316977191bca409dac97a0cd223be43a03fac7acb153bafc4c857382a8ae29e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be93040355bf29c5c23f25725fbace42a8c4e87149f54781b767539dc20cf504`  
		Last Modified: Tue, 08 Apr 2025 10:49:02 GMT  
		Size: 233.5 MB (233476855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:7f6e5cdeadc7696bb55921e2a30219a5d48b483e09f9d698dd934b28bfa15ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4802987aca1475d13fc58155ab1989d5789510e7961ad326ff3f0c7a05e6fb99`

```dockerfile
```

-	Layers:
	-	`sha256:253b9ae3ce5e09b9e82ca1ac3fcbe67e8bd9332025c8e18c1badd9df3085b13c`  
		Last Modified: Tue, 08 Apr 2025 10:48:57 GMT  
		Size: 4.0 MB (3979012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd310d7f0f093aa881f6d6beb86fedbafca89eba3eabe30fe233daf93087a8c`  
		Last Modified: Tue, 08 Apr 2025 10:48:56 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:bb5180ab836d2b9765e970861a734726951e55b490d86045511c69cffe5dcd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318921500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1379b48bf43ced6ff1dc1e0bc7150af59edb7c1cdf3e52a2b612cb94b64bb124`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5717094e375a7a30cbfd95d79b71ae2e1e438a9b730fb27e48eb343d0b981a1`  
		Last Modified: Tue, 08 Apr 2025 01:29:40 GMT  
		Size: 289.7 MB (289710769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:b34dca3bdc3700658baef2ef87246f01f1276f019a270f7d6651094d9ef5bd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58e87bde78e6421ad5701ed6e1895b2146e37f9ddbb710e6c3564c5aeaa912d`

```dockerfile
```

-	Layers:
	-	`sha256:3a5f365726ead50a517bb7a1e0a66f89be048dd83aa40e156c91402f469e650f`  
		Last Modified: Tue, 08 Apr 2025 01:29:33 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48c9848cb48320622ba069df1d248315014d723047a5ad2fe5c0984f63b29b4`  
		Last Modified: Tue, 08 Apr 2025 01:29:32 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:7c698b86ae28c62f50194162e6ce3ccb20929b7e102dcc9451daae302a190c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367337074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583a28a59a2f362110c00233e30bd9cbe585d26d44f01bae200b8bfcacbc3dd4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b1b3a088ca3ea201af18986b7436e4aec60625258327e913df52ff8591370`  
		Last Modified: Tue, 08 Apr 2025 07:30:39 GMT  
		Size: 335.3 MB (335268843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:053e7e4791aacc14950e3e3fd33978f493690d41cf4a6ce384c31f8a6b28e790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de63ee76d9cad60f0ede2a9ebfa9ceaa8033826728ff25b231320f60c2a513e`

```dockerfile
```

-	Layers:
	-	`sha256:cb9a48cc982aca824da80a9466474cea0ca2889c619a740a0966fefe497cfeab`  
		Last Modified: Tue, 08 Apr 2025 07:30:30 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae8c4b9df6ac332d20cd1be109d998ae230fe05ebf9b7f6ee2cfb308c2bcb6d3`  
		Last Modified: Tue, 08 Apr 2025 07:30:29 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:6fbc766b1eba2d9ee4174bf5728c3d5cdfa04d6bd77051944c5c0fd8bff0295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5e6a02c07dc29b10ca722271c932c061c30824d57f634c336d1ea35d41f4cf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37b16f2d003c1f9e67bd6dfda070e17bd22a162101f28a4396a958280daf695`  
		Last Modified: Tue, 08 Apr 2025 06:20:23 GMT  
		Size: 344.0 MB (344011347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:8547ff21e07816223e9f6766d42bea2cb69c579334e2ac18d625ac04749bb5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146d2be439c484209ca809cc8ce80871138fe27edf39a29a708fa317e8175305`

```dockerfile
```

-	Layers:
	-	`sha256:0b77fa511d03b0701d0ef55560b74a78f3f6e64e484e0095d3be54b544545131`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2add6570625fb08371b11c1a0bc8716a08b4fdd1ad3706bde7cf21f4d9323ff4`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:3f391b0678a6e0c88fd26f13e399c9c515ac47354e3cadfee7daee3b21651a4f
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
$ docker pull rust@sha256:41b809ac8846aeacb14ccb5dd79734dc6336b1e8888529c1e0a6d26931443b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297829415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b78d2068c9472719a39cfbd28a9e0133db41638ba76fb051d4920fd18f6357`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210bb45fea98f7e6faa766c3c761469f156896c67811f25bec9d45f29b1dcbf0`  
		Last Modified: Tue, 08 Apr 2025 01:35:04 GMT  
		Size: 269.6 MB (269602156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:dcbbf8a097555fecc6ee6d280575383a22bc6a9ab9d7c62b65bce2c5ac8b95b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4053ef871c854e51688a9e9d237bc0def61479d6a5e3fb1a875747ca86268418`

```dockerfile
```

-	Layers:
	-	`sha256:3a8e6fbc9faed90473194037bdf9c636eecebcd8b7aa883b8ce27862a1779d1c`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d055c2481171ed38a99a22ae56c4e7c2b1bd465a4daf50f1676878fc24ef3643`  
		Last Modified: Tue, 08 Apr 2025 01:34:59 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:f2147dce0408c155cafde8cea27150a5716e908161387aa42d3d5cd5cc276e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313009317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfd2341a89215716ee5a10bd8b6d887794af904f07446e83403c73d9dc11c9a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f48bc660f38990c9b1a99eef7221c43c0941e46d2c77adb1059dcf83e133720`  
		Last Modified: Tue, 08 Apr 2025 16:49:54 GMT  
		Size: 289.1 MB (289071450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d03db0f51b3c203366e2d84c10c12ecefa338936f585b5e4493d144c0dd27b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d1df47ee7b8d27a616f617be86cd4d2c4bf9e6bacc9d6fac6c37bd6e2f6dd3`

```dockerfile
```

-	Layers:
	-	`sha256:6390c2b58d4d8b999d967a77f6c60f6e39fb1edcc78af868a9d39f02ea9c65cf`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 3.8 MB (3772732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89d90b466102965ae43f68698343d7a6deca9a2fa42f42bbab5b189ff921d00`  
		Last Modified: Tue, 08 Apr 2025 16:49:48 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea3f5851799ee3e8f16ab003ef563ccfb590e287eb7960ff91fe44688a3e587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261543175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f316977191bca409dac97a0cd223be43a03fac7acb153bafc4c857382a8ae29e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be93040355bf29c5c23f25725fbace42a8c4e87149f54781b767539dc20cf504`  
		Last Modified: Tue, 08 Apr 2025 10:49:02 GMT  
		Size: 233.5 MB (233476855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7f6e5cdeadc7696bb55921e2a30219a5d48b483e09f9d698dd934b28bfa15ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4802987aca1475d13fc58155ab1989d5789510e7961ad326ff3f0c7a05e6fb99`

```dockerfile
```

-	Layers:
	-	`sha256:253b9ae3ce5e09b9e82ca1ac3fcbe67e8bd9332025c8e18c1badd9df3085b13c`  
		Last Modified: Tue, 08 Apr 2025 10:48:57 GMT  
		Size: 4.0 MB (3979012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd310d7f0f093aa881f6d6beb86fedbafca89eba3eabe30fe233daf93087a8c`  
		Last Modified: Tue, 08 Apr 2025 10:48:56 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:bb5180ab836d2b9765e970861a734726951e55b490d86045511c69cffe5dcd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318921500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1379b48bf43ced6ff1dc1e0bc7150af59edb7c1cdf3e52a2b612cb94b64bb124`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5717094e375a7a30cbfd95d79b71ae2e1e438a9b730fb27e48eb343d0b981a1`  
		Last Modified: Tue, 08 Apr 2025 01:29:40 GMT  
		Size: 289.7 MB (289710769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b34dca3bdc3700658baef2ef87246f01f1276f019a270f7d6651094d9ef5bd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58e87bde78e6421ad5701ed6e1895b2146e37f9ddbb710e6c3564c5aeaa912d`

```dockerfile
```

-	Layers:
	-	`sha256:3a5f365726ead50a517bb7a1e0a66f89be048dd83aa40e156c91402f469e650f`  
		Last Modified: Tue, 08 Apr 2025 01:29:33 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48c9848cb48320622ba069df1d248315014d723047a5ad2fe5c0984f63b29b4`  
		Last Modified: Tue, 08 Apr 2025 01:29:32 GMT  
		Size: 13.2 KB (13219 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:7c698b86ae28c62f50194162e6ce3ccb20929b7e102dcc9451daae302a190c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367337074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583a28a59a2f362110c00233e30bd9cbe585d26d44f01bae200b8bfcacbc3dd4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14b1b3a088ca3ea201af18986b7436e4aec60625258327e913df52ff8591370`  
		Last Modified: Tue, 08 Apr 2025 07:30:39 GMT  
		Size: 335.3 MB (335268843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:053e7e4791aacc14950e3e3fd33978f493690d41cf4a6ce384c31f8a6b28e790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de63ee76d9cad60f0ede2a9ebfa9ceaa8033826728ff25b231320f60c2a513e`

```dockerfile
```

-	Layers:
	-	`sha256:cb9a48cc982aca824da80a9466474cea0ca2889c619a740a0966fefe497cfeab`  
		Last Modified: Tue, 08 Apr 2025 07:30:30 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae8c4b9df6ac332d20cd1be109d998ae230fe05ebf9b7f6ee2cfb308c2bcb6d3`  
		Last Modified: Tue, 08 Apr 2025 07:30:29 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:6fbc766b1eba2d9ee4174bf5728c3d5cdfa04d6bd77051944c5c0fd8bff0295a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5e6a02c07dc29b10ca722271c932c061c30824d57f634c336d1ea35d41f4cf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37b16f2d003c1f9e67bd6dfda070e17bd22a162101f28a4396a958280daf695`  
		Last Modified: Tue, 08 Apr 2025 06:20:23 GMT  
		Size: 344.0 MB (344011347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8547ff21e07816223e9f6766d42bea2cb69c579334e2ac18d625ac04749bb5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146d2be439c484209ca809cc8ce80871138fe27edf39a29a708fa317e8175305`

```dockerfile
```

-	Layers:
	-	`sha256:0b77fa511d03b0701d0ef55560b74a78f3f6e64e484e0095d3be54b544545131`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2add6570625fb08371b11c1a0bc8716a08b4fdd1ad3706bde7cf21f4d9323ff4`  
		Last Modified: Tue, 08 Apr 2025 06:20:17 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:405e5b0fe9f74098d19f3a7b65368c9cd4323758dd6b2d6305a35df8d2cc0a2a
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
$ docker pull rust@sha256:f8c0bb10d0e408141ae1ce9db3906933d04044014b81315956bb8babefdb4538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289245429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701ed3fc33b113775a941d354adccbf40b6a225401b883ee5966de1c83f41b2b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88fad72c2506246ffe6396d482cf40fced3dbdcef8f4356795a7cac8ff6b2ef`  
		Last Modified: Tue, 08 Apr 2025 01:35:00 GMT  
		Size: 259.0 MB (258988010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4741338f8e175f2156ac1827a7e205ed3ea2f97dab9e129c70963ec485678779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0edf37b8243573464db9fa035308a4066da5453afcc99b305823cb05f7a7437`

```dockerfile
```

-	Layers:
	-	`sha256:9eb94d3eacd1815973a9e0b2b8d9ea7e1aba5c23b593f6bc9dcc7afb1bdd484c`  
		Last Modified: Tue, 08 Apr 2025 01:34:55 GMT  
		Size: 4.2 MB (4175124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ba3cecfcf1347fea0549f31ad4367cab149129294dc8dfc57ccf6d6f0813fff`  
		Last Modified: Tue, 08 Apr 2025 01:34:55 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:64862b5819093237df39378fbaa1b43498424fab0bec03cae5733be1b24142b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.0 MB (309037855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6173382e6c055035ab42b01f20d2e1159bc44baf086271255b1ca3daf44909`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fabdae83abb8c4e7989a8005a7a92a8535e6ab6c0bd633442c316443e6f2bab`  
		Last Modified: Tue, 08 Apr 2025 16:53:16 GMT  
		Size: 283.5 MB (283498720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a1e648062c749afa43013786ee2772e71053aae03cb4782bbc4537e21bc45a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3995706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80946ceab5e2263d6a3d2080648d12b9fa299c11ee188d9f752f9d87cf949f4e`

```dockerfile
```

-	Layers:
	-	`sha256:82474d826cb3957f1fe6d11964dabb805591e256095862418b74e61335f2d2bb`  
		Last Modified: Tue, 08 Apr 2025 16:53:10 GMT  
		Size: 4.0 MB (3984274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c1e96c51cd14f17a15a43d875ce615aeb964e08b5edb459ce6c20c3722eb049`  
		Last Modified: Tue, 08 Apr 2025 16:53:09 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:663387b95b7c33a5430b967b31ff194fcdda0a1ce99f5b57701067a097d7790e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252089618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714f3327734efe4ca704111ca38e47742d41d1d6dbf7fd5f688890f0d51b0358`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae574b04e648f49bc601b389c9fe05b55820b884d921b0be2237f6bcbe8a3f94`  
		Last Modified: Tue, 08 Apr 2025 10:47:57 GMT  
		Size: 223.3 MB (223340120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:82d09db72e41c93ab2119868ef3741a813878f94117b474e06283adb390fbeab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4183262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544589af526ae2c336c2f08de66d4d92a1e44abc4a3bc1dc03656c481d5d7819`

```dockerfile
```

-	Layers:
	-	`sha256:b88826ea138c560bd03b90c875666115d0b79433cb4be2921f0d1aa605f9dc33`  
		Last Modified: Tue, 08 Apr 2025 10:47:52 GMT  
		Size: 4.2 MB (4171802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1ef1d405fbb2d4f000818000750480dae3e874eb9e5dd56ae60396665119ffe`  
		Last Modified: Tue, 08 Apr 2025 10:47:51 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:43df35999046bea8233d1a5fdfcd2356fba15a793fbeb9fa5224d1262adf2960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314097491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d34f303281cbb2b93f669a37283d0e2d6c0068957020ef6fa5232b882c63638`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c7f226a3ed9e3a783e859dc8479e50da2694130147ffb4885645e02664eedbec`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 31.2 MB (31184573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b380f9c572c29705a08754c4980a85f7915a4d9cd340d7f3c36e3926cba3001`  
		Last Modified: Tue, 08 Apr 2025 01:29:00 GMT  
		Size: 282.9 MB (282912918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:19d00c62057a0ddf1ba7ff04c110803c0702d91dcdad6a4eed7e9ff8f85cc8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80ca8b84c676afa150db9ce38fd1bfaca44431b98cdac4af32efe184523a8ca`

```dockerfile
```

-	Layers:
	-	`sha256:80703f1c4e5c8b72cdde3f31569d00b27ba521369410893b3e2dbc529daa0b19`  
		Last Modified: Tue, 08 Apr 2025 01:28:53 GMT  
		Size: 4.2 MB (4165381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1fd41d56f3f22ed5780318a7bc49397260241142ba692570d227a36598e668b`  
		Last Modified: Tue, 08 Apr 2025 01:28:53 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json
