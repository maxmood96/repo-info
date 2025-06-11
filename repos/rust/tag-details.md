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
-	[`rust:1.87`](#rust187)
-	[`rust:1.87-alpine`](#rust187-alpine)
-	[`rust:1.87-alpine3.20`](#rust187-alpine320)
-	[`rust:1.87-alpine3.21`](#rust187-alpine321)
-	[`rust:1.87-alpine3.22`](#rust187-alpine322)
-	[`rust:1.87-bookworm`](#rust187-bookworm)
-	[`rust:1.87-bullseye`](#rust187-bullseye)
-	[`rust:1.87-slim`](#rust187-slim)
-	[`rust:1.87-slim-bookworm`](#rust187-slim-bookworm)
-	[`rust:1.87-slim-bullseye`](#rust187-slim-bullseye)
-	[`rust:1.87.0`](#rust1870)
-	[`rust:1.87.0-alpine`](#rust1870-alpine)
-	[`rust:1.87.0-alpine3.20`](#rust1870-alpine320)
-	[`rust:1.87.0-alpine3.21`](#rust1870-alpine321)
-	[`rust:1.87.0-alpine3.22`](#rust1870-alpine322)
-	[`rust:1.87.0-bookworm`](#rust1870-bookworm)
-	[`rust:1.87.0-bullseye`](#rust1870-bullseye)
-	[`rust:1.87.0-slim`](#rust1870-slim)
-	[`rust:1.87.0-slim-bookworm`](#rust1870-slim-bookworm)
-	[`rust:1.87.0-slim-bullseye`](#rust1870-slim-bullseye)
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

## `rust:1`

```console
$ docker pull rust@sha256:b571d7b2dc7b9154517eeda87c0c3c97865d432e95ec205e34a194fd2baaff1d
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
$ docker pull rust@sha256:6d79f767859a5f025a062505fa9f2c1a041cadafcee71fbcbd226223be462f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553345588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a4a73321e80052e6fcd636dcd4ee26c8fa0ed0d655f95d92276efb7e759cc2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8862a18fa961ebfbac8484877dd4894e96ee88177d8c4f1f54d9727262b7d`  
		Last Modified: Wed, 11 Jun 2025 02:16:04 GMT  
		Size: 211.4 MB (211370316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d73d009ce498344941c85ff822a919ac7bb8976fd68dc8174f43a594bb3fa5`  
		Last Modified: Wed, 11 Jun 2025 03:21:03 GMT  
		Size: 205.1 MB (205065498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:503b69f42140f797db581680ee944348a715f85e374bf0f64688bb5e2d7f36ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15875572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9733726f707a166e40276a18d11a14103319579caa5d58f7e146f38d2b2cbe0d`

```dockerfile
```

-	Layers:
	-	`sha256:7fea0bce605acbffe3ad3faddcc83eebdef406125bb53e8a4ea980a11ae3fe32`  
		Last Modified: Wed, 11 Jun 2025 05:44:23 GMT  
		Size: 15.9 MB (15862434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8529bb6f4380c5ac83f220695448a518ba1d0d4b38c355cab9e014939ba116b`  
		Last Modified: Wed, 11 Jun 2025 05:44:24 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:72b485162489d2c8c49c305dd8b6ba86d4ff05ad986dfc71c07c9cf752fb23b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549362604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c922227a2a41f42eae2eebb9844a4b1e45540c0b00068b270c49c1a1e0b764`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22ee2db9f8d2ea3317ceb36f4b9bc7895f6cb8402903d639c8083eaec948450`  
		Last Modified: Tue, 03 Jun 2025 13:39:41 GMT  
		Size: 175.3 MB (175297793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92df434dc3b1ce2413f6828ef2e4c81ee8a8cef9cbe94a7d2215ad2bd340b292`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 248.3 MB (248281119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:2e7ce19770e0e30560aa4a23ada499e5a679b9dd1f61f479fe8d5abee6df0137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15386282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e40b43bdd8233f500a8bec0378ba7ac318dee0cafb4b7f582f11e2585a0396`

```dockerfile
```

-	Layers:
	-	`sha256:f8c270ee20e4767bc254f12fd15b19ddfb7c9f9a382a752ada7fd70bb37b3cc8`  
		Last Modified: Tue, 03 Jun 2025 15:36:17 GMT  
		Size: 15.4 MB (15373035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d32c5949c1f294d1c9fdbee6216a2148b76a885326b5d0372c69b726ab518b0`  
		Last Modified: Tue, 03 Jun 2025 15:36:16 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:40b030bf2085108f7fe5f75de0454fd4f6f855182477906360f40c0c29e95ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513085197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cecf015e8a7925026c922f69a93f75798f571a03fe30546ac7915e8760aaaa9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ee5cb7152015437e4a9b3066ae9e25a26a3bef6617d0b7f25368511c2d954`  
		Last Modified: Tue, 03 Jun 2025 13:30:35 GMT  
		Size: 202.8 MB (202762554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8a70e7346d3f568e98a68fc27e54274c16511edcd67498ae24761da6880cf6`  
		Last Modified: Tue, 03 Jun 2025 13:33:54 GMT  
		Size: 174.1 MB (174082075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:9719468f301df89ccc1071537f751d5e28f0c45df8834a133614066e3f97fd22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15612386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27147e11d32faab39878abb0d8cd3ca6bd4c56331b1722b30d8f48f9a45ece6e`

```dockerfile
```

-	Layers:
	-	`sha256:cc53a730eadb9784a7c191236378a7bcf219afa01f680521eb4bddf1d8ac993e`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 15.6 MB (15599095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e5657bfd53d43e028eb9d10e36db17bcc612d8fae30e5fe0fb076caa4b489b`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:8173985fad86853be81c2d2d427c1a22ad9d919982c5feb33ee56cc79a4b3c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579415232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e17162e2db334c9d6ff28fbd81344a20a803fde6a517c1c9410e6078a5a45d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731d58cf259468f5a31e00d6a586bde147720039c92e6c1ff4cb48a5dd996ae`  
		Last Modified: Wed, 11 Jun 2025 00:00:38 GMT  
		Size: 24.9 MB (24855706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce073e7b00b22009464483e266ff8ba48a8c0db86f16c877aa302337bbed6e9`  
		Last Modified: Wed, 11 Jun 2025 01:13:32 GMT  
		Size: 66.2 MB (66225240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75453a9e8c0ecda25b39aaabe16c9694b0bdb799dbc4bb61d1d0aee7d8b70850`  
		Last Modified: Wed, 11 Jun 2025 02:15:24 GMT  
		Size: 210.3 MB (210300359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a8e4b0736bc7a3d22fb842ad0ee81737c0ed14f5fe26606d2f4b5123616b6`  
		Last Modified: Wed, 11 Jun 2025 06:01:45 GMT  
		Size: 228.6 MB (228556453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:ab0c67f770b8da0cbe9479ecec374333e09badd00136782ce748b9cd17e281c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273c89500eb4e84dfb414ccb465c200b7f2a92f66f0b44e6f219b7dde68417b4`

```dockerfile
```

-	Layers:
	-	`sha256:dc04aee6f7f1d600381837690bbefc0648653c65ede9e2ecb6dc60dd7740d0c3`  
		Last Modified: Wed, 11 Jun 2025 05:45:01 GMT  
		Size: 15.8 MB (15839332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a2d3bfd52375162462af27b77692b39e0868ce869675ce142d35c98dcb3f11`  
		Last Modified: Wed, 11 Jun 2025 05:45:02 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:294e06b00a43a648e43744691fbef73c1bdb451465ac350c76f736ed8a50b602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639200335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98218e5b1f057d84b638dd735f30b4a14abac5bb993b7561c9580a3babcd22dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Tue, 03 Jun 2025 13:36:57 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Tue, 03 Jun 2025 13:36:59 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5288618fea79e9a348995382235e6bee52819db4047a345ffaeaddd2b82e06`  
		Last Modified: Tue, 03 Jun 2025 13:37:01 GMT  
		Size: 214.4 MB (214416172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acddbc7af9fd8740373f8026a505be271623021d28c5aaf7cf9cfce5371e307`  
		Last Modified: Tue, 03 Jun 2025 15:36:39 GMT  
		Size: 277.0 MB (276955569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:60293968af0cc8afff5372a51d16244ad649290286e9457b6475a872eaf44c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15558952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90744ca96e8742bd842f46bb381ee8f2bd14a575fbfcf610a629445664ae33b`

```dockerfile
```

-	Layers:
	-	`sha256:e7bef55039062c7c4ae93c0994d2baa58cc23620f26310f07c85affb73ade0e6`  
		Last Modified: Tue, 03 Jun 2025 15:36:29 GMT  
		Size: 15.5 MB (15545745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ac5c316843cde59da34e1480f62e0a90b78ace51a57f9f67917ce2812741f6`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:b9f17d320e48e042011cee37b615b2594ca1ac94588789d0978ac65e5e9671b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604371175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7ddbb7c8c246892af6179b2b4a9b8f8ceb4a0b60eff22c4736c5eaaf52b114`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Tue, 03 Jun 2025 13:37:08 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Tue, 03 Jun 2025 13:37:11 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3151505c70d8a7022bb518bbfce9c7488d1dd6ab624e1d96b883eb0654da7562`  
		Last Modified: Tue, 03 Jun 2025 13:37:22 GMT  
		Size: 183.4 MB (183405201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b0882d1ed7e92235dfca31dcc58a7de4c5cad3b764f0fe10874904586c5009`  
		Last Modified: Tue, 03 Jun 2025 14:16:08 GMT  
		Size: 286.3 MB (286308749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:751099b710c1a89fa55e82f9bc0fabfd70cb451e25cfbc7fc9449cc3fec7df28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15394148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd99f87c0d557b247c0e2c29a586dd93187c2ded1f463a78dd244eed473ac43a`

```dockerfile
```

-	Layers:
	-	`sha256:2d523435dd3012b7c822fc76bd1967e45ece2c7c3cda49a5a98a4c7c9fa13591`  
		Last Modified: Tue, 03 Jun 2025 15:36:32 GMT  
		Size: 15.4 MB (15381009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d39102b0130d44f2ec934dd1a55a3718747eb90d0591508f65d806ba52f578`  
		Last Modified: Tue, 03 Jun 2025 15:36:31 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:126df0f2a57e675f9306fe180b833982ffb996e90a92a793bb75253cfeed5475
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:2d5a7e008d9c1e86e54c0a3fffc00399eee945a13aa504fd5faf625e04110bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324451128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa6d9f8b73e08bfab3090a694fb52cea848dd5dfd249f9ff6352477596d5d38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aed27d59f9f3bafc26c73e1fa85e80d10a2b8b6221db885ef03875cbb2a92c3`  
		Last Modified: Tue, 03 Jun 2025 13:33:59 GMT  
		Size: 61.6 MB (61613723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a631e0f5786232f793b7aff2783c3a8252ee122748a6f63fb55c227e00e5002`  
		Last Modified: Tue, 03 Jun 2025 13:34:31 GMT  
		Size: 259.0 MB (259040559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:629b8efb80d6e9a1b711c46acd85e890c1c173b6b976ce39c598a8499163ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc3a74aa6b388d7315bb35c0e0fbd5fb39121d9296330833d8f9b79ffeb6a98`

```dockerfile
```

-	Layers:
	-	`sha256:03bc872db35194e79864e3a72cbb58ddd0548f438a45de2790469bf25a776a5e`  
		Last Modified: Wed, 04 Jun 2025 17:05:12 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c4e51ae8efcd54f48f7d1ced1a254f8c7ca2a7da2e3f6a81c2bedaed4895c9`  
		Last Modified: Wed, 04 Jun 2025 17:05:08 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fa3f412044d347294ad9c21eb3c9922a5e12e57b645ae53bbd27b8bc26173a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327194537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c83a1beaf9ddcfc60c8ec87a69dd7964f3e21bb48de7d530afe4816ca07fb61`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e525acaed56cf743f6ae8ee0c463c3fd7f0e9765bc0faaa7b0119fff2f2db4c4`  
		Last Modified: Tue, 03 Jun 2025 13:34:25 GMT  
		Size: 59.2 MB (59154215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1e992c2528e607b21a005bd23933eb8ae5f77fb262c96790f579f7f863d3c7`  
		Last Modified: Tue, 03 Jun 2025 13:34:30 GMT  
		Size: 263.9 MB (263904381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:0993ebd475453ccc6ded9cffa3118df8be36790fcfcf803fd1bf51bd147a22da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf7cab2f78729c23ec9792c67e373b2906e91cd19fe74c90616e885ff1ddd70`

```dockerfile
```

-	Layers:
	-	`sha256:59310aed03e6f7a9700cd2820322b4883fea2f9851c2e311a52617955a3abd14`  
		Last Modified: Wed, 04 Jun 2025 17:05:46 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e888f3541888d0dcd1e7f14fca30a9930a25f4836300284c59226514fe4b48`  
		Last Modified: Wed, 04 Jun 2025 17:05:45 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718715b3cbe3b4fd9094909206504e5958585bd739a34dc4fb5b7f6ed2131b8`  
		Last Modified: Fri, 16 May 2025 14:17:43 GMT  
		Size: 55.3 MB (55315586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeb4a9d8a98d7b7dadf2be0b1943267d81b081cb2fb12a85484c6aaadf235fb`  
		Last Modified: Fri, 16 May 2025 14:17:57 GMT  
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
		Last Modified: Thu, 15 May 2025 20:44:31 GMT  
		Size: 711.8 KB (711789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a9394ddea85fc3e016d5927f8ce6a38638e7c7eeea1996460a0e68f6915e5c6`  
		Last Modified: Thu, 15 May 2025 20:44:31 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c6aa5430354637d99185e3c6f997bb89b34d0340d714c59489470f3b28fb00`  
		Last Modified: Thu, 08 May 2025 23:40:24 GMT  
		Size: 53.0 MB (52950277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d7b743d7f5864c65b2894547a9334b33385928622ae90e6a32c6e8856c668`  
		Last Modified: Fri, 16 May 2025 14:28:10 GMT  
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
		Last Modified: Mon, 09 Jun 2025 05:43:46 GMT  
		Size: 747.7 KB (747721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5df0c715639e649fb2f087e25e05ab1d51803c9e80193b7ded83d66aa0f06e`  
		Last Modified: Mon, 09 Jun 2025 05:43:46 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b343ca42d769a088aad30a06435916be946b7bd77c275c4c48aa9c02d07ebc6`  
		Last Modified: Thu, 15 May 2025 20:45:48 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0312ddedcb8a05877b03a2214ddd4942d87d6bd8684a5f5bc0353f72d76def`  
		Last Modified: Thu, 15 May 2025 20:46:29 GMT  
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
		Last Modified: Thu, 15 May 2025 20:44:27 GMT  
		Size: 783.8 KB (783823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05e06b11fae76f35a913f94980f7b264abfa081dffa29929dd773c6969a089d`  
		Last Modified: Thu, 15 May 2025 20:44:27 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a8d04fc53dbb480e66cf7321229cda858c75a9bfa488474aabc6a3fbc3423`  
		Last Modified: Thu, 08 May 2025 17:05:51 GMT  
		Size: 59.1 MB (59101363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd10981d51d5c4342a74b76870500712f6977bafb0891f69b5b725cd3f83575b`  
		Last Modified: Fri, 16 May 2025 13:16:00 GMT  
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
		Last Modified: Fri, 16 May 2025 14:02:45 GMT  
		Size: 863.4 KB (863409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4799a729390389da9955e76bdba397218c8fff4138d88735449c1364a6120788`  
		Last Modified: Fri, 16 May 2025 14:02:46 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.22`

```console
$ docker pull rust@sha256:126df0f2a57e675f9306fe180b833982ffb996e90a92a793bb75253cfeed5475
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.22` - linux; amd64

```console
$ docker pull rust@sha256:2d5a7e008d9c1e86e54c0a3fffc00399eee945a13aa504fd5faf625e04110bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324451128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa6d9f8b73e08bfab3090a694fb52cea848dd5dfd249f9ff6352477596d5d38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aed27d59f9f3bafc26c73e1fa85e80d10a2b8b6221db885ef03875cbb2a92c3`  
		Last Modified: Tue, 03 Jun 2025 13:33:59 GMT  
		Size: 61.6 MB (61613723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a631e0f5786232f793b7aff2783c3a8252ee122748a6f63fb55c227e00e5002`  
		Last Modified: Tue, 03 Jun 2025 13:34:31 GMT  
		Size: 259.0 MB (259040559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:629b8efb80d6e9a1b711c46acd85e890c1c173b6b976ce39c598a8499163ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc3a74aa6b388d7315bb35c0e0fbd5fb39121d9296330833d8f9b79ffeb6a98`

```dockerfile
```

-	Layers:
	-	`sha256:03bc872db35194e79864e3a72cbb58ddd0548f438a45de2790469bf25a776a5e`  
		Last Modified: Wed, 04 Jun 2025 17:05:12 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c4e51ae8efcd54f48f7d1ced1a254f8c7ca2a7da2e3f6a81c2bedaed4895c9`  
		Last Modified: Wed, 04 Jun 2025 17:05:08 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fa3f412044d347294ad9c21eb3c9922a5e12e57b645ae53bbd27b8bc26173a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327194537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c83a1beaf9ddcfc60c8ec87a69dd7964f3e21bb48de7d530afe4816ca07fb61`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e525acaed56cf743f6ae8ee0c463c3fd7f0e9765bc0faaa7b0119fff2f2db4c4`  
		Last Modified: Tue, 03 Jun 2025 13:34:25 GMT  
		Size: 59.2 MB (59154215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1e992c2528e607b21a005bd23933eb8ae5f77fb262c96790f579f7f863d3c7`  
		Last Modified: Tue, 03 Jun 2025 13:34:30 GMT  
		Size: 263.9 MB (263904381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:0993ebd475453ccc6ded9cffa3118df8be36790fcfcf803fd1bf51bd147a22da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf7cab2f78729c23ec9792c67e373b2906e91cd19fe74c90616e885ff1ddd70`

```dockerfile
```

-	Layers:
	-	`sha256:59310aed03e6f7a9700cd2820322b4883fea2f9851c2e311a52617955a3abd14`  
		Last Modified: Wed, 04 Jun 2025 17:05:46 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e888f3541888d0dcd1e7f14fca30a9930a25f4836300284c59226514fe4b48`  
		Last Modified: Wed, 04 Jun 2025 17:05:45 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:b571d7b2dc7b9154517eeda87c0c3c97865d432e95ec205e34a194fd2baaff1d
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
$ docker pull rust@sha256:6d79f767859a5f025a062505fa9f2c1a041cadafcee71fbcbd226223be462f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553345588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a4a73321e80052e6fcd636dcd4ee26c8fa0ed0d655f95d92276efb7e759cc2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8862a18fa961ebfbac8484877dd4894e96ee88177d8c4f1f54d9727262b7d`  
		Last Modified: Wed, 11 Jun 2025 02:16:04 GMT  
		Size: 211.4 MB (211370316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d73d009ce498344941c85ff822a919ac7bb8976fd68dc8174f43a594bb3fa5`  
		Last Modified: Wed, 11 Jun 2025 03:21:03 GMT  
		Size: 205.1 MB (205065498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:503b69f42140f797db581680ee944348a715f85e374bf0f64688bb5e2d7f36ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15875572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9733726f707a166e40276a18d11a14103319579caa5d58f7e146f38d2b2cbe0d`

```dockerfile
```

-	Layers:
	-	`sha256:7fea0bce605acbffe3ad3faddcc83eebdef406125bb53e8a4ea980a11ae3fe32`  
		Last Modified: Wed, 11 Jun 2025 05:44:23 GMT  
		Size: 15.9 MB (15862434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8529bb6f4380c5ac83f220695448a518ba1d0d4b38c355cab9e014939ba116b`  
		Last Modified: Wed, 11 Jun 2025 05:44:24 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:72b485162489d2c8c49c305dd8b6ba86d4ff05ad986dfc71c07c9cf752fb23b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549362604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c922227a2a41f42eae2eebb9844a4b1e45540c0b00068b270c49c1a1e0b764`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22ee2db9f8d2ea3317ceb36f4b9bc7895f6cb8402903d639c8083eaec948450`  
		Last Modified: Tue, 03 Jun 2025 13:39:41 GMT  
		Size: 175.3 MB (175297793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92df434dc3b1ce2413f6828ef2e4c81ee8a8cef9cbe94a7d2215ad2bd340b292`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 248.3 MB (248281119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2e7ce19770e0e30560aa4a23ada499e5a679b9dd1f61f479fe8d5abee6df0137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15386282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e40b43bdd8233f500a8bec0378ba7ac318dee0cafb4b7f582f11e2585a0396`

```dockerfile
```

-	Layers:
	-	`sha256:f8c270ee20e4767bc254f12fd15b19ddfb7c9f9a382a752ada7fd70bb37b3cc8`  
		Last Modified: Tue, 03 Jun 2025 15:36:17 GMT  
		Size: 15.4 MB (15373035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d32c5949c1f294d1c9fdbee6216a2148b76a885326b5d0372c69b726ab518b0`  
		Last Modified: Tue, 03 Jun 2025 15:36:16 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:40b030bf2085108f7fe5f75de0454fd4f6f855182477906360f40c0c29e95ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513085197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cecf015e8a7925026c922f69a93f75798f571a03fe30546ac7915e8760aaaa9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ee5cb7152015437e4a9b3066ae9e25a26a3bef6617d0b7f25368511c2d954`  
		Last Modified: Tue, 03 Jun 2025 13:30:35 GMT  
		Size: 202.8 MB (202762554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8a70e7346d3f568e98a68fc27e54274c16511edcd67498ae24761da6880cf6`  
		Last Modified: Tue, 03 Jun 2025 13:33:54 GMT  
		Size: 174.1 MB (174082075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9719468f301df89ccc1071537f751d5e28f0c45df8834a133614066e3f97fd22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15612386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27147e11d32faab39878abb0d8cd3ca6bd4c56331b1722b30d8f48f9a45ece6e`

```dockerfile
```

-	Layers:
	-	`sha256:cc53a730eadb9784a7c191236378a7bcf219afa01f680521eb4bddf1d8ac993e`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 15.6 MB (15599095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e5657bfd53d43e028eb9d10e36db17bcc612d8fae30e5fe0fb076caa4b489b`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:8173985fad86853be81c2d2d427c1a22ad9d919982c5feb33ee56cc79a4b3c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579415232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e17162e2db334c9d6ff28fbd81344a20a803fde6a517c1c9410e6078a5a45d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731d58cf259468f5a31e00d6a586bde147720039c92e6c1ff4cb48a5dd996ae`  
		Last Modified: Wed, 11 Jun 2025 00:00:38 GMT  
		Size: 24.9 MB (24855706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce073e7b00b22009464483e266ff8ba48a8c0db86f16c877aa302337bbed6e9`  
		Last Modified: Wed, 11 Jun 2025 01:13:32 GMT  
		Size: 66.2 MB (66225240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75453a9e8c0ecda25b39aaabe16c9694b0bdb799dbc4bb61d1d0aee7d8b70850`  
		Last Modified: Wed, 11 Jun 2025 02:15:24 GMT  
		Size: 210.3 MB (210300359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a8e4b0736bc7a3d22fb842ad0ee81737c0ed14f5fe26606d2f4b5123616b6`  
		Last Modified: Wed, 11 Jun 2025 06:01:45 GMT  
		Size: 228.6 MB (228556453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ab0c67f770b8da0cbe9479ecec374333e09badd00136782ce748b9cd17e281c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273c89500eb4e84dfb414ccb465c200b7f2a92f66f0b44e6f219b7dde68417b4`

```dockerfile
```

-	Layers:
	-	`sha256:dc04aee6f7f1d600381837690bbefc0648653c65ede9e2ecb6dc60dd7740d0c3`  
		Last Modified: Wed, 11 Jun 2025 05:45:01 GMT  
		Size: 15.8 MB (15839332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a2d3bfd52375162462af27b77692b39e0868ce869675ce142d35c98dcb3f11`  
		Last Modified: Wed, 11 Jun 2025 05:45:02 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:294e06b00a43a648e43744691fbef73c1bdb451465ac350c76f736ed8a50b602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639200335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98218e5b1f057d84b638dd735f30b4a14abac5bb993b7561c9580a3babcd22dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Tue, 03 Jun 2025 13:36:57 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Tue, 03 Jun 2025 13:36:59 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5288618fea79e9a348995382235e6bee52819db4047a345ffaeaddd2b82e06`  
		Last Modified: Tue, 03 Jun 2025 13:37:01 GMT  
		Size: 214.4 MB (214416172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acddbc7af9fd8740373f8026a505be271623021d28c5aaf7cf9cfce5371e307`  
		Last Modified: Tue, 03 Jun 2025 15:36:39 GMT  
		Size: 277.0 MB (276955569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:60293968af0cc8afff5372a51d16244ad649290286e9457b6475a872eaf44c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15558952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90744ca96e8742bd842f46bb381ee8f2bd14a575fbfcf610a629445664ae33b`

```dockerfile
```

-	Layers:
	-	`sha256:e7bef55039062c7c4ae93c0994d2baa58cc23620f26310f07c85affb73ade0e6`  
		Last Modified: Tue, 03 Jun 2025 15:36:29 GMT  
		Size: 15.5 MB (15545745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ac5c316843cde59da34e1480f62e0a90b78ace51a57f9f67917ce2812741f6`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b9f17d320e48e042011cee37b615b2594ca1ac94588789d0978ac65e5e9671b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604371175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7ddbb7c8c246892af6179b2b4a9b8f8ceb4a0b60eff22c4736c5eaaf52b114`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Tue, 03 Jun 2025 13:37:08 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Tue, 03 Jun 2025 13:37:11 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3151505c70d8a7022bb518bbfce9c7488d1dd6ab624e1d96b883eb0654da7562`  
		Last Modified: Tue, 03 Jun 2025 13:37:22 GMT  
		Size: 183.4 MB (183405201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b0882d1ed7e92235dfca31dcc58a7de4c5cad3b764f0fe10874904586c5009`  
		Last Modified: Tue, 03 Jun 2025 14:16:08 GMT  
		Size: 286.3 MB (286308749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:751099b710c1a89fa55e82f9bc0fabfd70cb451e25cfbc7fc9449cc3fec7df28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15394148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd99f87c0d557b247c0e2c29a586dd93187c2ded1f463a78dd244eed473ac43a`

```dockerfile
```

-	Layers:
	-	`sha256:2d523435dd3012b7c822fc76bd1967e45ece2c7c3cda49a5a98a4c7c9fa13591`  
		Last Modified: Tue, 03 Jun 2025 15:36:32 GMT  
		Size: 15.4 MB (15381009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d39102b0130d44f2ec934dd1a55a3718747eb90d0591508f65d806ba52f578`  
		Last Modified: Tue, 03 Jun 2025 15:36:31 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:acd48e9a3f1a6cbfe9de41c88984b9dffa24c4e3e1f881d00c1b99145a0731e2
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
$ docker pull rust@sha256:867389037b7b993d5901a4dc22f719439d56df6322ae8ee5b3d659164ad8a90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526485218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34027bad41e7c5a2dfde8329ad0cdc735ca4cf8afc2bda755755a229a103d19d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2678613884c2f141cc551880b1a1587f0c890606a900bbac5a1ace2645be657`  
		Last Modified: Wed, 11 Jun 2025 00:02:35 GMT  
		Size: 54.8 MB (54757363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c6624995870ade650aaf0f5b37565d2e41e2500e8105fd69b79900eef086cf`  
		Last Modified: Wed, 11 Jun 2025 02:16:19 GMT  
		Size: 197.1 MB (197142069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40689c5eb1b4170233c72a76fb229e2b672f3ecbe0dfaba41511809c1f0054be`  
		Last Modified: Wed, 11 Jun 2025 03:20:02 GMT  
		Size: 205.1 MB (205065865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6939a7548b0bfc37a63c429bda574a8467fe2f00ec42b56a2d48f8407fa16a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15475148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6174e312182a700930c62add7e8dbe79bc0b6c7a153f83b5b3a5b150e2bedd3f`

```dockerfile
```

-	Layers:
	-	`sha256:82873fb0fa119fd347188508fb45ca824a73b0d6afc0611c941197f4af538f52`  
		Last Modified: Wed, 11 Jun 2025 05:44:34 GMT  
		Size: 15.5 MB (15463899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:782b06ea0a8cdf38dbf3b8fb9b63fa091b5c73b1d89bbfbd4c7a88c3356f08c8`  
		Last Modified: Wed, 11 Jun 2025 05:44:35 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:f0099d1100af3de76397f6b72386fb82e5bfe767c199e3af9dacabcb847cd818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.4 MB (530413542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a851fda81799e9f774be69c775a4b41a18a92ffb711d53f4a2fb7adbae061b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
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
	-	`sha256:2bf062f1f44f96722293994387f4b88016e2f0a9f49c7f09b2ceffefc7717199`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 49.0 MB (49041988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933c7aef3dae867caad0cbafef5672fb39317c04b3bf8bff0868bf265098c4de`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 14.9 MB (14880519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0144e65734487c61a592b9ecd7d576c77bc270bd5d65049de36718f77416c6`  
		Last Modified: Tue, 03 Jun 2025 14:32:58 GMT  
		Size: 50.6 MB (50631322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c9ac1f243c709a0fa1779761ca68b4f1c6b9419089c5cd54dcb97bb3d22f54`  
		Last Modified: Tue, 03 Jun 2025 14:33:03 GMT  
		Size: 167.6 MB (167578499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae8b0608788d75c99991c8f9c893341f4d11f3bc4aab4994d6807ed4b8d8163`  
		Last Modified: Thu, 05 Jun 2025 16:53:56 GMT  
		Size: 248.3 MB (248281214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:2cde4e1249e67514f7134d4cbb09b7ee38dd9714da18dcad9d4f654e29137c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14985623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a5ac1d1f5eb5b234db53835a6e11e4c5bf285fcac3a9d866d14a491a75c58d`

```dockerfile
```

-	Layers:
	-	`sha256:482f3adc2f97de782cc024fa5f52aa7dc9524f1440c109d95f33f0532d4878ff`  
		Last Modified: Wed, 11 Jun 2025 05:44:45 GMT  
		Size: 15.0 MB (14974298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ee59cf0e8a7913c311c3a1e425258ded463181f50bd06e068c6172b8725b4d`  
		Last Modified: Wed, 11 Jun 2025 05:44:46 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d9a2d79db5bd7b83232ed720e7460b712a4b3e4928d685f2235c2bf3ba8d5d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486978031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43e429bad1c4ae05ed881da09a277098e088e0e2baa6160638701e0d8dbc76a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a602f78cf8d696db9521d18affb7ecdb79ff690533efae26e3bdb1544cb1752`  
		Last Modified: Tue, 03 Jun 2025 13:31:09 GMT  
		Size: 15.8 MB (15750382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1b27af19f7550ac0d9c38bf6bcf26ba7eb53984e7e5e0886342816133c76e`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 54.9 MB (54853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d0d4413e7427c3ec24a23fc978dced4b2de0294ec9d2e02645e0f62aa2de32`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 190.0 MB (190044698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79cea524fba17622c1c30c1189d43e20ecef3a912b0c98eade8501625fc699b`  
		Last Modified: Tue, 03 Jun 2025 14:20:24 GMT  
		Size: 174.1 MB (174081960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f2c10e422b56bc7311c6e7a10646a49504aad296319e2495888010bf46be7246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe291b6ae25a37ca79695b56eb405b23c994dde1a5c2bb6a0870abd60f6af0d7`

```dockerfile
```

-	Layers:
	-	`sha256:6f81d3f70ab207ec9aadb6eb3a55fe12e8d125470cc73aa35be912d8c206ad93`  
		Last Modified: Wed, 11 Jun 2025 05:44:56 GMT  
		Size: 15.2 MB (15176927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5df7740191a1cba2214b1d3bc8489b68a7b671d82f48fac368d2c938dd1a0a58`  
		Last Modified: Wed, 11 Jun 2025 05:44:57 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:7a323c00d871336669f30ee2a4e6310bf99cea3b3d99279391cef0f3b69e84a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555605760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dabbac26160a93389a46a4bb2dd7d91f7d94dae182f0866446402a405b47539`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
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
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e7c1ed34c380b4c9e9f08e94b0f7b9bf90a0e8c42de246cb4b2159e2126fef`  
		Last Modified: Wed, 11 Jun 2025 00:00:47 GMT  
		Size: 16.3 MB (16268617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3a34392e433938214bbf2cba34365a474d819c470686803059c6d8390cf680`  
		Last Modified: Wed, 11 Jun 2025 01:13:31 GMT  
		Size: 56.0 MB (56049939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fc14c21031cb8eae2e7bca81acab0fca46817b5d8a4fa7fbfb97ff76557da5`  
		Last Modified: Wed, 11 Jun 2025 02:14:17 GMT  
		Size: 200.0 MB (200041378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f45e8e404b579a46068dee78945e0a0853c35cfb3c8a243538f86ff1821f17b`  
		Last Modified: Wed, 11 Jun 2025 09:54:26 GMT  
		Size: 228.6 MB (228555814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:63ea2ff898633a248c8bed35c0c0507387f1f57579f214745875538a0a8db1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f08987abd3e9f97128af9ebb7b448c5fb3e5ea5ab678209c26dcd46460e41e`

```dockerfile
```

-	Layers:
	-	`sha256:49ffb54271663c1d37909753b4895c96d08d07308be90ee479ef685461712fba`  
		Last Modified: Wed, 11 Jun 2025 05:45:08 GMT  
		Size: 15.5 MB (15450601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:191e5f9bf2a3f582caff72f6b5628f333cb7c8de24c23c3ea181aad5630b3378`  
		Last Modified: Wed, 11 Jun 2025 05:45:09 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:437507c3e719e4f968033b88d851ffa9f5aceeb2dcc2482cc6cb7647811a55eb
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
$ docker pull rust@sha256:c6d2b4f8115be78af2a07072f61cffbbb4d6c93b55a4712b922fb7391db6a2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3a4353cc539aea8fad45dd0dc90225aa41fc00a850fec6c15024aa793caa8f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb49401afa0e17bb5553a2c29d1dfcf82e44a6f845092a3e727d07c58cae51e`  
		Last Modified: Wed, 11 Jun 2025 02:46:35 GMT  
		Size: 275.8 MB (275821770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b992a82898a09273268714a1bee7910884463b9c54cff38b0a9aaed379224967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0efaf5c9b3bde5d5403cd7bfe7cd6cffebb0c548fad83f1c45b60d09237485d`

```dockerfile
```

-	Layers:
	-	`sha256:1444619cb92821045d11ffb02735da01990b56835388b8489569925a16c9a85b`  
		Last Modified: Wed, 11 Jun 2025 02:44:27 GMT  
		Size: 4.1 MB (4093196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860531365ea841bb950e17b4e50e3de256a47221cfdf954a40ea40c86c3dee21`  
		Last Modified: Wed, 11 Jun 2025 02:44:28 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:966e7302a5f24503c2fb6de767fae05595b40e37222459764a0a385ec37af077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320043588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b958cc8bdf7ee0e305edf9ce0e0863ceab33ff294219118e308d1cb2cae0aa9c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10dd721eeaf60b511757cc253292582f2dbe051a02adf667aa8ac4ba94997f0`  
		Last Modified: Wed, 11 Jun 2025 12:01:23 GMT  
		Size: 296.1 MB (296104844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:961687e45e0a213ac59675555b8ef714187ab0f3940ca58601da576f49066253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cc0add7a9f0b20fbb1b6d07518f411b4aeaa40dda619c70a752aedda655f1e`

```dockerfile
```

-	Layers:
	-	`sha256:4a53c52228ba7e41746447e406b7d8ce69b8ad263bd576e3ddb52841ae765dab`  
		Last Modified: Wed, 11 Jun 2025 11:44:27 GMT  
		Size: 3.9 MB (3907625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d0c6505620255b5d1bd1af5fa4ed9ed1f6a644865f9168f949f8fad11a10d0`  
		Last Modified: Wed, 11 Jun 2025 11:44:28 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0e216c245a1044e77982d24fd09991448bcd12648115cd6bf2ce1c3d63633a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268005202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834da5b79b78574e38bf973a76161d294a637d950101652138b9dbb92595d5ae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3835d9003112b328f6866eb687138cc59ca3dea0da56c9da555f235723c3a464`  
		Last Modified: Wed, 11 Jun 2025 08:47:07 GMT  
		Size: 239.9 MB (239927527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:2bcd57c614490ddc32c882435e924dcf857670d889481a167b10104b8f71d03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44c4ec5937533284046291218fb2b0376ff4649f1d44f388921b997949dc39f`

```dockerfile
```

-	Layers:
	-	`sha256:a7c21ba2560f3f989e8e7892ec85f8ed9b4fb76fabd4e88ec1e92f54a6de3fb9`  
		Last Modified: Wed, 11 Jun 2025 08:44:36 GMT  
		Size: 4.1 MB (4115540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168233367a2fd0fd2e5e9d69c0e40d5ef353bc704f5cebd9ec8a8b20a7a53703`  
		Last Modified: Wed, 11 Jun 2025 08:44:37 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:2ad11b3f0daccba195c8a3e2d537873b28c0a4d9739f06cc67c58451bf7a42b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325379390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b7914ccdd8d8409e9d85ee45f9969a13ef81e3e7ca5cd62b402205104f6d62`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7541639b044ca0ee0b02dbb730ab58d7da071f667f2a37ab0173489a979a307`  
		Last Modified: Wed, 11 Jun 2025 03:02:06 GMT  
		Size: 296.2 MB (296166957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:96ac86d3fdb37019662687ae8d46c3b145d264dcac844eb7d01cb9fb312769af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b424745a3a740149528fb53d8e6c563c3eeb9457ce88ec0538e221a0ffedf4f4`

```dockerfile
```

-	Layers:
	-	`sha256:6805d028c613af8d87b3ba1f5f56ae1c8e543065cde206869d7031d4b89fee3a`  
		Last Modified: Wed, 11 Jun 2025 02:44:44 GMT  
		Size: 4.1 MB (4072559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc4f4c22e4ea63b843fa608be1c31913653a04d371f1d372f63ab39cdf0fec2`  
		Last Modified: Wed, 11 Jun 2025 02:44:45 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:333d0518b417fd65a06c5a0ee4217fe07e9345093922191979f25a8901395ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377793386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43dd89cf4392e35cda901f980625fedd6b33b8ca171df7416f97273cee5f5fe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641961947f2e89b9782726648e622e267f8a2e965318c701be9c3141d43f9f5`  
		Last Modified: Wed, 11 Jun 2025 09:01:40 GMT  
		Size: 345.7 MB (345720591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:eb1a17643ff56aa1c2370c7f17f04522bf68c405f72150edd08aac2bf0398359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4078847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadaab8a496b8047c9ae84aa96b01e8a4a8c05f00eb3dfe6a62795d3119938d7`

```dockerfile
```

-	Layers:
	-	`sha256:50bbf10950c98ad566b72902fa2c8a087e58b6c3b3b265711bcaa1330922dbb3`  
		Last Modified: Wed, 11 Jun 2025 08:44:44 GMT  
		Size: 4.1 MB (4065509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60fecd5b455a4ae648136c59e20d9e13d41c7aef26ed54572d1a86744ccf3ef0`  
		Last Modified: Wed, 11 Jun 2025 08:44:45 GMT  
		Size: 13.3 KB (13338 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:5faea305cb32004ab4694cf9be72db317b86544c70cef24a43c9863e756ea6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363336119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f475f06d4297efbaf55ad8aae30d81a630a62cdd9286374386ae9d5facc0082e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f552a08d6186725df4030ad88bf2b444cc4868a9bfb86570d7cf36dd450471ee`  
		Last Modified: Wed, 11 Jun 2025 09:02:21 GMT  
		Size: 336.4 MB (336448266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:af734c9315ffbb0607238ba1205d3a3ba0250e7a63158b73cdc27e135f406e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc43a07563773310da6d9a09b86d0264d7db9b6542b5c600d604a26301fad5d`

```dockerfile
```

-	Layers:
	-	`sha256:76749c6d7cca227b6b9fa93d011effbc232138d91f89ff0944eb8c07b9179bf0`  
		Last Modified: Wed, 11 Jun 2025 08:44:50 GMT  
		Size: 3.9 MB (3930874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d70369bbe1eee7920586d7a5d9d0ce8a7f8a4c869fb9f9c0fa15589bd6cfb5c`  
		Last Modified: Wed, 11 Jun 2025 08:44:51 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:437507c3e719e4f968033b88d851ffa9f5aceeb2dcc2482cc6cb7647811a55eb
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
$ docker pull rust@sha256:c6d2b4f8115be78af2a07072f61cffbbb4d6c93b55a4712b922fb7391db6a2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3a4353cc539aea8fad45dd0dc90225aa41fc00a850fec6c15024aa793caa8f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb49401afa0e17bb5553a2c29d1dfcf82e44a6f845092a3e727d07c58cae51e`  
		Last Modified: Wed, 11 Jun 2025 02:46:35 GMT  
		Size: 275.8 MB (275821770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b992a82898a09273268714a1bee7910884463b9c54cff38b0a9aaed379224967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0efaf5c9b3bde5d5403cd7bfe7cd6cffebb0c548fad83f1c45b60d09237485d`

```dockerfile
```

-	Layers:
	-	`sha256:1444619cb92821045d11ffb02735da01990b56835388b8489569925a16c9a85b`  
		Last Modified: Wed, 11 Jun 2025 02:44:27 GMT  
		Size: 4.1 MB (4093196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860531365ea841bb950e17b4e50e3de256a47221cfdf954a40ea40c86c3dee21`  
		Last Modified: Wed, 11 Jun 2025 02:44:28 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:966e7302a5f24503c2fb6de767fae05595b40e37222459764a0a385ec37af077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320043588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b958cc8bdf7ee0e305edf9ce0e0863ceab33ff294219118e308d1cb2cae0aa9c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10dd721eeaf60b511757cc253292582f2dbe051a02adf667aa8ac4ba94997f0`  
		Last Modified: Wed, 11 Jun 2025 12:01:23 GMT  
		Size: 296.1 MB (296104844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:961687e45e0a213ac59675555b8ef714187ab0f3940ca58601da576f49066253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cc0add7a9f0b20fbb1b6d07518f411b4aeaa40dda619c70a752aedda655f1e`

```dockerfile
```

-	Layers:
	-	`sha256:4a53c52228ba7e41746447e406b7d8ce69b8ad263bd576e3ddb52841ae765dab`  
		Last Modified: Wed, 11 Jun 2025 11:44:27 GMT  
		Size: 3.9 MB (3907625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d0c6505620255b5d1bd1af5fa4ed9ed1f6a644865f9168f949f8fad11a10d0`  
		Last Modified: Wed, 11 Jun 2025 11:44:28 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0e216c245a1044e77982d24fd09991448bcd12648115cd6bf2ce1c3d63633a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268005202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834da5b79b78574e38bf973a76161d294a637d950101652138b9dbb92595d5ae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3835d9003112b328f6866eb687138cc59ca3dea0da56c9da555f235723c3a464`  
		Last Modified: Wed, 11 Jun 2025 08:47:07 GMT  
		Size: 239.9 MB (239927527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2bcd57c614490ddc32c882435e924dcf857670d889481a167b10104b8f71d03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44c4ec5937533284046291218fb2b0376ff4649f1d44f388921b997949dc39f`

```dockerfile
```

-	Layers:
	-	`sha256:a7c21ba2560f3f989e8e7892ec85f8ed9b4fb76fabd4e88ec1e92f54a6de3fb9`  
		Last Modified: Wed, 11 Jun 2025 08:44:36 GMT  
		Size: 4.1 MB (4115540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168233367a2fd0fd2e5e9d69c0e40d5ef353bc704f5cebd9ec8a8b20a7a53703`  
		Last Modified: Wed, 11 Jun 2025 08:44:37 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:2ad11b3f0daccba195c8a3e2d537873b28c0a4d9739f06cc67c58451bf7a42b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325379390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b7914ccdd8d8409e9d85ee45f9969a13ef81e3e7ca5cd62b402205104f6d62`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7541639b044ca0ee0b02dbb730ab58d7da071f667f2a37ab0173489a979a307`  
		Last Modified: Wed, 11 Jun 2025 03:02:06 GMT  
		Size: 296.2 MB (296166957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:96ac86d3fdb37019662687ae8d46c3b145d264dcac844eb7d01cb9fb312769af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b424745a3a740149528fb53d8e6c563c3eeb9457ce88ec0538e221a0ffedf4f4`

```dockerfile
```

-	Layers:
	-	`sha256:6805d028c613af8d87b3ba1f5f56ae1c8e543065cde206869d7031d4b89fee3a`  
		Last Modified: Wed, 11 Jun 2025 02:44:44 GMT  
		Size: 4.1 MB (4072559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc4f4c22e4ea63b843fa608be1c31913653a04d371f1d372f63ab39cdf0fec2`  
		Last Modified: Wed, 11 Jun 2025 02:44:45 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:333d0518b417fd65a06c5a0ee4217fe07e9345093922191979f25a8901395ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377793386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43dd89cf4392e35cda901f980625fedd6b33b8ca171df7416f97273cee5f5fe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641961947f2e89b9782726648e622e267f8a2e965318c701be9c3141d43f9f5`  
		Last Modified: Wed, 11 Jun 2025 09:01:40 GMT  
		Size: 345.7 MB (345720591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:eb1a17643ff56aa1c2370c7f17f04522bf68c405f72150edd08aac2bf0398359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4078847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadaab8a496b8047c9ae84aa96b01e8a4a8c05f00eb3dfe6a62795d3119938d7`

```dockerfile
```

-	Layers:
	-	`sha256:50bbf10950c98ad566b72902fa2c8a087e58b6c3b3b265711bcaa1330922dbb3`  
		Last Modified: Wed, 11 Jun 2025 08:44:44 GMT  
		Size: 4.1 MB (4065509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60fecd5b455a4ae648136c59e20d9e13d41c7aef26ed54572d1a86744ccf3ef0`  
		Last Modified: Wed, 11 Jun 2025 08:44:45 GMT  
		Size: 13.3 KB (13338 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:5faea305cb32004ab4694cf9be72db317b86544c70cef24a43c9863e756ea6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363336119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f475f06d4297efbaf55ad8aae30d81a630a62cdd9286374386ae9d5facc0082e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f552a08d6186725df4030ad88bf2b444cc4868a9bfb86570d7cf36dd450471ee`  
		Last Modified: Wed, 11 Jun 2025 09:02:21 GMT  
		Size: 336.4 MB (336448266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:af734c9315ffbb0607238ba1205d3a3ba0250e7a63158b73cdc27e135f406e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc43a07563773310da6d9a09b86d0264d7db9b6542b5c600d604a26301fad5d`

```dockerfile
```

-	Layers:
	-	`sha256:76749c6d7cca227b6b9fa93d011effbc232138d91f89ff0944eb8c07b9179bf0`  
		Last Modified: Wed, 11 Jun 2025 08:44:50 GMT  
		Size: 3.9 MB (3930874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d70369bbe1eee7920586d7a5d9d0ce8a7f8a4c869fb9f9c0fa15589bd6cfb5c`  
		Last Modified: Wed, 11 Jun 2025 08:44:51 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:c8bfa46d68a20e878e316e8302790d5f8c7410c56e35b562507d50f2bec64dd7
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
$ docker pull rust@sha256:39269e5da7fa88d82b633d74443d591bb0b7ec42c04e303356f7263217cf3e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295462508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b70ff91aa20633a2a939769ff5ae727e5dbad08a87aaa6968d3e778b11dad`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986242588b209fdbc06bae0292eda94e58818e8a997967091183318a0308eb6`  
		Last Modified: Wed, 11 Jun 2025 02:56:02 GMT  
		Size: 265.2 MB (265206444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f0f37b3d81805c9cc20c545e9fcab988ebfca75fa936074243743ec9af9a0a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435f25bbb55b5abd07537765c02175b2a0befbf9ea8cefdadb05f6befa275a57`

```dockerfile
```

-	Layers:
	-	`sha256:aee919936bec441ad56146de620886dedd3530c12ab86907b06458b3830ba6bb`  
		Last Modified: Wed, 11 Jun 2025 02:44:37 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61bcfe58120b961061985920c2c49c43574c0fcce8fd78770660c9b06944591f`  
		Last Modified: Wed, 11 Jun 2025 02:44:38 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:16a08d2d06bd1a9d1d6bde2dc5514183f36dc2f24e13042fc37b0b45ac661e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316099000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc56c85193c27255ecb90408767f9d68c274bc1196f45cb098d5ce6b90ea6678`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:254beacf3f323cf99977d539dcb720dc371b362af3a11b68a1c46f29aa86d29f`  
		Last Modified: Tue, 10 Jun 2025 22:48:19 GMT  
		Size: 25.5 MB (25544195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c2c4f56f4973aa426bbf799db8e68cde4b53a77cca960e30f5cce80bf2aa7f`  
		Last Modified: Wed, 11 Jun 2025 12:21:38 GMT  
		Size: 290.6 MB (290554805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f5ea5defe1c1fe621608dc360df4f5ff331dd46a68fe9aa37f478977462580bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7385c0ef64071bfa1afb032a6713f45d63b380778b4b3148bdc67bd681092a`

```dockerfile
```

-	Layers:
	-	`sha256:608e9b87f0307223cfdd260a571b0d674bd45db8f0fb974229c70dc33c749df4`  
		Last Modified: Wed, 11 Jun 2025 11:44:36 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4761277bd9d0f31fe1e8c4ddddf9957abd97fa921c5288901abe244d8de3cf7d`  
		Last Modified: Wed, 11 Jun 2025 11:44:37 GMT  
		Size: 11.4 KB (11431 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:72a16720d9ddf8a7b2dc8d1b1ace588379ca56d699f1d6ade8c501aff66ba039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258525579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3db1cfb8ec57c2e1c668c37e9498d466e905042d276a2b197a07d85338ee87a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a715c260ee097512a6f8b3db5041836c3694a52db693f5778bada15c1d44f171`  
		Last Modified: Wed, 11 Jun 2025 08:45:36 GMT  
		Size: 229.8 MB (229781394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:49f73dda4259a58747e62e4eb6c4fa65628e9f66ee44bdb93ad3e1d81fb41450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bc9a1161131b8fc7f7a7ab0d7bf7c121e0abf6d42e34c83f9ba766cce41fdd`

```dockerfile
```

-	Layers:
	-	`sha256:d80007aa3456840fd8abcf804d83d4b815f907a4e06448c7f1184528cf123af0`  
		Last Modified: Wed, 11 Jun 2025 08:44:42 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84c11e33c8cd2f4d6be8f5f448f2fb501785b8e526b31e414929455af60d8693`  
		Last Modified: Wed, 11 Jun 2025 08:44:43 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:03c578ce0b32d4737deeefaef6ecea7f0ac648ee25d4fee767f79d9c03ae99f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 MB (320511994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32eb66db9a96fa393a694a8787f4a4b6e70abcd17e925bef5790c75a30306789`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:1294ecac50b0f4fe7018ad5e666e6e3c43bd85fbdc4ff68322834fcc70904e3c`  
		Last Modified: Tue, 10 Jun 2025 23:26:42 GMT  
		Size: 31.2 MB (31189682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563e44106503f3d016cd7490b98df9b2aa3762a7e807aeb41e5f65752ff2986`  
		Last Modified: Wed, 11 Jun 2025 04:23:04 GMT  
		Size: 289.3 MB (289322312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f3928a493fc5a10fac96213e189c2986634e3b1873790ff662e908ecc4061a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d790ae2cf1ca80cca939a505b3e9cabef2ef7c0f112000bfef0e26a552016948`

```dockerfile
```

-	Layers:
	-	`sha256:2bb507ca83c8fe4625a244cd017cd4f83a5562e41548cdec226dac403b4e6795`  
		Last Modified: Wed, 11 Jun 2025 02:44:55 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7840377069666033ca9b65919363e35adad8b9fef3da1365876affb656c0d6`  
		Last Modified: Wed, 11 Jun 2025 02:44:56 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87`

```console
$ docker pull rust@sha256:b571d7b2dc7b9154517eeda87c0c3c97865d432e95ec205e34a194fd2baaff1d
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
$ docker pull rust@sha256:6d79f767859a5f025a062505fa9f2c1a041cadafcee71fbcbd226223be462f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553345588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a4a73321e80052e6fcd636dcd4ee26c8fa0ed0d655f95d92276efb7e759cc2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8862a18fa961ebfbac8484877dd4894e96ee88177d8c4f1f54d9727262b7d`  
		Last Modified: Wed, 11 Jun 2025 02:16:04 GMT  
		Size: 211.4 MB (211370316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d73d009ce498344941c85ff822a919ac7bb8976fd68dc8174f43a594bb3fa5`  
		Last Modified: Wed, 11 Jun 2025 03:21:03 GMT  
		Size: 205.1 MB (205065498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87` - unknown; unknown

```console
$ docker pull rust@sha256:503b69f42140f797db581680ee944348a715f85e374bf0f64688bb5e2d7f36ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15875572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9733726f707a166e40276a18d11a14103319579caa5d58f7e146f38d2b2cbe0d`

```dockerfile
```

-	Layers:
	-	`sha256:7fea0bce605acbffe3ad3faddcc83eebdef406125bb53e8a4ea980a11ae3fe32`  
		Last Modified: Wed, 11 Jun 2025 05:44:23 GMT  
		Size: 15.9 MB (15862434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8529bb6f4380c5ac83f220695448a518ba1d0d4b38c355cab9e014939ba116b`  
		Last Modified: Wed, 11 Jun 2025 05:44:24 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87` - linux; arm variant v7

```console
$ docker pull rust@sha256:72b485162489d2c8c49c305dd8b6ba86d4ff05ad986dfc71c07c9cf752fb23b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549362604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c922227a2a41f42eae2eebb9844a4b1e45540c0b00068b270c49c1a1e0b764`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22ee2db9f8d2ea3317ceb36f4b9bc7895f6cb8402903d639c8083eaec948450`  
		Last Modified: Tue, 03 Jun 2025 13:39:41 GMT  
		Size: 175.3 MB (175297793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92df434dc3b1ce2413f6828ef2e4c81ee8a8cef9cbe94a7d2215ad2bd340b292`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 248.3 MB (248281119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87` - unknown; unknown

```console
$ docker pull rust@sha256:2e7ce19770e0e30560aa4a23ada499e5a679b9dd1f61f479fe8d5abee6df0137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15386282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e40b43bdd8233f500a8bec0378ba7ac318dee0cafb4b7f582f11e2585a0396`

```dockerfile
```

-	Layers:
	-	`sha256:f8c270ee20e4767bc254f12fd15b19ddfb7c9f9a382a752ada7fd70bb37b3cc8`  
		Last Modified: Tue, 03 Jun 2025 15:36:17 GMT  
		Size: 15.4 MB (15373035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d32c5949c1f294d1c9fdbee6216a2148b76a885326b5d0372c69b726ab518b0`  
		Last Modified: Tue, 03 Jun 2025 15:36:16 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:40b030bf2085108f7fe5f75de0454fd4f6f855182477906360f40c0c29e95ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513085197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cecf015e8a7925026c922f69a93f75798f571a03fe30546ac7915e8760aaaa9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ee5cb7152015437e4a9b3066ae9e25a26a3bef6617d0b7f25368511c2d954`  
		Last Modified: Tue, 03 Jun 2025 13:30:35 GMT  
		Size: 202.8 MB (202762554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8a70e7346d3f568e98a68fc27e54274c16511edcd67498ae24761da6880cf6`  
		Last Modified: Tue, 03 Jun 2025 13:33:54 GMT  
		Size: 174.1 MB (174082075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87` - unknown; unknown

```console
$ docker pull rust@sha256:9719468f301df89ccc1071537f751d5e28f0c45df8834a133614066e3f97fd22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15612386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27147e11d32faab39878abb0d8cd3ca6bd4c56331b1722b30d8f48f9a45ece6e`

```dockerfile
```

-	Layers:
	-	`sha256:cc53a730eadb9784a7c191236378a7bcf219afa01f680521eb4bddf1d8ac993e`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 15.6 MB (15599095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e5657bfd53d43e028eb9d10e36db17bcc612d8fae30e5fe0fb076caa4b489b`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87` - linux; 386

```console
$ docker pull rust@sha256:8173985fad86853be81c2d2d427c1a22ad9d919982c5feb33ee56cc79a4b3c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579415232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e17162e2db334c9d6ff28fbd81344a20a803fde6a517c1c9410e6078a5a45d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731d58cf259468f5a31e00d6a586bde147720039c92e6c1ff4cb48a5dd996ae`  
		Last Modified: Wed, 11 Jun 2025 00:00:38 GMT  
		Size: 24.9 MB (24855706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce073e7b00b22009464483e266ff8ba48a8c0db86f16c877aa302337bbed6e9`  
		Last Modified: Wed, 11 Jun 2025 01:13:32 GMT  
		Size: 66.2 MB (66225240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75453a9e8c0ecda25b39aaabe16c9694b0bdb799dbc4bb61d1d0aee7d8b70850`  
		Last Modified: Wed, 11 Jun 2025 02:15:24 GMT  
		Size: 210.3 MB (210300359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a8e4b0736bc7a3d22fb842ad0ee81737c0ed14f5fe26606d2f4b5123616b6`  
		Last Modified: Wed, 11 Jun 2025 06:01:45 GMT  
		Size: 228.6 MB (228556453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87` - unknown; unknown

```console
$ docker pull rust@sha256:ab0c67f770b8da0cbe9479ecec374333e09badd00136782ce748b9cd17e281c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273c89500eb4e84dfb414ccb465c200b7f2a92f66f0b44e6f219b7dde68417b4`

```dockerfile
```

-	Layers:
	-	`sha256:dc04aee6f7f1d600381837690bbefc0648653c65ede9e2ecb6dc60dd7740d0c3`  
		Last Modified: Wed, 11 Jun 2025 05:45:01 GMT  
		Size: 15.8 MB (15839332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a2d3bfd52375162462af27b77692b39e0868ce869675ce142d35c98dcb3f11`  
		Last Modified: Wed, 11 Jun 2025 05:45:02 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87` - linux; ppc64le

```console
$ docker pull rust@sha256:294e06b00a43a648e43744691fbef73c1bdb451465ac350c76f736ed8a50b602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639200335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98218e5b1f057d84b638dd735f30b4a14abac5bb993b7561c9580a3babcd22dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Tue, 03 Jun 2025 13:36:57 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Tue, 03 Jun 2025 13:36:59 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5288618fea79e9a348995382235e6bee52819db4047a345ffaeaddd2b82e06`  
		Last Modified: Tue, 03 Jun 2025 13:37:01 GMT  
		Size: 214.4 MB (214416172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acddbc7af9fd8740373f8026a505be271623021d28c5aaf7cf9cfce5371e307`  
		Last Modified: Tue, 03 Jun 2025 15:36:39 GMT  
		Size: 277.0 MB (276955569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87` - unknown; unknown

```console
$ docker pull rust@sha256:60293968af0cc8afff5372a51d16244ad649290286e9457b6475a872eaf44c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15558952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90744ca96e8742bd842f46bb381ee8f2bd14a575fbfcf610a629445664ae33b`

```dockerfile
```

-	Layers:
	-	`sha256:e7bef55039062c7c4ae93c0994d2baa58cc23620f26310f07c85affb73ade0e6`  
		Last Modified: Tue, 03 Jun 2025 15:36:29 GMT  
		Size: 15.5 MB (15545745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ac5c316843cde59da34e1480f62e0a90b78ace51a57f9f67917ce2812741f6`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87` - linux; s390x

```console
$ docker pull rust@sha256:b9f17d320e48e042011cee37b615b2594ca1ac94588789d0978ac65e5e9671b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604371175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7ddbb7c8c246892af6179b2b4a9b8f8ceb4a0b60eff22c4736c5eaaf52b114`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Tue, 03 Jun 2025 13:37:08 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Tue, 03 Jun 2025 13:37:11 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3151505c70d8a7022bb518bbfce9c7488d1dd6ab624e1d96b883eb0654da7562`  
		Last Modified: Tue, 03 Jun 2025 13:37:22 GMT  
		Size: 183.4 MB (183405201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b0882d1ed7e92235dfca31dcc58a7de4c5cad3b764f0fe10874904586c5009`  
		Last Modified: Tue, 03 Jun 2025 14:16:08 GMT  
		Size: 286.3 MB (286308749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87` - unknown; unknown

```console
$ docker pull rust@sha256:751099b710c1a89fa55e82f9bc0fabfd70cb451e25cfbc7fc9449cc3fec7df28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15394148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd99f87c0d557b247c0e2c29a586dd93187c2ded1f463a78dd244eed473ac43a`

```dockerfile
```

-	Layers:
	-	`sha256:2d523435dd3012b7c822fc76bd1967e45ece2c7c3cda49a5a98a4c7c9fa13591`  
		Last Modified: Tue, 03 Jun 2025 15:36:32 GMT  
		Size: 15.4 MB (15381009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d39102b0130d44f2ec934dd1a55a3718747eb90d0591508f65d806ba52f578`  
		Last Modified: Tue, 03 Jun 2025 15:36:31 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87-alpine`

```console
$ docker pull rust@sha256:126df0f2a57e675f9306fe180b833982ffb996e90a92a793bb75253cfeed5475
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.87-alpine` - linux; amd64

```console
$ docker pull rust@sha256:2d5a7e008d9c1e86e54c0a3fffc00399eee945a13aa504fd5faf625e04110bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324451128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa6d9f8b73e08bfab3090a694fb52cea848dd5dfd249f9ff6352477596d5d38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aed27d59f9f3bafc26c73e1fa85e80d10a2b8b6221db885ef03875cbb2a92c3`  
		Last Modified: Tue, 03 Jun 2025 13:33:59 GMT  
		Size: 61.6 MB (61613723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a631e0f5786232f793b7aff2783c3a8252ee122748a6f63fb55c227e00e5002`  
		Last Modified: Tue, 03 Jun 2025 13:34:31 GMT  
		Size: 259.0 MB (259040559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:629b8efb80d6e9a1b711c46acd85e890c1c173b6b976ce39c598a8499163ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc3a74aa6b388d7315bb35c0e0fbd5fb39121d9296330833d8f9b79ffeb6a98`

```dockerfile
```

-	Layers:
	-	`sha256:03bc872db35194e79864e3a72cbb58ddd0548f438a45de2790469bf25a776a5e`  
		Last Modified: Wed, 04 Jun 2025 17:05:12 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c4e51ae8efcd54f48f7d1ced1a254f8c7ca2a7da2e3f6a81c2bedaed4895c9`  
		Last Modified: Wed, 04 Jun 2025 17:05:08 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fa3f412044d347294ad9c21eb3c9922a5e12e57b645ae53bbd27b8bc26173a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327194537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c83a1beaf9ddcfc60c8ec87a69dd7964f3e21bb48de7d530afe4816ca07fb61`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e525acaed56cf743f6ae8ee0c463c3fd7f0e9765bc0faaa7b0119fff2f2db4c4`  
		Last Modified: Tue, 03 Jun 2025 13:34:25 GMT  
		Size: 59.2 MB (59154215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1e992c2528e607b21a005bd23933eb8ae5f77fb262c96790f579f7f863d3c7`  
		Last Modified: Tue, 03 Jun 2025 13:34:30 GMT  
		Size: 263.9 MB (263904381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:0993ebd475453ccc6ded9cffa3118df8be36790fcfcf803fd1bf51bd147a22da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf7cab2f78729c23ec9792c67e373b2906e91cd19fe74c90616e885ff1ddd70`

```dockerfile
```

-	Layers:
	-	`sha256:59310aed03e6f7a9700cd2820322b4883fea2f9851c2e311a52617955a3abd14`  
		Last Modified: Wed, 04 Jun 2025 17:05:46 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e888f3541888d0dcd1e7f14fca30a9930a25f4836300284c59226514fe4b48`  
		Last Modified: Wed, 04 Jun 2025 17:05:45 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718715b3cbe3b4fd9094909206504e5958585bd739a34dc4fb5b7f6ed2131b8`  
		Last Modified: Fri, 16 May 2025 14:17:43 GMT  
		Size: 55.3 MB (55315586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeb4a9d8a98d7b7dadf2be0b1943267d81b081cb2fb12a85484c6aaadf235fb`  
		Last Modified: Fri, 16 May 2025 14:17:57 GMT  
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
		Last Modified: Thu, 15 May 2025 20:44:31 GMT  
		Size: 711.8 KB (711789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a9394ddea85fc3e016d5927f8ce6a38638e7c7eeea1996460a0e68f6915e5c6`  
		Last Modified: Thu, 15 May 2025 20:44:31 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c6aa5430354637d99185e3c6f997bb89b34d0340d714c59489470f3b28fb00`  
		Last Modified: Thu, 08 May 2025 23:40:24 GMT  
		Size: 53.0 MB (52950277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d7b743d7f5864c65b2894547a9334b33385928622ae90e6a32c6e8856c668`  
		Last Modified: Fri, 16 May 2025 14:28:10 GMT  
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
		Last Modified: Mon, 09 Jun 2025 05:43:46 GMT  
		Size: 747.7 KB (747721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5df0c715639e649fb2f087e25e05ab1d51803c9e80193b7ded83d66aa0f06e`  
		Last Modified: Mon, 09 Jun 2025 05:43:46 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b343ca42d769a088aad30a06435916be946b7bd77c275c4c48aa9c02d07ebc6`  
		Last Modified: Thu, 15 May 2025 20:45:48 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0312ddedcb8a05877b03a2214ddd4942d87d6bd8684a5f5bc0353f72d76def`  
		Last Modified: Thu, 15 May 2025 20:46:29 GMT  
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
		Last Modified: Thu, 15 May 2025 20:44:27 GMT  
		Size: 783.8 KB (783823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05e06b11fae76f35a913f94980f7b264abfa081dffa29929dd773c6969a089d`  
		Last Modified: Thu, 15 May 2025 20:44:27 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a8d04fc53dbb480e66cf7321229cda858c75a9bfa488474aabc6a3fbc3423`  
		Last Modified: Thu, 08 May 2025 17:05:51 GMT  
		Size: 59.1 MB (59101363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd10981d51d5c4342a74b76870500712f6977bafb0891f69b5b725cd3f83575b`  
		Last Modified: Fri, 16 May 2025 13:16:00 GMT  
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
		Last Modified: Fri, 16 May 2025 14:02:45 GMT  
		Size: 863.4 KB (863409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4799a729390389da9955e76bdba397218c8fff4138d88735449c1364a6120788`  
		Last Modified: Fri, 16 May 2025 14:02:46 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87-alpine3.22`

```console
$ docker pull rust@sha256:126df0f2a57e675f9306fe180b833982ffb996e90a92a793bb75253cfeed5475
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.87-alpine3.22` - linux; amd64

```console
$ docker pull rust@sha256:2d5a7e008d9c1e86e54c0a3fffc00399eee945a13aa504fd5faf625e04110bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324451128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa6d9f8b73e08bfab3090a694fb52cea848dd5dfd249f9ff6352477596d5d38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aed27d59f9f3bafc26c73e1fa85e80d10a2b8b6221db885ef03875cbb2a92c3`  
		Last Modified: Tue, 03 Jun 2025 13:33:59 GMT  
		Size: 61.6 MB (61613723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a631e0f5786232f793b7aff2783c3a8252ee122748a6f63fb55c227e00e5002`  
		Last Modified: Tue, 03 Jun 2025 13:34:31 GMT  
		Size: 259.0 MB (259040559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:629b8efb80d6e9a1b711c46acd85e890c1c173b6b976ce39c598a8499163ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc3a74aa6b388d7315bb35c0e0fbd5fb39121d9296330833d8f9b79ffeb6a98`

```dockerfile
```

-	Layers:
	-	`sha256:03bc872db35194e79864e3a72cbb58ddd0548f438a45de2790469bf25a776a5e`  
		Last Modified: Wed, 04 Jun 2025 17:05:12 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c4e51ae8efcd54f48f7d1ced1a254f8c7ca2a7da2e3f6a81c2bedaed4895c9`  
		Last Modified: Wed, 04 Jun 2025 17:05:08 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fa3f412044d347294ad9c21eb3c9922a5e12e57b645ae53bbd27b8bc26173a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327194537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c83a1beaf9ddcfc60c8ec87a69dd7964f3e21bb48de7d530afe4816ca07fb61`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e525acaed56cf743f6ae8ee0c463c3fd7f0e9765bc0faaa7b0119fff2f2db4c4`  
		Last Modified: Tue, 03 Jun 2025 13:34:25 GMT  
		Size: 59.2 MB (59154215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1e992c2528e607b21a005bd23933eb8ae5f77fb262c96790f579f7f863d3c7`  
		Last Modified: Tue, 03 Jun 2025 13:34:30 GMT  
		Size: 263.9 MB (263904381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:0993ebd475453ccc6ded9cffa3118df8be36790fcfcf803fd1bf51bd147a22da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf7cab2f78729c23ec9792c67e373b2906e91cd19fe74c90616e885ff1ddd70`

```dockerfile
```

-	Layers:
	-	`sha256:59310aed03e6f7a9700cd2820322b4883fea2f9851c2e311a52617955a3abd14`  
		Last Modified: Wed, 04 Jun 2025 17:05:46 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e888f3541888d0dcd1e7f14fca30a9930a25f4836300284c59226514fe4b48`  
		Last Modified: Wed, 04 Jun 2025 17:05:45 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87-bookworm`

```console
$ docker pull rust@sha256:b571d7b2dc7b9154517eeda87c0c3c97865d432e95ec205e34a194fd2baaff1d
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
$ docker pull rust@sha256:6d79f767859a5f025a062505fa9f2c1a041cadafcee71fbcbd226223be462f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553345588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a4a73321e80052e6fcd636dcd4ee26c8fa0ed0d655f95d92276efb7e759cc2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8862a18fa961ebfbac8484877dd4894e96ee88177d8c4f1f54d9727262b7d`  
		Last Modified: Wed, 11 Jun 2025 02:16:04 GMT  
		Size: 211.4 MB (211370316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d73d009ce498344941c85ff822a919ac7bb8976fd68dc8174f43a594bb3fa5`  
		Last Modified: Wed, 11 Jun 2025 03:21:03 GMT  
		Size: 205.1 MB (205065498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:503b69f42140f797db581680ee944348a715f85e374bf0f64688bb5e2d7f36ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15875572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9733726f707a166e40276a18d11a14103319579caa5d58f7e146f38d2b2cbe0d`

```dockerfile
```

-	Layers:
	-	`sha256:7fea0bce605acbffe3ad3faddcc83eebdef406125bb53e8a4ea980a11ae3fe32`  
		Last Modified: Wed, 11 Jun 2025 05:44:23 GMT  
		Size: 15.9 MB (15862434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8529bb6f4380c5ac83f220695448a518ba1d0d4b38c355cab9e014939ba116b`  
		Last Modified: Wed, 11 Jun 2025 05:44:24 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:72b485162489d2c8c49c305dd8b6ba86d4ff05ad986dfc71c07c9cf752fb23b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549362604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c922227a2a41f42eae2eebb9844a4b1e45540c0b00068b270c49c1a1e0b764`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22ee2db9f8d2ea3317ceb36f4b9bc7895f6cb8402903d639c8083eaec948450`  
		Last Modified: Tue, 03 Jun 2025 13:39:41 GMT  
		Size: 175.3 MB (175297793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92df434dc3b1ce2413f6828ef2e4c81ee8a8cef9cbe94a7d2215ad2bd340b292`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 248.3 MB (248281119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2e7ce19770e0e30560aa4a23ada499e5a679b9dd1f61f479fe8d5abee6df0137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15386282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e40b43bdd8233f500a8bec0378ba7ac318dee0cafb4b7f582f11e2585a0396`

```dockerfile
```

-	Layers:
	-	`sha256:f8c270ee20e4767bc254f12fd15b19ddfb7c9f9a382a752ada7fd70bb37b3cc8`  
		Last Modified: Tue, 03 Jun 2025 15:36:17 GMT  
		Size: 15.4 MB (15373035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d32c5949c1f294d1c9fdbee6216a2148b76a885326b5d0372c69b726ab518b0`  
		Last Modified: Tue, 03 Jun 2025 15:36:16 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:40b030bf2085108f7fe5f75de0454fd4f6f855182477906360f40c0c29e95ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513085197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cecf015e8a7925026c922f69a93f75798f571a03fe30546ac7915e8760aaaa9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ee5cb7152015437e4a9b3066ae9e25a26a3bef6617d0b7f25368511c2d954`  
		Last Modified: Tue, 03 Jun 2025 13:30:35 GMT  
		Size: 202.8 MB (202762554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8a70e7346d3f568e98a68fc27e54274c16511edcd67498ae24761da6880cf6`  
		Last Modified: Tue, 03 Jun 2025 13:33:54 GMT  
		Size: 174.1 MB (174082075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9719468f301df89ccc1071537f751d5e28f0c45df8834a133614066e3f97fd22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15612386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27147e11d32faab39878abb0d8cd3ca6bd4c56331b1722b30d8f48f9a45ece6e`

```dockerfile
```

-	Layers:
	-	`sha256:cc53a730eadb9784a7c191236378a7bcf219afa01f680521eb4bddf1d8ac993e`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 15.6 MB (15599095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e5657bfd53d43e028eb9d10e36db17bcc612d8fae30e5fe0fb076caa4b489b`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bookworm` - linux; 386

```console
$ docker pull rust@sha256:8173985fad86853be81c2d2d427c1a22ad9d919982c5feb33ee56cc79a4b3c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579415232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e17162e2db334c9d6ff28fbd81344a20a803fde6a517c1c9410e6078a5a45d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731d58cf259468f5a31e00d6a586bde147720039c92e6c1ff4cb48a5dd996ae`  
		Last Modified: Wed, 11 Jun 2025 00:00:38 GMT  
		Size: 24.9 MB (24855706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce073e7b00b22009464483e266ff8ba48a8c0db86f16c877aa302337bbed6e9`  
		Last Modified: Wed, 11 Jun 2025 01:13:32 GMT  
		Size: 66.2 MB (66225240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75453a9e8c0ecda25b39aaabe16c9694b0bdb799dbc4bb61d1d0aee7d8b70850`  
		Last Modified: Wed, 11 Jun 2025 02:15:24 GMT  
		Size: 210.3 MB (210300359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a8e4b0736bc7a3d22fb842ad0ee81737c0ed14f5fe26606d2f4b5123616b6`  
		Last Modified: Wed, 11 Jun 2025 06:01:45 GMT  
		Size: 228.6 MB (228556453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ab0c67f770b8da0cbe9479ecec374333e09badd00136782ce748b9cd17e281c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273c89500eb4e84dfb414ccb465c200b7f2a92f66f0b44e6f219b7dde68417b4`

```dockerfile
```

-	Layers:
	-	`sha256:dc04aee6f7f1d600381837690bbefc0648653c65ede9e2ecb6dc60dd7740d0c3`  
		Last Modified: Wed, 11 Jun 2025 05:45:01 GMT  
		Size: 15.8 MB (15839332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a2d3bfd52375162462af27b77692b39e0868ce869675ce142d35c98dcb3f11`  
		Last Modified: Wed, 11 Jun 2025 05:45:02 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:294e06b00a43a648e43744691fbef73c1bdb451465ac350c76f736ed8a50b602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639200335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98218e5b1f057d84b638dd735f30b4a14abac5bb993b7561c9580a3babcd22dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Tue, 03 Jun 2025 13:36:57 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Tue, 03 Jun 2025 13:36:59 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5288618fea79e9a348995382235e6bee52819db4047a345ffaeaddd2b82e06`  
		Last Modified: Tue, 03 Jun 2025 13:37:01 GMT  
		Size: 214.4 MB (214416172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acddbc7af9fd8740373f8026a505be271623021d28c5aaf7cf9cfce5371e307`  
		Last Modified: Tue, 03 Jun 2025 15:36:39 GMT  
		Size: 277.0 MB (276955569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:60293968af0cc8afff5372a51d16244ad649290286e9457b6475a872eaf44c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15558952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90744ca96e8742bd842f46bb381ee8f2bd14a575fbfcf610a629445664ae33b`

```dockerfile
```

-	Layers:
	-	`sha256:e7bef55039062c7c4ae93c0994d2baa58cc23620f26310f07c85affb73ade0e6`  
		Last Modified: Tue, 03 Jun 2025 15:36:29 GMT  
		Size: 15.5 MB (15545745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ac5c316843cde59da34e1480f62e0a90b78ace51a57f9f67917ce2812741f6`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b9f17d320e48e042011cee37b615b2594ca1ac94588789d0978ac65e5e9671b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604371175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7ddbb7c8c246892af6179b2b4a9b8f8ceb4a0b60eff22c4736c5eaaf52b114`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Tue, 03 Jun 2025 13:37:08 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Tue, 03 Jun 2025 13:37:11 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3151505c70d8a7022bb518bbfce9c7488d1dd6ab624e1d96b883eb0654da7562`  
		Last Modified: Tue, 03 Jun 2025 13:37:22 GMT  
		Size: 183.4 MB (183405201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b0882d1ed7e92235dfca31dcc58a7de4c5cad3b764f0fe10874904586c5009`  
		Last Modified: Tue, 03 Jun 2025 14:16:08 GMT  
		Size: 286.3 MB (286308749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:751099b710c1a89fa55e82f9bc0fabfd70cb451e25cfbc7fc9449cc3fec7df28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15394148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd99f87c0d557b247c0e2c29a586dd93187c2ded1f463a78dd244eed473ac43a`

```dockerfile
```

-	Layers:
	-	`sha256:2d523435dd3012b7c822fc76bd1967e45ece2c7c3cda49a5a98a4c7c9fa13591`  
		Last Modified: Tue, 03 Jun 2025 15:36:32 GMT  
		Size: 15.4 MB (15381009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d39102b0130d44f2ec934dd1a55a3718747eb90d0591508f65d806ba52f578`  
		Last Modified: Tue, 03 Jun 2025 15:36:31 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87-bullseye`

```console
$ docker pull rust@sha256:acd48e9a3f1a6cbfe9de41c88984b9dffa24c4e3e1f881d00c1b99145a0731e2
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
$ docker pull rust@sha256:867389037b7b993d5901a4dc22f719439d56df6322ae8ee5b3d659164ad8a90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526485218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34027bad41e7c5a2dfde8329ad0cdc735ca4cf8afc2bda755755a229a103d19d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2678613884c2f141cc551880b1a1587f0c890606a900bbac5a1ace2645be657`  
		Last Modified: Wed, 11 Jun 2025 00:02:35 GMT  
		Size: 54.8 MB (54757363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c6624995870ade650aaf0f5b37565d2e41e2500e8105fd69b79900eef086cf`  
		Last Modified: Wed, 11 Jun 2025 02:16:19 GMT  
		Size: 197.1 MB (197142069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40689c5eb1b4170233c72a76fb229e2b672f3ecbe0dfaba41511809c1f0054be`  
		Last Modified: Wed, 11 Jun 2025 03:20:02 GMT  
		Size: 205.1 MB (205065865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6939a7548b0bfc37a63c429bda574a8467fe2f00ec42b56a2d48f8407fa16a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15475148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6174e312182a700930c62add7e8dbe79bc0b6c7a153f83b5b3a5b150e2bedd3f`

```dockerfile
```

-	Layers:
	-	`sha256:82873fb0fa119fd347188508fb45ca824a73b0d6afc0611c941197f4af538f52`  
		Last Modified: Wed, 11 Jun 2025 05:44:34 GMT  
		Size: 15.5 MB (15463899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:782b06ea0a8cdf38dbf3b8fb9b63fa091b5c73b1d89bbfbd4c7a88c3356f08c8`  
		Last Modified: Wed, 11 Jun 2025 05:44:35 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:f0099d1100af3de76397f6b72386fb82e5bfe767c199e3af9dacabcb847cd818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.4 MB (530413542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a851fda81799e9f774be69c775a4b41a18a92ffb711d53f4a2fb7adbae061b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
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
	-	`sha256:2bf062f1f44f96722293994387f4b88016e2f0a9f49c7f09b2ceffefc7717199`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 49.0 MB (49041988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933c7aef3dae867caad0cbafef5672fb39317c04b3bf8bff0868bf265098c4de`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 14.9 MB (14880519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0144e65734487c61a592b9ecd7d576c77bc270bd5d65049de36718f77416c6`  
		Last Modified: Tue, 03 Jun 2025 14:32:58 GMT  
		Size: 50.6 MB (50631322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c9ac1f243c709a0fa1779761ca68b4f1c6b9419089c5cd54dcb97bb3d22f54`  
		Last Modified: Tue, 03 Jun 2025 14:33:03 GMT  
		Size: 167.6 MB (167578499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae8b0608788d75c99991c8f9c893341f4d11f3bc4aab4994d6807ed4b8d8163`  
		Last Modified: Thu, 05 Jun 2025 16:53:56 GMT  
		Size: 248.3 MB (248281214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:2cde4e1249e67514f7134d4cbb09b7ee38dd9714da18dcad9d4f654e29137c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14985623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a5ac1d1f5eb5b234db53835a6e11e4c5bf285fcac3a9d866d14a491a75c58d`

```dockerfile
```

-	Layers:
	-	`sha256:482f3adc2f97de782cc024fa5f52aa7dc9524f1440c109d95f33f0532d4878ff`  
		Last Modified: Wed, 11 Jun 2025 05:44:45 GMT  
		Size: 15.0 MB (14974298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ee59cf0e8a7913c311c3a1e425258ded463181f50bd06e068c6172b8725b4d`  
		Last Modified: Wed, 11 Jun 2025 05:44:46 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d9a2d79db5bd7b83232ed720e7460b712a4b3e4928d685f2235c2bf3ba8d5d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486978031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43e429bad1c4ae05ed881da09a277098e088e0e2baa6160638701e0d8dbc76a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a602f78cf8d696db9521d18affb7ecdb79ff690533efae26e3bdb1544cb1752`  
		Last Modified: Tue, 03 Jun 2025 13:31:09 GMT  
		Size: 15.8 MB (15750382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1b27af19f7550ac0d9c38bf6bcf26ba7eb53984e7e5e0886342816133c76e`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 54.9 MB (54853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d0d4413e7427c3ec24a23fc978dced4b2de0294ec9d2e02645e0f62aa2de32`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 190.0 MB (190044698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79cea524fba17622c1c30c1189d43e20ecef3a912b0c98eade8501625fc699b`  
		Last Modified: Tue, 03 Jun 2025 14:20:24 GMT  
		Size: 174.1 MB (174081960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f2c10e422b56bc7311c6e7a10646a49504aad296319e2495888010bf46be7246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe291b6ae25a37ca79695b56eb405b23c994dde1a5c2bb6a0870abd60f6af0d7`

```dockerfile
```

-	Layers:
	-	`sha256:6f81d3f70ab207ec9aadb6eb3a55fe12e8d125470cc73aa35be912d8c206ad93`  
		Last Modified: Wed, 11 Jun 2025 05:44:56 GMT  
		Size: 15.2 MB (15176927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5df7740191a1cba2214b1d3bc8489b68a7b671d82f48fac368d2c938dd1a0a58`  
		Last Modified: Wed, 11 Jun 2025 05:44:57 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-bullseye` - linux; 386

```console
$ docker pull rust@sha256:7a323c00d871336669f30ee2a4e6310bf99cea3b3d99279391cef0f3b69e84a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555605760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dabbac26160a93389a46a4bb2dd7d91f7d94dae182f0866446402a405b47539`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
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
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e7c1ed34c380b4c9e9f08e94b0f7b9bf90a0e8c42de246cb4b2159e2126fef`  
		Last Modified: Wed, 11 Jun 2025 00:00:47 GMT  
		Size: 16.3 MB (16268617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3a34392e433938214bbf2cba34365a474d819c470686803059c6d8390cf680`  
		Last Modified: Wed, 11 Jun 2025 01:13:31 GMT  
		Size: 56.0 MB (56049939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fc14c21031cb8eae2e7bca81acab0fca46817b5d8a4fa7fbfb97ff76557da5`  
		Last Modified: Wed, 11 Jun 2025 02:14:17 GMT  
		Size: 200.0 MB (200041378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f45e8e404b579a46068dee78945e0a0853c35cfb3c8a243538f86ff1821f17b`  
		Last Modified: Wed, 11 Jun 2025 09:54:26 GMT  
		Size: 228.6 MB (228555814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:63ea2ff898633a248c8bed35c0c0507387f1f57579f214745875538a0a8db1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f08987abd3e9f97128af9ebb7b448c5fb3e5ea5ab678209c26dcd46460e41e`

```dockerfile
```

-	Layers:
	-	`sha256:49ffb54271663c1d37909753b4895c96d08d07308be90ee479ef685461712fba`  
		Last Modified: Wed, 11 Jun 2025 05:45:08 GMT  
		Size: 15.5 MB (15450601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:191e5f9bf2a3f582caff72f6b5628f333cb7c8de24c23c3ea181aad5630b3378`  
		Last Modified: Wed, 11 Jun 2025 05:45:09 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87-slim`

```console
$ docker pull rust@sha256:437507c3e719e4f968033b88d851ffa9f5aceeb2dcc2482cc6cb7647811a55eb
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
$ docker pull rust@sha256:c6d2b4f8115be78af2a07072f61cffbbb4d6c93b55a4712b922fb7391db6a2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3a4353cc539aea8fad45dd0dc90225aa41fc00a850fec6c15024aa793caa8f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb49401afa0e17bb5553a2c29d1dfcf82e44a6f845092a3e727d07c58cae51e`  
		Last Modified: Wed, 11 Jun 2025 02:46:35 GMT  
		Size: 275.8 MB (275821770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b992a82898a09273268714a1bee7910884463b9c54cff38b0a9aaed379224967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0efaf5c9b3bde5d5403cd7bfe7cd6cffebb0c548fad83f1c45b60d09237485d`

```dockerfile
```

-	Layers:
	-	`sha256:1444619cb92821045d11ffb02735da01990b56835388b8489569925a16c9a85b`  
		Last Modified: Wed, 11 Jun 2025 02:44:27 GMT  
		Size: 4.1 MB (4093196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860531365ea841bb950e17b4e50e3de256a47221cfdf954a40ea40c86c3dee21`  
		Last Modified: Wed, 11 Jun 2025 02:44:28 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:966e7302a5f24503c2fb6de767fae05595b40e37222459764a0a385ec37af077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320043588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b958cc8bdf7ee0e305edf9ce0e0863ceab33ff294219118e308d1cb2cae0aa9c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10dd721eeaf60b511757cc253292582f2dbe051a02adf667aa8ac4ba94997f0`  
		Last Modified: Wed, 11 Jun 2025 12:01:23 GMT  
		Size: 296.1 MB (296104844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim` - unknown; unknown

```console
$ docker pull rust@sha256:961687e45e0a213ac59675555b8ef714187ab0f3940ca58601da576f49066253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cc0add7a9f0b20fbb1b6d07518f411b4aeaa40dda619c70a752aedda655f1e`

```dockerfile
```

-	Layers:
	-	`sha256:4a53c52228ba7e41746447e406b7d8ce69b8ad263bd576e3ddb52841ae765dab`  
		Last Modified: Wed, 11 Jun 2025 11:44:27 GMT  
		Size: 3.9 MB (3907625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d0c6505620255b5d1bd1af5fa4ed9ed1f6a644865f9168f949f8fad11a10d0`  
		Last Modified: Wed, 11 Jun 2025 11:44:28 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0e216c245a1044e77982d24fd09991448bcd12648115cd6bf2ce1c3d63633a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268005202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834da5b79b78574e38bf973a76161d294a637d950101652138b9dbb92595d5ae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3835d9003112b328f6866eb687138cc59ca3dea0da56c9da555f235723c3a464`  
		Last Modified: Wed, 11 Jun 2025 08:47:07 GMT  
		Size: 239.9 MB (239927527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim` - unknown; unknown

```console
$ docker pull rust@sha256:2bcd57c614490ddc32c882435e924dcf857670d889481a167b10104b8f71d03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44c4ec5937533284046291218fb2b0376ff4649f1d44f388921b997949dc39f`

```dockerfile
```

-	Layers:
	-	`sha256:a7c21ba2560f3f989e8e7892ec85f8ed9b4fb76fabd4e88ec1e92f54a6de3fb9`  
		Last Modified: Wed, 11 Jun 2025 08:44:36 GMT  
		Size: 4.1 MB (4115540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168233367a2fd0fd2e5e9d69c0e40d5ef353bc704f5cebd9ec8a8b20a7a53703`  
		Last Modified: Wed, 11 Jun 2025 08:44:37 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim` - linux; 386

```console
$ docker pull rust@sha256:2ad11b3f0daccba195c8a3e2d537873b28c0a4d9739f06cc67c58451bf7a42b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325379390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b7914ccdd8d8409e9d85ee45f9969a13ef81e3e7ca5cd62b402205104f6d62`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7541639b044ca0ee0b02dbb730ab58d7da071f667f2a37ab0173489a979a307`  
		Last Modified: Wed, 11 Jun 2025 03:02:06 GMT  
		Size: 296.2 MB (296166957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim` - unknown; unknown

```console
$ docker pull rust@sha256:96ac86d3fdb37019662687ae8d46c3b145d264dcac844eb7d01cb9fb312769af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b424745a3a740149528fb53d8e6c563c3eeb9457ce88ec0538e221a0ffedf4f4`

```dockerfile
```

-	Layers:
	-	`sha256:6805d028c613af8d87b3ba1f5f56ae1c8e543065cde206869d7031d4b89fee3a`  
		Last Modified: Wed, 11 Jun 2025 02:44:44 GMT  
		Size: 4.1 MB (4072559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc4f4c22e4ea63b843fa608be1c31913653a04d371f1d372f63ab39cdf0fec2`  
		Last Modified: Wed, 11 Jun 2025 02:44:45 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:333d0518b417fd65a06c5a0ee4217fe07e9345093922191979f25a8901395ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377793386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43dd89cf4392e35cda901f980625fedd6b33b8ca171df7416f97273cee5f5fe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641961947f2e89b9782726648e622e267f8a2e965318c701be9c3141d43f9f5`  
		Last Modified: Wed, 11 Jun 2025 09:01:40 GMT  
		Size: 345.7 MB (345720591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim` - unknown; unknown

```console
$ docker pull rust@sha256:eb1a17643ff56aa1c2370c7f17f04522bf68c405f72150edd08aac2bf0398359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4078847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadaab8a496b8047c9ae84aa96b01e8a4a8c05f00eb3dfe6a62795d3119938d7`

```dockerfile
```

-	Layers:
	-	`sha256:50bbf10950c98ad566b72902fa2c8a087e58b6c3b3b265711bcaa1330922dbb3`  
		Last Modified: Wed, 11 Jun 2025 08:44:44 GMT  
		Size: 4.1 MB (4065509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60fecd5b455a4ae648136c59e20d9e13d41c7aef26ed54572d1a86744ccf3ef0`  
		Last Modified: Wed, 11 Jun 2025 08:44:45 GMT  
		Size: 13.3 KB (13338 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim` - linux; s390x

```console
$ docker pull rust@sha256:5faea305cb32004ab4694cf9be72db317b86544c70cef24a43c9863e756ea6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363336119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f475f06d4297efbaf55ad8aae30d81a630a62cdd9286374386ae9d5facc0082e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f552a08d6186725df4030ad88bf2b444cc4868a9bfb86570d7cf36dd450471ee`  
		Last Modified: Wed, 11 Jun 2025 09:02:21 GMT  
		Size: 336.4 MB (336448266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim` - unknown; unknown

```console
$ docker pull rust@sha256:af734c9315ffbb0607238ba1205d3a3ba0250e7a63158b73cdc27e135f406e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc43a07563773310da6d9a09b86d0264d7db9b6542b5c600d604a26301fad5d`

```dockerfile
```

-	Layers:
	-	`sha256:76749c6d7cca227b6b9fa93d011effbc232138d91f89ff0944eb8c07b9179bf0`  
		Last Modified: Wed, 11 Jun 2025 08:44:50 GMT  
		Size: 3.9 MB (3930874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d70369bbe1eee7920586d7a5d9d0ce8a7f8a4c869fb9f9c0fa15589bd6cfb5c`  
		Last Modified: Wed, 11 Jun 2025 08:44:51 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87-slim-bookworm`

```console
$ docker pull rust@sha256:437507c3e719e4f968033b88d851ffa9f5aceeb2dcc2482cc6cb7647811a55eb
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
$ docker pull rust@sha256:c6d2b4f8115be78af2a07072f61cffbbb4d6c93b55a4712b922fb7391db6a2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3a4353cc539aea8fad45dd0dc90225aa41fc00a850fec6c15024aa793caa8f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb49401afa0e17bb5553a2c29d1dfcf82e44a6f845092a3e727d07c58cae51e`  
		Last Modified: Wed, 11 Jun 2025 02:46:35 GMT  
		Size: 275.8 MB (275821770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b992a82898a09273268714a1bee7910884463b9c54cff38b0a9aaed379224967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0efaf5c9b3bde5d5403cd7bfe7cd6cffebb0c548fad83f1c45b60d09237485d`

```dockerfile
```

-	Layers:
	-	`sha256:1444619cb92821045d11ffb02735da01990b56835388b8489569925a16c9a85b`  
		Last Modified: Wed, 11 Jun 2025 02:44:27 GMT  
		Size: 4.1 MB (4093196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860531365ea841bb950e17b4e50e3de256a47221cfdf954a40ea40c86c3dee21`  
		Last Modified: Wed, 11 Jun 2025 02:44:28 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:966e7302a5f24503c2fb6de767fae05595b40e37222459764a0a385ec37af077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320043588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b958cc8bdf7ee0e305edf9ce0e0863ceab33ff294219118e308d1cb2cae0aa9c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10dd721eeaf60b511757cc253292582f2dbe051a02adf667aa8ac4ba94997f0`  
		Last Modified: Wed, 11 Jun 2025 12:01:23 GMT  
		Size: 296.1 MB (296104844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:961687e45e0a213ac59675555b8ef714187ab0f3940ca58601da576f49066253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cc0add7a9f0b20fbb1b6d07518f411b4aeaa40dda619c70a752aedda655f1e`

```dockerfile
```

-	Layers:
	-	`sha256:4a53c52228ba7e41746447e406b7d8ce69b8ad263bd576e3ddb52841ae765dab`  
		Last Modified: Wed, 11 Jun 2025 11:44:27 GMT  
		Size: 3.9 MB (3907625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d0c6505620255b5d1bd1af5fa4ed9ed1f6a644865f9168f949f8fad11a10d0`  
		Last Modified: Wed, 11 Jun 2025 11:44:28 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0e216c245a1044e77982d24fd09991448bcd12648115cd6bf2ce1c3d63633a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268005202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834da5b79b78574e38bf973a76161d294a637d950101652138b9dbb92595d5ae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3835d9003112b328f6866eb687138cc59ca3dea0da56c9da555f235723c3a464`  
		Last Modified: Wed, 11 Jun 2025 08:47:07 GMT  
		Size: 239.9 MB (239927527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2bcd57c614490ddc32c882435e924dcf857670d889481a167b10104b8f71d03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44c4ec5937533284046291218fb2b0376ff4649f1d44f388921b997949dc39f`

```dockerfile
```

-	Layers:
	-	`sha256:a7c21ba2560f3f989e8e7892ec85f8ed9b4fb76fabd4e88ec1e92f54a6de3fb9`  
		Last Modified: Wed, 11 Jun 2025 08:44:36 GMT  
		Size: 4.1 MB (4115540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168233367a2fd0fd2e5e9d69c0e40d5ef353bc704f5cebd9ec8a8b20a7a53703`  
		Last Modified: Wed, 11 Jun 2025 08:44:37 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:2ad11b3f0daccba195c8a3e2d537873b28c0a4d9739f06cc67c58451bf7a42b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325379390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b7914ccdd8d8409e9d85ee45f9969a13ef81e3e7ca5cd62b402205104f6d62`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7541639b044ca0ee0b02dbb730ab58d7da071f667f2a37ab0173489a979a307`  
		Last Modified: Wed, 11 Jun 2025 03:02:06 GMT  
		Size: 296.2 MB (296166957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:96ac86d3fdb37019662687ae8d46c3b145d264dcac844eb7d01cb9fb312769af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b424745a3a740149528fb53d8e6c563c3eeb9457ce88ec0538e221a0ffedf4f4`

```dockerfile
```

-	Layers:
	-	`sha256:6805d028c613af8d87b3ba1f5f56ae1c8e543065cde206869d7031d4b89fee3a`  
		Last Modified: Wed, 11 Jun 2025 02:44:44 GMT  
		Size: 4.1 MB (4072559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc4f4c22e4ea63b843fa608be1c31913653a04d371f1d372f63ab39cdf0fec2`  
		Last Modified: Wed, 11 Jun 2025 02:44:45 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:333d0518b417fd65a06c5a0ee4217fe07e9345093922191979f25a8901395ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377793386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43dd89cf4392e35cda901f980625fedd6b33b8ca171df7416f97273cee5f5fe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641961947f2e89b9782726648e622e267f8a2e965318c701be9c3141d43f9f5`  
		Last Modified: Wed, 11 Jun 2025 09:01:40 GMT  
		Size: 345.7 MB (345720591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:eb1a17643ff56aa1c2370c7f17f04522bf68c405f72150edd08aac2bf0398359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4078847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadaab8a496b8047c9ae84aa96b01e8a4a8c05f00eb3dfe6a62795d3119938d7`

```dockerfile
```

-	Layers:
	-	`sha256:50bbf10950c98ad566b72902fa2c8a087e58b6c3b3b265711bcaa1330922dbb3`  
		Last Modified: Wed, 11 Jun 2025 08:44:44 GMT  
		Size: 4.1 MB (4065509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60fecd5b455a4ae648136c59e20d9e13d41c7aef26ed54572d1a86744ccf3ef0`  
		Last Modified: Wed, 11 Jun 2025 08:44:45 GMT  
		Size: 13.3 KB (13338 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:5faea305cb32004ab4694cf9be72db317b86544c70cef24a43c9863e756ea6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363336119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f475f06d4297efbaf55ad8aae30d81a630a62cdd9286374386ae9d5facc0082e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f552a08d6186725df4030ad88bf2b444cc4868a9bfb86570d7cf36dd450471ee`  
		Last Modified: Wed, 11 Jun 2025 09:02:21 GMT  
		Size: 336.4 MB (336448266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:af734c9315ffbb0607238ba1205d3a3ba0250e7a63158b73cdc27e135f406e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc43a07563773310da6d9a09b86d0264d7db9b6542b5c600d604a26301fad5d`

```dockerfile
```

-	Layers:
	-	`sha256:76749c6d7cca227b6b9fa93d011effbc232138d91f89ff0944eb8c07b9179bf0`  
		Last Modified: Wed, 11 Jun 2025 08:44:50 GMT  
		Size: 3.9 MB (3930874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d70369bbe1eee7920586d7a5d9d0ce8a7f8a4c869fb9f9c0fa15589bd6cfb5c`  
		Last Modified: Wed, 11 Jun 2025 08:44:51 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87-slim-bullseye`

```console
$ docker pull rust@sha256:c8bfa46d68a20e878e316e8302790d5f8c7410c56e35b562507d50f2bec64dd7
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
$ docker pull rust@sha256:39269e5da7fa88d82b633d74443d591bb0b7ec42c04e303356f7263217cf3e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295462508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b70ff91aa20633a2a939769ff5ae727e5dbad08a87aaa6968d3e778b11dad`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986242588b209fdbc06bae0292eda94e58818e8a997967091183318a0308eb6`  
		Last Modified: Wed, 11 Jun 2025 02:56:02 GMT  
		Size: 265.2 MB (265206444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f0f37b3d81805c9cc20c545e9fcab988ebfca75fa936074243743ec9af9a0a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435f25bbb55b5abd07537765c02175b2a0befbf9ea8cefdadb05f6befa275a57`

```dockerfile
```

-	Layers:
	-	`sha256:aee919936bec441ad56146de620886dedd3530c12ab86907b06458b3830ba6bb`  
		Last Modified: Wed, 11 Jun 2025 02:44:37 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61bcfe58120b961061985920c2c49c43574c0fcce8fd78770660c9b06944591f`  
		Last Modified: Wed, 11 Jun 2025 02:44:38 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:16a08d2d06bd1a9d1d6bde2dc5514183f36dc2f24e13042fc37b0b45ac661e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316099000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc56c85193c27255ecb90408767f9d68c274bc1196f45cb098d5ce6b90ea6678`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:254beacf3f323cf99977d539dcb720dc371b362af3a11b68a1c46f29aa86d29f`  
		Last Modified: Tue, 10 Jun 2025 22:48:19 GMT  
		Size: 25.5 MB (25544195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c2c4f56f4973aa426bbf799db8e68cde4b53a77cca960e30f5cce80bf2aa7f`  
		Last Modified: Wed, 11 Jun 2025 12:21:38 GMT  
		Size: 290.6 MB (290554805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f5ea5defe1c1fe621608dc360df4f5ff331dd46a68fe9aa37f478977462580bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7385c0ef64071bfa1afb032a6713f45d63b380778b4b3148bdc67bd681092a`

```dockerfile
```

-	Layers:
	-	`sha256:608e9b87f0307223cfdd260a571b0d674bd45db8f0fb974229c70dc33c749df4`  
		Last Modified: Wed, 11 Jun 2025 11:44:36 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4761277bd9d0f31fe1e8c4ddddf9957abd97fa921c5288901abe244d8de3cf7d`  
		Last Modified: Wed, 11 Jun 2025 11:44:37 GMT  
		Size: 11.4 KB (11431 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:72a16720d9ddf8a7b2dc8d1b1ace588379ca56d699f1d6ade8c501aff66ba039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258525579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3db1cfb8ec57c2e1c668c37e9498d466e905042d276a2b197a07d85338ee87a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a715c260ee097512a6f8b3db5041836c3694a52db693f5778bada15c1d44f171`  
		Last Modified: Wed, 11 Jun 2025 08:45:36 GMT  
		Size: 229.8 MB (229781394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:49f73dda4259a58747e62e4eb6c4fa65628e9f66ee44bdb93ad3e1d81fb41450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bc9a1161131b8fc7f7a7ab0d7bf7c121e0abf6d42e34c83f9ba766cce41fdd`

```dockerfile
```

-	Layers:
	-	`sha256:d80007aa3456840fd8abcf804d83d4b815f907a4e06448c7f1184528cf123af0`  
		Last Modified: Wed, 11 Jun 2025 08:44:42 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84c11e33c8cd2f4d6be8f5f448f2fb501785b8e526b31e414929455af60d8693`  
		Last Modified: Wed, 11 Jun 2025 08:44:43 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:03c578ce0b32d4737deeefaef6ecea7f0ac648ee25d4fee767f79d9c03ae99f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 MB (320511994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32eb66db9a96fa393a694a8787f4a4b6e70abcd17e925bef5790c75a30306789`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:1294ecac50b0f4fe7018ad5e666e6e3c43bd85fbdc4ff68322834fcc70904e3c`  
		Last Modified: Tue, 10 Jun 2025 23:26:42 GMT  
		Size: 31.2 MB (31189682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563e44106503f3d016cd7490b98df9b2aa3762a7e807aeb41e5f65752ff2986`  
		Last Modified: Wed, 11 Jun 2025 04:23:04 GMT  
		Size: 289.3 MB (289322312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f3928a493fc5a10fac96213e189c2986634e3b1873790ff662e908ecc4061a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d790ae2cf1ca80cca939a505b3e9cabef2ef7c0f112000bfef0e26a552016948`

```dockerfile
```

-	Layers:
	-	`sha256:2bb507ca83c8fe4625a244cd017cd4f83a5562e41548cdec226dac403b4e6795`  
		Last Modified: Wed, 11 Jun 2025 02:44:55 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7840377069666033ca9b65919363e35adad8b9fef3da1365876affb656c0d6`  
		Last Modified: Wed, 11 Jun 2025 02:44:56 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0`

```console
$ docker pull rust@sha256:b571d7b2dc7b9154517eeda87c0c3c97865d432e95ec205e34a194fd2baaff1d
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
$ docker pull rust@sha256:6d79f767859a5f025a062505fa9f2c1a041cadafcee71fbcbd226223be462f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553345588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a4a73321e80052e6fcd636dcd4ee26c8fa0ed0d655f95d92276efb7e759cc2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8862a18fa961ebfbac8484877dd4894e96ee88177d8c4f1f54d9727262b7d`  
		Last Modified: Wed, 11 Jun 2025 02:16:04 GMT  
		Size: 211.4 MB (211370316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d73d009ce498344941c85ff822a919ac7bb8976fd68dc8174f43a594bb3fa5`  
		Last Modified: Wed, 11 Jun 2025 03:21:03 GMT  
		Size: 205.1 MB (205065498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0` - unknown; unknown

```console
$ docker pull rust@sha256:503b69f42140f797db581680ee944348a715f85e374bf0f64688bb5e2d7f36ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15875572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9733726f707a166e40276a18d11a14103319579caa5d58f7e146f38d2b2cbe0d`

```dockerfile
```

-	Layers:
	-	`sha256:7fea0bce605acbffe3ad3faddcc83eebdef406125bb53e8a4ea980a11ae3fe32`  
		Last Modified: Wed, 11 Jun 2025 05:44:23 GMT  
		Size: 15.9 MB (15862434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8529bb6f4380c5ac83f220695448a518ba1d0d4b38c355cab9e014939ba116b`  
		Last Modified: Wed, 11 Jun 2025 05:44:24 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0` - linux; arm variant v7

```console
$ docker pull rust@sha256:72b485162489d2c8c49c305dd8b6ba86d4ff05ad986dfc71c07c9cf752fb23b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549362604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c922227a2a41f42eae2eebb9844a4b1e45540c0b00068b270c49c1a1e0b764`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22ee2db9f8d2ea3317ceb36f4b9bc7895f6cb8402903d639c8083eaec948450`  
		Last Modified: Tue, 03 Jun 2025 13:39:41 GMT  
		Size: 175.3 MB (175297793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92df434dc3b1ce2413f6828ef2e4c81ee8a8cef9cbe94a7d2215ad2bd340b292`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 248.3 MB (248281119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0` - unknown; unknown

```console
$ docker pull rust@sha256:2e7ce19770e0e30560aa4a23ada499e5a679b9dd1f61f479fe8d5abee6df0137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15386282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e40b43bdd8233f500a8bec0378ba7ac318dee0cafb4b7f582f11e2585a0396`

```dockerfile
```

-	Layers:
	-	`sha256:f8c270ee20e4767bc254f12fd15b19ddfb7c9f9a382a752ada7fd70bb37b3cc8`  
		Last Modified: Tue, 03 Jun 2025 15:36:17 GMT  
		Size: 15.4 MB (15373035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d32c5949c1f294d1c9fdbee6216a2148b76a885326b5d0372c69b726ab518b0`  
		Last Modified: Tue, 03 Jun 2025 15:36:16 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:40b030bf2085108f7fe5f75de0454fd4f6f855182477906360f40c0c29e95ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513085197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cecf015e8a7925026c922f69a93f75798f571a03fe30546ac7915e8760aaaa9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ee5cb7152015437e4a9b3066ae9e25a26a3bef6617d0b7f25368511c2d954`  
		Last Modified: Tue, 03 Jun 2025 13:30:35 GMT  
		Size: 202.8 MB (202762554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8a70e7346d3f568e98a68fc27e54274c16511edcd67498ae24761da6880cf6`  
		Last Modified: Tue, 03 Jun 2025 13:33:54 GMT  
		Size: 174.1 MB (174082075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0` - unknown; unknown

```console
$ docker pull rust@sha256:9719468f301df89ccc1071537f751d5e28f0c45df8834a133614066e3f97fd22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15612386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27147e11d32faab39878abb0d8cd3ca6bd4c56331b1722b30d8f48f9a45ece6e`

```dockerfile
```

-	Layers:
	-	`sha256:cc53a730eadb9784a7c191236378a7bcf219afa01f680521eb4bddf1d8ac993e`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 15.6 MB (15599095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e5657bfd53d43e028eb9d10e36db17bcc612d8fae30e5fe0fb076caa4b489b`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0` - linux; 386

```console
$ docker pull rust@sha256:8173985fad86853be81c2d2d427c1a22ad9d919982c5feb33ee56cc79a4b3c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579415232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e17162e2db334c9d6ff28fbd81344a20a803fde6a517c1c9410e6078a5a45d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731d58cf259468f5a31e00d6a586bde147720039c92e6c1ff4cb48a5dd996ae`  
		Last Modified: Wed, 11 Jun 2025 00:00:38 GMT  
		Size: 24.9 MB (24855706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce073e7b00b22009464483e266ff8ba48a8c0db86f16c877aa302337bbed6e9`  
		Last Modified: Wed, 11 Jun 2025 01:13:32 GMT  
		Size: 66.2 MB (66225240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75453a9e8c0ecda25b39aaabe16c9694b0bdb799dbc4bb61d1d0aee7d8b70850`  
		Last Modified: Wed, 11 Jun 2025 02:15:24 GMT  
		Size: 210.3 MB (210300359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a8e4b0736bc7a3d22fb842ad0ee81737c0ed14f5fe26606d2f4b5123616b6`  
		Last Modified: Wed, 11 Jun 2025 06:01:45 GMT  
		Size: 228.6 MB (228556453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0` - unknown; unknown

```console
$ docker pull rust@sha256:ab0c67f770b8da0cbe9479ecec374333e09badd00136782ce748b9cd17e281c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273c89500eb4e84dfb414ccb465c200b7f2a92f66f0b44e6f219b7dde68417b4`

```dockerfile
```

-	Layers:
	-	`sha256:dc04aee6f7f1d600381837690bbefc0648653c65ede9e2ecb6dc60dd7740d0c3`  
		Last Modified: Wed, 11 Jun 2025 05:45:01 GMT  
		Size: 15.8 MB (15839332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a2d3bfd52375162462af27b77692b39e0868ce869675ce142d35c98dcb3f11`  
		Last Modified: Wed, 11 Jun 2025 05:45:02 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0` - linux; ppc64le

```console
$ docker pull rust@sha256:294e06b00a43a648e43744691fbef73c1bdb451465ac350c76f736ed8a50b602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639200335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98218e5b1f057d84b638dd735f30b4a14abac5bb993b7561c9580a3babcd22dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Tue, 03 Jun 2025 13:36:57 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Tue, 03 Jun 2025 13:36:59 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5288618fea79e9a348995382235e6bee52819db4047a345ffaeaddd2b82e06`  
		Last Modified: Tue, 03 Jun 2025 13:37:01 GMT  
		Size: 214.4 MB (214416172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acddbc7af9fd8740373f8026a505be271623021d28c5aaf7cf9cfce5371e307`  
		Last Modified: Tue, 03 Jun 2025 15:36:39 GMT  
		Size: 277.0 MB (276955569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0` - unknown; unknown

```console
$ docker pull rust@sha256:60293968af0cc8afff5372a51d16244ad649290286e9457b6475a872eaf44c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15558952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90744ca96e8742bd842f46bb381ee8f2bd14a575fbfcf610a629445664ae33b`

```dockerfile
```

-	Layers:
	-	`sha256:e7bef55039062c7c4ae93c0994d2baa58cc23620f26310f07c85affb73ade0e6`  
		Last Modified: Tue, 03 Jun 2025 15:36:29 GMT  
		Size: 15.5 MB (15545745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ac5c316843cde59da34e1480f62e0a90b78ace51a57f9f67917ce2812741f6`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0` - linux; s390x

```console
$ docker pull rust@sha256:b9f17d320e48e042011cee37b615b2594ca1ac94588789d0978ac65e5e9671b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604371175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7ddbb7c8c246892af6179b2b4a9b8f8ceb4a0b60eff22c4736c5eaaf52b114`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Tue, 03 Jun 2025 13:37:08 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Tue, 03 Jun 2025 13:37:11 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3151505c70d8a7022bb518bbfce9c7488d1dd6ab624e1d96b883eb0654da7562`  
		Last Modified: Tue, 03 Jun 2025 13:37:22 GMT  
		Size: 183.4 MB (183405201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b0882d1ed7e92235dfca31dcc58a7de4c5cad3b764f0fe10874904586c5009`  
		Last Modified: Tue, 03 Jun 2025 14:16:08 GMT  
		Size: 286.3 MB (286308749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0` - unknown; unknown

```console
$ docker pull rust@sha256:751099b710c1a89fa55e82f9bc0fabfd70cb451e25cfbc7fc9449cc3fec7df28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15394148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd99f87c0d557b247c0e2c29a586dd93187c2ded1f463a78dd244eed473ac43a`

```dockerfile
```

-	Layers:
	-	`sha256:2d523435dd3012b7c822fc76bd1967e45ece2c7c3cda49a5a98a4c7c9fa13591`  
		Last Modified: Tue, 03 Jun 2025 15:36:32 GMT  
		Size: 15.4 MB (15381009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d39102b0130d44f2ec934dd1a55a3718747eb90d0591508f65d806ba52f578`  
		Last Modified: Tue, 03 Jun 2025 15:36:31 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0-alpine`

```console
$ docker pull rust@sha256:126df0f2a57e675f9306fe180b833982ffb996e90a92a793bb75253cfeed5475
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.87.0-alpine` - linux; amd64

```console
$ docker pull rust@sha256:2d5a7e008d9c1e86e54c0a3fffc00399eee945a13aa504fd5faf625e04110bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324451128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa6d9f8b73e08bfab3090a694fb52cea848dd5dfd249f9ff6352477596d5d38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aed27d59f9f3bafc26c73e1fa85e80d10a2b8b6221db885ef03875cbb2a92c3`  
		Last Modified: Tue, 03 Jun 2025 13:33:59 GMT  
		Size: 61.6 MB (61613723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a631e0f5786232f793b7aff2783c3a8252ee122748a6f63fb55c227e00e5002`  
		Last Modified: Tue, 03 Jun 2025 13:34:31 GMT  
		Size: 259.0 MB (259040559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:629b8efb80d6e9a1b711c46acd85e890c1c173b6b976ce39c598a8499163ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc3a74aa6b388d7315bb35c0e0fbd5fb39121d9296330833d8f9b79ffeb6a98`

```dockerfile
```

-	Layers:
	-	`sha256:03bc872db35194e79864e3a72cbb58ddd0548f438a45de2790469bf25a776a5e`  
		Last Modified: Wed, 04 Jun 2025 17:05:12 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c4e51ae8efcd54f48f7d1ced1a254f8c7ca2a7da2e3f6a81c2bedaed4895c9`  
		Last Modified: Wed, 04 Jun 2025 17:05:08 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fa3f412044d347294ad9c21eb3c9922a5e12e57b645ae53bbd27b8bc26173a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327194537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c83a1beaf9ddcfc60c8ec87a69dd7964f3e21bb48de7d530afe4816ca07fb61`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e525acaed56cf743f6ae8ee0c463c3fd7f0e9765bc0faaa7b0119fff2f2db4c4`  
		Last Modified: Tue, 03 Jun 2025 13:34:25 GMT  
		Size: 59.2 MB (59154215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1e992c2528e607b21a005bd23933eb8ae5f77fb262c96790f579f7f863d3c7`  
		Last Modified: Tue, 03 Jun 2025 13:34:30 GMT  
		Size: 263.9 MB (263904381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:0993ebd475453ccc6ded9cffa3118df8be36790fcfcf803fd1bf51bd147a22da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf7cab2f78729c23ec9792c67e373b2906e91cd19fe74c90616e885ff1ddd70`

```dockerfile
```

-	Layers:
	-	`sha256:59310aed03e6f7a9700cd2820322b4883fea2f9851c2e311a52617955a3abd14`  
		Last Modified: Wed, 04 Jun 2025 17:05:46 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e888f3541888d0dcd1e7f14fca30a9930a25f4836300284c59226514fe4b48`  
		Last Modified: Wed, 04 Jun 2025 17:05:45 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718715b3cbe3b4fd9094909206504e5958585bd739a34dc4fb5b7f6ed2131b8`  
		Last Modified: Fri, 16 May 2025 14:17:43 GMT  
		Size: 55.3 MB (55315586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeb4a9d8a98d7b7dadf2be0b1943267d81b081cb2fb12a85484c6aaadf235fb`  
		Last Modified: Fri, 16 May 2025 14:17:57 GMT  
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
		Last Modified: Thu, 15 May 2025 20:44:31 GMT  
		Size: 711.8 KB (711789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a9394ddea85fc3e016d5927f8ce6a38638e7c7eeea1996460a0e68f6915e5c6`  
		Last Modified: Thu, 15 May 2025 20:44:31 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c6aa5430354637d99185e3c6f997bb89b34d0340d714c59489470f3b28fb00`  
		Last Modified: Thu, 08 May 2025 23:40:24 GMT  
		Size: 53.0 MB (52950277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d7b743d7f5864c65b2894547a9334b33385928622ae90e6a32c6e8856c668`  
		Last Modified: Fri, 16 May 2025 14:28:10 GMT  
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
		Last Modified: Mon, 09 Jun 2025 05:43:46 GMT  
		Size: 747.7 KB (747721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5df0c715639e649fb2f087e25e05ab1d51803c9e80193b7ded83d66aa0f06e`  
		Last Modified: Mon, 09 Jun 2025 05:43:46 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b343ca42d769a088aad30a06435916be946b7bd77c275c4c48aa9c02d07ebc6`  
		Last Modified: Thu, 15 May 2025 20:45:48 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0312ddedcb8a05877b03a2214ddd4942d87d6bd8684a5f5bc0353f72d76def`  
		Last Modified: Thu, 15 May 2025 20:46:29 GMT  
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
		Last Modified: Thu, 15 May 2025 20:44:27 GMT  
		Size: 783.8 KB (783823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05e06b11fae76f35a913f94980f7b264abfa081dffa29929dd773c6969a089d`  
		Last Modified: Thu, 15 May 2025 20:44:27 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a8d04fc53dbb480e66cf7321229cda858c75a9bfa488474aabc6a3fbc3423`  
		Last Modified: Thu, 08 May 2025 17:05:51 GMT  
		Size: 59.1 MB (59101363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd10981d51d5c4342a74b76870500712f6977bafb0891f69b5b725cd3f83575b`  
		Last Modified: Fri, 16 May 2025 13:16:00 GMT  
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
		Last Modified: Fri, 16 May 2025 14:02:45 GMT  
		Size: 863.4 KB (863409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4799a729390389da9955e76bdba397218c8fff4138d88735449c1364a6120788`  
		Last Modified: Fri, 16 May 2025 14:02:46 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0-alpine3.22`

```console
$ docker pull rust@sha256:126df0f2a57e675f9306fe180b833982ffb996e90a92a793bb75253cfeed5475
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.87.0-alpine3.22` - linux; amd64

```console
$ docker pull rust@sha256:2d5a7e008d9c1e86e54c0a3fffc00399eee945a13aa504fd5faf625e04110bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324451128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa6d9f8b73e08bfab3090a694fb52cea848dd5dfd249f9ff6352477596d5d38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aed27d59f9f3bafc26c73e1fa85e80d10a2b8b6221db885ef03875cbb2a92c3`  
		Last Modified: Tue, 03 Jun 2025 13:33:59 GMT  
		Size: 61.6 MB (61613723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a631e0f5786232f793b7aff2783c3a8252ee122748a6f63fb55c227e00e5002`  
		Last Modified: Tue, 03 Jun 2025 13:34:31 GMT  
		Size: 259.0 MB (259040559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:629b8efb80d6e9a1b711c46acd85e890c1c173b6b976ce39c598a8499163ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc3a74aa6b388d7315bb35c0e0fbd5fb39121d9296330833d8f9b79ffeb6a98`

```dockerfile
```

-	Layers:
	-	`sha256:03bc872db35194e79864e3a72cbb58ddd0548f438a45de2790469bf25a776a5e`  
		Last Modified: Wed, 04 Jun 2025 17:05:12 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c4e51ae8efcd54f48f7d1ced1a254f8c7ca2a7da2e3f6a81c2bedaed4895c9`  
		Last Modified: Wed, 04 Jun 2025 17:05:08 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fa3f412044d347294ad9c21eb3c9922a5e12e57b645ae53bbd27b8bc26173a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327194537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c83a1beaf9ddcfc60c8ec87a69dd7964f3e21bb48de7d530afe4816ca07fb61`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e525acaed56cf743f6ae8ee0c463c3fd7f0e9765bc0faaa7b0119fff2f2db4c4`  
		Last Modified: Tue, 03 Jun 2025 13:34:25 GMT  
		Size: 59.2 MB (59154215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1e992c2528e607b21a005bd23933eb8ae5f77fb262c96790f579f7f863d3c7`  
		Last Modified: Tue, 03 Jun 2025 13:34:30 GMT  
		Size: 263.9 MB (263904381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:0993ebd475453ccc6ded9cffa3118df8be36790fcfcf803fd1bf51bd147a22da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf7cab2f78729c23ec9792c67e373b2906e91cd19fe74c90616e885ff1ddd70`

```dockerfile
```

-	Layers:
	-	`sha256:59310aed03e6f7a9700cd2820322b4883fea2f9851c2e311a52617955a3abd14`  
		Last Modified: Wed, 04 Jun 2025 17:05:46 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e888f3541888d0dcd1e7f14fca30a9930a25f4836300284c59226514fe4b48`  
		Last Modified: Wed, 04 Jun 2025 17:05:45 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0-bookworm`

```console
$ docker pull rust@sha256:b571d7b2dc7b9154517eeda87c0c3c97865d432e95ec205e34a194fd2baaff1d
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
$ docker pull rust@sha256:6d79f767859a5f025a062505fa9f2c1a041cadafcee71fbcbd226223be462f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553345588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a4a73321e80052e6fcd636dcd4ee26c8fa0ed0d655f95d92276efb7e759cc2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8862a18fa961ebfbac8484877dd4894e96ee88177d8c4f1f54d9727262b7d`  
		Last Modified: Wed, 11 Jun 2025 02:16:04 GMT  
		Size: 211.4 MB (211370316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d73d009ce498344941c85ff822a919ac7bb8976fd68dc8174f43a594bb3fa5`  
		Last Modified: Wed, 11 Jun 2025 03:21:03 GMT  
		Size: 205.1 MB (205065498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:503b69f42140f797db581680ee944348a715f85e374bf0f64688bb5e2d7f36ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15875572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9733726f707a166e40276a18d11a14103319579caa5d58f7e146f38d2b2cbe0d`

```dockerfile
```

-	Layers:
	-	`sha256:7fea0bce605acbffe3ad3faddcc83eebdef406125bb53e8a4ea980a11ae3fe32`  
		Last Modified: Wed, 11 Jun 2025 05:44:23 GMT  
		Size: 15.9 MB (15862434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8529bb6f4380c5ac83f220695448a518ba1d0d4b38c355cab9e014939ba116b`  
		Last Modified: Wed, 11 Jun 2025 05:44:24 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:72b485162489d2c8c49c305dd8b6ba86d4ff05ad986dfc71c07c9cf752fb23b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549362604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c922227a2a41f42eae2eebb9844a4b1e45540c0b00068b270c49c1a1e0b764`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22ee2db9f8d2ea3317ceb36f4b9bc7895f6cb8402903d639c8083eaec948450`  
		Last Modified: Tue, 03 Jun 2025 13:39:41 GMT  
		Size: 175.3 MB (175297793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92df434dc3b1ce2413f6828ef2e4c81ee8a8cef9cbe94a7d2215ad2bd340b292`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 248.3 MB (248281119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2e7ce19770e0e30560aa4a23ada499e5a679b9dd1f61f479fe8d5abee6df0137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15386282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e40b43bdd8233f500a8bec0378ba7ac318dee0cafb4b7f582f11e2585a0396`

```dockerfile
```

-	Layers:
	-	`sha256:f8c270ee20e4767bc254f12fd15b19ddfb7c9f9a382a752ada7fd70bb37b3cc8`  
		Last Modified: Tue, 03 Jun 2025 15:36:17 GMT  
		Size: 15.4 MB (15373035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d32c5949c1f294d1c9fdbee6216a2148b76a885326b5d0372c69b726ab518b0`  
		Last Modified: Tue, 03 Jun 2025 15:36:16 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:40b030bf2085108f7fe5f75de0454fd4f6f855182477906360f40c0c29e95ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513085197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cecf015e8a7925026c922f69a93f75798f571a03fe30546ac7915e8760aaaa9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ee5cb7152015437e4a9b3066ae9e25a26a3bef6617d0b7f25368511c2d954`  
		Last Modified: Tue, 03 Jun 2025 13:30:35 GMT  
		Size: 202.8 MB (202762554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8a70e7346d3f568e98a68fc27e54274c16511edcd67498ae24761da6880cf6`  
		Last Modified: Tue, 03 Jun 2025 13:33:54 GMT  
		Size: 174.1 MB (174082075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9719468f301df89ccc1071537f751d5e28f0c45df8834a133614066e3f97fd22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15612386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27147e11d32faab39878abb0d8cd3ca6bd4c56331b1722b30d8f48f9a45ece6e`

```dockerfile
```

-	Layers:
	-	`sha256:cc53a730eadb9784a7c191236378a7bcf219afa01f680521eb4bddf1d8ac993e`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 15.6 MB (15599095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e5657bfd53d43e028eb9d10e36db17bcc612d8fae30e5fe0fb076caa4b489b`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bookworm` - linux; 386

```console
$ docker pull rust@sha256:8173985fad86853be81c2d2d427c1a22ad9d919982c5feb33ee56cc79a4b3c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579415232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e17162e2db334c9d6ff28fbd81344a20a803fde6a517c1c9410e6078a5a45d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731d58cf259468f5a31e00d6a586bde147720039c92e6c1ff4cb48a5dd996ae`  
		Last Modified: Wed, 11 Jun 2025 00:00:38 GMT  
		Size: 24.9 MB (24855706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce073e7b00b22009464483e266ff8ba48a8c0db86f16c877aa302337bbed6e9`  
		Last Modified: Wed, 11 Jun 2025 01:13:32 GMT  
		Size: 66.2 MB (66225240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75453a9e8c0ecda25b39aaabe16c9694b0bdb799dbc4bb61d1d0aee7d8b70850`  
		Last Modified: Wed, 11 Jun 2025 02:15:24 GMT  
		Size: 210.3 MB (210300359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a8e4b0736bc7a3d22fb842ad0ee81737c0ed14f5fe26606d2f4b5123616b6`  
		Last Modified: Wed, 11 Jun 2025 06:01:45 GMT  
		Size: 228.6 MB (228556453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ab0c67f770b8da0cbe9479ecec374333e09badd00136782ce748b9cd17e281c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273c89500eb4e84dfb414ccb465c200b7f2a92f66f0b44e6f219b7dde68417b4`

```dockerfile
```

-	Layers:
	-	`sha256:dc04aee6f7f1d600381837690bbefc0648653c65ede9e2ecb6dc60dd7740d0c3`  
		Last Modified: Wed, 11 Jun 2025 05:45:01 GMT  
		Size: 15.8 MB (15839332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a2d3bfd52375162462af27b77692b39e0868ce869675ce142d35c98dcb3f11`  
		Last Modified: Wed, 11 Jun 2025 05:45:02 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:294e06b00a43a648e43744691fbef73c1bdb451465ac350c76f736ed8a50b602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639200335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98218e5b1f057d84b638dd735f30b4a14abac5bb993b7561c9580a3babcd22dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Tue, 03 Jun 2025 13:36:57 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Tue, 03 Jun 2025 13:36:59 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5288618fea79e9a348995382235e6bee52819db4047a345ffaeaddd2b82e06`  
		Last Modified: Tue, 03 Jun 2025 13:37:01 GMT  
		Size: 214.4 MB (214416172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acddbc7af9fd8740373f8026a505be271623021d28c5aaf7cf9cfce5371e307`  
		Last Modified: Tue, 03 Jun 2025 15:36:39 GMT  
		Size: 277.0 MB (276955569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:60293968af0cc8afff5372a51d16244ad649290286e9457b6475a872eaf44c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15558952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90744ca96e8742bd842f46bb381ee8f2bd14a575fbfcf610a629445664ae33b`

```dockerfile
```

-	Layers:
	-	`sha256:e7bef55039062c7c4ae93c0994d2baa58cc23620f26310f07c85affb73ade0e6`  
		Last Modified: Tue, 03 Jun 2025 15:36:29 GMT  
		Size: 15.5 MB (15545745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ac5c316843cde59da34e1480f62e0a90b78ace51a57f9f67917ce2812741f6`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b9f17d320e48e042011cee37b615b2594ca1ac94588789d0978ac65e5e9671b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604371175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7ddbb7c8c246892af6179b2b4a9b8f8ceb4a0b60eff22c4736c5eaaf52b114`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Tue, 03 Jun 2025 13:37:08 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Tue, 03 Jun 2025 13:37:11 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3151505c70d8a7022bb518bbfce9c7488d1dd6ab624e1d96b883eb0654da7562`  
		Last Modified: Tue, 03 Jun 2025 13:37:22 GMT  
		Size: 183.4 MB (183405201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b0882d1ed7e92235dfca31dcc58a7de4c5cad3b764f0fe10874904586c5009`  
		Last Modified: Tue, 03 Jun 2025 14:16:08 GMT  
		Size: 286.3 MB (286308749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:751099b710c1a89fa55e82f9bc0fabfd70cb451e25cfbc7fc9449cc3fec7df28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15394148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd99f87c0d557b247c0e2c29a586dd93187c2ded1f463a78dd244eed473ac43a`

```dockerfile
```

-	Layers:
	-	`sha256:2d523435dd3012b7c822fc76bd1967e45ece2c7c3cda49a5a98a4c7c9fa13591`  
		Last Modified: Tue, 03 Jun 2025 15:36:32 GMT  
		Size: 15.4 MB (15381009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d39102b0130d44f2ec934dd1a55a3718747eb90d0591508f65d806ba52f578`  
		Last Modified: Tue, 03 Jun 2025 15:36:31 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0-bullseye`

```console
$ docker pull rust@sha256:acd48e9a3f1a6cbfe9de41c88984b9dffa24c4e3e1f881d00c1b99145a0731e2
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
$ docker pull rust@sha256:867389037b7b993d5901a4dc22f719439d56df6322ae8ee5b3d659164ad8a90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526485218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34027bad41e7c5a2dfde8329ad0cdc735ca4cf8afc2bda755755a229a103d19d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2678613884c2f141cc551880b1a1587f0c890606a900bbac5a1ace2645be657`  
		Last Modified: Wed, 11 Jun 2025 00:02:35 GMT  
		Size: 54.8 MB (54757363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c6624995870ade650aaf0f5b37565d2e41e2500e8105fd69b79900eef086cf`  
		Last Modified: Wed, 11 Jun 2025 02:16:19 GMT  
		Size: 197.1 MB (197142069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40689c5eb1b4170233c72a76fb229e2b672f3ecbe0dfaba41511809c1f0054be`  
		Last Modified: Wed, 11 Jun 2025 03:20:02 GMT  
		Size: 205.1 MB (205065865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6939a7548b0bfc37a63c429bda574a8467fe2f00ec42b56a2d48f8407fa16a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15475148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6174e312182a700930c62add7e8dbe79bc0b6c7a153f83b5b3a5b150e2bedd3f`

```dockerfile
```

-	Layers:
	-	`sha256:82873fb0fa119fd347188508fb45ca824a73b0d6afc0611c941197f4af538f52`  
		Last Modified: Wed, 11 Jun 2025 05:44:34 GMT  
		Size: 15.5 MB (15463899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:782b06ea0a8cdf38dbf3b8fb9b63fa091b5c73b1d89bbfbd4c7a88c3356f08c8`  
		Last Modified: Wed, 11 Jun 2025 05:44:35 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:f0099d1100af3de76397f6b72386fb82e5bfe767c199e3af9dacabcb847cd818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.4 MB (530413542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a851fda81799e9f774be69c775a4b41a18a92ffb711d53f4a2fb7adbae061b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
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
	-	`sha256:2bf062f1f44f96722293994387f4b88016e2f0a9f49c7f09b2ceffefc7717199`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 49.0 MB (49041988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933c7aef3dae867caad0cbafef5672fb39317c04b3bf8bff0868bf265098c4de`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 14.9 MB (14880519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0144e65734487c61a592b9ecd7d576c77bc270bd5d65049de36718f77416c6`  
		Last Modified: Tue, 03 Jun 2025 14:32:58 GMT  
		Size: 50.6 MB (50631322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c9ac1f243c709a0fa1779761ca68b4f1c6b9419089c5cd54dcb97bb3d22f54`  
		Last Modified: Tue, 03 Jun 2025 14:33:03 GMT  
		Size: 167.6 MB (167578499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae8b0608788d75c99991c8f9c893341f4d11f3bc4aab4994d6807ed4b8d8163`  
		Last Modified: Thu, 05 Jun 2025 16:53:56 GMT  
		Size: 248.3 MB (248281214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:2cde4e1249e67514f7134d4cbb09b7ee38dd9714da18dcad9d4f654e29137c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14985623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a5ac1d1f5eb5b234db53835a6e11e4c5bf285fcac3a9d866d14a491a75c58d`

```dockerfile
```

-	Layers:
	-	`sha256:482f3adc2f97de782cc024fa5f52aa7dc9524f1440c109d95f33f0532d4878ff`  
		Last Modified: Wed, 11 Jun 2025 05:44:45 GMT  
		Size: 15.0 MB (14974298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ee59cf0e8a7913c311c3a1e425258ded463181f50bd06e068c6172b8725b4d`  
		Last Modified: Wed, 11 Jun 2025 05:44:46 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d9a2d79db5bd7b83232ed720e7460b712a4b3e4928d685f2235c2bf3ba8d5d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486978031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43e429bad1c4ae05ed881da09a277098e088e0e2baa6160638701e0d8dbc76a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a602f78cf8d696db9521d18affb7ecdb79ff690533efae26e3bdb1544cb1752`  
		Last Modified: Tue, 03 Jun 2025 13:31:09 GMT  
		Size: 15.8 MB (15750382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1b27af19f7550ac0d9c38bf6bcf26ba7eb53984e7e5e0886342816133c76e`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 54.9 MB (54853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d0d4413e7427c3ec24a23fc978dced4b2de0294ec9d2e02645e0f62aa2de32`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 190.0 MB (190044698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79cea524fba17622c1c30c1189d43e20ecef3a912b0c98eade8501625fc699b`  
		Last Modified: Tue, 03 Jun 2025 14:20:24 GMT  
		Size: 174.1 MB (174081960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f2c10e422b56bc7311c6e7a10646a49504aad296319e2495888010bf46be7246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe291b6ae25a37ca79695b56eb405b23c994dde1a5c2bb6a0870abd60f6af0d7`

```dockerfile
```

-	Layers:
	-	`sha256:6f81d3f70ab207ec9aadb6eb3a55fe12e8d125470cc73aa35be912d8c206ad93`  
		Last Modified: Wed, 11 Jun 2025 05:44:56 GMT  
		Size: 15.2 MB (15176927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5df7740191a1cba2214b1d3bc8489b68a7b671d82f48fac368d2c938dd1a0a58`  
		Last Modified: Wed, 11 Jun 2025 05:44:57 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-bullseye` - linux; 386

```console
$ docker pull rust@sha256:7a323c00d871336669f30ee2a4e6310bf99cea3b3d99279391cef0f3b69e84a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555605760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dabbac26160a93389a46a4bb2dd7d91f7d94dae182f0866446402a405b47539`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
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
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e7c1ed34c380b4c9e9f08e94b0f7b9bf90a0e8c42de246cb4b2159e2126fef`  
		Last Modified: Wed, 11 Jun 2025 00:00:47 GMT  
		Size: 16.3 MB (16268617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3a34392e433938214bbf2cba34365a474d819c470686803059c6d8390cf680`  
		Last Modified: Wed, 11 Jun 2025 01:13:31 GMT  
		Size: 56.0 MB (56049939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fc14c21031cb8eae2e7bca81acab0fca46817b5d8a4fa7fbfb97ff76557da5`  
		Last Modified: Wed, 11 Jun 2025 02:14:17 GMT  
		Size: 200.0 MB (200041378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f45e8e404b579a46068dee78945e0a0853c35cfb3c8a243538f86ff1821f17b`  
		Last Modified: Wed, 11 Jun 2025 09:54:26 GMT  
		Size: 228.6 MB (228555814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:63ea2ff898633a248c8bed35c0c0507387f1f57579f214745875538a0a8db1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f08987abd3e9f97128af9ebb7b448c5fb3e5ea5ab678209c26dcd46460e41e`

```dockerfile
```

-	Layers:
	-	`sha256:49ffb54271663c1d37909753b4895c96d08d07308be90ee479ef685461712fba`  
		Last Modified: Wed, 11 Jun 2025 05:45:08 GMT  
		Size: 15.5 MB (15450601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:191e5f9bf2a3f582caff72f6b5628f333cb7c8de24c23c3ea181aad5630b3378`  
		Last Modified: Wed, 11 Jun 2025 05:45:09 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0-slim`

```console
$ docker pull rust@sha256:437507c3e719e4f968033b88d851ffa9f5aceeb2dcc2482cc6cb7647811a55eb
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
$ docker pull rust@sha256:c6d2b4f8115be78af2a07072f61cffbbb4d6c93b55a4712b922fb7391db6a2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3a4353cc539aea8fad45dd0dc90225aa41fc00a850fec6c15024aa793caa8f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb49401afa0e17bb5553a2c29d1dfcf82e44a6f845092a3e727d07c58cae51e`  
		Last Modified: Wed, 11 Jun 2025 02:46:35 GMT  
		Size: 275.8 MB (275821770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b992a82898a09273268714a1bee7910884463b9c54cff38b0a9aaed379224967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0efaf5c9b3bde5d5403cd7bfe7cd6cffebb0c548fad83f1c45b60d09237485d`

```dockerfile
```

-	Layers:
	-	`sha256:1444619cb92821045d11ffb02735da01990b56835388b8489569925a16c9a85b`  
		Last Modified: Wed, 11 Jun 2025 02:44:27 GMT  
		Size: 4.1 MB (4093196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860531365ea841bb950e17b4e50e3de256a47221cfdf954a40ea40c86c3dee21`  
		Last Modified: Wed, 11 Jun 2025 02:44:28 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:966e7302a5f24503c2fb6de767fae05595b40e37222459764a0a385ec37af077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320043588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b958cc8bdf7ee0e305edf9ce0e0863ceab33ff294219118e308d1cb2cae0aa9c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10dd721eeaf60b511757cc253292582f2dbe051a02adf667aa8ac4ba94997f0`  
		Last Modified: Wed, 11 Jun 2025 12:01:23 GMT  
		Size: 296.1 MB (296104844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:961687e45e0a213ac59675555b8ef714187ab0f3940ca58601da576f49066253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cc0add7a9f0b20fbb1b6d07518f411b4aeaa40dda619c70a752aedda655f1e`

```dockerfile
```

-	Layers:
	-	`sha256:4a53c52228ba7e41746447e406b7d8ce69b8ad263bd576e3ddb52841ae765dab`  
		Last Modified: Wed, 11 Jun 2025 11:44:27 GMT  
		Size: 3.9 MB (3907625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d0c6505620255b5d1bd1af5fa4ed9ed1f6a644865f9168f949f8fad11a10d0`  
		Last Modified: Wed, 11 Jun 2025 11:44:28 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0e216c245a1044e77982d24fd09991448bcd12648115cd6bf2ce1c3d63633a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268005202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834da5b79b78574e38bf973a76161d294a637d950101652138b9dbb92595d5ae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3835d9003112b328f6866eb687138cc59ca3dea0da56c9da555f235723c3a464`  
		Last Modified: Wed, 11 Jun 2025 08:47:07 GMT  
		Size: 239.9 MB (239927527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:2bcd57c614490ddc32c882435e924dcf857670d889481a167b10104b8f71d03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44c4ec5937533284046291218fb2b0376ff4649f1d44f388921b997949dc39f`

```dockerfile
```

-	Layers:
	-	`sha256:a7c21ba2560f3f989e8e7892ec85f8ed9b4fb76fabd4e88ec1e92f54a6de3fb9`  
		Last Modified: Wed, 11 Jun 2025 08:44:36 GMT  
		Size: 4.1 MB (4115540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168233367a2fd0fd2e5e9d69c0e40d5ef353bc704f5cebd9ec8a8b20a7a53703`  
		Last Modified: Wed, 11 Jun 2025 08:44:37 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim` - linux; 386

```console
$ docker pull rust@sha256:2ad11b3f0daccba195c8a3e2d537873b28c0a4d9739f06cc67c58451bf7a42b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325379390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b7914ccdd8d8409e9d85ee45f9969a13ef81e3e7ca5cd62b402205104f6d62`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7541639b044ca0ee0b02dbb730ab58d7da071f667f2a37ab0173489a979a307`  
		Last Modified: Wed, 11 Jun 2025 03:02:06 GMT  
		Size: 296.2 MB (296166957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:96ac86d3fdb37019662687ae8d46c3b145d264dcac844eb7d01cb9fb312769af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b424745a3a740149528fb53d8e6c563c3eeb9457ce88ec0538e221a0ffedf4f4`

```dockerfile
```

-	Layers:
	-	`sha256:6805d028c613af8d87b3ba1f5f56ae1c8e543065cde206869d7031d4b89fee3a`  
		Last Modified: Wed, 11 Jun 2025 02:44:44 GMT  
		Size: 4.1 MB (4072559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc4f4c22e4ea63b843fa608be1c31913653a04d371f1d372f63ab39cdf0fec2`  
		Last Modified: Wed, 11 Jun 2025 02:44:45 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:333d0518b417fd65a06c5a0ee4217fe07e9345093922191979f25a8901395ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377793386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43dd89cf4392e35cda901f980625fedd6b33b8ca171df7416f97273cee5f5fe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641961947f2e89b9782726648e622e267f8a2e965318c701be9c3141d43f9f5`  
		Last Modified: Wed, 11 Jun 2025 09:01:40 GMT  
		Size: 345.7 MB (345720591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:eb1a17643ff56aa1c2370c7f17f04522bf68c405f72150edd08aac2bf0398359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4078847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadaab8a496b8047c9ae84aa96b01e8a4a8c05f00eb3dfe6a62795d3119938d7`

```dockerfile
```

-	Layers:
	-	`sha256:50bbf10950c98ad566b72902fa2c8a087e58b6c3b3b265711bcaa1330922dbb3`  
		Last Modified: Wed, 11 Jun 2025 08:44:44 GMT  
		Size: 4.1 MB (4065509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60fecd5b455a4ae648136c59e20d9e13d41c7aef26ed54572d1a86744ccf3ef0`  
		Last Modified: Wed, 11 Jun 2025 08:44:45 GMT  
		Size: 13.3 KB (13338 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim` - linux; s390x

```console
$ docker pull rust@sha256:5faea305cb32004ab4694cf9be72db317b86544c70cef24a43c9863e756ea6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363336119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f475f06d4297efbaf55ad8aae30d81a630a62cdd9286374386ae9d5facc0082e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f552a08d6186725df4030ad88bf2b444cc4868a9bfb86570d7cf36dd450471ee`  
		Last Modified: Wed, 11 Jun 2025 09:02:21 GMT  
		Size: 336.4 MB (336448266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:af734c9315ffbb0607238ba1205d3a3ba0250e7a63158b73cdc27e135f406e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc43a07563773310da6d9a09b86d0264d7db9b6542b5c600d604a26301fad5d`

```dockerfile
```

-	Layers:
	-	`sha256:76749c6d7cca227b6b9fa93d011effbc232138d91f89ff0944eb8c07b9179bf0`  
		Last Modified: Wed, 11 Jun 2025 08:44:50 GMT  
		Size: 3.9 MB (3930874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d70369bbe1eee7920586d7a5d9d0ce8a7f8a4c869fb9f9c0fa15589bd6cfb5c`  
		Last Modified: Wed, 11 Jun 2025 08:44:51 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0-slim-bookworm`

```console
$ docker pull rust@sha256:437507c3e719e4f968033b88d851ffa9f5aceeb2dcc2482cc6cb7647811a55eb
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
$ docker pull rust@sha256:c6d2b4f8115be78af2a07072f61cffbbb4d6c93b55a4712b922fb7391db6a2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3a4353cc539aea8fad45dd0dc90225aa41fc00a850fec6c15024aa793caa8f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb49401afa0e17bb5553a2c29d1dfcf82e44a6f845092a3e727d07c58cae51e`  
		Last Modified: Wed, 11 Jun 2025 02:46:35 GMT  
		Size: 275.8 MB (275821770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b992a82898a09273268714a1bee7910884463b9c54cff38b0a9aaed379224967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0efaf5c9b3bde5d5403cd7bfe7cd6cffebb0c548fad83f1c45b60d09237485d`

```dockerfile
```

-	Layers:
	-	`sha256:1444619cb92821045d11ffb02735da01990b56835388b8489569925a16c9a85b`  
		Last Modified: Wed, 11 Jun 2025 02:44:27 GMT  
		Size: 4.1 MB (4093196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860531365ea841bb950e17b4e50e3de256a47221cfdf954a40ea40c86c3dee21`  
		Last Modified: Wed, 11 Jun 2025 02:44:28 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:966e7302a5f24503c2fb6de767fae05595b40e37222459764a0a385ec37af077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320043588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b958cc8bdf7ee0e305edf9ce0e0863ceab33ff294219118e308d1cb2cae0aa9c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10dd721eeaf60b511757cc253292582f2dbe051a02adf667aa8ac4ba94997f0`  
		Last Modified: Wed, 11 Jun 2025 12:01:23 GMT  
		Size: 296.1 MB (296104844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:961687e45e0a213ac59675555b8ef714187ab0f3940ca58601da576f49066253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cc0add7a9f0b20fbb1b6d07518f411b4aeaa40dda619c70a752aedda655f1e`

```dockerfile
```

-	Layers:
	-	`sha256:4a53c52228ba7e41746447e406b7d8ce69b8ad263bd576e3ddb52841ae765dab`  
		Last Modified: Wed, 11 Jun 2025 11:44:27 GMT  
		Size: 3.9 MB (3907625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d0c6505620255b5d1bd1af5fa4ed9ed1f6a644865f9168f949f8fad11a10d0`  
		Last Modified: Wed, 11 Jun 2025 11:44:28 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0e216c245a1044e77982d24fd09991448bcd12648115cd6bf2ce1c3d63633a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268005202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834da5b79b78574e38bf973a76161d294a637d950101652138b9dbb92595d5ae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3835d9003112b328f6866eb687138cc59ca3dea0da56c9da555f235723c3a464`  
		Last Modified: Wed, 11 Jun 2025 08:47:07 GMT  
		Size: 239.9 MB (239927527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2bcd57c614490ddc32c882435e924dcf857670d889481a167b10104b8f71d03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44c4ec5937533284046291218fb2b0376ff4649f1d44f388921b997949dc39f`

```dockerfile
```

-	Layers:
	-	`sha256:a7c21ba2560f3f989e8e7892ec85f8ed9b4fb76fabd4e88ec1e92f54a6de3fb9`  
		Last Modified: Wed, 11 Jun 2025 08:44:36 GMT  
		Size: 4.1 MB (4115540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168233367a2fd0fd2e5e9d69c0e40d5ef353bc704f5cebd9ec8a8b20a7a53703`  
		Last Modified: Wed, 11 Jun 2025 08:44:37 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:2ad11b3f0daccba195c8a3e2d537873b28c0a4d9739f06cc67c58451bf7a42b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325379390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b7914ccdd8d8409e9d85ee45f9969a13ef81e3e7ca5cd62b402205104f6d62`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7541639b044ca0ee0b02dbb730ab58d7da071f667f2a37ab0173489a979a307`  
		Last Modified: Wed, 11 Jun 2025 03:02:06 GMT  
		Size: 296.2 MB (296166957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:96ac86d3fdb37019662687ae8d46c3b145d264dcac844eb7d01cb9fb312769af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b424745a3a740149528fb53d8e6c563c3eeb9457ce88ec0538e221a0ffedf4f4`

```dockerfile
```

-	Layers:
	-	`sha256:6805d028c613af8d87b3ba1f5f56ae1c8e543065cde206869d7031d4b89fee3a`  
		Last Modified: Wed, 11 Jun 2025 02:44:44 GMT  
		Size: 4.1 MB (4072559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc4f4c22e4ea63b843fa608be1c31913653a04d371f1d372f63ab39cdf0fec2`  
		Last Modified: Wed, 11 Jun 2025 02:44:45 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:333d0518b417fd65a06c5a0ee4217fe07e9345093922191979f25a8901395ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377793386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43dd89cf4392e35cda901f980625fedd6b33b8ca171df7416f97273cee5f5fe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641961947f2e89b9782726648e622e267f8a2e965318c701be9c3141d43f9f5`  
		Last Modified: Wed, 11 Jun 2025 09:01:40 GMT  
		Size: 345.7 MB (345720591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:eb1a17643ff56aa1c2370c7f17f04522bf68c405f72150edd08aac2bf0398359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4078847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadaab8a496b8047c9ae84aa96b01e8a4a8c05f00eb3dfe6a62795d3119938d7`

```dockerfile
```

-	Layers:
	-	`sha256:50bbf10950c98ad566b72902fa2c8a087e58b6c3b3b265711bcaa1330922dbb3`  
		Last Modified: Wed, 11 Jun 2025 08:44:44 GMT  
		Size: 4.1 MB (4065509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60fecd5b455a4ae648136c59e20d9e13d41c7aef26ed54572d1a86744ccf3ef0`  
		Last Modified: Wed, 11 Jun 2025 08:44:45 GMT  
		Size: 13.3 KB (13338 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:5faea305cb32004ab4694cf9be72db317b86544c70cef24a43c9863e756ea6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363336119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f475f06d4297efbaf55ad8aae30d81a630a62cdd9286374386ae9d5facc0082e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f552a08d6186725df4030ad88bf2b444cc4868a9bfb86570d7cf36dd450471ee`  
		Last Modified: Wed, 11 Jun 2025 09:02:21 GMT  
		Size: 336.4 MB (336448266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:af734c9315ffbb0607238ba1205d3a3ba0250e7a63158b73cdc27e135f406e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc43a07563773310da6d9a09b86d0264d7db9b6542b5c600d604a26301fad5d`

```dockerfile
```

-	Layers:
	-	`sha256:76749c6d7cca227b6b9fa93d011effbc232138d91f89ff0944eb8c07b9179bf0`  
		Last Modified: Wed, 11 Jun 2025 08:44:50 GMT  
		Size: 3.9 MB (3930874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d70369bbe1eee7920586d7a5d9d0ce8a7f8a4c869fb9f9c0fa15589bd6cfb5c`  
		Last Modified: Wed, 11 Jun 2025 08:44:51 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.87.0-slim-bullseye`

```console
$ docker pull rust@sha256:c8bfa46d68a20e878e316e8302790d5f8c7410c56e35b562507d50f2bec64dd7
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
$ docker pull rust@sha256:39269e5da7fa88d82b633d74443d591bb0b7ec42c04e303356f7263217cf3e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295462508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b70ff91aa20633a2a939769ff5ae727e5dbad08a87aaa6968d3e778b11dad`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986242588b209fdbc06bae0292eda94e58818e8a997967091183318a0308eb6`  
		Last Modified: Wed, 11 Jun 2025 02:56:02 GMT  
		Size: 265.2 MB (265206444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f0f37b3d81805c9cc20c545e9fcab988ebfca75fa936074243743ec9af9a0a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435f25bbb55b5abd07537765c02175b2a0befbf9ea8cefdadb05f6befa275a57`

```dockerfile
```

-	Layers:
	-	`sha256:aee919936bec441ad56146de620886dedd3530c12ab86907b06458b3830ba6bb`  
		Last Modified: Wed, 11 Jun 2025 02:44:37 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61bcfe58120b961061985920c2c49c43574c0fcce8fd78770660c9b06944591f`  
		Last Modified: Wed, 11 Jun 2025 02:44:38 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:16a08d2d06bd1a9d1d6bde2dc5514183f36dc2f24e13042fc37b0b45ac661e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316099000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc56c85193c27255ecb90408767f9d68c274bc1196f45cb098d5ce6b90ea6678`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:254beacf3f323cf99977d539dcb720dc371b362af3a11b68a1c46f29aa86d29f`  
		Last Modified: Tue, 10 Jun 2025 22:48:19 GMT  
		Size: 25.5 MB (25544195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c2c4f56f4973aa426bbf799db8e68cde4b53a77cca960e30f5cce80bf2aa7f`  
		Last Modified: Wed, 11 Jun 2025 12:21:38 GMT  
		Size: 290.6 MB (290554805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f5ea5defe1c1fe621608dc360df4f5ff331dd46a68fe9aa37f478977462580bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7385c0ef64071bfa1afb032a6713f45d63b380778b4b3148bdc67bd681092a`

```dockerfile
```

-	Layers:
	-	`sha256:608e9b87f0307223cfdd260a571b0d674bd45db8f0fb974229c70dc33c749df4`  
		Last Modified: Wed, 11 Jun 2025 11:44:36 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4761277bd9d0f31fe1e8c4ddddf9957abd97fa921c5288901abe244d8de3cf7d`  
		Last Modified: Wed, 11 Jun 2025 11:44:37 GMT  
		Size: 11.4 KB (11431 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:72a16720d9ddf8a7b2dc8d1b1ace588379ca56d699f1d6ade8c501aff66ba039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258525579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3db1cfb8ec57c2e1c668c37e9498d466e905042d276a2b197a07d85338ee87a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a715c260ee097512a6f8b3db5041836c3694a52db693f5778bada15c1d44f171`  
		Last Modified: Wed, 11 Jun 2025 08:45:36 GMT  
		Size: 229.8 MB (229781394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:49f73dda4259a58747e62e4eb6c4fa65628e9f66ee44bdb93ad3e1d81fb41450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bc9a1161131b8fc7f7a7ab0d7bf7c121e0abf6d42e34c83f9ba766cce41fdd`

```dockerfile
```

-	Layers:
	-	`sha256:d80007aa3456840fd8abcf804d83d4b815f907a4e06448c7f1184528cf123af0`  
		Last Modified: Wed, 11 Jun 2025 08:44:42 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84c11e33c8cd2f4d6be8f5f448f2fb501785b8e526b31e414929455af60d8693`  
		Last Modified: Wed, 11 Jun 2025 08:44:43 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.87.0-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:03c578ce0b32d4737deeefaef6ecea7f0ac648ee25d4fee767f79d9c03ae99f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 MB (320511994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32eb66db9a96fa393a694a8787f4a4b6e70abcd17e925bef5790c75a30306789`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:1294ecac50b0f4fe7018ad5e666e6e3c43bd85fbdc4ff68322834fcc70904e3c`  
		Last Modified: Tue, 10 Jun 2025 23:26:42 GMT  
		Size: 31.2 MB (31189682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563e44106503f3d016cd7490b98df9b2aa3762a7e807aeb41e5f65752ff2986`  
		Last Modified: Wed, 11 Jun 2025 04:23:04 GMT  
		Size: 289.3 MB (289322312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.87.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f3928a493fc5a10fac96213e189c2986634e3b1873790ff662e908ecc4061a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d790ae2cf1ca80cca939a505b3e9cabef2ef7c0f112000bfef0e26a552016948`

```dockerfile
```

-	Layers:
	-	`sha256:2bb507ca83c8fe4625a244cd017cd4f83a5562e41548cdec226dac403b4e6795`  
		Last Modified: Wed, 11 Jun 2025 02:44:55 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7840377069666033ca9b65919363e35adad8b9fef3da1365876affb656c0d6`  
		Last Modified: Wed, 11 Jun 2025 02:44:56 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:126df0f2a57e675f9306fe180b833982ffb996e90a92a793bb75253cfeed5475
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:2d5a7e008d9c1e86e54c0a3fffc00399eee945a13aa504fd5faf625e04110bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324451128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa6d9f8b73e08bfab3090a694fb52cea848dd5dfd249f9ff6352477596d5d38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aed27d59f9f3bafc26c73e1fa85e80d10a2b8b6221db885ef03875cbb2a92c3`  
		Last Modified: Tue, 03 Jun 2025 13:33:59 GMT  
		Size: 61.6 MB (61613723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a631e0f5786232f793b7aff2783c3a8252ee122748a6f63fb55c227e00e5002`  
		Last Modified: Tue, 03 Jun 2025 13:34:31 GMT  
		Size: 259.0 MB (259040559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:629b8efb80d6e9a1b711c46acd85e890c1c173b6b976ce39c598a8499163ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc3a74aa6b388d7315bb35c0e0fbd5fb39121d9296330833d8f9b79ffeb6a98`

```dockerfile
```

-	Layers:
	-	`sha256:03bc872db35194e79864e3a72cbb58ddd0548f438a45de2790469bf25a776a5e`  
		Last Modified: Wed, 04 Jun 2025 17:05:12 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c4e51ae8efcd54f48f7d1ced1a254f8c7ca2a7da2e3f6a81c2bedaed4895c9`  
		Last Modified: Wed, 04 Jun 2025 17:05:08 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fa3f412044d347294ad9c21eb3c9922a5e12e57b645ae53bbd27b8bc26173a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327194537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c83a1beaf9ddcfc60c8ec87a69dd7964f3e21bb48de7d530afe4816ca07fb61`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e525acaed56cf743f6ae8ee0c463c3fd7f0e9765bc0faaa7b0119fff2f2db4c4`  
		Last Modified: Tue, 03 Jun 2025 13:34:25 GMT  
		Size: 59.2 MB (59154215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1e992c2528e607b21a005bd23933eb8ae5f77fb262c96790f579f7f863d3c7`  
		Last Modified: Tue, 03 Jun 2025 13:34:30 GMT  
		Size: 263.9 MB (263904381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:0993ebd475453ccc6ded9cffa3118df8be36790fcfcf803fd1bf51bd147a22da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf7cab2f78729c23ec9792c67e373b2906e91cd19fe74c90616e885ff1ddd70`

```dockerfile
```

-	Layers:
	-	`sha256:59310aed03e6f7a9700cd2820322b4883fea2f9851c2e311a52617955a3abd14`  
		Last Modified: Wed, 04 Jun 2025 17:05:46 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e888f3541888d0dcd1e7f14fca30a9930a25f4836300284c59226514fe4b48`  
		Last Modified: Wed, 04 Jun 2025 17:05:45 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f718715b3cbe3b4fd9094909206504e5958585bd739a34dc4fb5b7f6ed2131b8`  
		Last Modified: Fri, 16 May 2025 14:17:43 GMT  
		Size: 55.3 MB (55315586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeb4a9d8a98d7b7dadf2be0b1943267d81b081cb2fb12a85484c6aaadf235fb`  
		Last Modified: Fri, 16 May 2025 14:17:57 GMT  
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
		Last Modified: Thu, 15 May 2025 20:44:31 GMT  
		Size: 711.8 KB (711789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a9394ddea85fc3e016d5927f8ce6a38638e7c7eeea1996460a0e68f6915e5c6`  
		Last Modified: Thu, 15 May 2025 20:44:31 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c6aa5430354637d99185e3c6f997bb89b34d0340d714c59489470f3b28fb00`  
		Last Modified: Thu, 08 May 2025 23:40:24 GMT  
		Size: 53.0 MB (52950277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d7b743d7f5864c65b2894547a9334b33385928622ae90e6a32c6e8856c668`  
		Last Modified: Fri, 16 May 2025 14:28:10 GMT  
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
		Last Modified: Mon, 09 Jun 2025 05:43:46 GMT  
		Size: 747.7 KB (747721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5df0c715639e649fb2f087e25e05ab1d51803c9e80193b7ded83d66aa0f06e`  
		Last Modified: Mon, 09 Jun 2025 05:43:46 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b343ca42d769a088aad30a06435916be946b7bd77c275c4c48aa9c02d07ebc6`  
		Last Modified: Thu, 15 May 2025 20:45:48 GMT  
		Size: 61.6 MB (61564812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0312ddedcb8a05877b03a2214ddd4942d87d6bd8684a5f5bc0353f72d76def`  
		Last Modified: Thu, 15 May 2025 20:46:29 GMT  
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
		Last Modified: Thu, 15 May 2025 20:44:27 GMT  
		Size: 783.8 KB (783823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f05e06b11fae76f35a913f94980f7b264abfa081dffa29929dd773c6969a089d`  
		Last Modified: Thu, 15 May 2025 20:44:27 GMT  
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
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a8d04fc53dbb480e66cf7321229cda858c75a9bfa488474aabc6a3fbc3423`  
		Last Modified: Thu, 08 May 2025 17:05:51 GMT  
		Size: 59.1 MB (59101363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd10981d51d5c4342a74b76870500712f6977bafb0891f69b5b725cd3f83575b`  
		Last Modified: Fri, 16 May 2025 13:16:00 GMT  
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
		Last Modified: Fri, 16 May 2025 14:02:45 GMT  
		Size: 863.4 KB (863409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4799a729390389da9955e76bdba397218c8fff4138d88735449c1364a6120788`  
		Last Modified: Fri, 16 May 2025 14:02:46 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.22`

```console
$ docker pull rust@sha256:126df0f2a57e675f9306fe180b833982ffb996e90a92a793bb75253cfeed5475
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.22` - linux; amd64

```console
$ docker pull rust@sha256:2d5a7e008d9c1e86e54c0a3fffc00399eee945a13aa504fd5faf625e04110bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324451128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa6d9f8b73e08bfab3090a694fb52cea848dd5dfd249f9ff6352477596d5d38`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aed27d59f9f3bafc26c73e1fa85e80d10a2b8b6221db885ef03875cbb2a92c3`  
		Last Modified: Tue, 03 Jun 2025 13:33:59 GMT  
		Size: 61.6 MB (61613723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a631e0f5786232f793b7aff2783c3a8252ee122748a6f63fb55c227e00e5002`  
		Last Modified: Tue, 03 Jun 2025 13:34:31 GMT  
		Size: 259.0 MB (259040559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:629b8efb80d6e9a1b711c46acd85e890c1c173b6b976ce39c598a8499163ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.5 KB (796520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc3a74aa6b388d7315bb35c0e0fbd5fb39121d9296330833d8f9b79ffeb6a98`

```dockerfile
```

-	Layers:
	-	`sha256:03bc872db35194e79864e3a72cbb58ddd0548f438a45de2790469bf25a776a5e`  
		Last Modified: Wed, 04 Jun 2025 17:05:12 GMT  
		Size: 784.6 KB (784602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c4e51ae8efcd54f48f7d1ced1a254f8c7ca2a7da2e3f6a81c2bedaed4895c9`  
		Last Modified: Wed, 04 Jun 2025 17:05:08 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fa3f412044d347294ad9c21eb3c9922a5e12e57b645ae53bbd27b8bc26173a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327194537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c83a1beaf9ddcfc60c8ec87a69dd7964f3e21bb48de7d530afe4816ca07fb61`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:46:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Fri, 30 May 2025 18:46:48 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Fri, 30 May 2025 18:46:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Fri, 30 May 2025 18:46:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e525acaed56cf743f6ae8ee0c463c3fd7f0e9765bc0faaa7b0119fff2f2db4c4`  
		Last Modified: Tue, 03 Jun 2025 13:34:25 GMT  
		Size: 59.2 MB (59154215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1e992c2528e607b21a005bd23933eb8ae5f77fb262c96790f579f7f863d3c7`  
		Last Modified: Tue, 03 Jun 2025 13:34:30 GMT  
		Size: 263.9 MB (263904381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:0993ebd475453ccc6ded9cffa3118df8be36790fcfcf803fd1bf51bd147a22da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 KB (876273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf7cab2f78729c23ec9792c67e373b2906e91cd19fe74c90616e885ff1ddd70`

```dockerfile
```

-	Layers:
	-	`sha256:59310aed03e6f7a9700cd2820322b4883fea2f9851c2e311a52617955a3abd14`  
		Last Modified: Wed, 04 Jun 2025 17:05:46 GMT  
		Size: 864.2 KB (864188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e888f3541888d0dcd1e7f14fca30a9930a25f4836300284c59226514fe4b48`  
		Last Modified: Wed, 04 Jun 2025 17:05:45 GMT  
		Size: 12.1 KB (12085 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:b571d7b2dc7b9154517eeda87c0c3c97865d432e95ec205e34a194fd2baaff1d
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
$ docker pull rust@sha256:6d79f767859a5f025a062505fa9f2c1a041cadafcee71fbcbd226223be462f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553345588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a4a73321e80052e6fcd636dcd4ee26c8fa0ed0d655f95d92276efb7e759cc2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8862a18fa961ebfbac8484877dd4894e96ee88177d8c4f1f54d9727262b7d`  
		Last Modified: Wed, 11 Jun 2025 02:16:04 GMT  
		Size: 211.4 MB (211370316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d73d009ce498344941c85ff822a919ac7bb8976fd68dc8174f43a594bb3fa5`  
		Last Modified: Wed, 11 Jun 2025 03:21:03 GMT  
		Size: 205.1 MB (205065498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:503b69f42140f797db581680ee944348a715f85e374bf0f64688bb5e2d7f36ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15875572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9733726f707a166e40276a18d11a14103319579caa5d58f7e146f38d2b2cbe0d`

```dockerfile
```

-	Layers:
	-	`sha256:7fea0bce605acbffe3ad3faddcc83eebdef406125bb53e8a4ea980a11ae3fe32`  
		Last Modified: Wed, 11 Jun 2025 05:44:23 GMT  
		Size: 15.9 MB (15862434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8529bb6f4380c5ac83f220695448a518ba1d0d4b38c355cab9e014939ba116b`  
		Last Modified: Wed, 11 Jun 2025 05:44:24 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:72b485162489d2c8c49c305dd8b6ba86d4ff05ad986dfc71c07c9cf752fb23b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549362604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c922227a2a41f42eae2eebb9844a4b1e45540c0b00068b270c49c1a1e0b764`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22ee2db9f8d2ea3317ceb36f4b9bc7895f6cb8402903d639c8083eaec948450`  
		Last Modified: Tue, 03 Jun 2025 13:39:41 GMT  
		Size: 175.3 MB (175297793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92df434dc3b1ce2413f6828ef2e4c81ee8a8cef9cbe94a7d2215ad2bd340b292`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 248.3 MB (248281119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2e7ce19770e0e30560aa4a23ada499e5a679b9dd1f61f479fe8d5abee6df0137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15386282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e40b43bdd8233f500a8bec0378ba7ac318dee0cafb4b7f582f11e2585a0396`

```dockerfile
```

-	Layers:
	-	`sha256:f8c270ee20e4767bc254f12fd15b19ddfb7c9f9a382a752ada7fd70bb37b3cc8`  
		Last Modified: Tue, 03 Jun 2025 15:36:17 GMT  
		Size: 15.4 MB (15373035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d32c5949c1f294d1c9fdbee6216a2148b76a885326b5d0372c69b726ab518b0`  
		Last Modified: Tue, 03 Jun 2025 15:36:16 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:40b030bf2085108f7fe5f75de0454fd4f6f855182477906360f40c0c29e95ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513085197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cecf015e8a7925026c922f69a93f75798f571a03fe30546ac7915e8760aaaa9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ee5cb7152015437e4a9b3066ae9e25a26a3bef6617d0b7f25368511c2d954`  
		Last Modified: Tue, 03 Jun 2025 13:30:35 GMT  
		Size: 202.8 MB (202762554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8a70e7346d3f568e98a68fc27e54274c16511edcd67498ae24761da6880cf6`  
		Last Modified: Tue, 03 Jun 2025 13:33:54 GMT  
		Size: 174.1 MB (174082075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9719468f301df89ccc1071537f751d5e28f0c45df8834a133614066e3f97fd22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15612386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27147e11d32faab39878abb0d8cd3ca6bd4c56331b1722b30d8f48f9a45ece6e`

```dockerfile
```

-	Layers:
	-	`sha256:cc53a730eadb9784a7c191236378a7bcf219afa01f680521eb4bddf1d8ac993e`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 15.6 MB (15599095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e5657bfd53d43e028eb9d10e36db17bcc612d8fae30e5fe0fb076caa4b489b`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:8173985fad86853be81c2d2d427c1a22ad9d919982c5feb33ee56cc79a4b3c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579415232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e17162e2db334c9d6ff28fbd81344a20a803fde6a517c1c9410e6078a5a45d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731d58cf259468f5a31e00d6a586bde147720039c92e6c1ff4cb48a5dd996ae`  
		Last Modified: Wed, 11 Jun 2025 00:00:38 GMT  
		Size: 24.9 MB (24855706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce073e7b00b22009464483e266ff8ba48a8c0db86f16c877aa302337bbed6e9`  
		Last Modified: Wed, 11 Jun 2025 01:13:32 GMT  
		Size: 66.2 MB (66225240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75453a9e8c0ecda25b39aaabe16c9694b0bdb799dbc4bb61d1d0aee7d8b70850`  
		Last Modified: Wed, 11 Jun 2025 02:15:24 GMT  
		Size: 210.3 MB (210300359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a8e4b0736bc7a3d22fb842ad0ee81737c0ed14f5fe26606d2f4b5123616b6`  
		Last Modified: Wed, 11 Jun 2025 06:01:45 GMT  
		Size: 228.6 MB (228556453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ab0c67f770b8da0cbe9479ecec374333e09badd00136782ce748b9cd17e281c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273c89500eb4e84dfb414ccb465c200b7f2a92f66f0b44e6f219b7dde68417b4`

```dockerfile
```

-	Layers:
	-	`sha256:dc04aee6f7f1d600381837690bbefc0648653c65ede9e2ecb6dc60dd7740d0c3`  
		Last Modified: Wed, 11 Jun 2025 05:45:01 GMT  
		Size: 15.8 MB (15839332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a2d3bfd52375162462af27b77692b39e0868ce869675ce142d35c98dcb3f11`  
		Last Modified: Wed, 11 Jun 2025 05:45:02 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:294e06b00a43a648e43744691fbef73c1bdb451465ac350c76f736ed8a50b602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639200335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98218e5b1f057d84b638dd735f30b4a14abac5bb993b7561c9580a3babcd22dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Tue, 03 Jun 2025 13:36:57 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Tue, 03 Jun 2025 13:36:59 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5288618fea79e9a348995382235e6bee52819db4047a345ffaeaddd2b82e06`  
		Last Modified: Tue, 03 Jun 2025 13:37:01 GMT  
		Size: 214.4 MB (214416172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acddbc7af9fd8740373f8026a505be271623021d28c5aaf7cf9cfce5371e307`  
		Last Modified: Tue, 03 Jun 2025 15:36:39 GMT  
		Size: 277.0 MB (276955569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:60293968af0cc8afff5372a51d16244ad649290286e9457b6475a872eaf44c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15558952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90744ca96e8742bd842f46bb381ee8f2bd14a575fbfcf610a629445664ae33b`

```dockerfile
```

-	Layers:
	-	`sha256:e7bef55039062c7c4ae93c0994d2baa58cc23620f26310f07c85affb73ade0e6`  
		Last Modified: Tue, 03 Jun 2025 15:36:29 GMT  
		Size: 15.5 MB (15545745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ac5c316843cde59da34e1480f62e0a90b78ace51a57f9f67917ce2812741f6`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b9f17d320e48e042011cee37b615b2594ca1ac94588789d0978ac65e5e9671b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604371175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7ddbb7c8c246892af6179b2b4a9b8f8ceb4a0b60eff22c4736c5eaaf52b114`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Tue, 03 Jun 2025 13:37:08 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Tue, 03 Jun 2025 13:37:11 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3151505c70d8a7022bb518bbfce9c7488d1dd6ab624e1d96b883eb0654da7562`  
		Last Modified: Tue, 03 Jun 2025 13:37:22 GMT  
		Size: 183.4 MB (183405201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b0882d1ed7e92235dfca31dcc58a7de4c5cad3b764f0fe10874904586c5009`  
		Last Modified: Tue, 03 Jun 2025 14:16:08 GMT  
		Size: 286.3 MB (286308749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:751099b710c1a89fa55e82f9bc0fabfd70cb451e25cfbc7fc9449cc3fec7df28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15394148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd99f87c0d557b247c0e2c29a586dd93187c2ded1f463a78dd244eed473ac43a`

```dockerfile
```

-	Layers:
	-	`sha256:2d523435dd3012b7c822fc76bd1967e45ece2c7c3cda49a5a98a4c7c9fa13591`  
		Last Modified: Tue, 03 Jun 2025 15:36:32 GMT  
		Size: 15.4 MB (15381009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d39102b0130d44f2ec934dd1a55a3718747eb90d0591508f65d806ba52f578`  
		Last Modified: Tue, 03 Jun 2025 15:36:31 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:acd48e9a3f1a6cbfe9de41c88984b9dffa24c4e3e1f881d00c1b99145a0731e2
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
$ docker pull rust@sha256:867389037b7b993d5901a4dc22f719439d56df6322ae8ee5b3d659164ad8a90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526485218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34027bad41e7c5a2dfde8329ad0cdc735ca4cf8afc2bda755755a229a103d19d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2678613884c2f141cc551880b1a1587f0c890606a900bbac5a1ace2645be657`  
		Last Modified: Wed, 11 Jun 2025 00:02:35 GMT  
		Size: 54.8 MB (54757363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c6624995870ade650aaf0f5b37565d2e41e2500e8105fd69b79900eef086cf`  
		Last Modified: Wed, 11 Jun 2025 02:16:19 GMT  
		Size: 197.1 MB (197142069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40689c5eb1b4170233c72a76fb229e2b672f3ecbe0dfaba41511809c1f0054be`  
		Last Modified: Wed, 11 Jun 2025 03:20:02 GMT  
		Size: 205.1 MB (205065865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6939a7548b0bfc37a63c429bda574a8467fe2f00ec42b56a2d48f8407fa16a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15475148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6174e312182a700930c62add7e8dbe79bc0b6c7a153f83b5b3a5b150e2bedd3f`

```dockerfile
```

-	Layers:
	-	`sha256:82873fb0fa119fd347188508fb45ca824a73b0d6afc0611c941197f4af538f52`  
		Last Modified: Wed, 11 Jun 2025 05:44:34 GMT  
		Size: 15.5 MB (15463899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:782b06ea0a8cdf38dbf3b8fb9b63fa091b5c73b1d89bbfbd4c7a88c3356f08c8`  
		Last Modified: Wed, 11 Jun 2025 05:44:35 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:f0099d1100af3de76397f6b72386fb82e5bfe767c199e3af9dacabcb847cd818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.4 MB (530413542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a851fda81799e9f774be69c775a4b41a18a92ffb711d53f4a2fb7adbae061b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
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
	-	`sha256:2bf062f1f44f96722293994387f4b88016e2f0a9f49c7f09b2ceffefc7717199`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 49.0 MB (49041988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933c7aef3dae867caad0cbafef5672fb39317c04b3bf8bff0868bf265098c4de`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 14.9 MB (14880519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0144e65734487c61a592b9ecd7d576c77bc270bd5d65049de36718f77416c6`  
		Last Modified: Tue, 03 Jun 2025 14:32:58 GMT  
		Size: 50.6 MB (50631322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c9ac1f243c709a0fa1779761ca68b4f1c6b9419089c5cd54dcb97bb3d22f54`  
		Last Modified: Tue, 03 Jun 2025 14:33:03 GMT  
		Size: 167.6 MB (167578499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae8b0608788d75c99991c8f9c893341f4d11f3bc4aab4994d6807ed4b8d8163`  
		Last Modified: Thu, 05 Jun 2025 16:53:56 GMT  
		Size: 248.3 MB (248281214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:2cde4e1249e67514f7134d4cbb09b7ee38dd9714da18dcad9d4f654e29137c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14985623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a5ac1d1f5eb5b234db53835a6e11e4c5bf285fcac3a9d866d14a491a75c58d`

```dockerfile
```

-	Layers:
	-	`sha256:482f3adc2f97de782cc024fa5f52aa7dc9524f1440c109d95f33f0532d4878ff`  
		Last Modified: Wed, 11 Jun 2025 05:44:45 GMT  
		Size: 15.0 MB (14974298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ee59cf0e8a7913c311c3a1e425258ded463181f50bd06e068c6172b8725b4d`  
		Last Modified: Wed, 11 Jun 2025 05:44:46 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d9a2d79db5bd7b83232ed720e7460b712a4b3e4928d685f2235c2bf3ba8d5d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486978031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43e429bad1c4ae05ed881da09a277098e088e0e2baa6160638701e0d8dbc76a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a602f78cf8d696db9521d18affb7ecdb79ff690533efae26e3bdb1544cb1752`  
		Last Modified: Tue, 03 Jun 2025 13:31:09 GMT  
		Size: 15.8 MB (15750382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1b27af19f7550ac0d9c38bf6bcf26ba7eb53984e7e5e0886342816133c76e`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 54.9 MB (54853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d0d4413e7427c3ec24a23fc978dced4b2de0294ec9d2e02645e0f62aa2de32`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 190.0 MB (190044698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79cea524fba17622c1c30c1189d43e20ecef3a912b0c98eade8501625fc699b`  
		Last Modified: Tue, 03 Jun 2025 14:20:24 GMT  
		Size: 174.1 MB (174081960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f2c10e422b56bc7311c6e7a10646a49504aad296319e2495888010bf46be7246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe291b6ae25a37ca79695b56eb405b23c994dde1a5c2bb6a0870abd60f6af0d7`

```dockerfile
```

-	Layers:
	-	`sha256:6f81d3f70ab207ec9aadb6eb3a55fe12e8d125470cc73aa35be912d8c206ad93`  
		Last Modified: Wed, 11 Jun 2025 05:44:56 GMT  
		Size: 15.2 MB (15176927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5df7740191a1cba2214b1d3bc8489b68a7b671d82f48fac368d2c938dd1a0a58`  
		Last Modified: Wed, 11 Jun 2025 05:44:57 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:7a323c00d871336669f30ee2a4e6310bf99cea3b3d99279391cef0f3b69e84a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.6 MB (555605760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dabbac26160a93389a46a4bb2dd7d91f7d94dae182f0866446402a405b47539`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
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
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e7c1ed34c380b4c9e9f08e94b0f7b9bf90a0e8c42de246cb4b2159e2126fef`  
		Last Modified: Wed, 11 Jun 2025 00:00:47 GMT  
		Size: 16.3 MB (16268617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3a34392e433938214bbf2cba34365a474d819c470686803059c6d8390cf680`  
		Last Modified: Wed, 11 Jun 2025 01:13:31 GMT  
		Size: 56.0 MB (56049939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fc14c21031cb8eae2e7bca81acab0fca46817b5d8a4fa7fbfb97ff76557da5`  
		Last Modified: Wed, 11 Jun 2025 02:14:17 GMT  
		Size: 200.0 MB (200041378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f45e8e404b579a46068dee78945e0a0853c35cfb3c8a243538f86ff1821f17b`  
		Last Modified: Wed, 11 Jun 2025 09:54:26 GMT  
		Size: 228.6 MB (228555814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:63ea2ff898633a248c8bed35c0c0507387f1f57579f214745875538a0a8db1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15461818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f08987abd3e9f97128af9ebb7b448c5fb3e5ea5ab678209c26dcd46460e41e`

```dockerfile
```

-	Layers:
	-	`sha256:49ffb54271663c1d37909753b4895c96d08d07308be90ee479ef685461712fba`  
		Last Modified: Wed, 11 Jun 2025 05:45:08 GMT  
		Size: 15.5 MB (15450601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:191e5f9bf2a3f582caff72f6b5628f333cb7c8de24c23c3ea181aad5630b3378`  
		Last Modified: Wed, 11 Jun 2025 05:45:09 GMT  
		Size: 11.2 KB (11217 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:b571d7b2dc7b9154517eeda87c0c3c97865d432e95ec205e34a194fd2baaff1d
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
$ docker pull rust@sha256:6d79f767859a5f025a062505fa9f2c1a041cadafcee71fbcbd226223be462f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.3 MB (553345588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a4a73321e80052e6fcd636dcd4ee26c8fa0ed0d655f95d92276efb7e759cc2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8862a18fa961ebfbac8484877dd4894e96ee88177d8c4f1f54d9727262b7d`  
		Last Modified: Wed, 11 Jun 2025 02:16:04 GMT  
		Size: 211.4 MB (211370316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d73d009ce498344941c85ff822a919ac7bb8976fd68dc8174f43a594bb3fa5`  
		Last Modified: Wed, 11 Jun 2025 03:21:03 GMT  
		Size: 205.1 MB (205065498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:503b69f42140f797db581680ee944348a715f85e374bf0f64688bb5e2d7f36ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15875572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9733726f707a166e40276a18d11a14103319579caa5d58f7e146f38d2b2cbe0d`

```dockerfile
```

-	Layers:
	-	`sha256:7fea0bce605acbffe3ad3faddcc83eebdef406125bb53e8a4ea980a11ae3fe32`  
		Last Modified: Wed, 11 Jun 2025 05:44:23 GMT  
		Size: 15.9 MB (15862434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8529bb6f4380c5ac83f220695448a518ba1d0d4b38c355cab9e014939ba116b`  
		Last Modified: Wed, 11 Jun 2025 05:44:24 GMT  
		Size: 13.1 KB (13138 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:72b485162489d2c8c49c305dd8b6ba86d4ff05ad986dfc71c07c9cf752fb23b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 MB (549362604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c922227a2a41f42eae2eebb9844a4b1e45540c0b00068b270c49c1a1e0b764`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22ee2db9f8d2ea3317ceb36f4b9bc7895f6cb8402903d639c8083eaec948450`  
		Last Modified: Tue, 03 Jun 2025 13:39:41 GMT  
		Size: 175.3 MB (175297793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92df434dc3b1ce2413f6828ef2e4c81ee8a8cef9cbe94a7d2215ad2bd340b292`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 248.3 MB (248281119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:2e7ce19770e0e30560aa4a23ada499e5a679b9dd1f61f479fe8d5abee6df0137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15386282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e40b43bdd8233f500a8bec0378ba7ac318dee0cafb4b7f582f11e2585a0396`

```dockerfile
```

-	Layers:
	-	`sha256:f8c270ee20e4767bc254f12fd15b19ddfb7c9f9a382a752ada7fd70bb37b3cc8`  
		Last Modified: Tue, 03 Jun 2025 15:36:17 GMT  
		Size: 15.4 MB (15373035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d32c5949c1f294d1c9fdbee6216a2148b76a885326b5d0372c69b726ab518b0`  
		Last Modified: Tue, 03 Jun 2025 15:36:16 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:40b030bf2085108f7fe5f75de0454fd4f6f855182477906360f40c0c29e95ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513085197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cecf015e8a7925026c922f69a93f75798f571a03fe30546ac7915e8760aaaa9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ee5cb7152015437e4a9b3066ae9e25a26a3bef6617d0b7f25368511c2d954`  
		Last Modified: Tue, 03 Jun 2025 13:30:35 GMT  
		Size: 202.8 MB (202762554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8a70e7346d3f568e98a68fc27e54274c16511edcd67498ae24761da6880cf6`  
		Last Modified: Tue, 03 Jun 2025 13:33:54 GMT  
		Size: 174.1 MB (174082075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:9719468f301df89ccc1071537f751d5e28f0c45df8834a133614066e3f97fd22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15612386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27147e11d32faab39878abb0d8cd3ca6bd4c56331b1722b30d8f48f9a45ece6e`

```dockerfile
```

-	Layers:
	-	`sha256:cc53a730eadb9784a7c191236378a7bcf219afa01f680521eb4bddf1d8ac993e`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 15.6 MB (15599095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e5657bfd53d43e028eb9d10e36db17bcc612d8fae30e5fe0fb076caa4b489b`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 13.3 KB (13291 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:8173985fad86853be81c2d2d427c1a22ad9d919982c5feb33ee56cc79a4b3c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579415232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e17162e2db334c9d6ff28fbd81344a20a803fde6a517c1c9410e6078a5a45d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731d58cf259468f5a31e00d6a586bde147720039c92e6c1ff4cb48a5dd996ae`  
		Last Modified: Wed, 11 Jun 2025 00:00:38 GMT  
		Size: 24.9 MB (24855706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce073e7b00b22009464483e266ff8ba48a8c0db86f16c877aa302337bbed6e9`  
		Last Modified: Wed, 11 Jun 2025 01:13:32 GMT  
		Size: 66.2 MB (66225240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75453a9e8c0ecda25b39aaabe16c9694b0bdb799dbc4bb61d1d0aee7d8b70850`  
		Last Modified: Wed, 11 Jun 2025 02:15:24 GMT  
		Size: 210.3 MB (210300359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a8e4b0736bc7a3d22fb842ad0ee81737c0ed14f5fe26606d2f4b5123616b6`  
		Last Modified: Wed, 11 Jun 2025 06:01:45 GMT  
		Size: 228.6 MB (228556453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:ab0c67f770b8da0cbe9479ecec374333e09badd00136782ce748b9cd17e281c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15852419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273c89500eb4e84dfb414ccb465c200b7f2a92f66f0b44e6f219b7dde68417b4`

```dockerfile
```

-	Layers:
	-	`sha256:dc04aee6f7f1d600381837690bbefc0648653c65ede9e2ecb6dc60dd7740d0c3`  
		Last Modified: Wed, 11 Jun 2025 05:45:01 GMT  
		Size: 15.8 MB (15839332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a2d3bfd52375162462af27b77692b39e0868ce869675ce142d35c98dcb3f11`  
		Last Modified: Wed, 11 Jun 2025 05:45:02 GMT  
		Size: 13.1 KB (13087 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:294e06b00a43a648e43744691fbef73c1bdb451465ac350c76f736ed8a50b602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 MB (639200335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98218e5b1f057d84b638dd735f30b4a14abac5bb993b7561c9580a3babcd22dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Tue, 03 Jun 2025 13:36:57 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Tue, 03 Jun 2025 13:36:59 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5288618fea79e9a348995382235e6bee52819db4047a345ffaeaddd2b82e06`  
		Last Modified: Tue, 03 Jun 2025 13:37:01 GMT  
		Size: 214.4 MB (214416172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acddbc7af9fd8740373f8026a505be271623021d28c5aaf7cf9cfce5371e307`  
		Last Modified: Tue, 03 Jun 2025 15:36:39 GMT  
		Size: 277.0 MB (276955569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:60293968af0cc8afff5372a51d16244ad649290286e9457b6475a872eaf44c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15558952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90744ca96e8742bd842f46bb381ee8f2bd14a575fbfcf610a629445664ae33b`

```dockerfile
```

-	Layers:
	-	`sha256:e7bef55039062c7c4ae93c0994d2baa58cc23620f26310f07c85affb73ade0e6`  
		Last Modified: Tue, 03 Jun 2025 15:36:29 GMT  
		Size: 15.5 MB (15545745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ac5c316843cde59da34e1480f62e0a90b78ace51a57f9f67917ce2812741f6`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:b9f17d320e48e042011cee37b615b2594ca1ac94588789d0978ac65e5e9671b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 MB (604371175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7ddbb7c8c246892af6179b2b4a9b8f8ceb4a0b60eff22c4736c5eaaf52b114`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Tue, 03 Jun 2025 13:37:08 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Tue, 03 Jun 2025 13:37:11 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3151505c70d8a7022bb518bbfce9c7488d1dd6ab624e1d96b883eb0654da7562`  
		Last Modified: Tue, 03 Jun 2025 13:37:22 GMT  
		Size: 183.4 MB (183405201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b0882d1ed7e92235dfca31dcc58a7de4c5cad3b764f0fe10874904586c5009`  
		Last Modified: Tue, 03 Jun 2025 14:16:08 GMT  
		Size: 286.3 MB (286308749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:751099b710c1a89fa55e82f9bc0fabfd70cb451e25cfbc7fc9449cc3fec7df28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15394148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd99f87c0d557b247c0e2c29a586dd93187c2ded1f463a78dd244eed473ac43a`

```dockerfile
```

-	Layers:
	-	`sha256:2d523435dd3012b7c822fc76bd1967e45ece2c7c3cda49a5a98a4c7c9fa13591`  
		Last Modified: Tue, 03 Jun 2025 15:36:32 GMT  
		Size: 15.4 MB (15381009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d39102b0130d44f2ec934dd1a55a3718747eb90d0591508f65d806ba52f578`  
		Last Modified: Tue, 03 Jun 2025 15:36:31 GMT  
		Size: 13.1 KB (13139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:437507c3e719e4f968033b88d851ffa9f5aceeb2dcc2482cc6cb7647811a55eb
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
$ docker pull rust@sha256:c6d2b4f8115be78af2a07072f61cffbbb4d6c93b55a4712b922fb7391db6a2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3a4353cc539aea8fad45dd0dc90225aa41fc00a850fec6c15024aa793caa8f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb49401afa0e17bb5553a2c29d1dfcf82e44a6f845092a3e727d07c58cae51e`  
		Last Modified: Wed, 11 Jun 2025 02:46:35 GMT  
		Size: 275.8 MB (275821770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:b992a82898a09273268714a1bee7910884463b9c54cff38b0a9aaed379224967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0efaf5c9b3bde5d5403cd7bfe7cd6cffebb0c548fad83f1c45b60d09237485d`

```dockerfile
```

-	Layers:
	-	`sha256:1444619cb92821045d11ffb02735da01990b56835388b8489569925a16c9a85b`  
		Last Modified: Wed, 11 Jun 2025 02:44:27 GMT  
		Size: 4.1 MB (4093196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860531365ea841bb950e17b4e50e3de256a47221cfdf954a40ea40c86c3dee21`  
		Last Modified: Wed, 11 Jun 2025 02:44:28 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:966e7302a5f24503c2fb6de767fae05595b40e37222459764a0a385ec37af077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320043588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b958cc8bdf7ee0e305edf9ce0e0863ceab33ff294219118e308d1cb2cae0aa9c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10dd721eeaf60b511757cc253292582f2dbe051a02adf667aa8ac4ba94997f0`  
		Last Modified: Wed, 11 Jun 2025 12:01:23 GMT  
		Size: 296.1 MB (296104844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:961687e45e0a213ac59675555b8ef714187ab0f3940ca58601da576f49066253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cc0add7a9f0b20fbb1b6d07518f411b4aeaa40dda619c70a752aedda655f1e`

```dockerfile
```

-	Layers:
	-	`sha256:4a53c52228ba7e41746447e406b7d8ce69b8ad263bd576e3ddb52841ae765dab`  
		Last Modified: Wed, 11 Jun 2025 11:44:27 GMT  
		Size: 3.9 MB (3907625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d0c6505620255b5d1bd1af5fa4ed9ed1f6a644865f9168f949f8fad11a10d0`  
		Last Modified: Wed, 11 Jun 2025 11:44:28 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0e216c245a1044e77982d24fd09991448bcd12648115cd6bf2ce1c3d63633a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268005202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834da5b79b78574e38bf973a76161d294a637d950101652138b9dbb92595d5ae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3835d9003112b328f6866eb687138cc59ca3dea0da56c9da555f235723c3a464`  
		Last Modified: Wed, 11 Jun 2025 08:47:07 GMT  
		Size: 239.9 MB (239927527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:2bcd57c614490ddc32c882435e924dcf857670d889481a167b10104b8f71d03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44c4ec5937533284046291218fb2b0376ff4649f1d44f388921b997949dc39f`

```dockerfile
```

-	Layers:
	-	`sha256:a7c21ba2560f3f989e8e7892ec85f8ed9b4fb76fabd4e88ec1e92f54a6de3fb9`  
		Last Modified: Wed, 11 Jun 2025 08:44:36 GMT  
		Size: 4.1 MB (4115540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168233367a2fd0fd2e5e9d69c0e40d5ef353bc704f5cebd9ec8a8b20a7a53703`  
		Last Modified: Wed, 11 Jun 2025 08:44:37 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:2ad11b3f0daccba195c8a3e2d537873b28c0a4d9739f06cc67c58451bf7a42b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325379390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b7914ccdd8d8409e9d85ee45f9969a13ef81e3e7ca5cd62b402205104f6d62`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7541639b044ca0ee0b02dbb730ab58d7da071f667f2a37ab0173489a979a307`  
		Last Modified: Wed, 11 Jun 2025 03:02:06 GMT  
		Size: 296.2 MB (296166957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:96ac86d3fdb37019662687ae8d46c3b145d264dcac844eb7d01cb9fb312769af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b424745a3a740149528fb53d8e6c563c3eeb9457ce88ec0538e221a0ffedf4f4`

```dockerfile
```

-	Layers:
	-	`sha256:6805d028c613af8d87b3ba1f5f56ae1c8e543065cde206869d7031d4b89fee3a`  
		Last Modified: Wed, 11 Jun 2025 02:44:44 GMT  
		Size: 4.1 MB (4072559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc4f4c22e4ea63b843fa608be1c31913653a04d371f1d372f63ab39cdf0fec2`  
		Last Modified: Wed, 11 Jun 2025 02:44:45 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:333d0518b417fd65a06c5a0ee4217fe07e9345093922191979f25a8901395ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377793386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43dd89cf4392e35cda901f980625fedd6b33b8ca171df7416f97273cee5f5fe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641961947f2e89b9782726648e622e267f8a2e965318c701be9c3141d43f9f5`  
		Last Modified: Wed, 11 Jun 2025 09:01:40 GMT  
		Size: 345.7 MB (345720591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:eb1a17643ff56aa1c2370c7f17f04522bf68c405f72150edd08aac2bf0398359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4078847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadaab8a496b8047c9ae84aa96b01e8a4a8c05f00eb3dfe6a62795d3119938d7`

```dockerfile
```

-	Layers:
	-	`sha256:50bbf10950c98ad566b72902fa2c8a087e58b6c3b3b265711bcaa1330922dbb3`  
		Last Modified: Wed, 11 Jun 2025 08:44:44 GMT  
		Size: 4.1 MB (4065509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60fecd5b455a4ae648136c59e20d9e13d41c7aef26ed54572d1a86744ccf3ef0`  
		Last Modified: Wed, 11 Jun 2025 08:44:45 GMT  
		Size: 13.3 KB (13338 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:5faea305cb32004ab4694cf9be72db317b86544c70cef24a43c9863e756ea6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363336119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f475f06d4297efbaf55ad8aae30d81a630a62cdd9286374386ae9d5facc0082e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f552a08d6186725df4030ad88bf2b444cc4868a9bfb86570d7cf36dd450471ee`  
		Last Modified: Wed, 11 Jun 2025 09:02:21 GMT  
		Size: 336.4 MB (336448266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:af734c9315ffbb0607238ba1205d3a3ba0250e7a63158b73cdc27e135f406e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc43a07563773310da6d9a09b86d0264d7db9b6542b5c600d604a26301fad5d`

```dockerfile
```

-	Layers:
	-	`sha256:76749c6d7cca227b6b9fa93d011effbc232138d91f89ff0944eb8c07b9179bf0`  
		Last Modified: Wed, 11 Jun 2025 08:44:50 GMT  
		Size: 3.9 MB (3930874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d70369bbe1eee7920586d7a5d9d0ce8a7f8a4c869fb9f9c0fa15589bd6cfb5c`  
		Last Modified: Wed, 11 Jun 2025 08:44:51 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:437507c3e719e4f968033b88d851ffa9f5aceeb2dcc2482cc6cb7647811a55eb
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
$ docker pull rust@sha256:c6d2b4f8115be78af2a07072f61cffbbb4d6c93b55a4712b922fb7391db6a2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304051899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3a4353cc539aea8fad45dd0dc90225aa41fc00a850fec6c15024aa793caa8f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb49401afa0e17bb5553a2c29d1dfcf82e44a6f845092a3e727d07c58cae51e`  
		Last Modified: Wed, 11 Jun 2025 02:46:35 GMT  
		Size: 275.8 MB (275821770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b992a82898a09273268714a1bee7910884463b9c54cff38b0a9aaed379224967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0efaf5c9b3bde5d5403cd7bfe7cd6cffebb0c548fad83f1c45b60d09237485d`

```dockerfile
```

-	Layers:
	-	`sha256:1444619cb92821045d11ffb02735da01990b56835388b8489569925a16c9a85b`  
		Last Modified: Wed, 11 Jun 2025 02:44:27 GMT  
		Size: 4.1 MB (4093196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860531365ea841bb950e17b4e50e3de256a47221cfdf954a40ea40c86c3dee21`  
		Last Modified: Wed, 11 Jun 2025 02:44:28 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:966e7302a5f24503c2fb6de767fae05595b40e37222459764a0a385ec37af077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320043588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b958cc8bdf7ee0e305edf9ce0e0863ceab33ff294219118e308d1cb2cae0aa9c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10dd721eeaf60b511757cc253292582f2dbe051a02adf667aa8ac4ba94997f0`  
		Last Modified: Wed, 11 Jun 2025 12:01:23 GMT  
		Size: 296.1 MB (296104844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:961687e45e0a213ac59675555b8ef714187ab0f3940ca58601da576f49066253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cc0add7a9f0b20fbb1b6d07518f411b4aeaa40dda619c70a752aedda655f1e`

```dockerfile
```

-	Layers:
	-	`sha256:4a53c52228ba7e41746447e406b7d8ce69b8ad263bd576e3ddb52841ae765dab`  
		Last Modified: Wed, 11 Jun 2025 11:44:27 GMT  
		Size: 3.9 MB (3907625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d0c6505620255b5d1bd1af5fa4ed9ed1f6a644865f9168f949f8fad11a10d0`  
		Last Modified: Wed, 11 Jun 2025 11:44:28 GMT  
		Size: 13.4 KB (13379 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:f0e216c245a1044e77982d24fd09991448bcd12648115cd6bf2ce1c3d63633a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268005202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834da5b79b78574e38bf973a76161d294a637d950101652138b9dbb92595d5ae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3835d9003112b328f6866eb687138cc59ca3dea0da56c9da555f235723c3a464`  
		Last Modified: Wed, 11 Jun 2025 08:47:07 GMT  
		Size: 239.9 MB (239927527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:2bcd57c614490ddc32c882435e924dcf857670d889481a167b10104b8f71d03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44c4ec5937533284046291218fb2b0376ff4649f1d44f388921b997949dc39f`

```dockerfile
```

-	Layers:
	-	`sha256:a7c21ba2560f3f989e8e7892ec85f8ed9b4fb76fabd4e88ec1e92f54a6de3fb9`  
		Last Modified: Wed, 11 Jun 2025 08:44:36 GMT  
		Size: 4.1 MB (4115540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168233367a2fd0fd2e5e9d69c0e40d5ef353bc704f5cebd9ec8a8b20a7a53703`  
		Last Modified: Wed, 11 Jun 2025 08:44:37 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:2ad11b3f0daccba195c8a3e2d537873b28c0a4d9739f06cc67c58451bf7a42b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325379390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b7914ccdd8d8409e9d85ee45f9969a13ef81e3e7ca5cd62b402205104f6d62`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7541639b044ca0ee0b02dbb730ab58d7da071f667f2a37ab0173489a979a307`  
		Last Modified: Wed, 11 Jun 2025 03:02:06 GMT  
		Size: 296.2 MB (296166957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:96ac86d3fdb37019662687ae8d46c3b145d264dcac844eb7d01cb9fb312769af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b424745a3a740149528fb53d8e6c563c3eeb9457ce88ec0538e221a0ffedf4f4`

```dockerfile
```

-	Layers:
	-	`sha256:6805d028c613af8d87b3ba1f5f56ae1c8e543065cde206869d7031d4b89fee3a`  
		Last Modified: Wed, 11 Jun 2025 02:44:44 GMT  
		Size: 4.1 MB (4072559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc4f4c22e4ea63b843fa608be1c31913653a04d371f1d372f63ab39cdf0fec2`  
		Last Modified: Wed, 11 Jun 2025 02:44:45 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:333d0518b417fd65a06c5a0ee4217fe07e9345093922191979f25a8901395ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377793386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43dd89cf4392e35cda901f980625fedd6b33b8ca171df7416f97273cee5f5fe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641961947f2e89b9782726648e622e267f8a2e965318c701be9c3141d43f9f5`  
		Last Modified: Wed, 11 Jun 2025 09:01:40 GMT  
		Size: 345.7 MB (345720591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:eb1a17643ff56aa1c2370c7f17f04522bf68c405f72150edd08aac2bf0398359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4078847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadaab8a496b8047c9ae84aa96b01e8a4a8c05f00eb3dfe6a62795d3119938d7`

```dockerfile
```

-	Layers:
	-	`sha256:50bbf10950c98ad566b72902fa2c8a087e58b6c3b3b265711bcaa1330922dbb3`  
		Last Modified: Wed, 11 Jun 2025 08:44:44 GMT  
		Size: 4.1 MB (4065509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60fecd5b455a4ae648136c59e20d9e13d41c7aef26ed54572d1a86744ccf3ef0`  
		Last Modified: Wed, 11 Jun 2025 08:44:45 GMT  
		Size: 13.3 KB (13338 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:5faea305cb32004ab4694cf9be72db317b86544c70cef24a43c9863e756ea6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363336119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f475f06d4297efbaf55ad8aae30d81a630a62cdd9286374386ae9d5facc0082e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f552a08d6186725df4030ad88bf2b444cc4868a9bfb86570d7cf36dd450471ee`  
		Last Modified: Wed, 11 Jun 2025 09:02:21 GMT  
		Size: 336.4 MB (336448266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:af734c9315ffbb0607238ba1205d3a3ba0250e7a63158b73cdc27e135f406e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc43a07563773310da6d9a09b86d0264d7db9b6542b5c600d604a26301fad5d`

```dockerfile
```

-	Layers:
	-	`sha256:76749c6d7cca227b6b9fa93d011effbc232138d91f89ff0944eb8c07b9179bf0`  
		Last Modified: Wed, 11 Jun 2025 08:44:50 GMT  
		Size: 3.9 MB (3930874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d70369bbe1eee7920586d7a5d9d0ce8a7f8a4c869fb9f9c0fa15589bd6cfb5c`  
		Last Modified: Wed, 11 Jun 2025 08:44:51 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:c8bfa46d68a20e878e316e8302790d5f8c7410c56e35b562507d50f2bec64dd7
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
$ docker pull rust@sha256:39269e5da7fa88d82b633d74443d591bb0b7ec42c04e303356f7263217cf3e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295462508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b70ff91aa20633a2a939769ff5ae727e5dbad08a87aaa6968d3e778b11dad`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986242588b209fdbc06bae0292eda94e58818e8a997967091183318a0308eb6`  
		Last Modified: Wed, 11 Jun 2025 02:56:02 GMT  
		Size: 265.2 MB (265206444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f0f37b3d81805c9cc20c545e9fcab988ebfca75fa936074243743ec9af9a0a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435f25bbb55b5abd07537765c02175b2a0befbf9ea8cefdadb05f6befa275a57`

```dockerfile
```

-	Layers:
	-	`sha256:aee919936bec441ad56146de620886dedd3530c12ab86907b06458b3830ba6bb`  
		Last Modified: Wed, 11 Jun 2025 02:44:37 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61bcfe58120b961061985920c2c49c43574c0fcce8fd78770660c9b06944591f`  
		Last Modified: Wed, 11 Jun 2025 02:44:38 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:16a08d2d06bd1a9d1d6bde2dc5514183f36dc2f24e13042fc37b0b45ac661e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316099000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc56c85193c27255ecb90408767f9d68c274bc1196f45cb098d5ce6b90ea6678`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:254beacf3f323cf99977d539dcb720dc371b362af3a11b68a1c46f29aa86d29f`  
		Last Modified: Tue, 10 Jun 2025 22:48:19 GMT  
		Size: 25.5 MB (25544195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c2c4f56f4973aa426bbf799db8e68cde4b53a77cca960e30f5cce80bf2aa7f`  
		Last Modified: Wed, 11 Jun 2025 12:21:38 GMT  
		Size: 290.6 MB (290554805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f5ea5defe1c1fe621608dc360df4f5ff331dd46a68fe9aa37f478977462580bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7385c0ef64071bfa1afb032a6713f45d63b380778b4b3148bdc67bd681092a`

```dockerfile
```

-	Layers:
	-	`sha256:608e9b87f0307223cfdd260a571b0d674bd45db8f0fb974229c70dc33c749df4`  
		Last Modified: Wed, 11 Jun 2025 11:44:36 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4761277bd9d0f31fe1e8c4ddddf9957abd97fa921c5288901abe244d8de3cf7d`  
		Last Modified: Wed, 11 Jun 2025 11:44:37 GMT  
		Size: 11.4 KB (11431 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:72a16720d9ddf8a7b2dc8d1b1ace588379ca56d699f1d6ade8c501aff66ba039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258525579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3db1cfb8ec57c2e1c668c37e9498d466e905042d276a2b197a07d85338ee87a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a715c260ee097512a6f8b3db5041836c3694a52db693f5778bada15c1d44f171`  
		Last Modified: Wed, 11 Jun 2025 08:45:36 GMT  
		Size: 229.8 MB (229781394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:49f73dda4259a58747e62e4eb6c4fa65628e9f66ee44bdb93ad3e1d81fb41450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bc9a1161131b8fc7f7a7ab0d7bf7c121e0abf6d42e34c83f9ba766cce41fdd`

```dockerfile
```

-	Layers:
	-	`sha256:d80007aa3456840fd8abcf804d83d4b815f907a4e06448c7f1184528cf123af0`  
		Last Modified: Wed, 11 Jun 2025 08:44:42 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84c11e33c8cd2f4d6be8f5f448f2fb501785b8e526b31e414929455af60d8693`  
		Last Modified: Wed, 11 Jun 2025 08:44:43 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:03c578ce0b32d4737deeefaef6ecea7f0ac648ee25d4fee767f79d9c03ae99f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 MB (320511994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32eb66db9a96fa393a694a8787f4a4b6e70abcd17e925bef5790c75a30306789`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 May 2025 12:43:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Thu, 15 May 2025 12:43:34 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 15 May 2025 12:43:34 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.87.0
# Thu, 15 May 2025 12:43:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:1294ecac50b0f4fe7018ad5e666e6e3c43bd85fbdc4ff68322834fcc70904e3c`  
		Last Modified: Tue, 10 Jun 2025 23:26:42 GMT  
		Size: 31.2 MB (31189682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e563e44106503f3d016cd7490b98df9b2aa3762a7e807aeb41e5f65752ff2986`  
		Last Modified: Wed, 11 Jun 2025 04:23:04 GMT  
		Size: 289.3 MB (289322312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f3928a493fc5a10fac96213e189c2986634e3b1873790ff662e908ecc4061a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d790ae2cf1ca80cca939a505b3e9cabef2ef7c0f112000bfef0e26a552016948`

```dockerfile
```

-	Layers:
	-	`sha256:2bb507ca83c8fe4625a244cd017cd4f83a5562e41548cdec226dac403b4e6795`  
		Last Modified: Wed, 11 Jun 2025 02:44:55 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7840377069666033ca9b65919363e35adad8b9fef3da1365876affb656c0d6`  
		Last Modified: Wed, 11 Jun 2025 02:44:56 GMT  
		Size: 11.3 KB (11324 bytes)  
		MIME: application/vnd.in-toto+json
