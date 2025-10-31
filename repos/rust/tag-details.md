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
-	[`rust:1.91`](#rust191)
-	[`rust:1.91-alpine`](#rust191-alpine)
-	[`rust:1.91-alpine3.20`](#rust191-alpine320)
-	[`rust:1.91-alpine3.21`](#rust191-alpine321)
-	[`rust:1.91-alpine3.22`](#rust191-alpine322)
-	[`rust:1.91-bookworm`](#rust191-bookworm)
-	[`rust:1.91-bullseye`](#rust191-bullseye)
-	[`rust:1.91-slim`](#rust191-slim)
-	[`rust:1.91-slim-bookworm`](#rust191-slim-bookworm)
-	[`rust:1.91-slim-bullseye`](#rust191-slim-bullseye)
-	[`rust:1.91-slim-trixie`](#rust191-slim-trixie)
-	[`rust:1.91-trixie`](#rust191-trixie)
-	[`rust:1.91.0`](#rust1910)
-	[`rust:1.91.0-alpine`](#rust1910-alpine)
-	[`rust:1.91.0-alpine3.20`](#rust1910-alpine320)
-	[`rust:1.91.0-alpine3.21`](#rust1910-alpine321)
-	[`rust:1.91.0-alpine3.22`](#rust1910-alpine322)
-	[`rust:1.91.0-bookworm`](#rust1910-bookworm)
-	[`rust:1.91.0-bullseye`](#rust1910-bullseye)
-	[`rust:1.91.0-slim`](#rust1910-slim)
-	[`rust:1.91.0-slim-bookworm`](#rust1910-slim-bookworm)
-	[`rust:1.91.0-slim-bullseye`](#rust1910-slim-bullseye)
-	[`rust:1.91.0-slim-trixie`](#rust1910-slim-trixie)
-	[`rust:1.91.0-trixie`](#rust1910-trixie)
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
$ docker pull rust@sha256:4cdae04e9e94e189ab2a6b462c93ed5f8ab248cde1c6100c59e958976b1c4594
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1` - linux; amd64

```console
$ docker pull rust@sha256:7ccdba2b655ebac8408566b54b8dbd02b44756759e8d73109227edb2b81b2942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589704892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd127f46648e9bce2a1ffa8096f2babd56565f986ae96fa6abef7bc6fc290ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d573bf42b377ce6a5a0451c15388849686fa4058efd68999f3b014daeb5b55`  
		Last Modified: Tue, 21 Oct 2025 01:42:47 GMT  
		Size: 25.6 MB (25615545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dfe2fac1c486e9aaf41d1028ed30be2c442aa84af44462bc7bac8c148ffb13`  
		Last Modified: Tue, 21 Oct 2025 04:47:38 GMT  
		Size: 67.8 MB (67784857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d5bd8a8d262418bf22e705535ce38c6789dc72e319d76b30aafa5c331b6924`  
		Last Modified: Tue, 21 Oct 2025 10:24:40 GMT  
		Size: 235.9 MB (235927971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68557728bac69b81da96dae42ed23a374347244afaca7210e768400aecefb4d`  
		Last Modified: Tue, 21 Oct 2025 12:18:46 GMT  
		Size: 211.1 MB (211091548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:c6e9c920b84edb3271e9884c7e7d7736fa75456c61d869517d117f8b006f02f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17223403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0af01840a4d7313dce07a4cd8705141858d215468038f488a00bc2983f4203`

```dockerfile
```

-	Layers:
	-	`sha256:4de25e75936e713c9998f626efb488832cbbc139588b1dab75dee11b9e80e7da`  
		Last Modified: Tue, 21 Oct 2025 14:44:21 GMT  
		Size: 17.2 MB (17209918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f86274d8e899d886607e02351051d3409137c5b77521eb87725d6ff4cfb078e`  
		Last Modified: Tue, 21 Oct 2025 14:44:22 GMT  
		Size: 13.5 KB (13485 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:df192b38e9142bc8d454be61de04235e6e3d6e3cc142b3ca4461565fdcdb5c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583252486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a735b8020181b775c6ff35bd4f4ddaf6fccacf90d6baef0e5b88f5fac468e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:20 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:20 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:20 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cda7f0b38d756bba039d1251605b315c32a18bef1d71d1a0a98df8f4c7fb6`  
		Last Modified: Tue, 21 Oct 2025 06:18:01 GMT  
		Size: 193.2 MB (193235864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7085e104656ea6c66d8ba95df53b71fae0ae8c42dce84c36d3dd51cc63114cc`  
		Last Modified: Thu, 30 Oct 2025 23:48:47 GMT  
		Size: 258.0 MB (257970062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:7bdc29f59dfa654c3d2300e1d752366f54275c8759cf65ee11f3b51b5ee02ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b60585f52529edd183ac79b90c91a6c5c7a9f7718df436557b6c48120de964f`

```dockerfile
```

-	Layers:
	-	`sha256:e7514cf6a08ba2c22ef71f6054b5e755385f65048788dccfe2a655928e7613af`  
		Last Modified: Thu, 30 Oct 2025 23:44:49 GMT  
		Size: 17.0 MB (16977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7716c3ffa9ab429830b3182885b3f920b00e895ca1ca6dc9aa0e0866b3405617`  
		Last Modified: Thu, 30 Oct 2025 23:44:50 GMT  
		Size: 15.5 KB (15508 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:69d4bc701fcca1d78e46d634aca8f1b0a3b967b755e87d0c3e883abf402a92c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.6 MB (548594894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124905d571200dee29c0250b5a56242cbb369d8d6a2f46770ef2060b9aa6ae19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:13 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f695ddffd81064f15ea19428e2d643e8b560e48e54ae801a8d63c45ad6ac29`  
		Last Modified: Tue, 21 Oct 2025 04:14:42 GMT  
		Size: 226.1 MB (226078014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b0009962587465f15c28cbaa4e05bede4600a6b68c86467eb69e4227df6c84`  
		Last Modified: Thu, 30 Oct 2025 23:44:37 GMT  
		Size: 180.3 MB (180266565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:a2ff1f30c17e94d0edaf28e068fd1a99b76f759cebd6a2b304606e7c085f21aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17309822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d625100634edff47e63fc8b469129a68a25115bad3e0531a1f7b594067d865`

```dockerfile
```

-	Layers:
	-	`sha256:b3eb795d70d03f35b63225b01143c51f0f8b6622f4022cb5db697d2ba9e108d7`  
		Last Modified: Thu, 30 Oct 2025 23:45:11 GMT  
		Size: 17.3 MB (17294274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f42745a111fee91795bb40aa7014469e06556069a7271890a09e381d064bfc`  
		Last Modified: Thu, 30 Oct 2025 23:45:12 GMT  
		Size: 15.5 KB (15548 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:0f36b8c5b45a1403f31ae3e1f2db1be6126a1a8d3d89157dfbf1a9caf8364a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.4 MB (625391663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5670c24f999c8b72981507cb47d2b2dcaf53d09af6a4187abbd6fe21f62d48fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:12 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e11ad5a4fd5be41f07ac93311f8ae1f7dfd6455edf9f5cf950e26d70ee4c6`  
		Last Modified: Tue, 21 Oct 2025 01:53:30 GMT  
		Size: 26.8 MB (26775679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e99453a1ea6755d1a3a58fe6632281db5820c733291dbefe645ffd8397c7e4`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 69.8 MB (69795039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4be1d74f0f5cdfd17973a37d16dc7ed75a3f628a94c99be57d59571d3a9b4`  
		Last Modified: Tue, 21 Oct 2025 04:13:56 GMT  
		Size: 240.1 MB (240053433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b95b67c6e22caf5578ea1eddb03fde4e1cedc03293a23c829f701c73cc927b`  
		Last Modified: Thu, 30 Oct 2025 23:51:31 GMT  
		Size: 238.0 MB (237966938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:de9c5a2a0cb7e4e8b0375014aeac39baef1c37299b1295b32c691537e29bbdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17193526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7797bff6bc0b961011e7f5b876cc1e1e46af5fb5bb27dddfa8a0836045fbdcf6`

```dockerfile
```

-	Layers:
	-	`sha256:4ba4d0a028ca002c9baa8b6e271bbed6f0b707811424f49afb3dbed5b7bbbc66`  
		Last Modified: Thu, 30 Oct 2025 23:45:27 GMT  
		Size: 17.2 MB (17178183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f46fff4553bf23d62e5ffce1a59bed624919c2fea3703b65b013ef50394d42`  
		Last Modified: Thu, 30 Oct 2025 23:45:28 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:a29f6e27737a6b59309a166a28c4cf97dd2eefbfa88c3aca3304faa0ff08a3e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672649528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a952fb3ef83a44fc6533607fda15f4d747a2350849923b66222c95ce97864c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dfb88672cf0a942c4fdfcadf1912c35c9d30a3a001b18a9dad505fb960ae8`  
		Last Modified: Tue, 21 Oct 2025 07:47:00 GMT  
		Size: 27.0 MB (26996207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06029381e2f1b3a0885caf1b758b0461bfaf9db7b9642ca0b79ab28ed1dd4ecc`  
		Last Modified: Tue, 21 Oct 2025 17:35:58 GMT  
		Size: 73.0 MB (73029685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac677cb325b211e7ad7714eb6d52abf13c0d7630be372cac77812dd27241a158`  
		Last Modified: Wed, 22 Oct 2025 01:27:43 GMT  
		Size: 231.1 MB (231086523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff2e4d4f9807f075e3ff5c6c28631a324397b2b771ee6555b6d8e923ee06e0b`  
		Last Modified: Wed, 22 Oct 2025 14:51:26 GMT  
		Size: 288.4 MB (288427637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:f33a0240a7d92b5fda177a193f6e7c05cb951abb7c29daf3858c351311dbac60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17209060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36284e92be8526f5f13c82a2f801a21cf15d46cdae17422ca12254be41d6339`

```dockerfile
```

-	Layers:
	-	`sha256:3d6645f5d1a853359ab88d5ea6d06cd386d73bef8d296c30d6ee843f5dbd6028`  
		Last Modified: Wed, 22 Oct 2025 14:45:21 GMT  
		Size: 17.2 MB (17195507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0297a39c3c72137eb2edc4ce4ff2993062b460caa31ef206b40f28e10b1fe71`  
		Last Modified: Wed, 22 Oct 2025 14:45:22 GMT  
		Size: 13.6 KB (13553 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; riscv64

```console
$ docker pull rust@sha256:db568b830f6fd90592497dd0eda8001ed384c555723f1082ceb67a49b9968c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.7 MB (731746485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dde95f55f8cca95c0c52acf2dc0afce27141a1ec0354bce98292db2d8245a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:41:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:41:49 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c640441904d97046ee4a137483e3b6745e0a18782c3b688fede8e9ddf18261f`  
		Last Modified: Wed, 22 Oct 2025 18:09:29 GMT  
		Size: 25.0 MB (24953874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb6fec5cd2588ba9a09a9491547b6e7005f3640a81c530cc1f2e651257c901`  
		Last Modified: Fri, 24 Oct 2025 21:34:03 GMT  
		Size: 66.7 MB (66662364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c02978248d2c72ee734dd5ab68325ab5be1edbbfe6026472d198390eabe8cf`  
		Last Modified: Sun, 26 Oct 2025 13:26:52 GMT  
		Size: 322.8 MB (322829684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af21d31669ce50f730bd664ae7d97ab0697a48fc4c1fc527c93c32c6f717c3f3`  
		Last Modified: Thu, 30 Oct 2025 21:56:54 GMT  
		Size: 269.5 MB (269530257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:5d2476fa78b8cae7f942b74725782b510c4b6a2f687346c648591dd4613b5b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17281556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c73611675d5101a89fa89d59b3a33599e9498dfc407639e4c3b51d2879ed92d`

```dockerfile
```

-	Layers:
	-	`sha256:de5eee62216cb8618afba94f9d4c277f9a550568818b3cbe17aa78900016e6f7`  
		Last Modified: Thu, 30 Oct 2025 23:45:56 GMT  
		Size: 17.3 MB (17266092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c38e4c4e014047f4332c3cf3bf8372bf0ff126eadb475671eb5f6759bb6503e9`  
		Last Modified: Thu, 30 Oct 2025 23:45:57 GMT  
		Size: 15.5 KB (15464 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:58124806371c4a39a5ac92593a6f823c354d5d002cae39305db81a0b200dc7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.1 MB (648135109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571bb1f5470229ff143899581ee0538e785fbd8bb45168569fa265be37201747`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 22:48:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:48:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:48:48 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9f518343ed4506c34ae7900f538c56bac66f4fad9740034ee8b819bd8d15e`  
		Last Modified: Tue, 21 Oct 2025 12:43:19 GMT  
		Size: 26.8 MB (26783314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb7d34d2ff189fa2150ed8d82914c7669f312817531bbe187965e9d30825d3`  
		Last Modified: Tue, 21 Oct 2025 23:25:03 GMT  
		Size: 68.6 MB (68630635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4131ad2e1cf6d0e51274c6e30ebc34015c8e72c5b79a0146220944b33c750ff`  
		Last Modified: Wed, 22 Oct 2025 12:46:56 GMT  
		Size: 206.5 MB (206460184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2905cafaed65f05704ab3b4e23479ae861bb4a148a0aac8b459931962ccf1469`  
		Last Modified: Thu, 30 Oct 2025 22:52:24 GMT  
		Size: 296.9 MB (296909277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:54a2179f33db9cea350dd680ac4622e0df5e333f36232801102916c3b7ff749b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17002545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c6960bfd3415ad92fd83afb42906df93f6f114175be156af8cd8f842cfa20c`

```dockerfile
```

-	Layers:
	-	`sha256:24c7152c5b9ea076d3348e04b2479b166ba9b19eff01141c458fb04c53fdcdd6`  
		Last Modified: Thu, 30 Oct 2025 23:46:10 GMT  
		Size: 17.0 MB (16987149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc6358b456c6334b83aedd51c445eeedb3650635525e2e50790b42a8d5968cd`  
		Last Modified: Thu, 30 Oct 2025 23:46:11 GMT  
		Size: 15.4 KB (15396 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:29beb3c7b3b1f8c6e2e5b9e7e6c79a38a7e8a8102d92f50f98951feae046a999
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:ee9b9f2ebd8741e4ecf1ade08918e492d642c4e625be481bb7b7954b89e9d504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328784700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffa4185585206d4d98e871b83bebc561866519a6dba20de63e3192e6804528c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b94f1896c7d7197d473e46aa720688e4b64cabd8c559482b9ad62f5d1c54ea`  
		Last Modified: Wed, 08 Oct 2025 23:46:44 GMT  
		Size: 61.6 MB (61604379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fe284ea8abe7a0d30bbfc5a349ac250b13a8a3d1760d8ee638d1c27fbf60b9`  
		Last Modified: Wed, 08 Oct 2025 23:48:01 GMT  
		Size: 263.4 MB (263377869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b05da53540ad6b64b76c78df048088711a426b503ce3d7581f4359156aacb4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.0 KB (794968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81b251f281fcb5a2b4f9301b279ee799dbd08e11092d95582b55c6da2b21b4b`

```dockerfile
```

-	Layers:
	-	`sha256:703eec4d4cc485186fb35c31aed213134f9ac25b9ea2420f1fed91ec0b037f1d`  
		Last Modified: Wed, 08 Oct 2025 23:44:42 GMT  
		Size: 782.7 KB (782673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40831b0dc30117747a9bf98ef753d0b9c681127cd96f9f85d11abebfa5eb8934`  
		Last Modified: Wed, 08 Oct 2025 23:44:43 GMT  
		Size: 12.3 KB (12295 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d8a0b1798b6837e717df2a58ce2f5653c3cf064617ef1345c7fa2e9d83f35044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338571527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c334672aeafb6097099971d43eda27635fb349cd96669fe6b776259c094c0621`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:06 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:06 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:21 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3cfaef0615cb0253cafffaabf7ec4ecc5175443b4ab6064f2e6ee284a050c1`  
		Last Modified: Thu, 30 Oct 2025 21:36:13 GMT  
		Size: 59.1 MB (59143801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9674b249fc5ce80c99c4602fb01c94be64a649a3024dac74778ee94d7db0705`  
		Last Modified: Thu, 30 Oct 2025 22:50:59 GMT  
		Size: 275.3 MB (275289657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:ae5caee0dbfd83810c65df11e27dabf9dcff493e569bade06d6c3cf6dfbe8db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.7 KB (875736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c20db5b6d61ba982bc0de623cef8139d3cca9749848be2c546175c599723f`

```dockerfile
```

-	Layers:
	-	`sha256:240bdbfb8f97567899690facfafee478aa0eea76bee43834ce0e312b2abe7c6e`  
		Last Modified: Thu, 30 Oct 2025 23:44:39 GMT  
		Size: 862.3 KB (862259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f33d22a8ba00cd9de8a1cef55af65f0faaeac769c82fb9d7ff25993b539c3e`  
		Last Modified: Thu, 30 Oct 2025 23:44:40 GMT  
		Size: 13.5 KB (13477 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; ppc64le

```console
$ docker pull rust@sha256:9036b3b6866c1835ae0647bf6e39ed634c24250cbe5ce9323476525325207c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350263091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1c326a8fb61738f78b6e832d76856f610184e585f0bea48eeb0b05acc9a561`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a56909a4c35c502dd43802ef31d4890df3cd54f15133b9f35dcaab1ec3f3219`  
		Last Modified: Thu, 09 Oct 2025 05:14:10 GMT  
		Size: 59.0 MB (59006725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20f6c21afdba425061e0ba687974793c99c42b22eafef8cce1227eb48c95ad`  
		Last Modified: Thu, 09 Oct 2025 08:45:22 GMT  
		Size: 287.5 MB (287524125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:fd67dce82d8a2b47d722b477a74576185f4a69052847396ccba385aec9c0cc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **807.6 KB (807608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c44369fd4d6569b24f091dde0bde6f511b3ece2eeadb14bc5830c655a4e4bf5`

```dockerfile
```

-	Layers:
	-	`sha256:ed8dccf24b40112f8c8bfb29e2beac0c23ea4a599fc28af8dd896d2a067e715e`  
		Last Modified: Thu, 09 Oct 2025 08:44:26 GMT  
		Size: 795.2 KB (795241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417fb1d78b372874952b95cf42ae7f491a90983707634ae9103ede8f18d7de58`  
		Last Modified: Thu, 09 Oct 2025 08:44:27 GMT  
		Size: 12.4 KB (12367 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:657189ee5207a86316e5946bcfddd4f5ba765f8163768a4e27d97c88a10cca80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:a97b713ba0b992d4855de682705a1671a9f1bdbf56c63106e3b450732ffd31ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322314091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f5a88bc4032951a2b68c4d0695f33ba0c4d4313454952d17e7a3a403713a51`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a081b9ffe7512b030d0920eb506f7c1bdbd5353c51f1960af8fc4d16a313033`  
		Last Modified: Wed, 08 Oct 2025 23:48:38 GMT  
		Size: 55.3 MB (55309661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483b1a71ca7cafce114e0d2124a2448acddbf1e3eda67dfb387c28d92d6b498c`  
		Last Modified: Wed, 08 Oct 2025 23:49:06 GMT  
		Size: 263.4 MB (263377374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:24e8dd54d6ad7a7e7dbecca0c8c9e83421a68648c336216f8217e666a50ca241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.0 KB (720952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d368e2e22b7effe99b5a2bc6ccace24606c18a48fa7fb0382074f287232c805e`

```dockerfile
```

-	Layers:
	-	`sha256:f7637da0d7c6704319b9717d659cab4afc248751241fd31c1faae5ecfebbb85f`  
		Last Modified: Wed, 08 Oct 2025 23:44:30 GMT  
		Size: 709.9 KB (709860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686c296cfedd0c7ba040e33922df421ff0eb8f7e42fc4d42dbd32143f0338fd0`  
		Last Modified: Wed, 08 Oct 2025 23:44:30 GMT  
		Size: 11.1 KB (11092 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2b1f24765d5621e41b309cbcf190fad00badbcd79cddcfbcc6e9afb4e74859e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332323361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2be9399e5a5e1241a21bc9d4b6a3fb9a91eda423ff9f867729f1c7d4dd1494`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:32 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:32 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:48 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4701d29124b0199e51ffb3475f695f3b57083f5755bdca3b30b7fb7e41ace7ab`  
		Last Modified: Thu, 30 Oct 2025 21:36:44 GMT  
		Size: 52.9 MB (52945684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7e5474d3d895c6f5799dd4f3bbbdcfa776a9e50f408ba69a4717a2899eb367`  
		Last Modified: Thu, 30 Oct 2025 21:36:29 GMT  
		Size: 275.3 MB (275288300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:2b3d670ab5944d9837c64cdbfd523b88a99f9a56456dd23f8118f9363cc14688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.0 KB (758017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f15731caffee3bf6608f446feff1ee659f031fd1cd8f5b09435eb35688932a2`

```dockerfile
```

-	Layers:
	-	`sha256:6912c322cae1e576478d01096232f97779aa51160ce3cfe9cfaec428fcf894a3`  
		Last Modified: Thu, 30 Oct 2025 23:46:04 GMT  
		Size: 745.8 KB (745792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e187fd7b741e285cb843267475b89466d15f6b182c4390c712e27e84fcf08123`  
		Last Modified: Thu, 30 Oct 2025 23:46:06 GMT  
		Size: 12.2 KB (12225 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; ppc64le

```console
$ docker pull rust@sha256:323e9bb9f5bdb3e1b11a122014bc05492bc31fc24ad050be8e38a6774662b1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345167925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01759e6bacb31eac791d7252f80007f9302f67878ee1a72bbde55ad9e4a211ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.20.8-ppc64le.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a78577222d4c08b54b062e8bf30834a3c610281d9b4780d34cac9394431f7f25`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 3.6 MB (3575563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3d4fef061972b5a536d5dc27c6e2ec1a6af1868c7a8ed73649e96ef403cc78`  
		Last Modified: Thu, 09 Oct 2025 11:00:09 GMT  
		Size: 54.1 MB (54069626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959cfe92ddb8a18926e7717589b1acaf295e33b15ca60e9c9e7e65a7567b6de`  
		Last Modified: Thu, 09 Oct 2025 11:01:15 GMT  
		Size: 287.5 MB (287522736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:abdc08db7e1da362ae2750b3c87e0e0bf162b47b03ba70929616e05f4660490d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **714.9 KB (714867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d3a994f7137a606e5fc3bb60732e62b3e11339944cb30264794ee2aff7d0e`

```dockerfile
```

-	Layers:
	-	`sha256:299f111c291c6146617598d78e4abf1162dd1e235a847eeaad20bfeef341b474`  
		Last Modified: Thu, 09 Oct 2025 08:44:30 GMT  
		Size: 703.7 KB (703728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf82392610784b6dc5a5fc46d0db40e68de482571e5808a27a534fc99f1b32d`  
		Last Modified: Thu, 09 Oct 2025 08:44:31 GMT  
		Size: 11.1 KB (11139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.21`

```console
$ docker pull rust@sha256:fa5f395f8f6fd74863960299c24fa0e1eecf7587acbd8abf308a120f505f410d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:ae572f2a6f7d6790ad87264078d4268b6b8618fe1741e61351938474b3981b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328583689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b473418392e0e4e8bec14410ddb1c78d704e4dda726ae28c63d72ae8d39d461f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129b51f390fdd40aaf39ff5cb8eae55f7068b85b99e151bd9be23bcc2a776817`  
		Last Modified: Wed, 08 Oct 2025 23:20:40 GMT  
		Size: 61.6 MB (61563786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741a12271e539b62a08b9044001f072cbc32a6fba77e5f9c606417557d0a1da8`  
		Last Modified: Wed, 08 Oct 2025 23:45:17 GMT  
		Size: 263.4 MB (263377334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:7cf01932cc651a307073160fdf88a0afd7e41ff56bebf14c0f4636a8a3390341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **791.8 KB (791783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1513a03317b2d74a7ef63f021d267865d8903e96ac1bd5f732609a72d165690c`

```dockerfile
```

-	Layers:
	-	`sha256:4d06a9911725da4e0a3dca9033e9b573ffd8ec46f3405912a4c481eb4d4060da`  
		Last Modified: Wed, 08 Oct 2025 23:44:36 GMT  
		Size: 780.7 KB (780690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43b6dce726eed8669c3b712d102c9c2206f16dc85add3d7e8aa6d8f8bc9ef41d`  
		Last Modified: Wed, 08 Oct 2025 23:44:37 GMT  
		Size: 11.1 KB (11093 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a8d313620e805ad10815a56881e538d77f2691f105866bf1c3d06a763c821ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338380943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917e8113aca6a443a4a106b586c655c769fa81ffae061acf9520322b8ca153f7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:33 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:33 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:33 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:48 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108b0b7e1f75a2459f5f726e6189c5c2d3641caf14b00d2ca791da1bf9326c47`  
		Last Modified: Thu, 30 Oct 2025 21:36:41 GMT  
		Size: 59.1 MB (59098892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360f393f0b81dc80a22d0dedab45fc6b4fda056ff253f63643f56d81e2db340d`  
		Last Modified: Thu, 30 Oct 2025 21:36:29 GMT  
		Size: 275.3 MB (275289698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:f0d8e262a56e25c2157fb337c3d8b20dc1db76f484d732577849cca7c8888fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.5 KB (872454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b3ad2c369a7b6bd488f24704a97ec90f0a3318cb7bb60340efe6720f17797e`

```dockerfile
```

-	Layers:
	-	`sha256:4d344bf8bbc4d9656f3eefb11ac3675e925a0a32b5c22728bd7ebc3473c5dc83`  
		Last Modified: Thu, 30 Oct 2025 23:44:48 GMT  
		Size: 860.2 KB (860228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05b732c240fc68ebdbe4f1cdb77483fdc405ee55243fdc8dac13b63d314636a3`  
		Last Modified: Thu, 30 Oct 2025 23:44:49 GMT  
		Size: 12.2 KB (12226 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.21` - linux; ppc64le

```console
$ docker pull rust@sha256:f4dd90421dec60a7fb1accd10539fa73f7ee02a5f7a2626ee7a1e0d7358ade8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350063686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628dcf3397d10c30cfe3a2da197cbc7802d9013f083afaf5724ba0f884fcff00`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602f64aa625bdbad2f881a453963786cb9d664579705975b5c2752ce620d76f2`  
		Last Modified: Thu, 09 Oct 2025 05:12:09 GMT  
		Size: 59.0 MB (58965844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d12187cc736d95350ac1b48c8022932d8f49cc52cbb21f4f21301a7f609105c`  
		Last Modified: Thu, 09 Oct 2025 06:12:28 GMT  
		Size: 287.5 MB (287523767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:75a3a8807264a9e00056be7f21a4d445e55d62566993b3f1a421d2e96e22e14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **804.4 KB (804373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5d3ae9c51942ce90d391458c8f1986586930cf8ce915f3c4cb0946360a6359`

```dockerfile
```

-	Layers:
	-	`sha256:1249f653cab516099082a6ed253d0534f56a8f1e528d0baa470435062437e22f`  
		Last Modified: Thu, 09 Oct 2025 08:44:35 GMT  
		Size: 793.2 KB (793234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb6899ed56649363cee6901aacd976f0b84c33f626067370cf29f452a487ff5`  
		Last Modified: Thu, 09 Oct 2025 08:44:35 GMT  
		Size: 11.1 KB (11139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.22`

```console
$ docker pull rust@sha256:29beb3c7b3b1f8c6e2e5b9e7e6c79a38a7e8a8102d92f50f98951feae046a999
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-alpine3.22` - linux; amd64

```console
$ docker pull rust@sha256:ee9b9f2ebd8741e4ecf1ade08918e492d642c4e625be481bb7b7954b89e9d504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328784700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffa4185585206d4d98e871b83bebc561866519a6dba20de63e3192e6804528c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b94f1896c7d7197d473e46aa720688e4b64cabd8c559482b9ad62f5d1c54ea`  
		Last Modified: Wed, 08 Oct 2025 23:46:44 GMT  
		Size: 61.6 MB (61604379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fe284ea8abe7a0d30bbfc5a349ac250b13a8a3d1760d8ee638d1c27fbf60b9`  
		Last Modified: Wed, 08 Oct 2025 23:48:01 GMT  
		Size: 263.4 MB (263377869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:b05da53540ad6b64b76c78df048088711a426b503ce3d7581f4359156aacb4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.0 KB (794968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81b251f281fcb5a2b4f9301b279ee799dbd08e11092d95582b55c6da2b21b4b`

```dockerfile
```

-	Layers:
	-	`sha256:703eec4d4cc485186fb35c31aed213134f9ac25b9ea2420f1fed91ec0b037f1d`  
		Last Modified: Wed, 08 Oct 2025 23:44:42 GMT  
		Size: 782.7 KB (782673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40831b0dc30117747a9bf98ef753d0b9c681127cd96f9f85d11abebfa5eb8934`  
		Last Modified: Wed, 08 Oct 2025 23:44:43 GMT  
		Size: 12.3 KB (12295 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d8a0b1798b6837e717df2a58ce2f5653c3cf064617ef1345c7fa2e9d83f35044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338571527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c334672aeafb6097099971d43eda27635fb349cd96669fe6b776259c094c0621`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:06 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:06 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:21 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3cfaef0615cb0253cafffaabf7ec4ecc5175443b4ab6064f2e6ee284a050c1`  
		Last Modified: Thu, 30 Oct 2025 21:36:13 GMT  
		Size: 59.1 MB (59143801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9674b249fc5ce80c99c4602fb01c94be64a649a3024dac74778ee94d7db0705`  
		Last Modified: Thu, 30 Oct 2025 22:50:59 GMT  
		Size: 275.3 MB (275289657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:ae5caee0dbfd83810c65df11e27dabf9dcff493e569bade06d6c3cf6dfbe8db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.7 KB (875736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c20db5b6d61ba982bc0de623cef8139d3cca9749848be2c546175c599723f`

```dockerfile
```

-	Layers:
	-	`sha256:240bdbfb8f97567899690facfafee478aa0eea76bee43834ce0e312b2abe7c6e`  
		Last Modified: Thu, 30 Oct 2025 23:44:39 GMT  
		Size: 862.3 KB (862259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f33d22a8ba00cd9de8a1cef55af65f0faaeac769c82fb9d7ff25993b539c3e`  
		Last Modified: Thu, 30 Oct 2025 23:44:40 GMT  
		Size: 13.5 KB (13477 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.22` - linux; ppc64le

```console
$ docker pull rust@sha256:9036b3b6866c1835ae0647bf6e39ed634c24250cbe5ce9323476525325207c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350263091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1c326a8fb61738f78b6e832d76856f610184e585f0bea48eeb0b05acc9a561`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a56909a4c35c502dd43802ef31d4890df3cd54f15133b9f35dcaab1ec3f3219`  
		Last Modified: Thu, 09 Oct 2025 05:14:10 GMT  
		Size: 59.0 MB (59006725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20f6c21afdba425061e0ba687974793c99c42b22eafef8cce1227eb48c95ad`  
		Last Modified: Thu, 09 Oct 2025 08:45:22 GMT  
		Size: 287.5 MB (287524125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:fd67dce82d8a2b47d722b477a74576185f4a69052847396ccba385aec9c0cc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **807.6 KB (807608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c44369fd4d6569b24f091dde0bde6f511b3ece2eeadb14bc5830c655a4e4bf5`

```dockerfile
```

-	Layers:
	-	`sha256:ed8dccf24b40112f8c8bfb29e2beac0c23ea4a599fc28af8dd896d2a067e715e`  
		Last Modified: Thu, 09 Oct 2025 08:44:26 GMT  
		Size: 795.2 KB (795241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417fb1d78b372874952b95cf42ae7f491a90983707634ae9103ede8f18d7de58`  
		Last Modified: Thu, 09 Oct 2025 08:44:27 GMT  
		Size: 12.4 KB (12367 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:863fbd5895cd638392b24e0197f02f94e3f2ad3d8bd41f97377a595324d1032b
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
$ docker pull rust@sha256:3f6e6f8d8725a65a2db964bb828850f888d430c68784d661f753144e5d787207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.4 MB (559447275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc39c88add68c6e4ed377beccd6a659e59b286954d2c7e5c8e5b1dde2a82a8e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279d33abc52c7384e0cbbb666ea22064ea29b50a968ec29ae3ad817f62e16e7`  
		Last Modified: Tue, 21 Oct 2025 04:46:37 GMT  
		Size: 24.0 MB (24028898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa5a418829f3daa90a80438cd84706b5f7fa0c795eb7936874864ef1ab7b0c`  
		Last Modified: Tue, 21 Oct 2025 04:47:27 GMT  
		Size: 64.4 MB (64396405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3556d62e9bd977c17e315ad64979017739fd90fc5a2a89ec07cf82348133f3`  
		Last Modified: Tue, 21 Oct 2025 10:21:00 GMT  
		Size: 211.4 MB (211449932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cabf358425b152d1908f63c0d4471be829cdbdb7e870867b6ff0d00609ccbb`  
		Last Modified: Tue, 21 Oct 2025 12:22:16 GMT  
		Size: 211.1 MB (211091477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b752e3300679d23dbcf05365edca183b090eb1f9ce4dbf386a63ff33fee8b581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15880926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2835758bbb69db26b153b201c88297c845154b61da6c1e3cfb620ab6a7ee50e9`

```dockerfile
```

-	Layers:
	-	`sha256:4abe2dd3e5b0b21ed2011090e044227e18c07d5b7203b58f5721012b36baffc6`  
		Last Modified: Tue, 21 Oct 2025 14:44:29 GMT  
		Size: 15.9 MB (15868950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:447779a4f4a311c28359e75fde4de4d5a8c5e594ad701431360f62b2299162bc`  
		Last Modified: Tue, 21 Oct 2025 14:44:30 GMT  
		Size: 12.0 KB (11976 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:051b0136c8a4e3e112b39e508921112fbde875a02b07b38c87a737e1e81cc746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.1 MB (559108573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be8e386e015e2bb88eaa00172139beb421d17d3570f6121a8fb2dbe27f2e20b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:35:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:42 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178651637d26f6ae6fc6c2a3297b37f8bbef12e80d822930b05b14f51a262382`  
		Last Modified: Tue, 21 Oct 2025 02:43:48 GMT  
		Size: 21.9 MB (21934505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14411cad8875b2a42f951ec95179ed8a844d1522990ec8b96f1c4d269ce3c71f`  
		Last Modified: Tue, 21 Oct 2025 04:11:04 GMT  
		Size: 59.7 MB (59652688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934fb9fcc0f174aa356a518c85a7e2e8a62dd5902afe2a8dbbf58f5f8b37166b`  
		Last Modified: Tue, 21 Oct 2025 06:17:29 GMT  
		Size: 175.4 MB (175355007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a2122d86f314de64147fdae6b5b37d7b95098ae45f73107f366595e6097bc`  
		Last Modified: Thu, 30 Oct 2025 21:36:31 GMT  
		Size: 258.0 MB (257970463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:29db2457c6db102e7a390b4609d14f799d0b4dc98f04e20b278bee9349696010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15685187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840c6decc4d442f284b6c01b397281e4a69f76e76b12d384284a4eb807702448`

```dockerfile
```

-	Layers:
	-	`sha256:8db0f390e801710744db2d01b0058a149ac8d4833025dd5538c43e761de709dd`  
		Last Modified: Thu, 30 Oct 2025 23:45:19 GMT  
		Size: 15.7 MB (15671436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd29c41b660a030fe351fe27c96ba66c2b369e2fa4d46468e264be654f4fc10a`  
		Last Modified: Thu, 30 Oct 2025 23:45:20 GMT  
		Size: 13.8 KB (13751 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b5ea992358738c5ac3d06cafcd8f8274a36b77738ff7c8ac37828322399a6c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.6 MB (519553946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4518efce2e74532fa1aab649f80dd367117838d24a5a2c3caeba50ab3d523197`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:56 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:56 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15270faa4e93fc4bcc62caecce8d2f5dfc1443d3c99572dfb689973b24c0a4`  
		Last Modified: Tue, 21 Oct 2025 02:35:23 GMT  
		Size: 64.4 MB (64370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6803b5e31b40492f4747e974e6e4ae692982b12beb2b87ed9d9ffbdaedefcfd4`  
		Last Modified: Tue, 21 Oct 2025 04:13:43 GMT  
		Size: 203.0 MB (202958684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3099636657b1560c5cdee62a47498eec65574f75745e2e59dbe17331d4c6cedd`  
		Last Modified: Thu, 30 Oct 2025 23:48:57 GMT  
		Size: 180.3 MB (180267344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:eb1282379cca9bd583c19b02bb212db62b40aedd81ce17ed2fb038637a279a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15911254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee670b912d558498da8a680449137c57f480fd39afb5dcb916fa1b657838370a`

```dockerfile
```

-	Layers:
	-	`sha256:310f60a24c03dd47886646e436808491680a7092f501e1625c0b0137803aca44`  
		Last Modified: Thu, 30 Oct 2025 23:45:35 GMT  
		Size: 15.9 MB (15897478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f59b3162dc6c5eae0e6dc9c486d6af675e4ee71d672067d47e274f3c0c9d0fd`  
		Last Modified: Thu, 30 Oct 2025 23:45:36 GMT  
		Size: 13.8 KB (13776 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:3df2b6dd56af4590d062038eb7ea187a744fdaf081514e183042ff7d02854301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.9 MB (588911073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e8ebf3e452e9009e6ac8977f62eeb4677af9d14fe10adff5b5a5229350c519`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3426ba65368da59a25d050cab9d7713d7873264014ab6dfaa6b0c33f0632cb80`  
		Last Modified: Tue, 21 Oct 2025 00:20:21 GMT  
		Size: 49.5 MB (49466720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f14d3e3fda83046fcd165bb976221020273830b54d963f634e53e7796b47053`  
		Last Modified: Tue, 21 Oct 2025 01:52:59 GMT  
		Size: 24.9 MB (24864208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39058bc352da86cee9643b9b447133a3295983ec455cdba2fac6cbbed8726db6`  
		Last Modified: Tue, 21 Oct 2025 02:35:47 GMT  
		Size: 66.2 MB (66231902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed15f8c1488a55d242a6bf3226b75c0d0de56631f3ea18bb327cec39013003bd`  
		Last Modified: Tue, 21 Oct 2025 04:13:40 GMT  
		Size: 210.4 MB (210381245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284a00e05bc16cf43c2f874e7ffa10dfd7a2b9db4a6677907e35dd79fe9a958`  
		Last Modified: Thu, 30 Oct 2025 21:36:44 GMT  
		Size: 238.0 MB (237966998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0599233bf7ca1dbdaf9211ea1d633238a82678ba0c72f9df870614f4db971837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15859504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ad9e5af8c0e73f8cbf71baff9a986c09dce838cd776e52aef2bf3deb361ccd`

```dockerfile
```

-	Layers:
	-	`sha256:4507749c6cb049d9b9929284ce90ffcbb7ec4eb94fb4c9c0262e135f7fc1071f`  
		Last Modified: Thu, 30 Oct 2025 23:45:50 GMT  
		Size: 15.8 MB (15845864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e4d18122dd7bb11ec0aa43861a1fc3f5cff14e9b8487a97a8493193a79c5282`  
		Last Modified: Thu, 30 Oct 2025 23:45:51 GMT  
		Size: 13.6 KB (13640 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:9eba237a8a91d4d4b3daa3f9b16925ee32acaae05e9f4140bbe52f0f306291e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.8 MB (650761894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90a0390e5c3f2327709ea58c4600fdaea64e7b2d73feebbf945b0c74868610e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:297b234228c60cb6a9bc0156bdf582119f3c4f22112d7d2e8128e4d1403158cb`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 52.3 MB (52326787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665a6d4e6976a738d68a77f188daf2501160c6ad54e4788282d2395e926b5e6`  
		Last Modified: Tue, 21 Oct 2025 07:42:57 GMT  
		Size: 25.7 MB (25672119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9014e4879ede8e5983b7a1a0f265054143b5d897d5a848c01fe4c938fdaa27`  
		Last Modified: Tue, 21 Oct 2025 17:30:59 GMT  
		Size: 69.8 MB (69845634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56011ccaf4727bb2311ac874db524178647f03b759d374824a9593362ec2964a`  
		Last Modified: Wed, 22 Oct 2025 01:54:45 GMT  
		Size: 214.5 MB (214489889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39aaba2f0db3400914a4e2127ac5540b1f081213e989e48c3c3237d2f8b665c`  
		Last Modified: Wed, 22 Oct 2025 16:06:12 GMT  
		Size: 288.4 MB (288427465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bb4c74d769d3c2fc4ef7eda580d7fa1c9938cbfd1c2b38121b8091a1ffbaaebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15857497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1969e92357e8b86e012df9d155afd7d29441fccef237fc92372a75b1627b2016`

```dockerfile
```

-	Layers:
	-	`sha256:4b4b17fa7f4c21642766fab5286c683a962e3ba61375736c767f61a550a06434`  
		Last Modified: Wed, 22 Oct 2025 14:45:19 GMT  
		Size: 15.8 MB (15845477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08c81e19f8fe22fd88d08411312c59342f9439abe4bcce945bdb4fde2da63d3`  
		Last Modified: Wed, 22 Oct 2025 14:45:20 GMT  
		Size: 12.0 KB (12020 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:697ff40e2e322426b97c54857174bef11b523a775040bd451466892908de2bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.1 MB (615060656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4faa2b9c9fb04ed6c7fb91522e3b4ad2232170657cc84637e5cca4b424cfd02a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 22:39:51 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:39:51 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:39:51 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca271e8b0e27269a77c65ea555986eaaadf5db02b1ac24f66f8ce2e45a475b`  
		Last Modified: Tue, 21 Oct 2025 22:50:23 GMT  
		Size: 24.0 MB (24027291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944e6bdda425b877e973cde5b6c8eeabf7eed45bfaba0fd705b4f180a07f001f`  
		Last Modified: Wed, 22 Oct 2025 06:00:23 GMT  
		Size: 63.5 MB (63501423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7d40c47b93ce5dc5166e5aa44baae913a478ae1ba5f7865fe24556acef9200`  
		Last Modified: Wed, 22 Oct 2025 14:21:48 GMT  
		Size: 183.5 MB (183485270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1617ee534ab322072d5a49e5b16309a0c49cf8b0232baabd7f545d5675371d`  
		Last Modified: Thu, 30 Oct 2025 22:43:17 GMT  
		Size: 296.9 MB (296909151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:478d1ea453072bde935424c02d4c412b2552cb3b6f3802e364b9daa69bb78b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15690219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9dc7449fb5d0d433daa7aa7b48a617e07616fd804e869aa43d91049e329468`

```dockerfile
```

-	Layers:
	-	`sha256:e5617194576bbf4d19500cc175ba3bdd7dc056a09db6529ed35a8a3df0ebac65`  
		Last Modified: Thu, 30 Oct 2025 23:46:22 GMT  
		Size: 15.7 MB (15676546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f013fc0c2ae0f7a32936873b795b686a9fe5f9867e41c993b818dbda395aa7cc`  
		Last Modified: Thu, 30 Oct 2025 23:46:23 GMT  
		Size: 13.7 KB (13673 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:e0c87d49c7c5eab3d5493afa6ed718ab3dfc68fff1b046553eebd69bb712f21e
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
$ docker pull rust@sha256:ba3a8b9eb24de14c1879efe8acff7d4eb747723ca957e0d2409d0bc2ea9f84a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.6 MB (532573818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90deb942227e65f117f7086b8b8e0d4b8aabd132e494b2f6da8dae5a8aea8660`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b6f830cd306f01980373f1e0120f2d00018fbe51a9506b7262f5d9e4bbda74f9`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 53.8 MB (53756115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfa9ab09db8d94503213f634b29be3505174979f2e0c6e3fd46c2acc0716c25`  
		Last Modified: Tue, 21 Oct 2025 04:46:42 GMT  
		Size: 15.8 MB (15764056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e663cb3204c49ebc21b005f5976ee62e4f00b632aaa8000dbe6db86d9cde2a1`  
		Last Modified: Tue, 21 Oct 2025 04:47:30 GMT  
		Size: 54.8 MB (54755162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bafbf91825be17f2ceae6674de95a31e6f8a5a24c7cb95ae123d19de9c63e61`  
		Last Modified: Tue, 21 Oct 2025 10:22:52 GMT  
		Size: 197.2 MB (197204867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2934a4a54c0280356719b64463655074b644e9cce9b90e0856432515bc70324c`  
		Last Modified: Tue, 21 Oct 2025 12:34:54 GMT  
		Size: 211.1 MB (211093618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ada36de672c97de12b518347973806e954a9857e39a4a99a4a78ca6e6ea4fa6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15475300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6b018c655fb9ea7fb0efcc34ce311abbe59313ea016dfea5cc4330f70bfb1a`

```dockerfile
```

-	Layers:
	-	`sha256:0ffcb85ba366a629649a13c3dd79c68a97772f673c73b252ca6e6f8f611b7453`  
		Last Modified: Tue, 21 Oct 2025 14:44:36 GMT  
		Size: 15.5 MB (15464051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772732437b28b188679156785245b01fe3aa24403d84d740b9257f330059f3d1`  
		Last Modified: Tue, 21 Oct 2025 14:44:36 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:4debe238b6bccd468958311c5ee086154be57fe1f47fb1e17e9a3357f90139be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.5 MB (540499385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a512f11edcf77ed82a2ac07b66308eaf931cc80877cb617b60b8f763011be2f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:35:30 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:30 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:30 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:680ed921e0c94a719af1d242eac2d0c1be8482153680a3940f3435ee5598303a`  
		Last Modified: Tue, 21 Oct 2025 00:20:24 GMT  
		Size: 49.0 MB (49046121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c68013a317d7d802bb25c57a724c8753caec2fc7f0e78fc13f9a38fd22ecd4`  
		Last Modified: Tue, 21 Oct 2025 02:44:25 GMT  
		Size: 14.9 MB (14879264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895fddf2807e047e5b02e5418fd04d343d3e9b5b393b2f3f0cd6704cad44b8f0`  
		Last Modified: Tue, 21 Oct 2025 04:10:49 GMT  
		Size: 50.6 MB (50628495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ef331acdad14a3d1bfe859a1c645cb9f4b9526e16e3fed550eee6b86681db7`  
		Last Modified: Tue, 21 Oct 2025 06:17:35 GMT  
		Size: 168.0 MB (167976463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2345c283f9f7c727f33c6a1e2c5ffa229106bb1e7b3f3f2073146f627866f815`  
		Last Modified: Thu, 30 Oct 2025 21:36:20 GMT  
		Size: 258.0 MB (257969042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f6a16886d335243aaaf88af9f27e0a70520e083485569ce2cca1c2bdd490b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15275978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f206f730d7eeec8a3b422fc88a2602f2e8f4d5d0542c706027b0a2fe2928a2b1`

```dockerfile
```

-	Layers:
	-	`sha256:69bab675147da3f449e5f163a075b2d55e9aa4ed4021b6e356a242df2ef4a59a`  
		Last Modified: Thu, 30 Oct 2025 23:45:27 GMT  
		Size: 15.3 MB (15263395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac6fc96e9abd4822cf5b32fc13e672b114ae72330f34d3a5301f3009e139e4b0`  
		Last Modified: Thu, 30 Oct 2025 23:45:29 GMT  
		Size: 12.6 KB (12583 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bdd72efd5f91a90aa1746b27a7cd1cc1ea77ae0606dc1e0bb9ea3fb1c4adb42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.2 MB (493232128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a548930c92a6745dcce895941534ec91e5af27593c0ae426e760e382ee6bcf7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:39 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a72c4e347b74aa6a0086cf3d1d928528ab02577a17bff4e22366a7df681f564`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 52.3 MB (52257444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f7bdca064e682157394f36dabd112bc9831aff9743216b035e2ccccf704cc3`  
		Last Modified: Tue, 21 Oct 2025 01:46:24 GMT  
		Size: 15.7 MB (15749510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc7a49f7691cb1ac5f0f40edbe6f4beec62021b4fd2544c431d8f694b4b4647`  
		Last Modified: Tue, 21 Oct 2025 02:35:21 GMT  
		Size: 54.9 MB (54860806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0452b809e62b80ba90b1a217898e5cf7675ff6aac67b2967e58600172590649e`  
		Last Modified: Tue, 21 Oct 2025 04:14:12 GMT  
		Size: 190.1 MB (190097178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1493ba40974f9698cde6967247a220e8b21c09de76901470d4a5ed125bfc1cb2`  
		Last Modified: Thu, 30 Oct 2025 21:35:20 GMT  
		Size: 180.3 MB (180267190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:174a6996165236196e2e2234b5a3e3fd65d247300e29913fdf2df1ee0adea225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15478629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e3fdfeaf6bf3fc08da419feb6196d81eb718e95950ce77f11a97ffb49dcb98`

```dockerfile
```

-	Layers:
	-	`sha256:9196d2d341db75ce952d1a4e29bd491214fe5bb55b9f55a90c7343d81100d44d`  
		Last Modified: Thu, 30 Oct 2025 23:45:42 GMT  
		Size: 15.5 MB (15466022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915a2f913a028e29271d667bf808cdabccd5dc980730eeb68ed9556c1750d267`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:ebfb2e206c2b74a1bb2d9b549cf50bddf2c1313e09fabb019c831ae5f7495a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.1 MB (565086977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0f7bf5bc46fc016e2a1fbd23835673151045c1b511f6c146c2dd9d721eef6c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:32 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:32 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:10d430deaa3d2ab4898db053e80d62403503897839bf6efd17ed5412b18d7973`  
		Last Modified: Tue, 21 Oct 2025 00:20:39 GMT  
		Size: 54.7 MB (54699294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c453fe6b4c7a680d5464137a3450d263e01a7ec4d491659295432d36b0198bbc`  
		Last Modified: Tue, 21 Oct 2025 01:53:19 GMT  
		Size: 16.3 MB (16267847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96adc169c4af311ffba07fa68db5821d6b9b00d285e00f44dad87eff52496658`  
		Last Modified: Tue, 21 Oct 2025 02:35:42 GMT  
		Size: 56.0 MB (56048779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd845a5707f187f6670f0831bc55034f6333f3aa3eede705f688f3c3342392e`  
		Last Modified: Tue, 21 Oct 2025 04:14:36 GMT  
		Size: 200.1 MB (200103484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae4b0e0faf517253d9eb9d5185f476ec1cdfd4f000a81910c9827c0acc7d451`  
		Last Modified: Thu, 30 Oct 2025 21:35:16 GMT  
		Size: 238.0 MB (237967573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:66f198e4ca90d5791b0a7ff640ee5c546edbfd2e0dfeb179fb4f174b4be5814e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15463224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d7dafb0e855c67125a259fe625f7a9d7f828eb79aad926e34bbb81d981988c`

```dockerfile
```

-	Layers:
	-	`sha256:1b2ab51fb7cebaa093a1da9d9de0794786d042ff60414a0211a492701aab92a9`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 15.5 MB (15450753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fd7b2b4922a57612d543c90720e157bdeb2bd2a9b6c5aa37cafabc33a2328f0`  
		Last Modified: Thu, 30 Oct 2025 23:46:00 GMT  
		Size: 12.5 KB (12471 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:79e8bbf426da1710dea53aa80da3ba8823060dc1761e6fd2a92c49e0f4809c76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1-slim` - linux; amd64

```console
$ docker pull rust@sha256:618466f4caae45cd6b7b6adfa98764ad462aacf67e7149c6d277c625da9f1282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316292209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c7ce709bce953db30bba7b3470638840d37d0e0a97220d6ba0542ae17aad67`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de44ca22a261b7801f942055dc9512f4e262e99021abda7f616cb77e45f2ac15`  
		Last Modified: Tue, 21 Oct 2025 08:48:56 GMT  
		Size: 286.5 MB (286514285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:65edc8293295cd16da8bf098701a6a507618a7dd2a9331e3f668a57ffe1c63df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4178629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6aa3d298b90262ca1f963f745149eb9cd429a8e23605e7cdc8ed89a4a4bb2f2`

```dockerfile
```

-	Layers:
	-	`sha256:4a5d4e539b906905d0a1a8cf26f58a195fa73f0755e02e96c515a60213341b47`  
		Last Modified: Tue, 21 Oct 2025 08:45:29 GMT  
		Size: 4.2 MB (4165011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e92458c8a75e4c47ff513c54b479567ce494fbb4081e948a711085a94e7b4b`  
		Last Modified: Tue, 21 Oct 2025 08:45:30 GMT  
		Size: 13.6 KB (13618 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:36bd228e236519c3a747a87570e7f83dab399d17eca3ef372e6484c3055c6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334448212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c202a0d535ea0887983203aae69fdf71f527951cf86b2b21f3fb6c2cf9a538`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:37:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:37:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:37:12 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6e00fb9e9c84f34ed2d592246743cef540466ac4115722b315d862bccdbb44`  
		Last Modified: Thu, 30 Oct 2025 21:37:57 GMT  
		Size: 308.2 MB (308235318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4e20e1ca9b0f23d783ec6d6ed5be8fa58ddaf53b726d80cd6fe80cf82a708eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b868546b1ef1b0edf1d23ec51f66614251da1094f46405866d3bf09b052aecad`

```dockerfile
```

-	Layers:
	-	`sha256:14738f7012d7020bd06896025d57d8d8f840e853cca38898526091bad7f49804`  
		Last Modified: Thu, 30 Oct 2025 23:45:32 GMT  
		Size: 4.0 MB (3969887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da73b8e3cdf4379799012870a7c21e494173161ddc8b1b353fc501f5632e4cf`  
		Last Modified: Thu, 30 Oct 2025 23:45:33 GMT  
		Size: 15.7 KB (15744 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8f015c79dd7ae0d1ab3218f86dda57f805a046991a5a67aa40088a67965806e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280064640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ccfb92e01921c8ed8fe03746498812688fe017b71f41f9e31a6cea79147abe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9e403b0cf550d52dedd0ab0aa7cbdcdd11f44b28ceb00d624c5c3d50a41df8`  
		Last Modified: Thu, 30 Oct 2025 23:47:09 GMT  
		Size: 249.9 MB (249922513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:cc442428572057302c62370a3c8514cb787a1a7daeed774b9f01e3a53f53d5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96a2c18c7d5bc0df280a6b286dc537b572cbe31668fcf2ad169f1bdf85194d`

```dockerfile
```

-	Layers:
	-	`sha256:606f393a1954d59bcd6d8915d68d376cd05d29024f9a559d92c8ad47da7baa53`  
		Last Modified: Thu, 30 Oct 2025 23:45:37 GMT  
		Size: 4.3 MB (4256227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32db46c306be7344e9ad5e0d189a1f9fccfa49d28d6336ecf1d9609a07d3da88`  
		Last Modified: Thu, 30 Oct 2025 23:45:38 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:ef194da922ba0594e7b7ddf8676004948a82926c4d57ac47bf5a47d85b43d571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341758796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4548274d12a2843de650e527ef6fbf4c3a6d29412091c3b2129c37809a899eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:52 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e995015b3e24125a0c10003ec7b1e384ce24f06f88cbd49bce3e36d2e4ffd8f`  
		Last Modified: Thu, 30 Oct 2025 21:36:35 GMT  
		Size: 310.5 MB (310464168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:5a52de8d007cb783912f98e3a2bc9ef1bea117a247b300d3bf0ed25db3ef7b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05360c911e791bc9a471f2026d992be7509b06ede83672b314adfab6d540bf4b`

```dockerfile
```

-	Layers:
	-	`sha256:657d29bb5c22513fcfdf6fccc85d309ca3ac85cc4258c72801d105ab1c31c57a`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 4.1 MB (4138524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed724e78f81430b3f4c6c9bf61b7039d1389fa37f5495feb17edb5614799f43`  
		Last Modified: Thu, 30 Oct 2025 23:45:44 GMT  
		Size: 15.6 KB (15579 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:72b668dd78a23c4a07810e311f75b18800d78d8b842f464b61ebf09659fc734a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 MB (388910993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11aecbbe059663e629a6a1abc931ed99632579ce2b826607539fd7c5dbe41e57`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a2a3e69fb5be32fda430122dfe24ff452aed1c97ebc7a331f684085f9a9caa`  
		Last Modified: Tue, 21 Oct 2025 18:09:51 GMT  
		Size: 355.3 MB (355312475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4051cc4a20c93b4a51262e6e33ba8be0c65a6769b70b76e8486124d3f31b7cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddf9a019c7107abe4e7b64c25d8cce534229de6341057921d82c64ec2afc5fb`

```dockerfile
```

-	Layers:
	-	`sha256:f9375169da8a2e632c640de11742ddfd32dcdc88e874a300d9caedcd94bc08fb`  
		Last Modified: Tue, 21 Oct 2025 17:44:42 GMT  
		Size: 4.2 MB (4161472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72f384288b484aab5875d8e0d36379250accb364045389bd7d5b1c897f9b7a0e`  
		Last Modified: Tue, 21 Oct 2025 17:44:43 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; riscv64

```console
$ docker pull rust@sha256:aaf1ec04eb2b47005e3b8560b0ab3fa83b42cb6b8c8cd6c6eb55a3c1ca29fd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 MB (391690936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd90d32888708414dd2407217bdbeb9884c97b7b7c8bf613038f97a472c8c4f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:00:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:00:19 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2315ad783eb28b652f5440fe195ec3068e8c8429c644f9745c84f8c522147`  
		Last Modified: Thu, 30 Oct 2025 22:12:21 GMT  
		Size: 363.4 MB (363415286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b085520540a279fab989fbd055fdff984bfe91d00f603dc6d9c1ee6747d497ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cc7bb3bca0e889b9a141380fcd0cf516a70126219e8fbac44ce160e69a9225`

```dockerfile
```

-	Layers:
	-	`sha256:e20ad570b9c4befd769026dc8b5716c3cf74fc0c6bdbddae3ab6e42e13ccdf5e`  
		Last Modified: Thu, 30 Oct 2025 23:45:53 GMT  
		Size: 4.2 MB (4239428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8670d848e45c5e062ecf29084ab05335daba00c88a567e96c2cc5fca9b04fbe3`  
		Last Modified: Thu, 30 Oct 2025 23:45:54 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:38ebb79c4b041ab046e504b5de098381f8027201a2594744a1eb1fecba242ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.1 MB (379117853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd57e4210e0c402a7b13d84e7dbf8a58418c9777b67aa36fa3c2222c9bae1144`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:54:35 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:54:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:54:35 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9805f4fca0189a31ca7f470c6efdd8dd933a751f5e840c7dbe3eb3034acef906`  
		Last Modified: Thu, 30 Oct 2025 22:56:45 GMT  
		Size: 349.3 MB (349280598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:e2b502b6ae9b904b73922a60e8ebe8814262ef8cb49c465af48c8494dbd80fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5388a6f6d7beec83a26ed19423edba57454d4145bb7d7f5aaefbf1faaa6eb99d`

```dockerfile
```

-	Layers:
	-	`sha256:51b388bf3623dd03362dcb15f7452b4677d633e967a003b3bc39faf47e960502`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 4.0 MB (3982759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a69eb51b743dde6eed89af2bfc049b12313cde5e899319a66fa67ebbb2c5ac`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:4abb5e12778478ce3b5677763cfac7b548364550163f36170fda96e3b3dd384c
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
$ docker pull rust@sha256:4f572135209e89d488fadb81d8a07309857f9b9c5280b54c85a44b71629e8cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310087390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd87f1b314f1f2fdc33693c2d57a945f5597602f63261311dbfe7debabf73393`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3a41ef4bf77ba6860bf1eb6281bdece6349b93d33e84d3f8445240f8062abf`  
		Last Modified: Tue, 21 Oct 2025 08:46:30 GMT  
		Size: 281.9 MB (281859069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8b0e00390a9a6c8e7a5b1493e02e15aabc96eb6b2abda74dc2664f047207be55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50eb0611fe6868b1ac58de80a9850ae872e1020933a9d57c03213a1458bbe096`

```dockerfile
```

-	Layers:
	-	`sha256:0baa4d2138bc1798e0eae0ef60c7b41dff4596720c43a883c93448d71b6db064`  
		Last Modified: Tue, 21 Oct 2025 08:45:10 GMT  
		Size: 4.1 MB (4095479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa65cc6e87b30f22cc9142de730e39496af45a42e414bb528eee3db369a8a41d`  
		Last Modified: Tue, 21 Oct 2025 08:45:10 GMT  
		Size: 12.1 KB (12084 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:1a66676e5c0a918aa45dc2fd4f34c16341d8bd0d064bcb7d815d84948da34398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329757809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c700e6793c04e8485ea32a54a1c3181ceb258694c1ee891dbaa530f552a2137`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 21:35:35 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:35 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb5b7bfc507827968f205851cea67b7a646a133c9116ec8737777be53b48787`  
		Last Modified: Thu, 30 Oct 2025 21:36:19 GMT  
		Size: 305.8 MB (305823786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4d727c9416ea7aa7accb2b6d82a1f1de5c78dc426821a57097eada3482d424d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3389581a9eef53aef89c9fe9accc7fed4cb4a49b423420c31e055cb167a7c7de`

```dockerfile
```

-	Layers:
	-	`sha256:9a1821533a3548a60f32478502545e387b5512c73dc2ef81518a839c820dfd39`  
		Last Modified: Thu, 30 Oct 2025 23:45:42 GMT  
		Size: 3.9 MB (3909876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6ed7f684cc050dc1b7ba74ce805f9039dbc61ddf92e8fe680bdb0a148f49b5b`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 14.0 KB (13964 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:756adb3f9d5c27df7bda4994157cb1cdca4cfdf76b8067a906ce5ff86976859e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274222169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0949ace3836ff38d491823d42f6201e9900fc4d22cf7a1b5d1e486cb355cdd9f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 21:35:36 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:36 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:36 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1f6c6c415a2d4c2edb9805e85b4dd69f95451b08268ffadfa1cdc061e695e0`  
		Last Modified: Thu, 30 Oct 2025 21:36:13 GMT  
		Size: 246.1 MB (246119979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:26a1086edf6420fbae6f26d20f0a2e8dca444eece965956194efe35e03d12a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b8fa2cd2b51fd9918b40c6c59ef73fac18d50aeb2bda9819c79a14219bcd30`

```dockerfile
```

-	Layers:
	-	`sha256:49e6348f3e8ffeac0bcd864980bf5f66c031fe768ed1d3c96c76d88dc7d4580f`  
		Last Modified: Thu, 30 Oct 2025 23:45:49 GMT  
		Size: 4.1 MB (4117775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90e56046bfcea1eefde6da940a766b28525d88059af7258ec565aa8e2c50f09a`  
		Last Modified: Thu, 30 Oct 2025 23:45:50 GMT  
		Size: 14.0 KB (13988 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:8ee0bf09c075a2f76ab2a753178a50023da8354eaa3066be15ae6df16b40eb26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.8 MB (334773527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f02408a764c4d03ef0ac688ee39de788035eb1fc14f6701fc34b094b37ec2a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df86e57d1d11515507bced15d2c5b47745ef47d90bf56ccfea3ffeb9852fdea4`  
		Last Modified: Thu, 30 Oct 2025 21:36:42 GMT  
		Size: 305.6 MB (305563849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4c7086dfaf26b09349225db4c780cf050cd5c0c5587f443eb99860dab7dcc2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4088714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ca752b45a8a21a6be117b63b2108326231dbd39bf5ad0f1421afa525c16f0f`

```dockerfile
```

-	Layers:
	-	`sha256:41e7bf57a66535222d70a721ed5c6d7627a2529faa2fa47097ea4924980ffe34`  
		Last Modified: Thu, 30 Oct 2025 23:45:56 GMT  
		Size: 4.1 MB (4074862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d529607b7e48cf2c2deba92ff2676f549bc263c168014cc85eaccd836f9b478`  
		Last Modified: Thu, 30 Oct 2025 23:45:57 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:618319743dba7907bf939f4fd93e4780a26f850891390db402bb5410fd296f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.3 MB (389270928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9901f02b9f06ecb4ec8b7de647fc610ee1ff40888508743a53f7af37b2588b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f2c98917f6ab10ac1a3e91d3f450c9d291d357d9f62f4fa1c6aeff0ac06969`  
		Last Modified: Tue, 21 Oct 2025 18:03:16 GMT  
		Size: 357.2 MB (357202148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0debd4a0f8008916877b1c7a02f3cb353375e45f10ddc5ffe275c4023fc20550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a048f7267ae5d5dbf804407baf9bc29c402ed905fb44e6f8ead9a068d7c80e`

```dockerfile
```

-	Layers:
	-	`sha256:cac15ddb9bc0ce5dd1e6e206817449698fe25f593fb8b3ff13b1f84b2c0517d6`  
		Last Modified: Tue, 21 Oct 2025 17:44:47 GMT  
		Size: 4.1 MB (4069081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6cc684615c6eb1c2c5f68c068da0b19e0e3ecff77cd4fb8fc7b8d20982c0199`  
		Last Modified: Tue, 21 Oct 2025 17:44:48 GMT  
		Size: 12.1 KB (12127 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b5ae74b41977de30791004301b9a55684a4a354fbbfe5a46fd7c412a1db484b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.9 MB (373924203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c02d1953e53a49919fdf3212d3b0191ff68e4b62f8b6cd5875592f08ab9f534`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 22:45:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:45:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:45:13 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:43b0f588b497b17691a3547afa4ae41853829cffde6930e6425ddae4a3f89278`  
		Last Modified: Tue, 21 Oct 2025 00:21:28 GMT  
		Size: 26.9 MB (26884356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ac26cb25e9079f7df28678594c9546404a88850ef59d1906cdae0af1834af2`  
		Last Modified: Thu, 30 Oct 2025 22:47:19 GMT  
		Size: 347.0 MB (347039847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ca7ec822c8eac17e6a09f4496f9ea73f7f5cf4a227037de86239e19824a01cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7bdc57546b9d419b45fd2009461ac7feb00999dd5424e0861ae69445408a1d`

```dockerfile
```

-	Layers:
	-	`sha256:a163636249f2f57c519801b581ece738bbca25c2502343f983fc21023358dc51`  
		Last Modified: Thu, 30 Oct 2025 23:46:05 GMT  
		Size: 3.9 MB (3933157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4082065c8b0d4a306a1d88f8e5c972213af58b5b72c4f05bb1bdf4f35a0db44`  
		Last Modified: Thu, 30 Oct 2025 23:46:06 GMT  
		Size: 13.9 KB (13884 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:511c91223741697cf68aa071b1d676f1545ad354760bb2a6f9ec65b4efa2450d
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
$ docker pull rust@sha256:532c9bafb504801211101abb4e38741bf310e674b45ba05fe837a0c48b18093a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301490013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375eb8ec7a7a87934ba8adca1300d377595f58bbbf6720a63077f2c567e43e17`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95330b7f3a0a801883f9715ffac7f513641a9c3c181e15460a2979b4e7981877`  
		Last Modified: Tue, 21 Oct 2025 08:48:23 GMT  
		Size: 271.2 MB (271231648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:67072e1caa1ac00c1f7896e4cd9c0020bfbf87f34547d25c8406e77ad587f21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df21e2a5b857681a8e521b60d9687f161de4cebccf166ef2b31fa12fa8b3bae4`

```dockerfile
```

-	Layers:
	-	`sha256:36dcd507b25119bcc46133aaf8f95f2f4b063ba744c8da723dc4c733200e14dd`  
		Last Modified: Tue, 21 Oct 2025 08:45:21 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5d4b466b9bdcddd1284d82d1b6e4cd805119fb7d12373a0324ad1da312749c`  
		Last Modified: Tue, 21 Oct 2025 08:45:22 GMT  
		Size: 11.4 KB (11355 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:13fc3a2170515d49a864808c172e6ef2cdb6ceb7d516c49d43f25dc6d7220aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325804399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e041264a283725f3e8d0e27bf0c41b94d5c1f7a4f0ad080f4bab768ec221cd17`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 21:35:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:42 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4b897c04dec26603bcc1b01b4283220cd1ffb208f0ec4c0db9e08dab58fcfb5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 25.5 MB (25546187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f470db143d0044ed53ee3c62d37c264ce9347606e374e60113030bb748254e`  
		Last Modified: Thu, 30 Oct 2025 21:36:25 GMT  
		Size: 300.3 MB (300258212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:80c8d376c747cb7f8555437910e6c9a1add734f8d43488803a7fbb48d5300c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cb2dd69accf11a0b247c6ebd6851c11ca87d48376f5b4c43e55069d8779493`

```dockerfile
```

-	Layers:
	-	`sha256:3886373e00abc1e6f64ba5c91f674e54b4699c88fafb62b650aaaf8da12bec8e`  
		Last Modified: Thu, 30 Oct 2025 23:45:53 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea67c0e765b1816115cb1b8753a4b992d18c1f0dbe17cbdafddb31a15734a966`  
		Last Modified: Thu, 30 Oct 2025 23:45:54 GMT  
		Size: 12.8 KB (12794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7ff887fd3eb13d26eecb0f40398028fdc12a3298ef48c8528331016decfb0ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264715851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ae94dab2b12284d1f2e92e3e2ac7b56eff6bb02864e3639caa14c43b4390fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 21:34:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:39 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db337e821e80e597fa142716f1cb02566d2cf4168196f5f08a415cfb4a249b7`  
		Last Modified: Thu, 30 Oct 2025 21:35:15 GMT  
		Size: 236.0 MB (235967450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f46b8601c7c669072e496b7807335af3362860103487ba6340ac14700e4d2e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3c48bda2928a06b24f54d0c55cb10592408f842b75a6984f01eb69ebb7f065`

```dockerfile
```

-	Layers:
	-	`sha256:ab6b83830f27e4a54af4a4ff3428fe72f6898a17d7e3c21d3a7b6165de49140c`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4018ce6087359d14714e6bcbfbfdc372aa884d3abeff3000503021a2c3381d0f`  
		Last Modified: Thu, 30 Oct 2025 23:46:00 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:a8c4281836aee33f681efe73b74c2fe608821ab8a79e1e4f53c408cbee6a616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329920628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44d16d04c4e9d940226b9321174f5ada41cc3046700d8f53b9f75357436b02a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 21:35:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:04 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ed9b7a4c5998c0d248e37f414fa0883c2b695df7b879c0ba096280f29fcb2660`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 31.2 MB (31191494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8bca4c0d96694e3d489bc0df62c181f63f68bd29966b3d385296b7f25514f0`  
		Last Modified: Thu, 30 Oct 2025 21:35:46 GMT  
		Size: 298.7 MB (298729134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8220d5bc4c59b662f331a750b1c3e053eb553fcf58d971daa7ceda6433fac105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ee75a2e521250b772ff737b27beb9860a1292184f784af6f4e157e5a734559`

```dockerfile
```

-	Layers:
	-	`sha256:5ee000ac8ab06e33a71014e51eeb45b60c7820fd0d03e45c9fd2b1573f530073`  
		Last Modified: Thu, 30 Oct 2025 23:46:05 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fb44d48fb78f0b88ebc033734c23af5eb6f66040ca67ec8536dcd1a1755ed6f`  
		Last Modified: Thu, 30 Oct 2025 23:46:06 GMT  
		Size: 12.7 KB (12682 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-trixie`

```console
$ docker pull rust@sha256:79e8bbf426da1710dea53aa80da3ba8823060dc1761e6fd2a92c49e0f4809c76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1-slim-trixie` - linux; amd64

```console
$ docker pull rust@sha256:618466f4caae45cd6b7b6adfa98764ad462aacf67e7149c6d277c625da9f1282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316292209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c7ce709bce953db30bba7b3470638840d37d0e0a97220d6ba0542ae17aad67`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de44ca22a261b7801f942055dc9512f4e262e99021abda7f616cb77e45f2ac15`  
		Last Modified: Tue, 21 Oct 2025 08:48:56 GMT  
		Size: 286.5 MB (286514285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:65edc8293295cd16da8bf098701a6a507618a7dd2a9331e3f668a57ffe1c63df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4178629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6aa3d298b90262ca1f963f745149eb9cd429a8e23605e7cdc8ed89a4a4bb2f2`

```dockerfile
```

-	Layers:
	-	`sha256:4a5d4e539b906905d0a1a8cf26f58a195fa73f0755e02e96c515a60213341b47`  
		Last Modified: Tue, 21 Oct 2025 08:45:29 GMT  
		Size: 4.2 MB (4165011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e92458c8a75e4c47ff513c54b479567ce494fbb4081e948a711085a94e7b4b`  
		Last Modified: Tue, 21 Oct 2025 08:45:30 GMT  
		Size: 13.6 KB (13618 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:36bd228e236519c3a747a87570e7f83dab399d17eca3ef372e6484c3055c6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334448212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c202a0d535ea0887983203aae69fdf71f527951cf86b2b21f3fb6c2cf9a538`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:37:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:37:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:37:12 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6e00fb9e9c84f34ed2d592246743cef540466ac4115722b315d862bccdbb44`  
		Last Modified: Thu, 30 Oct 2025 21:37:57 GMT  
		Size: 308.2 MB (308235318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:4e20e1ca9b0f23d783ec6d6ed5be8fa58ddaf53b726d80cd6fe80cf82a708eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b868546b1ef1b0edf1d23ec51f66614251da1094f46405866d3bf09b052aecad`

```dockerfile
```

-	Layers:
	-	`sha256:14738f7012d7020bd06896025d57d8d8f840e853cca38898526091bad7f49804`  
		Last Modified: Thu, 30 Oct 2025 23:45:32 GMT  
		Size: 4.0 MB (3969887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da73b8e3cdf4379799012870a7c21e494173161ddc8b1b353fc501f5632e4cf`  
		Last Modified: Thu, 30 Oct 2025 23:45:33 GMT  
		Size: 15.7 KB (15744 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8f015c79dd7ae0d1ab3218f86dda57f805a046991a5a67aa40088a67965806e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280064640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ccfb92e01921c8ed8fe03746498812688fe017b71f41f9e31a6cea79147abe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9e403b0cf550d52dedd0ab0aa7cbdcdd11f44b28ceb00d624c5c3d50a41df8`  
		Last Modified: Thu, 30 Oct 2025 23:47:09 GMT  
		Size: 249.9 MB (249922513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:cc442428572057302c62370a3c8514cb787a1a7daeed774b9f01e3a53f53d5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96a2c18c7d5bc0df280a6b286dc537b572cbe31668fcf2ad169f1bdf85194d`

```dockerfile
```

-	Layers:
	-	`sha256:606f393a1954d59bcd6d8915d68d376cd05d29024f9a559d92c8ad47da7baa53`  
		Last Modified: Thu, 30 Oct 2025 23:45:37 GMT  
		Size: 4.3 MB (4256227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32db46c306be7344e9ad5e0d189a1f9fccfa49d28d6336ecf1d9609a07d3da88`  
		Last Modified: Thu, 30 Oct 2025 23:45:38 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; 386

```console
$ docker pull rust@sha256:ef194da922ba0594e7b7ddf8676004948a82926c4d57ac47bf5a47d85b43d571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341758796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4548274d12a2843de650e527ef6fbf4c3a6d29412091c3b2129c37809a899eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:52 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e995015b3e24125a0c10003ec7b1e384ce24f06f88cbd49bce3e36d2e4ffd8f`  
		Last Modified: Thu, 30 Oct 2025 21:36:35 GMT  
		Size: 310.5 MB (310464168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:5a52de8d007cb783912f98e3a2bc9ef1bea117a247b300d3bf0ed25db3ef7b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05360c911e791bc9a471f2026d992be7509b06ede83672b314adfab6d540bf4b`

```dockerfile
```

-	Layers:
	-	`sha256:657d29bb5c22513fcfdf6fccc85d309ca3ac85cc4258c72801d105ab1c31c57a`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 4.1 MB (4138524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed724e78f81430b3f4c6c9bf61b7039d1389fa37f5495feb17edb5614799f43`  
		Last Modified: Thu, 30 Oct 2025 23:45:44 GMT  
		Size: 15.6 KB (15579 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; ppc64le

```console
$ docker pull rust@sha256:72b668dd78a23c4a07810e311f75b18800d78d8b842f464b61ebf09659fc734a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 MB (388910993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11aecbbe059663e629a6a1abc931ed99632579ce2b826607539fd7c5dbe41e57`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a2a3e69fb5be32fda430122dfe24ff452aed1c97ebc7a331f684085f9a9caa`  
		Last Modified: Tue, 21 Oct 2025 18:09:51 GMT  
		Size: 355.3 MB (355312475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:4051cc4a20c93b4a51262e6e33ba8be0c65a6769b70b76e8486124d3f31b7cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddf9a019c7107abe4e7b64c25d8cce534229de6341057921d82c64ec2afc5fb`

```dockerfile
```

-	Layers:
	-	`sha256:f9375169da8a2e632c640de11742ddfd32dcdc88e874a300d9caedcd94bc08fb`  
		Last Modified: Tue, 21 Oct 2025 17:44:42 GMT  
		Size: 4.2 MB (4161472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72f384288b484aab5875d8e0d36379250accb364045389bd7d5b1c897f9b7a0e`  
		Last Modified: Tue, 21 Oct 2025 17:44:43 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; riscv64

```console
$ docker pull rust@sha256:aaf1ec04eb2b47005e3b8560b0ab3fa83b42cb6b8c8cd6c6eb55a3c1ca29fd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 MB (391690936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd90d32888708414dd2407217bdbeb9884c97b7b7c8bf613038f97a472c8c4f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:00:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:00:19 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2315ad783eb28b652f5440fe195ec3068e8c8429c644f9745c84f8c522147`  
		Last Modified: Thu, 30 Oct 2025 22:12:21 GMT  
		Size: 363.4 MB (363415286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:b085520540a279fab989fbd055fdff984bfe91d00f603dc6d9c1ee6747d497ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cc7bb3bca0e889b9a141380fcd0cf516a70126219e8fbac44ce160e69a9225`

```dockerfile
```

-	Layers:
	-	`sha256:e20ad570b9c4befd769026dc8b5716c3cf74fc0c6bdbddae3ab6e42e13ccdf5e`  
		Last Modified: Thu, 30 Oct 2025 23:45:53 GMT  
		Size: 4.2 MB (4239428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8670d848e45c5e062ecf29084ab05335daba00c88a567e96c2cc5fca9b04fbe3`  
		Last Modified: Thu, 30 Oct 2025 23:45:54 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-trixie` - linux; s390x

```console
$ docker pull rust@sha256:38ebb79c4b041ab046e504b5de098381f8027201a2594744a1eb1fecba242ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.1 MB (379117853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd57e4210e0c402a7b13d84e7dbf8a58418c9777b67aa36fa3c2222c9bae1144`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:54:35 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:54:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:54:35 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9805f4fca0189a31ca7f470c6efdd8dd933a751f5e840c7dbe3eb3034acef906`  
		Last Modified: Thu, 30 Oct 2025 22:56:45 GMT  
		Size: 349.3 MB (349280598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:e2b502b6ae9b904b73922a60e8ebe8814262ef8cb49c465af48c8494dbd80fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5388a6f6d7beec83a26ed19423edba57454d4145bb7d7f5aaefbf1faaa6eb99d`

```dockerfile
```

-	Layers:
	-	`sha256:51b388bf3623dd03362dcb15f7452b4677d633e967a003b3bc39faf47e960502`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 4.0 MB (3982759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a69eb51b743dde6eed89af2bfc049b12313cde5e899319a66fa67ebbb2c5ac`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-trixie`

```console
$ docker pull rust@sha256:4cdae04e9e94e189ab2a6b462c93ed5f8ab248cde1c6100c59e958976b1c4594
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1-trixie` - linux; amd64

```console
$ docker pull rust@sha256:7ccdba2b655ebac8408566b54b8dbd02b44756759e8d73109227edb2b81b2942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589704892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd127f46648e9bce2a1ffa8096f2babd56565f986ae96fa6abef7bc6fc290ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d573bf42b377ce6a5a0451c15388849686fa4058efd68999f3b014daeb5b55`  
		Last Modified: Tue, 21 Oct 2025 01:42:47 GMT  
		Size: 25.6 MB (25615545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dfe2fac1c486e9aaf41d1028ed30be2c442aa84af44462bc7bac8c148ffb13`  
		Last Modified: Tue, 21 Oct 2025 04:47:38 GMT  
		Size: 67.8 MB (67784857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d5bd8a8d262418bf22e705535ce38c6789dc72e319d76b30aafa5c331b6924`  
		Last Modified: Tue, 21 Oct 2025 10:24:40 GMT  
		Size: 235.9 MB (235927971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68557728bac69b81da96dae42ed23a374347244afaca7210e768400aecefb4d`  
		Last Modified: Tue, 21 Oct 2025 12:18:46 GMT  
		Size: 211.1 MB (211091548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:c6e9c920b84edb3271e9884c7e7d7736fa75456c61d869517d117f8b006f02f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17223403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0af01840a4d7313dce07a4cd8705141858d215468038f488a00bc2983f4203`

```dockerfile
```

-	Layers:
	-	`sha256:4de25e75936e713c9998f626efb488832cbbc139588b1dab75dee11b9e80e7da`  
		Last Modified: Tue, 21 Oct 2025 14:44:21 GMT  
		Size: 17.2 MB (17209918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f86274d8e899d886607e02351051d3409137c5b77521eb87725d6ff4cfb078e`  
		Last Modified: Tue, 21 Oct 2025 14:44:22 GMT  
		Size: 13.5 KB (13485 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:df192b38e9142bc8d454be61de04235e6e3d6e3cc142b3ca4461565fdcdb5c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583252486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a735b8020181b775c6ff35bd4f4ddaf6fccacf90d6baef0e5b88f5fac468e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:20 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:20 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:20 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cda7f0b38d756bba039d1251605b315c32a18bef1d71d1a0a98df8f4c7fb6`  
		Last Modified: Tue, 21 Oct 2025 06:18:01 GMT  
		Size: 193.2 MB (193235864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7085e104656ea6c66d8ba95df53b71fae0ae8c42dce84c36d3dd51cc63114cc`  
		Last Modified: Thu, 30 Oct 2025 23:48:47 GMT  
		Size: 258.0 MB (257970062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:7bdc29f59dfa654c3d2300e1d752366f54275c8759cf65ee11f3b51b5ee02ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b60585f52529edd183ac79b90c91a6c5c7a9f7718df436557b6c48120de964f`

```dockerfile
```

-	Layers:
	-	`sha256:e7514cf6a08ba2c22ef71f6054b5e755385f65048788dccfe2a655928e7613af`  
		Last Modified: Thu, 30 Oct 2025 23:44:49 GMT  
		Size: 17.0 MB (16977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7716c3ffa9ab429830b3182885b3f920b00e895ca1ca6dc9aa0e0866b3405617`  
		Last Modified: Thu, 30 Oct 2025 23:44:50 GMT  
		Size: 15.5 KB (15508 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:69d4bc701fcca1d78e46d634aca8f1b0a3b967b755e87d0c3e883abf402a92c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.6 MB (548594894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124905d571200dee29c0250b5a56242cbb369d8d6a2f46770ef2060b9aa6ae19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:13 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f695ddffd81064f15ea19428e2d643e8b560e48e54ae801a8d63c45ad6ac29`  
		Last Modified: Tue, 21 Oct 2025 04:14:42 GMT  
		Size: 226.1 MB (226078014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b0009962587465f15c28cbaa4e05bede4600a6b68c86467eb69e4227df6c84`  
		Last Modified: Thu, 30 Oct 2025 23:44:37 GMT  
		Size: 180.3 MB (180266565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:a2ff1f30c17e94d0edaf28e068fd1a99b76f759cebd6a2b304606e7c085f21aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17309822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d625100634edff47e63fc8b469129a68a25115bad3e0531a1f7b594067d865`

```dockerfile
```

-	Layers:
	-	`sha256:b3eb795d70d03f35b63225b01143c51f0f8b6622f4022cb5db697d2ba9e108d7`  
		Last Modified: Thu, 30 Oct 2025 23:45:11 GMT  
		Size: 17.3 MB (17294274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f42745a111fee91795bb40aa7014469e06556069a7271890a09e381d064bfc`  
		Last Modified: Thu, 30 Oct 2025 23:45:12 GMT  
		Size: 15.5 KB (15548 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-trixie` - linux; 386

```console
$ docker pull rust@sha256:0f36b8c5b45a1403f31ae3e1f2db1be6126a1a8d3d89157dfbf1a9caf8364a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.4 MB (625391663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5670c24f999c8b72981507cb47d2b2dcaf53d09af6a4187abbd6fe21f62d48fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:12 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e11ad5a4fd5be41f07ac93311f8ae1f7dfd6455edf9f5cf950e26d70ee4c6`  
		Last Modified: Tue, 21 Oct 2025 01:53:30 GMT  
		Size: 26.8 MB (26775679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e99453a1ea6755d1a3a58fe6632281db5820c733291dbefe645ffd8397c7e4`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 69.8 MB (69795039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4be1d74f0f5cdfd17973a37d16dc7ed75a3f628a94c99be57d59571d3a9b4`  
		Last Modified: Tue, 21 Oct 2025 04:13:56 GMT  
		Size: 240.1 MB (240053433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b95b67c6e22caf5578ea1eddb03fde4e1cedc03293a23c829f701c73cc927b`  
		Last Modified: Thu, 30 Oct 2025 23:51:31 GMT  
		Size: 238.0 MB (237966938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:de9c5a2a0cb7e4e8b0375014aeac39baef1c37299b1295b32c691537e29bbdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17193526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7797bff6bc0b961011e7f5b876cc1e1e46af5fb5bb27dddfa8a0836045fbdcf6`

```dockerfile
```

-	Layers:
	-	`sha256:4ba4d0a028ca002c9baa8b6e271bbed6f0b707811424f49afb3dbed5b7bbbc66`  
		Last Modified: Thu, 30 Oct 2025 23:45:27 GMT  
		Size: 17.2 MB (17178183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f46fff4553bf23d62e5ffce1a59bed624919c2fea3703b65b013ef50394d42`  
		Last Modified: Thu, 30 Oct 2025 23:45:28 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-trixie` - linux; ppc64le

```console
$ docker pull rust@sha256:a29f6e27737a6b59309a166a28c4cf97dd2eefbfa88c3aca3304faa0ff08a3e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672649528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a952fb3ef83a44fc6533607fda15f4d747a2350849923b66222c95ce97864c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dfb88672cf0a942c4fdfcadf1912c35c9d30a3a001b18a9dad505fb960ae8`  
		Last Modified: Tue, 21 Oct 2025 07:47:00 GMT  
		Size: 27.0 MB (26996207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06029381e2f1b3a0885caf1b758b0461bfaf9db7b9642ca0b79ab28ed1dd4ecc`  
		Last Modified: Tue, 21 Oct 2025 17:35:58 GMT  
		Size: 73.0 MB (73029685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac677cb325b211e7ad7714eb6d52abf13c0d7630be372cac77812dd27241a158`  
		Last Modified: Wed, 22 Oct 2025 01:27:43 GMT  
		Size: 231.1 MB (231086523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff2e4d4f9807f075e3ff5c6c28631a324397b2b771ee6555b6d8e923ee06e0b`  
		Last Modified: Wed, 22 Oct 2025 14:51:26 GMT  
		Size: 288.4 MB (288427637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:f33a0240a7d92b5fda177a193f6e7c05cb951abb7c29daf3858c351311dbac60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17209060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36284e92be8526f5f13c82a2f801a21cf15d46cdae17422ca12254be41d6339`

```dockerfile
```

-	Layers:
	-	`sha256:3d6645f5d1a853359ab88d5ea6d06cd386d73bef8d296c30d6ee843f5dbd6028`  
		Last Modified: Wed, 22 Oct 2025 14:45:21 GMT  
		Size: 17.2 MB (17195507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0297a39c3c72137eb2edc4ce4ff2993062b460caa31ef206b40f28e10b1fe71`  
		Last Modified: Wed, 22 Oct 2025 14:45:22 GMT  
		Size: 13.6 KB (13553 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-trixie` - linux; riscv64

```console
$ docker pull rust@sha256:db568b830f6fd90592497dd0eda8001ed384c555723f1082ceb67a49b9968c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.7 MB (731746485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dde95f55f8cca95c0c52acf2dc0afce27141a1ec0354bce98292db2d8245a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:41:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:41:49 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c640441904d97046ee4a137483e3b6745e0a18782c3b688fede8e9ddf18261f`  
		Last Modified: Wed, 22 Oct 2025 18:09:29 GMT  
		Size: 25.0 MB (24953874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb6fec5cd2588ba9a09a9491547b6e7005f3640a81c530cc1f2e651257c901`  
		Last Modified: Fri, 24 Oct 2025 21:34:03 GMT  
		Size: 66.7 MB (66662364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c02978248d2c72ee734dd5ab68325ab5be1edbbfe6026472d198390eabe8cf`  
		Last Modified: Sun, 26 Oct 2025 13:26:52 GMT  
		Size: 322.8 MB (322829684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af21d31669ce50f730bd664ae7d97ab0697a48fc4c1fc527c93c32c6f717c3f3`  
		Last Modified: Thu, 30 Oct 2025 21:56:54 GMT  
		Size: 269.5 MB (269530257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:5d2476fa78b8cae7f942b74725782b510c4b6a2f687346c648591dd4613b5b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17281556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c73611675d5101a89fa89d59b3a33599e9498dfc407639e4c3b51d2879ed92d`

```dockerfile
```

-	Layers:
	-	`sha256:de5eee62216cb8618afba94f9d4c277f9a550568818b3cbe17aa78900016e6f7`  
		Last Modified: Thu, 30 Oct 2025 23:45:56 GMT  
		Size: 17.3 MB (17266092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c38e4c4e014047f4332c3cf3bf8372bf0ff126eadb475671eb5f6759bb6503e9`  
		Last Modified: Thu, 30 Oct 2025 23:45:57 GMT  
		Size: 15.5 KB (15464 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-trixie` - linux; s390x

```console
$ docker pull rust@sha256:58124806371c4a39a5ac92593a6f823c354d5d002cae39305db81a0b200dc7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.1 MB (648135109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571bb1f5470229ff143899581ee0538e785fbd8bb45168569fa265be37201747`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 22:48:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:48:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:48:48 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9f518343ed4506c34ae7900f538c56bac66f4fad9740034ee8b819bd8d15e`  
		Last Modified: Tue, 21 Oct 2025 12:43:19 GMT  
		Size: 26.8 MB (26783314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb7d34d2ff189fa2150ed8d82914c7669f312817531bbe187965e9d30825d3`  
		Last Modified: Tue, 21 Oct 2025 23:25:03 GMT  
		Size: 68.6 MB (68630635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4131ad2e1cf6d0e51274c6e30ebc34015c8e72c5b79a0146220944b33c750ff`  
		Last Modified: Wed, 22 Oct 2025 12:46:56 GMT  
		Size: 206.5 MB (206460184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2905cafaed65f05704ab3b4e23479ae861bb4a148a0aac8b459931962ccf1469`  
		Last Modified: Thu, 30 Oct 2025 22:52:24 GMT  
		Size: 296.9 MB (296909277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:54a2179f33db9cea350dd680ac4622e0df5e333f36232801102916c3b7ff749b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17002545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c6960bfd3415ad92fd83afb42906df93f6f114175be156af8cd8f842cfa20c`

```dockerfile
```

-	Layers:
	-	`sha256:24c7152c5b9ea076d3348e04b2479b166ba9b19eff01141c458fb04c53fdcdd6`  
		Last Modified: Thu, 30 Oct 2025 23:46:10 GMT  
		Size: 17.0 MB (16987149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc6358b456c6334b83aedd51c445eeedb3650635525e2e50790b42a8d5968cd`  
		Last Modified: Thu, 30 Oct 2025 23:46:11 GMT  
		Size: 15.4 KB (15396 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91`

```console
$ docker pull rust@sha256:eac325268dbdd1c874282a92ad2e0012f19005f65732f9828ecb077c1065c0f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.91` - linux; arm variant v7

```console
$ docker pull rust@sha256:df192b38e9142bc8d454be61de04235e6e3d6e3cc142b3ca4461565fdcdb5c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583252486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a735b8020181b775c6ff35bd4f4ddaf6fccacf90d6baef0e5b88f5fac468e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:20 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:20 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:20 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cda7f0b38d756bba039d1251605b315c32a18bef1d71d1a0a98df8f4c7fb6`  
		Last Modified: Tue, 21 Oct 2025 06:18:01 GMT  
		Size: 193.2 MB (193235864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7085e104656ea6c66d8ba95df53b71fae0ae8c42dce84c36d3dd51cc63114cc`  
		Last Modified: Thu, 30 Oct 2025 23:48:47 GMT  
		Size: 258.0 MB (257970062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91` - unknown; unknown

```console
$ docker pull rust@sha256:7bdc29f59dfa654c3d2300e1d752366f54275c8759cf65ee11f3b51b5ee02ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b60585f52529edd183ac79b90c91a6c5c7a9f7718df436557b6c48120de964f`

```dockerfile
```

-	Layers:
	-	`sha256:e7514cf6a08ba2c22ef71f6054b5e755385f65048788dccfe2a655928e7613af`  
		Last Modified: Thu, 30 Oct 2025 23:44:49 GMT  
		Size: 17.0 MB (16977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7716c3ffa9ab429830b3182885b3f920b00e895ca1ca6dc9aa0e0866b3405617`  
		Last Modified: Thu, 30 Oct 2025 23:44:50 GMT  
		Size: 15.5 KB (15508 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:69d4bc701fcca1d78e46d634aca8f1b0a3b967b755e87d0c3e883abf402a92c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.6 MB (548594894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124905d571200dee29c0250b5a56242cbb369d8d6a2f46770ef2060b9aa6ae19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:13 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f695ddffd81064f15ea19428e2d643e8b560e48e54ae801a8d63c45ad6ac29`  
		Last Modified: Tue, 21 Oct 2025 04:14:42 GMT  
		Size: 226.1 MB (226078014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b0009962587465f15c28cbaa4e05bede4600a6b68c86467eb69e4227df6c84`  
		Last Modified: Thu, 30 Oct 2025 23:44:37 GMT  
		Size: 180.3 MB (180266565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91` - unknown; unknown

```console
$ docker pull rust@sha256:a2ff1f30c17e94d0edaf28e068fd1a99b76f759cebd6a2b304606e7c085f21aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17309822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d625100634edff47e63fc8b469129a68a25115bad3e0531a1f7b594067d865`

```dockerfile
```

-	Layers:
	-	`sha256:b3eb795d70d03f35b63225b01143c51f0f8b6622f4022cb5db697d2ba9e108d7`  
		Last Modified: Thu, 30 Oct 2025 23:45:11 GMT  
		Size: 17.3 MB (17294274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f42745a111fee91795bb40aa7014469e06556069a7271890a09e381d064bfc`  
		Last Modified: Thu, 30 Oct 2025 23:45:12 GMT  
		Size: 15.5 KB (15548 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91` - linux; 386

```console
$ docker pull rust@sha256:0f36b8c5b45a1403f31ae3e1f2db1be6126a1a8d3d89157dfbf1a9caf8364a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.4 MB (625391663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5670c24f999c8b72981507cb47d2b2dcaf53d09af6a4187abbd6fe21f62d48fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:12 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e11ad5a4fd5be41f07ac93311f8ae1f7dfd6455edf9f5cf950e26d70ee4c6`  
		Last Modified: Tue, 21 Oct 2025 01:53:30 GMT  
		Size: 26.8 MB (26775679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e99453a1ea6755d1a3a58fe6632281db5820c733291dbefe645ffd8397c7e4`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 69.8 MB (69795039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4be1d74f0f5cdfd17973a37d16dc7ed75a3f628a94c99be57d59571d3a9b4`  
		Last Modified: Tue, 21 Oct 2025 04:13:56 GMT  
		Size: 240.1 MB (240053433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b95b67c6e22caf5578ea1eddb03fde4e1cedc03293a23c829f701c73cc927b`  
		Last Modified: Thu, 30 Oct 2025 23:51:31 GMT  
		Size: 238.0 MB (237966938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91` - unknown; unknown

```console
$ docker pull rust@sha256:de9c5a2a0cb7e4e8b0375014aeac39baef1c37299b1295b32c691537e29bbdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17193526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7797bff6bc0b961011e7f5b876cc1e1e46af5fb5bb27dddfa8a0836045fbdcf6`

```dockerfile
```

-	Layers:
	-	`sha256:4ba4d0a028ca002c9baa8b6e271bbed6f0b707811424f49afb3dbed5b7bbbc66`  
		Last Modified: Thu, 30 Oct 2025 23:45:27 GMT  
		Size: 17.2 MB (17178183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f46fff4553bf23d62e5ffce1a59bed624919c2fea3703b65b013ef50394d42`  
		Last Modified: Thu, 30 Oct 2025 23:45:28 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91` - linux; riscv64

```console
$ docker pull rust@sha256:db568b830f6fd90592497dd0eda8001ed384c555723f1082ceb67a49b9968c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.7 MB (731746485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dde95f55f8cca95c0c52acf2dc0afce27141a1ec0354bce98292db2d8245a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:41:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:41:49 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c640441904d97046ee4a137483e3b6745e0a18782c3b688fede8e9ddf18261f`  
		Last Modified: Wed, 22 Oct 2025 18:09:29 GMT  
		Size: 25.0 MB (24953874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb6fec5cd2588ba9a09a9491547b6e7005f3640a81c530cc1f2e651257c901`  
		Last Modified: Fri, 24 Oct 2025 21:34:03 GMT  
		Size: 66.7 MB (66662364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c02978248d2c72ee734dd5ab68325ab5be1edbbfe6026472d198390eabe8cf`  
		Last Modified: Sun, 26 Oct 2025 13:26:52 GMT  
		Size: 322.8 MB (322829684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af21d31669ce50f730bd664ae7d97ab0697a48fc4c1fc527c93c32c6f717c3f3`  
		Last Modified: Thu, 30 Oct 2025 21:56:54 GMT  
		Size: 269.5 MB (269530257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91` - unknown; unknown

```console
$ docker pull rust@sha256:5d2476fa78b8cae7f942b74725782b510c4b6a2f687346c648591dd4613b5b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17281556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c73611675d5101a89fa89d59b3a33599e9498dfc407639e4c3b51d2879ed92d`

```dockerfile
```

-	Layers:
	-	`sha256:de5eee62216cb8618afba94f9d4c277f9a550568818b3cbe17aa78900016e6f7`  
		Last Modified: Thu, 30 Oct 2025 23:45:56 GMT  
		Size: 17.3 MB (17266092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c38e4c4e014047f4332c3cf3bf8372bf0ff126eadb475671eb5f6759bb6503e9`  
		Last Modified: Thu, 30 Oct 2025 23:45:57 GMT  
		Size: 15.5 KB (15464 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91` - linux; s390x

```console
$ docker pull rust@sha256:58124806371c4a39a5ac92593a6f823c354d5d002cae39305db81a0b200dc7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.1 MB (648135109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571bb1f5470229ff143899581ee0538e785fbd8bb45168569fa265be37201747`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 22:48:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:48:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:48:48 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9f518343ed4506c34ae7900f538c56bac66f4fad9740034ee8b819bd8d15e`  
		Last Modified: Tue, 21 Oct 2025 12:43:19 GMT  
		Size: 26.8 MB (26783314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb7d34d2ff189fa2150ed8d82914c7669f312817531bbe187965e9d30825d3`  
		Last Modified: Tue, 21 Oct 2025 23:25:03 GMT  
		Size: 68.6 MB (68630635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4131ad2e1cf6d0e51274c6e30ebc34015c8e72c5b79a0146220944b33c750ff`  
		Last Modified: Wed, 22 Oct 2025 12:46:56 GMT  
		Size: 206.5 MB (206460184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2905cafaed65f05704ab3b4e23479ae861bb4a148a0aac8b459931962ccf1469`  
		Last Modified: Thu, 30 Oct 2025 22:52:24 GMT  
		Size: 296.9 MB (296909277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91` - unknown; unknown

```console
$ docker pull rust@sha256:54a2179f33db9cea350dd680ac4622e0df5e333f36232801102916c3b7ff749b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17002545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c6960bfd3415ad92fd83afb42906df93f6f114175be156af8cd8f842cfa20c`

```dockerfile
```

-	Layers:
	-	`sha256:24c7152c5b9ea076d3348e04b2479b166ba9b19eff01141c458fb04c53fdcdd6`  
		Last Modified: Thu, 30 Oct 2025 23:46:10 GMT  
		Size: 17.0 MB (16987149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc6358b456c6334b83aedd51c445eeedb3650635525e2e50790b42a8d5968cd`  
		Last Modified: Thu, 30 Oct 2025 23:46:11 GMT  
		Size: 15.4 KB (15396 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91-alpine`

```console
$ docker pull rust@sha256:9fd0e182b22d47dd156d65614ded598572c438bc3db79c109c892cd45ab205f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.91-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d8a0b1798b6837e717df2a58ce2f5653c3cf064617ef1345c7fa2e9d83f35044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338571527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c334672aeafb6097099971d43eda27635fb349cd96669fe6b776259c094c0621`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:06 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:06 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:21 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3cfaef0615cb0253cafffaabf7ec4ecc5175443b4ab6064f2e6ee284a050c1`  
		Last Modified: Thu, 30 Oct 2025 21:36:13 GMT  
		Size: 59.1 MB (59143801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9674b249fc5ce80c99c4602fb01c94be64a649a3024dac74778ee94d7db0705`  
		Last Modified: Thu, 30 Oct 2025 22:50:59 GMT  
		Size: 275.3 MB (275289657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:ae5caee0dbfd83810c65df11e27dabf9dcff493e569bade06d6c3cf6dfbe8db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.7 KB (875736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c20db5b6d61ba982bc0de623cef8139d3cca9749848be2c546175c599723f`

```dockerfile
```

-	Layers:
	-	`sha256:240bdbfb8f97567899690facfafee478aa0eea76bee43834ce0e312b2abe7c6e`  
		Last Modified: Thu, 30 Oct 2025 23:44:39 GMT  
		Size: 862.3 KB (862259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f33d22a8ba00cd9de8a1cef55af65f0faaeac769c82fb9d7ff25993b539c3e`  
		Last Modified: Thu, 30 Oct 2025 23:44:40 GMT  
		Size: 13.5 KB (13477 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91-alpine3.20`

```console
$ docker pull rust@sha256:028f385627e06cdb0eca7f662c2850ba734af65b6769551050e3d693ce7afe31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.91-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2b1f24765d5621e41b309cbcf190fad00badbcd79cddcfbcc6e9afb4e74859e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332323361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2be9399e5a5e1241a21bc9d4b6a3fb9a91eda423ff9f867729f1c7d4dd1494`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:32 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:32 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:48 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4701d29124b0199e51ffb3475f695f3b57083f5755bdca3b30b7fb7e41ace7ab`  
		Last Modified: Thu, 30 Oct 2025 21:36:44 GMT  
		Size: 52.9 MB (52945684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7e5474d3d895c6f5799dd4f3bbbdcfa776a9e50f408ba69a4717a2899eb367`  
		Last Modified: Thu, 30 Oct 2025 21:36:29 GMT  
		Size: 275.3 MB (275288300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:2b3d670ab5944d9837c64cdbfd523b88a99f9a56456dd23f8118f9363cc14688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.0 KB (758017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f15731caffee3bf6608f446feff1ee659f031fd1cd8f5b09435eb35688932a2`

```dockerfile
```

-	Layers:
	-	`sha256:6912c322cae1e576478d01096232f97779aa51160ce3cfe9cfaec428fcf894a3`  
		Last Modified: Thu, 30 Oct 2025 23:46:04 GMT  
		Size: 745.8 KB (745792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e187fd7b741e285cb843267475b89466d15f6b182c4390c712e27e84fcf08123`  
		Last Modified: Thu, 30 Oct 2025 23:46:06 GMT  
		Size: 12.2 KB (12225 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91-alpine3.21`

```console
$ docker pull rust@sha256:3b4d4d9c0135f422d65504ff9fa1bc6c9a28b75bbbf442720d7f26fbf19f705f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.91-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a8d313620e805ad10815a56881e538d77f2691f105866bf1c3d06a763c821ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338380943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917e8113aca6a443a4a106b586c655c769fa81ffae061acf9520322b8ca153f7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:33 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:33 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:33 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:48 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108b0b7e1f75a2459f5f726e6189c5c2d3641caf14b00d2ca791da1bf9326c47`  
		Last Modified: Thu, 30 Oct 2025 21:36:41 GMT  
		Size: 59.1 MB (59098892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360f393f0b81dc80a22d0dedab45fc6b4fda056ff253f63643f56d81e2db340d`  
		Last Modified: Thu, 30 Oct 2025 21:36:29 GMT  
		Size: 275.3 MB (275289698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:f0d8e262a56e25c2157fb337c3d8b20dc1db76f484d732577849cca7c8888fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.5 KB (872454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b3ad2c369a7b6bd488f24704a97ec90f0a3318cb7bb60340efe6720f17797e`

```dockerfile
```

-	Layers:
	-	`sha256:4d344bf8bbc4d9656f3eefb11ac3675e925a0a32b5c22728bd7ebc3473c5dc83`  
		Last Modified: Thu, 30 Oct 2025 23:44:48 GMT  
		Size: 860.2 KB (860228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05b732c240fc68ebdbe4f1cdb77483fdc405ee55243fdc8dac13b63d314636a3`  
		Last Modified: Thu, 30 Oct 2025 23:44:49 GMT  
		Size: 12.2 KB (12226 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91-alpine3.22`

```console
$ docker pull rust@sha256:9fd0e182b22d47dd156d65614ded598572c438bc3db79c109c892cd45ab205f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.91-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d8a0b1798b6837e717df2a58ce2f5653c3cf064617ef1345c7fa2e9d83f35044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338571527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c334672aeafb6097099971d43eda27635fb349cd96669fe6b776259c094c0621`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:06 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:06 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:21 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3cfaef0615cb0253cafffaabf7ec4ecc5175443b4ab6064f2e6ee284a050c1`  
		Last Modified: Thu, 30 Oct 2025 21:36:13 GMT  
		Size: 59.1 MB (59143801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9674b249fc5ce80c99c4602fb01c94be64a649a3024dac74778ee94d7db0705`  
		Last Modified: Thu, 30 Oct 2025 22:50:59 GMT  
		Size: 275.3 MB (275289657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:ae5caee0dbfd83810c65df11e27dabf9dcff493e569bade06d6c3cf6dfbe8db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.7 KB (875736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c20db5b6d61ba982bc0de623cef8139d3cca9749848be2c546175c599723f`

```dockerfile
```

-	Layers:
	-	`sha256:240bdbfb8f97567899690facfafee478aa0eea76bee43834ce0e312b2abe7c6e`  
		Last Modified: Thu, 30 Oct 2025 23:44:39 GMT  
		Size: 862.3 KB (862259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f33d22a8ba00cd9de8a1cef55af65f0faaeac769c82fb9d7ff25993b539c3e`  
		Last Modified: Thu, 30 Oct 2025 23:44:40 GMT  
		Size: 13.5 KB (13477 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91-bookworm`

```console
$ docker pull rust@sha256:1799e112d1f0b81caf2dc0c3e9cc40f1279b1ff2747db9557bfb0c17eb7a751b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.91-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:051b0136c8a4e3e112b39e508921112fbde875a02b07b38c87a737e1e81cc746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.1 MB (559108573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be8e386e015e2bb88eaa00172139beb421d17d3570f6121a8fb2dbe27f2e20b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:35:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:42 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178651637d26f6ae6fc6c2a3297b37f8bbef12e80d822930b05b14f51a262382`  
		Last Modified: Tue, 21 Oct 2025 02:43:48 GMT  
		Size: 21.9 MB (21934505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14411cad8875b2a42f951ec95179ed8a844d1522990ec8b96f1c4d269ce3c71f`  
		Last Modified: Tue, 21 Oct 2025 04:11:04 GMT  
		Size: 59.7 MB (59652688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934fb9fcc0f174aa356a518c85a7e2e8a62dd5902afe2a8dbbf58f5f8b37166b`  
		Last Modified: Tue, 21 Oct 2025 06:17:29 GMT  
		Size: 175.4 MB (175355007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a2122d86f314de64147fdae6b5b37d7b95098ae45f73107f366595e6097bc`  
		Last Modified: Thu, 30 Oct 2025 21:36:31 GMT  
		Size: 258.0 MB (257970463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:29db2457c6db102e7a390b4609d14f799d0b4dc98f04e20b278bee9349696010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15685187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840c6decc4d442f284b6c01b397281e4a69f76e76b12d384284a4eb807702448`

```dockerfile
```

-	Layers:
	-	`sha256:8db0f390e801710744db2d01b0058a149ac8d4833025dd5538c43e761de709dd`  
		Last Modified: Thu, 30 Oct 2025 23:45:19 GMT  
		Size: 15.7 MB (15671436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd29c41b660a030fe351fe27c96ba66c2b369e2fa4d46468e264be654f4fc10a`  
		Last Modified: Thu, 30 Oct 2025 23:45:20 GMT  
		Size: 13.8 KB (13751 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b5ea992358738c5ac3d06cafcd8f8274a36b77738ff7c8ac37828322399a6c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.6 MB (519553946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4518efce2e74532fa1aab649f80dd367117838d24a5a2c3caeba50ab3d523197`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:56 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:56 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15270faa4e93fc4bcc62caecce8d2f5dfc1443d3c99572dfb689973b24c0a4`  
		Last Modified: Tue, 21 Oct 2025 02:35:23 GMT  
		Size: 64.4 MB (64370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6803b5e31b40492f4747e974e6e4ae692982b12beb2b87ed9d9ffbdaedefcfd4`  
		Last Modified: Tue, 21 Oct 2025 04:13:43 GMT  
		Size: 203.0 MB (202958684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3099636657b1560c5cdee62a47498eec65574f75745e2e59dbe17331d4c6cedd`  
		Last Modified: Thu, 30 Oct 2025 23:48:57 GMT  
		Size: 180.3 MB (180267344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:eb1282379cca9bd583c19b02bb212db62b40aedd81ce17ed2fb038637a279a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15911254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee670b912d558498da8a680449137c57f480fd39afb5dcb916fa1b657838370a`

```dockerfile
```

-	Layers:
	-	`sha256:310f60a24c03dd47886646e436808491680a7092f501e1625c0b0137803aca44`  
		Last Modified: Thu, 30 Oct 2025 23:45:35 GMT  
		Size: 15.9 MB (15897478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f59b3162dc6c5eae0e6dc9c486d6af675e4ee71d672067d47e274f3c0c9d0fd`  
		Last Modified: Thu, 30 Oct 2025 23:45:36 GMT  
		Size: 13.8 KB (13776 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-bookworm` - linux; 386

```console
$ docker pull rust@sha256:3df2b6dd56af4590d062038eb7ea187a744fdaf081514e183042ff7d02854301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.9 MB (588911073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e8ebf3e452e9009e6ac8977f62eeb4677af9d14fe10adff5b5a5229350c519`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3426ba65368da59a25d050cab9d7713d7873264014ab6dfaa6b0c33f0632cb80`  
		Last Modified: Tue, 21 Oct 2025 00:20:21 GMT  
		Size: 49.5 MB (49466720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f14d3e3fda83046fcd165bb976221020273830b54d963f634e53e7796b47053`  
		Last Modified: Tue, 21 Oct 2025 01:52:59 GMT  
		Size: 24.9 MB (24864208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39058bc352da86cee9643b9b447133a3295983ec455cdba2fac6cbbed8726db6`  
		Last Modified: Tue, 21 Oct 2025 02:35:47 GMT  
		Size: 66.2 MB (66231902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed15f8c1488a55d242a6bf3226b75c0d0de56631f3ea18bb327cec39013003bd`  
		Last Modified: Tue, 21 Oct 2025 04:13:40 GMT  
		Size: 210.4 MB (210381245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284a00e05bc16cf43c2f874e7ffa10dfd7a2b9db4a6677907e35dd79fe9a958`  
		Last Modified: Thu, 30 Oct 2025 21:36:44 GMT  
		Size: 238.0 MB (237966998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0599233bf7ca1dbdaf9211ea1d633238a82678ba0c72f9df870614f4db971837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15859504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ad9e5af8c0e73f8cbf71baff9a986c09dce838cd776e52aef2bf3deb361ccd`

```dockerfile
```

-	Layers:
	-	`sha256:4507749c6cb049d9b9929284ce90ffcbb7ec4eb94fb4c9c0262e135f7fc1071f`  
		Last Modified: Thu, 30 Oct 2025 23:45:50 GMT  
		Size: 15.8 MB (15845864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e4d18122dd7bb11ec0aa43861a1fc3f5cff14e9b8487a97a8493193a79c5282`  
		Last Modified: Thu, 30 Oct 2025 23:45:51 GMT  
		Size: 13.6 KB (13640 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:697ff40e2e322426b97c54857174bef11b523a775040bd451466892908de2bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.1 MB (615060656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4faa2b9c9fb04ed6c7fb91522e3b4ad2232170657cc84637e5cca4b424cfd02a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 22:39:51 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:39:51 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:39:51 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca271e8b0e27269a77c65ea555986eaaadf5db02b1ac24f66f8ce2e45a475b`  
		Last Modified: Tue, 21 Oct 2025 22:50:23 GMT  
		Size: 24.0 MB (24027291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944e6bdda425b877e973cde5b6c8eeabf7eed45bfaba0fd705b4f180a07f001f`  
		Last Modified: Wed, 22 Oct 2025 06:00:23 GMT  
		Size: 63.5 MB (63501423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7d40c47b93ce5dc5166e5aa44baae913a478ae1ba5f7865fe24556acef9200`  
		Last Modified: Wed, 22 Oct 2025 14:21:48 GMT  
		Size: 183.5 MB (183485270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1617ee534ab322072d5a49e5b16309a0c49cf8b0232baabd7f545d5675371d`  
		Last Modified: Thu, 30 Oct 2025 22:43:17 GMT  
		Size: 296.9 MB (296909151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:478d1ea453072bde935424c02d4c412b2552cb3b6f3802e364b9daa69bb78b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15690219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9dc7449fb5d0d433daa7aa7b48a617e07616fd804e869aa43d91049e329468`

```dockerfile
```

-	Layers:
	-	`sha256:e5617194576bbf4d19500cc175ba3bdd7dc056a09db6529ed35a8a3df0ebac65`  
		Last Modified: Thu, 30 Oct 2025 23:46:22 GMT  
		Size: 15.7 MB (15676546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f013fc0c2ae0f7a32936873b795b686a9fe5f9867e41c993b818dbda395aa7cc`  
		Last Modified: Thu, 30 Oct 2025 23:46:23 GMT  
		Size: 13.7 KB (13673 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91-bullseye`

```console
$ docker pull rust@sha256:84653a7bcf40cb6085bb0f4f6b106c29025d35a022481100cb2e4da62448b4d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.91-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:4debe238b6bccd468958311c5ee086154be57fe1f47fb1e17e9a3357f90139be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.5 MB (540499385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a512f11edcf77ed82a2ac07b66308eaf931cc80877cb617b60b8f763011be2f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:35:30 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:30 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:30 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:680ed921e0c94a719af1d242eac2d0c1be8482153680a3940f3435ee5598303a`  
		Last Modified: Tue, 21 Oct 2025 00:20:24 GMT  
		Size: 49.0 MB (49046121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c68013a317d7d802bb25c57a724c8753caec2fc7f0e78fc13f9a38fd22ecd4`  
		Last Modified: Tue, 21 Oct 2025 02:44:25 GMT  
		Size: 14.9 MB (14879264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895fddf2807e047e5b02e5418fd04d343d3e9b5b393b2f3f0cd6704cad44b8f0`  
		Last Modified: Tue, 21 Oct 2025 04:10:49 GMT  
		Size: 50.6 MB (50628495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ef331acdad14a3d1bfe859a1c645cb9f4b9526e16e3fed550eee6b86681db7`  
		Last Modified: Tue, 21 Oct 2025 06:17:35 GMT  
		Size: 168.0 MB (167976463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2345c283f9f7c727f33c6a1e2c5ffa229106bb1e7b3f3f2073146f627866f815`  
		Last Modified: Thu, 30 Oct 2025 21:36:20 GMT  
		Size: 258.0 MB (257969042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f6a16886d335243aaaf88af9f27e0a70520e083485569ce2cca1c2bdd490b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15275978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f206f730d7eeec8a3b422fc88a2602f2e8f4d5d0542c706027b0a2fe2928a2b1`

```dockerfile
```

-	Layers:
	-	`sha256:69bab675147da3f449e5f163a075b2d55e9aa4ed4021b6e356a242df2ef4a59a`  
		Last Modified: Thu, 30 Oct 2025 23:45:27 GMT  
		Size: 15.3 MB (15263395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac6fc96e9abd4822cf5b32fc13e672b114ae72330f34d3a5301f3009e139e4b0`  
		Last Modified: Thu, 30 Oct 2025 23:45:29 GMT  
		Size: 12.6 KB (12583 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bdd72efd5f91a90aa1746b27a7cd1cc1ea77ae0606dc1e0bb9ea3fb1c4adb42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.2 MB (493232128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a548930c92a6745dcce895941534ec91e5af27593c0ae426e760e382ee6bcf7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:39 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a72c4e347b74aa6a0086cf3d1d928528ab02577a17bff4e22366a7df681f564`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 52.3 MB (52257444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f7bdca064e682157394f36dabd112bc9831aff9743216b035e2ccccf704cc3`  
		Last Modified: Tue, 21 Oct 2025 01:46:24 GMT  
		Size: 15.7 MB (15749510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc7a49f7691cb1ac5f0f40edbe6f4beec62021b4fd2544c431d8f694b4b4647`  
		Last Modified: Tue, 21 Oct 2025 02:35:21 GMT  
		Size: 54.9 MB (54860806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0452b809e62b80ba90b1a217898e5cf7675ff6aac67b2967e58600172590649e`  
		Last Modified: Tue, 21 Oct 2025 04:14:12 GMT  
		Size: 190.1 MB (190097178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1493ba40974f9698cde6967247a220e8b21c09de76901470d4a5ed125bfc1cb2`  
		Last Modified: Thu, 30 Oct 2025 21:35:20 GMT  
		Size: 180.3 MB (180267190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:174a6996165236196e2e2234b5a3e3fd65d247300e29913fdf2df1ee0adea225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15478629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e3fdfeaf6bf3fc08da419feb6196d81eb718e95950ce77f11a97ffb49dcb98`

```dockerfile
```

-	Layers:
	-	`sha256:9196d2d341db75ce952d1a4e29bd491214fe5bb55b9f55a90c7343d81100d44d`  
		Last Modified: Thu, 30 Oct 2025 23:45:42 GMT  
		Size: 15.5 MB (15466022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915a2f913a028e29271d667bf808cdabccd5dc980730eeb68ed9556c1750d267`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-bullseye` - linux; 386

```console
$ docker pull rust@sha256:ebfb2e206c2b74a1bb2d9b549cf50bddf2c1313e09fabb019c831ae5f7495a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.1 MB (565086977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0f7bf5bc46fc016e2a1fbd23835673151045c1b511f6c146c2dd9d721eef6c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:32 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:32 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:10d430deaa3d2ab4898db053e80d62403503897839bf6efd17ed5412b18d7973`  
		Last Modified: Tue, 21 Oct 2025 00:20:39 GMT  
		Size: 54.7 MB (54699294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c453fe6b4c7a680d5464137a3450d263e01a7ec4d491659295432d36b0198bbc`  
		Last Modified: Tue, 21 Oct 2025 01:53:19 GMT  
		Size: 16.3 MB (16267847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96adc169c4af311ffba07fa68db5821d6b9b00d285e00f44dad87eff52496658`  
		Last Modified: Tue, 21 Oct 2025 02:35:42 GMT  
		Size: 56.0 MB (56048779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd845a5707f187f6670f0831bc55034f6333f3aa3eede705f688f3c3342392e`  
		Last Modified: Tue, 21 Oct 2025 04:14:36 GMT  
		Size: 200.1 MB (200103484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae4b0e0faf517253d9eb9d5185f476ec1cdfd4f000a81910c9827c0acc7d451`  
		Last Modified: Thu, 30 Oct 2025 21:35:16 GMT  
		Size: 238.0 MB (237967573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:66f198e4ca90d5791b0a7ff640ee5c546edbfd2e0dfeb179fb4f174b4be5814e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15463224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d7dafb0e855c67125a259fe625f7a9d7f828eb79aad926e34bbb81d981988c`

```dockerfile
```

-	Layers:
	-	`sha256:1b2ab51fb7cebaa093a1da9d9de0794786d042ff60414a0211a492701aab92a9`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 15.5 MB (15450753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fd7b2b4922a57612d543c90720e157bdeb2bd2a9b6c5aa37cafabc33a2328f0`  
		Last Modified: Thu, 30 Oct 2025 23:46:00 GMT  
		Size: 12.5 KB (12471 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91-slim`

```console
$ docker pull rust@sha256:2b4610b8bba6b252286b4e7d3a9fce4d66f7e6bf7d4cbb6ab1b127649bb4bdcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.91-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:36bd228e236519c3a747a87570e7f83dab399d17eca3ef372e6484c3055c6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334448212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c202a0d535ea0887983203aae69fdf71f527951cf86b2b21f3fb6c2cf9a538`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:37:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:37:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:37:12 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6e00fb9e9c84f34ed2d592246743cef540466ac4115722b315d862bccdbb44`  
		Last Modified: Thu, 30 Oct 2025 21:37:57 GMT  
		Size: 308.2 MB (308235318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4e20e1ca9b0f23d783ec6d6ed5be8fa58ddaf53b726d80cd6fe80cf82a708eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b868546b1ef1b0edf1d23ec51f66614251da1094f46405866d3bf09b052aecad`

```dockerfile
```

-	Layers:
	-	`sha256:14738f7012d7020bd06896025d57d8d8f840e853cca38898526091bad7f49804`  
		Last Modified: Thu, 30 Oct 2025 23:45:32 GMT  
		Size: 4.0 MB (3969887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da73b8e3cdf4379799012870a7c21e494173161ddc8b1b353fc501f5632e4cf`  
		Last Modified: Thu, 30 Oct 2025 23:45:33 GMT  
		Size: 15.7 KB (15744 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8f015c79dd7ae0d1ab3218f86dda57f805a046991a5a67aa40088a67965806e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280064640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ccfb92e01921c8ed8fe03746498812688fe017b71f41f9e31a6cea79147abe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9e403b0cf550d52dedd0ab0aa7cbdcdd11f44b28ceb00d624c5c3d50a41df8`  
		Last Modified: Thu, 30 Oct 2025 23:47:09 GMT  
		Size: 249.9 MB (249922513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim` - unknown; unknown

```console
$ docker pull rust@sha256:cc442428572057302c62370a3c8514cb787a1a7daeed774b9f01e3a53f53d5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96a2c18c7d5bc0df280a6b286dc537b572cbe31668fcf2ad169f1bdf85194d`

```dockerfile
```

-	Layers:
	-	`sha256:606f393a1954d59bcd6d8915d68d376cd05d29024f9a559d92c8ad47da7baa53`  
		Last Modified: Thu, 30 Oct 2025 23:45:37 GMT  
		Size: 4.3 MB (4256227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32db46c306be7344e9ad5e0d189a1f9fccfa49d28d6336ecf1d9609a07d3da88`  
		Last Modified: Thu, 30 Oct 2025 23:45:38 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-slim` - linux; 386

```console
$ docker pull rust@sha256:ef194da922ba0594e7b7ddf8676004948a82926c4d57ac47bf5a47d85b43d571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341758796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4548274d12a2843de650e527ef6fbf4c3a6d29412091c3b2129c37809a899eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:52 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e995015b3e24125a0c10003ec7b1e384ce24f06f88cbd49bce3e36d2e4ffd8f`  
		Last Modified: Thu, 30 Oct 2025 21:36:35 GMT  
		Size: 310.5 MB (310464168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim` - unknown; unknown

```console
$ docker pull rust@sha256:5a52de8d007cb783912f98e3a2bc9ef1bea117a247b300d3bf0ed25db3ef7b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05360c911e791bc9a471f2026d992be7509b06ede83672b314adfab6d540bf4b`

```dockerfile
```

-	Layers:
	-	`sha256:657d29bb5c22513fcfdf6fccc85d309ca3ac85cc4258c72801d105ab1c31c57a`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 4.1 MB (4138524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed724e78f81430b3f4c6c9bf61b7039d1389fa37f5495feb17edb5614799f43`  
		Last Modified: Thu, 30 Oct 2025 23:45:44 GMT  
		Size: 15.6 KB (15579 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-slim` - linux; riscv64

```console
$ docker pull rust@sha256:aaf1ec04eb2b47005e3b8560b0ab3fa83b42cb6b8c8cd6c6eb55a3c1ca29fd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 MB (391690936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd90d32888708414dd2407217bdbeb9884c97b7b7c8bf613038f97a472c8c4f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:00:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:00:19 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2315ad783eb28b652f5440fe195ec3068e8c8429c644f9745c84f8c522147`  
		Last Modified: Thu, 30 Oct 2025 22:12:21 GMT  
		Size: 363.4 MB (363415286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b085520540a279fab989fbd055fdff984bfe91d00f603dc6d9c1ee6747d497ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cc7bb3bca0e889b9a141380fcd0cf516a70126219e8fbac44ce160e69a9225`

```dockerfile
```

-	Layers:
	-	`sha256:e20ad570b9c4befd769026dc8b5716c3cf74fc0c6bdbddae3ab6e42e13ccdf5e`  
		Last Modified: Thu, 30 Oct 2025 23:45:53 GMT  
		Size: 4.2 MB (4239428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8670d848e45c5e062ecf29084ab05335daba00c88a567e96c2cc5fca9b04fbe3`  
		Last Modified: Thu, 30 Oct 2025 23:45:54 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-slim` - linux; s390x

```console
$ docker pull rust@sha256:38ebb79c4b041ab046e504b5de098381f8027201a2594744a1eb1fecba242ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.1 MB (379117853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd57e4210e0c402a7b13d84e7dbf8a58418c9777b67aa36fa3c2222c9bae1144`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:54:35 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:54:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:54:35 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9805f4fca0189a31ca7f470c6efdd8dd933a751f5e840c7dbe3eb3034acef906`  
		Last Modified: Thu, 30 Oct 2025 22:56:45 GMT  
		Size: 349.3 MB (349280598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim` - unknown; unknown

```console
$ docker pull rust@sha256:e2b502b6ae9b904b73922a60e8ebe8814262ef8cb49c465af48c8494dbd80fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5388a6f6d7beec83a26ed19423edba57454d4145bb7d7f5aaefbf1faaa6eb99d`

```dockerfile
```

-	Layers:
	-	`sha256:51b388bf3623dd03362dcb15f7452b4677d633e967a003b3bc39faf47e960502`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 4.0 MB (3982759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a69eb51b743dde6eed89af2bfc049b12313cde5e899319a66fa67ebbb2c5ac`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91-slim-bookworm`

```console
$ docker pull rust@sha256:1c2b169164fcaa923f6ff28a4af74b9955c548e9924c1b4945758d3ba886a483
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.91-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:1a66676e5c0a918aa45dc2fd4f34c16341d8bd0d064bcb7d815d84948da34398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329757809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c700e6793c04e8485ea32a54a1c3181ceb258694c1ee891dbaa530f552a2137`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 21:35:35 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:35 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb5b7bfc507827968f205851cea67b7a646a133c9116ec8737777be53b48787`  
		Last Modified: Thu, 30 Oct 2025 21:36:19 GMT  
		Size: 305.8 MB (305823786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4d727c9416ea7aa7accb2b6d82a1f1de5c78dc426821a57097eada3482d424d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3389581a9eef53aef89c9fe9accc7fed4cb4a49b423420c31e055cb167a7c7de`

```dockerfile
```

-	Layers:
	-	`sha256:9a1821533a3548a60f32478502545e387b5512c73dc2ef81518a839c820dfd39`  
		Last Modified: Thu, 30 Oct 2025 23:45:42 GMT  
		Size: 3.9 MB (3909876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6ed7f684cc050dc1b7ba74ce805f9039dbc61ddf92e8fe680bdb0a148f49b5b`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 14.0 KB (13964 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:756adb3f9d5c27df7bda4994157cb1cdca4cfdf76b8067a906ce5ff86976859e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274222169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0949ace3836ff38d491823d42f6201e9900fc4d22cf7a1b5d1e486cb355cdd9f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 21:35:36 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:36 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:36 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1f6c6c415a2d4c2edb9805e85b4dd69f95451b08268ffadfa1cdc061e695e0`  
		Last Modified: Thu, 30 Oct 2025 21:36:13 GMT  
		Size: 246.1 MB (246119979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:26a1086edf6420fbae6f26d20f0a2e8dca444eece965956194efe35e03d12a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b8fa2cd2b51fd9918b40c6c59ef73fac18d50aeb2bda9819c79a14219bcd30`

```dockerfile
```

-	Layers:
	-	`sha256:49e6348f3e8ffeac0bcd864980bf5f66c031fe768ed1d3c96c76d88dc7d4580f`  
		Last Modified: Thu, 30 Oct 2025 23:45:49 GMT  
		Size: 4.1 MB (4117775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90e56046bfcea1eefde6da940a766b28525d88059af7258ec565aa8e2c50f09a`  
		Last Modified: Thu, 30 Oct 2025 23:45:50 GMT  
		Size: 14.0 KB (13988 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:8ee0bf09c075a2f76ab2a753178a50023da8354eaa3066be15ae6df16b40eb26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.8 MB (334773527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f02408a764c4d03ef0ac688ee39de788035eb1fc14f6701fc34b094b37ec2a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df86e57d1d11515507bced15d2c5b47745ef47d90bf56ccfea3ffeb9852fdea4`  
		Last Modified: Thu, 30 Oct 2025 21:36:42 GMT  
		Size: 305.6 MB (305563849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4c7086dfaf26b09349225db4c780cf050cd5c0c5587f443eb99860dab7dcc2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4088714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ca752b45a8a21a6be117b63b2108326231dbd39bf5ad0f1421afa525c16f0f`

```dockerfile
```

-	Layers:
	-	`sha256:41e7bf57a66535222d70a721ed5c6d7627a2529faa2fa47097ea4924980ffe34`  
		Last Modified: Thu, 30 Oct 2025 23:45:56 GMT  
		Size: 4.1 MB (4074862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d529607b7e48cf2c2deba92ff2676f549bc263c168014cc85eaccd836f9b478`  
		Last Modified: Thu, 30 Oct 2025 23:45:57 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b5ae74b41977de30791004301b9a55684a4a354fbbfe5a46fd7c412a1db484b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.9 MB (373924203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c02d1953e53a49919fdf3212d3b0191ff68e4b62f8b6cd5875592f08ab9f534`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 22:45:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:45:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:45:13 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:43b0f588b497b17691a3547afa4ae41853829cffde6930e6425ddae4a3f89278`  
		Last Modified: Tue, 21 Oct 2025 00:21:28 GMT  
		Size: 26.9 MB (26884356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ac26cb25e9079f7df28678594c9546404a88850ef59d1906cdae0af1834af2`  
		Last Modified: Thu, 30 Oct 2025 22:47:19 GMT  
		Size: 347.0 MB (347039847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ca7ec822c8eac17e6a09f4496f9ea73f7f5cf4a227037de86239e19824a01cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7bdc57546b9d419b45fd2009461ac7feb00999dd5424e0861ae69445408a1d`

```dockerfile
```

-	Layers:
	-	`sha256:a163636249f2f57c519801b581ece738bbca25c2502343f983fc21023358dc51`  
		Last Modified: Thu, 30 Oct 2025 23:46:05 GMT  
		Size: 3.9 MB (3933157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4082065c8b0d4a306a1d88f8e5c972213af58b5b72c4f05bb1bdf4f35a0db44`  
		Last Modified: Thu, 30 Oct 2025 23:46:06 GMT  
		Size: 13.9 KB (13884 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91-slim-bullseye`

```console
$ docker pull rust@sha256:b9f673be74dc9469a3802a767dc3601ed64553a0df026e9124076e6b60e80919
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.91-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:13fc3a2170515d49a864808c172e6ef2cdb6ceb7d516c49d43f25dc6d7220aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325804399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e041264a283725f3e8d0e27bf0c41b94d5c1f7a4f0ad080f4bab768ec221cd17`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 21:35:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:42 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4b897c04dec26603bcc1b01b4283220cd1ffb208f0ec4c0db9e08dab58fcfb5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 25.5 MB (25546187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f470db143d0044ed53ee3c62d37c264ce9347606e374e60113030bb748254e`  
		Last Modified: Thu, 30 Oct 2025 21:36:25 GMT  
		Size: 300.3 MB (300258212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:80c8d376c747cb7f8555437910e6c9a1add734f8d43488803a7fbb48d5300c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cb2dd69accf11a0b247c6ebd6851c11ca87d48376f5b4c43e55069d8779493`

```dockerfile
```

-	Layers:
	-	`sha256:3886373e00abc1e6f64ba5c91f674e54b4699c88fafb62b650aaaf8da12bec8e`  
		Last Modified: Thu, 30 Oct 2025 23:45:53 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea67c0e765b1816115cb1b8753a4b992d18c1f0dbe17cbdafddb31a15734a966`  
		Last Modified: Thu, 30 Oct 2025 23:45:54 GMT  
		Size: 12.8 KB (12794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7ff887fd3eb13d26eecb0f40398028fdc12a3298ef48c8528331016decfb0ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264715851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ae94dab2b12284d1f2e92e3e2ac7b56eff6bb02864e3639caa14c43b4390fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 21:34:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:39 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db337e821e80e597fa142716f1cb02566d2cf4168196f5f08a415cfb4a249b7`  
		Last Modified: Thu, 30 Oct 2025 21:35:15 GMT  
		Size: 236.0 MB (235967450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f46b8601c7c669072e496b7807335af3362860103487ba6340ac14700e4d2e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3c48bda2928a06b24f54d0c55cb10592408f842b75a6984f01eb69ebb7f065`

```dockerfile
```

-	Layers:
	-	`sha256:ab6b83830f27e4a54af4a4ff3428fe72f6898a17d7e3c21d3a7b6165de49140c`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4018ce6087359d14714e6bcbfbfdc372aa884d3abeff3000503021a2c3381d0f`  
		Last Modified: Thu, 30 Oct 2025 23:46:00 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:a8c4281836aee33f681efe73b74c2fe608821ab8a79e1e4f53c408cbee6a616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329920628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44d16d04c4e9d940226b9321174f5ada41cc3046700d8f53b9f75357436b02a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 21:35:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:04 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ed9b7a4c5998c0d248e37f414fa0883c2b695df7b879c0ba096280f29fcb2660`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 31.2 MB (31191494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8bca4c0d96694e3d489bc0df62c181f63f68bd29966b3d385296b7f25514f0`  
		Last Modified: Thu, 30 Oct 2025 21:35:46 GMT  
		Size: 298.7 MB (298729134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8220d5bc4c59b662f331a750b1c3e053eb553fcf58d971daa7ceda6433fac105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ee75a2e521250b772ff737b27beb9860a1292184f784af6f4e157e5a734559`

```dockerfile
```

-	Layers:
	-	`sha256:5ee000ac8ab06e33a71014e51eeb45b60c7820fd0d03e45c9fd2b1573f530073`  
		Last Modified: Thu, 30 Oct 2025 23:46:05 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fb44d48fb78f0b88ebc033734c23af5eb6f66040ca67ec8536dcd1a1755ed6f`  
		Last Modified: Thu, 30 Oct 2025 23:46:06 GMT  
		Size: 12.7 KB (12682 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91-slim-trixie`

```console
$ docker pull rust@sha256:2b4610b8bba6b252286b4e7d3a9fce4d66f7e6bf7d4cbb6ab1b127649bb4bdcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.91-slim-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:36bd228e236519c3a747a87570e7f83dab399d17eca3ef372e6484c3055c6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334448212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c202a0d535ea0887983203aae69fdf71f527951cf86b2b21f3fb6c2cf9a538`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:37:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:37:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:37:12 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6e00fb9e9c84f34ed2d592246743cef540466ac4115722b315d862bccdbb44`  
		Last Modified: Thu, 30 Oct 2025 21:37:57 GMT  
		Size: 308.2 MB (308235318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:4e20e1ca9b0f23d783ec6d6ed5be8fa58ddaf53b726d80cd6fe80cf82a708eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b868546b1ef1b0edf1d23ec51f66614251da1094f46405866d3bf09b052aecad`

```dockerfile
```

-	Layers:
	-	`sha256:14738f7012d7020bd06896025d57d8d8f840e853cca38898526091bad7f49804`  
		Last Modified: Thu, 30 Oct 2025 23:45:32 GMT  
		Size: 4.0 MB (3969887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da73b8e3cdf4379799012870a7c21e494173161ddc8b1b353fc501f5632e4cf`  
		Last Modified: Thu, 30 Oct 2025 23:45:33 GMT  
		Size: 15.7 KB (15744 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8f015c79dd7ae0d1ab3218f86dda57f805a046991a5a67aa40088a67965806e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280064640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ccfb92e01921c8ed8fe03746498812688fe017b71f41f9e31a6cea79147abe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9e403b0cf550d52dedd0ab0aa7cbdcdd11f44b28ceb00d624c5c3d50a41df8`  
		Last Modified: Thu, 30 Oct 2025 23:47:09 GMT  
		Size: 249.9 MB (249922513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:cc442428572057302c62370a3c8514cb787a1a7daeed774b9f01e3a53f53d5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96a2c18c7d5bc0df280a6b286dc537b572cbe31668fcf2ad169f1bdf85194d`

```dockerfile
```

-	Layers:
	-	`sha256:606f393a1954d59bcd6d8915d68d376cd05d29024f9a559d92c8ad47da7baa53`  
		Last Modified: Thu, 30 Oct 2025 23:45:37 GMT  
		Size: 4.3 MB (4256227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32db46c306be7344e9ad5e0d189a1f9fccfa49d28d6336ecf1d9609a07d3da88`  
		Last Modified: Thu, 30 Oct 2025 23:45:38 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-slim-trixie` - linux; 386

```console
$ docker pull rust@sha256:ef194da922ba0594e7b7ddf8676004948a82926c4d57ac47bf5a47d85b43d571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341758796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4548274d12a2843de650e527ef6fbf4c3a6d29412091c3b2129c37809a899eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:52 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e995015b3e24125a0c10003ec7b1e384ce24f06f88cbd49bce3e36d2e4ffd8f`  
		Last Modified: Thu, 30 Oct 2025 21:36:35 GMT  
		Size: 310.5 MB (310464168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:5a52de8d007cb783912f98e3a2bc9ef1bea117a247b300d3bf0ed25db3ef7b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05360c911e791bc9a471f2026d992be7509b06ede83672b314adfab6d540bf4b`

```dockerfile
```

-	Layers:
	-	`sha256:657d29bb5c22513fcfdf6fccc85d309ca3ac85cc4258c72801d105ab1c31c57a`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 4.1 MB (4138524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed724e78f81430b3f4c6c9bf61b7039d1389fa37f5495feb17edb5614799f43`  
		Last Modified: Thu, 30 Oct 2025 23:45:44 GMT  
		Size: 15.6 KB (15579 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-slim-trixie` - linux; riscv64

```console
$ docker pull rust@sha256:aaf1ec04eb2b47005e3b8560b0ab3fa83b42cb6b8c8cd6c6eb55a3c1ca29fd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 MB (391690936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd90d32888708414dd2407217bdbeb9884c97b7b7c8bf613038f97a472c8c4f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:00:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:00:19 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2315ad783eb28b652f5440fe195ec3068e8c8429c644f9745c84f8c522147`  
		Last Modified: Thu, 30 Oct 2025 22:12:21 GMT  
		Size: 363.4 MB (363415286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:b085520540a279fab989fbd055fdff984bfe91d00f603dc6d9c1ee6747d497ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cc7bb3bca0e889b9a141380fcd0cf516a70126219e8fbac44ce160e69a9225`

```dockerfile
```

-	Layers:
	-	`sha256:e20ad570b9c4befd769026dc8b5716c3cf74fc0c6bdbddae3ab6e42e13ccdf5e`  
		Last Modified: Thu, 30 Oct 2025 23:45:53 GMT  
		Size: 4.2 MB (4239428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8670d848e45c5e062ecf29084ab05335daba00c88a567e96c2cc5fca9b04fbe3`  
		Last Modified: Thu, 30 Oct 2025 23:45:54 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-slim-trixie` - linux; s390x

```console
$ docker pull rust@sha256:38ebb79c4b041ab046e504b5de098381f8027201a2594744a1eb1fecba242ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.1 MB (379117853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd57e4210e0c402a7b13d84e7dbf8a58418c9777b67aa36fa3c2222c9bae1144`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:54:35 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:54:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:54:35 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9805f4fca0189a31ca7f470c6efdd8dd933a751f5e840c7dbe3eb3034acef906`  
		Last Modified: Thu, 30 Oct 2025 22:56:45 GMT  
		Size: 349.3 MB (349280598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:e2b502b6ae9b904b73922a60e8ebe8814262ef8cb49c465af48c8494dbd80fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5388a6f6d7beec83a26ed19423edba57454d4145bb7d7f5aaefbf1faaa6eb99d`

```dockerfile
```

-	Layers:
	-	`sha256:51b388bf3623dd03362dcb15f7452b4677d633e967a003b3bc39faf47e960502`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 4.0 MB (3982759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a69eb51b743dde6eed89af2bfc049b12313cde5e899319a66fa67ebbb2c5ac`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91-trixie`

```console
$ docker pull rust@sha256:eac325268dbdd1c874282a92ad2e0012f19005f65732f9828ecb077c1065c0f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.91-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:df192b38e9142bc8d454be61de04235e6e3d6e3cc142b3ca4461565fdcdb5c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583252486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a735b8020181b775c6ff35bd4f4ddaf6fccacf90d6baef0e5b88f5fac468e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:20 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:20 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:20 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cda7f0b38d756bba039d1251605b315c32a18bef1d71d1a0a98df8f4c7fb6`  
		Last Modified: Tue, 21 Oct 2025 06:18:01 GMT  
		Size: 193.2 MB (193235864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7085e104656ea6c66d8ba95df53b71fae0ae8c42dce84c36d3dd51cc63114cc`  
		Last Modified: Thu, 30 Oct 2025 23:48:47 GMT  
		Size: 258.0 MB (257970062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:7bdc29f59dfa654c3d2300e1d752366f54275c8759cf65ee11f3b51b5ee02ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b60585f52529edd183ac79b90c91a6c5c7a9f7718df436557b6c48120de964f`

```dockerfile
```

-	Layers:
	-	`sha256:e7514cf6a08ba2c22ef71f6054b5e755385f65048788dccfe2a655928e7613af`  
		Last Modified: Thu, 30 Oct 2025 23:44:49 GMT  
		Size: 17.0 MB (16977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7716c3ffa9ab429830b3182885b3f920b00e895ca1ca6dc9aa0e0866b3405617`  
		Last Modified: Thu, 30 Oct 2025 23:44:50 GMT  
		Size: 15.5 KB (15508 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:69d4bc701fcca1d78e46d634aca8f1b0a3b967b755e87d0c3e883abf402a92c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.6 MB (548594894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124905d571200dee29c0250b5a56242cbb369d8d6a2f46770ef2060b9aa6ae19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:13 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f695ddffd81064f15ea19428e2d643e8b560e48e54ae801a8d63c45ad6ac29`  
		Last Modified: Tue, 21 Oct 2025 04:14:42 GMT  
		Size: 226.1 MB (226078014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b0009962587465f15c28cbaa4e05bede4600a6b68c86467eb69e4227df6c84`  
		Last Modified: Thu, 30 Oct 2025 23:44:37 GMT  
		Size: 180.3 MB (180266565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:a2ff1f30c17e94d0edaf28e068fd1a99b76f759cebd6a2b304606e7c085f21aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17309822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d625100634edff47e63fc8b469129a68a25115bad3e0531a1f7b594067d865`

```dockerfile
```

-	Layers:
	-	`sha256:b3eb795d70d03f35b63225b01143c51f0f8b6622f4022cb5db697d2ba9e108d7`  
		Last Modified: Thu, 30 Oct 2025 23:45:11 GMT  
		Size: 17.3 MB (17294274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f42745a111fee91795bb40aa7014469e06556069a7271890a09e381d064bfc`  
		Last Modified: Thu, 30 Oct 2025 23:45:12 GMT  
		Size: 15.5 KB (15548 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-trixie` - linux; 386

```console
$ docker pull rust@sha256:0f36b8c5b45a1403f31ae3e1f2db1be6126a1a8d3d89157dfbf1a9caf8364a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.4 MB (625391663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5670c24f999c8b72981507cb47d2b2dcaf53d09af6a4187abbd6fe21f62d48fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:12 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e11ad5a4fd5be41f07ac93311f8ae1f7dfd6455edf9f5cf950e26d70ee4c6`  
		Last Modified: Tue, 21 Oct 2025 01:53:30 GMT  
		Size: 26.8 MB (26775679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e99453a1ea6755d1a3a58fe6632281db5820c733291dbefe645ffd8397c7e4`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 69.8 MB (69795039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4be1d74f0f5cdfd17973a37d16dc7ed75a3f628a94c99be57d59571d3a9b4`  
		Last Modified: Tue, 21 Oct 2025 04:13:56 GMT  
		Size: 240.1 MB (240053433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b95b67c6e22caf5578ea1eddb03fde4e1cedc03293a23c829f701c73cc927b`  
		Last Modified: Thu, 30 Oct 2025 23:51:31 GMT  
		Size: 238.0 MB (237966938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:de9c5a2a0cb7e4e8b0375014aeac39baef1c37299b1295b32c691537e29bbdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17193526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7797bff6bc0b961011e7f5b876cc1e1e46af5fb5bb27dddfa8a0836045fbdcf6`

```dockerfile
```

-	Layers:
	-	`sha256:4ba4d0a028ca002c9baa8b6e271bbed6f0b707811424f49afb3dbed5b7bbbc66`  
		Last Modified: Thu, 30 Oct 2025 23:45:27 GMT  
		Size: 17.2 MB (17178183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f46fff4553bf23d62e5ffce1a59bed624919c2fea3703b65b013ef50394d42`  
		Last Modified: Thu, 30 Oct 2025 23:45:28 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-trixie` - linux; riscv64

```console
$ docker pull rust@sha256:db568b830f6fd90592497dd0eda8001ed384c555723f1082ceb67a49b9968c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.7 MB (731746485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dde95f55f8cca95c0c52acf2dc0afce27141a1ec0354bce98292db2d8245a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:41:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:41:49 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c640441904d97046ee4a137483e3b6745e0a18782c3b688fede8e9ddf18261f`  
		Last Modified: Wed, 22 Oct 2025 18:09:29 GMT  
		Size: 25.0 MB (24953874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb6fec5cd2588ba9a09a9491547b6e7005f3640a81c530cc1f2e651257c901`  
		Last Modified: Fri, 24 Oct 2025 21:34:03 GMT  
		Size: 66.7 MB (66662364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c02978248d2c72ee734dd5ab68325ab5be1edbbfe6026472d198390eabe8cf`  
		Last Modified: Sun, 26 Oct 2025 13:26:52 GMT  
		Size: 322.8 MB (322829684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af21d31669ce50f730bd664ae7d97ab0697a48fc4c1fc527c93c32c6f717c3f3`  
		Last Modified: Thu, 30 Oct 2025 21:56:54 GMT  
		Size: 269.5 MB (269530257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:5d2476fa78b8cae7f942b74725782b510c4b6a2f687346c648591dd4613b5b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17281556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c73611675d5101a89fa89d59b3a33599e9498dfc407639e4c3b51d2879ed92d`

```dockerfile
```

-	Layers:
	-	`sha256:de5eee62216cb8618afba94f9d4c277f9a550568818b3cbe17aa78900016e6f7`  
		Last Modified: Thu, 30 Oct 2025 23:45:56 GMT  
		Size: 17.3 MB (17266092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c38e4c4e014047f4332c3cf3bf8372bf0ff126eadb475671eb5f6759bb6503e9`  
		Last Modified: Thu, 30 Oct 2025 23:45:57 GMT  
		Size: 15.5 KB (15464 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91-trixie` - linux; s390x

```console
$ docker pull rust@sha256:58124806371c4a39a5ac92593a6f823c354d5d002cae39305db81a0b200dc7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.1 MB (648135109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571bb1f5470229ff143899581ee0538e785fbd8bb45168569fa265be37201747`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 22:48:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:48:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:48:48 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9f518343ed4506c34ae7900f538c56bac66f4fad9740034ee8b819bd8d15e`  
		Last Modified: Tue, 21 Oct 2025 12:43:19 GMT  
		Size: 26.8 MB (26783314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb7d34d2ff189fa2150ed8d82914c7669f312817531bbe187965e9d30825d3`  
		Last Modified: Tue, 21 Oct 2025 23:25:03 GMT  
		Size: 68.6 MB (68630635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4131ad2e1cf6d0e51274c6e30ebc34015c8e72c5b79a0146220944b33c750ff`  
		Last Modified: Wed, 22 Oct 2025 12:46:56 GMT  
		Size: 206.5 MB (206460184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2905cafaed65f05704ab3b4e23479ae861bb4a148a0aac8b459931962ccf1469`  
		Last Modified: Thu, 30 Oct 2025 22:52:24 GMT  
		Size: 296.9 MB (296909277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:54a2179f33db9cea350dd680ac4622e0df5e333f36232801102916c3b7ff749b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17002545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c6960bfd3415ad92fd83afb42906df93f6f114175be156af8cd8f842cfa20c`

```dockerfile
```

-	Layers:
	-	`sha256:24c7152c5b9ea076d3348e04b2479b166ba9b19eff01141c458fb04c53fdcdd6`  
		Last Modified: Thu, 30 Oct 2025 23:46:10 GMT  
		Size: 17.0 MB (16987149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc6358b456c6334b83aedd51c445eeedb3650635525e2e50790b42a8d5968cd`  
		Last Modified: Thu, 30 Oct 2025 23:46:11 GMT  
		Size: 15.4 KB (15396 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91.0`

```console
$ docker pull rust@sha256:eac325268dbdd1c874282a92ad2e0012f19005f65732f9828ecb077c1065c0f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.91.0` - linux; arm variant v7

```console
$ docker pull rust@sha256:df192b38e9142bc8d454be61de04235e6e3d6e3cc142b3ca4461565fdcdb5c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583252486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a735b8020181b775c6ff35bd4f4ddaf6fccacf90d6baef0e5b88f5fac468e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:20 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:20 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:20 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cda7f0b38d756bba039d1251605b315c32a18bef1d71d1a0a98df8f4c7fb6`  
		Last Modified: Tue, 21 Oct 2025 06:18:01 GMT  
		Size: 193.2 MB (193235864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7085e104656ea6c66d8ba95df53b71fae0ae8c42dce84c36d3dd51cc63114cc`  
		Last Modified: Thu, 30 Oct 2025 23:48:47 GMT  
		Size: 258.0 MB (257970062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0` - unknown; unknown

```console
$ docker pull rust@sha256:7bdc29f59dfa654c3d2300e1d752366f54275c8759cf65ee11f3b51b5ee02ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b60585f52529edd183ac79b90c91a6c5c7a9f7718df436557b6c48120de964f`

```dockerfile
```

-	Layers:
	-	`sha256:e7514cf6a08ba2c22ef71f6054b5e755385f65048788dccfe2a655928e7613af`  
		Last Modified: Thu, 30 Oct 2025 23:44:49 GMT  
		Size: 17.0 MB (16977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7716c3ffa9ab429830b3182885b3f920b00e895ca1ca6dc9aa0e0866b3405617`  
		Last Modified: Thu, 30 Oct 2025 23:44:50 GMT  
		Size: 15.5 KB (15508 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:69d4bc701fcca1d78e46d634aca8f1b0a3b967b755e87d0c3e883abf402a92c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.6 MB (548594894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124905d571200dee29c0250b5a56242cbb369d8d6a2f46770ef2060b9aa6ae19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:13 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f695ddffd81064f15ea19428e2d643e8b560e48e54ae801a8d63c45ad6ac29`  
		Last Modified: Tue, 21 Oct 2025 04:14:42 GMT  
		Size: 226.1 MB (226078014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b0009962587465f15c28cbaa4e05bede4600a6b68c86467eb69e4227df6c84`  
		Last Modified: Thu, 30 Oct 2025 23:44:37 GMT  
		Size: 180.3 MB (180266565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0` - unknown; unknown

```console
$ docker pull rust@sha256:a2ff1f30c17e94d0edaf28e068fd1a99b76f759cebd6a2b304606e7c085f21aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17309822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d625100634edff47e63fc8b469129a68a25115bad3e0531a1f7b594067d865`

```dockerfile
```

-	Layers:
	-	`sha256:b3eb795d70d03f35b63225b01143c51f0f8b6622f4022cb5db697d2ba9e108d7`  
		Last Modified: Thu, 30 Oct 2025 23:45:11 GMT  
		Size: 17.3 MB (17294274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f42745a111fee91795bb40aa7014469e06556069a7271890a09e381d064bfc`  
		Last Modified: Thu, 30 Oct 2025 23:45:12 GMT  
		Size: 15.5 KB (15548 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0` - linux; 386

```console
$ docker pull rust@sha256:0f36b8c5b45a1403f31ae3e1f2db1be6126a1a8d3d89157dfbf1a9caf8364a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.4 MB (625391663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5670c24f999c8b72981507cb47d2b2dcaf53d09af6a4187abbd6fe21f62d48fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:12 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e11ad5a4fd5be41f07ac93311f8ae1f7dfd6455edf9f5cf950e26d70ee4c6`  
		Last Modified: Tue, 21 Oct 2025 01:53:30 GMT  
		Size: 26.8 MB (26775679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e99453a1ea6755d1a3a58fe6632281db5820c733291dbefe645ffd8397c7e4`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 69.8 MB (69795039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4be1d74f0f5cdfd17973a37d16dc7ed75a3f628a94c99be57d59571d3a9b4`  
		Last Modified: Tue, 21 Oct 2025 04:13:56 GMT  
		Size: 240.1 MB (240053433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b95b67c6e22caf5578ea1eddb03fde4e1cedc03293a23c829f701c73cc927b`  
		Last Modified: Thu, 30 Oct 2025 23:51:31 GMT  
		Size: 238.0 MB (237966938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0` - unknown; unknown

```console
$ docker pull rust@sha256:de9c5a2a0cb7e4e8b0375014aeac39baef1c37299b1295b32c691537e29bbdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17193526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7797bff6bc0b961011e7f5b876cc1e1e46af5fb5bb27dddfa8a0836045fbdcf6`

```dockerfile
```

-	Layers:
	-	`sha256:4ba4d0a028ca002c9baa8b6e271bbed6f0b707811424f49afb3dbed5b7bbbc66`  
		Last Modified: Thu, 30 Oct 2025 23:45:27 GMT  
		Size: 17.2 MB (17178183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f46fff4553bf23d62e5ffce1a59bed624919c2fea3703b65b013ef50394d42`  
		Last Modified: Thu, 30 Oct 2025 23:45:28 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0` - linux; riscv64

```console
$ docker pull rust@sha256:db568b830f6fd90592497dd0eda8001ed384c555723f1082ceb67a49b9968c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.7 MB (731746485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dde95f55f8cca95c0c52acf2dc0afce27141a1ec0354bce98292db2d8245a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:41:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:41:49 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c640441904d97046ee4a137483e3b6745e0a18782c3b688fede8e9ddf18261f`  
		Last Modified: Wed, 22 Oct 2025 18:09:29 GMT  
		Size: 25.0 MB (24953874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb6fec5cd2588ba9a09a9491547b6e7005f3640a81c530cc1f2e651257c901`  
		Last Modified: Fri, 24 Oct 2025 21:34:03 GMT  
		Size: 66.7 MB (66662364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c02978248d2c72ee734dd5ab68325ab5be1edbbfe6026472d198390eabe8cf`  
		Last Modified: Sun, 26 Oct 2025 13:26:52 GMT  
		Size: 322.8 MB (322829684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af21d31669ce50f730bd664ae7d97ab0697a48fc4c1fc527c93c32c6f717c3f3`  
		Last Modified: Thu, 30 Oct 2025 21:56:54 GMT  
		Size: 269.5 MB (269530257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0` - unknown; unknown

```console
$ docker pull rust@sha256:5d2476fa78b8cae7f942b74725782b510c4b6a2f687346c648591dd4613b5b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17281556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c73611675d5101a89fa89d59b3a33599e9498dfc407639e4c3b51d2879ed92d`

```dockerfile
```

-	Layers:
	-	`sha256:de5eee62216cb8618afba94f9d4c277f9a550568818b3cbe17aa78900016e6f7`  
		Last Modified: Thu, 30 Oct 2025 23:45:56 GMT  
		Size: 17.3 MB (17266092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c38e4c4e014047f4332c3cf3bf8372bf0ff126eadb475671eb5f6759bb6503e9`  
		Last Modified: Thu, 30 Oct 2025 23:45:57 GMT  
		Size: 15.5 KB (15464 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0` - linux; s390x

```console
$ docker pull rust@sha256:58124806371c4a39a5ac92593a6f823c354d5d002cae39305db81a0b200dc7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.1 MB (648135109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571bb1f5470229ff143899581ee0538e785fbd8bb45168569fa265be37201747`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 22:48:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:48:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:48:48 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9f518343ed4506c34ae7900f538c56bac66f4fad9740034ee8b819bd8d15e`  
		Last Modified: Tue, 21 Oct 2025 12:43:19 GMT  
		Size: 26.8 MB (26783314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb7d34d2ff189fa2150ed8d82914c7669f312817531bbe187965e9d30825d3`  
		Last Modified: Tue, 21 Oct 2025 23:25:03 GMT  
		Size: 68.6 MB (68630635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4131ad2e1cf6d0e51274c6e30ebc34015c8e72c5b79a0146220944b33c750ff`  
		Last Modified: Wed, 22 Oct 2025 12:46:56 GMT  
		Size: 206.5 MB (206460184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2905cafaed65f05704ab3b4e23479ae861bb4a148a0aac8b459931962ccf1469`  
		Last Modified: Thu, 30 Oct 2025 22:52:24 GMT  
		Size: 296.9 MB (296909277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0` - unknown; unknown

```console
$ docker pull rust@sha256:54a2179f33db9cea350dd680ac4622e0df5e333f36232801102916c3b7ff749b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17002545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c6960bfd3415ad92fd83afb42906df93f6f114175be156af8cd8f842cfa20c`

```dockerfile
```

-	Layers:
	-	`sha256:24c7152c5b9ea076d3348e04b2479b166ba9b19eff01141c458fb04c53fdcdd6`  
		Last Modified: Thu, 30 Oct 2025 23:46:10 GMT  
		Size: 17.0 MB (16987149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc6358b456c6334b83aedd51c445eeedb3650635525e2e50790b42a8d5968cd`  
		Last Modified: Thu, 30 Oct 2025 23:46:11 GMT  
		Size: 15.4 KB (15396 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91.0-alpine`

```console
$ docker pull rust@sha256:9fd0e182b22d47dd156d65614ded598572c438bc3db79c109c892cd45ab205f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.91.0-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d8a0b1798b6837e717df2a58ce2f5653c3cf064617ef1345c7fa2e9d83f35044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338571527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c334672aeafb6097099971d43eda27635fb349cd96669fe6b776259c094c0621`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:06 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:06 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:21 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3cfaef0615cb0253cafffaabf7ec4ecc5175443b4ab6064f2e6ee284a050c1`  
		Last Modified: Thu, 30 Oct 2025 21:36:13 GMT  
		Size: 59.1 MB (59143801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9674b249fc5ce80c99c4602fb01c94be64a649a3024dac74778ee94d7db0705`  
		Last Modified: Thu, 30 Oct 2025 22:50:59 GMT  
		Size: 275.3 MB (275289657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:ae5caee0dbfd83810c65df11e27dabf9dcff493e569bade06d6c3cf6dfbe8db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.7 KB (875736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c20db5b6d61ba982bc0de623cef8139d3cca9749848be2c546175c599723f`

```dockerfile
```

-	Layers:
	-	`sha256:240bdbfb8f97567899690facfafee478aa0eea76bee43834ce0e312b2abe7c6e`  
		Last Modified: Thu, 30 Oct 2025 23:44:39 GMT  
		Size: 862.3 KB (862259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f33d22a8ba00cd9de8a1cef55af65f0faaeac769c82fb9d7ff25993b539c3e`  
		Last Modified: Thu, 30 Oct 2025 23:44:40 GMT  
		Size: 13.5 KB (13477 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91.0-alpine3.20`

```console
$ docker pull rust@sha256:028f385627e06cdb0eca7f662c2850ba734af65b6769551050e3d693ce7afe31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.91.0-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2b1f24765d5621e41b309cbcf190fad00badbcd79cddcfbcc6e9afb4e74859e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332323361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2be9399e5a5e1241a21bc9d4b6a3fb9a91eda423ff9f867729f1c7d4dd1494`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:32 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:32 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:48 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4701d29124b0199e51ffb3475f695f3b57083f5755bdca3b30b7fb7e41ace7ab`  
		Last Modified: Thu, 30 Oct 2025 21:36:44 GMT  
		Size: 52.9 MB (52945684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7e5474d3d895c6f5799dd4f3bbbdcfa776a9e50f408ba69a4717a2899eb367`  
		Last Modified: Thu, 30 Oct 2025 21:36:29 GMT  
		Size: 275.3 MB (275288300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:2b3d670ab5944d9837c64cdbfd523b88a99f9a56456dd23f8118f9363cc14688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.0 KB (758017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f15731caffee3bf6608f446feff1ee659f031fd1cd8f5b09435eb35688932a2`

```dockerfile
```

-	Layers:
	-	`sha256:6912c322cae1e576478d01096232f97779aa51160ce3cfe9cfaec428fcf894a3`  
		Last Modified: Thu, 30 Oct 2025 23:46:04 GMT  
		Size: 745.8 KB (745792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e187fd7b741e285cb843267475b89466d15f6b182c4390c712e27e84fcf08123`  
		Last Modified: Thu, 30 Oct 2025 23:46:06 GMT  
		Size: 12.2 KB (12225 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91.0-alpine3.21`

```console
$ docker pull rust@sha256:3b4d4d9c0135f422d65504ff9fa1bc6c9a28b75bbbf442720d7f26fbf19f705f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.91.0-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a8d313620e805ad10815a56881e538d77f2691f105866bf1c3d06a763c821ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338380943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917e8113aca6a443a4a106b586c655c769fa81ffae061acf9520322b8ca153f7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:33 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:33 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:33 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:48 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108b0b7e1f75a2459f5f726e6189c5c2d3641caf14b00d2ca791da1bf9326c47`  
		Last Modified: Thu, 30 Oct 2025 21:36:41 GMT  
		Size: 59.1 MB (59098892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360f393f0b81dc80a22d0dedab45fc6b4fda056ff253f63643f56d81e2db340d`  
		Last Modified: Thu, 30 Oct 2025 21:36:29 GMT  
		Size: 275.3 MB (275289698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:f0d8e262a56e25c2157fb337c3d8b20dc1db76f484d732577849cca7c8888fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.5 KB (872454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b3ad2c369a7b6bd488f24704a97ec90f0a3318cb7bb60340efe6720f17797e`

```dockerfile
```

-	Layers:
	-	`sha256:4d344bf8bbc4d9656f3eefb11ac3675e925a0a32b5c22728bd7ebc3473c5dc83`  
		Last Modified: Thu, 30 Oct 2025 23:44:48 GMT  
		Size: 860.2 KB (860228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05b732c240fc68ebdbe4f1cdb77483fdc405ee55243fdc8dac13b63d314636a3`  
		Last Modified: Thu, 30 Oct 2025 23:44:49 GMT  
		Size: 12.2 KB (12226 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91.0-alpine3.22`

```console
$ docker pull rust@sha256:9fd0e182b22d47dd156d65614ded598572c438bc3db79c109c892cd45ab205f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.91.0-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d8a0b1798b6837e717df2a58ce2f5653c3cf064617ef1345c7fa2e9d83f35044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338571527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c334672aeafb6097099971d43eda27635fb349cd96669fe6b776259c094c0621`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:06 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:06 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:21 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3cfaef0615cb0253cafffaabf7ec4ecc5175443b4ab6064f2e6ee284a050c1`  
		Last Modified: Thu, 30 Oct 2025 21:36:13 GMT  
		Size: 59.1 MB (59143801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9674b249fc5ce80c99c4602fb01c94be64a649a3024dac74778ee94d7db0705`  
		Last Modified: Thu, 30 Oct 2025 22:50:59 GMT  
		Size: 275.3 MB (275289657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:ae5caee0dbfd83810c65df11e27dabf9dcff493e569bade06d6c3cf6dfbe8db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.7 KB (875736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c20db5b6d61ba982bc0de623cef8139d3cca9749848be2c546175c599723f`

```dockerfile
```

-	Layers:
	-	`sha256:240bdbfb8f97567899690facfafee478aa0eea76bee43834ce0e312b2abe7c6e`  
		Last Modified: Thu, 30 Oct 2025 23:44:39 GMT  
		Size: 862.3 KB (862259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f33d22a8ba00cd9de8a1cef55af65f0faaeac769c82fb9d7ff25993b539c3e`  
		Last Modified: Thu, 30 Oct 2025 23:44:40 GMT  
		Size: 13.5 KB (13477 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91.0-bookworm`

```console
$ docker pull rust@sha256:1799e112d1f0b81caf2dc0c3e9cc40f1279b1ff2747db9557bfb0c17eb7a751b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.91.0-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:051b0136c8a4e3e112b39e508921112fbde875a02b07b38c87a737e1e81cc746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.1 MB (559108573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be8e386e015e2bb88eaa00172139beb421d17d3570f6121a8fb2dbe27f2e20b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:35:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:42 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178651637d26f6ae6fc6c2a3297b37f8bbef12e80d822930b05b14f51a262382`  
		Last Modified: Tue, 21 Oct 2025 02:43:48 GMT  
		Size: 21.9 MB (21934505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14411cad8875b2a42f951ec95179ed8a844d1522990ec8b96f1c4d269ce3c71f`  
		Last Modified: Tue, 21 Oct 2025 04:11:04 GMT  
		Size: 59.7 MB (59652688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934fb9fcc0f174aa356a518c85a7e2e8a62dd5902afe2a8dbbf58f5f8b37166b`  
		Last Modified: Tue, 21 Oct 2025 06:17:29 GMT  
		Size: 175.4 MB (175355007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a2122d86f314de64147fdae6b5b37d7b95098ae45f73107f366595e6097bc`  
		Last Modified: Thu, 30 Oct 2025 21:36:31 GMT  
		Size: 258.0 MB (257970463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:29db2457c6db102e7a390b4609d14f799d0b4dc98f04e20b278bee9349696010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15685187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840c6decc4d442f284b6c01b397281e4a69f76e76b12d384284a4eb807702448`

```dockerfile
```

-	Layers:
	-	`sha256:8db0f390e801710744db2d01b0058a149ac8d4833025dd5538c43e761de709dd`  
		Last Modified: Thu, 30 Oct 2025 23:45:19 GMT  
		Size: 15.7 MB (15671436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd29c41b660a030fe351fe27c96ba66c2b369e2fa4d46468e264be654f4fc10a`  
		Last Modified: Thu, 30 Oct 2025 23:45:20 GMT  
		Size: 13.8 KB (13751 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b5ea992358738c5ac3d06cafcd8f8274a36b77738ff7c8ac37828322399a6c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.6 MB (519553946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4518efce2e74532fa1aab649f80dd367117838d24a5a2c3caeba50ab3d523197`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:56 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:56 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15270faa4e93fc4bcc62caecce8d2f5dfc1443d3c99572dfb689973b24c0a4`  
		Last Modified: Tue, 21 Oct 2025 02:35:23 GMT  
		Size: 64.4 MB (64370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6803b5e31b40492f4747e974e6e4ae692982b12beb2b87ed9d9ffbdaedefcfd4`  
		Last Modified: Tue, 21 Oct 2025 04:13:43 GMT  
		Size: 203.0 MB (202958684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3099636657b1560c5cdee62a47498eec65574f75745e2e59dbe17331d4c6cedd`  
		Last Modified: Thu, 30 Oct 2025 23:48:57 GMT  
		Size: 180.3 MB (180267344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:eb1282379cca9bd583c19b02bb212db62b40aedd81ce17ed2fb038637a279a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15911254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee670b912d558498da8a680449137c57f480fd39afb5dcb916fa1b657838370a`

```dockerfile
```

-	Layers:
	-	`sha256:310f60a24c03dd47886646e436808491680a7092f501e1625c0b0137803aca44`  
		Last Modified: Thu, 30 Oct 2025 23:45:35 GMT  
		Size: 15.9 MB (15897478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f59b3162dc6c5eae0e6dc9c486d6af675e4ee71d672067d47e274f3c0c9d0fd`  
		Last Modified: Thu, 30 Oct 2025 23:45:36 GMT  
		Size: 13.8 KB (13776 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-bookworm` - linux; 386

```console
$ docker pull rust@sha256:3df2b6dd56af4590d062038eb7ea187a744fdaf081514e183042ff7d02854301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.9 MB (588911073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e8ebf3e452e9009e6ac8977f62eeb4677af9d14fe10adff5b5a5229350c519`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3426ba65368da59a25d050cab9d7713d7873264014ab6dfaa6b0c33f0632cb80`  
		Last Modified: Tue, 21 Oct 2025 00:20:21 GMT  
		Size: 49.5 MB (49466720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f14d3e3fda83046fcd165bb976221020273830b54d963f634e53e7796b47053`  
		Last Modified: Tue, 21 Oct 2025 01:52:59 GMT  
		Size: 24.9 MB (24864208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39058bc352da86cee9643b9b447133a3295983ec455cdba2fac6cbbed8726db6`  
		Last Modified: Tue, 21 Oct 2025 02:35:47 GMT  
		Size: 66.2 MB (66231902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed15f8c1488a55d242a6bf3226b75c0d0de56631f3ea18bb327cec39013003bd`  
		Last Modified: Tue, 21 Oct 2025 04:13:40 GMT  
		Size: 210.4 MB (210381245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284a00e05bc16cf43c2f874e7ffa10dfd7a2b9db4a6677907e35dd79fe9a958`  
		Last Modified: Thu, 30 Oct 2025 21:36:44 GMT  
		Size: 238.0 MB (237966998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0599233bf7ca1dbdaf9211ea1d633238a82678ba0c72f9df870614f4db971837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15859504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ad9e5af8c0e73f8cbf71baff9a986c09dce838cd776e52aef2bf3deb361ccd`

```dockerfile
```

-	Layers:
	-	`sha256:4507749c6cb049d9b9929284ce90ffcbb7ec4eb94fb4c9c0262e135f7fc1071f`  
		Last Modified: Thu, 30 Oct 2025 23:45:50 GMT  
		Size: 15.8 MB (15845864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e4d18122dd7bb11ec0aa43861a1fc3f5cff14e9b8487a97a8493193a79c5282`  
		Last Modified: Thu, 30 Oct 2025 23:45:51 GMT  
		Size: 13.6 KB (13640 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:697ff40e2e322426b97c54857174bef11b523a775040bd451466892908de2bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.1 MB (615060656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4faa2b9c9fb04ed6c7fb91522e3b4ad2232170657cc84637e5cca4b424cfd02a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 22:39:51 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:39:51 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:39:51 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca271e8b0e27269a77c65ea555986eaaadf5db02b1ac24f66f8ce2e45a475b`  
		Last Modified: Tue, 21 Oct 2025 22:50:23 GMT  
		Size: 24.0 MB (24027291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944e6bdda425b877e973cde5b6c8eeabf7eed45bfaba0fd705b4f180a07f001f`  
		Last Modified: Wed, 22 Oct 2025 06:00:23 GMT  
		Size: 63.5 MB (63501423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7d40c47b93ce5dc5166e5aa44baae913a478ae1ba5f7865fe24556acef9200`  
		Last Modified: Wed, 22 Oct 2025 14:21:48 GMT  
		Size: 183.5 MB (183485270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1617ee534ab322072d5a49e5b16309a0c49cf8b0232baabd7f545d5675371d`  
		Last Modified: Thu, 30 Oct 2025 22:43:17 GMT  
		Size: 296.9 MB (296909151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:478d1ea453072bde935424c02d4c412b2552cb3b6f3802e364b9daa69bb78b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15690219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9dc7449fb5d0d433daa7aa7b48a617e07616fd804e869aa43d91049e329468`

```dockerfile
```

-	Layers:
	-	`sha256:e5617194576bbf4d19500cc175ba3bdd7dc056a09db6529ed35a8a3df0ebac65`  
		Last Modified: Thu, 30 Oct 2025 23:46:22 GMT  
		Size: 15.7 MB (15676546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f013fc0c2ae0f7a32936873b795b686a9fe5f9867e41c993b818dbda395aa7cc`  
		Last Modified: Thu, 30 Oct 2025 23:46:23 GMT  
		Size: 13.7 KB (13673 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91.0-bullseye`

```console
$ docker pull rust@sha256:84653a7bcf40cb6085bb0f4f6b106c29025d35a022481100cb2e4da62448b4d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.91.0-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:4debe238b6bccd468958311c5ee086154be57fe1f47fb1e17e9a3357f90139be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.5 MB (540499385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a512f11edcf77ed82a2ac07b66308eaf931cc80877cb617b60b8f763011be2f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:35:30 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:30 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:30 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:680ed921e0c94a719af1d242eac2d0c1be8482153680a3940f3435ee5598303a`  
		Last Modified: Tue, 21 Oct 2025 00:20:24 GMT  
		Size: 49.0 MB (49046121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c68013a317d7d802bb25c57a724c8753caec2fc7f0e78fc13f9a38fd22ecd4`  
		Last Modified: Tue, 21 Oct 2025 02:44:25 GMT  
		Size: 14.9 MB (14879264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895fddf2807e047e5b02e5418fd04d343d3e9b5b393b2f3f0cd6704cad44b8f0`  
		Last Modified: Tue, 21 Oct 2025 04:10:49 GMT  
		Size: 50.6 MB (50628495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ef331acdad14a3d1bfe859a1c645cb9f4b9526e16e3fed550eee6b86681db7`  
		Last Modified: Tue, 21 Oct 2025 06:17:35 GMT  
		Size: 168.0 MB (167976463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2345c283f9f7c727f33c6a1e2c5ffa229106bb1e7b3f3f2073146f627866f815`  
		Last Modified: Thu, 30 Oct 2025 21:36:20 GMT  
		Size: 258.0 MB (257969042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f6a16886d335243aaaf88af9f27e0a70520e083485569ce2cca1c2bdd490b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15275978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f206f730d7eeec8a3b422fc88a2602f2e8f4d5d0542c706027b0a2fe2928a2b1`

```dockerfile
```

-	Layers:
	-	`sha256:69bab675147da3f449e5f163a075b2d55e9aa4ed4021b6e356a242df2ef4a59a`  
		Last Modified: Thu, 30 Oct 2025 23:45:27 GMT  
		Size: 15.3 MB (15263395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac6fc96e9abd4822cf5b32fc13e672b114ae72330f34d3a5301f3009e139e4b0`  
		Last Modified: Thu, 30 Oct 2025 23:45:29 GMT  
		Size: 12.6 KB (12583 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bdd72efd5f91a90aa1746b27a7cd1cc1ea77ae0606dc1e0bb9ea3fb1c4adb42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.2 MB (493232128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a548930c92a6745dcce895941534ec91e5af27593c0ae426e760e382ee6bcf7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:39 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a72c4e347b74aa6a0086cf3d1d928528ab02577a17bff4e22366a7df681f564`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 52.3 MB (52257444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f7bdca064e682157394f36dabd112bc9831aff9743216b035e2ccccf704cc3`  
		Last Modified: Tue, 21 Oct 2025 01:46:24 GMT  
		Size: 15.7 MB (15749510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc7a49f7691cb1ac5f0f40edbe6f4beec62021b4fd2544c431d8f694b4b4647`  
		Last Modified: Tue, 21 Oct 2025 02:35:21 GMT  
		Size: 54.9 MB (54860806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0452b809e62b80ba90b1a217898e5cf7675ff6aac67b2967e58600172590649e`  
		Last Modified: Tue, 21 Oct 2025 04:14:12 GMT  
		Size: 190.1 MB (190097178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1493ba40974f9698cde6967247a220e8b21c09de76901470d4a5ed125bfc1cb2`  
		Last Modified: Thu, 30 Oct 2025 21:35:20 GMT  
		Size: 180.3 MB (180267190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:174a6996165236196e2e2234b5a3e3fd65d247300e29913fdf2df1ee0adea225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15478629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e3fdfeaf6bf3fc08da419feb6196d81eb718e95950ce77f11a97ffb49dcb98`

```dockerfile
```

-	Layers:
	-	`sha256:9196d2d341db75ce952d1a4e29bd491214fe5bb55b9f55a90c7343d81100d44d`  
		Last Modified: Thu, 30 Oct 2025 23:45:42 GMT  
		Size: 15.5 MB (15466022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915a2f913a028e29271d667bf808cdabccd5dc980730eeb68ed9556c1750d267`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-bullseye` - linux; 386

```console
$ docker pull rust@sha256:ebfb2e206c2b74a1bb2d9b549cf50bddf2c1313e09fabb019c831ae5f7495a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.1 MB (565086977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0f7bf5bc46fc016e2a1fbd23835673151045c1b511f6c146c2dd9d721eef6c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:32 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:32 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:10d430deaa3d2ab4898db053e80d62403503897839bf6efd17ed5412b18d7973`  
		Last Modified: Tue, 21 Oct 2025 00:20:39 GMT  
		Size: 54.7 MB (54699294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c453fe6b4c7a680d5464137a3450d263e01a7ec4d491659295432d36b0198bbc`  
		Last Modified: Tue, 21 Oct 2025 01:53:19 GMT  
		Size: 16.3 MB (16267847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96adc169c4af311ffba07fa68db5821d6b9b00d285e00f44dad87eff52496658`  
		Last Modified: Tue, 21 Oct 2025 02:35:42 GMT  
		Size: 56.0 MB (56048779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd845a5707f187f6670f0831bc55034f6333f3aa3eede705f688f3c3342392e`  
		Last Modified: Tue, 21 Oct 2025 04:14:36 GMT  
		Size: 200.1 MB (200103484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae4b0e0faf517253d9eb9d5185f476ec1cdfd4f000a81910c9827c0acc7d451`  
		Last Modified: Thu, 30 Oct 2025 21:35:16 GMT  
		Size: 238.0 MB (237967573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:66f198e4ca90d5791b0a7ff640ee5c546edbfd2e0dfeb179fb4f174b4be5814e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15463224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d7dafb0e855c67125a259fe625f7a9d7f828eb79aad926e34bbb81d981988c`

```dockerfile
```

-	Layers:
	-	`sha256:1b2ab51fb7cebaa093a1da9d9de0794786d042ff60414a0211a492701aab92a9`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 15.5 MB (15450753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fd7b2b4922a57612d543c90720e157bdeb2bd2a9b6c5aa37cafabc33a2328f0`  
		Last Modified: Thu, 30 Oct 2025 23:46:00 GMT  
		Size: 12.5 KB (12471 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91.0-slim`

```console
$ docker pull rust@sha256:2b4610b8bba6b252286b4e7d3a9fce4d66f7e6bf7d4cbb6ab1b127649bb4bdcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.91.0-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:36bd228e236519c3a747a87570e7f83dab399d17eca3ef372e6484c3055c6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334448212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c202a0d535ea0887983203aae69fdf71f527951cf86b2b21f3fb6c2cf9a538`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:37:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:37:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:37:12 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6e00fb9e9c84f34ed2d592246743cef540466ac4115722b315d862bccdbb44`  
		Last Modified: Thu, 30 Oct 2025 21:37:57 GMT  
		Size: 308.2 MB (308235318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4e20e1ca9b0f23d783ec6d6ed5be8fa58ddaf53b726d80cd6fe80cf82a708eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b868546b1ef1b0edf1d23ec51f66614251da1094f46405866d3bf09b052aecad`

```dockerfile
```

-	Layers:
	-	`sha256:14738f7012d7020bd06896025d57d8d8f840e853cca38898526091bad7f49804`  
		Last Modified: Thu, 30 Oct 2025 23:45:32 GMT  
		Size: 4.0 MB (3969887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da73b8e3cdf4379799012870a7c21e494173161ddc8b1b353fc501f5632e4cf`  
		Last Modified: Thu, 30 Oct 2025 23:45:33 GMT  
		Size: 15.7 KB (15744 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8f015c79dd7ae0d1ab3218f86dda57f805a046991a5a67aa40088a67965806e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280064640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ccfb92e01921c8ed8fe03746498812688fe017b71f41f9e31a6cea79147abe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9e403b0cf550d52dedd0ab0aa7cbdcdd11f44b28ceb00d624c5c3d50a41df8`  
		Last Modified: Thu, 30 Oct 2025 23:47:09 GMT  
		Size: 249.9 MB (249922513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:cc442428572057302c62370a3c8514cb787a1a7daeed774b9f01e3a53f53d5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96a2c18c7d5bc0df280a6b286dc537b572cbe31668fcf2ad169f1bdf85194d`

```dockerfile
```

-	Layers:
	-	`sha256:606f393a1954d59bcd6d8915d68d376cd05d29024f9a559d92c8ad47da7baa53`  
		Last Modified: Thu, 30 Oct 2025 23:45:37 GMT  
		Size: 4.3 MB (4256227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32db46c306be7344e9ad5e0d189a1f9fccfa49d28d6336ecf1d9609a07d3da88`  
		Last Modified: Thu, 30 Oct 2025 23:45:38 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-slim` - linux; 386

```console
$ docker pull rust@sha256:ef194da922ba0594e7b7ddf8676004948a82926c4d57ac47bf5a47d85b43d571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341758796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4548274d12a2843de650e527ef6fbf4c3a6d29412091c3b2129c37809a899eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:52 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e995015b3e24125a0c10003ec7b1e384ce24f06f88cbd49bce3e36d2e4ffd8f`  
		Last Modified: Thu, 30 Oct 2025 21:36:35 GMT  
		Size: 310.5 MB (310464168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:5a52de8d007cb783912f98e3a2bc9ef1bea117a247b300d3bf0ed25db3ef7b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05360c911e791bc9a471f2026d992be7509b06ede83672b314adfab6d540bf4b`

```dockerfile
```

-	Layers:
	-	`sha256:657d29bb5c22513fcfdf6fccc85d309ca3ac85cc4258c72801d105ab1c31c57a`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 4.1 MB (4138524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed724e78f81430b3f4c6c9bf61b7039d1389fa37f5495feb17edb5614799f43`  
		Last Modified: Thu, 30 Oct 2025 23:45:44 GMT  
		Size: 15.6 KB (15579 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-slim` - linux; riscv64

```console
$ docker pull rust@sha256:aaf1ec04eb2b47005e3b8560b0ab3fa83b42cb6b8c8cd6c6eb55a3c1ca29fd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 MB (391690936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd90d32888708414dd2407217bdbeb9884c97b7b7c8bf613038f97a472c8c4f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:00:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:00:19 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2315ad783eb28b652f5440fe195ec3068e8c8429c644f9745c84f8c522147`  
		Last Modified: Thu, 30 Oct 2025 22:12:21 GMT  
		Size: 363.4 MB (363415286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b085520540a279fab989fbd055fdff984bfe91d00f603dc6d9c1ee6747d497ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cc7bb3bca0e889b9a141380fcd0cf516a70126219e8fbac44ce160e69a9225`

```dockerfile
```

-	Layers:
	-	`sha256:e20ad570b9c4befd769026dc8b5716c3cf74fc0c6bdbddae3ab6e42e13ccdf5e`  
		Last Modified: Thu, 30 Oct 2025 23:45:53 GMT  
		Size: 4.2 MB (4239428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8670d848e45c5e062ecf29084ab05335daba00c88a567e96c2cc5fca9b04fbe3`  
		Last Modified: Thu, 30 Oct 2025 23:45:54 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-slim` - linux; s390x

```console
$ docker pull rust@sha256:38ebb79c4b041ab046e504b5de098381f8027201a2594744a1eb1fecba242ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.1 MB (379117853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd57e4210e0c402a7b13d84e7dbf8a58418c9777b67aa36fa3c2222c9bae1144`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:54:35 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:54:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:54:35 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9805f4fca0189a31ca7f470c6efdd8dd933a751f5e840c7dbe3eb3034acef906`  
		Last Modified: Thu, 30 Oct 2025 22:56:45 GMT  
		Size: 349.3 MB (349280598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:e2b502b6ae9b904b73922a60e8ebe8814262ef8cb49c465af48c8494dbd80fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5388a6f6d7beec83a26ed19423edba57454d4145bb7d7f5aaefbf1faaa6eb99d`

```dockerfile
```

-	Layers:
	-	`sha256:51b388bf3623dd03362dcb15f7452b4677d633e967a003b3bc39faf47e960502`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 4.0 MB (3982759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a69eb51b743dde6eed89af2bfc049b12313cde5e899319a66fa67ebbb2c5ac`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91.0-slim-bookworm`

```console
$ docker pull rust@sha256:1c2b169164fcaa923f6ff28a4af74b9955c548e9924c1b4945758d3ba886a483
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.91.0-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:1a66676e5c0a918aa45dc2fd4f34c16341d8bd0d064bcb7d815d84948da34398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329757809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c700e6793c04e8485ea32a54a1c3181ceb258694c1ee891dbaa530f552a2137`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 21:35:35 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:35 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb5b7bfc507827968f205851cea67b7a646a133c9116ec8737777be53b48787`  
		Last Modified: Thu, 30 Oct 2025 21:36:19 GMT  
		Size: 305.8 MB (305823786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4d727c9416ea7aa7accb2b6d82a1f1de5c78dc426821a57097eada3482d424d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3389581a9eef53aef89c9fe9accc7fed4cb4a49b423420c31e055cb167a7c7de`

```dockerfile
```

-	Layers:
	-	`sha256:9a1821533a3548a60f32478502545e387b5512c73dc2ef81518a839c820dfd39`  
		Last Modified: Thu, 30 Oct 2025 23:45:42 GMT  
		Size: 3.9 MB (3909876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6ed7f684cc050dc1b7ba74ce805f9039dbc61ddf92e8fe680bdb0a148f49b5b`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 14.0 KB (13964 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:756adb3f9d5c27df7bda4994157cb1cdca4cfdf76b8067a906ce5ff86976859e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274222169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0949ace3836ff38d491823d42f6201e9900fc4d22cf7a1b5d1e486cb355cdd9f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 21:35:36 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:36 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:36 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1f6c6c415a2d4c2edb9805e85b4dd69f95451b08268ffadfa1cdc061e695e0`  
		Last Modified: Thu, 30 Oct 2025 21:36:13 GMT  
		Size: 246.1 MB (246119979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:26a1086edf6420fbae6f26d20f0a2e8dca444eece965956194efe35e03d12a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b8fa2cd2b51fd9918b40c6c59ef73fac18d50aeb2bda9819c79a14219bcd30`

```dockerfile
```

-	Layers:
	-	`sha256:49e6348f3e8ffeac0bcd864980bf5f66c031fe768ed1d3c96c76d88dc7d4580f`  
		Last Modified: Thu, 30 Oct 2025 23:45:49 GMT  
		Size: 4.1 MB (4117775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90e56046bfcea1eefde6da940a766b28525d88059af7258ec565aa8e2c50f09a`  
		Last Modified: Thu, 30 Oct 2025 23:45:50 GMT  
		Size: 14.0 KB (13988 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:8ee0bf09c075a2f76ab2a753178a50023da8354eaa3066be15ae6df16b40eb26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.8 MB (334773527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f02408a764c4d03ef0ac688ee39de788035eb1fc14f6701fc34b094b37ec2a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df86e57d1d11515507bced15d2c5b47745ef47d90bf56ccfea3ffeb9852fdea4`  
		Last Modified: Thu, 30 Oct 2025 21:36:42 GMT  
		Size: 305.6 MB (305563849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4c7086dfaf26b09349225db4c780cf050cd5c0c5587f443eb99860dab7dcc2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4088714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ca752b45a8a21a6be117b63b2108326231dbd39bf5ad0f1421afa525c16f0f`

```dockerfile
```

-	Layers:
	-	`sha256:41e7bf57a66535222d70a721ed5c6d7627a2529faa2fa47097ea4924980ffe34`  
		Last Modified: Thu, 30 Oct 2025 23:45:56 GMT  
		Size: 4.1 MB (4074862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d529607b7e48cf2c2deba92ff2676f549bc263c168014cc85eaccd836f9b478`  
		Last Modified: Thu, 30 Oct 2025 23:45:57 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b5ae74b41977de30791004301b9a55684a4a354fbbfe5a46fd7c412a1db484b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.9 MB (373924203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c02d1953e53a49919fdf3212d3b0191ff68e4b62f8b6cd5875592f08ab9f534`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 22:45:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:45:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:45:13 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:43b0f588b497b17691a3547afa4ae41853829cffde6930e6425ddae4a3f89278`  
		Last Modified: Tue, 21 Oct 2025 00:21:28 GMT  
		Size: 26.9 MB (26884356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ac26cb25e9079f7df28678594c9546404a88850ef59d1906cdae0af1834af2`  
		Last Modified: Thu, 30 Oct 2025 22:47:19 GMT  
		Size: 347.0 MB (347039847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ca7ec822c8eac17e6a09f4496f9ea73f7f5cf4a227037de86239e19824a01cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7bdc57546b9d419b45fd2009461ac7feb00999dd5424e0861ae69445408a1d`

```dockerfile
```

-	Layers:
	-	`sha256:a163636249f2f57c519801b581ece738bbca25c2502343f983fc21023358dc51`  
		Last Modified: Thu, 30 Oct 2025 23:46:05 GMT  
		Size: 3.9 MB (3933157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4082065c8b0d4a306a1d88f8e5c972213af58b5b72c4f05bb1bdf4f35a0db44`  
		Last Modified: Thu, 30 Oct 2025 23:46:06 GMT  
		Size: 13.9 KB (13884 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91.0-slim-bullseye`

```console
$ docker pull rust@sha256:b9f673be74dc9469a3802a767dc3601ed64553a0df026e9124076e6b60e80919
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.91.0-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:13fc3a2170515d49a864808c172e6ef2cdb6ceb7d516c49d43f25dc6d7220aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325804399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e041264a283725f3e8d0e27bf0c41b94d5c1f7a4f0ad080f4bab768ec221cd17`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 21:35:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:42 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4b897c04dec26603bcc1b01b4283220cd1ffb208f0ec4c0db9e08dab58fcfb5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 25.5 MB (25546187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f470db143d0044ed53ee3c62d37c264ce9347606e374e60113030bb748254e`  
		Last Modified: Thu, 30 Oct 2025 21:36:25 GMT  
		Size: 300.3 MB (300258212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:80c8d376c747cb7f8555437910e6c9a1add734f8d43488803a7fbb48d5300c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cb2dd69accf11a0b247c6ebd6851c11ca87d48376f5b4c43e55069d8779493`

```dockerfile
```

-	Layers:
	-	`sha256:3886373e00abc1e6f64ba5c91f674e54b4699c88fafb62b650aaaf8da12bec8e`  
		Last Modified: Thu, 30 Oct 2025 23:45:53 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea67c0e765b1816115cb1b8753a4b992d18c1f0dbe17cbdafddb31a15734a966`  
		Last Modified: Thu, 30 Oct 2025 23:45:54 GMT  
		Size: 12.8 KB (12794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7ff887fd3eb13d26eecb0f40398028fdc12a3298ef48c8528331016decfb0ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264715851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ae94dab2b12284d1f2e92e3e2ac7b56eff6bb02864e3639caa14c43b4390fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 21:34:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:39 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db337e821e80e597fa142716f1cb02566d2cf4168196f5f08a415cfb4a249b7`  
		Last Modified: Thu, 30 Oct 2025 21:35:15 GMT  
		Size: 236.0 MB (235967450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f46b8601c7c669072e496b7807335af3362860103487ba6340ac14700e4d2e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3c48bda2928a06b24f54d0c55cb10592408f842b75a6984f01eb69ebb7f065`

```dockerfile
```

-	Layers:
	-	`sha256:ab6b83830f27e4a54af4a4ff3428fe72f6898a17d7e3c21d3a7b6165de49140c`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4018ce6087359d14714e6bcbfbfdc372aa884d3abeff3000503021a2c3381d0f`  
		Last Modified: Thu, 30 Oct 2025 23:46:00 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:a8c4281836aee33f681efe73b74c2fe608821ab8a79e1e4f53c408cbee6a616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329920628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44d16d04c4e9d940226b9321174f5ada41cc3046700d8f53b9f75357436b02a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 21:35:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:04 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ed9b7a4c5998c0d248e37f414fa0883c2b695df7b879c0ba096280f29fcb2660`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 31.2 MB (31191494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8bca4c0d96694e3d489bc0df62c181f63f68bd29966b3d385296b7f25514f0`  
		Last Modified: Thu, 30 Oct 2025 21:35:46 GMT  
		Size: 298.7 MB (298729134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8220d5bc4c59b662f331a750b1c3e053eb553fcf58d971daa7ceda6433fac105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ee75a2e521250b772ff737b27beb9860a1292184f784af6f4e157e5a734559`

```dockerfile
```

-	Layers:
	-	`sha256:5ee000ac8ab06e33a71014e51eeb45b60c7820fd0d03e45c9fd2b1573f530073`  
		Last Modified: Thu, 30 Oct 2025 23:46:05 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fb44d48fb78f0b88ebc033734c23af5eb6f66040ca67ec8536dcd1a1755ed6f`  
		Last Modified: Thu, 30 Oct 2025 23:46:06 GMT  
		Size: 12.7 KB (12682 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91.0-slim-trixie`

```console
$ docker pull rust@sha256:2b4610b8bba6b252286b4e7d3a9fce4d66f7e6bf7d4cbb6ab1b127649bb4bdcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.91.0-slim-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:36bd228e236519c3a747a87570e7f83dab399d17eca3ef372e6484c3055c6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334448212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c202a0d535ea0887983203aae69fdf71f527951cf86b2b21f3fb6c2cf9a538`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:37:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:37:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:37:12 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6e00fb9e9c84f34ed2d592246743cef540466ac4115722b315d862bccdbb44`  
		Last Modified: Thu, 30 Oct 2025 21:37:57 GMT  
		Size: 308.2 MB (308235318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:4e20e1ca9b0f23d783ec6d6ed5be8fa58ddaf53b726d80cd6fe80cf82a708eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b868546b1ef1b0edf1d23ec51f66614251da1094f46405866d3bf09b052aecad`

```dockerfile
```

-	Layers:
	-	`sha256:14738f7012d7020bd06896025d57d8d8f840e853cca38898526091bad7f49804`  
		Last Modified: Thu, 30 Oct 2025 23:45:32 GMT  
		Size: 4.0 MB (3969887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da73b8e3cdf4379799012870a7c21e494173161ddc8b1b353fc501f5632e4cf`  
		Last Modified: Thu, 30 Oct 2025 23:45:33 GMT  
		Size: 15.7 KB (15744 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8f015c79dd7ae0d1ab3218f86dda57f805a046991a5a67aa40088a67965806e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280064640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ccfb92e01921c8ed8fe03746498812688fe017b71f41f9e31a6cea79147abe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9e403b0cf550d52dedd0ab0aa7cbdcdd11f44b28ceb00d624c5c3d50a41df8`  
		Last Modified: Thu, 30 Oct 2025 23:47:09 GMT  
		Size: 249.9 MB (249922513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:cc442428572057302c62370a3c8514cb787a1a7daeed774b9f01e3a53f53d5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96a2c18c7d5bc0df280a6b286dc537b572cbe31668fcf2ad169f1bdf85194d`

```dockerfile
```

-	Layers:
	-	`sha256:606f393a1954d59bcd6d8915d68d376cd05d29024f9a559d92c8ad47da7baa53`  
		Last Modified: Thu, 30 Oct 2025 23:45:37 GMT  
		Size: 4.3 MB (4256227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32db46c306be7344e9ad5e0d189a1f9fccfa49d28d6336ecf1d9609a07d3da88`  
		Last Modified: Thu, 30 Oct 2025 23:45:38 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-slim-trixie` - linux; 386

```console
$ docker pull rust@sha256:ef194da922ba0594e7b7ddf8676004948a82926c4d57ac47bf5a47d85b43d571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341758796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4548274d12a2843de650e527ef6fbf4c3a6d29412091c3b2129c37809a899eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:52 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e995015b3e24125a0c10003ec7b1e384ce24f06f88cbd49bce3e36d2e4ffd8f`  
		Last Modified: Thu, 30 Oct 2025 21:36:35 GMT  
		Size: 310.5 MB (310464168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:5a52de8d007cb783912f98e3a2bc9ef1bea117a247b300d3bf0ed25db3ef7b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05360c911e791bc9a471f2026d992be7509b06ede83672b314adfab6d540bf4b`

```dockerfile
```

-	Layers:
	-	`sha256:657d29bb5c22513fcfdf6fccc85d309ca3ac85cc4258c72801d105ab1c31c57a`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 4.1 MB (4138524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed724e78f81430b3f4c6c9bf61b7039d1389fa37f5495feb17edb5614799f43`  
		Last Modified: Thu, 30 Oct 2025 23:45:44 GMT  
		Size: 15.6 KB (15579 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-slim-trixie` - linux; riscv64

```console
$ docker pull rust@sha256:aaf1ec04eb2b47005e3b8560b0ab3fa83b42cb6b8c8cd6c6eb55a3c1ca29fd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 MB (391690936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd90d32888708414dd2407217bdbeb9884c97b7b7c8bf613038f97a472c8c4f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:00:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:00:19 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2315ad783eb28b652f5440fe195ec3068e8c8429c644f9745c84f8c522147`  
		Last Modified: Thu, 30 Oct 2025 22:12:21 GMT  
		Size: 363.4 MB (363415286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:b085520540a279fab989fbd055fdff984bfe91d00f603dc6d9c1ee6747d497ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cc7bb3bca0e889b9a141380fcd0cf516a70126219e8fbac44ce160e69a9225`

```dockerfile
```

-	Layers:
	-	`sha256:e20ad570b9c4befd769026dc8b5716c3cf74fc0c6bdbddae3ab6e42e13ccdf5e`  
		Last Modified: Thu, 30 Oct 2025 23:45:53 GMT  
		Size: 4.2 MB (4239428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8670d848e45c5e062ecf29084ab05335daba00c88a567e96c2cc5fca9b04fbe3`  
		Last Modified: Thu, 30 Oct 2025 23:45:54 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-slim-trixie` - linux; s390x

```console
$ docker pull rust@sha256:38ebb79c4b041ab046e504b5de098381f8027201a2594744a1eb1fecba242ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.1 MB (379117853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd57e4210e0c402a7b13d84e7dbf8a58418c9777b67aa36fa3c2222c9bae1144`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:54:35 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:54:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:54:35 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9805f4fca0189a31ca7f470c6efdd8dd933a751f5e840c7dbe3eb3034acef906`  
		Last Modified: Thu, 30 Oct 2025 22:56:45 GMT  
		Size: 349.3 MB (349280598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:e2b502b6ae9b904b73922a60e8ebe8814262ef8cb49c465af48c8494dbd80fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5388a6f6d7beec83a26ed19423edba57454d4145bb7d7f5aaefbf1faaa6eb99d`

```dockerfile
```

-	Layers:
	-	`sha256:51b388bf3623dd03362dcb15f7452b4677d633e967a003b3bc39faf47e960502`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 4.0 MB (3982759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a69eb51b743dde6eed89af2bfc049b12313cde5e899319a66fa67ebbb2c5ac`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.91.0-trixie`

```console
$ docker pull rust@sha256:eac325268dbdd1c874282a92ad2e0012f19005f65732f9828ecb077c1065c0f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1.91.0-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:df192b38e9142bc8d454be61de04235e6e3d6e3cc142b3ca4461565fdcdb5c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583252486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a735b8020181b775c6ff35bd4f4ddaf6fccacf90d6baef0e5b88f5fac468e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:20 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:20 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:20 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cda7f0b38d756bba039d1251605b315c32a18bef1d71d1a0a98df8f4c7fb6`  
		Last Modified: Tue, 21 Oct 2025 06:18:01 GMT  
		Size: 193.2 MB (193235864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7085e104656ea6c66d8ba95df53b71fae0ae8c42dce84c36d3dd51cc63114cc`  
		Last Modified: Thu, 30 Oct 2025 23:48:47 GMT  
		Size: 258.0 MB (257970062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:7bdc29f59dfa654c3d2300e1d752366f54275c8759cf65ee11f3b51b5ee02ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b60585f52529edd183ac79b90c91a6c5c7a9f7718df436557b6c48120de964f`

```dockerfile
```

-	Layers:
	-	`sha256:e7514cf6a08ba2c22ef71f6054b5e755385f65048788dccfe2a655928e7613af`  
		Last Modified: Thu, 30 Oct 2025 23:44:49 GMT  
		Size: 17.0 MB (16977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7716c3ffa9ab429830b3182885b3f920b00e895ca1ca6dc9aa0e0866b3405617`  
		Last Modified: Thu, 30 Oct 2025 23:44:50 GMT  
		Size: 15.5 KB (15508 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:69d4bc701fcca1d78e46d634aca8f1b0a3b967b755e87d0c3e883abf402a92c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.6 MB (548594894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124905d571200dee29c0250b5a56242cbb369d8d6a2f46770ef2060b9aa6ae19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:13 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f695ddffd81064f15ea19428e2d643e8b560e48e54ae801a8d63c45ad6ac29`  
		Last Modified: Tue, 21 Oct 2025 04:14:42 GMT  
		Size: 226.1 MB (226078014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b0009962587465f15c28cbaa4e05bede4600a6b68c86467eb69e4227df6c84`  
		Last Modified: Thu, 30 Oct 2025 23:44:37 GMT  
		Size: 180.3 MB (180266565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:a2ff1f30c17e94d0edaf28e068fd1a99b76f759cebd6a2b304606e7c085f21aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17309822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d625100634edff47e63fc8b469129a68a25115bad3e0531a1f7b594067d865`

```dockerfile
```

-	Layers:
	-	`sha256:b3eb795d70d03f35b63225b01143c51f0f8b6622f4022cb5db697d2ba9e108d7`  
		Last Modified: Thu, 30 Oct 2025 23:45:11 GMT  
		Size: 17.3 MB (17294274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f42745a111fee91795bb40aa7014469e06556069a7271890a09e381d064bfc`  
		Last Modified: Thu, 30 Oct 2025 23:45:12 GMT  
		Size: 15.5 KB (15548 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-trixie` - linux; 386

```console
$ docker pull rust@sha256:0f36b8c5b45a1403f31ae3e1f2db1be6126a1a8d3d89157dfbf1a9caf8364a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.4 MB (625391663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5670c24f999c8b72981507cb47d2b2dcaf53d09af6a4187abbd6fe21f62d48fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:12 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e11ad5a4fd5be41f07ac93311f8ae1f7dfd6455edf9f5cf950e26d70ee4c6`  
		Last Modified: Tue, 21 Oct 2025 01:53:30 GMT  
		Size: 26.8 MB (26775679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e99453a1ea6755d1a3a58fe6632281db5820c733291dbefe645ffd8397c7e4`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 69.8 MB (69795039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4be1d74f0f5cdfd17973a37d16dc7ed75a3f628a94c99be57d59571d3a9b4`  
		Last Modified: Tue, 21 Oct 2025 04:13:56 GMT  
		Size: 240.1 MB (240053433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b95b67c6e22caf5578ea1eddb03fde4e1cedc03293a23c829f701c73cc927b`  
		Last Modified: Thu, 30 Oct 2025 23:51:31 GMT  
		Size: 238.0 MB (237966938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:de9c5a2a0cb7e4e8b0375014aeac39baef1c37299b1295b32c691537e29bbdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17193526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7797bff6bc0b961011e7f5b876cc1e1e46af5fb5bb27dddfa8a0836045fbdcf6`

```dockerfile
```

-	Layers:
	-	`sha256:4ba4d0a028ca002c9baa8b6e271bbed6f0b707811424f49afb3dbed5b7bbbc66`  
		Last Modified: Thu, 30 Oct 2025 23:45:27 GMT  
		Size: 17.2 MB (17178183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f46fff4553bf23d62e5ffce1a59bed624919c2fea3703b65b013ef50394d42`  
		Last Modified: Thu, 30 Oct 2025 23:45:28 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-trixie` - linux; riscv64

```console
$ docker pull rust@sha256:db568b830f6fd90592497dd0eda8001ed384c555723f1082ceb67a49b9968c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.7 MB (731746485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dde95f55f8cca95c0c52acf2dc0afce27141a1ec0354bce98292db2d8245a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:41:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:41:49 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c640441904d97046ee4a137483e3b6745e0a18782c3b688fede8e9ddf18261f`  
		Last Modified: Wed, 22 Oct 2025 18:09:29 GMT  
		Size: 25.0 MB (24953874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb6fec5cd2588ba9a09a9491547b6e7005f3640a81c530cc1f2e651257c901`  
		Last Modified: Fri, 24 Oct 2025 21:34:03 GMT  
		Size: 66.7 MB (66662364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c02978248d2c72ee734dd5ab68325ab5be1edbbfe6026472d198390eabe8cf`  
		Last Modified: Sun, 26 Oct 2025 13:26:52 GMT  
		Size: 322.8 MB (322829684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af21d31669ce50f730bd664ae7d97ab0697a48fc4c1fc527c93c32c6f717c3f3`  
		Last Modified: Thu, 30 Oct 2025 21:56:54 GMT  
		Size: 269.5 MB (269530257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:5d2476fa78b8cae7f942b74725782b510c4b6a2f687346c648591dd4613b5b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17281556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c73611675d5101a89fa89d59b3a33599e9498dfc407639e4c3b51d2879ed92d`

```dockerfile
```

-	Layers:
	-	`sha256:de5eee62216cb8618afba94f9d4c277f9a550568818b3cbe17aa78900016e6f7`  
		Last Modified: Thu, 30 Oct 2025 23:45:56 GMT  
		Size: 17.3 MB (17266092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c38e4c4e014047f4332c3cf3bf8372bf0ff126eadb475671eb5f6759bb6503e9`  
		Last Modified: Thu, 30 Oct 2025 23:45:57 GMT  
		Size: 15.5 KB (15464 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.91.0-trixie` - linux; s390x

```console
$ docker pull rust@sha256:58124806371c4a39a5ac92593a6f823c354d5d002cae39305db81a0b200dc7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.1 MB (648135109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571bb1f5470229ff143899581ee0538e785fbd8bb45168569fa265be37201747`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 22:48:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:48:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:48:48 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9f518343ed4506c34ae7900f538c56bac66f4fad9740034ee8b819bd8d15e`  
		Last Modified: Tue, 21 Oct 2025 12:43:19 GMT  
		Size: 26.8 MB (26783314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb7d34d2ff189fa2150ed8d82914c7669f312817531bbe187965e9d30825d3`  
		Last Modified: Tue, 21 Oct 2025 23:25:03 GMT  
		Size: 68.6 MB (68630635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4131ad2e1cf6d0e51274c6e30ebc34015c8e72c5b79a0146220944b33c750ff`  
		Last Modified: Wed, 22 Oct 2025 12:46:56 GMT  
		Size: 206.5 MB (206460184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2905cafaed65f05704ab3b4e23479ae861bb4a148a0aac8b459931962ccf1469`  
		Last Modified: Thu, 30 Oct 2025 22:52:24 GMT  
		Size: 296.9 MB (296909277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.91.0-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:54a2179f33db9cea350dd680ac4622e0df5e333f36232801102916c3b7ff749b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17002545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c6960bfd3415ad92fd83afb42906df93f6f114175be156af8cd8f842cfa20c`

```dockerfile
```

-	Layers:
	-	`sha256:24c7152c5b9ea076d3348e04b2479b166ba9b19eff01141c458fb04c53fdcdd6`  
		Last Modified: Thu, 30 Oct 2025 23:46:10 GMT  
		Size: 17.0 MB (16987149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc6358b456c6334b83aedd51c445eeedb3650635525e2e50790b42a8d5968cd`  
		Last Modified: Thu, 30 Oct 2025 23:46:11 GMT  
		Size: 15.4 KB (15396 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:29beb3c7b3b1f8c6e2e5b9e7e6c79a38a7e8a8102d92f50f98951feae046a999
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:ee9b9f2ebd8741e4ecf1ade08918e492d642c4e625be481bb7b7954b89e9d504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328784700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffa4185585206d4d98e871b83bebc561866519a6dba20de63e3192e6804528c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b94f1896c7d7197d473e46aa720688e4b64cabd8c559482b9ad62f5d1c54ea`  
		Last Modified: Wed, 08 Oct 2025 23:46:44 GMT  
		Size: 61.6 MB (61604379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fe284ea8abe7a0d30bbfc5a349ac250b13a8a3d1760d8ee638d1c27fbf60b9`  
		Last Modified: Wed, 08 Oct 2025 23:48:01 GMT  
		Size: 263.4 MB (263377869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b05da53540ad6b64b76c78df048088711a426b503ce3d7581f4359156aacb4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.0 KB (794968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81b251f281fcb5a2b4f9301b279ee799dbd08e11092d95582b55c6da2b21b4b`

```dockerfile
```

-	Layers:
	-	`sha256:703eec4d4cc485186fb35c31aed213134f9ac25b9ea2420f1fed91ec0b037f1d`  
		Last Modified: Wed, 08 Oct 2025 23:44:42 GMT  
		Size: 782.7 KB (782673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40831b0dc30117747a9bf98ef753d0b9c681127cd96f9f85d11abebfa5eb8934`  
		Last Modified: Wed, 08 Oct 2025 23:44:43 GMT  
		Size: 12.3 KB (12295 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d8a0b1798b6837e717df2a58ce2f5653c3cf064617ef1345c7fa2e9d83f35044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338571527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c334672aeafb6097099971d43eda27635fb349cd96669fe6b776259c094c0621`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:06 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:06 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:21 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3cfaef0615cb0253cafffaabf7ec4ecc5175443b4ab6064f2e6ee284a050c1`  
		Last Modified: Thu, 30 Oct 2025 21:36:13 GMT  
		Size: 59.1 MB (59143801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9674b249fc5ce80c99c4602fb01c94be64a649a3024dac74778ee94d7db0705`  
		Last Modified: Thu, 30 Oct 2025 22:50:59 GMT  
		Size: 275.3 MB (275289657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:ae5caee0dbfd83810c65df11e27dabf9dcff493e569bade06d6c3cf6dfbe8db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.7 KB (875736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c20db5b6d61ba982bc0de623cef8139d3cca9749848be2c546175c599723f`

```dockerfile
```

-	Layers:
	-	`sha256:240bdbfb8f97567899690facfafee478aa0eea76bee43834ce0e312b2abe7c6e`  
		Last Modified: Thu, 30 Oct 2025 23:44:39 GMT  
		Size: 862.3 KB (862259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f33d22a8ba00cd9de8a1cef55af65f0faaeac769c82fb9d7ff25993b539c3e`  
		Last Modified: Thu, 30 Oct 2025 23:44:40 GMT  
		Size: 13.5 KB (13477 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; ppc64le

```console
$ docker pull rust@sha256:9036b3b6866c1835ae0647bf6e39ed634c24250cbe5ce9323476525325207c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350263091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1c326a8fb61738f78b6e832d76856f610184e585f0bea48eeb0b05acc9a561`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a56909a4c35c502dd43802ef31d4890df3cd54f15133b9f35dcaab1ec3f3219`  
		Last Modified: Thu, 09 Oct 2025 05:14:10 GMT  
		Size: 59.0 MB (59006725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20f6c21afdba425061e0ba687974793c99c42b22eafef8cce1227eb48c95ad`  
		Last Modified: Thu, 09 Oct 2025 08:45:22 GMT  
		Size: 287.5 MB (287524125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:fd67dce82d8a2b47d722b477a74576185f4a69052847396ccba385aec9c0cc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **807.6 KB (807608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c44369fd4d6569b24f091dde0bde6f511b3ece2eeadb14bc5830c655a4e4bf5`

```dockerfile
```

-	Layers:
	-	`sha256:ed8dccf24b40112f8c8bfb29e2beac0c23ea4a599fc28af8dd896d2a067e715e`  
		Last Modified: Thu, 09 Oct 2025 08:44:26 GMT  
		Size: 795.2 KB (795241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417fb1d78b372874952b95cf42ae7f491a90983707634ae9103ede8f18d7de58`  
		Last Modified: Thu, 09 Oct 2025 08:44:27 GMT  
		Size: 12.4 KB (12367 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.20`

```console
$ docker pull rust@sha256:657189ee5207a86316e5946bcfddd4f5ba765f8163768a4e27d97c88a10cca80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:a97b713ba0b992d4855de682705a1671a9f1bdbf56c63106e3b450732ffd31ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322314091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f5a88bc4032951a2b68c4d0695f33ba0c4d4313454952d17e7a3a403713a51`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a081b9ffe7512b030d0920eb506f7c1bdbd5353c51f1960af8fc4d16a313033`  
		Last Modified: Wed, 08 Oct 2025 23:48:38 GMT  
		Size: 55.3 MB (55309661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483b1a71ca7cafce114e0d2124a2448acddbf1e3eda67dfb387c28d92d6b498c`  
		Last Modified: Wed, 08 Oct 2025 23:49:06 GMT  
		Size: 263.4 MB (263377374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:24e8dd54d6ad7a7e7dbecca0c8c9e83421a68648c336216f8217e666a50ca241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.0 KB (720952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d368e2e22b7effe99b5a2bc6ccace24606c18a48fa7fb0382074f287232c805e`

```dockerfile
```

-	Layers:
	-	`sha256:f7637da0d7c6704319b9717d659cab4afc248751241fd31c1faae5ecfebbb85f`  
		Last Modified: Wed, 08 Oct 2025 23:44:30 GMT  
		Size: 709.9 KB (709860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686c296cfedd0c7ba040e33922df421ff0eb8f7e42fc4d42dbd32143f0338fd0`  
		Last Modified: Wed, 08 Oct 2025 23:44:30 GMT  
		Size: 11.1 KB (11092 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:2b1f24765d5621e41b309cbcf190fad00badbcd79cddcfbcc6e9afb4e74859e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332323361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2be9399e5a5e1241a21bc9d4b6a3fb9a91eda423ff9f867729f1c7d4dd1494`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:32 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:32 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:48 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4701d29124b0199e51ffb3475f695f3b57083f5755bdca3b30b7fb7e41ace7ab`  
		Last Modified: Thu, 30 Oct 2025 21:36:44 GMT  
		Size: 52.9 MB (52945684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7e5474d3d895c6f5799dd4f3bbbdcfa776a9e50f408ba69a4717a2899eb367`  
		Last Modified: Thu, 30 Oct 2025 21:36:29 GMT  
		Size: 275.3 MB (275288300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:2b3d670ab5944d9837c64cdbfd523b88a99f9a56456dd23f8118f9363cc14688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.0 KB (758017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f15731caffee3bf6608f446feff1ee659f031fd1cd8f5b09435eb35688932a2`

```dockerfile
```

-	Layers:
	-	`sha256:6912c322cae1e576478d01096232f97779aa51160ce3cfe9cfaec428fcf894a3`  
		Last Modified: Thu, 30 Oct 2025 23:46:04 GMT  
		Size: 745.8 KB (745792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e187fd7b741e285cb843267475b89466d15f6b182c4390c712e27e84fcf08123`  
		Last Modified: Thu, 30 Oct 2025 23:46:06 GMT  
		Size: 12.2 KB (12225 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; ppc64le

```console
$ docker pull rust@sha256:323e9bb9f5bdb3e1b11a122014bc05492bc31fc24ad050be8e38a6774662b1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345167925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01759e6bacb31eac791d7252f80007f9302f67878ee1a72bbde55ad9e4a211ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.20.8-ppc64le.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a78577222d4c08b54b062e8bf30834a3c610281d9b4780d34cac9394431f7f25`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 3.6 MB (3575563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3d4fef061972b5a536d5dc27c6e2ec1a6af1868c7a8ed73649e96ef403cc78`  
		Last Modified: Thu, 09 Oct 2025 11:00:09 GMT  
		Size: 54.1 MB (54069626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959cfe92ddb8a18926e7717589b1acaf295e33b15ca60e9c9e7e65a7567b6de`  
		Last Modified: Thu, 09 Oct 2025 11:01:15 GMT  
		Size: 287.5 MB (287522736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:abdc08db7e1da362ae2750b3c87e0e0bf162b47b03ba70929616e05f4660490d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **714.9 KB (714867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d3a994f7137a606e5fc3bb60732e62b3e11339944cb30264794ee2aff7d0e`

```dockerfile
```

-	Layers:
	-	`sha256:299f111c291c6146617598d78e4abf1162dd1e235a847eeaad20bfeef341b474`  
		Last Modified: Thu, 09 Oct 2025 08:44:30 GMT  
		Size: 703.7 KB (703728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf82392610784b6dc5a5fc46d0db40e68de482571e5808a27a534fc99f1b32d`  
		Last Modified: Thu, 09 Oct 2025 08:44:31 GMT  
		Size: 11.1 KB (11139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.21`

```console
$ docker pull rust@sha256:fa5f395f8f6fd74863960299c24fa0e1eecf7587acbd8abf308a120f505f410d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:ae572f2a6f7d6790ad87264078d4268b6b8618fe1741e61351938474b3981b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328583689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b473418392e0e4e8bec14410ddb1c78d704e4dda726ae28c63d72ae8d39d461f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129b51f390fdd40aaf39ff5cb8eae55f7068b85b99e151bd9be23bcc2a776817`  
		Last Modified: Wed, 08 Oct 2025 23:20:40 GMT  
		Size: 61.6 MB (61563786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741a12271e539b62a08b9044001f072cbc32a6fba77e5f9c606417557d0a1da8`  
		Last Modified: Wed, 08 Oct 2025 23:45:17 GMT  
		Size: 263.4 MB (263377334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:7cf01932cc651a307073160fdf88a0afd7e41ff56bebf14c0f4636a8a3390341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **791.8 KB (791783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1513a03317b2d74a7ef63f021d267865d8903e96ac1bd5f732609a72d165690c`

```dockerfile
```

-	Layers:
	-	`sha256:4d06a9911725da4e0a3dca9033e9b573ffd8ec46f3405912a4c481eb4d4060da`  
		Last Modified: Wed, 08 Oct 2025 23:44:36 GMT  
		Size: 780.7 KB (780690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43b6dce726eed8669c3b712d102c9c2206f16dc85add3d7e8aa6d8f8bc9ef41d`  
		Last Modified: Wed, 08 Oct 2025 23:44:37 GMT  
		Size: 11.1 KB (11093 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a8d313620e805ad10815a56881e538d77f2691f105866bf1c3d06a763c821ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338380943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917e8113aca6a443a4a106b586c655c769fa81ffae061acf9520322b8ca153f7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:33 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:33 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:33 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:48 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108b0b7e1f75a2459f5f726e6189c5c2d3641caf14b00d2ca791da1bf9326c47`  
		Last Modified: Thu, 30 Oct 2025 21:36:41 GMT  
		Size: 59.1 MB (59098892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360f393f0b81dc80a22d0dedab45fc6b4fda056ff253f63643f56d81e2db340d`  
		Last Modified: Thu, 30 Oct 2025 21:36:29 GMT  
		Size: 275.3 MB (275289698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:f0d8e262a56e25c2157fb337c3d8b20dc1db76f484d732577849cca7c8888fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.5 KB (872454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b3ad2c369a7b6bd488f24704a97ec90f0a3318cb7bb60340efe6720f17797e`

```dockerfile
```

-	Layers:
	-	`sha256:4d344bf8bbc4d9656f3eefb11ac3675e925a0a32b5c22728bd7ebc3473c5dc83`  
		Last Modified: Thu, 30 Oct 2025 23:44:48 GMT  
		Size: 860.2 KB (860228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05b732c240fc68ebdbe4f1cdb77483fdc405ee55243fdc8dac13b63d314636a3`  
		Last Modified: Thu, 30 Oct 2025 23:44:49 GMT  
		Size: 12.2 KB (12226 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.21` - linux; ppc64le

```console
$ docker pull rust@sha256:f4dd90421dec60a7fb1accd10539fa73f7ee02a5f7a2626ee7a1e0d7358ade8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350063686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628dcf3397d10c30cfe3a2da197cbc7802d9013f083afaf5724ba0f884fcff00`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602f64aa625bdbad2f881a453963786cb9d664579705975b5c2752ce620d76f2`  
		Last Modified: Thu, 09 Oct 2025 05:12:09 GMT  
		Size: 59.0 MB (58965844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d12187cc736d95350ac1b48c8022932d8f49cc52cbb21f4f21301a7f609105c`  
		Last Modified: Thu, 09 Oct 2025 06:12:28 GMT  
		Size: 287.5 MB (287523767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:75a3a8807264a9e00056be7f21a4d445e55d62566993b3f1a421d2e96e22e14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **804.4 KB (804373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5d3ae9c51942ce90d391458c8f1986586930cf8ce915f3c4cb0946360a6359`

```dockerfile
```

-	Layers:
	-	`sha256:1249f653cab516099082a6ed253d0534f56a8f1e528d0baa470435062437e22f`  
		Last Modified: Thu, 09 Oct 2025 08:44:35 GMT  
		Size: 793.2 KB (793234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb6899ed56649363cee6901aacd976f0b84c33f626067370cf29f452a487ff5`  
		Last Modified: Thu, 09 Oct 2025 08:44:35 GMT  
		Size: 11.1 KB (11139 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.22`

```console
$ docker pull rust@sha256:29beb3c7b3b1f8c6e2e5b9e7e6c79a38a7e8a8102d92f50f98951feae046a999
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine3.22` - linux; amd64

```console
$ docker pull rust@sha256:ee9b9f2ebd8741e4ecf1ade08918e492d642c4e625be481bb7b7954b89e9d504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328784700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffa4185585206d4d98e871b83bebc561866519a6dba20de63e3192e6804528c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b94f1896c7d7197d473e46aa720688e4b64cabd8c559482b9ad62f5d1c54ea`  
		Last Modified: Wed, 08 Oct 2025 23:46:44 GMT  
		Size: 61.6 MB (61604379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fe284ea8abe7a0d30bbfc5a349ac250b13a8a3d1760d8ee638d1c27fbf60b9`  
		Last Modified: Wed, 08 Oct 2025 23:48:01 GMT  
		Size: 263.4 MB (263377869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:b05da53540ad6b64b76c78df048088711a426b503ce3d7581f4359156aacb4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.0 KB (794968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81b251f281fcb5a2b4f9301b279ee799dbd08e11092d95582b55c6da2b21b4b`

```dockerfile
```

-	Layers:
	-	`sha256:703eec4d4cc485186fb35c31aed213134f9ac25b9ea2420f1fed91ec0b037f1d`  
		Last Modified: Wed, 08 Oct 2025 23:44:42 GMT  
		Size: 782.7 KB (782673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40831b0dc30117747a9bf98ef753d0b9c681127cd96f9f85d11abebfa5eb8934`  
		Last Modified: Wed, 08 Oct 2025 23:44:43 GMT  
		Size: 12.3 KB (12295 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d8a0b1798b6837e717df2a58ce2f5653c3cf064617ef1345c7fa2e9d83f35044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338571527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c334672aeafb6097099971d43eda27635fb349cd96669fe6b776259c094c0621`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 30 Oct 2025 21:35:06 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:06 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 30 Oct 2025 21:35:06 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:21 GMT
RUN set -eux;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             rustArch='x86_64-unknown-linux-musl';             rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2';             ;;         'aarch64')             rustArch='aarch64-unknown-linux-musl';             rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9';             ;;         'ppc64le')             rustArch='powerpc64le-unknown-linux-musl';             rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3cfaef0615cb0253cafffaabf7ec4ecc5175443b4ab6064f2e6ee284a050c1`  
		Last Modified: Thu, 30 Oct 2025 21:36:13 GMT  
		Size: 59.1 MB (59143801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9674b249fc5ce80c99c4602fb01c94be64a649a3024dac74778ee94d7db0705`  
		Last Modified: Thu, 30 Oct 2025 22:50:59 GMT  
		Size: 275.3 MB (275289657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:ae5caee0dbfd83810c65df11e27dabf9dcff493e569bade06d6c3cf6dfbe8db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.7 KB (875736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c20db5b6d61ba982bc0de623cef8139d3cca9749848be2c546175c599723f`

```dockerfile
```

-	Layers:
	-	`sha256:240bdbfb8f97567899690facfafee478aa0eea76bee43834ce0e312b2abe7c6e`  
		Last Modified: Thu, 30 Oct 2025 23:44:39 GMT  
		Size: 862.3 KB (862259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f33d22a8ba00cd9de8a1cef55af65f0faaeac769c82fb9d7ff25993b539c3e`  
		Last Modified: Thu, 30 Oct 2025 23:44:40 GMT  
		Size: 13.5 KB (13477 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.22` - linux; ppc64le

```console
$ docker pull rust@sha256:9036b3b6866c1835ae0647bf6e39ed634c24250cbe5ce9323476525325207c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350263091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1c326a8fb61738f78b6e832d76856f610184e585f0bea48eeb0b05acc9a561`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a56909a4c35c502dd43802ef31d4890df3cd54f15133b9f35dcaab1ec3f3219`  
		Last Modified: Thu, 09 Oct 2025 05:14:10 GMT  
		Size: 59.0 MB (59006725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20f6c21afdba425061e0ba687974793c99c42b22eafef8cce1227eb48c95ad`  
		Last Modified: Thu, 09 Oct 2025 08:45:22 GMT  
		Size: 287.5 MB (287524125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.22` - unknown; unknown

```console
$ docker pull rust@sha256:fd67dce82d8a2b47d722b477a74576185f4a69052847396ccba385aec9c0cc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **807.6 KB (807608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c44369fd4d6569b24f091dde0bde6f511b3ece2eeadb14bc5830c655a4e4bf5`

```dockerfile
```

-	Layers:
	-	`sha256:ed8dccf24b40112f8c8bfb29e2beac0c23ea4a599fc28af8dd896d2a067e715e`  
		Last Modified: Thu, 09 Oct 2025 08:44:26 GMT  
		Size: 795.2 KB (795241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417fb1d78b372874952b95cf42ae7f491a90983707634ae9103ede8f18d7de58`  
		Last Modified: Thu, 09 Oct 2025 08:44:27 GMT  
		Size: 12.4 KB (12367 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:863fbd5895cd638392b24e0197f02f94e3f2ad3d8bd41f97377a595324d1032b
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
$ docker pull rust@sha256:3f6e6f8d8725a65a2db964bb828850f888d430c68784d661f753144e5d787207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.4 MB (559447275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc39c88add68c6e4ed377beccd6a659e59b286954d2c7e5c8e5b1dde2a82a8e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279d33abc52c7384e0cbbb666ea22064ea29b50a968ec29ae3ad817f62e16e7`  
		Last Modified: Tue, 21 Oct 2025 04:46:37 GMT  
		Size: 24.0 MB (24028898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa5a418829f3daa90a80438cd84706b5f7fa0c795eb7936874864ef1ab7b0c`  
		Last Modified: Tue, 21 Oct 2025 04:47:27 GMT  
		Size: 64.4 MB (64396405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3556d62e9bd977c17e315ad64979017739fd90fc5a2a89ec07cf82348133f3`  
		Last Modified: Tue, 21 Oct 2025 10:21:00 GMT  
		Size: 211.4 MB (211449932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cabf358425b152d1908f63c0d4471be829cdbdb7e870867b6ff0d00609ccbb`  
		Last Modified: Tue, 21 Oct 2025 12:22:16 GMT  
		Size: 211.1 MB (211091477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b752e3300679d23dbcf05365edca183b090eb1f9ce4dbf386a63ff33fee8b581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15880926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2835758bbb69db26b153b201c88297c845154b61da6c1e3cfb620ab6a7ee50e9`

```dockerfile
```

-	Layers:
	-	`sha256:4abe2dd3e5b0b21ed2011090e044227e18c07d5b7203b58f5721012b36baffc6`  
		Last Modified: Tue, 21 Oct 2025 14:44:29 GMT  
		Size: 15.9 MB (15868950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:447779a4f4a311c28359e75fde4de4d5a8c5e594ad701431360f62b2299162bc`  
		Last Modified: Tue, 21 Oct 2025 14:44:30 GMT  
		Size: 12.0 KB (11976 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:051b0136c8a4e3e112b39e508921112fbde875a02b07b38c87a737e1e81cc746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.1 MB (559108573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be8e386e015e2bb88eaa00172139beb421d17d3570f6121a8fb2dbe27f2e20b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:35:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:42 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178651637d26f6ae6fc6c2a3297b37f8bbef12e80d822930b05b14f51a262382`  
		Last Modified: Tue, 21 Oct 2025 02:43:48 GMT  
		Size: 21.9 MB (21934505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14411cad8875b2a42f951ec95179ed8a844d1522990ec8b96f1c4d269ce3c71f`  
		Last Modified: Tue, 21 Oct 2025 04:11:04 GMT  
		Size: 59.7 MB (59652688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934fb9fcc0f174aa356a518c85a7e2e8a62dd5902afe2a8dbbf58f5f8b37166b`  
		Last Modified: Tue, 21 Oct 2025 06:17:29 GMT  
		Size: 175.4 MB (175355007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a2122d86f314de64147fdae6b5b37d7b95098ae45f73107f366595e6097bc`  
		Last Modified: Thu, 30 Oct 2025 21:36:31 GMT  
		Size: 258.0 MB (257970463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:29db2457c6db102e7a390b4609d14f799d0b4dc98f04e20b278bee9349696010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15685187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840c6decc4d442f284b6c01b397281e4a69f76e76b12d384284a4eb807702448`

```dockerfile
```

-	Layers:
	-	`sha256:8db0f390e801710744db2d01b0058a149ac8d4833025dd5538c43e761de709dd`  
		Last Modified: Thu, 30 Oct 2025 23:45:19 GMT  
		Size: 15.7 MB (15671436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd29c41b660a030fe351fe27c96ba66c2b369e2fa4d46468e264be654f4fc10a`  
		Last Modified: Thu, 30 Oct 2025 23:45:20 GMT  
		Size: 13.8 KB (13751 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b5ea992358738c5ac3d06cafcd8f8274a36b77738ff7c8ac37828322399a6c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.6 MB (519553946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4518efce2e74532fa1aab649f80dd367117838d24a5a2c3caeba50ab3d523197`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:56 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:56 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:56 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15270faa4e93fc4bcc62caecce8d2f5dfc1443d3c99572dfb689973b24c0a4`  
		Last Modified: Tue, 21 Oct 2025 02:35:23 GMT  
		Size: 64.4 MB (64370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6803b5e31b40492f4747e974e6e4ae692982b12beb2b87ed9d9ffbdaedefcfd4`  
		Last Modified: Tue, 21 Oct 2025 04:13:43 GMT  
		Size: 203.0 MB (202958684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3099636657b1560c5cdee62a47498eec65574f75745e2e59dbe17331d4c6cedd`  
		Last Modified: Thu, 30 Oct 2025 23:48:57 GMT  
		Size: 180.3 MB (180267344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:eb1282379cca9bd583c19b02bb212db62b40aedd81ce17ed2fb038637a279a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15911254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee670b912d558498da8a680449137c57f480fd39afb5dcb916fa1b657838370a`

```dockerfile
```

-	Layers:
	-	`sha256:310f60a24c03dd47886646e436808491680a7092f501e1625c0b0137803aca44`  
		Last Modified: Thu, 30 Oct 2025 23:45:35 GMT  
		Size: 15.9 MB (15897478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f59b3162dc6c5eae0e6dc9c486d6af675e4ee71d672067d47e274f3c0c9d0fd`  
		Last Modified: Thu, 30 Oct 2025 23:45:36 GMT  
		Size: 13.8 KB (13776 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:3df2b6dd56af4590d062038eb7ea187a744fdaf081514e183042ff7d02854301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.9 MB (588911073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e8ebf3e452e9009e6ac8977f62eeb4677af9d14fe10adff5b5a5229350c519`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3426ba65368da59a25d050cab9d7713d7873264014ab6dfaa6b0c33f0632cb80`  
		Last Modified: Tue, 21 Oct 2025 00:20:21 GMT  
		Size: 49.5 MB (49466720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f14d3e3fda83046fcd165bb976221020273830b54d963f634e53e7796b47053`  
		Last Modified: Tue, 21 Oct 2025 01:52:59 GMT  
		Size: 24.9 MB (24864208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39058bc352da86cee9643b9b447133a3295983ec455cdba2fac6cbbed8726db6`  
		Last Modified: Tue, 21 Oct 2025 02:35:47 GMT  
		Size: 66.2 MB (66231902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed15f8c1488a55d242a6bf3226b75c0d0de56631f3ea18bb327cec39013003bd`  
		Last Modified: Tue, 21 Oct 2025 04:13:40 GMT  
		Size: 210.4 MB (210381245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284a00e05bc16cf43c2f874e7ffa10dfd7a2b9db4a6677907e35dd79fe9a958`  
		Last Modified: Thu, 30 Oct 2025 21:36:44 GMT  
		Size: 238.0 MB (237966998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0599233bf7ca1dbdaf9211ea1d633238a82678ba0c72f9df870614f4db971837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15859504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ad9e5af8c0e73f8cbf71baff9a986c09dce838cd776e52aef2bf3deb361ccd`

```dockerfile
```

-	Layers:
	-	`sha256:4507749c6cb049d9b9929284ce90ffcbb7ec4eb94fb4c9c0262e135f7fc1071f`  
		Last Modified: Thu, 30 Oct 2025 23:45:50 GMT  
		Size: 15.8 MB (15845864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e4d18122dd7bb11ec0aa43861a1fc3f5cff14e9b8487a97a8493193a79c5282`  
		Last Modified: Thu, 30 Oct 2025 23:45:51 GMT  
		Size: 13.6 KB (13640 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:9eba237a8a91d4d4b3daa3f9b16925ee32acaae05e9f4140bbe52f0f306291e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.8 MB (650761894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90a0390e5c3f2327709ea58c4600fdaea64e7b2d73feebbf945b0c74868610e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:297b234228c60cb6a9bc0156bdf582119f3c4f22112d7d2e8128e4d1403158cb`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 52.3 MB (52326787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665a6d4e6976a738d68a77f188daf2501160c6ad54e4788282d2395e926b5e6`  
		Last Modified: Tue, 21 Oct 2025 07:42:57 GMT  
		Size: 25.7 MB (25672119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9014e4879ede8e5983b7a1a0f265054143b5d897d5a848c01fe4c938fdaa27`  
		Last Modified: Tue, 21 Oct 2025 17:30:59 GMT  
		Size: 69.8 MB (69845634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56011ccaf4727bb2311ac874db524178647f03b759d374824a9593362ec2964a`  
		Last Modified: Wed, 22 Oct 2025 01:54:45 GMT  
		Size: 214.5 MB (214489889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39aaba2f0db3400914a4e2127ac5540b1f081213e989e48c3c3237d2f8b665c`  
		Last Modified: Wed, 22 Oct 2025 16:06:12 GMT  
		Size: 288.4 MB (288427465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bb4c74d769d3c2fc4ef7eda580d7fa1c9938cbfd1c2b38121b8091a1ffbaaebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15857497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1969e92357e8b86e012df9d155afd7d29441fccef237fc92372a75b1627b2016`

```dockerfile
```

-	Layers:
	-	`sha256:4b4b17fa7f4c21642766fab5286c683a962e3ba61375736c767f61a550a06434`  
		Last Modified: Wed, 22 Oct 2025 14:45:19 GMT  
		Size: 15.8 MB (15845477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08c81e19f8fe22fd88d08411312c59342f9439abe4bcce945bdb4fde2da63d3`  
		Last Modified: Wed, 22 Oct 2025 14:45:20 GMT  
		Size: 12.0 KB (12020 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:697ff40e2e322426b97c54857174bef11b523a775040bd451466892908de2bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.1 MB (615060656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4faa2b9c9fb04ed6c7fb91522e3b4ad2232170657cc84637e5cca4b424cfd02a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 22:39:51 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:39:51 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:39:51 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca271e8b0e27269a77c65ea555986eaaadf5db02b1ac24f66f8ce2e45a475b`  
		Last Modified: Tue, 21 Oct 2025 22:50:23 GMT  
		Size: 24.0 MB (24027291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944e6bdda425b877e973cde5b6c8eeabf7eed45bfaba0fd705b4f180a07f001f`  
		Last Modified: Wed, 22 Oct 2025 06:00:23 GMT  
		Size: 63.5 MB (63501423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7d40c47b93ce5dc5166e5aa44baae913a478ae1ba5f7865fe24556acef9200`  
		Last Modified: Wed, 22 Oct 2025 14:21:48 GMT  
		Size: 183.5 MB (183485270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1617ee534ab322072d5a49e5b16309a0c49cf8b0232baabd7f545d5675371d`  
		Last Modified: Thu, 30 Oct 2025 22:43:17 GMT  
		Size: 296.9 MB (296909151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:478d1ea453072bde935424c02d4c412b2552cb3b6f3802e364b9daa69bb78b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15690219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9dc7449fb5d0d433daa7aa7b48a617e07616fd804e869aa43d91049e329468`

```dockerfile
```

-	Layers:
	-	`sha256:e5617194576bbf4d19500cc175ba3bdd7dc056a09db6529ed35a8a3df0ebac65`  
		Last Modified: Thu, 30 Oct 2025 23:46:22 GMT  
		Size: 15.7 MB (15676546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f013fc0c2ae0f7a32936873b795b686a9fe5f9867e41c993b818dbda395aa7cc`  
		Last Modified: Thu, 30 Oct 2025 23:46:23 GMT  
		Size: 13.7 KB (13673 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:e0c87d49c7c5eab3d5493afa6ed718ab3dfc68fff1b046553eebd69bb712f21e
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
$ docker pull rust@sha256:ba3a8b9eb24de14c1879efe8acff7d4eb747723ca957e0d2409d0bc2ea9f84a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.6 MB (532573818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90deb942227e65f117f7086b8b8e0d4b8aabd132e494b2f6da8dae5a8aea8660`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b6f830cd306f01980373f1e0120f2d00018fbe51a9506b7262f5d9e4bbda74f9`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 53.8 MB (53756115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfa9ab09db8d94503213f634b29be3505174979f2e0c6e3fd46c2acc0716c25`  
		Last Modified: Tue, 21 Oct 2025 04:46:42 GMT  
		Size: 15.8 MB (15764056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e663cb3204c49ebc21b005f5976ee62e4f00b632aaa8000dbe6db86d9cde2a1`  
		Last Modified: Tue, 21 Oct 2025 04:47:30 GMT  
		Size: 54.8 MB (54755162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bafbf91825be17f2ceae6674de95a31e6f8a5a24c7cb95ae123d19de9c63e61`  
		Last Modified: Tue, 21 Oct 2025 10:22:52 GMT  
		Size: 197.2 MB (197204867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2934a4a54c0280356719b64463655074b644e9cce9b90e0856432515bc70324c`  
		Last Modified: Tue, 21 Oct 2025 12:34:54 GMT  
		Size: 211.1 MB (211093618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ada36de672c97de12b518347973806e954a9857e39a4a99a4a78ca6e6ea4fa6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15475300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6b018c655fb9ea7fb0efcc34ce311abbe59313ea016dfea5cc4330f70bfb1a`

```dockerfile
```

-	Layers:
	-	`sha256:0ffcb85ba366a629649a13c3dd79c68a97772f673c73b252ca6e6f8f611b7453`  
		Last Modified: Tue, 21 Oct 2025 14:44:36 GMT  
		Size: 15.5 MB (15464051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772732437b28b188679156785245b01fe3aa24403d84d740b9257f330059f3d1`  
		Last Modified: Tue, 21 Oct 2025 14:44:36 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:4debe238b6bccd468958311c5ee086154be57fe1f47fb1e17e9a3357f90139be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.5 MB (540499385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a512f11edcf77ed82a2ac07b66308eaf931cc80877cb617b60b8f763011be2f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:35:30 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:30 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:30 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:680ed921e0c94a719af1d242eac2d0c1be8482153680a3940f3435ee5598303a`  
		Last Modified: Tue, 21 Oct 2025 00:20:24 GMT  
		Size: 49.0 MB (49046121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c68013a317d7d802bb25c57a724c8753caec2fc7f0e78fc13f9a38fd22ecd4`  
		Last Modified: Tue, 21 Oct 2025 02:44:25 GMT  
		Size: 14.9 MB (14879264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895fddf2807e047e5b02e5418fd04d343d3e9b5b393b2f3f0cd6704cad44b8f0`  
		Last Modified: Tue, 21 Oct 2025 04:10:49 GMT  
		Size: 50.6 MB (50628495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ef331acdad14a3d1bfe859a1c645cb9f4b9526e16e3fed550eee6b86681db7`  
		Last Modified: Tue, 21 Oct 2025 06:17:35 GMT  
		Size: 168.0 MB (167976463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2345c283f9f7c727f33c6a1e2c5ffa229106bb1e7b3f3f2073146f627866f815`  
		Last Modified: Thu, 30 Oct 2025 21:36:20 GMT  
		Size: 258.0 MB (257969042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:9f6a16886d335243aaaf88af9f27e0a70520e083485569ce2cca1c2bdd490b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15275978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f206f730d7eeec8a3b422fc88a2602f2e8f4d5d0542c706027b0a2fe2928a2b1`

```dockerfile
```

-	Layers:
	-	`sha256:69bab675147da3f449e5f163a075b2d55e9aa4ed4021b6e356a242df2ef4a59a`  
		Last Modified: Thu, 30 Oct 2025 23:45:27 GMT  
		Size: 15.3 MB (15263395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac6fc96e9abd4822cf5b32fc13e672b114ae72330f34d3a5301f3009e139e4b0`  
		Last Modified: Thu, 30 Oct 2025 23:45:29 GMT  
		Size: 12.6 KB (12583 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bdd72efd5f91a90aa1746b27a7cd1cc1ea77ae0606dc1e0bb9ea3fb1c4adb42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.2 MB (493232128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a548930c92a6745dcce895941534ec91e5af27593c0ae426e760e382ee6bcf7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:39 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0a72c4e347b74aa6a0086cf3d1d928528ab02577a17bff4e22366a7df681f564`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 52.3 MB (52257444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f7bdca064e682157394f36dabd112bc9831aff9743216b035e2ccccf704cc3`  
		Last Modified: Tue, 21 Oct 2025 01:46:24 GMT  
		Size: 15.7 MB (15749510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc7a49f7691cb1ac5f0f40edbe6f4beec62021b4fd2544c431d8f694b4b4647`  
		Last Modified: Tue, 21 Oct 2025 02:35:21 GMT  
		Size: 54.9 MB (54860806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0452b809e62b80ba90b1a217898e5cf7675ff6aac67b2967e58600172590649e`  
		Last Modified: Tue, 21 Oct 2025 04:14:12 GMT  
		Size: 190.1 MB (190097178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1493ba40974f9698cde6967247a220e8b21c09de76901470d4a5ed125bfc1cb2`  
		Last Modified: Thu, 30 Oct 2025 21:35:20 GMT  
		Size: 180.3 MB (180267190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:174a6996165236196e2e2234b5a3e3fd65d247300e29913fdf2df1ee0adea225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15478629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e3fdfeaf6bf3fc08da419feb6196d81eb718e95950ce77f11a97ffb49dcb98`

```dockerfile
```

-	Layers:
	-	`sha256:9196d2d341db75ce952d1a4e29bd491214fe5bb55b9f55a90c7343d81100d44d`  
		Last Modified: Thu, 30 Oct 2025 23:45:42 GMT  
		Size: 15.5 MB (15466022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915a2f913a028e29271d667bf808cdabccd5dc980730eeb68ed9556c1750d267`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:ebfb2e206c2b74a1bb2d9b549cf50bddf2c1313e09fabb019c831ae5f7495a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.1 MB (565086977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0f7bf5bc46fc016e2a1fbd23835673151045c1b511f6c146c2dd9d721eef6c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:32 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:32 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:10d430deaa3d2ab4898db053e80d62403503897839bf6efd17ed5412b18d7973`  
		Last Modified: Tue, 21 Oct 2025 00:20:39 GMT  
		Size: 54.7 MB (54699294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c453fe6b4c7a680d5464137a3450d263e01a7ec4d491659295432d36b0198bbc`  
		Last Modified: Tue, 21 Oct 2025 01:53:19 GMT  
		Size: 16.3 MB (16267847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96adc169c4af311ffba07fa68db5821d6b9b00d285e00f44dad87eff52496658`  
		Last Modified: Tue, 21 Oct 2025 02:35:42 GMT  
		Size: 56.0 MB (56048779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd845a5707f187f6670f0831bc55034f6333f3aa3eede705f688f3c3342392e`  
		Last Modified: Tue, 21 Oct 2025 04:14:36 GMT  
		Size: 200.1 MB (200103484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae4b0e0faf517253d9eb9d5185f476ec1cdfd4f000a81910c9827c0acc7d451`  
		Last Modified: Thu, 30 Oct 2025 21:35:16 GMT  
		Size: 238.0 MB (237967573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:66f198e4ca90d5791b0a7ff640ee5c546edbfd2e0dfeb179fb4f174b4be5814e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15463224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d7dafb0e855c67125a259fe625f7a9d7f828eb79aad926e34bbb81d981988c`

```dockerfile
```

-	Layers:
	-	`sha256:1b2ab51fb7cebaa093a1da9d9de0794786d042ff60414a0211a492701aab92a9`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 15.5 MB (15450753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fd7b2b4922a57612d543c90720e157bdeb2bd2a9b6c5aa37cafabc33a2328f0`  
		Last Modified: Thu, 30 Oct 2025 23:46:00 GMT  
		Size: 12.5 KB (12471 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:4cdae04e9e94e189ab2a6b462c93ed5f8ab248cde1c6100c59e958976b1c4594
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:latest` - linux; amd64

```console
$ docker pull rust@sha256:7ccdba2b655ebac8408566b54b8dbd02b44756759e8d73109227edb2b81b2942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589704892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd127f46648e9bce2a1ffa8096f2babd56565f986ae96fa6abef7bc6fc290ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d573bf42b377ce6a5a0451c15388849686fa4058efd68999f3b014daeb5b55`  
		Last Modified: Tue, 21 Oct 2025 01:42:47 GMT  
		Size: 25.6 MB (25615545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dfe2fac1c486e9aaf41d1028ed30be2c442aa84af44462bc7bac8c148ffb13`  
		Last Modified: Tue, 21 Oct 2025 04:47:38 GMT  
		Size: 67.8 MB (67784857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d5bd8a8d262418bf22e705535ce38c6789dc72e319d76b30aafa5c331b6924`  
		Last Modified: Tue, 21 Oct 2025 10:24:40 GMT  
		Size: 235.9 MB (235927971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68557728bac69b81da96dae42ed23a374347244afaca7210e768400aecefb4d`  
		Last Modified: Tue, 21 Oct 2025 12:18:46 GMT  
		Size: 211.1 MB (211091548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:c6e9c920b84edb3271e9884c7e7d7736fa75456c61d869517d117f8b006f02f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17223403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0af01840a4d7313dce07a4cd8705141858d215468038f488a00bc2983f4203`

```dockerfile
```

-	Layers:
	-	`sha256:4de25e75936e713c9998f626efb488832cbbc139588b1dab75dee11b9e80e7da`  
		Last Modified: Tue, 21 Oct 2025 14:44:21 GMT  
		Size: 17.2 MB (17209918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f86274d8e899d886607e02351051d3409137c5b77521eb87725d6ff4cfb078e`  
		Last Modified: Tue, 21 Oct 2025 14:44:22 GMT  
		Size: 13.5 KB (13485 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:df192b38e9142bc8d454be61de04235e6e3d6e3cc142b3ca4461565fdcdb5c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583252486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a735b8020181b775c6ff35bd4f4ddaf6fccacf90d6baef0e5b88f5fac468e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:20 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:20 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:20 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cda7f0b38d756bba039d1251605b315c32a18bef1d71d1a0a98df8f4c7fb6`  
		Last Modified: Tue, 21 Oct 2025 06:18:01 GMT  
		Size: 193.2 MB (193235864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7085e104656ea6c66d8ba95df53b71fae0ae8c42dce84c36d3dd51cc63114cc`  
		Last Modified: Thu, 30 Oct 2025 23:48:47 GMT  
		Size: 258.0 MB (257970062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:7bdc29f59dfa654c3d2300e1d752366f54275c8759cf65ee11f3b51b5ee02ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b60585f52529edd183ac79b90c91a6c5c7a9f7718df436557b6c48120de964f`

```dockerfile
```

-	Layers:
	-	`sha256:e7514cf6a08ba2c22ef71f6054b5e755385f65048788dccfe2a655928e7613af`  
		Last Modified: Thu, 30 Oct 2025 23:44:49 GMT  
		Size: 17.0 MB (16977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7716c3ffa9ab429830b3182885b3f920b00e895ca1ca6dc9aa0e0866b3405617`  
		Last Modified: Thu, 30 Oct 2025 23:44:50 GMT  
		Size: 15.5 KB (15508 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:69d4bc701fcca1d78e46d634aca8f1b0a3b967b755e87d0c3e883abf402a92c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.6 MB (548594894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124905d571200dee29c0250b5a56242cbb369d8d6a2f46770ef2060b9aa6ae19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:13 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f695ddffd81064f15ea19428e2d643e8b560e48e54ae801a8d63c45ad6ac29`  
		Last Modified: Tue, 21 Oct 2025 04:14:42 GMT  
		Size: 226.1 MB (226078014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b0009962587465f15c28cbaa4e05bede4600a6b68c86467eb69e4227df6c84`  
		Last Modified: Thu, 30 Oct 2025 23:44:37 GMT  
		Size: 180.3 MB (180266565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:a2ff1f30c17e94d0edaf28e068fd1a99b76f759cebd6a2b304606e7c085f21aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17309822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d625100634edff47e63fc8b469129a68a25115bad3e0531a1f7b594067d865`

```dockerfile
```

-	Layers:
	-	`sha256:b3eb795d70d03f35b63225b01143c51f0f8b6622f4022cb5db697d2ba9e108d7`  
		Last Modified: Thu, 30 Oct 2025 23:45:11 GMT  
		Size: 17.3 MB (17294274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f42745a111fee91795bb40aa7014469e06556069a7271890a09e381d064bfc`  
		Last Modified: Thu, 30 Oct 2025 23:45:12 GMT  
		Size: 15.5 KB (15548 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:0f36b8c5b45a1403f31ae3e1f2db1be6126a1a8d3d89157dfbf1a9caf8364a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.4 MB (625391663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5670c24f999c8b72981507cb47d2b2dcaf53d09af6a4187abbd6fe21f62d48fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:12 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e11ad5a4fd5be41f07ac93311f8ae1f7dfd6455edf9f5cf950e26d70ee4c6`  
		Last Modified: Tue, 21 Oct 2025 01:53:30 GMT  
		Size: 26.8 MB (26775679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e99453a1ea6755d1a3a58fe6632281db5820c733291dbefe645ffd8397c7e4`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 69.8 MB (69795039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4be1d74f0f5cdfd17973a37d16dc7ed75a3f628a94c99be57d59571d3a9b4`  
		Last Modified: Tue, 21 Oct 2025 04:13:56 GMT  
		Size: 240.1 MB (240053433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b95b67c6e22caf5578ea1eddb03fde4e1cedc03293a23c829f701c73cc927b`  
		Last Modified: Thu, 30 Oct 2025 23:51:31 GMT  
		Size: 238.0 MB (237966938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:de9c5a2a0cb7e4e8b0375014aeac39baef1c37299b1295b32c691537e29bbdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17193526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7797bff6bc0b961011e7f5b876cc1e1e46af5fb5bb27dddfa8a0836045fbdcf6`

```dockerfile
```

-	Layers:
	-	`sha256:4ba4d0a028ca002c9baa8b6e271bbed6f0b707811424f49afb3dbed5b7bbbc66`  
		Last Modified: Thu, 30 Oct 2025 23:45:27 GMT  
		Size: 17.2 MB (17178183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f46fff4553bf23d62e5ffce1a59bed624919c2fea3703b65b013ef50394d42`  
		Last Modified: Thu, 30 Oct 2025 23:45:28 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:a29f6e27737a6b59309a166a28c4cf97dd2eefbfa88c3aca3304faa0ff08a3e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672649528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a952fb3ef83a44fc6533607fda15f4d747a2350849923b66222c95ce97864c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dfb88672cf0a942c4fdfcadf1912c35c9d30a3a001b18a9dad505fb960ae8`  
		Last Modified: Tue, 21 Oct 2025 07:47:00 GMT  
		Size: 27.0 MB (26996207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06029381e2f1b3a0885caf1b758b0461bfaf9db7b9642ca0b79ab28ed1dd4ecc`  
		Last Modified: Tue, 21 Oct 2025 17:35:58 GMT  
		Size: 73.0 MB (73029685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac677cb325b211e7ad7714eb6d52abf13c0d7630be372cac77812dd27241a158`  
		Last Modified: Wed, 22 Oct 2025 01:27:43 GMT  
		Size: 231.1 MB (231086523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff2e4d4f9807f075e3ff5c6c28631a324397b2b771ee6555b6d8e923ee06e0b`  
		Last Modified: Wed, 22 Oct 2025 14:51:26 GMT  
		Size: 288.4 MB (288427637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:f33a0240a7d92b5fda177a193f6e7c05cb951abb7c29daf3858c351311dbac60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17209060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36284e92be8526f5f13c82a2f801a21cf15d46cdae17422ca12254be41d6339`

```dockerfile
```

-	Layers:
	-	`sha256:3d6645f5d1a853359ab88d5ea6d06cd386d73bef8d296c30d6ee843f5dbd6028`  
		Last Modified: Wed, 22 Oct 2025 14:45:21 GMT  
		Size: 17.2 MB (17195507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0297a39c3c72137eb2edc4ce4ff2993062b460caa31ef206b40f28e10b1fe71`  
		Last Modified: Wed, 22 Oct 2025 14:45:22 GMT  
		Size: 13.6 KB (13553 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; riscv64

```console
$ docker pull rust@sha256:db568b830f6fd90592497dd0eda8001ed384c555723f1082ceb67a49b9968c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.7 MB (731746485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dde95f55f8cca95c0c52acf2dc0afce27141a1ec0354bce98292db2d8245a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:41:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:41:49 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c640441904d97046ee4a137483e3b6745e0a18782c3b688fede8e9ddf18261f`  
		Last Modified: Wed, 22 Oct 2025 18:09:29 GMT  
		Size: 25.0 MB (24953874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb6fec5cd2588ba9a09a9491547b6e7005f3640a81c530cc1f2e651257c901`  
		Last Modified: Fri, 24 Oct 2025 21:34:03 GMT  
		Size: 66.7 MB (66662364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c02978248d2c72ee734dd5ab68325ab5be1edbbfe6026472d198390eabe8cf`  
		Last Modified: Sun, 26 Oct 2025 13:26:52 GMT  
		Size: 322.8 MB (322829684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af21d31669ce50f730bd664ae7d97ab0697a48fc4c1fc527c93c32c6f717c3f3`  
		Last Modified: Thu, 30 Oct 2025 21:56:54 GMT  
		Size: 269.5 MB (269530257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:5d2476fa78b8cae7f942b74725782b510c4b6a2f687346c648591dd4613b5b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17281556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c73611675d5101a89fa89d59b3a33599e9498dfc407639e4c3b51d2879ed92d`

```dockerfile
```

-	Layers:
	-	`sha256:de5eee62216cb8618afba94f9d4c277f9a550568818b3cbe17aa78900016e6f7`  
		Last Modified: Thu, 30 Oct 2025 23:45:56 GMT  
		Size: 17.3 MB (17266092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c38e4c4e014047f4332c3cf3bf8372bf0ff126eadb475671eb5f6759bb6503e9`  
		Last Modified: Thu, 30 Oct 2025 23:45:57 GMT  
		Size: 15.5 KB (15464 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:58124806371c4a39a5ac92593a6f823c354d5d002cae39305db81a0b200dc7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.1 MB (648135109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571bb1f5470229ff143899581ee0538e785fbd8bb45168569fa265be37201747`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 22:48:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:48:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:48:48 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9f518343ed4506c34ae7900f538c56bac66f4fad9740034ee8b819bd8d15e`  
		Last Modified: Tue, 21 Oct 2025 12:43:19 GMT  
		Size: 26.8 MB (26783314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb7d34d2ff189fa2150ed8d82914c7669f312817531bbe187965e9d30825d3`  
		Last Modified: Tue, 21 Oct 2025 23:25:03 GMT  
		Size: 68.6 MB (68630635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4131ad2e1cf6d0e51274c6e30ebc34015c8e72c5b79a0146220944b33c750ff`  
		Last Modified: Wed, 22 Oct 2025 12:46:56 GMT  
		Size: 206.5 MB (206460184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2905cafaed65f05704ab3b4e23479ae861bb4a148a0aac8b459931962ccf1469`  
		Last Modified: Thu, 30 Oct 2025 22:52:24 GMT  
		Size: 296.9 MB (296909277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:54a2179f33db9cea350dd680ac4622e0df5e333f36232801102916c3b7ff749b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17002545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c6960bfd3415ad92fd83afb42906df93f6f114175be156af8cd8f842cfa20c`

```dockerfile
```

-	Layers:
	-	`sha256:24c7152c5b9ea076d3348e04b2479b166ba9b19eff01141c458fb04c53fdcdd6`  
		Last Modified: Thu, 30 Oct 2025 23:46:10 GMT  
		Size: 17.0 MB (16987149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc6358b456c6334b83aedd51c445eeedb3650635525e2e50790b42a8d5968cd`  
		Last Modified: Thu, 30 Oct 2025 23:46:11 GMT  
		Size: 15.4 KB (15396 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:79e8bbf426da1710dea53aa80da3ba8823060dc1761e6fd2a92c49e0f4809c76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:slim` - linux; amd64

```console
$ docker pull rust@sha256:618466f4caae45cd6b7b6adfa98764ad462aacf67e7149c6d277c625da9f1282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316292209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c7ce709bce953db30bba7b3470638840d37d0e0a97220d6ba0542ae17aad67`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de44ca22a261b7801f942055dc9512f4e262e99021abda7f616cb77e45f2ac15`  
		Last Modified: Tue, 21 Oct 2025 08:48:56 GMT  
		Size: 286.5 MB (286514285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:65edc8293295cd16da8bf098701a6a507618a7dd2a9331e3f668a57ffe1c63df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4178629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6aa3d298b90262ca1f963f745149eb9cd429a8e23605e7cdc8ed89a4a4bb2f2`

```dockerfile
```

-	Layers:
	-	`sha256:4a5d4e539b906905d0a1a8cf26f58a195fa73f0755e02e96c515a60213341b47`  
		Last Modified: Tue, 21 Oct 2025 08:45:29 GMT  
		Size: 4.2 MB (4165011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e92458c8a75e4c47ff513c54b479567ce494fbb4081e948a711085a94e7b4b`  
		Last Modified: Tue, 21 Oct 2025 08:45:30 GMT  
		Size: 13.6 KB (13618 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:36bd228e236519c3a747a87570e7f83dab399d17eca3ef372e6484c3055c6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334448212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c202a0d535ea0887983203aae69fdf71f527951cf86b2b21f3fb6c2cf9a538`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:37:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:37:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:37:12 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6e00fb9e9c84f34ed2d592246743cef540466ac4115722b315d862bccdbb44`  
		Last Modified: Thu, 30 Oct 2025 21:37:57 GMT  
		Size: 308.2 MB (308235318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:4e20e1ca9b0f23d783ec6d6ed5be8fa58ddaf53b726d80cd6fe80cf82a708eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b868546b1ef1b0edf1d23ec51f66614251da1094f46405866d3bf09b052aecad`

```dockerfile
```

-	Layers:
	-	`sha256:14738f7012d7020bd06896025d57d8d8f840e853cca38898526091bad7f49804`  
		Last Modified: Thu, 30 Oct 2025 23:45:32 GMT  
		Size: 4.0 MB (3969887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da73b8e3cdf4379799012870a7c21e494173161ddc8b1b353fc501f5632e4cf`  
		Last Modified: Thu, 30 Oct 2025 23:45:33 GMT  
		Size: 15.7 KB (15744 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8f015c79dd7ae0d1ab3218f86dda57f805a046991a5a67aa40088a67965806e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280064640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ccfb92e01921c8ed8fe03746498812688fe017b71f41f9e31a6cea79147abe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9e403b0cf550d52dedd0ab0aa7cbdcdd11f44b28ceb00d624c5c3d50a41df8`  
		Last Modified: Thu, 30 Oct 2025 23:47:09 GMT  
		Size: 249.9 MB (249922513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:cc442428572057302c62370a3c8514cb787a1a7daeed774b9f01e3a53f53d5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96a2c18c7d5bc0df280a6b286dc537b572cbe31668fcf2ad169f1bdf85194d`

```dockerfile
```

-	Layers:
	-	`sha256:606f393a1954d59bcd6d8915d68d376cd05d29024f9a559d92c8ad47da7baa53`  
		Last Modified: Thu, 30 Oct 2025 23:45:37 GMT  
		Size: 4.3 MB (4256227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32db46c306be7344e9ad5e0d189a1f9fccfa49d28d6336ecf1d9609a07d3da88`  
		Last Modified: Thu, 30 Oct 2025 23:45:38 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:ef194da922ba0594e7b7ddf8676004948a82926c4d57ac47bf5a47d85b43d571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341758796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4548274d12a2843de650e527ef6fbf4c3a6d29412091c3b2129c37809a899eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:52 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e995015b3e24125a0c10003ec7b1e384ce24f06f88cbd49bce3e36d2e4ffd8f`  
		Last Modified: Thu, 30 Oct 2025 21:36:35 GMT  
		Size: 310.5 MB (310464168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:5a52de8d007cb783912f98e3a2bc9ef1bea117a247b300d3bf0ed25db3ef7b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05360c911e791bc9a471f2026d992be7509b06ede83672b314adfab6d540bf4b`

```dockerfile
```

-	Layers:
	-	`sha256:657d29bb5c22513fcfdf6fccc85d309ca3ac85cc4258c72801d105ab1c31c57a`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 4.1 MB (4138524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed724e78f81430b3f4c6c9bf61b7039d1389fa37f5495feb17edb5614799f43`  
		Last Modified: Thu, 30 Oct 2025 23:45:44 GMT  
		Size: 15.6 KB (15579 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:72b668dd78a23c4a07810e311f75b18800d78d8b842f464b61ebf09659fc734a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 MB (388910993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11aecbbe059663e629a6a1abc931ed99632579ce2b826607539fd7c5dbe41e57`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a2a3e69fb5be32fda430122dfe24ff452aed1c97ebc7a331f684085f9a9caa`  
		Last Modified: Tue, 21 Oct 2025 18:09:51 GMT  
		Size: 355.3 MB (355312475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:4051cc4a20c93b4a51262e6e33ba8be0c65a6769b70b76e8486124d3f31b7cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddf9a019c7107abe4e7b64c25d8cce534229de6341057921d82c64ec2afc5fb`

```dockerfile
```

-	Layers:
	-	`sha256:f9375169da8a2e632c640de11742ddfd32dcdc88e874a300d9caedcd94bc08fb`  
		Last Modified: Tue, 21 Oct 2025 17:44:42 GMT  
		Size: 4.2 MB (4161472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72f384288b484aab5875d8e0d36379250accb364045389bd7d5b1c897f9b7a0e`  
		Last Modified: Tue, 21 Oct 2025 17:44:43 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; riscv64

```console
$ docker pull rust@sha256:aaf1ec04eb2b47005e3b8560b0ab3fa83b42cb6b8c8cd6c6eb55a3c1ca29fd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 MB (391690936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd90d32888708414dd2407217bdbeb9884c97b7b7c8bf613038f97a472c8c4f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:00:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:00:19 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2315ad783eb28b652f5440fe195ec3068e8c8429c644f9745c84f8c522147`  
		Last Modified: Thu, 30 Oct 2025 22:12:21 GMT  
		Size: 363.4 MB (363415286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:b085520540a279fab989fbd055fdff984bfe91d00f603dc6d9c1ee6747d497ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cc7bb3bca0e889b9a141380fcd0cf516a70126219e8fbac44ce160e69a9225`

```dockerfile
```

-	Layers:
	-	`sha256:e20ad570b9c4befd769026dc8b5716c3cf74fc0c6bdbddae3ab6e42e13ccdf5e`  
		Last Modified: Thu, 30 Oct 2025 23:45:53 GMT  
		Size: 4.2 MB (4239428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8670d848e45c5e062ecf29084ab05335daba00c88a567e96c2cc5fca9b04fbe3`  
		Last Modified: Thu, 30 Oct 2025 23:45:54 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:38ebb79c4b041ab046e504b5de098381f8027201a2594744a1eb1fecba242ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.1 MB (379117853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd57e4210e0c402a7b13d84e7dbf8a58418c9777b67aa36fa3c2222c9bae1144`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:54:35 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:54:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:54:35 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9805f4fca0189a31ca7f470c6efdd8dd933a751f5e840c7dbe3eb3034acef906`  
		Last Modified: Thu, 30 Oct 2025 22:56:45 GMT  
		Size: 349.3 MB (349280598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:e2b502b6ae9b904b73922a60e8ebe8814262ef8cb49c465af48c8494dbd80fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5388a6f6d7beec83a26ed19423edba57454d4145bb7d7f5aaefbf1faaa6eb99d`

```dockerfile
```

-	Layers:
	-	`sha256:51b388bf3623dd03362dcb15f7452b4677d633e967a003b3bc39faf47e960502`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 4.0 MB (3982759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a69eb51b743dde6eed89af2bfc049b12313cde5e899319a66fa67ebbb2c5ac`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:4abb5e12778478ce3b5677763cfac7b548364550163f36170fda96e3b3dd384c
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
$ docker pull rust@sha256:4f572135209e89d488fadb81d8a07309857f9b9c5280b54c85a44b71629e8cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310087390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd87f1b314f1f2fdc33693c2d57a945f5597602f63261311dbfe7debabf73393`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3a41ef4bf77ba6860bf1eb6281bdece6349b93d33e84d3f8445240f8062abf`  
		Last Modified: Tue, 21 Oct 2025 08:46:30 GMT  
		Size: 281.9 MB (281859069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8b0e00390a9a6c8e7a5b1493e02e15aabc96eb6b2abda74dc2664f047207be55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50eb0611fe6868b1ac58de80a9850ae872e1020933a9d57c03213a1458bbe096`

```dockerfile
```

-	Layers:
	-	`sha256:0baa4d2138bc1798e0eae0ef60c7b41dff4596720c43a883c93448d71b6db064`  
		Last Modified: Tue, 21 Oct 2025 08:45:10 GMT  
		Size: 4.1 MB (4095479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa65cc6e87b30f22cc9142de730e39496af45a42e414bb528eee3db369a8a41d`  
		Last Modified: Tue, 21 Oct 2025 08:45:10 GMT  
		Size: 12.1 KB (12084 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:1a66676e5c0a918aa45dc2fd4f34c16341d8bd0d064bcb7d815d84948da34398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329757809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c700e6793c04e8485ea32a54a1c3181ceb258694c1ee891dbaa530f552a2137`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 21:35:35 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:35 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb5b7bfc507827968f205851cea67b7a646a133c9116ec8737777be53b48787`  
		Last Modified: Thu, 30 Oct 2025 21:36:19 GMT  
		Size: 305.8 MB (305823786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4d727c9416ea7aa7accb2b6d82a1f1de5c78dc426821a57097eada3482d424d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3389581a9eef53aef89c9fe9accc7fed4cb4a49b423420c31e055cb167a7c7de`

```dockerfile
```

-	Layers:
	-	`sha256:9a1821533a3548a60f32478502545e387b5512c73dc2ef81518a839c820dfd39`  
		Last Modified: Thu, 30 Oct 2025 23:45:42 GMT  
		Size: 3.9 MB (3909876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6ed7f684cc050dc1b7ba74ce805f9039dbc61ddf92e8fe680bdb0a148f49b5b`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 14.0 KB (13964 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:756adb3f9d5c27df7bda4994157cb1cdca4cfdf76b8067a906ce5ff86976859e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274222169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0949ace3836ff38d491823d42f6201e9900fc4d22cf7a1b5d1e486cb355cdd9f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 21:35:36 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:36 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:36 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1f6c6c415a2d4c2edb9805e85b4dd69f95451b08268ffadfa1cdc061e695e0`  
		Last Modified: Thu, 30 Oct 2025 21:36:13 GMT  
		Size: 246.1 MB (246119979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:26a1086edf6420fbae6f26d20f0a2e8dca444eece965956194efe35e03d12a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b8fa2cd2b51fd9918b40c6c59ef73fac18d50aeb2bda9819c79a14219bcd30`

```dockerfile
```

-	Layers:
	-	`sha256:49e6348f3e8ffeac0bcd864980bf5f66c031fe768ed1d3c96c76d88dc7d4580f`  
		Last Modified: Thu, 30 Oct 2025 23:45:49 GMT  
		Size: 4.1 MB (4117775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90e56046bfcea1eefde6da940a766b28525d88059af7258ec565aa8e2c50f09a`  
		Last Modified: Thu, 30 Oct 2025 23:45:50 GMT  
		Size: 14.0 KB (13988 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:8ee0bf09c075a2f76ab2a753178a50023da8354eaa3066be15ae6df16b40eb26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.8 MB (334773527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f02408a764c4d03ef0ac688ee39de788035eb1fc14f6701fc34b094b37ec2a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df86e57d1d11515507bced15d2c5b47745ef47d90bf56ccfea3ffeb9852fdea4`  
		Last Modified: Thu, 30 Oct 2025 21:36:42 GMT  
		Size: 305.6 MB (305563849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4c7086dfaf26b09349225db4c780cf050cd5c0c5587f443eb99860dab7dcc2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4088714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ca752b45a8a21a6be117b63b2108326231dbd39bf5ad0f1421afa525c16f0f`

```dockerfile
```

-	Layers:
	-	`sha256:41e7bf57a66535222d70a721ed5c6d7627a2529faa2fa47097ea4924980ffe34`  
		Last Modified: Thu, 30 Oct 2025 23:45:56 GMT  
		Size: 4.1 MB (4074862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d529607b7e48cf2c2deba92ff2676f549bc263c168014cc85eaccd836f9b478`  
		Last Modified: Thu, 30 Oct 2025 23:45:57 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:618319743dba7907bf939f4fd93e4780a26f850891390db402bb5410fd296f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.3 MB (389270928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9901f02b9f06ecb4ec8b7de647fc610ee1ff40888508743a53f7af37b2588b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f2c98917f6ab10ac1a3e91d3f450c9d291d357d9f62f4fa1c6aeff0ac06969`  
		Last Modified: Tue, 21 Oct 2025 18:03:16 GMT  
		Size: 357.2 MB (357202148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0debd4a0f8008916877b1c7a02f3cb353375e45f10ddc5ffe275c4023fc20550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a048f7267ae5d5dbf804407baf9bc29c402ed905fb44e6f8ead9a068d7c80e`

```dockerfile
```

-	Layers:
	-	`sha256:cac15ddb9bc0ce5dd1e6e206817449698fe25f593fb8b3ff13b1f84b2c0517d6`  
		Last Modified: Tue, 21 Oct 2025 17:44:47 GMT  
		Size: 4.1 MB (4069081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6cc684615c6eb1c2c5f68c068da0b19e0e3ecff77cd4fb8fc7b8d20982c0199`  
		Last Modified: Tue, 21 Oct 2025 17:44:48 GMT  
		Size: 12.1 KB (12127 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:b5ae74b41977de30791004301b9a55684a4a354fbbfe5a46fd7c412a1db484b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.9 MB (373924203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c02d1953e53a49919fdf3212d3b0191ff68e4b62f8b6cd5875592f08ab9f534`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Thu, 30 Oct 2025 22:45:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:45:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:45:13 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:43b0f588b497b17691a3547afa4ae41853829cffde6930e6425ddae4a3f89278`  
		Last Modified: Tue, 21 Oct 2025 00:21:28 GMT  
		Size: 26.9 MB (26884356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ac26cb25e9079f7df28678594c9546404a88850ef59d1906cdae0af1834af2`  
		Last Modified: Thu, 30 Oct 2025 22:47:19 GMT  
		Size: 347.0 MB (347039847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ca7ec822c8eac17e6a09f4496f9ea73f7f5cf4a227037de86239e19824a01cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7bdc57546b9d419b45fd2009461ac7feb00999dd5424e0861ae69445408a1d`

```dockerfile
```

-	Layers:
	-	`sha256:a163636249f2f57c519801b581ece738bbca25c2502343f983fc21023358dc51`  
		Last Modified: Thu, 30 Oct 2025 23:46:05 GMT  
		Size: 3.9 MB (3933157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4082065c8b0d4a306a1d88f8e5c972213af58b5b72c4f05bb1bdf4f35a0db44`  
		Last Modified: Thu, 30 Oct 2025 23:46:06 GMT  
		Size: 13.9 KB (13884 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:511c91223741697cf68aa071b1d676f1545ad354760bb2a6f9ec65b4efa2450d
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
$ docker pull rust@sha256:532c9bafb504801211101abb4e38741bf310e674b45ba05fe837a0c48b18093a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301490013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375eb8ec7a7a87934ba8adca1300d377595f58bbbf6720a63077f2c567e43e17`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95330b7f3a0a801883f9715ffac7f513641a9c3c181e15460a2979b4e7981877`  
		Last Modified: Tue, 21 Oct 2025 08:48:23 GMT  
		Size: 271.2 MB (271231648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:67072e1caa1ac00c1f7896e4cd9c0020bfbf87f34547d25c8406e77ad587f21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df21e2a5b857681a8e521b60d9687f161de4cebccf166ef2b31fa12fa8b3bae4`

```dockerfile
```

-	Layers:
	-	`sha256:36dcd507b25119bcc46133aaf8f95f2f4b063ba744c8da723dc4c733200e14dd`  
		Last Modified: Tue, 21 Oct 2025 08:45:21 GMT  
		Size: 4.3 MB (4303602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5d4b466b9bdcddd1284d82d1b6e4cd805119fb7d12373a0324ad1da312749c`  
		Last Modified: Tue, 21 Oct 2025 08:45:22 GMT  
		Size: 11.4 KB (11355 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:13fc3a2170515d49a864808c172e6ef2cdb6ceb7d516c49d43f25dc6d7220aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325804399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e041264a283725f3e8d0e27bf0c41b94d5c1f7a4f0ad080f4bab768ec221cd17`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 21:35:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:42 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4b897c04dec26603bcc1b01b4283220cd1ffb208f0ec4c0db9e08dab58fcfb5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 25.5 MB (25546187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f470db143d0044ed53ee3c62d37c264ce9347606e374e60113030bb748254e`  
		Last Modified: Thu, 30 Oct 2025 21:36:25 GMT  
		Size: 300.3 MB (300258212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:80c8d376c747cb7f8555437910e6c9a1add734f8d43488803a7fbb48d5300c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cb2dd69accf11a0b247c6ebd6851c11ca87d48376f5b4c43e55069d8779493`

```dockerfile
```

-	Layers:
	-	`sha256:3886373e00abc1e6f64ba5c91f674e54b4699c88fafb62b650aaaf8da12bec8e`  
		Last Modified: Thu, 30 Oct 2025 23:45:53 GMT  
		Size: 4.1 MB (4111595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea67c0e765b1816115cb1b8753a4b992d18c1f0dbe17cbdafddb31a15734a966`  
		Last Modified: Thu, 30 Oct 2025 23:45:54 GMT  
		Size: 12.8 KB (12794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:7ff887fd3eb13d26eecb0f40398028fdc12a3298ef48c8528331016decfb0ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264715851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ae94dab2b12284d1f2e92e3e2ac7b56eff6bb02864e3639caa14c43b4390fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 21:34:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:34:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:34:39 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db337e821e80e597fa142716f1cb02566d2cf4168196f5f08a415cfb4a249b7`  
		Last Modified: Thu, 30 Oct 2025 21:35:15 GMT  
		Size: 236.0 MB (235967450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f46b8601c7c669072e496b7807335af3362860103487ba6340ac14700e4d2e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3c48bda2928a06b24f54d0c55cb10592408f842b75a6984f01eb69ebb7f065`

```dockerfile
```

-	Layers:
	-	`sha256:ab6b83830f27e4a54af4a4ff3428fe72f6898a17d7e3c21d3a7b6165de49140c`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 4.3 MB (4299991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4018ce6087359d14714e6bcbfbfdc372aa884d3abeff3000503021a2c3381d0f`  
		Last Modified: Thu, 30 Oct 2025 23:46:00 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:a8c4281836aee33f681efe73b74c2fe608821ab8a79e1e4f53c408cbee6a616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329920628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44d16d04c4e9d940226b9321174f5ada41cc3046700d8f53b9f75357436b02a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 21:35:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:04 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ed9b7a4c5998c0d248e37f414fa0883c2b695df7b879c0ba096280f29fcb2660`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 31.2 MB (31191494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8bca4c0d96694e3d489bc0df62c181f63f68bd29966b3d385296b7f25514f0`  
		Last Modified: Thu, 30 Oct 2025 21:35:46 GMT  
		Size: 298.7 MB (298729134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8220d5bc4c59b662f331a750b1c3e053eb553fcf58d971daa7ceda6433fac105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ee75a2e521250b772ff737b27beb9860a1292184f784af6f4e157e5a734559`

```dockerfile
```

-	Layers:
	-	`sha256:5ee000ac8ab06e33a71014e51eeb45b60c7820fd0d03e45c9fd2b1573f530073`  
		Last Modified: Thu, 30 Oct 2025 23:46:05 GMT  
		Size: 4.3 MB (4293344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fb44d48fb78f0b88ebc033734c23af5eb6f66040ca67ec8536dcd1a1755ed6f`  
		Last Modified: Thu, 30 Oct 2025 23:46:06 GMT  
		Size: 12.7 KB (12682 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-trixie`

```console
$ docker pull rust@sha256:79e8bbf426da1710dea53aa80da3ba8823060dc1761e6fd2a92c49e0f4809c76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:slim-trixie` - linux; amd64

```console
$ docker pull rust@sha256:618466f4caae45cd6b7b6adfa98764ad462aacf67e7149c6d277c625da9f1282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316292209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c7ce709bce953db30bba7b3470638840d37d0e0a97220d6ba0542ae17aad67`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de44ca22a261b7801f942055dc9512f4e262e99021abda7f616cb77e45f2ac15`  
		Last Modified: Tue, 21 Oct 2025 08:48:56 GMT  
		Size: 286.5 MB (286514285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:65edc8293295cd16da8bf098701a6a507618a7dd2a9331e3f668a57ffe1c63df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4178629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6aa3d298b90262ca1f963f745149eb9cd429a8e23605e7cdc8ed89a4a4bb2f2`

```dockerfile
```

-	Layers:
	-	`sha256:4a5d4e539b906905d0a1a8cf26f58a195fa73f0755e02e96c515a60213341b47`  
		Last Modified: Tue, 21 Oct 2025 08:45:29 GMT  
		Size: 4.2 MB (4165011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e92458c8a75e4c47ff513c54b479567ce494fbb4081e948a711085a94e7b4b`  
		Last Modified: Tue, 21 Oct 2025 08:45:30 GMT  
		Size: 13.6 KB (13618 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:36bd228e236519c3a747a87570e7f83dab399d17eca3ef372e6484c3055c6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334448212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c202a0d535ea0887983203aae69fdf71f527951cf86b2b21f3fb6c2cf9a538`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:37:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:37:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:37:12 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6e00fb9e9c84f34ed2d592246743cef540466ac4115722b315d862bccdbb44`  
		Last Modified: Thu, 30 Oct 2025 21:37:57 GMT  
		Size: 308.2 MB (308235318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:4e20e1ca9b0f23d783ec6d6ed5be8fa58ddaf53b726d80cd6fe80cf82a708eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b868546b1ef1b0edf1d23ec51f66614251da1094f46405866d3bf09b052aecad`

```dockerfile
```

-	Layers:
	-	`sha256:14738f7012d7020bd06896025d57d8d8f840e853cca38898526091bad7f49804`  
		Last Modified: Thu, 30 Oct 2025 23:45:32 GMT  
		Size: 4.0 MB (3969887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da73b8e3cdf4379799012870a7c21e494173161ddc8b1b353fc501f5632e4cf`  
		Last Modified: Thu, 30 Oct 2025 23:45:33 GMT  
		Size: 15.7 KB (15744 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:8f015c79dd7ae0d1ab3218f86dda57f805a046991a5a67aa40088a67965806e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280064640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ccfb92e01921c8ed8fe03746498812688fe017b71f41f9e31a6cea79147abe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:55 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:55 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:55 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9e403b0cf550d52dedd0ab0aa7cbdcdd11f44b28ceb00d624c5c3d50a41df8`  
		Last Modified: Thu, 30 Oct 2025 23:47:09 GMT  
		Size: 249.9 MB (249922513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:cc442428572057302c62370a3c8514cb787a1a7daeed774b9f01e3a53f53d5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96a2c18c7d5bc0df280a6b286dc537b572cbe31668fcf2ad169f1bdf85194d`

```dockerfile
```

-	Layers:
	-	`sha256:606f393a1954d59bcd6d8915d68d376cd05d29024f9a559d92c8ad47da7baa53`  
		Last Modified: Thu, 30 Oct 2025 23:45:37 GMT  
		Size: 4.3 MB (4256227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32db46c306be7344e9ad5e0d189a1f9fccfa49d28d6336ecf1d9609a07d3da88`  
		Last Modified: Thu, 30 Oct 2025 23:45:38 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; 386

```console
$ docker pull rust@sha256:ef194da922ba0594e7b7ddf8676004948a82926c4d57ac47bf5a47d85b43d571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341758796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4548274d12a2843de650e527ef6fbf4c3a6d29412091c3b2129c37809a899eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:35:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:35:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:35:52 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e995015b3e24125a0c10003ec7b1e384ce24f06f88cbd49bce3e36d2e4ffd8f`  
		Last Modified: Thu, 30 Oct 2025 21:36:35 GMT  
		Size: 310.5 MB (310464168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:5a52de8d007cb783912f98e3a2bc9ef1bea117a247b300d3bf0ed25db3ef7b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05360c911e791bc9a471f2026d992be7509b06ede83672b314adfab6d540bf4b`

```dockerfile
```

-	Layers:
	-	`sha256:657d29bb5c22513fcfdf6fccc85d309ca3ac85cc4258c72801d105ab1c31c57a`  
		Last Modified: Thu, 30 Oct 2025 23:45:43 GMT  
		Size: 4.1 MB (4138524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed724e78f81430b3f4c6c9bf61b7039d1389fa37f5495feb17edb5614799f43`  
		Last Modified: Thu, 30 Oct 2025 23:45:44 GMT  
		Size: 15.6 KB (15579 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; ppc64le

```console
$ docker pull rust@sha256:72b668dd78a23c4a07810e311f75b18800d78d8b842f464b61ebf09659fc734a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 MB (388910993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11aecbbe059663e629a6a1abc931ed99632579ce2b826607539fd7c5dbe41e57`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a2a3e69fb5be32fda430122dfe24ff452aed1c97ebc7a331f684085f9a9caa`  
		Last Modified: Tue, 21 Oct 2025 18:09:51 GMT  
		Size: 355.3 MB (355312475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:4051cc4a20c93b4a51262e6e33ba8be0c65a6769b70b76e8486124d3f31b7cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddf9a019c7107abe4e7b64c25d8cce534229de6341057921d82c64ec2afc5fb`

```dockerfile
```

-	Layers:
	-	`sha256:f9375169da8a2e632c640de11742ddfd32dcdc88e874a300d9caedcd94bc08fb`  
		Last Modified: Tue, 21 Oct 2025 17:44:42 GMT  
		Size: 4.2 MB (4161472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72f384288b484aab5875d8e0d36379250accb364045389bd7d5b1c897f9b7a0e`  
		Last Modified: Tue, 21 Oct 2025 17:44:43 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; riscv64

```console
$ docker pull rust@sha256:aaf1ec04eb2b47005e3b8560b0ab3fa83b42cb6b8c8cd6c6eb55a3c1ca29fd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 MB (391690936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd90d32888708414dd2407217bdbeb9884c97b7b7c8bf613038f97a472c8c4f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:00:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:00:19 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2315ad783eb28b652f5440fe195ec3068e8c8429c644f9745c84f8c522147`  
		Last Modified: Thu, 30 Oct 2025 22:12:21 GMT  
		Size: 363.4 MB (363415286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:b085520540a279fab989fbd055fdff984bfe91d00f603dc6d9c1ee6747d497ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cc7bb3bca0e889b9a141380fcd0cf516a70126219e8fbac44ce160e69a9225`

```dockerfile
```

-	Layers:
	-	`sha256:e20ad570b9c4befd769026dc8b5716c3cf74fc0c6bdbddae3ab6e42e13ccdf5e`  
		Last Modified: Thu, 30 Oct 2025 23:45:53 GMT  
		Size: 4.2 MB (4239428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8670d848e45c5e062ecf29084ab05335daba00c88a567e96c2cc5fca9b04fbe3`  
		Last Modified: Thu, 30 Oct 2025 23:45:54 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-trixie` - linux; s390x

```console
$ docker pull rust@sha256:38ebb79c4b041ab046e504b5de098381f8027201a2594744a1eb1fecba242ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.1 MB (379117853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd57e4210e0c402a7b13d84e7dbf8a58418c9777b67aa36fa3c2222c9bae1144`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 22:54:35 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:54:35 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:54:35 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9805f4fca0189a31ca7f470c6efdd8dd933a751f5e840c7dbe3eb3034acef906`  
		Last Modified: Thu, 30 Oct 2025 22:56:45 GMT  
		Size: 349.3 MB (349280598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-trixie` - unknown; unknown

```console
$ docker pull rust@sha256:e2b502b6ae9b904b73922a60e8ebe8814262ef8cb49c465af48c8494dbd80fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5388a6f6d7beec83a26ed19423edba57454d4145bb7d7f5aaefbf1faaa6eb99d`

```dockerfile
```

-	Layers:
	-	`sha256:51b388bf3623dd03362dcb15f7452b4677d633e967a003b3bc39faf47e960502`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 4.0 MB (3982759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a69eb51b743dde6eed89af2bfc049b12313cde5e899319a66fa67ebbb2c5ac`  
		Last Modified: Thu, 30 Oct 2025 23:45:59 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:trixie`

```console
$ docker pull rust@sha256:4cdae04e9e94e189ab2a6b462c93ed5f8ab248cde1c6100c59e958976b1c4594
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:trixie` - linux; amd64

```console
$ docker pull rust@sha256:7ccdba2b655ebac8408566b54b8dbd02b44756759e8d73109227edb2b81b2942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589704892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd127f46648e9bce2a1ffa8096f2babd56565f986ae96fa6abef7bc6fc290ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d573bf42b377ce6a5a0451c15388849686fa4058efd68999f3b014daeb5b55`  
		Last Modified: Tue, 21 Oct 2025 01:42:47 GMT  
		Size: 25.6 MB (25615545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dfe2fac1c486e9aaf41d1028ed30be2c442aa84af44462bc7bac8c148ffb13`  
		Last Modified: Tue, 21 Oct 2025 04:47:38 GMT  
		Size: 67.8 MB (67784857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d5bd8a8d262418bf22e705535ce38c6789dc72e319d76b30aafa5c331b6924`  
		Last Modified: Tue, 21 Oct 2025 10:24:40 GMT  
		Size: 235.9 MB (235927971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68557728bac69b81da96dae42ed23a374347244afaca7210e768400aecefb4d`  
		Last Modified: Tue, 21 Oct 2025 12:18:46 GMT  
		Size: 211.1 MB (211091548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:trixie` - unknown; unknown

```console
$ docker pull rust@sha256:c6e9c920b84edb3271e9884c7e7d7736fa75456c61d869517d117f8b006f02f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17223403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0af01840a4d7313dce07a4cd8705141858d215468038f488a00bc2983f4203`

```dockerfile
```

-	Layers:
	-	`sha256:4de25e75936e713c9998f626efb488832cbbc139588b1dab75dee11b9e80e7da`  
		Last Modified: Tue, 21 Oct 2025 14:44:21 GMT  
		Size: 17.2 MB (17209918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f86274d8e899d886607e02351051d3409137c5b77521eb87725d6ff4cfb078e`  
		Last Modified: Tue, 21 Oct 2025 14:44:22 GMT  
		Size: 13.5 KB (13485 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:trixie` - linux; arm variant v7

```console
$ docker pull rust@sha256:df192b38e9142bc8d454be61de04235e6e3d6e3cc142b3ca4461565fdcdb5c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583252486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a735b8020181b775c6ff35bd4f4ddaf6fccacf90d6baef0e5b88f5fac468e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:20 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:20 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:20 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cda7f0b38d756bba039d1251605b315c32a18bef1d71d1a0a98df8f4c7fb6`  
		Last Modified: Tue, 21 Oct 2025 06:18:01 GMT  
		Size: 193.2 MB (193235864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7085e104656ea6c66d8ba95df53b71fae0ae8c42dce84c36d3dd51cc63114cc`  
		Last Modified: Thu, 30 Oct 2025 23:48:47 GMT  
		Size: 258.0 MB (257970062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:trixie` - unknown; unknown

```console
$ docker pull rust@sha256:7bdc29f59dfa654c3d2300e1d752366f54275c8759cf65ee11f3b51b5ee02ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b60585f52529edd183ac79b90c91a6c5c7a9f7718df436557b6c48120de964f`

```dockerfile
```

-	Layers:
	-	`sha256:e7514cf6a08ba2c22ef71f6054b5e755385f65048788dccfe2a655928e7613af`  
		Last Modified: Thu, 30 Oct 2025 23:44:49 GMT  
		Size: 17.0 MB (16977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7716c3ffa9ab429830b3182885b3f920b00e895ca1ca6dc9aa0e0866b3405617`  
		Last Modified: Thu, 30 Oct 2025 23:44:50 GMT  
		Size: 15.5 KB (15508 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:trixie` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:69d4bc701fcca1d78e46d634aca8f1b0a3b967b755e87d0c3e883abf402a92c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.6 MB (548594894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124905d571200dee29c0250b5a56242cbb369d8d6a2f46770ef2060b9aa6ae19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:13 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f695ddffd81064f15ea19428e2d643e8b560e48e54ae801a8d63c45ad6ac29`  
		Last Modified: Tue, 21 Oct 2025 04:14:42 GMT  
		Size: 226.1 MB (226078014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b0009962587465f15c28cbaa4e05bede4600a6b68c86467eb69e4227df6c84`  
		Last Modified: Thu, 30 Oct 2025 23:44:37 GMT  
		Size: 180.3 MB (180266565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:trixie` - unknown; unknown

```console
$ docker pull rust@sha256:a2ff1f30c17e94d0edaf28e068fd1a99b76f759cebd6a2b304606e7c085f21aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17309822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d625100634edff47e63fc8b469129a68a25115bad3e0531a1f7b594067d865`

```dockerfile
```

-	Layers:
	-	`sha256:b3eb795d70d03f35b63225b01143c51f0f8b6622f4022cb5db697d2ba9e108d7`  
		Last Modified: Thu, 30 Oct 2025 23:45:11 GMT  
		Size: 17.3 MB (17294274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f42745a111fee91795bb40aa7014469e06556069a7271890a09e381d064bfc`  
		Last Modified: Thu, 30 Oct 2025 23:45:12 GMT  
		Size: 15.5 KB (15548 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:trixie` - linux; 386

```console
$ docker pull rust@sha256:0f36b8c5b45a1403f31ae3e1f2db1be6126a1a8d3d89157dfbf1a9caf8364a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.4 MB (625391663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5670c24f999c8b72981507cb47d2b2dcaf53d09af6a4187abbd6fe21f62d48fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:36:12 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:36:12 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:36:12 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e11ad5a4fd5be41f07ac93311f8ae1f7dfd6455edf9f5cf950e26d70ee4c6`  
		Last Modified: Tue, 21 Oct 2025 01:53:30 GMT  
		Size: 26.8 MB (26775679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e99453a1ea6755d1a3a58fe6632281db5820c733291dbefe645ffd8397c7e4`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 69.8 MB (69795039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4be1d74f0f5cdfd17973a37d16dc7ed75a3f628a94c99be57d59571d3a9b4`  
		Last Modified: Tue, 21 Oct 2025 04:13:56 GMT  
		Size: 240.1 MB (240053433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b95b67c6e22caf5578ea1eddb03fde4e1cedc03293a23c829f701c73cc927b`  
		Last Modified: Thu, 30 Oct 2025 23:51:31 GMT  
		Size: 238.0 MB (237966938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:trixie` - unknown; unknown

```console
$ docker pull rust@sha256:de9c5a2a0cb7e4e8b0375014aeac39baef1c37299b1295b32c691537e29bbdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17193526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7797bff6bc0b961011e7f5b876cc1e1e46af5fb5bb27dddfa8a0836045fbdcf6`

```dockerfile
```

-	Layers:
	-	`sha256:4ba4d0a028ca002c9baa8b6e271bbed6f0b707811424f49afb3dbed5b7bbbc66`  
		Last Modified: Thu, 30 Oct 2025 23:45:27 GMT  
		Size: 17.2 MB (17178183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f46fff4553bf23d62e5ffce1a59bed624919c2fea3703b65b013ef50394d42`  
		Last Modified: Thu, 30 Oct 2025 23:45:28 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:trixie` - linux; ppc64le

```console
$ docker pull rust@sha256:a29f6e27737a6b59309a166a28c4cf97dd2eefbfa88c3aca3304faa0ff08a3e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672649528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a952fb3ef83a44fc6533607fda15f4d747a2350849923b66222c95ce97864c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572' ;;         riscv64) rustArch='riscv64gc-unknown-linux-gnu'; rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dfb88672cf0a942c4fdfcadf1912c35c9d30a3a001b18a9dad505fb960ae8`  
		Last Modified: Tue, 21 Oct 2025 07:47:00 GMT  
		Size: 27.0 MB (26996207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06029381e2f1b3a0885caf1b758b0461bfaf9db7b9642ca0b79ab28ed1dd4ecc`  
		Last Modified: Tue, 21 Oct 2025 17:35:58 GMT  
		Size: 73.0 MB (73029685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac677cb325b211e7ad7714eb6d52abf13c0d7630be372cac77812dd27241a158`  
		Last Modified: Wed, 22 Oct 2025 01:27:43 GMT  
		Size: 231.1 MB (231086523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff2e4d4f9807f075e3ff5c6c28631a324397b2b771ee6555b6d8e923ee06e0b`  
		Last Modified: Wed, 22 Oct 2025 14:51:26 GMT  
		Size: 288.4 MB (288427637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:trixie` - unknown; unknown

```console
$ docker pull rust@sha256:f33a0240a7d92b5fda177a193f6e7c05cb951abb7c29daf3858c351311dbac60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17209060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36284e92be8526f5f13c82a2f801a21cf15d46cdae17422ca12254be41d6339`

```dockerfile
```

-	Layers:
	-	`sha256:3d6645f5d1a853359ab88d5ea6d06cd386d73bef8d296c30d6ee843f5dbd6028`  
		Last Modified: Wed, 22 Oct 2025 14:45:21 GMT  
		Size: 17.2 MB (17195507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0297a39c3c72137eb2edc4ce4ff2993062b460caa31ef206b40f28e10b1fe71`  
		Last Modified: Wed, 22 Oct 2025 14:45:22 GMT  
		Size: 13.6 KB (13553 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:trixie` - linux; riscv64

```console
$ docker pull rust@sha256:db568b830f6fd90592497dd0eda8001ed384c555723f1082ceb67a49b9968c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.7 MB (731746485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dde95f55f8cca95c0c52acf2dc0afce27141a1ec0354bce98292db2d8245a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 21:41:49 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 21:41:49 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 21:41:49 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c640441904d97046ee4a137483e3b6745e0a18782c3b688fede8e9ddf18261f`  
		Last Modified: Wed, 22 Oct 2025 18:09:29 GMT  
		Size: 25.0 MB (24953874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb6fec5cd2588ba9a09a9491547b6e7005f3640a81c530cc1f2e651257c901`  
		Last Modified: Fri, 24 Oct 2025 21:34:03 GMT  
		Size: 66.7 MB (66662364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c02978248d2c72ee734dd5ab68325ab5be1edbbfe6026472d198390eabe8cf`  
		Last Modified: Sun, 26 Oct 2025 13:26:52 GMT  
		Size: 322.8 MB (322829684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af21d31669ce50f730bd664ae7d97ab0697a48fc4c1fc527c93c32c6f717c3f3`  
		Last Modified: Thu, 30 Oct 2025 21:56:54 GMT  
		Size: 269.5 MB (269530257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:trixie` - unknown; unknown

```console
$ docker pull rust@sha256:5d2476fa78b8cae7f942b74725782b510c4b6a2f687346c648591dd4613b5b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17281556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c73611675d5101a89fa89d59b3a33599e9498dfc407639e4c3b51d2879ed92d`

```dockerfile
```

-	Layers:
	-	`sha256:de5eee62216cb8618afba94f9d4c277f9a550568818b3cbe17aa78900016e6f7`  
		Last Modified: Thu, 30 Oct 2025 23:45:56 GMT  
		Size: 17.3 MB (17266092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c38e4c4e014047f4332c3cf3bf8372bf0ff126eadb475671eb5f6759bb6503e9`  
		Last Modified: Thu, 30 Oct 2025 23:45:57 GMT  
		Size: 15.5 KB (15464 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:trixie` - linux; s390x

```console
$ docker pull rust@sha256:58124806371c4a39a5ac92593a6f823c354d5d002cae39305db81a0b200dc7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.1 MB (648135109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571bb1f5470229ff143899581ee0538e785fbd8bb45168569fa265be37201747`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 30 Oct 2025 22:48:48 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 30 Oct 2025 22:48:48 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.91.0
# Thu, 30 Oct 2025 22:48:48 GMT
RUN set -eux;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='3b8daab6cc3135f2cd4b12919559e6adaee73a2fbefb830fadf0405c20231d61';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='a5db2c4b29d23e9b318b955dd0337d6b52e93933608469085c924e0d05b1df1f';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='acd89c42b47c93bd4266163a7b05d3f26287d5148413c0d47b2e8a7aa67c9dc0';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='726b7fd5d8805e73eab4a024a2889f8859d5a44e36041abac0a2436a52d42572';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='09e64cc1b7a3e99adaa15dd2d46a3aad9d44d71041e2a96100d165c98a8fd7a7';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9f518343ed4506c34ae7900f538c56bac66f4fad9740034ee8b819bd8d15e`  
		Last Modified: Tue, 21 Oct 2025 12:43:19 GMT  
		Size: 26.8 MB (26783314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb7d34d2ff189fa2150ed8d82914c7669f312817531bbe187965e9d30825d3`  
		Last Modified: Tue, 21 Oct 2025 23:25:03 GMT  
		Size: 68.6 MB (68630635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4131ad2e1cf6d0e51274c6e30ebc34015c8e72c5b79a0146220944b33c750ff`  
		Last Modified: Wed, 22 Oct 2025 12:46:56 GMT  
		Size: 206.5 MB (206460184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2905cafaed65f05704ab3b4e23479ae861bb4a148a0aac8b459931962ccf1469`  
		Last Modified: Thu, 30 Oct 2025 22:52:24 GMT  
		Size: 296.9 MB (296909277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:trixie` - unknown; unknown

```console
$ docker pull rust@sha256:54a2179f33db9cea350dd680ac4622e0df5e333f36232801102916c3b7ff749b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17002545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c6960bfd3415ad92fd83afb42906df93f6f114175be156af8cd8f842cfa20c`

```dockerfile
```

-	Layers:
	-	`sha256:24c7152c5b9ea076d3348e04b2479b166ba9b19eff01141c458fb04c53fdcdd6`  
		Last Modified: Thu, 30 Oct 2025 23:46:10 GMT  
		Size: 17.0 MB (16987149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc6358b456c6334b83aedd51c445eeedb3650635525e2e50790b42a8d5968cd`  
		Last Modified: Thu, 30 Oct 2025 23:46:11 GMT  
		Size: 15.4 KB (15396 bytes)  
		MIME: application/vnd.in-toto+json
