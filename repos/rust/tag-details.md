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
$ docker pull rust@sha256:ff735b1f09be7bb43d0ceece3d6f03b877292ae0307e35b32f75165a05d574c5
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
$ docker pull rust@sha256:f163d1a53e6d105d037f8798f47f7947c062671bfb8d4485c612a1d00a3cbf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547098954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209b88fdf20bcc777094ee4ff43efc6ef043406c3a4c169785eda17fecc6318c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187b51b626e1d60ab369727b81f440adea9d45e97a45e137fc318be0bb7f09f`  
		Last Modified: Mon, 28 Apr 2025 23:12:20 GMT  
		Size: 211.4 MB (211356050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa897cd1d909c6f9aeeb2eb86f8281d7f1bd22ec60b937531af70f77e3b8c978`  
		Last Modified: Tue, 29 Apr 2025 00:20:42 GMT  
		Size: 198.8 MB (198846097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:c28aff946bf6a9641ea9333906292d4bcaca20d9730ac06f65c73b7dbfe00bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91b52445b0f0d88b77d2754a8b302421f4d6c97b7cb7d4de220050178066182`

```dockerfile
```

-	Layers:
	-	`sha256:b79e6f075844c12dfa724e6e05d0844d5de320465830dbb322f023f18d80c8fc`  
		Last Modified: Tue, 29 Apr 2025 00:20:37 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49427446706d8a35b3d9da8f7db167c3935e0225c64c41163ace92f38a50fb6`  
		Last Modified: Tue, 29 Apr 2025 00:20:36 GMT  
		Size: 13.1 KB (13137 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff3403ae6581adf67c0bbde3bcab29a147bf80f4392ab0af5dbed3377c1e119b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542266054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3698017437d2ae8077abed8488d38727dc5dba1f88e48876e5d3733f532a6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5414268749270f000845caf5689fb7740534b9fe922712301ba571a6afca96`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 59.6 MB (59639425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd5426bd57bea2caac0e0e87b98c0988fb39decb07637e76311bc28b01e6b7`  
		Last Modified: Tue, 08 Apr 2025 20:34:20 GMT  
		Size: 175.3 MB (175297229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093acd39fc465167a3795c75afa1eb7603459d1e396309304795a5c261b5a699`  
		Last Modified: Wed, 09 Apr 2025 03:31:38 GMT  
		Size: 241.2 MB (241214386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:965b9904c21bcd441911c4b25119ecca1e3f2fba0c3ab636faf4e528fc89a355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15289059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ac2dfec33d3f464c032fb6c8ec95b36285cdc7aca6e1012458969150a6d286`

```dockerfile
```

-	Layers:
	-	`sha256:69935c7f7900e361aabe717ea482ce229c0f4290d1f011ce1e508dba7b96a093`  
		Last Modified: Wed, 09 Apr 2025 03:31:32 GMT  
		Size: 15.3 MB (15275812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd85c681d8a8c03f05a9c034397cd1615a023bca10a054649801c9a54062374`  
		Last Modified: Wed, 09 Apr 2025 03:31:31 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0a27f7509b3def95327fe3735084c6a475bb52054efee7316d84fd91fc17736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506611045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee291f151e5b030a604f543d9a5c4541b96d0e637888a2a09334bd826322ab1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002e18bd5659ca9d155e99922678788bec836a3ac4964d8a9567ce59e2154de9`  
		Last Modified: Tue, 08 Apr 2025 15:52:42 GMT  
		Size: 202.7 MB (202735307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775439c6d731e711d1e42014fd69218e477c0c43221098e6d1513428f9946240`  
		Last Modified: Tue, 08 Apr 2025 21:32:10 GMT  
		Size: 167.6 MB (167648150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:63403d5c50b5086ee37972bd4ddb3dac08ba9444f59ed275e4639aa2c44c5c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e9f0697f2a2efe50253e36a3bc474bac40598a69515a99e7596cbf41d4c034`

```dockerfile
```

-	Layers:
	-	`sha256:2af08bf3572f4cd46f60afd036e4b1bf91b775e6c09a6bf6295ec9afbec238bf`  
		Last Modified: Tue, 08 Apr 2025 21:32:07 GMT  
		Size: 15.5 MB (15499945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32389045ed63fed52cb8d7ec269d8b4a0e5421639eb6f7906eba095d4d5d1e64`  
		Last Modified: Tue, 08 Apr 2025 21:32:06 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:69531fcb8a67b072bfc78f893d76a5d5c5a325536a4f948493f5fae1756d4019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572991948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f4ce1664011b7b08cabc2bcb040af4431dd6da7fff8a55460b8c4e9fd01a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Mon, 28 Apr 2025 21:53:42 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce8929d56fab56325a8eea211cb4cd1021bc6ffc1e7a794d505ddbe638b23cd`  
		Last Modified: Mon, 28 Apr 2025 22:15:00 GMT  
		Size: 66.2 MB (66228922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1528cc13747bb103866d00332de43f9304156fef5a2f396b15d9e173b1365f5`  
		Last Modified: Mon, 28 Apr 2025 23:13:00 GMT  
		Size: 210.3 MB (210293092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a0a0e26e85220e6482bcf2859ccd19dc889d8c6237381e13a52446ce56f374`  
		Last Modified: Tue, 29 Apr 2025 00:19:10 GMT  
		Size: 222.1 MB (222144215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:e26a24e515fc29bea5fb4ad97d93055e97736137dbbff6c0a66d1e3cb662a266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2a0d93c03f13377ffa686d882edf0901118adbaeea959c691a9dc76256ea5b`

```dockerfile
```

-	Layers:
	-	`sha256:38affa8290df1776c35aab78bc46e1491c5b3a525152f3b1e737e46e6456d55e`  
		Last Modified: Tue, 29 Apr 2025 00:19:06 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04d9a14a26e0b8792115fbad3c25692abd8c3ea50dc544ff6954cc8a9d3b12ab`  
		Last Modified: Tue, 29 Apr 2025 00:19:05 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:6ff43004246ac7409ecbc3cf1d1f64fe97af549cff6e4eeffb347c53123695c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628715675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52ec6298460494f48ebd94562ccdc697dcc3bb3d3915515c744d5def51728ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675af5e5720aa9e9d4f74b056a7b58aa0a84a5b3cc2c23272c361e473b9c5b8`  
		Last Modified: Tue, 08 Apr 2025 15:34:04 GMT  
		Size: 214.4 MB (214387209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fd4fb10062d551eeb2e024d3e563728a42549e867f8f166eb7d3c22b7d6b78`  
		Last Modified: Tue, 08 Apr 2025 19:25:14 GMT  
		Size: 266.5 MB (266502721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:c47a89a1025ff4dbb33264cf2765a8e1e0c24ff47135d1b6c7c7e977468d89e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15459677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7827834152d2d52c8fbc16a215bf024a151d424dffb4ab149188341b0cc1f14`

```dockerfile
```

-	Layers:
	-	`sha256:23ddb56e82f0fa073703d355e296183384c1fc63c0b493b2a1bac0b20c353294`  
		Last Modified: Tue, 08 Apr 2025 19:25:07 GMT  
		Size: 15.4 MB (15446470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfcaa31a08c5def654ca430c6b47811b40f07fd5cbdfd2e94e2fb98d08e77e8`  
		Last Modified: Tue, 08 Apr 2025 19:25:06 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:aaf804c60805de2a84400664811dd543e7a735e684976c5b4ac22ea1ae537910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611949825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f71016804f1861e6054a214aea01f56260a9f54e32cde4b102889b5ba38c3b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fde99ce0eec506f038695c59ba0ff56bd0df358636c0b067f55c60d7d566c`  
		Last Modified: Tue, 08 Apr 2025 06:52:25 GMT  
		Size: 63.5 MB (63498375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766d2c4791b14ffb813f2bd4d87d95e9030a5939b65f31722bc2c223f845ecf8`  
		Last Modified: Tue, 08 Apr 2025 10:02:09 GMT  
		Size: 183.4 MB (183388438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eb0c69619b19f87369d4a1737b46098625d76f72f75d41c18ecc2b9f8019cc`  
		Last Modified: Tue, 08 Apr 2025 18:17:17 GMT  
		Size: 293.9 MB (293903680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:21d031f77b8b2c841a56916b430442b3dbbfd340d1aadee3bf1561f97999cc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15297196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49e7c039c53b210b5e3cfc85ca1eb9fcaa5480271c4f2b0c5e5e6aa37781915`

```dockerfile
```

-	Layers:
	-	`sha256:0d2bad61871ee6c24e5ae84182871a58c88b6f3593a3f0a381f6236eec0606e9`  
		Last Modified: Tue, 08 Apr 2025 18:17:08 GMT  
		Size: 15.3 MB (15284058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1589d850c8b322cdebed632bcf0d29ee300ca793b83044f540479e4b39431e1`  
		Last Modified: Tue, 08 Apr 2025 18:17:07 GMT  
		Size: 13.1 KB (13138 bytes)  
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
$ docker pull rust@sha256:ff735b1f09be7bb43d0ceece3d6f03b877292ae0307e35b32f75165a05d574c5
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
$ docker pull rust@sha256:f163d1a53e6d105d037f8798f47f7947c062671bfb8d4485c612a1d00a3cbf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547098954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209b88fdf20bcc777094ee4ff43efc6ef043406c3a4c169785eda17fecc6318c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187b51b626e1d60ab369727b81f440adea9d45e97a45e137fc318be0bb7f09f`  
		Last Modified: Mon, 28 Apr 2025 23:12:20 GMT  
		Size: 211.4 MB (211356050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa897cd1d909c6f9aeeb2eb86f8281d7f1bd22ec60b937531af70f77e3b8c978`  
		Last Modified: Tue, 29 Apr 2025 00:20:42 GMT  
		Size: 198.8 MB (198846097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c28aff946bf6a9641ea9333906292d4bcaca20d9730ac06f65c73b7dbfe00bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91b52445b0f0d88b77d2754a8b302421f4d6c97b7cb7d4de220050178066182`

```dockerfile
```

-	Layers:
	-	`sha256:b79e6f075844c12dfa724e6e05d0844d5de320465830dbb322f023f18d80c8fc`  
		Last Modified: Tue, 29 Apr 2025 00:20:37 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49427446706d8a35b3d9da8f7db167c3935e0225c64c41163ace92f38a50fb6`  
		Last Modified: Tue, 29 Apr 2025 00:20:36 GMT  
		Size: 13.1 KB (13137 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff3403ae6581adf67c0bbde3bcab29a147bf80f4392ab0af5dbed3377c1e119b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542266054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3698017437d2ae8077abed8488d38727dc5dba1f88e48876e5d3733f532a6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5414268749270f000845caf5689fb7740534b9fe922712301ba571a6afca96`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 59.6 MB (59639425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd5426bd57bea2caac0e0e87b98c0988fb39decb07637e76311bc28b01e6b7`  
		Last Modified: Tue, 08 Apr 2025 20:34:20 GMT  
		Size: 175.3 MB (175297229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093acd39fc465167a3795c75afa1eb7603459d1e396309304795a5c261b5a699`  
		Last Modified: Wed, 09 Apr 2025 03:31:38 GMT  
		Size: 241.2 MB (241214386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:965b9904c21bcd441911c4b25119ecca1e3f2fba0c3ab636faf4e528fc89a355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15289059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ac2dfec33d3f464c032fb6c8ec95b36285cdc7aca6e1012458969150a6d286`

```dockerfile
```

-	Layers:
	-	`sha256:69935c7f7900e361aabe717ea482ce229c0f4290d1f011ce1e508dba7b96a093`  
		Last Modified: Wed, 09 Apr 2025 03:31:32 GMT  
		Size: 15.3 MB (15275812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd85c681d8a8c03f05a9c034397cd1615a023bca10a054649801c9a54062374`  
		Last Modified: Wed, 09 Apr 2025 03:31:31 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0a27f7509b3def95327fe3735084c6a475bb52054efee7316d84fd91fc17736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506611045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee291f151e5b030a604f543d9a5c4541b96d0e637888a2a09334bd826322ab1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002e18bd5659ca9d155e99922678788bec836a3ac4964d8a9567ce59e2154de9`  
		Last Modified: Tue, 08 Apr 2025 15:52:42 GMT  
		Size: 202.7 MB (202735307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775439c6d731e711d1e42014fd69218e477c0c43221098e6d1513428f9946240`  
		Last Modified: Tue, 08 Apr 2025 21:32:10 GMT  
		Size: 167.6 MB (167648150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:63403d5c50b5086ee37972bd4ddb3dac08ba9444f59ed275e4639aa2c44c5c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e9f0697f2a2efe50253e36a3bc474bac40598a69515a99e7596cbf41d4c034`

```dockerfile
```

-	Layers:
	-	`sha256:2af08bf3572f4cd46f60afd036e4b1bf91b775e6c09a6bf6295ec9afbec238bf`  
		Last Modified: Tue, 08 Apr 2025 21:32:07 GMT  
		Size: 15.5 MB (15499945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32389045ed63fed52cb8d7ec269d8b4a0e5421639eb6f7906eba095d4d5d1e64`  
		Last Modified: Tue, 08 Apr 2025 21:32:06 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:69531fcb8a67b072bfc78f893d76a5d5c5a325536a4f948493f5fae1756d4019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572991948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f4ce1664011b7b08cabc2bcb040af4431dd6da7fff8a55460b8c4e9fd01a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Mon, 28 Apr 2025 21:53:42 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce8929d56fab56325a8eea211cb4cd1021bc6ffc1e7a794d505ddbe638b23cd`  
		Last Modified: Mon, 28 Apr 2025 22:15:00 GMT  
		Size: 66.2 MB (66228922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1528cc13747bb103866d00332de43f9304156fef5a2f396b15d9e173b1365f5`  
		Last Modified: Mon, 28 Apr 2025 23:13:00 GMT  
		Size: 210.3 MB (210293092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a0a0e26e85220e6482bcf2859ccd19dc889d8c6237381e13a52446ce56f374`  
		Last Modified: Tue, 29 Apr 2025 00:19:10 GMT  
		Size: 222.1 MB (222144215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e26a24e515fc29bea5fb4ad97d93055e97736137dbbff6c0a66d1e3cb662a266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2a0d93c03f13377ffa686d882edf0901118adbaeea959c691a9dc76256ea5b`

```dockerfile
```

-	Layers:
	-	`sha256:38affa8290df1776c35aab78bc46e1491c5b3a525152f3b1e737e46e6456d55e`  
		Last Modified: Tue, 29 Apr 2025 00:19:06 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04d9a14a26e0b8792115fbad3c25692abd8c3ea50dc544ff6954cc8a9d3b12ab`  
		Last Modified: Tue, 29 Apr 2025 00:19:05 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:6ff43004246ac7409ecbc3cf1d1f64fe97af549cff6e4eeffb347c53123695c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628715675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52ec6298460494f48ebd94562ccdc697dcc3bb3d3915515c744d5def51728ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675af5e5720aa9e9d4f74b056a7b58aa0a84a5b3cc2c23272c361e473b9c5b8`  
		Last Modified: Tue, 08 Apr 2025 15:34:04 GMT  
		Size: 214.4 MB (214387209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fd4fb10062d551eeb2e024d3e563728a42549e867f8f166eb7d3c22b7d6b78`  
		Last Modified: Tue, 08 Apr 2025 19:25:14 GMT  
		Size: 266.5 MB (266502721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c47a89a1025ff4dbb33264cf2765a8e1e0c24ff47135d1b6c7c7e977468d89e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15459677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7827834152d2d52c8fbc16a215bf024a151d424dffb4ab149188341b0cc1f14`

```dockerfile
```

-	Layers:
	-	`sha256:23ddb56e82f0fa073703d355e296183384c1fc63c0b493b2a1bac0b20c353294`  
		Last Modified: Tue, 08 Apr 2025 19:25:07 GMT  
		Size: 15.4 MB (15446470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfcaa31a08c5def654ca430c6b47811b40f07fd5cbdfd2e94e2fb98d08e77e8`  
		Last Modified: Tue, 08 Apr 2025 19:25:06 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:aaf804c60805de2a84400664811dd543e7a735e684976c5b4ac22ea1ae537910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611949825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f71016804f1861e6054a214aea01f56260a9f54e32cde4b102889b5ba38c3b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fde99ce0eec506f038695c59ba0ff56bd0df358636c0b067f55c60d7d566c`  
		Last Modified: Tue, 08 Apr 2025 06:52:25 GMT  
		Size: 63.5 MB (63498375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766d2c4791b14ffb813f2bd4d87d95e9030a5939b65f31722bc2c223f845ecf8`  
		Last Modified: Tue, 08 Apr 2025 10:02:09 GMT  
		Size: 183.4 MB (183388438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eb0c69619b19f87369d4a1737b46098625d76f72f75d41c18ecc2b9f8019cc`  
		Last Modified: Tue, 08 Apr 2025 18:17:17 GMT  
		Size: 293.9 MB (293903680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:21d031f77b8b2c841a56916b430442b3dbbfd340d1aadee3bf1561f97999cc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15297196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49e7c039c53b210b5e3cfc85ca1eb9fcaa5480271c4f2b0c5e5e6aa37781915`

```dockerfile
```

-	Layers:
	-	`sha256:0d2bad61871ee6c24e5ae84182871a58c88b6f3593a3f0a381f6236eec0606e9`  
		Last Modified: Tue, 08 Apr 2025 18:17:08 GMT  
		Size: 15.3 MB (15284058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1589d850c8b322cdebed632bcf0d29ee300ca793b83044f540479e4b39431e1`  
		Last Modified: Tue, 08 Apr 2025 18:17:07 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:eea163213169a83a58a975c16c59d71e344d9932f663cb850735e57d04e3a78d
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
$ docker pull rust@sha256:8c271c0f0dcb01fa63c88f6dea15e7bc3635576f84d26032170faac2d52a4e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.2 MB (520220542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15453801e070ee0e2545d6aacd3ede9512be0950202af0ba7e0521e3dab5a657`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Mon, 28 Apr 2025 22:15:30 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee2c8b84461fce714721ac74cb275f6aaa0de67c2aeaccb8193af9ea8b4d38`  
		Last Modified: Mon, 28 Apr 2025 23:12:29 GMT  
		Size: 197.1 MB (197107708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9066c54499afbbfd0cbc1d4f2a3e1de04f748f13531dffada1a0c61dfd36453f`  
		Last Modified: Tue, 29 Apr 2025 00:47:26 GMT  
		Size: 198.8 MB (198845544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:21a84938f50b45e05ce5cbb41e4714dbe3e866640e145d22188429f356ad4429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15086862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147b76c7800402cd7050842d3c7612cbc837d0bcf39d2b64d87d5990349a9f4a`

```dockerfile
```

-	Layers:
	-	`sha256:53a2905058c19fa7e018208b2351a1b70af430d00b6b1d6d32c52729ebd558c8`  
		Last Modified: Tue, 29 Apr 2025 00:47:24 GMT  
		Size: 15.1 MB (15075615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f89f6d37e15f2c84bf3a2d0edb1030882e2d1ee819bbdb8e39c702b9227c86ce`  
		Last Modified: Tue, 29 Apr 2025 00:47:23 GMT  
		Size: 11.2 KB (11247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:ed129955a5f1efbd8557d1c3d3ed9ae637d9adbf423c79a29dfe2a6779254295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.3 MB (523310260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b42a94efe835df3c1ee60011feb7bec025b4df5f862b615031133e68d2a3b0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
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
	-	`sha256:8c2fc9e6d23f3debfa68416a2b96331b92d563b20272933315ecfbbada38e955`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 49.0 MB (49031449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525b68fed12d763a57f1b020aa1579673112de80a5b780b5ffaa045109c81f23`  
		Last Modified: Tue, 08 Apr 2025 07:38:26 GMT  
		Size: 14.9 MB (14878713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909681b45fdfcbd0bfebc28d96cd1bdab32fd85e3af6788b49d9cb80e8ff865a`  
		Last Modified: Tue, 08 Apr 2025 17:30:33 GMT  
		Size: 50.6 MB (50624452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ae4904ff46404ac5bb348da93b4e4f750b89ecaf468fd2f4b669038dc51cfb`  
		Last Modified: Tue, 08 Apr 2025 20:36:13 GMT  
		Size: 167.6 MB (167560460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9324aa48468359b44400cdd12929b0da8d31a43b594b8361c6a6eb9c9252c1`  
		Last Modified: Wed, 09 Apr 2025 03:29:40 GMT  
		Size: 241.2 MB (241215186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:28192187a807cc51ff78c007c700090895505aa9bbcb1e554e1e887bec3c50d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14887676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb595f8ced635b06fcf9a61717b019b48d031bc466e3a6ee8dd2439c17103dd5`

```dockerfile
```

-	Layers:
	-	`sha256:7c157d370bd0a5868efeec965f7bdab7d6202c55ade93b51998737e616cdb623`  
		Last Modified: Wed, 09 Apr 2025 03:29:36 GMT  
		Size: 14.9 MB (14876352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6557cfe726aaf265db580bb9f6cf75eb3c19cab87774acfaa4183ba88ac1a943`  
		Last Modified: Wed, 09 Apr 2025 03:29:34 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:09a7f7dcc5882af5bbccc6dc2d269e4ad12b8614dd251c3aabfc4f7411b0f8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.5 MB (480522553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7757be1da64936c13a88161dfcf370ffdc62353fd997f8283cbce57cbe1ca3b1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322dad1d7c942b6794e486e4e0b838c10dfb06247f1794d20cc703ddfee969f`  
		Last Modified: Tue, 08 Apr 2025 06:03:40 GMT  
		Size: 15.7 MB (15749086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebaef8f9f6ff21c71a0e336a0e9a00fbb65d469480593ef8d1ef507941e6f6d`  
		Last Modified: Tue, 08 Apr 2025 12:18:43 GMT  
		Size: 54.9 MB (54850009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848ef88a118038c35ad53e6bc0e94192e99b916044a11fb61a40b31c77edc820`  
		Last Modified: Tue, 08 Apr 2025 15:54:19 GMT  
		Size: 190.0 MB (190022174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d5d165da97b462feba12c3696936055a7ddb81249fd994f73056e2bbb08d5f`  
		Last Modified: Tue, 08 Apr 2025 21:31:15 GMT  
		Size: 167.6 MB (167647062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d112402618f4d6f27648b816c07a25745eb4d79aa34ea481f96aac9ed675a320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15089174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a8450527599dfb60c80da9bb3f35748ff58ac969abe44738329c168e8195b1`

```dockerfile
```

-	Layers:
	-	`sha256:22c68f5deda14220e1d89c790721da688dcdd27e932e2f7e33e3734a63d2ab4d`  
		Last Modified: Tue, 08 Apr 2025 21:31:11 GMT  
		Size: 15.1 MB (15077821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ca44f0d2397d24f0dbb2d7aafc86c60976ef147f078230b9734ce5418cc0f8`  
		Last Modified: Tue, 08 Apr 2025 21:31:10 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:9cbc7bd302c43e0a62cdb858f9c24a58b87aca7bf043ffab7cb079d4d5770139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549153535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3ace1c51d4464391099c6feb9831aed5ef6fd61345c2f970e108a016c5ebee`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
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
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb48ef4c334135b55fe5dd328911059bfd41eec15edf03ff0ab96ca44fb6a1`  
		Last Modified: Mon, 28 Apr 2025 21:53:52 GMT  
		Size: 16.3 MB (16267399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f9ff435d5a831802e386be1d29f22419a5d3951a76711fcdfc9f9bad0e6e3`  
		Last Modified: Mon, 28 Apr 2025 22:14:52 GMT  
		Size: 56.0 MB (56047280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ef040f15a9c521f9352beaf246f79eec04035acb8b716f343f27a2aea49563`  
		Last Modified: Mon, 28 Apr 2025 23:12:49 GMT  
		Size: 200.0 MB (200011534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84444c00c33828bec847a0ebe02cdf86e4a38c359cd763bbab9e70a5c8548f42`  
		Last Modified: Tue, 29 Apr 2025 00:17:33 GMT  
		Size: 222.1 MB (222144220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a2265636dfa483bc6134f1471d3440d26019c187f2e845c84c8ab33248f5d8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15073859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65970c74d4efc0b684a893fd52a296fbf9af95f404deca1b28741c80dbc4580`

```dockerfile
```

-	Layers:
	-	`sha256:a255f8f56087be5473d5e5866f9da323ec16bcb91c91c88845c86ba78c4f2fe4`  
		Last Modified: Tue, 29 Apr 2025 00:17:28 GMT  
		Size: 15.1 MB (15062642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973d0dfea887d74ea1652c8a1f21f05a292fbb82170d601ae82d934a72dbc336`  
		Last Modified: Tue, 29 Apr 2025 00:17:27 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:3deccec2419f46f7052356d99e0c76ceba02a0164a45e1c5894481a4785e7895
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
$ docker pull rust@sha256:5265cf7f0324e5af0d0af625952b426cfaf5fc6daafd79b1fdedac07bd69b999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297830650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7f574507b85a8cc381daab85fd042918977aa4e469b8c0b3adca5ebbf2f53d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d2c2c6f222aae0625c61e9d3f36afe3bd17ebed1d2eb21f1bf888d76a5d60b`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
		Size: 269.6 MB (269603008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:19dd7a17f1dc76c4e00c549b877018bc870343a6ecbc8ef68fe7946a84a356d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f410651604a0a715d015565863b7efe3c81dcf3da755fb9cf24f7a5237556b`

```dockerfile
```

-	Layers:
	-	`sha256:ff862d7e48c414c8bb95d3a1388b734c191baea434a62085f4346713d401770d`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675eae4d6651df312a550a92c9e8941bcaedafe4f550de7cad9f475791b9a3b0`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
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
$ docker pull rust@sha256:9b4588a9375c6c2a2a7454768c282c8e549784b521eb0c5ea3e32d7568affed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318922232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4afab512f48e1dfcccdf517247ac52f880b84fd820a0b2d4949efd3c0301d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f7195df9fd10fb92d71646b4d86321f170c6c731039dd4e34938be58f58cb9`  
		Last Modified: Mon, 28 Apr 2025 21:59:24 GMT  
		Size: 289.7 MB (289711366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:51adece521582dbdc49671e0fbe582c8e8a6789f6274dc195eeee01c43cc3705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0b4b1a80ee612bf4ae7a0cf824e5305b3644dbae73ef8d0d8d832945a7b784`

```dockerfile
```

-	Layers:
	-	`sha256:0cf266b3c804c8acfcb96fe5b018f864f17e2d3be0b00960512021e7dedea803`  
		Last Modified: Mon, 28 Apr 2025 21:59:18 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a2e0dd93e9a6d69a21bdeb2e6d7d8350d6e6bd032336a2c1593141e3d80c57`  
		Last Modified: Mon, 28 Apr 2025 21:59:17 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:e5aeefd41ca6f9abd02b12460157ca851369b314458f653836b6041460b89818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367336038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84bea10cf021c1602244cf068230d973768342a4cd724e0c3118bfae5cfa97`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c04e3602592a873e00fef80b178c6583f85417553600599ea8e1e61736cad8`  
		Last Modified: Tue, 29 Apr 2025 03:38:35 GMT  
		Size: 335.3 MB (335267595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:f23567e86bb567602fbd3b97382d2e63737d1c041296ed7e66094cf7711c5063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c1b4c721edb518831b46540fa64acf0c3efa8d91e5d44979f23bf0a9e5a60a`

```dockerfile
```

-	Layers:
	-	`sha256:d780a892b067eb8a87aeba5b1ddc996252fb597316ab13515b746c3bdf531ef0`  
		Last Modified: Tue, 29 Apr 2025 03:38:27 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:188d119007c4e10172952ad43483211958e15eddcf785427c58e34052df76afa`  
		Last Modified: Tue, 29 Apr 2025 03:38:26 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:cd75cace871d1241847f08379dfd7b2913730d65f88736c71cd4073eebc53b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e951356ca72c6d32f55a1a349ce8e5030b100b4da94dd52e05829406fd63a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5365383afac604f9c2f2ab1254332b6835b90d820e7e3d14137a8ab8bd5f849`  
		Last Modified: Tue, 29 Apr 2025 02:34:37 GMT  
		Size: 344.0 MB (344011014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3fd3ab8f79e47636e149395239ceb7c46785b04e3f66d11d2b3645c2e0c130a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ab2946a315baa636e061bf47c4e0d08f33e4e452ee0dd0dbabb4c8cd56d7c5`

```dockerfile
```

-	Layers:
	-	`sha256:89ea65b28be4d0e2d05e9cd9e7b13b402be9f781990fc713eeb4ac680fee4ed0`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d046b9ce46b62be8c69446342f660b1449e172e7dfa84284fa1c4242cb3b348a`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:3deccec2419f46f7052356d99e0c76ceba02a0164a45e1c5894481a4785e7895
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
$ docker pull rust@sha256:5265cf7f0324e5af0d0af625952b426cfaf5fc6daafd79b1fdedac07bd69b999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297830650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7f574507b85a8cc381daab85fd042918977aa4e469b8c0b3adca5ebbf2f53d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d2c2c6f222aae0625c61e9d3f36afe3bd17ebed1d2eb21f1bf888d76a5d60b`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
		Size: 269.6 MB (269603008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:19dd7a17f1dc76c4e00c549b877018bc870343a6ecbc8ef68fe7946a84a356d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f410651604a0a715d015565863b7efe3c81dcf3da755fb9cf24f7a5237556b`

```dockerfile
```

-	Layers:
	-	`sha256:ff862d7e48c414c8bb95d3a1388b734c191baea434a62085f4346713d401770d`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675eae4d6651df312a550a92c9e8941bcaedafe4f550de7cad9f475791b9a3b0`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
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
$ docker pull rust@sha256:9b4588a9375c6c2a2a7454768c282c8e549784b521eb0c5ea3e32d7568affed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318922232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4afab512f48e1dfcccdf517247ac52f880b84fd820a0b2d4949efd3c0301d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f7195df9fd10fb92d71646b4d86321f170c6c731039dd4e34938be58f58cb9`  
		Last Modified: Mon, 28 Apr 2025 21:59:24 GMT  
		Size: 289.7 MB (289711366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:51adece521582dbdc49671e0fbe582c8e8a6789f6274dc195eeee01c43cc3705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0b4b1a80ee612bf4ae7a0cf824e5305b3644dbae73ef8d0d8d832945a7b784`

```dockerfile
```

-	Layers:
	-	`sha256:0cf266b3c804c8acfcb96fe5b018f864f17e2d3be0b00960512021e7dedea803`  
		Last Modified: Mon, 28 Apr 2025 21:59:18 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a2e0dd93e9a6d69a21bdeb2e6d7d8350d6e6bd032336a2c1593141e3d80c57`  
		Last Modified: Mon, 28 Apr 2025 21:59:17 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:e5aeefd41ca6f9abd02b12460157ca851369b314458f653836b6041460b89818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367336038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84bea10cf021c1602244cf068230d973768342a4cd724e0c3118bfae5cfa97`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c04e3602592a873e00fef80b178c6583f85417553600599ea8e1e61736cad8`  
		Last Modified: Tue, 29 Apr 2025 03:38:35 GMT  
		Size: 335.3 MB (335267595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f23567e86bb567602fbd3b97382d2e63737d1c041296ed7e66094cf7711c5063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c1b4c721edb518831b46540fa64acf0c3efa8d91e5d44979f23bf0a9e5a60a`

```dockerfile
```

-	Layers:
	-	`sha256:d780a892b067eb8a87aeba5b1ddc996252fb597316ab13515b746c3bdf531ef0`  
		Last Modified: Tue, 29 Apr 2025 03:38:27 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:188d119007c4e10172952ad43483211958e15eddcf785427c58e34052df76afa`  
		Last Modified: Tue, 29 Apr 2025 03:38:26 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:cd75cace871d1241847f08379dfd7b2913730d65f88736c71cd4073eebc53b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e951356ca72c6d32f55a1a349ce8e5030b100b4da94dd52e05829406fd63a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5365383afac604f9c2f2ab1254332b6835b90d820e7e3d14137a8ab8bd5f849`  
		Last Modified: Tue, 29 Apr 2025 02:34:37 GMT  
		Size: 344.0 MB (344011014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3fd3ab8f79e47636e149395239ceb7c46785b04e3f66d11d2b3645c2e0c130a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ab2946a315baa636e061bf47c4e0d08f33e4e452ee0dd0dbabb4c8cd56d7c5`

```dockerfile
```

-	Layers:
	-	`sha256:89ea65b28be4d0e2d05e9cd9e7b13b402be9f781990fc713eeb4ac680fee4ed0`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d046b9ce46b62be8c69446342f660b1449e172e7dfa84284fa1c4242cb3b348a`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:8b4fb6e91904117e77ff7fb19d63dc83c6f1ed3caa7915b9390e5380b19cb55d
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
$ docker pull rust@sha256:61200dad758eb2c4e99313d0c6782e7fa89311bd83c94b9bc39bc01948f587db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289241682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25e74260d87c5fa7492be92ca0677a11a991844226d26af85a21722fe8fd4dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0797f92ce1279f464536d8c0af7023351ee2e207ccec21fe543d01eb4c4248`  
		Last Modified: Mon, 28 Apr 2025 22:05:28 GMT  
		Size: 259.0 MB (258987078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1836529f3ca5bc812985db92eb733b1bccd994105d29fded97d9d61adea71be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e36b0a70ce16003c9069f2825bd02e341920e739a895f46f2a469f7a79fd07`

```dockerfile
```

-	Layers:
	-	`sha256:13123c2d58f95072da02ee8e10ac5a44b16d4f6545106822ca9f98b7eee11c9c`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
		Size: 4.2 MB (4175178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4758d2f11990f0f5dceffd56dc922a42f33a2fb2873222c6bc096a6c1cb942`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
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
$ docker pull rust@sha256:091710edd306bd2bf84340d1127b91227bc8fa29f7e37ba0036ec2686cd16113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314101243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd162dda1171190a0aa571d0efa79d256bae0efec08e9afdc2e79c38754466a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:73bb1b80ecf1f8784ad6f92a35120b6e2306657fc7e8cbaedca1f45900f3d746`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 31.2 MB (31187893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e304cb55c66d1a5edc35eacf691a84c62d770f1198d127335959a3166eeb088`  
		Last Modified: Mon, 28 Apr 2025 21:58:49 GMT  
		Size: 282.9 MB (282913350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4a0423225bb2de1faea503c48c34dce51dc7696d8c40f13d16e30180c1c91ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ef654c9879524c59c0bf60a53ef350537343ebe309bf9fa7371daa378cec71`

```dockerfile
```

-	Layers:
	-	`sha256:acd11de69428b51d1eeb16ee8532107d4b7f03aa5deb5323de965df13bf84155`  
		Last Modified: Mon, 28 Apr 2025 21:58:43 GMT  
		Size: 4.2 MB (4165435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58625db462ea2607636281f9a865fc50b768ee088febe47023718de82b41b7e4`  
		Last Modified: Mon, 28 Apr 2025 21:58:42 GMT  
		Size: 11.3 KB (11323 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86`

```console
$ docker pull rust@sha256:ff735b1f09be7bb43d0ceece3d6f03b877292ae0307e35b32f75165a05d574c5
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
$ docker pull rust@sha256:f163d1a53e6d105d037f8798f47f7947c062671bfb8d4485c612a1d00a3cbf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547098954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209b88fdf20bcc777094ee4ff43efc6ef043406c3a4c169785eda17fecc6318c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187b51b626e1d60ab369727b81f440adea9d45e97a45e137fc318be0bb7f09f`  
		Last Modified: Mon, 28 Apr 2025 23:12:20 GMT  
		Size: 211.4 MB (211356050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa897cd1d909c6f9aeeb2eb86f8281d7f1bd22ec60b937531af70f77e3b8c978`  
		Last Modified: Tue, 29 Apr 2025 00:20:42 GMT  
		Size: 198.8 MB (198846097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86` - unknown; unknown

```console
$ docker pull rust@sha256:c28aff946bf6a9641ea9333906292d4bcaca20d9730ac06f65c73b7dbfe00bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91b52445b0f0d88b77d2754a8b302421f4d6c97b7cb7d4de220050178066182`

```dockerfile
```

-	Layers:
	-	`sha256:b79e6f075844c12dfa724e6e05d0844d5de320465830dbb322f023f18d80c8fc`  
		Last Modified: Tue, 29 Apr 2025 00:20:37 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49427446706d8a35b3d9da8f7db167c3935e0225c64c41163ace92f38a50fb6`  
		Last Modified: Tue, 29 Apr 2025 00:20:36 GMT  
		Size: 13.1 KB (13137 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff3403ae6581adf67c0bbde3bcab29a147bf80f4392ab0af5dbed3377c1e119b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542266054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3698017437d2ae8077abed8488d38727dc5dba1f88e48876e5d3733f532a6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5414268749270f000845caf5689fb7740534b9fe922712301ba571a6afca96`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 59.6 MB (59639425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd5426bd57bea2caac0e0e87b98c0988fb39decb07637e76311bc28b01e6b7`  
		Last Modified: Tue, 08 Apr 2025 20:34:20 GMT  
		Size: 175.3 MB (175297229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093acd39fc465167a3795c75afa1eb7603459d1e396309304795a5c261b5a699`  
		Last Modified: Wed, 09 Apr 2025 03:31:38 GMT  
		Size: 241.2 MB (241214386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86` - unknown; unknown

```console
$ docker pull rust@sha256:965b9904c21bcd441911c4b25119ecca1e3f2fba0c3ab636faf4e528fc89a355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15289059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ac2dfec33d3f464c032fb6c8ec95b36285cdc7aca6e1012458969150a6d286`

```dockerfile
```

-	Layers:
	-	`sha256:69935c7f7900e361aabe717ea482ce229c0f4290d1f011ce1e508dba7b96a093`  
		Last Modified: Wed, 09 Apr 2025 03:31:32 GMT  
		Size: 15.3 MB (15275812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd85c681d8a8c03f05a9c034397cd1615a023bca10a054649801c9a54062374`  
		Last Modified: Wed, 09 Apr 2025 03:31:31 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0a27f7509b3def95327fe3735084c6a475bb52054efee7316d84fd91fc17736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506611045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee291f151e5b030a604f543d9a5c4541b96d0e637888a2a09334bd826322ab1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002e18bd5659ca9d155e99922678788bec836a3ac4964d8a9567ce59e2154de9`  
		Last Modified: Tue, 08 Apr 2025 15:52:42 GMT  
		Size: 202.7 MB (202735307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775439c6d731e711d1e42014fd69218e477c0c43221098e6d1513428f9946240`  
		Last Modified: Tue, 08 Apr 2025 21:32:10 GMT  
		Size: 167.6 MB (167648150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86` - unknown; unknown

```console
$ docker pull rust@sha256:63403d5c50b5086ee37972bd4ddb3dac08ba9444f59ed275e4639aa2c44c5c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e9f0697f2a2efe50253e36a3bc474bac40598a69515a99e7596cbf41d4c034`

```dockerfile
```

-	Layers:
	-	`sha256:2af08bf3572f4cd46f60afd036e4b1bf91b775e6c09a6bf6295ec9afbec238bf`  
		Last Modified: Tue, 08 Apr 2025 21:32:07 GMT  
		Size: 15.5 MB (15499945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32389045ed63fed52cb8d7ec269d8b4a0e5421639eb6f7906eba095d4d5d1e64`  
		Last Modified: Tue, 08 Apr 2025 21:32:06 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86` - linux; 386

```console
$ docker pull rust@sha256:69531fcb8a67b072bfc78f893d76a5d5c5a325536a4f948493f5fae1756d4019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572991948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f4ce1664011b7b08cabc2bcb040af4431dd6da7fff8a55460b8c4e9fd01a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Mon, 28 Apr 2025 21:53:42 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce8929d56fab56325a8eea211cb4cd1021bc6ffc1e7a794d505ddbe638b23cd`  
		Last Modified: Mon, 28 Apr 2025 22:15:00 GMT  
		Size: 66.2 MB (66228922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1528cc13747bb103866d00332de43f9304156fef5a2f396b15d9e173b1365f5`  
		Last Modified: Mon, 28 Apr 2025 23:13:00 GMT  
		Size: 210.3 MB (210293092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a0a0e26e85220e6482bcf2859ccd19dc889d8c6237381e13a52446ce56f374`  
		Last Modified: Tue, 29 Apr 2025 00:19:10 GMT  
		Size: 222.1 MB (222144215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86` - unknown; unknown

```console
$ docker pull rust@sha256:e26a24e515fc29bea5fb4ad97d93055e97736137dbbff6c0a66d1e3cb662a266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2a0d93c03f13377ffa686d882edf0901118adbaeea959c691a9dc76256ea5b`

```dockerfile
```

-	Layers:
	-	`sha256:38affa8290df1776c35aab78bc46e1491c5b3a525152f3b1e737e46e6456d55e`  
		Last Modified: Tue, 29 Apr 2025 00:19:06 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04d9a14a26e0b8792115fbad3c25692abd8c3ea50dc544ff6954cc8a9d3b12ab`  
		Last Modified: Tue, 29 Apr 2025 00:19:05 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86` - linux; ppc64le

```console
$ docker pull rust@sha256:6ff43004246ac7409ecbc3cf1d1f64fe97af549cff6e4eeffb347c53123695c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628715675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52ec6298460494f48ebd94562ccdc697dcc3bb3d3915515c744d5def51728ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675af5e5720aa9e9d4f74b056a7b58aa0a84a5b3cc2c23272c361e473b9c5b8`  
		Last Modified: Tue, 08 Apr 2025 15:34:04 GMT  
		Size: 214.4 MB (214387209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fd4fb10062d551eeb2e024d3e563728a42549e867f8f166eb7d3c22b7d6b78`  
		Last Modified: Tue, 08 Apr 2025 19:25:14 GMT  
		Size: 266.5 MB (266502721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86` - unknown; unknown

```console
$ docker pull rust@sha256:c47a89a1025ff4dbb33264cf2765a8e1e0c24ff47135d1b6c7c7e977468d89e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15459677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7827834152d2d52c8fbc16a215bf024a151d424dffb4ab149188341b0cc1f14`

```dockerfile
```

-	Layers:
	-	`sha256:23ddb56e82f0fa073703d355e296183384c1fc63c0b493b2a1bac0b20c353294`  
		Last Modified: Tue, 08 Apr 2025 19:25:07 GMT  
		Size: 15.4 MB (15446470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfcaa31a08c5def654ca430c6b47811b40f07fd5cbdfd2e94e2fb98d08e77e8`  
		Last Modified: Tue, 08 Apr 2025 19:25:06 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86` - linux; s390x

```console
$ docker pull rust@sha256:aaf804c60805de2a84400664811dd543e7a735e684976c5b4ac22ea1ae537910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611949825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f71016804f1861e6054a214aea01f56260a9f54e32cde4b102889b5ba38c3b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fde99ce0eec506f038695c59ba0ff56bd0df358636c0b067f55c60d7d566c`  
		Last Modified: Tue, 08 Apr 2025 06:52:25 GMT  
		Size: 63.5 MB (63498375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766d2c4791b14ffb813f2bd4d87d95e9030a5939b65f31722bc2c223f845ecf8`  
		Last Modified: Tue, 08 Apr 2025 10:02:09 GMT  
		Size: 183.4 MB (183388438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eb0c69619b19f87369d4a1737b46098625d76f72f75d41c18ecc2b9f8019cc`  
		Last Modified: Tue, 08 Apr 2025 18:17:17 GMT  
		Size: 293.9 MB (293903680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86` - unknown; unknown

```console
$ docker pull rust@sha256:21d031f77b8b2c841a56916b430442b3dbbfd340d1aadee3bf1561f97999cc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15297196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49e7c039c53b210b5e3cfc85ca1eb9fcaa5480271c4f2b0c5e5e6aa37781915`

```dockerfile
```

-	Layers:
	-	`sha256:0d2bad61871ee6c24e5ae84182871a58c88b6f3593a3f0a381f6236eec0606e9`  
		Last Modified: Tue, 08 Apr 2025 18:17:08 GMT  
		Size: 15.3 MB (15284058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1589d850c8b322cdebed632bcf0d29ee300ca793b83044f540479e4b39431e1`  
		Last Modified: Tue, 08 Apr 2025 18:17:07 GMT  
		Size: 13.1 KB (13138 bytes)  
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
$ docker pull rust@sha256:ff735b1f09be7bb43d0ceece3d6f03b877292ae0307e35b32f75165a05d574c5
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
$ docker pull rust@sha256:f163d1a53e6d105d037f8798f47f7947c062671bfb8d4485c612a1d00a3cbf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547098954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209b88fdf20bcc777094ee4ff43efc6ef043406c3a4c169785eda17fecc6318c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187b51b626e1d60ab369727b81f440adea9d45e97a45e137fc318be0bb7f09f`  
		Last Modified: Mon, 28 Apr 2025 23:12:20 GMT  
		Size: 211.4 MB (211356050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa897cd1d909c6f9aeeb2eb86f8281d7f1bd22ec60b937531af70f77e3b8c978`  
		Last Modified: Tue, 29 Apr 2025 00:20:42 GMT  
		Size: 198.8 MB (198846097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c28aff946bf6a9641ea9333906292d4bcaca20d9730ac06f65c73b7dbfe00bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91b52445b0f0d88b77d2754a8b302421f4d6c97b7cb7d4de220050178066182`

```dockerfile
```

-	Layers:
	-	`sha256:b79e6f075844c12dfa724e6e05d0844d5de320465830dbb322f023f18d80c8fc`  
		Last Modified: Tue, 29 Apr 2025 00:20:37 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49427446706d8a35b3d9da8f7db167c3935e0225c64c41163ace92f38a50fb6`  
		Last Modified: Tue, 29 Apr 2025 00:20:36 GMT  
		Size: 13.1 KB (13137 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff3403ae6581adf67c0bbde3bcab29a147bf80f4392ab0af5dbed3377c1e119b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542266054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3698017437d2ae8077abed8488d38727dc5dba1f88e48876e5d3733f532a6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5414268749270f000845caf5689fb7740534b9fe922712301ba571a6afca96`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 59.6 MB (59639425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd5426bd57bea2caac0e0e87b98c0988fb39decb07637e76311bc28b01e6b7`  
		Last Modified: Tue, 08 Apr 2025 20:34:20 GMT  
		Size: 175.3 MB (175297229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093acd39fc465167a3795c75afa1eb7603459d1e396309304795a5c261b5a699`  
		Last Modified: Wed, 09 Apr 2025 03:31:38 GMT  
		Size: 241.2 MB (241214386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:965b9904c21bcd441911c4b25119ecca1e3f2fba0c3ab636faf4e528fc89a355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15289059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ac2dfec33d3f464c032fb6c8ec95b36285cdc7aca6e1012458969150a6d286`

```dockerfile
```

-	Layers:
	-	`sha256:69935c7f7900e361aabe717ea482ce229c0f4290d1f011ce1e508dba7b96a093`  
		Last Modified: Wed, 09 Apr 2025 03:31:32 GMT  
		Size: 15.3 MB (15275812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd85c681d8a8c03f05a9c034397cd1615a023bca10a054649801c9a54062374`  
		Last Modified: Wed, 09 Apr 2025 03:31:31 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0a27f7509b3def95327fe3735084c6a475bb52054efee7316d84fd91fc17736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506611045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee291f151e5b030a604f543d9a5c4541b96d0e637888a2a09334bd826322ab1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002e18bd5659ca9d155e99922678788bec836a3ac4964d8a9567ce59e2154de9`  
		Last Modified: Tue, 08 Apr 2025 15:52:42 GMT  
		Size: 202.7 MB (202735307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775439c6d731e711d1e42014fd69218e477c0c43221098e6d1513428f9946240`  
		Last Modified: Tue, 08 Apr 2025 21:32:10 GMT  
		Size: 167.6 MB (167648150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:63403d5c50b5086ee37972bd4ddb3dac08ba9444f59ed275e4639aa2c44c5c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e9f0697f2a2efe50253e36a3bc474bac40598a69515a99e7596cbf41d4c034`

```dockerfile
```

-	Layers:
	-	`sha256:2af08bf3572f4cd46f60afd036e4b1bf91b775e6c09a6bf6295ec9afbec238bf`  
		Last Modified: Tue, 08 Apr 2025 21:32:07 GMT  
		Size: 15.5 MB (15499945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32389045ed63fed52cb8d7ec269d8b4a0e5421639eb6f7906eba095d4d5d1e64`  
		Last Modified: Tue, 08 Apr 2025 21:32:06 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bookworm` - linux; 386

```console
$ docker pull rust@sha256:69531fcb8a67b072bfc78f893d76a5d5c5a325536a4f948493f5fae1756d4019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572991948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f4ce1664011b7b08cabc2bcb040af4431dd6da7fff8a55460b8c4e9fd01a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Mon, 28 Apr 2025 21:53:42 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce8929d56fab56325a8eea211cb4cd1021bc6ffc1e7a794d505ddbe638b23cd`  
		Last Modified: Mon, 28 Apr 2025 22:15:00 GMT  
		Size: 66.2 MB (66228922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1528cc13747bb103866d00332de43f9304156fef5a2f396b15d9e173b1365f5`  
		Last Modified: Mon, 28 Apr 2025 23:13:00 GMT  
		Size: 210.3 MB (210293092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a0a0e26e85220e6482bcf2859ccd19dc889d8c6237381e13a52446ce56f374`  
		Last Modified: Tue, 29 Apr 2025 00:19:10 GMT  
		Size: 222.1 MB (222144215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e26a24e515fc29bea5fb4ad97d93055e97736137dbbff6c0a66d1e3cb662a266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2a0d93c03f13377ffa686d882edf0901118adbaeea959c691a9dc76256ea5b`

```dockerfile
```

-	Layers:
	-	`sha256:38affa8290df1776c35aab78bc46e1491c5b3a525152f3b1e737e46e6456d55e`  
		Last Modified: Tue, 29 Apr 2025 00:19:06 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04d9a14a26e0b8792115fbad3c25692abd8c3ea50dc544ff6954cc8a9d3b12ab`  
		Last Modified: Tue, 29 Apr 2025 00:19:05 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:6ff43004246ac7409ecbc3cf1d1f64fe97af549cff6e4eeffb347c53123695c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628715675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52ec6298460494f48ebd94562ccdc697dcc3bb3d3915515c744d5def51728ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675af5e5720aa9e9d4f74b056a7b58aa0a84a5b3cc2c23272c361e473b9c5b8`  
		Last Modified: Tue, 08 Apr 2025 15:34:04 GMT  
		Size: 214.4 MB (214387209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fd4fb10062d551eeb2e024d3e563728a42549e867f8f166eb7d3c22b7d6b78`  
		Last Modified: Tue, 08 Apr 2025 19:25:14 GMT  
		Size: 266.5 MB (266502721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c47a89a1025ff4dbb33264cf2765a8e1e0c24ff47135d1b6c7c7e977468d89e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15459677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7827834152d2d52c8fbc16a215bf024a151d424dffb4ab149188341b0cc1f14`

```dockerfile
```

-	Layers:
	-	`sha256:23ddb56e82f0fa073703d355e296183384c1fc63c0b493b2a1bac0b20c353294`  
		Last Modified: Tue, 08 Apr 2025 19:25:07 GMT  
		Size: 15.4 MB (15446470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfcaa31a08c5def654ca430c6b47811b40f07fd5cbdfd2e94e2fb98d08e77e8`  
		Last Modified: Tue, 08 Apr 2025 19:25:06 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:aaf804c60805de2a84400664811dd543e7a735e684976c5b4ac22ea1ae537910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611949825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f71016804f1861e6054a214aea01f56260a9f54e32cde4b102889b5ba38c3b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fde99ce0eec506f038695c59ba0ff56bd0df358636c0b067f55c60d7d566c`  
		Last Modified: Tue, 08 Apr 2025 06:52:25 GMT  
		Size: 63.5 MB (63498375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766d2c4791b14ffb813f2bd4d87d95e9030a5939b65f31722bc2c223f845ecf8`  
		Last Modified: Tue, 08 Apr 2025 10:02:09 GMT  
		Size: 183.4 MB (183388438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eb0c69619b19f87369d4a1737b46098625d76f72f75d41c18ecc2b9f8019cc`  
		Last Modified: Tue, 08 Apr 2025 18:17:17 GMT  
		Size: 293.9 MB (293903680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:21d031f77b8b2c841a56916b430442b3dbbfd340d1aadee3bf1561f97999cc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15297196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49e7c039c53b210b5e3cfc85ca1eb9fcaa5480271c4f2b0c5e5e6aa37781915`

```dockerfile
```

-	Layers:
	-	`sha256:0d2bad61871ee6c24e5ae84182871a58c88b6f3593a3f0a381f6236eec0606e9`  
		Last Modified: Tue, 08 Apr 2025 18:17:08 GMT  
		Size: 15.3 MB (15284058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1589d850c8b322cdebed632bcf0d29ee300ca793b83044f540479e4b39431e1`  
		Last Modified: Tue, 08 Apr 2025 18:17:07 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86-bullseye`

```console
$ docker pull rust@sha256:eea163213169a83a58a975c16c59d71e344d9932f663cb850735e57d04e3a78d
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
$ docker pull rust@sha256:8c271c0f0dcb01fa63c88f6dea15e7bc3635576f84d26032170faac2d52a4e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.2 MB (520220542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15453801e070ee0e2545d6aacd3ede9512be0950202af0ba7e0521e3dab5a657`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Mon, 28 Apr 2025 22:15:30 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee2c8b84461fce714721ac74cb275f6aaa0de67c2aeaccb8193af9ea8b4d38`  
		Last Modified: Mon, 28 Apr 2025 23:12:29 GMT  
		Size: 197.1 MB (197107708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9066c54499afbbfd0cbc1d4f2a3e1de04f748f13531dffada1a0c61dfd36453f`  
		Last Modified: Tue, 29 Apr 2025 00:47:26 GMT  
		Size: 198.8 MB (198845544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:21a84938f50b45e05ce5cbb41e4714dbe3e866640e145d22188429f356ad4429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15086862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147b76c7800402cd7050842d3c7612cbc837d0bcf39d2b64d87d5990349a9f4a`

```dockerfile
```

-	Layers:
	-	`sha256:53a2905058c19fa7e018208b2351a1b70af430d00b6b1d6d32c52729ebd558c8`  
		Last Modified: Tue, 29 Apr 2025 00:47:24 GMT  
		Size: 15.1 MB (15075615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f89f6d37e15f2c84bf3a2d0edb1030882e2d1ee819bbdb8e39c702b9227c86ce`  
		Last Modified: Tue, 29 Apr 2025 00:47:23 GMT  
		Size: 11.2 KB (11247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:ed129955a5f1efbd8557d1c3d3ed9ae637d9adbf423c79a29dfe2a6779254295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.3 MB (523310260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b42a94efe835df3c1ee60011feb7bec025b4df5f862b615031133e68d2a3b0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
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
	-	`sha256:8c2fc9e6d23f3debfa68416a2b96331b92d563b20272933315ecfbbada38e955`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 49.0 MB (49031449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525b68fed12d763a57f1b020aa1579673112de80a5b780b5ffaa045109c81f23`  
		Last Modified: Tue, 08 Apr 2025 07:38:26 GMT  
		Size: 14.9 MB (14878713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909681b45fdfcbd0bfebc28d96cd1bdab32fd85e3af6788b49d9cb80e8ff865a`  
		Last Modified: Tue, 08 Apr 2025 17:30:33 GMT  
		Size: 50.6 MB (50624452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ae4904ff46404ac5bb348da93b4e4f750b89ecaf468fd2f4b669038dc51cfb`  
		Last Modified: Tue, 08 Apr 2025 20:36:13 GMT  
		Size: 167.6 MB (167560460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9324aa48468359b44400cdd12929b0da8d31a43b594b8361c6a6eb9c9252c1`  
		Last Modified: Wed, 09 Apr 2025 03:29:40 GMT  
		Size: 241.2 MB (241215186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:28192187a807cc51ff78c007c700090895505aa9bbcb1e554e1e887bec3c50d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14887676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb595f8ced635b06fcf9a61717b019b48d031bc466e3a6ee8dd2439c17103dd5`

```dockerfile
```

-	Layers:
	-	`sha256:7c157d370bd0a5868efeec965f7bdab7d6202c55ade93b51998737e616cdb623`  
		Last Modified: Wed, 09 Apr 2025 03:29:36 GMT  
		Size: 14.9 MB (14876352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6557cfe726aaf265db580bb9f6cf75eb3c19cab87774acfaa4183ba88ac1a943`  
		Last Modified: Wed, 09 Apr 2025 03:29:34 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:09a7f7dcc5882af5bbccc6dc2d269e4ad12b8614dd251c3aabfc4f7411b0f8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.5 MB (480522553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7757be1da64936c13a88161dfcf370ffdc62353fd997f8283cbce57cbe1ca3b1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322dad1d7c942b6794e486e4e0b838c10dfb06247f1794d20cc703ddfee969f`  
		Last Modified: Tue, 08 Apr 2025 06:03:40 GMT  
		Size: 15.7 MB (15749086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebaef8f9f6ff21c71a0e336a0e9a00fbb65d469480593ef8d1ef507941e6f6d`  
		Last Modified: Tue, 08 Apr 2025 12:18:43 GMT  
		Size: 54.9 MB (54850009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848ef88a118038c35ad53e6bc0e94192e99b916044a11fb61a40b31c77edc820`  
		Last Modified: Tue, 08 Apr 2025 15:54:19 GMT  
		Size: 190.0 MB (190022174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d5d165da97b462feba12c3696936055a7ddb81249fd994f73056e2bbb08d5f`  
		Last Modified: Tue, 08 Apr 2025 21:31:15 GMT  
		Size: 167.6 MB (167647062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d112402618f4d6f27648b816c07a25745eb4d79aa34ea481f96aac9ed675a320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15089174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a8450527599dfb60c80da9bb3f35748ff58ac969abe44738329c168e8195b1`

```dockerfile
```

-	Layers:
	-	`sha256:22c68f5deda14220e1d89c790721da688dcdd27e932e2f7e33e3734a63d2ab4d`  
		Last Modified: Tue, 08 Apr 2025 21:31:11 GMT  
		Size: 15.1 MB (15077821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ca44f0d2397d24f0dbb2d7aafc86c60976ef147f078230b9734ce5418cc0f8`  
		Last Modified: Tue, 08 Apr 2025 21:31:10 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-bullseye` - linux; 386

```console
$ docker pull rust@sha256:9cbc7bd302c43e0a62cdb858f9c24a58b87aca7bf043ffab7cb079d4d5770139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549153535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3ace1c51d4464391099c6feb9831aed5ef6fd61345c2f970e108a016c5ebee`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
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
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb48ef4c334135b55fe5dd328911059bfd41eec15edf03ff0ab96ca44fb6a1`  
		Last Modified: Mon, 28 Apr 2025 21:53:52 GMT  
		Size: 16.3 MB (16267399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f9ff435d5a831802e386be1d29f22419a5d3951a76711fcdfc9f9bad0e6e3`  
		Last Modified: Mon, 28 Apr 2025 22:14:52 GMT  
		Size: 56.0 MB (56047280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ef040f15a9c521f9352beaf246f79eec04035acb8b716f343f27a2aea49563`  
		Last Modified: Mon, 28 Apr 2025 23:12:49 GMT  
		Size: 200.0 MB (200011534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84444c00c33828bec847a0ebe02cdf86e4a38c359cd763bbab9e70a5c8548f42`  
		Last Modified: Tue, 29 Apr 2025 00:17:33 GMT  
		Size: 222.1 MB (222144220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a2265636dfa483bc6134f1471d3440d26019c187f2e845c84c8ab33248f5d8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15073859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65970c74d4efc0b684a893fd52a296fbf9af95f404deca1b28741c80dbc4580`

```dockerfile
```

-	Layers:
	-	`sha256:a255f8f56087be5473d5e5866f9da323ec16bcb91c91c88845c86ba78c4f2fe4`  
		Last Modified: Tue, 29 Apr 2025 00:17:28 GMT  
		Size: 15.1 MB (15062642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973d0dfea887d74ea1652c8a1f21f05a292fbb82170d601ae82d934a72dbc336`  
		Last Modified: Tue, 29 Apr 2025 00:17:27 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86-slim`

```console
$ docker pull rust@sha256:3deccec2419f46f7052356d99e0c76ceba02a0164a45e1c5894481a4785e7895
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
$ docker pull rust@sha256:5265cf7f0324e5af0d0af625952b426cfaf5fc6daafd79b1fdedac07bd69b999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297830650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7f574507b85a8cc381daab85fd042918977aa4e469b8c0b3adca5ebbf2f53d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d2c2c6f222aae0625c61e9d3f36afe3bd17ebed1d2eb21f1bf888d76a5d60b`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
		Size: 269.6 MB (269603008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim` - unknown; unknown

```console
$ docker pull rust@sha256:19dd7a17f1dc76c4e00c549b877018bc870343a6ecbc8ef68fe7946a84a356d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f410651604a0a715d015565863b7efe3c81dcf3da755fb9cf24f7a5237556b`

```dockerfile
```

-	Layers:
	-	`sha256:ff862d7e48c414c8bb95d3a1388b734c191baea434a62085f4346713d401770d`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675eae4d6651df312a550a92c9e8941bcaedafe4f550de7cad9f475791b9a3b0`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
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
$ docker pull rust@sha256:9b4588a9375c6c2a2a7454768c282c8e549784b521eb0c5ea3e32d7568affed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318922232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4afab512f48e1dfcccdf517247ac52f880b84fd820a0b2d4949efd3c0301d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f7195df9fd10fb92d71646b4d86321f170c6c731039dd4e34938be58f58cb9`  
		Last Modified: Mon, 28 Apr 2025 21:59:24 GMT  
		Size: 289.7 MB (289711366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim` - unknown; unknown

```console
$ docker pull rust@sha256:51adece521582dbdc49671e0fbe582c8e8a6789f6274dc195eeee01c43cc3705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0b4b1a80ee612bf4ae7a0cf824e5305b3644dbae73ef8d0d8d832945a7b784`

```dockerfile
```

-	Layers:
	-	`sha256:0cf266b3c804c8acfcb96fe5b018f864f17e2d3be0b00960512021e7dedea803`  
		Last Modified: Mon, 28 Apr 2025 21:59:18 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a2e0dd93e9a6d69a21bdeb2e6d7d8350d6e6bd032336a2c1593141e3d80c57`  
		Last Modified: Mon, 28 Apr 2025 21:59:17 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:e5aeefd41ca6f9abd02b12460157ca851369b314458f653836b6041460b89818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367336038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84bea10cf021c1602244cf068230d973768342a4cd724e0c3118bfae5cfa97`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c04e3602592a873e00fef80b178c6583f85417553600599ea8e1e61736cad8`  
		Last Modified: Tue, 29 Apr 2025 03:38:35 GMT  
		Size: 335.3 MB (335267595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim` - unknown; unknown

```console
$ docker pull rust@sha256:f23567e86bb567602fbd3b97382d2e63737d1c041296ed7e66094cf7711c5063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c1b4c721edb518831b46540fa64acf0c3efa8d91e5d44979f23bf0a9e5a60a`

```dockerfile
```

-	Layers:
	-	`sha256:d780a892b067eb8a87aeba5b1ddc996252fb597316ab13515b746c3bdf531ef0`  
		Last Modified: Tue, 29 Apr 2025 03:38:27 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:188d119007c4e10172952ad43483211958e15eddcf785427c58e34052df76afa`  
		Last Modified: Tue, 29 Apr 2025 03:38:26 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim` - linux; s390x

```console
$ docker pull rust@sha256:cd75cace871d1241847f08379dfd7b2913730d65f88736c71cd4073eebc53b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e951356ca72c6d32f55a1a349ce8e5030b100b4da94dd52e05829406fd63a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5365383afac604f9c2f2ab1254332b6835b90d820e7e3d14137a8ab8bd5f849`  
		Last Modified: Tue, 29 Apr 2025 02:34:37 GMT  
		Size: 344.0 MB (344011014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3fd3ab8f79e47636e149395239ceb7c46785b04e3f66d11d2b3645c2e0c130a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ab2946a315baa636e061bf47c4e0d08f33e4e452ee0dd0dbabb4c8cd56d7c5`

```dockerfile
```

-	Layers:
	-	`sha256:89ea65b28be4d0e2d05e9cd9e7b13b402be9f781990fc713eeb4ac680fee4ed0`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d046b9ce46b62be8c69446342f660b1449e172e7dfa84284fa1c4242cb3b348a`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86-slim-bookworm`

```console
$ docker pull rust@sha256:3deccec2419f46f7052356d99e0c76ceba02a0164a45e1c5894481a4785e7895
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
$ docker pull rust@sha256:5265cf7f0324e5af0d0af625952b426cfaf5fc6daafd79b1fdedac07bd69b999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297830650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7f574507b85a8cc381daab85fd042918977aa4e469b8c0b3adca5ebbf2f53d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d2c2c6f222aae0625c61e9d3f36afe3bd17ebed1d2eb21f1bf888d76a5d60b`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
		Size: 269.6 MB (269603008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:19dd7a17f1dc76c4e00c549b877018bc870343a6ecbc8ef68fe7946a84a356d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f410651604a0a715d015565863b7efe3c81dcf3da755fb9cf24f7a5237556b`

```dockerfile
```

-	Layers:
	-	`sha256:ff862d7e48c414c8bb95d3a1388b734c191baea434a62085f4346713d401770d`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675eae4d6651df312a550a92c9e8941bcaedafe4f550de7cad9f475791b9a3b0`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
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
$ docker pull rust@sha256:9b4588a9375c6c2a2a7454768c282c8e549784b521eb0c5ea3e32d7568affed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318922232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4afab512f48e1dfcccdf517247ac52f880b84fd820a0b2d4949efd3c0301d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f7195df9fd10fb92d71646b4d86321f170c6c731039dd4e34938be58f58cb9`  
		Last Modified: Mon, 28 Apr 2025 21:59:24 GMT  
		Size: 289.7 MB (289711366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:51adece521582dbdc49671e0fbe582c8e8a6789f6274dc195eeee01c43cc3705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0b4b1a80ee612bf4ae7a0cf824e5305b3644dbae73ef8d0d8d832945a7b784`

```dockerfile
```

-	Layers:
	-	`sha256:0cf266b3c804c8acfcb96fe5b018f864f17e2d3be0b00960512021e7dedea803`  
		Last Modified: Mon, 28 Apr 2025 21:59:18 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a2e0dd93e9a6d69a21bdeb2e6d7d8350d6e6bd032336a2c1593141e3d80c57`  
		Last Modified: Mon, 28 Apr 2025 21:59:17 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:e5aeefd41ca6f9abd02b12460157ca851369b314458f653836b6041460b89818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367336038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84bea10cf021c1602244cf068230d973768342a4cd724e0c3118bfae5cfa97`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c04e3602592a873e00fef80b178c6583f85417553600599ea8e1e61736cad8`  
		Last Modified: Tue, 29 Apr 2025 03:38:35 GMT  
		Size: 335.3 MB (335267595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f23567e86bb567602fbd3b97382d2e63737d1c041296ed7e66094cf7711c5063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c1b4c721edb518831b46540fa64acf0c3efa8d91e5d44979f23bf0a9e5a60a`

```dockerfile
```

-	Layers:
	-	`sha256:d780a892b067eb8a87aeba5b1ddc996252fb597316ab13515b746c3bdf531ef0`  
		Last Modified: Tue, 29 Apr 2025 03:38:27 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:188d119007c4e10172952ad43483211958e15eddcf785427c58e34052df76afa`  
		Last Modified: Tue, 29 Apr 2025 03:38:26 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:cd75cace871d1241847f08379dfd7b2913730d65f88736c71cd4073eebc53b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e951356ca72c6d32f55a1a349ce8e5030b100b4da94dd52e05829406fd63a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5365383afac604f9c2f2ab1254332b6835b90d820e7e3d14137a8ab8bd5f849`  
		Last Modified: Tue, 29 Apr 2025 02:34:37 GMT  
		Size: 344.0 MB (344011014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3fd3ab8f79e47636e149395239ceb7c46785b04e3f66d11d2b3645c2e0c130a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ab2946a315baa636e061bf47c4e0d08f33e4e452ee0dd0dbabb4c8cd56d7c5`

```dockerfile
```

-	Layers:
	-	`sha256:89ea65b28be4d0e2d05e9cd9e7b13b402be9f781990fc713eeb4ac680fee4ed0`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d046b9ce46b62be8c69446342f660b1449e172e7dfa84284fa1c4242cb3b348a`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86-slim-bullseye`

```console
$ docker pull rust@sha256:8b4fb6e91904117e77ff7fb19d63dc83c6f1ed3caa7915b9390e5380b19cb55d
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
$ docker pull rust@sha256:61200dad758eb2c4e99313d0c6782e7fa89311bd83c94b9bc39bc01948f587db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289241682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25e74260d87c5fa7492be92ca0677a11a991844226d26af85a21722fe8fd4dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0797f92ce1279f464536d8c0af7023351ee2e207ccec21fe543d01eb4c4248`  
		Last Modified: Mon, 28 Apr 2025 22:05:28 GMT  
		Size: 259.0 MB (258987078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1836529f3ca5bc812985db92eb733b1bccd994105d29fded97d9d61adea71be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e36b0a70ce16003c9069f2825bd02e341920e739a895f46f2a469f7a79fd07`

```dockerfile
```

-	Layers:
	-	`sha256:13123c2d58f95072da02ee8e10ac5a44b16d4f6545106822ca9f98b7eee11c9c`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
		Size: 4.2 MB (4175178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4758d2f11990f0f5dceffd56dc922a42f33a2fb2873222c6bc096a6c1cb942`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
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
$ docker pull rust@sha256:091710edd306bd2bf84340d1127b91227bc8fa29f7e37ba0036ec2686cd16113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314101243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd162dda1171190a0aa571d0efa79d256bae0efec08e9afdc2e79c38754466a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:73bb1b80ecf1f8784ad6f92a35120b6e2306657fc7e8cbaedca1f45900f3d746`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 31.2 MB (31187893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e304cb55c66d1a5edc35eacf691a84c62d770f1198d127335959a3166eeb088`  
		Last Modified: Mon, 28 Apr 2025 21:58:49 GMT  
		Size: 282.9 MB (282913350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4a0423225bb2de1faea503c48c34dce51dc7696d8c40f13d16e30180c1c91ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ef654c9879524c59c0bf60a53ef350537343ebe309bf9fa7371daa378cec71`

```dockerfile
```

-	Layers:
	-	`sha256:acd11de69428b51d1eeb16ee8532107d4b7f03aa5deb5323de965df13bf84155`  
		Last Modified: Mon, 28 Apr 2025 21:58:43 GMT  
		Size: 4.2 MB (4165435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58625db462ea2607636281f9a865fc50b768ee088febe47023718de82b41b7e4`  
		Last Modified: Mon, 28 Apr 2025 21:58:42 GMT  
		Size: 11.3 KB (11323 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0`

```console
$ docker pull rust@sha256:ff735b1f09be7bb43d0ceece3d6f03b877292ae0307e35b32f75165a05d574c5
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
$ docker pull rust@sha256:f163d1a53e6d105d037f8798f47f7947c062671bfb8d4485c612a1d00a3cbf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547098954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209b88fdf20bcc777094ee4ff43efc6ef043406c3a4c169785eda17fecc6318c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187b51b626e1d60ab369727b81f440adea9d45e97a45e137fc318be0bb7f09f`  
		Last Modified: Mon, 28 Apr 2025 23:12:20 GMT  
		Size: 211.4 MB (211356050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa897cd1d909c6f9aeeb2eb86f8281d7f1bd22ec60b937531af70f77e3b8c978`  
		Last Modified: Tue, 29 Apr 2025 00:20:42 GMT  
		Size: 198.8 MB (198846097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0` - unknown; unknown

```console
$ docker pull rust@sha256:c28aff946bf6a9641ea9333906292d4bcaca20d9730ac06f65c73b7dbfe00bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91b52445b0f0d88b77d2754a8b302421f4d6c97b7cb7d4de220050178066182`

```dockerfile
```

-	Layers:
	-	`sha256:b79e6f075844c12dfa724e6e05d0844d5de320465830dbb322f023f18d80c8fc`  
		Last Modified: Tue, 29 Apr 2025 00:20:37 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49427446706d8a35b3d9da8f7db167c3935e0225c64c41163ace92f38a50fb6`  
		Last Modified: Tue, 29 Apr 2025 00:20:36 GMT  
		Size: 13.1 KB (13137 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff3403ae6581adf67c0bbde3bcab29a147bf80f4392ab0af5dbed3377c1e119b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542266054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3698017437d2ae8077abed8488d38727dc5dba1f88e48876e5d3733f532a6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5414268749270f000845caf5689fb7740534b9fe922712301ba571a6afca96`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 59.6 MB (59639425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd5426bd57bea2caac0e0e87b98c0988fb39decb07637e76311bc28b01e6b7`  
		Last Modified: Tue, 08 Apr 2025 20:34:20 GMT  
		Size: 175.3 MB (175297229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093acd39fc465167a3795c75afa1eb7603459d1e396309304795a5c261b5a699`  
		Last Modified: Wed, 09 Apr 2025 03:31:38 GMT  
		Size: 241.2 MB (241214386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0` - unknown; unknown

```console
$ docker pull rust@sha256:965b9904c21bcd441911c4b25119ecca1e3f2fba0c3ab636faf4e528fc89a355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15289059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ac2dfec33d3f464c032fb6c8ec95b36285cdc7aca6e1012458969150a6d286`

```dockerfile
```

-	Layers:
	-	`sha256:69935c7f7900e361aabe717ea482ce229c0f4290d1f011ce1e508dba7b96a093`  
		Last Modified: Wed, 09 Apr 2025 03:31:32 GMT  
		Size: 15.3 MB (15275812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd85c681d8a8c03f05a9c034397cd1615a023bca10a054649801c9a54062374`  
		Last Modified: Wed, 09 Apr 2025 03:31:31 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0a27f7509b3def95327fe3735084c6a475bb52054efee7316d84fd91fc17736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506611045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee291f151e5b030a604f543d9a5c4541b96d0e637888a2a09334bd826322ab1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002e18bd5659ca9d155e99922678788bec836a3ac4964d8a9567ce59e2154de9`  
		Last Modified: Tue, 08 Apr 2025 15:52:42 GMT  
		Size: 202.7 MB (202735307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775439c6d731e711d1e42014fd69218e477c0c43221098e6d1513428f9946240`  
		Last Modified: Tue, 08 Apr 2025 21:32:10 GMT  
		Size: 167.6 MB (167648150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0` - unknown; unknown

```console
$ docker pull rust@sha256:63403d5c50b5086ee37972bd4ddb3dac08ba9444f59ed275e4639aa2c44c5c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e9f0697f2a2efe50253e36a3bc474bac40598a69515a99e7596cbf41d4c034`

```dockerfile
```

-	Layers:
	-	`sha256:2af08bf3572f4cd46f60afd036e4b1bf91b775e6c09a6bf6295ec9afbec238bf`  
		Last Modified: Tue, 08 Apr 2025 21:32:07 GMT  
		Size: 15.5 MB (15499945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32389045ed63fed52cb8d7ec269d8b4a0e5421639eb6f7906eba095d4d5d1e64`  
		Last Modified: Tue, 08 Apr 2025 21:32:06 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0` - linux; 386

```console
$ docker pull rust@sha256:69531fcb8a67b072bfc78f893d76a5d5c5a325536a4f948493f5fae1756d4019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572991948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f4ce1664011b7b08cabc2bcb040af4431dd6da7fff8a55460b8c4e9fd01a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Mon, 28 Apr 2025 21:53:42 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce8929d56fab56325a8eea211cb4cd1021bc6ffc1e7a794d505ddbe638b23cd`  
		Last Modified: Mon, 28 Apr 2025 22:15:00 GMT  
		Size: 66.2 MB (66228922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1528cc13747bb103866d00332de43f9304156fef5a2f396b15d9e173b1365f5`  
		Last Modified: Mon, 28 Apr 2025 23:13:00 GMT  
		Size: 210.3 MB (210293092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a0a0e26e85220e6482bcf2859ccd19dc889d8c6237381e13a52446ce56f374`  
		Last Modified: Tue, 29 Apr 2025 00:19:10 GMT  
		Size: 222.1 MB (222144215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0` - unknown; unknown

```console
$ docker pull rust@sha256:e26a24e515fc29bea5fb4ad97d93055e97736137dbbff6c0a66d1e3cb662a266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2a0d93c03f13377ffa686d882edf0901118adbaeea959c691a9dc76256ea5b`

```dockerfile
```

-	Layers:
	-	`sha256:38affa8290df1776c35aab78bc46e1491c5b3a525152f3b1e737e46e6456d55e`  
		Last Modified: Tue, 29 Apr 2025 00:19:06 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04d9a14a26e0b8792115fbad3c25692abd8c3ea50dc544ff6954cc8a9d3b12ab`  
		Last Modified: Tue, 29 Apr 2025 00:19:05 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0` - linux; ppc64le

```console
$ docker pull rust@sha256:6ff43004246ac7409ecbc3cf1d1f64fe97af549cff6e4eeffb347c53123695c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628715675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52ec6298460494f48ebd94562ccdc697dcc3bb3d3915515c744d5def51728ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675af5e5720aa9e9d4f74b056a7b58aa0a84a5b3cc2c23272c361e473b9c5b8`  
		Last Modified: Tue, 08 Apr 2025 15:34:04 GMT  
		Size: 214.4 MB (214387209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fd4fb10062d551eeb2e024d3e563728a42549e867f8f166eb7d3c22b7d6b78`  
		Last Modified: Tue, 08 Apr 2025 19:25:14 GMT  
		Size: 266.5 MB (266502721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0` - unknown; unknown

```console
$ docker pull rust@sha256:c47a89a1025ff4dbb33264cf2765a8e1e0c24ff47135d1b6c7c7e977468d89e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15459677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7827834152d2d52c8fbc16a215bf024a151d424dffb4ab149188341b0cc1f14`

```dockerfile
```

-	Layers:
	-	`sha256:23ddb56e82f0fa073703d355e296183384c1fc63c0b493b2a1bac0b20c353294`  
		Last Modified: Tue, 08 Apr 2025 19:25:07 GMT  
		Size: 15.4 MB (15446470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfcaa31a08c5def654ca430c6b47811b40f07fd5cbdfd2e94e2fb98d08e77e8`  
		Last Modified: Tue, 08 Apr 2025 19:25:06 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0` - linux; s390x

```console
$ docker pull rust@sha256:aaf804c60805de2a84400664811dd543e7a735e684976c5b4ac22ea1ae537910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611949825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f71016804f1861e6054a214aea01f56260a9f54e32cde4b102889b5ba38c3b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fde99ce0eec506f038695c59ba0ff56bd0df358636c0b067f55c60d7d566c`  
		Last Modified: Tue, 08 Apr 2025 06:52:25 GMT  
		Size: 63.5 MB (63498375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766d2c4791b14ffb813f2bd4d87d95e9030a5939b65f31722bc2c223f845ecf8`  
		Last Modified: Tue, 08 Apr 2025 10:02:09 GMT  
		Size: 183.4 MB (183388438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eb0c69619b19f87369d4a1737b46098625d76f72f75d41c18ecc2b9f8019cc`  
		Last Modified: Tue, 08 Apr 2025 18:17:17 GMT  
		Size: 293.9 MB (293903680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0` - unknown; unknown

```console
$ docker pull rust@sha256:21d031f77b8b2c841a56916b430442b3dbbfd340d1aadee3bf1561f97999cc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15297196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49e7c039c53b210b5e3cfc85ca1eb9fcaa5480271c4f2b0c5e5e6aa37781915`

```dockerfile
```

-	Layers:
	-	`sha256:0d2bad61871ee6c24e5ae84182871a58c88b6f3593a3f0a381f6236eec0606e9`  
		Last Modified: Tue, 08 Apr 2025 18:17:08 GMT  
		Size: 15.3 MB (15284058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1589d850c8b322cdebed632bcf0d29ee300ca793b83044f540479e4b39431e1`  
		Last Modified: Tue, 08 Apr 2025 18:17:07 GMT  
		Size: 13.1 KB (13138 bytes)  
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
$ docker pull rust@sha256:ff735b1f09be7bb43d0ceece3d6f03b877292ae0307e35b32f75165a05d574c5
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
$ docker pull rust@sha256:f163d1a53e6d105d037f8798f47f7947c062671bfb8d4485c612a1d00a3cbf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547098954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209b88fdf20bcc777094ee4ff43efc6ef043406c3a4c169785eda17fecc6318c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187b51b626e1d60ab369727b81f440adea9d45e97a45e137fc318be0bb7f09f`  
		Last Modified: Mon, 28 Apr 2025 23:12:20 GMT  
		Size: 211.4 MB (211356050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa897cd1d909c6f9aeeb2eb86f8281d7f1bd22ec60b937531af70f77e3b8c978`  
		Last Modified: Tue, 29 Apr 2025 00:20:42 GMT  
		Size: 198.8 MB (198846097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c28aff946bf6a9641ea9333906292d4bcaca20d9730ac06f65c73b7dbfe00bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91b52445b0f0d88b77d2754a8b302421f4d6c97b7cb7d4de220050178066182`

```dockerfile
```

-	Layers:
	-	`sha256:b79e6f075844c12dfa724e6e05d0844d5de320465830dbb322f023f18d80c8fc`  
		Last Modified: Tue, 29 Apr 2025 00:20:37 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49427446706d8a35b3d9da8f7db167c3935e0225c64c41163ace92f38a50fb6`  
		Last Modified: Tue, 29 Apr 2025 00:20:36 GMT  
		Size: 13.1 KB (13137 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff3403ae6581adf67c0bbde3bcab29a147bf80f4392ab0af5dbed3377c1e119b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542266054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3698017437d2ae8077abed8488d38727dc5dba1f88e48876e5d3733f532a6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5414268749270f000845caf5689fb7740534b9fe922712301ba571a6afca96`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 59.6 MB (59639425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd5426bd57bea2caac0e0e87b98c0988fb39decb07637e76311bc28b01e6b7`  
		Last Modified: Tue, 08 Apr 2025 20:34:20 GMT  
		Size: 175.3 MB (175297229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093acd39fc465167a3795c75afa1eb7603459d1e396309304795a5c261b5a699`  
		Last Modified: Wed, 09 Apr 2025 03:31:38 GMT  
		Size: 241.2 MB (241214386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:965b9904c21bcd441911c4b25119ecca1e3f2fba0c3ab636faf4e528fc89a355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15289059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ac2dfec33d3f464c032fb6c8ec95b36285cdc7aca6e1012458969150a6d286`

```dockerfile
```

-	Layers:
	-	`sha256:69935c7f7900e361aabe717ea482ce229c0f4290d1f011ce1e508dba7b96a093`  
		Last Modified: Wed, 09 Apr 2025 03:31:32 GMT  
		Size: 15.3 MB (15275812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd85c681d8a8c03f05a9c034397cd1615a023bca10a054649801c9a54062374`  
		Last Modified: Wed, 09 Apr 2025 03:31:31 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0a27f7509b3def95327fe3735084c6a475bb52054efee7316d84fd91fc17736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506611045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee291f151e5b030a604f543d9a5c4541b96d0e637888a2a09334bd826322ab1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002e18bd5659ca9d155e99922678788bec836a3ac4964d8a9567ce59e2154de9`  
		Last Modified: Tue, 08 Apr 2025 15:52:42 GMT  
		Size: 202.7 MB (202735307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775439c6d731e711d1e42014fd69218e477c0c43221098e6d1513428f9946240`  
		Last Modified: Tue, 08 Apr 2025 21:32:10 GMT  
		Size: 167.6 MB (167648150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:63403d5c50b5086ee37972bd4ddb3dac08ba9444f59ed275e4639aa2c44c5c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e9f0697f2a2efe50253e36a3bc474bac40598a69515a99e7596cbf41d4c034`

```dockerfile
```

-	Layers:
	-	`sha256:2af08bf3572f4cd46f60afd036e4b1bf91b775e6c09a6bf6295ec9afbec238bf`  
		Last Modified: Tue, 08 Apr 2025 21:32:07 GMT  
		Size: 15.5 MB (15499945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32389045ed63fed52cb8d7ec269d8b4a0e5421639eb6f7906eba095d4d5d1e64`  
		Last Modified: Tue, 08 Apr 2025 21:32:06 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bookworm` - linux; 386

```console
$ docker pull rust@sha256:69531fcb8a67b072bfc78f893d76a5d5c5a325536a4f948493f5fae1756d4019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572991948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f4ce1664011b7b08cabc2bcb040af4431dd6da7fff8a55460b8c4e9fd01a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Mon, 28 Apr 2025 21:53:42 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce8929d56fab56325a8eea211cb4cd1021bc6ffc1e7a794d505ddbe638b23cd`  
		Last Modified: Mon, 28 Apr 2025 22:15:00 GMT  
		Size: 66.2 MB (66228922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1528cc13747bb103866d00332de43f9304156fef5a2f396b15d9e173b1365f5`  
		Last Modified: Mon, 28 Apr 2025 23:13:00 GMT  
		Size: 210.3 MB (210293092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a0a0e26e85220e6482bcf2859ccd19dc889d8c6237381e13a52446ce56f374`  
		Last Modified: Tue, 29 Apr 2025 00:19:10 GMT  
		Size: 222.1 MB (222144215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e26a24e515fc29bea5fb4ad97d93055e97736137dbbff6c0a66d1e3cb662a266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2a0d93c03f13377ffa686d882edf0901118adbaeea959c691a9dc76256ea5b`

```dockerfile
```

-	Layers:
	-	`sha256:38affa8290df1776c35aab78bc46e1491c5b3a525152f3b1e737e46e6456d55e`  
		Last Modified: Tue, 29 Apr 2025 00:19:06 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04d9a14a26e0b8792115fbad3c25692abd8c3ea50dc544ff6954cc8a9d3b12ab`  
		Last Modified: Tue, 29 Apr 2025 00:19:05 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:6ff43004246ac7409ecbc3cf1d1f64fe97af549cff6e4eeffb347c53123695c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628715675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52ec6298460494f48ebd94562ccdc697dcc3bb3d3915515c744d5def51728ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675af5e5720aa9e9d4f74b056a7b58aa0a84a5b3cc2c23272c361e473b9c5b8`  
		Last Modified: Tue, 08 Apr 2025 15:34:04 GMT  
		Size: 214.4 MB (214387209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fd4fb10062d551eeb2e024d3e563728a42549e867f8f166eb7d3c22b7d6b78`  
		Last Modified: Tue, 08 Apr 2025 19:25:14 GMT  
		Size: 266.5 MB (266502721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c47a89a1025ff4dbb33264cf2765a8e1e0c24ff47135d1b6c7c7e977468d89e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15459677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7827834152d2d52c8fbc16a215bf024a151d424dffb4ab149188341b0cc1f14`

```dockerfile
```

-	Layers:
	-	`sha256:23ddb56e82f0fa073703d355e296183384c1fc63c0b493b2a1bac0b20c353294`  
		Last Modified: Tue, 08 Apr 2025 19:25:07 GMT  
		Size: 15.4 MB (15446470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfcaa31a08c5def654ca430c6b47811b40f07fd5cbdfd2e94e2fb98d08e77e8`  
		Last Modified: Tue, 08 Apr 2025 19:25:06 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:aaf804c60805de2a84400664811dd543e7a735e684976c5b4ac22ea1ae537910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611949825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f71016804f1861e6054a214aea01f56260a9f54e32cde4b102889b5ba38c3b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fde99ce0eec506f038695c59ba0ff56bd0df358636c0b067f55c60d7d566c`  
		Last Modified: Tue, 08 Apr 2025 06:52:25 GMT  
		Size: 63.5 MB (63498375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766d2c4791b14ffb813f2bd4d87d95e9030a5939b65f31722bc2c223f845ecf8`  
		Last Modified: Tue, 08 Apr 2025 10:02:09 GMT  
		Size: 183.4 MB (183388438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eb0c69619b19f87369d4a1737b46098625d76f72f75d41c18ecc2b9f8019cc`  
		Last Modified: Tue, 08 Apr 2025 18:17:17 GMT  
		Size: 293.9 MB (293903680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:21d031f77b8b2c841a56916b430442b3dbbfd340d1aadee3bf1561f97999cc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15297196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49e7c039c53b210b5e3cfc85ca1eb9fcaa5480271c4f2b0c5e5e6aa37781915`

```dockerfile
```

-	Layers:
	-	`sha256:0d2bad61871ee6c24e5ae84182871a58c88b6f3593a3f0a381f6236eec0606e9`  
		Last Modified: Tue, 08 Apr 2025 18:17:08 GMT  
		Size: 15.3 MB (15284058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1589d850c8b322cdebed632bcf0d29ee300ca793b83044f540479e4b39431e1`  
		Last Modified: Tue, 08 Apr 2025 18:17:07 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0-bullseye`

```console
$ docker pull rust@sha256:eea163213169a83a58a975c16c59d71e344d9932f663cb850735e57d04e3a78d
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
$ docker pull rust@sha256:8c271c0f0dcb01fa63c88f6dea15e7bc3635576f84d26032170faac2d52a4e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.2 MB (520220542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15453801e070ee0e2545d6aacd3ede9512be0950202af0ba7e0521e3dab5a657`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Mon, 28 Apr 2025 22:15:30 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee2c8b84461fce714721ac74cb275f6aaa0de67c2aeaccb8193af9ea8b4d38`  
		Last Modified: Mon, 28 Apr 2025 23:12:29 GMT  
		Size: 197.1 MB (197107708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9066c54499afbbfd0cbc1d4f2a3e1de04f748f13531dffada1a0c61dfd36453f`  
		Last Modified: Tue, 29 Apr 2025 00:47:26 GMT  
		Size: 198.8 MB (198845544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:21a84938f50b45e05ce5cbb41e4714dbe3e866640e145d22188429f356ad4429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15086862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147b76c7800402cd7050842d3c7612cbc837d0bcf39d2b64d87d5990349a9f4a`

```dockerfile
```

-	Layers:
	-	`sha256:53a2905058c19fa7e018208b2351a1b70af430d00b6b1d6d32c52729ebd558c8`  
		Last Modified: Tue, 29 Apr 2025 00:47:24 GMT  
		Size: 15.1 MB (15075615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f89f6d37e15f2c84bf3a2d0edb1030882e2d1ee819bbdb8e39c702b9227c86ce`  
		Last Modified: Tue, 29 Apr 2025 00:47:23 GMT  
		Size: 11.2 KB (11247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:ed129955a5f1efbd8557d1c3d3ed9ae637d9adbf423c79a29dfe2a6779254295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.3 MB (523310260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b42a94efe835df3c1ee60011feb7bec025b4df5f862b615031133e68d2a3b0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
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
	-	`sha256:8c2fc9e6d23f3debfa68416a2b96331b92d563b20272933315ecfbbada38e955`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 49.0 MB (49031449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525b68fed12d763a57f1b020aa1579673112de80a5b780b5ffaa045109c81f23`  
		Last Modified: Tue, 08 Apr 2025 07:38:26 GMT  
		Size: 14.9 MB (14878713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909681b45fdfcbd0bfebc28d96cd1bdab32fd85e3af6788b49d9cb80e8ff865a`  
		Last Modified: Tue, 08 Apr 2025 17:30:33 GMT  
		Size: 50.6 MB (50624452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ae4904ff46404ac5bb348da93b4e4f750b89ecaf468fd2f4b669038dc51cfb`  
		Last Modified: Tue, 08 Apr 2025 20:36:13 GMT  
		Size: 167.6 MB (167560460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9324aa48468359b44400cdd12929b0da8d31a43b594b8361c6a6eb9c9252c1`  
		Last Modified: Wed, 09 Apr 2025 03:29:40 GMT  
		Size: 241.2 MB (241215186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:28192187a807cc51ff78c007c700090895505aa9bbcb1e554e1e887bec3c50d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14887676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb595f8ced635b06fcf9a61717b019b48d031bc466e3a6ee8dd2439c17103dd5`

```dockerfile
```

-	Layers:
	-	`sha256:7c157d370bd0a5868efeec965f7bdab7d6202c55ade93b51998737e616cdb623`  
		Last Modified: Wed, 09 Apr 2025 03:29:36 GMT  
		Size: 14.9 MB (14876352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6557cfe726aaf265db580bb9f6cf75eb3c19cab87774acfaa4183ba88ac1a943`  
		Last Modified: Wed, 09 Apr 2025 03:29:34 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:09a7f7dcc5882af5bbccc6dc2d269e4ad12b8614dd251c3aabfc4f7411b0f8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.5 MB (480522553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7757be1da64936c13a88161dfcf370ffdc62353fd997f8283cbce57cbe1ca3b1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322dad1d7c942b6794e486e4e0b838c10dfb06247f1794d20cc703ddfee969f`  
		Last Modified: Tue, 08 Apr 2025 06:03:40 GMT  
		Size: 15.7 MB (15749086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebaef8f9f6ff21c71a0e336a0e9a00fbb65d469480593ef8d1ef507941e6f6d`  
		Last Modified: Tue, 08 Apr 2025 12:18:43 GMT  
		Size: 54.9 MB (54850009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848ef88a118038c35ad53e6bc0e94192e99b916044a11fb61a40b31c77edc820`  
		Last Modified: Tue, 08 Apr 2025 15:54:19 GMT  
		Size: 190.0 MB (190022174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d5d165da97b462feba12c3696936055a7ddb81249fd994f73056e2bbb08d5f`  
		Last Modified: Tue, 08 Apr 2025 21:31:15 GMT  
		Size: 167.6 MB (167647062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d112402618f4d6f27648b816c07a25745eb4d79aa34ea481f96aac9ed675a320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15089174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a8450527599dfb60c80da9bb3f35748ff58ac969abe44738329c168e8195b1`

```dockerfile
```

-	Layers:
	-	`sha256:22c68f5deda14220e1d89c790721da688dcdd27e932e2f7e33e3734a63d2ab4d`  
		Last Modified: Tue, 08 Apr 2025 21:31:11 GMT  
		Size: 15.1 MB (15077821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ca44f0d2397d24f0dbb2d7aafc86c60976ef147f078230b9734ce5418cc0f8`  
		Last Modified: Tue, 08 Apr 2025 21:31:10 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-bullseye` - linux; 386

```console
$ docker pull rust@sha256:9cbc7bd302c43e0a62cdb858f9c24a58b87aca7bf043ffab7cb079d4d5770139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549153535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3ace1c51d4464391099c6feb9831aed5ef6fd61345c2f970e108a016c5ebee`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
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
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb48ef4c334135b55fe5dd328911059bfd41eec15edf03ff0ab96ca44fb6a1`  
		Last Modified: Mon, 28 Apr 2025 21:53:52 GMT  
		Size: 16.3 MB (16267399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f9ff435d5a831802e386be1d29f22419a5d3951a76711fcdfc9f9bad0e6e3`  
		Last Modified: Mon, 28 Apr 2025 22:14:52 GMT  
		Size: 56.0 MB (56047280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ef040f15a9c521f9352beaf246f79eec04035acb8b716f343f27a2aea49563`  
		Last Modified: Mon, 28 Apr 2025 23:12:49 GMT  
		Size: 200.0 MB (200011534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84444c00c33828bec847a0ebe02cdf86e4a38c359cd763bbab9e70a5c8548f42`  
		Last Modified: Tue, 29 Apr 2025 00:17:33 GMT  
		Size: 222.1 MB (222144220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a2265636dfa483bc6134f1471d3440d26019c187f2e845c84c8ab33248f5d8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15073859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65970c74d4efc0b684a893fd52a296fbf9af95f404deca1b28741c80dbc4580`

```dockerfile
```

-	Layers:
	-	`sha256:a255f8f56087be5473d5e5866f9da323ec16bcb91c91c88845c86ba78c4f2fe4`  
		Last Modified: Tue, 29 Apr 2025 00:17:28 GMT  
		Size: 15.1 MB (15062642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973d0dfea887d74ea1652c8a1f21f05a292fbb82170d601ae82d934a72dbc336`  
		Last Modified: Tue, 29 Apr 2025 00:17:27 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0-slim`

```console
$ docker pull rust@sha256:3deccec2419f46f7052356d99e0c76ceba02a0164a45e1c5894481a4785e7895
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
$ docker pull rust@sha256:5265cf7f0324e5af0d0af625952b426cfaf5fc6daafd79b1fdedac07bd69b999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297830650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7f574507b85a8cc381daab85fd042918977aa4e469b8c0b3adca5ebbf2f53d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d2c2c6f222aae0625c61e9d3f36afe3bd17ebed1d2eb21f1bf888d76a5d60b`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
		Size: 269.6 MB (269603008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:19dd7a17f1dc76c4e00c549b877018bc870343a6ecbc8ef68fe7946a84a356d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f410651604a0a715d015565863b7efe3c81dcf3da755fb9cf24f7a5237556b`

```dockerfile
```

-	Layers:
	-	`sha256:ff862d7e48c414c8bb95d3a1388b734c191baea434a62085f4346713d401770d`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675eae4d6651df312a550a92c9e8941bcaedafe4f550de7cad9f475791b9a3b0`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
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
$ docker pull rust@sha256:9b4588a9375c6c2a2a7454768c282c8e549784b521eb0c5ea3e32d7568affed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318922232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4afab512f48e1dfcccdf517247ac52f880b84fd820a0b2d4949efd3c0301d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f7195df9fd10fb92d71646b4d86321f170c6c731039dd4e34938be58f58cb9`  
		Last Modified: Mon, 28 Apr 2025 21:59:24 GMT  
		Size: 289.7 MB (289711366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:51adece521582dbdc49671e0fbe582c8e8a6789f6274dc195eeee01c43cc3705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0b4b1a80ee612bf4ae7a0cf824e5305b3644dbae73ef8d0d8d832945a7b784`

```dockerfile
```

-	Layers:
	-	`sha256:0cf266b3c804c8acfcb96fe5b018f864f17e2d3be0b00960512021e7dedea803`  
		Last Modified: Mon, 28 Apr 2025 21:59:18 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a2e0dd93e9a6d69a21bdeb2e6d7d8350d6e6bd032336a2c1593141e3d80c57`  
		Last Modified: Mon, 28 Apr 2025 21:59:17 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:e5aeefd41ca6f9abd02b12460157ca851369b314458f653836b6041460b89818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367336038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84bea10cf021c1602244cf068230d973768342a4cd724e0c3118bfae5cfa97`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c04e3602592a873e00fef80b178c6583f85417553600599ea8e1e61736cad8`  
		Last Modified: Tue, 29 Apr 2025 03:38:35 GMT  
		Size: 335.3 MB (335267595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:f23567e86bb567602fbd3b97382d2e63737d1c041296ed7e66094cf7711c5063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c1b4c721edb518831b46540fa64acf0c3efa8d91e5d44979f23bf0a9e5a60a`

```dockerfile
```

-	Layers:
	-	`sha256:d780a892b067eb8a87aeba5b1ddc996252fb597316ab13515b746c3bdf531ef0`  
		Last Modified: Tue, 29 Apr 2025 03:38:27 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:188d119007c4e10172952ad43483211958e15eddcf785427c58e34052df76afa`  
		Last Modified: Tue, 29 Apr 2025 03:38:26 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim` - linux; s390x

```console
$ docker pull rust@sha256:cd75cace871d1241847f08379dfd7b2913730d65f88736c71cd4073eebc53b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e951356ca72c6d32f55a1a349ce8e5030b100b4da94dd52e05829406fd63a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5365383afac604f9c2f2ab1254332b6835b90d820e7e3d14137a8ab8bd5f849`  
		Last Modified: Tue, 29 Apr 2025 02:34:37 GMT  
		Size: 344.0 MB (344011014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3fd3ab8f79e47636e149395239ceb7c46785b04e3f66d11d2b3645c2e0c130a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ab2946a315baa636e061bf47c4e0d08f33e4e452ee0dd0dbabb4c8cd56d7c5`

```dockerfile
```

-	Layers:
	-	`sha256:89ea65b28be4d0e2d05e9cd9e7b13b402be9f781990fc713eeb4ac680fee4ed0`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d046b9ce46b62be8c69446342f660b1449e172e7dfa84284fa1c4242cb3b348a`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0-slim-bookworm`

```console
$ docker pull rust@sha256:3deccec2419f46f7052356d99e0c76ceba02a0164a45e1c5894481a4785e7895
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
$ docker pull rust@sha256:5265cf7f0324e5af0d0af625952b426cfaf5fc6daafd79b1fdedac07bd69b999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297830650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7f574507b85a8cc381daab85fd042918977aa4e469b8c0b3adca5ebbf2f53d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d2c2c6f222aae0625c61e9d3f36afe3bd17ebed1d2eb21f1bf888d76a5d60b`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
		Size: 269.6 MB (269603008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:19dd7a17f1dc76c4e00c549b877018bc870343a6ecbc8ef68fe7946a84a356d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f410651604a0a715d015565863b7efe3c81dcf3da755fb9cf24f7a5237556b`

```dockerfile
```

-	Layers:
	-	`sha256:ff862d7e48c414c8bb95d3a1388b734c191baea434a62085f4346713d401770d`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675eae4d6651df312a550a92c9e8941bcaedafe4f550de7cad9f475791b9a3b0`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
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
$ docker pull rust@sha256:9b4588a9375c6c2a2a7454768c282c8e549784b521eb0c5ea3e32d7568affed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318922232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4afab512f48e1dfcccdf517247ac52f880b84fd820a0b2d4949efd3c0301d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f7195df9fd10fb92d71646b4d86321f170c6c731039dd4e34938be58f58cb9`  
		Last Modified: Mon, 28 Apr 2025 21:59:24 GMT  
		Size: 289.7 MB (289711366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:51adece521582dbdc49671e0fbe582c8e8a6789f6274dc195eeee01c43cc3705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0b4b1a80ee612bf4ae7a0cf824e5305b3644dbae73ef8d0d8d832945a7b784`

```dockerfile
```

-	Layers:
	-	`sha256:0cf266b3c804c8acfcb96fe5b018f864f17e2d3be0b00960512021e7dedea803`  
		Last Modified: Mon, 28 Apr 2025 21:59:18 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a2e0dd93e9a6d69a21bdeb2e6d7d8350d6e6bd032336a2c1593141e3d80c57`  
		Last Modified: Mon, 28 Apr 2025 21:59:17 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:e5aeefd41ca6f9abd02b12460157ca851369b314458f653836b6041460b89818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367336038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84bea10cf021c1602244cf068230d973768342a4cd724e0c3118bfae5cfa97`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c04e3602592a873e00fef80b178c6583f85417553600599ea8e1e61736cad8`  
		Last Modified: Tue, 29 Apr 2025 03:38:35 GMT  
		Size: 335.3 MB (335267595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f23567e86bb567602fbd3b97382d2e63737d1c041296ed7e66094cf7711c5063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c1b4c721edb518831b46540fa64acf0c3efa8d91e5d44979f23bf0a9e5a60a`

```dockerfile
```

-	Layers:
	-	`sha256:d780a892b067eb8a87aeba5b1ddc996252fb597316ab13515b746c3bdf531ef0`  
		Last Modified: Tue, 29 Apr 2025 03:38:27 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:188d119007c4e10172952ad43483211958e15eddcf785427c58e34052df76afa`  
		Last Modified: Tue, 29 Apr 2025 03:38:26 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.86.0-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:cd75cace871d1241847f08379dfd7b2913730d65f88736c71cd4073eebc53b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e951356ca72c6d32f55a1a349ce8e5030b100b4da94dd52e05829406fd63a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5365383afac604f9c2f2ab1254332b6835b90d820e7e3d14137a8ab8bd5f849`  
		Last Modified: Tue, 29 Apr 2025 02:34:37 GMT  
		Size: 344.0 MB (344011014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3fd3ab8f79e47636e149395239ceb7c46785b04e3f66d11d2b3645c2e0c130a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ab2946a315baa636e061bf47c4e0d08f33e4e452ee0dd0dbabb4c8cd56d7c5`

```dockerfile
```

-	Layers:
	-	`sha256:89ea65b28be4d0e2d05e9cd9e7b13b402be9f781990fc713eeb4ac680fee4ed0`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d046b9ce46b62be8c69446342f660b1449e172e7dfa84284fa1c4242cb3b348a`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.86.0-slim-bullseye`

```console
$ docker pull rust@sha256:8b4fb6e91904117e77ff7fb19d63dc83c6f1ed3caa7915b9390e5380b19cb55d
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
$ docker pull rust@sha256:61200dad758eb2c4e99313d0c6782e7fa89311bd83c94b9bc39bc01948f587db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289241682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25e74260d87c5fa7492be92ca0677a11a991844226d26af85a21722fe8fd4dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0797f92ce1279f464536d8c0af7023351ee2e207ccec21fe543d01eb4c4248`  
		Last Modified: Mon, 28 Apr 2025 22:05:28 GMT  
		Size: 259.0 MB (258987078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1836529f3ca5bc812985db92eb733b1bccd994105d29fded97d9d61adea71be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e36b0a70ce16003c9069f2825bd02e341920e739a895f46f2a469f7a79fd07`

```dockerfile
```

-	Layers:
	-	`sha256:13123c2d58f95072da02ee8e10ac5a44b16d4f6545106822ca9f98b7eee11c9c`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
		Size: 4.2 MB (4175178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4758d2f11990f0f5dceffd56dc922a42f33a2fb2873222c6bc096a6c1cb942`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
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
$ docker pull rust@sha256:091710edd306bd2bf84340d1127b91227bc8fa29f7e37ba0036ec2686cd16113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314101243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd162dda1171190a0aa571d0efa79d256bae0efec08e9afdc2e79c38754466a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:73bb1b80ecf1f8784ad6f92a35120b6e2306657fc7e8cbaedca1f45900f3d746`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 31.2 MB (31187893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e304cb55c66d1a5edc35eacf691a84c62d770f1198d127335959a3166eeb088`  
		Last Modified: Mon, 28 Apr 2025 21:58:49 GMT  
		Size: 282.9 MB (282913350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.86.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4a0423225bb2de1faea503c48c34dce51dc7696d8c40f13d16e30180c1c91ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ef654c9879524c59c0bf60a53ef350537343ebe309bf9fa7371daa378cec71`

```dockerfile
```

-	Layers:
	-	`sha256:acd11de69428b51d1eeb16ee8532107d4b7f03aa5deb5323de965df13bf84155`  
		Last Modified: Mon, 28 Apr 2025 21:58:43 GMT  
		Size: 4.2 MB (4165435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58625db462ea2607636281f9a865fc50b768ee088febe47023718de82b41b7e4`  
		Last Modified: Mon, 28 Apr 2025 21:58:42 GMT  
		Size: 11.3 KB (11323 bytes)  
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
$ docker pull rust@sha256:ff735b1f09be7bb43d0ceece3d6f03b877292ae0307e35b32f75165a05d574c5
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
$ docker pull rust@sha256:f163d1a53e6d105d037f8798f47f7947c062671bfb8d4485c612a1d00a3cbf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547098954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209b88fdf20bcc777094ee4ff43efc6ef043406c3a4c169785eda17fecc6318c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187b51b626e1d60ab369727b81f440adea9d45e97a45e137fc318be0bb7f09f`  
		Last Modified: Mon, 28 Apr 2025 23:12:20 GMT  
		Size: 211.4 MB (211356050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa897cd1d909c6f9aeeb2eb86f8281d7f1bd22ec60b937531af70f77e3b8c978`  
		Last Modified: Tue, 29 Apr 2025 00:20:42 GMT  
		Size: 198.8 MB (198846097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c28aff946bf6a9641ea9333906292d4bcaca20d9730ac06f65c73b7dbfe00bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91b52445b0f0d88b77d2754a8b302421f4d6c97b7cb7d4de220050178066182`

```dockerfile
```

-	Layers:
	-	`sha256:b79e6f075844c12dfa724e6e05d0844d5de320465830dbb322f023f18d80c8fc`  
		Last Modified: Tue, 29 Apr 2025 00:20:37 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49427446706d8a35b3d9da8f7db167c3935e0225c64c41163ace92f38a50fb6`  
		Last Modified: Tue, 29 Apr 2025 00:20:36 GMT  
		Size: 13.1 KB (13137 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff3403ae6581adf67c0bbde3bcab29a147bf80f4392ab0af5dbed3377c1e119b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542266054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3698017437d2ae8077abed8488d38727dc5dba1f88e48876e5d3733f532a6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5414268749270f000845caf5689fb7740534b9fe922712301ba571a6afca96`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 59.6 MB (59639425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd5426bd57bea2caac0e0e87b98c0988fb39decb07637e76311bc28b01e6b7`  
		Last Modified: Tue, 08 Apr 2025 20:34:20 GMT  
		Size: 175.3 MB (175297229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093acd39fc465167a3795c75afa1eb7603459d1e396309304795a5c261b5a699`  
		Last Modified: Wed, 09 Apr 2025 03:31:38 GMT  
		Size: 241.2 MB (241214386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:965b9904c21bcd441911c4b25119ecca1e3f2fba0c3ab636faf4e528fc89a355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15289059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ac2dfec33d3f464c032fb6c8ec95b36285cdc7aca6e1012458969150a6d286`

```dockerfile
```

-	Layers:
	-	`sha256:69935c7f7900e361aabe717ea482ce229c0f4290d1f011ce1e508dba7b96a093`  
		Last Modified: Wed, 09 Apr 2025 03:31:32 GMT  
		Size: 15.3 MB (15275812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd85c681d8a8c03f05a9c034397cd1615a023bca10a054649801c9a54062374`  
		Last Modified: Wed, 09 Apr 2025 03:31:31 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0a27f7509b3def95327fe3735084c6a475bb52054efee7316d84fd91fc17736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506611045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee291f151e5b030a604f543d9a5c4541b96d0e637888a2a09334bd826322ab1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002e18bd5659ca9d155e99922678788bec836a3ac4964d8a9567ce59e2154de9`  
		Last Modified: Tue, 08 Apr 2025 15:52:42 GMT  
		Size: 202.7 MB (202735307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775439c6d731e711d1e42014fd69218e477c0c43221098e6d1513428f9946240`  
		Last Modified: Tue, 08 Apr 2025 21:32:10 GMT  
		Size: 167.6 MB (167648150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:63403d5c50b5086ee37972bd4ddb3dac08ba9444f59ed275e4639aa2c44c5c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e9f0697f2a2efe50253e36a3bc474bac40598a69515a99e7596cbf41d4c034`

```dockerfile
```

-	Layers:
	-	`sha256:2af08bf3572f4cd46f60afd036e4b1bf91b775e6c09a6bf6295ec9afbec238bf`  
		Last Modified: Tue, 08 Apr 2025 21:32:07 GMT  
		Size: 15.5 MB (15499945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32389045ed63fed52cb8d7ec269d8b4a0e5421639eb6f7906eba095d4d5d1e64`  
		Last Modified: Tue, 08 Apr 2025 21:32:06 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:69531fcb8a67b072bfc78f893d76a5d5c5a325536a4f948493f5fae1756d4019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572991948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f4ce1664011b7b08cabc2bcb040af4431dd6da7fff8a55460b8c4e9fd01a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Mon, 28 Apr 2025 21:53:42 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce8929d56fab56325a8eea211cb4cd1021bc6ffc1e7a794d505ddbe638b23cd`  
		Last Modified: Mon, 28 Apr 2025 22:15:00 GMT  
		Size: 66.2 MB (66228922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1528cc13747bb103866d00332de43f9304156fef5a2f396b15d9e173b1365f5`  
		Last Modified: Mon, 28 Apr 2025 23:13:00 GMT  
		Size: 210.3 MB (210293092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a0a0e26e85220e6482bcf2859ccd19dc889d8c6237381e13a52446ce56f374`  
		Last Modified: Tue, 29 Apr 2025 00:19:10 GMT  
		Size: 222.1 MB (222144215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e26a24e515fc29bea5fb4ad97d93055e97736137dbbff6c0a66d1e3cb662a266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2a0d93c03f13377ffa686d882edf0901118adbaeea959c691a9dc76256ea5b`

```dockerfile
```

-	Layers:
	-	`sha256:38affa8290df1776c35aab78bc46e1491c5b3a525152f3b1e737e46e6456d55e`  
		Last Modified: Tue, 29 Apr 2025 00:19:06 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04d9a14a26e0b8792115fbad3c25692abd8c3ea50dc544ff6954cc8a9d3b12ab`  
		Last Modified: Tue, 29 Apr 2025 00:19:05 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:6ff43004246ac7409ecbc3cf1d1f64fe97af549cff6e4eeffb347c53123695c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628715675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52ec6298460494f48ebd94562ccdc697dcc3bb3d3915515c744d5def51728ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675af5e5720aa9e9d4f74b056a7b58aa0a84a5b3cc2c23272c361e473b9c5b8`  
		Last Modified: Tue, 08 Apr 2025 15:34:04 GMT  
		Size: 214.4 MB (214387209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fd4fb10062d551eeb2e024d3e563728a42549e867f8f166eb7d3c22b7d6b78`  
		Last Modified: Tue, 08 Apr 2025 19:25:14 GMT  
		Size: 266.5 MB (266502721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c47a89a1025ff4dbb33264cf2765a8e1e0c24ff47135d1b6c7c7e977468d89e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15459677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7827834152d2d52c8fbc16a215bf024a151d424dffb4ab149188341b0cc1f14`

```dockerfile
```

-	Layers:
	-	`sha256:23ddb56e82f0fa073703d355e296183384c1fc63c0b493b2a1bac0b20c353294`  
		Last Modified: Tue, 08 Apr 2025 19:25:07 GMT  
		Size: 15.4 MB (15446470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfcaa31a08c5def654ca430c6b47811b40f07fd5cbdfd2e94e2fb98d08e77e8`  
		Last Modified: Tue, 08 Apr 2025 19:25:06 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:aaf804c60805de2a84400664811dd543e7a735e684976c5b4ac22ea1ae537910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611949825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f71016804f1861e6054a214aea01f56260a9f54e32cde4b102889b5ba38c3b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fde99ce0eec506f038695c59ba0ff56bd0df358636c0b067f55c60d7d566c`  
		Last Modified: Tue, 08 Apr 2025 06:52:25 GMT  
		Size: 63.5 MB (63498375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766d2c4791b14ffb813f2bd4d87d95e9030a5939b65f31722bc2c223f845ecf8`  
		Last Modified: Tue, 08 Apr 2025 10:02:09 GMT  
		Size: 183.4 MB (183388438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eb0c69619b19f87369d4a1737b46098625d76f72f75d41c18ecc2b9f8019cc`  
		Last Modified: Tue, 08 Apr 2025 18:17:17 GMT  
		Size: 293.9 MB (293903680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:21d031f77b8b2c841a56916b430442b3dbbfd340d1aadee3bf1561f97999cc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15297196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49e7c039c53b210b5e3cfc85ca1eb9fcaa5480271c4f2b0c5e5e6aa37781915`

```dockerfile
```

-	Layers:
	-	`sha256:0d2bad61871ee6c24e5ae84182871a58c88b6f3593a3f0a381f6236eec0606e9`  
		Last Modified: Tue, 08 Apr 2025 18:17:08 GMT  
		Size: 15.3 MB (15284058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1589d850c8b322cdebed632bcf0d29ee300ca793b83044f540479e4b39431e1`  
		Last Modified: Tue, 08 Apr 2025 18:17:07 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:eea163213169a83a58a975c16c59d71e344d9932f663cb850735e57d04e3a78d
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
$ docker pull rust@sha256:8c271c0f0dcb01fa63c88f6dea15e7bc3635576f84d26032170faac2d52a4e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.2 MB (520220542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15453801e070ee0e2545d6aacd3ede9512be0950202af0ba7e0521e3dab5a657`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Mon, 28 Apr 2025 22:15:30 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee2c8b84461fce714721ac74cb275f6aaa0de67c2aeaccb8193af9ea8b4d38`  
		Last Modified: Mon, 28 Apr 2025 23:12:29 GMT  
		Size: 197.1 MB (197107708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9066c54499afbbfd0cbc1d4f2a3e1de04f748f13531dffada1a0c61dfd36453f`  
		Last Modified: Tue, 29 Apr 2025 00:47:26 GMT  
		Size: 198.8 MB (198845544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:21a84938f50b45e05ce5cbb41e4714dbe3e866640e145d22188429f356ad4429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15086862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147b76c7800402cd7050842d3c7612cbc837d0bcf39d2b64d87d5990349a9f4a`

```dockerfile
```

-	Layers:
	-	`sha256:53a2905058c19fa7e018208b2351a1b70af430d00b6b1d6d32c52729ebd558c8`  
		Last Modified: Tue, 29 Apr 2025 00:47:24 GMT  
		Size: 15.1 MB (15075615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f89f6d37e15f2c84bf3a2d0edb1030882e2d1ee819bbdb8e39c702b9227c86ce`  
		Last Modified: Tue, 29 Apr 2025 00:47:23 GMT  
		Size: 11.2 KB (11247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:ed129955a5f1efbd8557d1c3d3ed9ae637d9adbf423c79a29dfe2a6779254295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.3 MB (523310260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b42a94efe835df3c1ee60011feb7bec025b4df5f862b615031133e68d2a3b0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
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
	-	`sha256:8c2fc9e6d23f3debfa68416a2b96331b92d563b20272933315ecfbbada38e955`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 49.0 MB (49031449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525b68fed12d763a57f1b020aa1579673112de80a5b780b5ffaa045109c81f23`  
		Last Modified: Tue, 08 Apr 2025 07:38:26 GMT  
		Size: 14.9 MB (14878713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909681b45fdfcbd0bfebc28d96cd1bdab32fd85e3af6788b49d9cb80e8ff865a`  
		Last Modified: Tue, 08 Apr 2025 17:30:33 GMT  
		Size: 50.6 MB (50624452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ae4904ff46404ac5bb348da93b4e4f750b89ecaf468fd2f4b669038dc51cfb`  
		Last Modified: Tue, 08 Apr 2025 20:36:13 GMT  
		Size: 167.6 MB (167560460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9324aa48468359b44400cdd12929b0da8d31a43b594b8361c6a6eb9c9252c1`  
		Last Modified: Wed, 09 Apr 2025 03:29:40 GMT  
		Size: 241.2 MB (241215186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:28192187a807cc51ff78c007c700090895505aa9bbcb1e554e1e887bec3c50d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14887676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb595f8ced635b06fcf9a61717b019b48d031bc466e3a6ee8dd2439c17103dd5`

```dockerfile
```

-	Layers:
	-	`sha256:7c157d370bd0a5868efeec965f7bdab7d6202c55ade93b51998737e616cdb623`  
		Last Modified: Wed, 09 Apr 2025 03:29:36 GMT  
		Size: 14.9 MB (14876352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6557cfe726aaf265db580bb9f6cf75eb3c19cab87774acfaa4183ba88ac1a943`  
		Last Modified: Wed, 09 Apr 2025 03:29:34 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:09a7f7dcc5882af5bbccc6dc2d269e4ad12b8614dd251c3aabfc4f7411b0f8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.5 MB (480522553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7757be1da64936c13a88161dfcf370ffdc62353fd997f8283cbce57cbe1ca3b1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322dad1d7c942b6794e486e4e0b838c10dfb06247f1794d20cc703ddfee969f`  
		Last Modified: Tue, 08 Apr 2025 06:03:40 GMT  
		Size: 15.7 MB (15749086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebaef8f9f6ff21c71a0e336a0e9a00fbb65d469480593ef8d1ef507941e6f6d`  
		Last Modified: Tue, 08 Apr 2025 12:18:43 GMT  
		Size: 54.9 MB (54850009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848ef88a118038c35ad53e6bc0e94192e99b916044a11fb61a40b31c77edc820`  
		Last Modified: Tue, 08 Apr 2025 15:54:19 GMT  
		Size: 190.0 MB (190022174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d5d165da97b462feba12c3696936055a7ddb81249fd994f73056e2bbb08d5f`  
		Last Modified: Tue, 08 Apr 2025 21:31:15 GMT  
		Size: 167.6 MB (167647062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d112402618f4d6f27648b816c07a25745eb4d79aa34ea481f96aac9ed675a320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15089174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a8450527599dfb60c80da9bb3f35748ff58ac969abe44738329c168e8195b1`

```dockerfile
```

-	Layers:
	-	`sha256:22c68f5deda14220e1d89c790721da688dcdd27e932e2f7e33e3734a63d2ab4d`  
		Last Modified: Tue, 08 Apr 2025 21:31:11 GMT  
		Size: 15.1 MB (15077821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ca44f0d2397d24f0dbb2d7aafc86c60976ef147f078230b9734ce5418cc0f8`  
		Last Modified: Tue, 08 Apr 2025 21:31:10 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:9cbc7bd302c43e0a62cdb858f9c24a58b87aca7bf043ffab7cb079d4d5770139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549153535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3ace1c51d4464391099c6feb9831aed5ef6fd61345c2f970e108a016c5ebee`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
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
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb48ef4c334135b55fe5dd328911059bfd41eec15edf03ff0ab96ca44fb6a1`  
		Last Modified: Mon, 28 Apr 2025 21:53:52 GMT  
		Size: 16.3 MB (16267399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f9ff435d5a831802e386be1d29f22419a5d3951a76711fcdfc9f9bad0e6e3`  
		Last Modified: Mon, 28 Apr 2025 22:14:52 GMT  
		Size: 56.0 MB (56047280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ef040f15a9c521f9352beaf246f79eec04035acb8b716f343f27a2aea49563`  
		Last Modified: Mon, 28 Apr 2025 23:12:49 GMT  
		Size: 200.0 MB (200011534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84444c00c33828bec847a0ebe02cdf86e4a38c359cd763bbab9e70a5c8548f42`  
		Last Modified: Tue, 29 Apr 2025 00:17:33 GMT  
		Size: 222.1 MB (222144220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a2265636dfa483bc6134f1471d3440d26019c187f2e845c84c8ab33248f5d8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15073859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65970c74d4efc0b684a893fd52a296fbf9af95f404deca1b28741c80dbc4580`

```dockerfile
```

-	Layers:
	-	`sha256:a255f8f56087be5473d5e5866f9da323ec16bcb91c91c88845c86ba78c4f2fe4`  
		Last Modified: Tue, 29 Apr 2025 00:17:28 GMT  
		Size: 15.1 MB (15062642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973d0dfea887d74ea1652c8a1f21f05a292fbb82170d601ae82d934a72dbc336`  
		Last Modified: Tue, 29 Apr 2025 00:17:27 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:ff735b1f09be7bb43d0ceece3d6f03b877292ae0307e35b32f75165a05d574c5
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
$ docker pull rust@sha256:f163d1a53e6d105d037f8798f47f7947c062671bfb8d4485c612a1d00a3cbf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.1 MB (547098954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209b88fdf20bcc777094ee4ff43efc6ef043406c3a4c169785eda17fecc6318c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187b51b626e1d60ab369727b81f440adea9d45e97a45e137fc318be0bb7f09f`  
		Last Modified: Mon, 28 Apr 2025 23:12:20 GMT  
		Size: 211.4 MB (211356050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa897cd1d909c6f9aeeb2eb86f8281d7f1bd22ec60b937531af70f77e3b8c978`  
		Last Modified: Tue, 29 Apr 2025 00:20:42 GMT  
		Size: 198.8 MB (198846097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:c28aff946bf6a9641ea9333906292d4bcaca20d9730ac06f65c73b7dbfe00bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91b52445b0f0d88b77d2754a8b302421f4d6c97b7cb7d4de220050178066182`

```dockerfile
```

-	Layers:
	-	`sha256:b79e6f075844c12dfa724e6e05d0844d5de320465830dbb322f023f18d80c8fc`  
		Last Modified: Tue, 29 Apr 2025 00:20:37 GMT  
		Size: 15.5 MB (15471370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49427446706d8a35b3d9da8f7db167c3935e0225c64c41163ace92f38a50fb6`  
		Last Modified: Tue, 29 Apr 2025 00:20:36 GMT  
		Size: 13.1 KB (13137 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff3403ae6581adf67c0bbde3bcab29a147bf80f4392ab0af5dbed3377c1e119b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542266054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3698017437d2ae8077abed8488d38727dc5dba1f88e48876e5d3733f532a6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5414268749270f000845caf5689fb7740534b9fe922712301ba571a6afca96`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 59.6 MB (59639425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd5426bd57bea2caac0e0e87b98c0988fb39decb07637e76311bc28b01e6b7`  
		Last Modified: Tue, 08 Apr 2025 20:34:20 GMT  
		Size: 175.3 MB (175297229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093acd39fc465167a3795c75afa1eb7603459d1e396309304795a5c261b5a699`  
		Last Modified: Wed, 09 Apr 2025 03:31:38 GMT  
		Size: 241.2 MB (241214386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:965b9904c21bcd441911c4b25119ecca1e3f2fba0c3ab636faf4e528fc89a355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15289059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ac2dfec33d3f464c032fb6c8ec95b36285cdc7aca6e1012458969150a6d286`

```dockerfile
```

-	Layers:
	-	`sha256:69935c7f7900e361aabe717ea482ce229c0f4290d1f011ce1e508dba7b96a093`  
		Last Modified: Wed, 09 Apr 2025 03:31:32 GMT  
		Size: 15.3 MB (15275812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd85c681d8a8c03f05a9c034397cd1615a023bca10a054649801c9a54062374`  
		Last Modified: Wed, 09 Apr 2025 03:31:31 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0a27f7509b3def95327fe3735084c6a475bb52054efee7316d84fd91fc17736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506611045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee291f151e5b030a604f543d9a5c4541b96d0e637888a2a09334bd826322ab1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002e18bd5659ca9d155e99922678788bec836a3ac4964d8a9567ce59e2154de9`  
		Last Modified: Tue, 08 Apr 2025 15:52:42 GMT  
		Size: 202.7 MB (202735307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775439c6d731e711d1e42014fd69218e477c0c43221098e6d1513428f9946240`  
		Last Modified: Tue, 08 Apr 2025 21:32:10 GMT  
		Size: 167.6 MB (167648150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:63403d5c50b5086ee37972bd4ddb3dac08ba9444f59ed275e4639aa2c44c5c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e9f0697f2a2efe50253e36a3bc474bac40598a69515a99e7596cbf41d4c034`

```dockerfile
```

-	Layers:
	-	`sha256:2af08bf3572f4cd46f60afd036e4b1bf91b775e6c09a6bf6295ec9afbec238bf`  
		Last Modified: Tue, 08 Apr 2025 21:32:07 GMT  
		Size: 15.5 MB (15499945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32389045ed63fed52cb8d7ec269d8b4a0e5421639eb6f7906eba095d4d5d1e64`  
		Last Modified: Tue, 08 Apr 2025 21:32:06 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:69531fcb8a67b072bfc78f893d76a5d5c5a325536a4f948493f5fae1756d4019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (572991948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f4ce1664011b7b08cabc2bcb040af4431dd6da7fff8a55460b8c4e9fd01a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Mon, 28 Apr 2025 21:53:42 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce8929d56fab56325a8eea211cb4cd1021bc6ffc1e7a794d505ddbe638b23cd`  
		Last Modified: Mon, 28 Apr 2025 22:15:00 GMT  
		Size: 66.2 MB (66228922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1528cc13747bb103866d00332de43f9304156fef5a2f396b15d9e173b1365f5`  
		Last Modified: Mon, 28 Apr 2025 23:13:00 GMT  
		Size: 210.3 MB (210293092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a0a0e26e85220e6482bcf2859ccd19dc889d8c6237381e13a52446ce56f374`  
		Last Modified: Tue, 29 Apr 2025 00:19:10 GMT  
		Size: 222.1 MB (222144215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:e26a24e515fc29bea5fb4ad97d93055e97736137dbbff6c0a66d1e3cb662a266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2a0d93c03f13377ffa686d882edf0901118adbaeea959c691a9dc76256ea5b`

```dockerfile
```

-	Layers:
	-	`sha256:38affa8290df1776c35aab78bc46e1491c5b3a525152f3b1e737e46e6456d55e`  
		Last Modified: Tue, 29 Apr 2025 00:19:06 GMT  
		Size: 15.4 MB (15448635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04d9a14a26e0b8792115fbad3c25692abd8c3ea50dc544ff6954cc8a9d3b12ab`  
		Last Modified: Tue, 29 Apr 2025 00:19:05 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:6ff43004246ac7409ecbc3cf1d1f64fe97af549cff6e4eeffb347c53123695c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.7 MB (628715675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52ec6298460494f48ebd94562ccdc697dcc3bb3d3915515c744d5def51728ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675af5e5720aa9e9d4f74b056a7b58aa0a84a5b3cc2c23272c361e473b9c5b8`  
		Last Modified: Tue, 08 Apr 2025 15:34:04 GMT  
		Size: 214.4 MB (214387209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fd4fb10062d551eeb2e024d3e563728a42549e867f8f166eb7d3c22b7d6b78`  
		Last Modified: Tue, 08 Apr 2025 19:25:14 GMT  
		Size: 266.5 MB (266502721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:c47a89a1025ff4dbb33264cf2765a8e1e0c24ff47135d1b6c7c7e977468d89e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15459677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7827834152d2d52c8fbc16a215bf024a151d424dffb4ab149188341b0cc1f14`

```dockerfile
```

-	Layers:
	-	`sha256:23ddb56e82f0fa073703d355e296183384c1fc63c0b493b2a1bac0b20c353294`  
		Last Modified: Tue, 08 Apr 2025 19:25:07 GMT  
		Size: 15.4 MB (15446470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfcaa31a08c5def654ca430c6b47811b40f07fd5cbdfd2e94e2fb98d08e77e8`  
		Last Modified: Tue, 08 Apr 2025 19:25:06 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:aaf804c60805de2a84400664811dd543e7a735e684976c5b4ac22ea1ae537910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611949825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f71016804f1861e6054a214aea01f56260a9f54e32cde4b102889b5ba38c3b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fde99ce0eec506f038695c59ba0ff56bd0df358636c0b067f55c60d7d566c`  
		Last Modified: Tue, 08 Apr 2025 06:52:25 GMT  
		Size: 63.5 MB (63498375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766d2c4791b14ffb813f2bd4d87d95e9030a5939b65f31722bc2c223f845ecf8`  
		Last Modified: Tue, 08 Apr 2025 10:02:09 GMT  
		Size: 183.4 MB (183388438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eb0c69619b19f87369d4a1737b46098625d76f72f75d41c18ecc2b9f8019cc`  
		Last Modified: Tue, 08 Apr 2025 18:17:17 GMT  
		Size: 293.9 MB (293903680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:21d031f77b8b2c841a56916b430442b3dbbfd340d1aadee3bf1561f97999cc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15297196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49e7c039c53b210b5e3cfc85ca1eb9fcaa5480271c4f2b0c5e5e6aa37781915`

```dockerfile
```

-	Layers:
	-	`sha256:0d2bad61871ee6c24e5ae84182871a58c88b6f3593a3f0a381f6236eec0606e9`  
		Last Modified: Tue, 08 Apr 2025 18:17:08 GMT  
		Size: 15.3 MB (15284058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1589d850c8b322cdebed632bcf0d29ee300ca793b83044f540479e4b39431e1`  
		Last Modified: Tue, 08 Apr 2025 18:17:07 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:3deccec2419f46f7052356d99e0c76ceba02a0164a45e1c5894481a4785e7895
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
$ docker pull rust@sha256:5265cf7f0324e5af0d0af625952b426cfaf5fc6daafd79b1fdedac07bd69b999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297830650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7f574507b85a8cc381daab85fd042918977aa4e469b8c0b3adca5ebbf2f53d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d2c2c6f222aae0625c61e9d3f36afe3bd17ebed1d2eb21f1bf888d76a5d60b`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
		Size: 269.6 MB (269603008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:19dd7a17f1dc76c4e00c549b877018bc870343a6ecbc8ef68fe7946a84a356d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f410651604a0a715d015565863b7efe3c81dcf3da755fb9cf24f7a5237556b`

```dockerfile
```

-	Layers:
	-	`sha256:ff862d7e48c414c8bb95d3a1388b734c191baea434a62085f4346713d401770d`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675eae4d6651df312a550a92c9e8941bcaedafe4f550de7cad9f475791b9a3b0`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
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
$ docker pull rust@sha256:9b4588a9375c6c2a2a7454768c282c8e549784b521eb0c5ea3e32d7568affed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318922232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4afab512f48e1dfcccdf517247ac52f880b84fd820a0b2d4949efd3c0301d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f7195df9fd10fb92d71646b4d86321f170c6c731039dd4e34938be58f58cb9`  
		Last Modified: Mon, 28 Apr 2025 21:59:24 GMT  
		Size: 289.7 MB (289711366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:51adece521582dbdc49671e0fbe582c8e8a6789f6274dc195eeee01c43cc3705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0b4b1a80ee612bf4ae7a0cf824e5305b3644dbae73ef8d0d8d832945a7b784`

```dockerfile
```

-	Layers:
	-	`sha256:0cf266b3c804c8acfcb96fe5b018f864f17e2d3be0b00960512021e7dedea803`  
		Last Modified: Mon, 28 Apr 2025 21:59:18 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a2e0dd93e9a6d69a21bdeb2e6d7d8350d6e6bd032336a2c1593141e3d80c57`  
		Last Modified: Mon, 28 Apr 2025 21:59:17 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:e5aeefd41ca6f9abd02b12460157ca851369b314458f653836b6041460b89818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367336038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84bea10cf021c1602244cf068230d973768342a4cd724e0c3118bfae5cfa97`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c04e3602592a873e00fef80b178c6583f85417553600599ea8e1e61736cad8`  
		Last Modified: Tue, 29 Apr 2025 03:38:35 GMT  
		Size: 335.3 MB (335267595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:f23567e86bb567602fbd3b97382d2e63737d1c041296ed7e66094cf7711c5063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c1b4c721edb518831b46540fa64acf0c3efa8d91e5d44979f23bf0a9e5a60a`

```dockerfile
```

-	Layers:
	-	`sha256:d780a892b067eb8a87aeba5b1ddc996252fb597316ab13515b746c3bdf531ef0`  
		Last Modified: Tue, 29 Apr 2025 03:38:27 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:188d119007c4e10172952ad43483211958e15eddcf785427c58e34052df76afa`  
		Last Modified: Tue, 29 Apr 2025 03:38:26 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:cd75cace871d1241847f08379dfd7b2913730d65f88736c71cd4073eebc53b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e951356ca72c6d32f55a1a349ce8e5030b100b4da94dd52e05829406fd63a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5365383afac604f9c2f2ab1254332b6835b90d820e7e3d14137a8ab8bd5f849`  
		Last Modified: Tue, 29 Apr 2025 02:34:37 GMT  
		Size: 344.0 MB (344011014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:3fd3ab8f79e47636e149395239ceb7c46785b04e3f66d11d2b3645c2e0c130a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ab2946a315baa636e061bf47c4e0d08f33e4e452ee0dd0dbabb4c8cd56d7c5`

```dockerfile
```

-	Layers:
	-	`sha256:89ea65b28be4d0e2d05e9cd9e7b13b402be9f781990fc713eeb4ac680fee4ed0`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d046b9ce46b62be8c69446342f660b1449e172e7dfa84284fa1c4242cb3b348a`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:3deccec2419f46f7052356d99e0c76ceba02a0164a45e1c5894481a4785e7895
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
$ docker pull rust@sha256:5265cf7f0324e5af0d0af625952b426cfaf5fc6daafd79b1fdedac07bd69b999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297830650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7f574507b85a8cc381daab85fd042918977aa4e469b8c0b3adca5ebbf2f53d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d2c2c6f222aae0625c61e9d3f36afe3bd17ebed1d2eb21f1bf888d76a5d60b`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
		Size: 269.6 MB (269603008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:19dd7a17f1dc76c4e00c549b877018bc870343a6ecbc8ef68fe7946a84a356d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f410651604a0a715d015565863b7efe3c81dcf3da755fb9cf24f7a5237556b`

```dockerfile
```

-	Layers:
	-	`sha256:ff862d7e48c414c8bb95d3a1388b734c191baea434a62085f4346713d401770d`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
		Size: 4.0 MB (3956669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675eae4d6651df312a550a92c9e8941bcaedafe4f550de7cad9f475791b9a3b0`  
		Last Modified: Mon, 28 Apr 2025 22:05:17 GMT  
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
$ docker pull rust@sha256:9b4588a9375c6c2a2a7454768c282c8e549784b521eb0c5ea3e32d7568affed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318922232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4afab512f48e1dfcccdf517247ac52f880b84fd820a0b2d4949efd3c0301d0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f7195df9fd10fb92d71646b4d86321f170c6c731039dd4e34938be58f58cb9`  
		Last Modified: Mon, 28 Apr 2025 21:59:24 GMT  
		Size: 289.7 MB (289711366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:51adece521582dbdc49671e0fbe582c8e8a6789f6274dc195eeee01c43cc3705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0b4b1a80ee612bf4ae7a0cf824e5305b3644dbae73ef8d0d8d832945a7b784`

```dockerfile
```

-	Layers:
	-	`sha256:0cf266b3c804c8acfcb96fe5b018f864f17e2d3be0b00960512021e7dedea803`  
		Last Modified: Mon, 28 Apr 2025 21:59:18 GMT  
		Size: 3.9 MB (3936584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a2e0dd93e9a6d69a21bdeb2e6d7d8350d6e6bd032336a2c1593141e3d80c57`  
		Last Modified: Mon, 28 Apr 2025 21:59:17 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:e5aeefd41ca6f9abd02b12460157ca851369b314458f653836b6041460b89818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367336038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84bea10cf021c1602244cf068230d973768342a4cd724e0c3118bfae5cfa97`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c04e3602592a873e00fef80b178c6583f85417553600599ea8e1e61736cad8`  
		Last Modified: Tue, 29 Apr 2025 03:38:35 GMT  
		Size: 335.3 MB (335267595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f23567e86bb567602fbd3b97382d2e63737d1c041296ed7e66094cf7711c5063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c1b4c721edb518831b46540fa64acf0c3efa8d91e5d44979f23bf0a9e5a60a`

```dockerfile
```

-	Layers:
	-	`sha256:d780a892b067eb8a87aeba5b1ddc996252fb597316ab13515b746c3bdf531ef0`  
		Last Modified: Tue, 29 Apr 2025 03:38:27 GMT  
		Size: 3.9 MB (3929230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:188d119007c4e10172952ad43483211958e15eddcf785427c58e34052df76afa`  
		Last Modified: Tue, 29 Apr 2025 03:38:26 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:cd75cace871d1241847f08379dfd7b2913730d65f88736c71cd4073eebc53b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370895881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e951356ca72c6d32f55a1a349ce8e5030b100b4da94dd52e05829406fd63a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5365383afac604f9c2f2ab1254332b6835b90d820e7e3d14137a8ab8bd5f849`  
		Last Modified: Tue, 29 Apr 2025 02:34:37 GMT  
		Size: 344.0 MB (344011014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3fd3ab8f79e47636e149395239ceb7c46785b04e3f66d11d2b3645c2e0c130a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ab2946a315baa636e061bf47c4e0d08f33e4e452ee0dd0dbabb4c8cd56d7c5`

```dockerfile
```

-	Layers:
	-	`sha256:89ea65b28be4d0e2d05e9cd9e7b13b402be9f781990fc713eeb4ac680fee4ed0`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 3.8 MB (3798569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d046b9ce46b62be8c69446342f660b1449e172e7dfa84284fa1c4242cb3b348a`  
		Last Modified: Tue, 29 Apr 2025 02:34:31 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:8b4fb6e91904117e77ff7fb19d63dc83c6f1ed3caa7915b9390e5380b19cb55d
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
$ docker pull rust@sha256:61200dad758eb2c4e99313d0c6782e7fa89311bd83c94b9bc39bc01948f587db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289241682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25e74260d87c5fa7492be92ca0677a11a991844226d26af85a21722fe8fd4dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0797f92ce1279f464536d8c0af7023351ee2e207ccec21fe543d01eb4c4248`  
		Last Modified: Mon, 28 Apr 2025 22:05:28 GMT  
		Size: 259.0 MB (258987078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1836529f3ca5bc812985db92eb733b1bccd994105d29fded97d9d61adea71be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e36b0a70ce16003c9069f2825bd02e341920e739a895f46f2a469f7a79fd07`

```dockerfile
```

-	Layers:
	-	`sha256:13123c2d58f95072da02ee8e10ac5a44b16d4f6545106822ca9f98b7eee11c9c`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
		Size: 4.2 MB (4175178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4758d2f11990f0f5dceffd56dc922a42f33a2fb2873222c6bc096a6c1cb942`  
		Last Modified: Mon, 28 Apr 2025 22:05:23 GMT  
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
$ docker pull rust@sha256:091710edd306bd2bf84340d1127b91227bc8fa29f7e37ba0036ec2686cd16113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314101243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd162dda1171190a0aa571d0efa79d256bae0efec08e9afdc2e79c38754466a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Apr 2025 09:55:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Thu, 03 Apr 2025 09:55:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 03 Apr 2025 09:55:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.86.0
# Thu, 03 Apr 2025 09:55:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:73bb1b80ecf1f8784ad6f92a35120b6e2306657fc7e8cbaedca1f45900f3d746`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 31.2 MB (31187893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e304cb55c66d1a5edc35eacf691a84c62d770f1198d127335959a3166eeb088`  
		Last Modified: Mon, 28 Apr 2025 21:58:49 GMT  
		Size: 282.9 MB (282913350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4a0423225bb2de1faea503c48c34dce51dc7696d8c40f13d16e30180c1c91ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ef654c9879524c59c0bf60a53ef350537343ebe309bf9fa7371daa378cec71`

```dockerfile
```

-	Layers:
	-	`sha256:acd11de69428b51d1eeb16ee8532107d4b7f03aa5deb5323de965df13bf84155`  
		Last Modified: Mon, 28 Apr 2025 21:58:43 GMT  
		Size: 4.2 MB (4165435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58625db462ea2607636281f9a865fc50b768ee088febe47023718de82b41b7e4`  
		Last Modified: Mon, 28 Apr 2025 21:58:42 GMT  
		Size: 11.3 KB (11323 bytes)  
		MIME: application/vnd.in-toto+json
