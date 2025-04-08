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
$ docker pull rust@sha256:249447250f1b9a75f5594a9e87f131622998cec0eb1477742cb29f8dfe933c47
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
$ docker pull rust@sha256:eb7e6764434a2bef33e68393177d061cc699d76fbc40f8d3301cd6ccac870c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572983715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb3ea8f24932f89b621228271fe3d9e453b1b3e20aea5e40e74f609521dee47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10bac27a676efda08e5b5aa398d8105182245c036138383494ad65da58e29e4`  
		Last Modified: Mon, 17 Mar 2025 23:32:45 GMT  
		Size: 24.8 MB (24846980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eb868ed69ff5115af5ee8fc248b3921cbc2936c23ef4556d264cc6842793cd`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 66.2 MB (66237259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e05e85a9740664efbffa28a6c9ab5ff6e64e564bd74dda762da2a13fc614b3`  
		Last Modified: Tue, 18 Mar 2025 01:13:58 GMT  
		Size: 210.3 MB (210299811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294695d0dacfa29cc31fb50ecfb4ca45feab85de0cb0d74bb46777640e160c61`  
		Last Modified: Thu, 03 Apr 2025 17:11:22 GMT  
		Size: 222.1 MB (222145185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:4231f06176670dffd20e1d8687ecf2849b8521991cf73360ebb69d9af9a03555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204ca13cabbb2b0c644990efefc2b83de967e2fca45fb4efffefe605f56089ad`

```dockerfile
```

-	Layers:
	-	`sha256:e2a240e2961c0c788f7ded3d2ecbb8bb5094202dafac8e1cbfabc2b529e5221d`  
		Last Modified: Thu, 03 Apr 2025 17:11:18 GMT  
		Size: 15.4 MB (15447217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f70ec62bd7b3025a317ef4637f2b9d2cbfc3eadb0478dc4fe063bf760720017`  
		Last Modified: Thu, 03 Apr 2025 17:11:17 GMT  
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
$ docker pull rust@sha256:249447250f1b9a75f5594a9e87f131622998cec0eb1477742cb29f8dfe933c47
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
$ docker pull rust@sha256:eb7e6764434a2bef33e68393177d061cc699d76fbc40f8d3301cd6ccac870c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572983715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb3ea8f24932f89b621228271fe3d9e453b1b3e20aea5e40e74f609521dee47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10bac27a676efda08e5b5aa398d8105182245c036138383494ad65da58e29e4`  
		Last Modified: Mon, 17 Mar 2025 23:32:45 GMT  
		Size: 24.8 MB (24846980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eb868ed69ff5115af5ee8fc248b3921cbc2936c23ef4556d264cc6842793cd`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 66.2 MB (66237259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e05e85a9740664efbffa28a6c9ab5ff6e64e564bd74dda762da2a13fc614b3`  
		Last Modified: Tue, 18 Mar 2025 01:13:58 GMT  
		Size: 210.3 MB (210299811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294695d0dacfa29cc31fb50ecfb4ca45feab85de0cb0d74bb46777640e160c61`  
		Last Modified: Thu, 03 Apr 2025 17:11:22 GMT  
		Size: 222.1 MB (222145185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4231f06176670dffd20e1d8687ecf2849b8521991cf73360ebb69d9af9a03555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204ca13cabbb2b0c644990efefc2b83de967e2fca45fb4efffefe605f56089ad`

```dockerfile
```

-	Layers:
	-	`sha256:e2a240e2961c0c788f7ded3d2ecbb8bb5094202dafac8e1cbfabc2b529e5221d`  
		Last Modified: Thu, 03 Apr 2025 17:11:18 GMT  
		Size: 15.4 MB (15447217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f70ec62bd7b3025a317ef4637f2b9d2cbfc3eadb0478dc4fe063bf760720017`  
		Last Modified: Thu, 03 Apr 2025 17:11:17 GMT  
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
$ docker pull rust@sha256:dea730db38a523c754db764c2dd5d7888c307a48e9167c0bc06ad83760fd45f5
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
$ docker pull rust@sha256:116ee24bc2bcf89ccd0df098b17cb62533758110249786fa82a4b7b4cfd52a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548923785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0223150941c1f151a39c1fd7b9fd2158d553757ca11184f3ce11742a5a8fabc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
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
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5503af74d5075005e8a2caef8b6b369ec49cf0d7a20dcdd1fe79d68aa4ba6c`  
		Last Modified: Mon, 17 Mar 2025 23:32:34 GMT  
		Size: 16.1 MB (16062045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfffc7337857c58b61734136d663ca328549ab864bf18f3217e50e3fdc25680`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 56.0 MB (56030008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df6c0e66903ef70af0189af240e3c0623f78105cc07d6d179e9ccce9fb96781`  
		Last Modified: Tue, 18 Mar 2025 01:13:46 GMT  
		Size: 200.0 MB (200008164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9a735890ea7b015e1d19036fb031bb7552e74a93669ffc6d2c4431b818edaf`  
		Last Modified: Thu, 03 Apr 2025 17:11:34 GMT  
		Size: 222.1 MB (222144951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fbe17c34b9c84ffc968b1b9436bd5edaed400e143670ab5871efcdd9738442cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657fe2fbe451682ec3fc344460a44690a5555b2ddc960f6e91042158e7561103`

```dockerfile
```

-	Layers:
	-	`sha256:b256b5471fa5852299fc7492e5cdaa7832b97e8339a236ee0ad6fb2ce0875f31`  
		Last Modified: Thu, 03 Apr 2025 17:11:29 GMT  
		Size: 15.1 MB (15060620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03b9746b8dc267ec4e985f761d56a8df08f701e18833adac3b4c9abec47544e6`  
		Last Modified: Thu, 03 Apr 2025 17:11:28 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:c9eb52a5885c612df1f3a4d33d8eda6551f4e031d9f70bf256c57dbcafb19ee9
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
$ docker pull rust@sha256:c2e7a7d6f29a9d7719c23ae8fcc1b1bad94252e19a4b8678fa6b9c37b0f1f8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312986330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf20e8fec8e0685a3f37b4febd5ec1b5df88f18d8cb8d213d9f0a2d4321bcc2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58adefba86783bc364d159fc22200bb03f894cb3fca161ea999164bd44ad114d`  
		Last Modified: Thu, 03 Apr 2025 17:17:42 GMT  
		Size: 289.1 MB (289071242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:efd2bc156bf4e4d29cf4066eee24be0a001f33841f36b13b443826c3f02d78df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536f8535a55f26676330b86e7d8cb8f4b2423781ee98ac90299fe3386a609a55`

```dockerfile
```

-	Layers:
	-	`sha256:0bcdf3f2aa00ce635c14e89d996f190c9aa59ae13e3b841a044aa295f1ee744f`  
		Last Modified: Thu, 03 Apr 2025 17:17:37 GMT  
		Size: 3.8 MB (3771430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7711827842af2a4b96a035321719b385bc8e7af71a53448df511cf5620ceb857`  
		Last Modified: Thu, 03 Apr 2025 17:17:36 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d99100695f972ea286dd147b28dd807afe671305fcd23b732af09e6808ab3b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261520590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d1de1d75b59c3594376db14d4d6aeec6eef299828cbe62d1ea269ab3afcdf8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69376836448bc4f9d8087267845eb8a699215cd30a26ffc0f9e22328a7d0699a`  
		Last Modified: Thu, 03 Apr 2025 17:14:48 GMT  
		Size: 233.5 MB (233476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:219256112fd42e45fbe31c73c48eed36274b06ee2564f608d5289081c28148c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304a63c101c2d9ee8827a02afa441b85e07c948ea21ecc3e5fd70857c66e4407`

```dockerfile
```

-	Layers:
	-	`sha256:21b6701ecafeeeae919bd7fb4f80cc83179b8e068d1647ede4c9adafdf5c1969`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
		Size: 4.0 MB (3977710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc59da900c4e5aacd5f290abd628dfe6026decfc4c9b9d97907fd5f30f8c22c`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
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
$ docker pull rust@sha256:a36b873515c7a154cc0025f743c0c21fb528189308617b0ed15c95d2d6cc33af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367314762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d3c94ba741ffa44249470b54024e0579a7f703793216268961a2fcff5cfcb6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d695732d21c179c92e5836b87c86603c671891bd1f9b5abfc579f62d0f627`  
		Last Modified: Thu, 03 Apr 2025 17:15:13 GMT  
		Size: 335.3 MB (335266948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:948446e8b6cdcdaef62423f730bfcfe2313c426578b52224c3866fafd4a97143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ba7219b45ac300f7a30f8055cf30c92bf74219e5a60b59433412a5319a147e`

```dockerfile
```

-	Layers:
	-	`sha256:f6bde322ffc902cb55d8b885a30b59db1527dcf2175b7c7fedbd0308c67f514e`  
		Last Modified: Thu, 03 Apr 2025 17:15:05 GMT  
		Size: 3.9 MB (3927928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31607417122df605649579f7ee4f3d01be51ae3603b2177b716180a7d164449`  
		Last Modified: Thu, 03 Apr 2025 17:15:04 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:fae104d7293dc4dec2b0bfa3d7c85b0ddb722b186b9dce3be618096ec50a0705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370871457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9c141f13ccee43ed7603ab4b606dd2115767f0d913925f999762c7118afc60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffe1d4aad8e16c34c41ca8abf6a12dabe09eae50a357ebef71e8afcd4d4e301`  
		Last Modified: Thu, 03 Apr 2025 17:14:22 GMT  
		Size: 344.0 MB (344010398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:32b19984f00d21884bb253746121346288d68655691691277e05040dc2978833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a108b23bf4af9c780bea0e00c4f8e83d12491c6df990fbfe1ace4c5478d26b37`

```dockerfile
```

-	Layers:
	-	`sha256:53fa0f0cc3073997feee47af9b8db8c47bb2fb3ed389e879e278b6aa4dd55c36`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 3.8 MB (3797267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40da86d43f0b95e47c685150107a93fcf90c5d099fb02fe0f6bc209188755c72`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:c9eb52a5885c612df1f3a4d33d8eda6551f4e031d9f70bf256c57dbcafb19ee9
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
$ docker pull rust@sha256:c2e7a7d6f29a9d7719c23ae8fcc1b1bad94252e19a4b8678fa6b9c37b0f1f8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312986330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf20e8fec8e0685a3f37b4febd5ec1b5df88f18d8cb8d213d9f0a2d4321bcc2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58adefba86783bc364d159fc22200bb03f894cb3fca161ea999164bd44ad114d`  
		Last Modified: Thu, 03 Apr 2025 17:17:42 GMT  
		Size: 289.1 MB (289071242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:efd2bc156bf4e4d29cf4066eee24be0a001f33841f36b13b443826c3f02d78df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536f8535a55f26676330b86e7d8cb8f4b2423781ee98ac90299fe3386a609a55`

```dockerfile
```

-	Layers:
	-	`sha256:0bcdf3f2aa00ce635c14e89d996f190c9aa59ae13e3b841a044aa295f1ee744f`  
		Last Modified: Thu, 03 Apr 2025 17:17:37 GMT  
		Size: 3.8 MB (3771430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7711827842af2a4b96a035321719b385bc8e7af71a53448df511cf5620ceb857`  
		Last Modified: Thu, 03 Apr 2025 17:17:36 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d99100695f972ea286dd147b28dd807afe671305fcd23b732af09e6808ab3b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261520590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d1de1d75b59c3594376db14d4d6aeec6eef299828cbe62d1ea269ab3afcdf8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69376836448bc4f9d8087267845eb8a699215cd30a26ffc0f9e22328a7d0699a`  
		Last Modified: Thu, 03 Apr 2025 17:14:48 GMT  
		Size: 233.5 MB (233476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:219256112fd42e45fbe31c73c48eed36274b06ee2564f608d5289081c28148c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304a63c101c2d9ee8827a02afa441b85e07c948ea21ecc3e5fd70857c66e4407`

```dockerfile
```

-	Layers:
	-	`sha256:21b6701ecafeeeae919bd7fb4f80cc83179b8e068d1647ede4c9adafdf5c1969`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
		Size: 4.0 MB (3977710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc59da900c4e5aacd5f290abd628dfe6026decfc4c9b9d97907fd5f30f8c22c`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
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
$ docker pull rust@sha256:a36b873515c7a154cc0025f743c0c21fb528189308617b0ed15c95d2d6cc33af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367314762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d3c94ba741ffa44249470b54024e0579a7f703793216268961a2fcff5cfcb6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d695732d21c179c92e5836b87c86603c671891bd1f9b5abfc579f62d0f627`  
		Last Modified: Thu, 03 Apr 2025 17:15:13 GMT  
		Size: 335.3 MB (335266948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:948446e8b6cdcdaef62423f730bfcfe2313c426578b52224c3866fafd4a97143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ba7219b45ac300f7a30f8055cf30c92bf74219e5a60b59433412a5319a147e`

```dockerfile
```

-	Layers:
	-	`sha256:f6bde322ffc902cb55d8b885a30b59db1527dcf2175b7c7fedbd0308c67f514e`  
		Last Modified: Thu, 03 Apr 2025 17:15:05 GMT  
		Size: 3.9 MB (3927928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31607417122df605649579f7ee4f3d01be51ae3603b2177b716180a7d164449`  
		Last Modified: Thu, 03 Apr 2025 17:15:04 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:fae104d7293dc4dec2b0bfa3d7c85b0ddb722b186b9dce3be618096ec50a0705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370871457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9c141f13ccee43ed7603ab4b606dd2115767f0d913925f999762c7118afc60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffe1d4aad8e16c34c41ca8abf6a12dabe09eae50a357ebef71e8afcd4d4e301`  
		Last Modified: Thu, 03 Apr 2025 17:14:22 GMT  
		Size: 344.0 MB (344010398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:32b19984f00d21884bb253746121346288d68655691691277e05040dc2978833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a108b23bf4af9c780bea0e00c4f8e83d12491c6df990fbfe1ace4c5478d26b37`

```dockerfile
```

-	Layers:
	-	`sha256:53fa0f0cc3073997feee47af9b8db8c47bb2fb3ed389e879e278b6aa4dd55c36`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 3.8 MB (3797267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40da86d43f0b95e47c685150107a93fcf90c5d099fb02fe0f6bc209188755c72`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:be137fabf963328d3ee0304496521dbbd3ca69af0fb8801155b5512c57e00515
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
$ docker pull rust@sha256:e325724019d0122003c69e3be4a0a71d6613243861e4187e34a215645256589b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308829763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c601a8eb2de08ddbfbd4cc187b317a74c571caa89f7071a5086014ce7e141708`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d05e5307839376198f22b171832782220d67b6bdd086664554ce6d987c7172c`  
		Last Modified: Thu, 03 Apr 2025 17:13:34 GMT  
		Size: 283.3 MB (283294419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:69cd421f2f4be3540bca681c6dd21edbff03203892c77ace8a7174106f2c987f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520975aebc7b52e9d2d354cf543a8572d8de9746b3395ae7d6c5e69cad573b2f`

```dockerfile
```

-	Layers:
	-	`sha256:822cb013a20cf21814005faafcf04e5465014d84ab49ec7ce7f62cae66c7c894`  
		Last Modified: Thu, 03 Apr 2025 17:13:27 GMT  
		Size: 4.0 MB (3982396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e9b343b1b2b9159f06c6a1b7c2d34bc589d5fface5d637c987212660eddcd54`  
		Last Modified: Thu, 03 Apr 2025 17:13:26 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7a54ab5c176dd6ba0d7b929683aaefa735929f71989029b48aadb23fb2d40642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251881734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f5359f1e436b09430003e77cc14e4e3968b4b24be4a6d8c4431af009ef81b7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507256b3d9772056115743145e266583385b05b43a68e8d3e732522c0c1487d0`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 223.1 MB (223135811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f3612ea27e656875b3165a0b1782de54ca3dc74e64437b08f3c564d0620382f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9424549dc96efa68ccf044bb50eafe08a3147ad572aa6d88b93306dd39dce40a`

```dockerfile
```

-	Layers:
	-	`sha256:7850f9163a23ca47e81c5a7f4b95ae374f2348f7edfc344e386d1ec95ef247cd`  
		Last Modified: Thu, 03 Apr 2025 17:12:06 GMT  
		Size: 4.2 MB (4169924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e57a8b24de7a434ab536b4cf649219fc6dbaba5df8160d56ffc0cc122ca254d`  
		Last Modified: Thu, 03 Apr 2025 17:12:06 GMT  
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
$ docker pull rust@sha256:249447250f1b9a75f5594a9e87f131622998cec0eb1477742cb29f8dfe933c47
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
$ docker pull rust@sha256:eb7e6764434a2bef33e68393177d061cc699d76fbc40f8d3301cd6ccac870c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572983715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb3ea8f24932f89b621228271fe3d9e453b1b3e20aea5e40e74f609521dee47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10bac27a676efda08e5b5aa398d8105182245c036138383494ad65da58e29e4`  
		Last Modified: Mon, 17 Mar 2025 23:32:45 GMT  
		Size: 24.8 MB (24846980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eb868ed69ff5115af5ee8fc248b3921cbc2936c23ef4556d264cc6842793cd`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 66.2 MB (66237259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e05e85a9740664efbffa28a6c9ab5ff6e64e564bd74dda762da2a13fc614b3`  
		Last Modified: Tue, 18 Mar 2025 01:13:58 GMT  
		Size: 210.3 MB (210299811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294695d0dacfa29cc31fb50ecfb4ca45feab85de0cb0d74bb46777640e160c61`  
		Last Modified: Thu, 03 Apr 2025 17:11:22 GMT  
		Size: 222.1 MB (222145185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86` - unknown; unknown

```console
$ docker pull rust@sha256:4231f06176670dffd20e1d8687ecf2849b8521991cf73360ebb69d9af9a03555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204ca13cabbb2b0c644990efefc2b83de967e2fca45fb4efffefe605f56089ad`

```dockerfile
```

-	Layers:
	-	`sha256:e2a240e2961c0c788f7ded3d2ecbb8bb5094202dafac8e1cbfabc2b529e5221d`  
		Last Modified: Thu, 03 Apr 2025 17:11:18 GMT  
		Size: 15.4 MB (15447217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f70ec62bd7b3025a317ef4637f2b9d2cbfc3eadb0478dc4fe063bf760720017`  
		Last Modified: Thu, 03 Apr 2025 17:11:17 GMT  
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
$ docker pull rust@sha256:249447250f1b9a75f5594a9e87f131622998cec0eb1477742cb29f8dfe933c47
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
$ docker pull rust@sha256:eb7e6764434a2bef33e68393177d061cc699d76fbc40f8d3301cd6ccac870c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572983715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb3ea8f24932f89b621228271fe3d9e453b1b3e20aea5e40e74f609521dee47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10bac27a676efda08e5b5aa398d8105182245c036138383494ad65da58e29e4`  
		Last Modified: Mon, 17 Mar 2025 23:32:45 GMT  
		Size: 24.8 MB (24846980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eb868ed69ff5115af5ee8fc248b3921cbc2936c23ef4556d264cc6842793cd`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 66.2 MB (66237259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e05e85a9740664efbffa28a6c9ab5ff6e64e564bd74dda762da2a13fc614b3`  
		Last Modified: Tue, 18 Mar 2025 01:13:58 GMT  
		Size: 210.3 MB (210299811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294695d0dacfa29cc31fb50ecfb4ca45feab85de0cb0d74bb46777640e160c61`  
		Last Modified: Thu, 03 Apr 2025 17:11:22 GMT  
		Size: 222.1 MB (222145185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4231f06176670dffd20e1d8687ecf2849b8521991cf73360ebb69d9af9a03555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204ca13cabbb2b0c644990efefc2b83de967e2fca45fb4efffefe605f56089ad`

```dockerfile
```

-	Layers:
	-	`sha256:e2a240e2961c0c788f7ded3d2ecbb8bb5094202dafac8e1cbfabc2b529e5221d`  
		Last Modified: Thu, 03 Apr 2025 17:11:18 GMT  
		Size: 15.4 MB (15447217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f70ec62bd7b3025a317ef4637f2b9d2cbfc3eadb0478dc4fe063bf760720017`  
		Last Modified: Thu, 03 Apr 2025 17:11:17 GMT  
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
$ docker pull rust@sha256:dea730db38a523c754db764c2dd5d7888c307a48e9167c0bc06ad83760fd45f5
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
$ docker pull rust@sha256:116ee24bc2bcf89ccd0df098b17cb62533758110249786fa82a4b7b4cfd52a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548923785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0223150941c1f151a39c1fd7b9fd2158d553757ca11184f3ce11742a5a8fabc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
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
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5503af74d5075005e8a2caef8b6b369ec49cf0d7a20dcdd1fe79d68aa4ba6c`  
		Last Modified: Mon, 17 Mar 2025 23:32:34 GMT  
		Size: 16.1 MB (16062045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfffc7337857c58b61734136d663ca328549ab864bf18f3217e50e3fdc25680`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 56.0 MB (56030008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df6c0e66903ef70af0189af240e3c0623f78105cc07d6d179e9ccce9fb96781`  
		Last Modified: Tue, 18 Mar 2025 01:13:46 GMT  
		Size: 200.0 MB (200008164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9a735890ea7b015e1d19036fb031bb7552e74a93669ffc6d2c4431b818edaf`  
		Last Modified: Thu, 03 Apr 2025 17:11:34 GMT  
		Size: 222.1 MB (222144951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fbe17c34b9c84ffc968b1b9436bd5edaed400e143670ab5871efcdd9738442cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657fe2fbe451682ec3fc344460a44690a5555b2ddc960f6e91042158e7561103`

```dockerfile
```

-	Layers:
	-	`sha256:b256b5471fa5852299fc7492e5cdaa7832b97e8339a236ee0ad6fb2ce0875f31`  
		Last Modified: Thu, 03 Apr 2025 17:11:29 GMT  
		Size: 15.1 MB (15060620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03b9746b8dc267ec4e985f761d56a8df08f701e18833adac3b4c9abec47544e6`  
		Last Modified: Thu, 03 Apr 2025 17:11:28 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86-slim`

```console
$ docker pull rust@sha256:c9eb52a5885c612df1f3a4d33d8eda6551f4e031d9f70bf256c57dbcafb19ee9
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
$ docker pull rust@sha256:c2e7a7d6f29a9d7719c23ae8fcc1b1bad94252e19a4b8678fa6b9c37b0f1f8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312986330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf20e8fec8e0685a3f37b4febd5ec1b5df88f18d8cb8d213d9f0a2d4321bcc2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58adefba86783bc364d159fc22200bb03f894cb3fca161ea999164bd44ad114d`  
		Last Modified: Thu, 03 Apr 2025 17:17:42 GMT  
		Size: 289.1 MB (289071242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim` - unknown; unknown

```console
$ docker pull rust@sha256:efd2bc156bf4e4d29cf4066eee24be0a001f33841f36b13b443826c3f02d78df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536f8535a55f26676330b86e7d8cb8f4b2423781ee98ac90299fe3386a609a55`

```dockerfile
```

-	Layers:
	-	`sha256:0bcdf3f2aa00ce635c14e89d996f190c9aa59ae13e3b841a044aa295f1ee744f`  
		Last Modified: Thu, 03 Apr 2025 17:17:37 GMT  
		Size: 3.8 MB (3771430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7711827842af2a4b96a035321719b385bc8e7af71a53448df511cf5620ceb857`  
		Last Modified: Thu, 03 Apr 2025 17:17:36 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d99100695f972ea286dd147b28dd807afe671305fcd23b732af09e6808ab3b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261520590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d1de1d75b59c3594376db14d4d6aeec6eef299828cbe62d1ea269ab3afcdf8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69376836448bc4f9d8087267845eb8a699215cd30a26ffc0f9e22328a7d0699a`  
		Last Modified: Thu, 03 Apr 2025 17:14:48 GMT  
		Size: 233.5 MB (233476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim` - unknown; unknown

```console
$ docker pull rust@sha256:219256112fd42e45fbe31c73c48eed36274b06ee2564f608d5289081c28148c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304a63c101c2d9ee8827a02afa441b85e07c948ea21ecc3e5fd70857c66e4407`

```dockerfile
```

-	Layers:
	-	`sha256:21b6701ecafeeeae919bd7fb4f80cc83179b8e068d1647ede4c9adafdf5c1969`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
		Size: 4.0 MB (3977710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc59da900c4e5aacd5f290abd628dfe6026decfc4c9b9d97907fd5f30f8c22c`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
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
$ docker pull rust@sha256:a36b873515c7a154cc0025f743c0c21fb528189308617b0ed15c95d2d6cc33af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367314762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d3c94ba741ffa44249470b54024e0579a7f703793216268961a2fcff5cfcb6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d695732d21c179c92e5836b87c86603c671891bd1f9b5abfc579f62d0f627`  
		Last Modified: Thu, 03 Apr 2025 17:15:13 GMT  
		Size: 335.3 MB (335266948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim` - unknown; unknown

```console
$ docker pull rust@sha256:948446e8b6cdcdaef62423f730bfcfe2313c426578b52224c3866fafd4a97143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ba7219b45ac300f7a30f8055cf30c92bf74219e5a60b59433412a5319a147e`

```dockerfile
```

-	Layers:
	-	`sha256:f6bde322ffc902cb55d8b885a30b59db1527dcf2175b7c7fedbd0308c67f514e`  
		Last Modified: Thu, 03 Apr 2025 17:15:05 GMT  
		Size: 3.9 MB (3927928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31607417122df605649579f7ee4f3d01be51ae3603b2177b716180a7d164449`  
		Last Modified: Thu, 03 Apr 2025 17:15:04 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim` - linux; s390x

```console
$ docker pull rust@sha256:fae104d7293dc4dec2b0bfa3d7c85b0ddb722b186b9dce3be618096ec50a0705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370871457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9c141f13ccee43ed7603ab4b606dd2115767f0d913925f999762c7118afc60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffe1d4aad8e16c34c41ca8abf6a12dabe09eae50a357ebef71e8afcd4d4e301`  
		Last Modified: Thu, 03 Apr 2025 17:14:22 GMT  
		Size: 344.0 MB (344010398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim` - unknown; unknown

```console
$ docker pull rust@sha256:32b19984f00d21884bb253746121346288d68655691691277e05040dc2978833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a108b23bf4af9c780bea0e00c4f8e83d12491c6df990fbfe1ace4c5478d26b37`

```dockerfile
```

-	Layers:
	-	`sha256:53fa0f0cc3073997feee47af9b8db8c47bb2fb3ed389e879e278b6aa4dd55c36`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 3.8 MB (3797267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40da86d43f0b95e47c685150107a93fcf90c5d099fb02fe0f6bc209188755c72`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86-slim-bookworm`

```console
$ docker pull rust@sha256:c9eb52a5885c612df1f3a4d33d8eda6551f4e031d9f70bf256c57dbcafb19ee9
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
$ docker pull rust@sha256:c2e7a7d6f29a9d7719c23ae8fcc1b1bad94252e19a4b8678fa6b9c37b0f1f8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312986330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf20e8fec8e0685a3f37b4febd5ec1b5df88f18d8cb8d213d9f0a2d4321bcc2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58adefba86783bc364d159fc22200bb03f894cb3fca161ea999164bd44ad114d`  
		Last Modified: Thu, 03 Apr 2025 17:17:42 GMT  
		Size: 289.1 MB (289071242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:efd2bc156bf4e4d29cf4066eee24be0a001f33841f36b13b443826c3f02d78df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536f8535a55f26676330b86e7d8cb8f4b2423781ee98ac90299fe3386a609a55`

```dockerfile
```

-	Layers:
	-	`sha256:0bcdf3f2aa00ce635c14e89d996f190c9aa59ae13e3b841a044aa295f1ee744f`  
		Last Modified: Thu, 03 Apr 2025 17:17:37 GMT  
		Size: 3.8 MB (3771430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7711827842af2a4b96a035321719b385bc8e7af71a53448df511cf5620ceb857`  
		Last Modified: Thu, 03 Apr 2025 17:17:36 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d99100695f972ea286dd147b28dd807afe671305fcd23b732af09e6808ab3b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261520590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d1de1d75b59c3594376db14d4d6aeec6eef299828cbe62d1ea269ab3afcdf8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69376836448bc4f9d8087267845eb8a699215cd30a26ffc0f9e22328a7d0699a`  
		Last Modified: Thu, 03 Apr 2025 17:14:48 GMT  
		Size: 233.5 MB (233476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:219256112fd42e45fbe31c73c48eed36274b06ee2564f608d5289081c28148c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304a63c101c2d9ee8827a02afa441b85e07c948ea21ecc3e5fd70857c66e4407`

```dockerfile
```

-	Layers:
	-	`sha256:21b6701ecafeeeae919bd7fb4f80cc83179b8e068d1647ede4c9adafdf5c1969`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
		Size: 4.0 MB (3977710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc59da900c4e5aacd5f290abd628dfe6026decfc4c9b9d97907fd5f30f8c22c`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
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
$ docker pull rust@sha256:a36b873515c7a154cc0025f743c0c21fb528189308617b0ed15c95d2d6cc33af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367314762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d3c94ba741ffa44249470b54024e0579a7f703793216268961a2fcff5cfcb6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d695732d21c179c92e5836b87c86603c671891bd1f9b5abfc579f62d0f627`  
		Last Modified: Thu, 03 Apr 2025 17:15:13 GMT  
		Size: 335.3 MB (335266948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:948446e8b6cdcdaef62423f730bfcfe2313c426578b52224c3866fafd4a97143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ba7219b45ac300f7a30f8055cf30c92bf74219e5a60b59433412a5319a147e`

```dockerfile
```

-	Layers:
	-	`sha256:f6bde322ffc902cb55d8b885a30b59db1527dcf2175b7c7fedbd0308c67f514e`  
		Last Modified: Thu, 03 Apr 2025 17:15:05 GMT  
		Size: 3.9 MB (3927928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31607417122df605649579f7ee4f3d01be51ae3603b2177b716180a7d164449`  
		Last Modified: Thu, 03 Apr 2025 17:15:04 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:fae104d7293dc4dec2b0bfa3d7c85b0ddb722b186b9dce3be618096ec50a0705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370871457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9c141f13ccee43ed7603ab4b606dd2115767f0d913925f999762c7118afc60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffe1d4aad8e16c34c41ca8abf6a12dabe09eae50a357ebef71e8afcd4d4e301`  
		Last Modified: Thu, 03 Apr 2025 17:14:22 GMT  
		Size: 344.0 MB (344010398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:32b19984f00d21884bb253746121346288d68655691691277e05040dc2978833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a108b23bf4af9c780bea0e00c4f8e83d12491c6df990fbfe1ace4c5478d26b37`

```dockerfile
```

-	Layers:
	-	`sha256:53fa0f0cc3073997feee47af9b8db8c47bb2fb3ed389e879e278b6aa4dd55c36`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 3.8 MB (3797267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40da86d43f0b95e47c685150107a93fcf90c5d099fb02fe0f6bc209188755c72`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86-slim-bullseye`

```console
$ docker pull rust@sha256:be137fabf963328d3ee0304496521dbbd3ca69af0fb8801155b5512c57e00515
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
$ docker pull rust@sha256:e325724019d0122003c69e3be4a0a71d6613243861e4187e34a215645256589b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308829763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c601a8eb2de08ddbfbd4cc187b317a74c571caa89f7071a5086014ce7e141708`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d05e5307839376198f22b171832782220d67b6bdd086664554ce6d987c7172c`  
		Last Modified: Thu, 03 Apr 2025 17:13:34 GMT  
		Size: 283.3 MB (283294419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:69cd421f2f4be3540bca681c6dd21edbff03203892c77ace8a7174106f2c987f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520975aebc7b52e9d2d354cf543a8572d8de9746b3395ae7d6c5e69cad573b2f`

```dockerfile
```

-	Layers:
	-	`sha256:822cb013a20cf21814005faafcf04e5465014d84ab49ec7ce7f62cae66c7c894`  
		Last Modified: Thu, 03 Apr 2025 17:13:27 GMT  
		Size: 4.0 MB (3982396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e9b343b1b2b9159f06c6a1b7c2d34bc589d5fface5d637c987212660eddcd54`  
		Last Modified: Thu, 03 Apr 2025 17:13:26 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7a54ab5c176dd6ba0d7b929683aaefa735929f71989029b48aadb23fb2d40642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251881734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f5359f1e436b09430003e77cc14e4e3968b4b24be4a6d8c4431af009ef81b7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507256b3d9772056115743145e266583385b05b43a68e8d3e732522c0c1487d0`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 223.1 MB (223135811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f3612ea27e656875b3165a0b1782de54ca3dc74e64437b08f3c564d0620382f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9424549dc96efa68ccf044bb50eafe08a3147ad572aa6d88b93306dd39dce40a`

```dockerfile
```

-	Layers:
	-	`sha256:7850f9163a23ca47e81c5a7f4b95ae374f2348f7edfc344e386d1ec95ef247cd`  
		Last Modified: Thu, 03 Apr 2025 17:12:06 GMT  
		Size: 4.2 MB (4169924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e57a8b24de7a434ab536b4cf649219fc6dbaba5df8160d56ffc0cc122ca254d`  
		Last Modified: Thu, 03 Apr 2025 17:12:06 GMT  
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
$ docker pull rust@sha256:249447250f1b9a75f5594a9e87f131622998cec0eb1477742cb29f8dfe933c47
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
$ docker pull rust@sha256:eb7e6764434a2bef33e68393177d061cc699d76fbc40f8d3301cd6ccac870c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572983715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb3ea8f24932f89b621228271fe3d9e453b1b3e20aea5e40e74f609521dee47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10bac27a676efda08e5b5aa398d8105182245c036138383494ad65da58e29e4`  
		Last Modified: Mon, 17 Mar 2025 23:32:45 GMT  
		Size: 24.8 MB (24846980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eb868ed69ff5115af5ee8fc248b3921cbc2936c23ef4556d264cc6842793cd`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 66.2 MB (66237259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e05e85a9740664efbffa28a6c9ab5ff6e64e564bd74dda762da2a13fc614b3`  
		Last Modified: Tue, 18 Mar 2025 01:13:58 GMT  
		Size: 210.3 MB (210299811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294695d0dacfa29cc31fb50ecfb4ca45feab85de0cb0d74bb46777640e160c61`  
		Last Modified: Thu, 03 Apr 2025 17:11:22 GMT  
		Size: 222.1 MB (222145185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0` - unknown; unknown

```console
$ docker pull rust@sha256:4231f06176670dffd20e1d8687ecf2849b8521991cf73360ebb69d9af9a03555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204ca13cabbb2b0c644990efefc2b83de967e2fca45fb4efffefe605f56089ad`

```dockerfile
```

-	Layers:
	-	`sha256:e2a240e2961c0c788f7ded3d2ecbb8bb5094202dafac8e1cbfabc2b529e5221d`  
		Last Modified: Thu, 03 Apr 2025 17:11:18 GMT  
		Size: 15.4 MB (15447217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f70ec62bd7b3025a317ef4637f2b9d2cbfc3eadb0478dc4fe063bf760720017`  
		Last Modified: Thu, 03 Apr 2025 17:11:17 GMT  
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
$ docker pull rust@sha256:249447250f1b9a75f5594a9e87f131622998cec0eb1477742cb29f8dfe933c47
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
$ docker pull rust@sha256:eb7e6764434a2bef33e68393177d061cc699d76fbc40f8d3301cd6ccac870c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572983715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb3ea8f24932f89b621228271fe3d9e453b1b3e20aea5e40e74f609521dee47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10bac27a676efda08e5b5aa398d8105182245c036138383494ad65da58e29e4`  
		Last Modified: Mon, 17 Mar 2025 23:32:45 GMT  
		Size: 24.8 MB (24846980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eb868ed69ff5115af5ee8fc248b3921cbc2936c23ef4556d264cc6842793cd`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 66.2 MB (66237259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e05e85a9740664efbffa28a6c9ab5ff6e64e564bd74dda762da2a13fc614b3`  
		Last Modified: Tue, 18 Mar 2025 01:13:58 GMT  
		Size: 210.3 MB (210299811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294695d0dacfa29cc31fb50ecfb4ca45feab85de0cb0d74bb46777640e160c61`  
		Last Modified: Thu, 03 Apr 2025 17:11:22 GMT  
		Size: 222.1 MB (222145185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4231f06176670dffd20e1d8687ecf2849b8521991cf73360ebb69d9af9a03555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204ca13cabbb2b0c644990efefc2b83de967e2fca45fb4efffefe605f56089ad`

```dockerfile
```

-	Layers:
	-	`sha256:e2a240e2961c0c788f7ded3d2ecbb8bb5094202dafac8e1cbfabc2b529e5221d`  
		Last Modified: Thu, 03 Apr 2025 17:11:18 GMT  
		Size: 15.4 MB (15447217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f70ec62bd7b3025a317ef4637f2b9d2cbfc3eadb0478dc4fe063bf760720017`  
		Last Modified: Thu, 03 Apr 2025 17:11:17 GMT  
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
$ docker pull rust@sha256:dea730db38a523c754db764c2dd5d7888c307a48e9167c0bc06ad83760fd45f5
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
$ docker pull rust@sha256:116ee24bc2bcf89ccd0df098b17cb62533758110249786fa82a4b7b4cfd52a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548923785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0223150941c1f151a39c1fd7b9fd2158d553757ca11184f3ce11742a5a8fabc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
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
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5503af74d5075005e8a2caef8b6b369ec49cf0d7a20dcdd1fe79d68aa4ba6c`  
		Last Modified: Mon, 17 Mar 2025 23:32:34 GMT  
		Size: 16.1 MB (16062045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfffc7337857c58b61734136d663ca328549ab864bf18f3217e50e3fdc25680`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 56.0 MB (56030008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df6c0e66903ef70af0189af240e3c0623f78105cc07d6d179e9ccce9fb96781`  
		Last Modified: Tue, 18 Mar 2025 01:13:46 GMT  
		Size: 200.0 MB (200008164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9a735890ea7b015e1d19036fb031bb7552e74a93669ffc6d2c4431b818edaf`  
		Last Modified: Thu, 03 Apr 2025 17:11:34 GMT  
		Size: 222.1 MB (222144951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fbe17c34b9c84ffc968b1b9436bd5edaed400e143670ab5871efcdd9738442cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657fe2fbe451682ec3fc344460a44690a5555b2ddc960f6e91042158e7561103`

```dockerfile
```

-	Layers:
	-	`sha256:b256b5471fa5852299fc7492e5cdaa7832b97e8339a236ee0ad6fb2ce0875f31`  
		Last Modified: Thu, 03 Apr 2025 17:11:29 GMT  
		Size: 15.1 MB (15060620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03b9746b8dc267ec4e985f761d56a8df08f701e18833adac3b4c9abec47544e6`  
		Last Modified: Thu, 03 Apr 2025 17:11:28 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0-slim`

```console
$ docker pull rust@sha256:c9eb52a5885c612df1f3a4d33d8eda6551f4e031d9f70bf256c57dbcafb19ee9
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
$ docker pull rust@sha256:c2e7a7d6f29a9d7719c23ae8fcc1b1bad94252e19a4b8678fa6b9c37b0f1f8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312986330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf20e8fec8e0685a3f37b4febd5ec1b5df88f18d8cb8d213d9f0a2d4321bcc2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58adefba86783bc364d159fc22200bb03f894cb3fca161ea999164bd44ad114d`  
		Last Modified: Thu, 03 Apr 2025 17:17:42 GMT  
		Size: 289.1 MB (289071242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:efd2bc156bf4e4d29cf4066eee24be0a001f33841f36b13b443826c3f02d78df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536f8535a55f26676330b86e7d8cb8f4b2423781ee98ac90299fe3386a609a55`

```dockerfile
```

-	Layers:
	-	`sha256:0bcdf3f2aa00ce635c14e89d996f190c9aa59ae13e3b841a044aa295f1ee744f`  
		Last Modified: Thu, 03 Apr 2025 17:17:37 GMT  
		Size: 3.8 MB (3771430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7711827842af2a4b96a035321719b385bc8e7af71a53448df511cf5620ceb857`  
		Last Modified: Thu, 03 Apr 2025 17:17:36 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d99100695f972ea286dd147b28dd807afe671305fcd23b732af09e6808ab3b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261520590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d1de1d75b59c3594376db14d4d6aeec6eef299828cbe62d1ea269ab3afcdf8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69376836448bc4f9d8087267845eb8a699215cd30a26ffc0f9e22328a7d0699a`  
		Last Modified: Thu, 03 Apr 2025 17:14:48 GMT  
		Size: 233.5 MB (233476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:219256112fd42e45fbe31c73c48eed36274b06ee2564f608d5289081c28148c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304a63c101c2d9ee8827a02afa441b85e07c948ea21ecc3e5fd70857c66e4407`

```dockerfile
```

-	Layers:
	-	`sha256:21b6701ecafeeeae919bd7fb4f80cc83179b8e068d1647ede4c9adafdf5c1969`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
		Size: 4.0 MB (3977710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc59da900c4e5aacd5f290abd628dfe6026decfc4c9b9d97907fd5f30f8c22c`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
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
$ docker pull rust@sha256:a36b873515c7a154cc0025f743c0c21fb528189308617b0ed15c95d2d6cc33af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367314762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d3c94ba741ffa44249470b54024e0579a7f703793216268961a2fcff5cfcb6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d695732d21c179c92e5836b87c86603c671891bd1f9b5abfc579f62d0f627`  
		Last Modified: Thu, 03 Apr 2025 17:15:13 GMT  
		Size: 335.3 MB (335266948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:948446e8b6cdcdaef62423f730bfcfe2313c426578b52224c3866fafd4a97143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ba7219b45ac300f7a30f8055cf30c92bf74219e5a60b59433412a5319a147e`

```dockerfile
```

-	Layers:
	-	`sha256:f6bde322ffc902cb55d8b885a30b59db1527dcf2175b7c7fedbd0308c67f514e`  
		Last Modified: Thu, 03 Apr 2025 17:15:05 GMT  
		Size: 3.9 MB (3927928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31607417122df605649579f7ee4f3d01be51ae3603b2177b716180a7d164449`  
		Last Modified: Thu, 03 Apr 2025 17:15:04 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim` - linux; s390x

```console
$ docker pull rust@sha256:fae104d7293dc4dec2b0bfa3d7c85b0ddb722b186b9dce3be618096ec50a0705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370871457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9c141f13ccee43ed7603ab4b606dd2115767f0d913925f999762c7118afc60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffe1d4aad8e16c34c41ca8abf6a12dabe09eae50a357ebef71e8afcd4d4e301`  
		Last Modified: Thu, 03 Apr 2025 17:14:22 GMT  
		Size: 344.0 MB (344010398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:32b19984f00d21884bb253746121346288d68655691691277e05040dc2978833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a108b23bf4af9c780bea0e00c4f8e83d12491c6df990fbfe1ace4c5478d26b37`

```dockerfile
```

-	Layers:
	-	`sha256:53fa0f0cc3073997feee47af9b8db8c47bb2fb3ed389e879e278b6aa4dd55c36`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 3.8 MB (3797267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40da86d43f0b95e47c685150107a93fcf90c5d099fb02fe0f6bc209188755c72`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0-slim-bookworm`

```console
$ docker pull rust@sha256:c9eb52a5885c612df1f3a4d33d8eda6551f4e031d9f70bf256c57dbcafb19ee9
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
$ docker pull rust@sha256:c2e7a7d6f29a9d7719c23ae8fcc1b1bad94252e19a4b8678fa6b9c37b0f1f8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312986330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf20e8fec8e0685a3f37b4febd5ec1b5df88f18d8cb8d213d9f0a2d4321bcc2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58adefba86783bc364d159fc22200bb03f894cb3fca161ea999164bd44ad114d`  
		Last Modified: Thu, 03 Apr 2025 17:17:42 GMT  
		Size: 289.1 MB (289071242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:efd2bc156bf4e4d29cf4066eee24be0a001f33841f36b13b443826c3f02d78df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536f8535a55f26676330b86e7d8cb8f4b2423781ee98ac90299fe3386a609a55`

```dockerfile
```

-	Layers:
	-	`sha256:0bcdf3f2aa00ce635c14e89d996f190c9aa59ae13e3b841a044aa295f1ee744f`  
		Last Modified: Thu, 03 Apr 2025 17:17:37 GMT  
		Size: 3.8 MB (3771430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7711827842af2a4b96a035321719b385bc8e7af71a53448df511cf5620ceb857`  
		Last Modified: Thu, 03 Apr 2025 17:17:36 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d99100695f972ea286dd147b28dd807afe671305fcd23b732af09e6808ab3b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261520590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d1de1d75b59c3594376db14d4d6aeec6eef299828cbe62d1ea269ab3afcdf8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69376836448bc4f9d8087267845eb8a699215cd30a26ffc0f9e22328a7d0699a`  
		Last Modified: Thu, 03 Apr 2025 17:14:48 GMT  
		Size: 233.5 MB (233476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:219256112fd42e45fbe31c73c48eed36274b06ee2564f608d5289081c28148c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304a63c101c2d9ee8827a02afa441b85e07c948ea21ecc3e5fd70857c66e4407`

```dockerfile
```

-	Layers:
	-	`sha256:21b6701ecafeeeae919bd7fb4f80cc83179b8e068d1647ede4c9adafdf5c1969`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
		Size: 4.0 MB (3977710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc59da900c4e5aacd5f290abd628dfe6026decfc4c9b9d97907fd5f30f8c22c`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
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
$ docker pull rust@sha256:a36b873515c7a154cc0025f743c0c21fb528189308617b0ed15c95d2d6cc33af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367314762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d3c94ba741ffa44249470b54024e0579a7f703793216268961a2fcff5cfcb6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d695732d21c179c92e5836b87c86603c671891bd1f9b5abfc579f62d0f627`  
		Last Modified: Thu, 03 Apr 2025 17:15:13 GMT  
		Size: 335.3 MB (335266948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:948446e8b6cdcdaef62423f730bfcfe2313c426578b52224c3866fafd4a97143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ba7219b45ac300f7a30f8055cf30c92bf74219e5a60b59433412a5319a147e`

```dockerfile
```

-	Layers:
	-	`sha256:f6bde322ffc902cb55d8b885a30b59db1527dcf2175b7c7fedbd0308c67f514e`  
		Last Modified: Thu, 03 Apr 2025 17:15:05 GMT  
		Size: 3.9 MB (3927928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31607417122df605649579f7ee4f3d01be51ae3603b2177b716180a7d164449`  
		Last Modified: Thu, 03 Apr 2025 17:15:04 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:fae104d7293dc4dec2b0bfa3d7c85b0ddb722b186b9dce3be618096ec50a0705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370871457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9c141f13ccee43ed7603ab4b606dd2115767f0d913925f999762c7118afc60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffe1d4aad8e16c34c41ca8abf6a12dabe09eae50a357ebef71e8afcd4d4e301`  
		Last Modified: Thu, 03 Apr 2025 17:14:22 GMT  
		Size: 344.0 MB (344010398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:32b19984f00d21884bb253746121346288d68655691691277e05040dc2978833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a108b23bf4af9c780bea0e00c4f8e83d12491c6df990fbfe1ace4c5478d26b37`

```dockerfile
```

-	Layers:
	-	`sha256:53fa0f0cc3073997feee47af9b8db8c47bb2fb3ed389e879e278b6aa4dd55c36`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 3.8 MB (3797267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40da86d43f0b95e47c685150107a93fcf90c5d099fb02fe0f6bc209188755c72`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0-slim-bullseye`

```console
$ docker pull rust@sha256:be137fabf963328d3ee0304496521dbbd3ca69af0fb8801155b5512c57e00515
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
$ docker pull rust@sha256:e325724019d0122003c69e3be4a0a71d6613243861e4187e34a215645256589b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308829763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c601a8eb2de08ddbfbd4cc187b317a74c571caa89f7071a5086014ce7e141708`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d05e5307839376198f22b171832782220d67b6bdd086664554ce6d987c7172c`  
		Last Modified: Thu, 03 Apr 2025 17:13:34 GMT  
		Size: 283.3 MB (283294419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:69cd421f2f4be3540bca681c6dd21edbff03203892c77ace8a7174106f2c987f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520975aebc7b52e9d2d354cf543a8572d8de9746b3395ae7d6c5e69cad573b2f`

```dockerfile
```

-	Layers:
	-	`sha256:822cb013a20cf21814005faafcf04e5465014d84ab49ec7ce7f62cae66c7c894`  
		Last Modified: Thu, 03 Apr 2025 17:13:27 GMT  
		Size: 4.0 MB (3982396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e9b343b1b2b9159f06c6a1b7c2d34bc589d5fface5d637c987212660eddcd54`  
		Last Modified: Thu, 03 Apr 2025 17:13:26 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7a54ab5c176dd6ba0d7b929683aaefa735929f71989029b48aadb23fb2d40642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251881734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f5359f1e436b09430003e77cc14e4e3968b4b24be4a6d8c4431af009ef81b7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507256b3d9772056115743145e266583385b05b43a68e8d3e732522c0c1487d0`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 223.1 MB (223135811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f3612ea27e656875b3165a0b1782de54ca3dc74e64437b08f3c564d0620382f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9424549dc96efa68ccf044bb50eafe08a3147ad572aa6d88b93306dd39dce40a`

```dockerfile
```

-	Layers:
	-	`sha256:7850f9163a23ca47e81c5a7f4b95ae374f2348f7edfc344e386d1ec95ef247cd`  
		Last Modified: Thu, 03 Apr 2025 17:12:06 GMT  
		Size: 4.2 MB (4169924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e57a8b24de7a434ab536b4cf649219fc6dbaba5df8160d56ffc0cc122ca254d`  
		Last Modified: Thu, 03 Apr 2025 17:12:06 GMT  
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
$ docker pull rust@sha256:249447250f1b9a75f5594a9e87f131622998cec0eb1477742cb29f8dfe933c47
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
$ docker pull rust@sha256:eb7e6764434a2bef33e68393177d061cc699d76fbc40f8d3301cd6ccac870c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572983715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb3ea8f24932f89b621228271fe3d9e453b1b3e20aea5e40e74f609521dee47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10bac27a676efda08e5b5aa398d8105182245c036138383494ad65da58e29e4`  
		Last Modified: Mon, 17 Mar 2025 23:32:45 GMT  
		Size: 24.8 MB (24846980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eb868ed69ff5115af5ee8fc248b3921cbc2936c23ef4556d264cc6842793cd`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 66.2 MB (66237259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e05e85a9740664efbffa28a6c9ab5ff6e64e564bd74dda762da2a13fc614b3`  
		Last Modified: Tue, 18 Mar 2025 01:13:58 GMT  
		Size: 210.3 MB (210299811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294695d0dacfa29cc31fb50ecfb4ca45feab85de0cb0d74bb46777640e160c61`  
		Last Modified: Thu, 03 Apr 2025 17:11:22 GMT  
		Size: 222.1 MB (222145185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4231f06176670dffd20e1d8687ecf2849b8521991cf73360ebb69d9af9a03555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204ca13cabbb2b0c644990efefc2b83de967e2fca45fb4efffefe605f56089ad`

```dockerfile
```

-	Layers:
	-	`sha256:e2a240e2961c0c788f7ded3d2ecbb8bb5094202dafac8e1cbfabc2b529e5221d`  
		Last Modified: Thu, 03 Apr 2025 17:11:18 GMT  
		Size: 15.4 MB (15447217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f70ec62bd7b3025a317ef4637f2b9d2cbfc3eadb0478dc4fe063bf760720017`  
		Last Modified: Thu, 03 Apr 2025 17:11:17 GMT  
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
$ docker pull rust@sha256:dea730db38a523c754db764c2dd5d7888c307a48e9167c0bc06ad83760fd45f5
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
$ docker pull rust@sha256:116ee24bc2bcf89ccd0df098b17cb62533758110249786fa82a4b7b4cfd52a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548923785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0223150941c1f151a39c1fd7b9fd2158d553757ca11184f3ce11742a5a8fabc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
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
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5503af74d5075005e8a2caef8b6b369ec49cf0d7a20dcdd1fe79d68aa4ba6c`  
		Last Modified: Mon, 17 Mar 2025 23:32:34 GMT  
		Size: 16.1 MB (16062045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfffc7337857c58b61734136d663ca328549ab864bf18f3217e50e3fdc25680`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 56.0 MB (56030008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df6c0e66903ef70af0189af240e3c0623f78105cc07d6d179e9ccce9fb96781`  
		Last Modified: Tue, 18 Mar 2025 01:13:46 GMT  
		Size: 200.0 MB (200008164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9a735890ea7b015e1d19036fb031bb7552e74a93669ffc6d2c4431b818edaf`  
		Last Modified: Thu, 03 Apr 2025 17:11:34 GMT  
		Size: 222.1 MB (222144951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:fbe17c34b9c84ffc968b1b9436bd5edaed400e143670ab5871efcdd9738442cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15071837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657fe2fbe451682ec3fc344460a44690a5555b2ddc960f6e91042158e7561103`

```dockerfile
```

-	Layers:
	-	`sha256:b256b5471fa5852299fc7492e5cdaa7832b97e8339a236ee0ad6fb2ce0875f31`  
		Last Modified: Thu, 03 Apr 2025 17:11:29 GMT  
		Size: 15.1 MB (15060620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03b9746b8dc267ec4e985f761d56a8df08f701e18833adac3b4c9abec47544e6`  
		Last Modified: Thu, 03 Apr 2025 17:11:28 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:249447250f1b9a75f5594a9e87f131622998cec0eb1477742cb29f8dfe933c47
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
$ docker pull rust@sha256:eb7e6764434a2bef33e68393177d061cc699d76fbc40f8d3301cd6ccac870c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572983715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb3ea8f24932f89b621228271fe3d9e453b1b3e20aea5e40e74f609521dee47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10bac27a676efda08e5b5aa398d8105182245c036138383494ad65da58e29e4`  
		Last Modified: Mon, 17 Mar 2025 23:32:45 GMT  
		Size: 24.8 MB (24846980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eb868ed69ff5115af5ee8fc248b3921cbc2936c23ef4556d264cc6842793cd`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 66.2 MB (66237259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e05e85a9740664efbffa28a6c9ab5ff6e64e564bd74dda762da2a13fc614b3`  
		Last Modified: Tue, 18 Mar 2025 01:13:58 GMT  
		Size: 210.3 MB (210299811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294695d0dacfa29cc31fb50ecfb4ca45feab85de0cb0d74bb46777640e160c61`  
		Last Modified: Thu, 03 Apr 2025 17:11:22 GMT  
		Size: 222.1 MB (222145185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:4231f06176670dffd20e1d8687ecf2849b8521991cf73360ebb69d9af9a03555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204ca13cabbb2b0c644990efefc2b83de967e2fca45fb4efffefe605f56089ad`

```dockerfile
```

-	Layers:
	-	`sha256:e2a240e2961c0c788f7ded3d2ecbb8bb5094202dafac8e1cbfabc2b529e5221d`  
		Last Modified: Thu, 03 Apr 2025 17:11:18 GMT  
		Size: 15.4 MB (15447217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f70ec62bd7b3025a317ef4637f2b9d2cbfc3eadb0478dc4fe063bf760720017`  
		Last Modified: Thu, 03 Apr 2025 17:11:17 GMT  
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
$ docker pull rust@sha256:c9eb52a5885c612df1f3a4d33d8eda6551f4e031d9f70bf256c57dbcafb19ee9
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
$ docker pull rust@sha256:c2e7a7d6f29a9d7719c23ae8fcc1b1bad94252e19a4b8678fa6b9c37b0f1f8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312986330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf20e8fec8e0685a3f37b4febd5ec1b5df88f18d8cb8d213d9f0a2d4321bcc2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58adefba86783bc364d159fc22200bb03f894cb3fca161ea999164bd44ad114d`  
		Last Modified: Thu, 03 Apr 2025 17:17:42 GMT  
		Size: 289.1 MB (289071242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:efd2bc156bf4e4d29cf4066eee24be0a001f33841f36b13b443826c3f02d78df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536f8535a55f26676330b86e7d8cb8f4b2423781ee98ac90299fe3386a609a55`

```dockerfile
```

-	Layers:
	-	`sha256:0bcdf3f2aa00ce635c14e89d996f190c9aa59ae13e3b841a044aa295f1ee744f`  
		Last Modified: Thu, 03 Apr 2025 17:17:37 GMT  
		Size: 3.8 MB (3771430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7711827842af2a4b96a035321719b385bc8e7af71a53448df511cf5620ceb857`  
		Last Modified: Thu, 03 Apr 2025 17:17:36 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d99100695f972ea286dd147b28dd807afe671305fcd23b732af09e6808ab3b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261520590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d1de1d75b59c3594376db14d4d6aeec6eef299828cbe62d1ea269ab3afcdf8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69376836448bc4f9d8087267845eb8a699215cd30a26ffc0f9e22328a7d0699a`  
		Last Modified: Thu, 03 Apr 2025 17:14:48 GMT  
		Size: 233.5 MB (233476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:219256112fd42e45fbe31c73c48eed36274b06ee2564f608d5289081c28148c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304a63c101c2d9ee8827a02afa441b85e07c948ea21ecc3e5fd70857c66e4407`

```dockerfile
```

-	Layers:
	-	`sha256:21b6701ecafeeeae919bd7fb4f80cc83179b8e068d1647ede4c9adafdf5c1969`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
		Size: 4.0 MB (3977710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc59da900c4e5aacd5f290abd628dfe6026decfc4c9b9d97907fd5f30f8c22c`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
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
$ docker pull rust@sha256:a36b873515c7a154cc0025f743c0c21fb528189308617b0ed15c95d2d6cc33af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367314762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d3c94ba741ffa44249470b54024e0579a7f703793216268961a2fcff5cfcb6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d695732d21c179c92e5836b87c86603c671891bd1f9b5abfc579f62d0f627`  
		Last Modified: Thu, 03 Apr 2025 17:15:13 GMT  
		Size: 335.3 MB (335266948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:948446e8b6cdcdaef62423f730bfcfe2313c426578b52224c3866fafd4a97143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ba7219b45ac300f7a30f8055cf30c92bf74219e5a60b59433412a5319a147e`

```dockerfile
```

-	Layers:
	-	`sha256:f6bde322ffc902cb55d8b885a30b59db1527dcf2175b7c7fedbd0308c67f514e`  
		Last Modified: Thu, 03 Apr 2025 17:15:05 GMT  
		Size: 3.9 MB (3927928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31607417122df605649579f7ee4f3d01be51ae3603b2177b716180a7d164449`  
		Last Modified: Thu, 03 Apr 2025 17:15:04 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:fae104d7293dc4dec2b0bfa3d7c85b0ddb722b186b9dce3be618096ec50a0705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370871457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9c141f13ccee43ed7603ab4b606dd2115767f0d913925f999762c7118afc60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffe1d4aad8e16c34c41ca8abf6a12dabe09eae50a357ebef71e8afcd4d4e301`  
		Last Modified: Thu, 03 Apr 2025 17:14:22 GMT  
		Size: 344.0 MB (344010398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:32b19984f00d21884bb253746121346288d68655691691277e05040dc2978833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a108b23bf4af9c780bea0e00c4f8e83d12491c6df990fbfe1ace4c5478d26b37`

```dockerfile
```

-	Layers:
	-	`sha256:53fa0f0cc3073997feee47af9b8db8c47bb2fb3ed389e879e278b6aa4dd55c36`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 3.8 MB (3797267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40da86d43f0b95e47c685150107a93fcf90c5d099fb02fe0f6bc209188755c72`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:c9eb52a5885c612df1f3a4d33d8eda6551f4e031d9f70bf256c57dbcafb19ee9
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
$ docker pull rust@sha256:c2e7a7d6f29a9d7719c23ae8fcc1b1bad94252e19a4b8678fa6b9c37b0f1f8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312986330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf20e8fec8e0685a3f37b4febd5ec1b5df88f18d8cb8d213d9f0a2d4321bcc2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58adefba86783bc364d159fc22200bb03f894cb3fca161ea999164bd44ad114d`  
		Last Modified: Thu, 03 Apr 2025 17:17:42 GMT  
		Size: 289.1 MB (289071242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:efd2bc156bf4e4d29cf4066eee24be0a001f33841f36b13b443826c3f02d78df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536f8535a55f26676330b86e7d8cb8f4b2423781ee98ac90299fe3386a609a55`

```dockerfile
```

-	Layers:
	-	`sha256:0bcdf3f2aa00ce635c14e89d996f190c9aa59ae13e3b841a044aa295f1ee744f`  
		Last Modified: Thu, 03 Apr 2025 17:17:37 GMT  
		Size: 3.8 MB (3771430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7711827842af2a4b96a035321719b385bc8e7af71a53448df511cf5620ceb857`  
		Last Modified: Thu, 03 Apr 2025 17:17:36 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d99100695f972ea286dd147b28dd807afe671305fcd23b732af09e6808ab3b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261520590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d1de1d75b59c3594376db14d4d6aeec6eef299828cbe62d1ea269ab3afcdf8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69376836448bc4f9d8087267845eb8a699215cd30a26ffc0f9e22328a7d0699a`  
		Last Modified: Thu, 03 Apr 2025 17:14:48 GMT  
		Size: 233.5 MB (233476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:219256112fd42e45fbe31c73c48eed36274b06ee2564f608d5289081c28148c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304a63c101c2d9ee8827a02afa441b85e07c948ea21ecc3e5fd70857c66e4407`

```dockerfile
```

-	Layers:
	-	`sha256:21b6701ecafeeeae919bd7fb4f80cc83179b8e068d1647ede4c9adafdf5c1969`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
		Size: 4.0 MB (3977710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc59da900c4e5aacd5f290abd628dfe6026decfc4c9b9d97907fd5f30f8c22c`  
		Last Modified: Thu, 03 Apr 2025 17:14:41 GMT  
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
$ docker pull rust@sha256:a36b873515c7a154cc0025f743c0c21fb528189308617b0ed15c95d2d6cc33af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367314762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d3c94ba741ffa44249470b54024e0579a7f703793216268961a2fcff5cfcb6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d695732d21c179c92e5836b87c86603c671891bd1f9b5abfc579f62d0f627`  
		Last Modified: Thu, 03 Apr 2025 17:15:13 GMT  
		Size: 335.3 MB (335266948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:948446e8b6cdcdaef62423f730bfcfe2313c426578b52224c3866fafd4a97143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ba7219b45ac300f7a30f8055cf30c92bf74219e5a60b59433412a5319a147e`

```dockerfile
```

-	Layers:
	-	`sha256:f6bde322ffc902cb55d8b885a30b59db1527dcf2175b7c7fedbd0308c67f514e`  
		Last Modified: Thu, 03 Apr 2025 17:15:05 GMT  
		Size: 3.9 MB (3927928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31607417122df605649579f7ee4f3d01be51ae3603b2177b716180a7d164449`  
		Last Modified: Thu, 03 Apr 2025 17:15:04 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:fae104d7293dc4dec2b0bfa3d7c85b0ddb722b186b9dce3be618096ec50a0705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370871457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9c141f13ccee43ed7603ab4b606dd2115767f0d913925f999762c7118afc60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffe1d4aad8e16c34c41ca8abf6a12dabe09eae50a357ebef71e8afcd4d4e301`  
		Last Modified: Thu, 03 Apr 2025 17:14:22 GMT  
		Size: 344.0 MB (344010398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:32b19984f00d21884bb253746121346288d68655691691277e05040dc2978833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a108b23bf4af9c780bea0e00c4f8e83d12491c6df990fbfe1ace4c5478d26b37`

```dockerfile
```

-	Layers:
	-	`sha256:53fa0f0cc3073997feee47af9b8db8c47bb2fb3ed389e879e278b6aa4dd55c36`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 3.8 MB (3797267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40da86d43f0b95e47c685150107a93fcf90c5d099fb02fe0f6bc209188755c72`  
		Last Modified: Thu, 03 Apr 2025 17:14:15 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:be137fabf963328d3ee0304496521dbbd3ca69af0fb8801155b5512c57e00515
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
$ docker pull rust@sha256:e325724019d0122003c69e3be4a0a71d6613243861e4187e34a215645256589b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308829763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c601a8eb2de08ddbfbd4cc187b317a74c571caa89f7071a5086014ce7e141708`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d05e5307839376198f22b171832782220d67b6bdd086664554ce6d987c7172c`  
		Last Modified: Thu, 03 Apr 2025 17:13:34 GMT  
		Size: 283.3 MB (283294419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:69cd421f2f4be3540bca681c6dd21edbff03203892c77ace8a7174106f2c987f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3993828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520975aebc7b52e9d2d354cf543a8572d8de9746b3395ae7d6c5e69cad573b2f`

```dockerfile
```

-	Layers:
	-	`sha256:822cb013a20cf21814005faafcf04e5465014d84ab49ec7ce7f62cae66c7c894`  
		Last Modified: Thu, 03 Apr 2025 17:13:27 GMT  
		Size: 4.0 MB (3982396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e9b343b1b2b9159f06c6a1b7c2d34bc589d5fface5d637c987212660eddcd54`  
		Last Modified: Thu, 03 Apr 2025 17:13:26 GMT  
		Size: 11.4 KB (11432 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7a54ab5c176dd6ba0d7b929683aaefa735929f71989029b48aadb23fb2d40642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251881734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f5359f1e436b09430003e77cc14e4e3968b4b24be4a6d8c4431af009ef81b7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507256b3d9772056115743145e266583385b05b43a68e8d3e732522c0c1487d0`  
		Last Modified: Thu, 03 Apr 2025 17:12:14 GMT  
		Size: 223.1 MB (223135811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f3612ea27e656875b3165a0b1782de54ca3dc74e64437b08f3c564d0620382f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4181384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9424549dc96efa68ccf044bb50eafe08a3147ad572aa6d88b93306dd39dce40a`

```dockerfile
```

-	Layers:
	-	`sha256:7850f9163a23ca47e81c5a7f4b95ae374f2348f7edfc344e386d1ec95ef247cd`  
		Last Modified: Thu, 03 Apr 2025 17:12:06 GMT  
		Size: 4.2 MB (4169924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e57a8b24de7a434ab536b4cf649219fc6dbaba5df8160d56ffc0cc122ca254d`  
		Last Modified: Thu, 03 Apr 2025 17:12:06 GMT  
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
