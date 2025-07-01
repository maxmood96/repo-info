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
$ docker pull rust@sha256:fb1b9e6b795d92bd186972987462ff013f3280a19d499a181fbe82008ebf011f
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
$ docker pull rust@sha256:895ea71a7ae33c9cbc0fcbc94153438211130b013f617319f50e4160c81a220f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546878344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d78446a6d18fa5c39c70f6d9f3ef920d2cc7aaef913d70a144ed7ec3ab6cc80`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8855ed7a68d9f8fe7d302fae88c166a75915bfbd2d109d79128b51764e3ec`  
		Last Modified: Wed, 11 Jun 2025 13:11:47 GMT  
		Size: 59.7 MB (59656919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20141335d0d810c9798b867a5d9e5d431c308cc8d2a3e7473792f67b70aebe54`  
		Last Modified: Wed, 11 Jun 2025 20:18:23 GMT  
		Size: 175.3 MB (175295615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66c6df9d9091a8f6d9370d213c49202c7730465229248bb42768f524f2662d`  
		Last Modified: Thu, 26 Jun 2025 20:51:35 GMT  
		Size: 245.8 MB (245792958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:b6fca0ae80c8939c1e4e08e56ec0210d2d79ec4ff585e954a3e49475a5eeb242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15678199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c6ebe2d6af8c1e6cbc28fcd0cc553d5117ace909aa53c42417b4855613b7f9`

```dockerfile
```

-	Layers:
	-	`sha256:732caeae73f5c54ec5f524c6fe0020017c0c58db473f8ff2a710de368676ff14`  
		Last Modified: Thu, 26 Jun 2025 20:44:51 GMT  
		Size: 15.7 MB (15664952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06bfcb4e7407db2632aded32db4a998203a2604e14ea343c041a906e564efe0`  
		Last Modified: Thu, 26 Jun 2025 20:44:52 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:07203b26f0bc7b37a78fd6c28206aaa083c42062c2361c0cb5e4e2de00a91a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513279152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69c797e91bf1841b5a3751b4b4ea6531fa8498f918b0bd200a85c7c04570a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f00d2fce1661cc6f10e2982ec23164c04e8216c9b6becd72c7dfa2c1500773`  
		Last Modified: Wed, 11 Jun 2025 16:22:16 GMT  
		Size: 202.8 MB (202765551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ace51316f37de564f1549a097ccad8107773f4a1ab8ef9b10c1d12891d19c2`  
		Last Modified: Thu, 26 Jun 2025 20:46:26 GMT  
		Size: 174.3 MB (174260340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:ac62b16c27941e28f0cb53f19d3bc71c672502ecc67c38d9ca95c3c429a8a559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15904301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b1db06222577a81afd4f1843567d7bda4a3674b70ec03948effb350c77543f`

```dockerfile
```

-	Layers:
	-	`sha256:e194bc445bfa04b2abdc4e4c1a1044a14a3bc323ba848a5084e53b129e21a97a`  
		Last Modified: Thu, 26 Jun 2025 20:45:04 GMT  
		Size: 15.9 MB (15891010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52324b0c09d8cd669336d9e92e9e0f7725c702d42c92cb272ff5611d1cdede19`  
		Last Modified: Thu, 26 Jun 2025 20:45:05 GMT  
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
$ docker pull rust@sha256:0b25ce5415397e604e8b05fb81496e2e932cd5226190aae57feefe5111f0902d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635974169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1726aeaf732f42a6bafa41db07ed616fab7d5b57de9c51cdb9cf2deae07af0a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcd3217ebdd78ee7f5f6a67c7b4b49ee252ec2305007272d04d562f9e83004`  
		Last Modified: Wed, 11 Jun 2025 17:40:53 GMT  
		Size: 25.7 MB (25657425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5e3e648b0af066a27f67ff1ab192ecc1e665ef5dd174521d0a856b9bff018`  
		Last Modified: Wed, 11 Jun 2025 22:39:56 GMT  
		Size: 69.8 MB (69839696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad59f4a8d63a9a6d3a38c0e8051f843741fd0dabd3b5114b4175e24dd0aab6f`  
		Last Modified: Wed, 11 Jun 2025 22:32:07 GMT  
		Size: 214.4 MB (214421221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bb55ec2c635976ec434105335e47f0492f045ced96a86aeb23414fed78db0f`  
		Last Modified: Thu, 26 Jun 2025 21:03:12 GMT  
		Size: 273.7 MB (273718470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:222537a02739997e871907c9ee5c541fdf9978c1506600702185cc11b3a0a24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15850871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712926ca1eda4b14f5a61a8ca974f155fc5bf765a95534e9d2416935d4f17744`

```dockerfile
```

-	Layers:
	-	`sha256:9e100efe9a1554a97c120beacd16067a091fbaac495418644f5de26fea5aafd8`  
		Last Modified: Thu, 26 Jun 2025 20:45:33 GMT  
		Size: 15.8 MB (15837664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638e899fbd6428c2fa049d7380fb089ad66a6550e78036d0b9603c2c58b6db1b`  
		Last Modified: Thu, 26 Jun 2025 20:45:34 GMT  
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
		Last Modified: Tue, 01 Jul 2025 19:42:30 GMT  
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
$ docker pull rust@sha256:fb1b9e6b795d92bd186972987462ff013f3280a19d499a181fbe82008ebf011f
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
$ docker pull rust@sha256:895ea71a7ae33c9cbc0fcbc94153438211130b013f617319f50e4160c81a220f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546878344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d78446a6d18fa5c39c70f6d9f3ef920d2cc7aaef913d70a144ed7ec3ab6cc80`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8855ed7a68d9f8fe7d302fae88c166a75915bfbd2d109d79128b51764e3ec`  
		Last Modified: Wed, 11 Jun 2025 13:11:47 GMT  
		Size: 59.7 MB (59656919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20141335d0d810c9798b867a5d9e5d431c308cc8d2a3e7473792f67b70aebe54`  
		Last Modified: Wed, 11 Jun 2025 20:18:23 GMT  
		Size: 175.3 MB (175295615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66c6df9d9091a8f6d9370d213c49202c7730465229248bb42768f524f2662d`  
		Last Modified: Thu, 26 Jun 2025 20:51:35 GMT  
		Size: 245.8 MB (245792958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b6fca0ae80c8939c1e4e08e56ec0210d2d79ec4ff585e954a3e49475a5eeb242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15678199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c6ebe2d6af8c1e6cbc28fcd0cc553d5117ace909aa53c42417b4855613b7f9`

```dockerfile
```

-	Layers:
	-	`sha256:732caeae73f5c54ec5f524c6fe0020017c0c58db473f8ff2a710de368676ff14`  
		Last Modified: Thu, 26 Jun 2025 20:44:51 GMT  
		Size: 15.7 MB (15664952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06bfcb4e7407db2632aded32db4a998203a2604e14ea343c041a906e564efe0`  
		Last Modified: Thu, 26 Jun 2025 20:44:52 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:07203b26f0bc7b37a78fd6c28206aaa083c42062c2361c0cb5e4e2de00a91a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513279152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69c797e91bf1841b5a3751b4b4ea6531fa8498f918b0bd200a85c7c04570a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f00d2fce1661cc6f10e2982ec23164c04e8216c9b6becd72c7dfa2c1500773`  
		Last Modified: Wed, 11 Jun 2025 16:22:16 GMT  
		Size: 202.8 MB (202765551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ace51316f37de564f1549a097ccad8107773f4a1ab8ef9b10c1d12891d19c2`  
		Last Modified: Thu, 26 Jun 2025 20:46:26 GMT  
		Size: 174.3 MB (174260340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ac62b16c27941e28f0cb53f19d3bc71c672502ecc67c38d9ca95c3c429a8a559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15904301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b1db06222577a81afd4f1843567d7bda4a3674b70ec03948effb350c77543f`

```dockerfile
```

-	Layers:
	-	`sha256:e194bc445bfa04b2abdc4e4c1a1044a14a3bc323ba848a5084e53b129e21a97a`  
		Last Modified: Thu, 26 Jun 2025 20:45:04 GMT  
		Size: 15.9 MB (15891010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52324b0c09d8cd669336d9e92e9e0f7725c702d42c92cb272ff5611d1cdede19`  
		Last Modified: Thu, 26 Jun 2025 20:45:05 GMT  
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
$ docker pull rust@sha256:0b25ce5415397e604e8b05fb81496e2e932cd5226190aae57feefe5111f0902d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635974169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1726aeaf732f42a6bafa41db07ed616fab7d5b57de9c51cdb9cf2deae07af0a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcd3217ebdd78ee7f5f6a67c7b4b49ee252ec2305007272d04d562f9e83004`  
		Last Modified: Wed, 11 Jun 2025 17:40:53 GMT  
		Size: 25.7 MB (25657425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5e3e648b0af066a27f67ff1ab192ecc1e665ef5dd174521d0a856b9bff018`  
		Last Modified: Wed, 11 Jun 2025 22:39:56 GMT  
		Size: 69.8 MB (69839696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad59f4a8d63a9a6d3a38c0e8051f843741fd0dabd3b5114b4175e24dd0aab6f`  
		Last Modified: Wed, 11 Jun 2025 22:32:07 GMT  
		Size: 214.4 MB (214421221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bb55ec2c635976ec434105335e47f0492f045ced96a86aeb23414fed78db0f`  
		Last Modified: Thu, 26 Jun 2025 21:03:12 GMT  
		Size: 273.7 MB (273718470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:222537a02739997e871907c9ee5c541fdf9978c1506600702185cc11b3a0a24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15850871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712926ca1eda4b14f5a61a8ca974f155fc5bf765a95534e9d2416935d4f17744`

```dockerfile
```

-	Layers:
	-	`sha256:9e100efe9a1554a97c120beacd16067a091fbaac495418644f5de26fea5aafd8`  
		Last Modified: Thu, 26 Jun 2025 20:45:33 GMT  
		Size: 15.8 MB (15837664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638e899fbd6428c2fa049d7380fb089ad66a6550e78036d0b9603c2c58b6db1b`  
		Last Modified: Thu, 26 Jun 2025 20:45:34 GMT  
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
		Last Modified: Tue, 01 Jul 2025 19:42:30 GMT  
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
$ docker pull rust@sha256:3f1357462f45bc05d87b57947b58f7643250f1bff197c3e8cdaf764430f74f5a
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
$ docker pull rust@sha256:3d5dcba2950d2d4acb0f1c3341e071f827a89d62ed59bf4093e1005573220814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.4 MB (528445849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c253817677603b767a9d700612a3cd865785f9e23e357620753b0581123fbd83`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
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
	-	`sha256:c43258def9bd93af20e1c5bd4e42a71d9db281a9fc468bbb5eb78d7a51c6472a`  
		Last Modified: Tue, 10 Jun 2025 22:47:56 GMT  
		Size: 49.0 MB (49043954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319bc9ba38020b34f4e3f562e110c9ab25e658493eaf95bfc783a633f2d4b036`  
		Last Modified: Wed, 11 Jun 2025 20:11:47 GMT  
		Size: 14.9 MB (14880672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc07acb5bb3458d1880be716fdb2bcc90e78327b21f1c1531b5e4bd0941213a8`  
		Last Modified: Wed, 11 Jun 2025 13:12:55 GMT  
		Size: 50.6 MB (50630824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734851a2b324bac96f57123943a6df950697f3e23e8b67c0c61d1bf8cb6ebe94`  
		Last Modified: Wed, 11 Jun 2025 20:11:59 GMT  
		Size: 168.1 MB (168096630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae769690ee9a1aeba88ad10dbdad1dabda3298645b352d6ab708aad2c05e2439`  
		Last Modified: Fri, 27 Jun 2025 00:47:06 GMT  
		Size: 245.8 MB (245793769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e56f6186facb077b70078f154b4e8cdb635365aacca7f2a5acaeeb4a22556c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15274568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876e8c569cb51753d776be9c901b3db68b92609e32242851a609000f68317398`

```dockerfile
```

-	Layers:
	-	`sha256:2d17e9bc89d8181e8e5c7f161121f4966b1f28643695cdf5d0d3bf9048db22ca`  
		Last Modified: Thu, 26 Jun 2025 20:45:18 GMT  
		Size: 15.3 MB (15263243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:007810245b707ec1d6e1631716a6a54ea20b381502a6bb617cb31243da1f3b33`  
		Last Modified: Thu, 26 Jun 2025 20:45:19 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d8bfc08f0c62d05daca481296ab000c26f146149c46d1d43a41d3e49f8566341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.7 MB (487719631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c70d925a62827811ff74f98444b6c54111dae39d583fbfcb78edd3409c732`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6f3b6fbce84c42871ea80f05b2c61e622e08647f7164e9a95a391926c1f714`  
		Last Modified: Wed, 11 Jun 2025 02:56:50 GMT  
		Size: 15.8 MB (15750566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7850095446c84fa9107622e378378aa7daf4b928caeecbc1149118900d32f7`  
		Last Modified: Wed, 11 Jun 2025 10:33:17 GMT  
		Size: 54.9 MB (54853082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2fd7e06d1539d559e26d6be731f625763a107e4ea18988324824efe75999cc`  
		Last Modified: Wed, 11 Jun 2025 19:39:52 GMT  
		Size: 190.6 MB (190602978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a453dd81708428a36251ceed4f7e001eecc28074e8b85eb0770abe54be6f673`  
		Last Modified: Thu, 26 Jun 2025 21:22:17 GMT  
		Size: 174.3 MB (174260704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7a966cad7400fb33ba761c570f273fc2b09b2016b7b7e68cd4179be0f6e6e9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15479015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fb3d5e288112029fa6c1e40d62d545e06ec84624a21e4858527769c5f300e7`

```dockerfile
```

-	Layers:
	-	`sha256:72917cdaacc8a67c2e396fd25bb0fae773e496622ac87d65315875d6aa2baa23`  
		Last Modified: Thu, 26 Jun 2025 20:45:29 GMT  
		Size: 15.5 MB (15467662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b6d77efe90961a274c606ebfdf56c8d015e7edef16f52e1fcae37862f92484f`  
		Last Modified: Thu, 26 Jun 2025 20:45:30 GMT  
		Size: 11.4 KB (11353 bytes)  
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
		Last Modified: Tue, 01 Jul 2025 17:58:05 GMT  
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
		Last Modified: Tue, 01 Jul 2025 17:58:05 GMT  
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
		Last Modified: Tue, 01 Jul 2025 17:56:06 GMT  
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

## `rust:1.88`

```console
$ docker pull rust@sha256:fb1b9e6b795d92bd186972987462ff013f3280a19d499a181fbe82008ebf011f
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
$ docker pull rust@sha256:895ea71a7ae33c9cbc0fcbc94153438211130b013f617319f50e4160c81a220f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546878344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d78446a6d18fa5c39c70f6d9f3ef920d2cc7aaef913d70a144ed7ec3ab6cc80`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8855ed7a68d9f8fe7d302fae88c166a75915bfbd2d109d79128b51764e3ec`  
		Last Modified: Wed, 11 Jun 2025 13:11:47 GMT  
		Size: 59.7 MB (59656919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20141335d0d810c9798b867a5d9e5d431c308cc8d2a3e7473792f67b70aebe54`  
		Last Modified: Wed, 11 Jun 2025 20:18:23 GMT  
		Size: 175.3 MB (175295615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66c6df9d9091a8f6d9370d213c49202c7730465229248bb42768f524f2662d`  
		Last Modified: Thu, 26 Jun 2025 20:51:35 GMT  
		Size: 245.8 MB (245792958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88` - unknown; unknown

```console
$ docker pull rust@sha256:b6fca0ae80c8939c1e4e08e56ec0210d2d79ec4ff585e954a3e49475a5eeb242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15678199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c6ebe2d6af8c1e6cbc28fcd0cc553d5117ace909aa53c42417b4855613b7f9`

```dockerfile
```

-	Layers:
	-	`sha256:732caeae73f5c54ec5f524c6fe0020017c0c58db473f8ff2a710de368676ff14`  
		Last Modified: Thu, 26 Jun 2025 20:44:51 GMT  
		Size: 15.7 MB (15664952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06bfcb4e7407db2632aded32db4a998203a2604e14ea343c041a906e564efe0`  
		Last Modified: Thu, 26 Jun 2025 20:44:52 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:07203b26f0bc7b37a78fd6c28206aaa083c42062c2361c0cb5e4e2de00a91a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513279152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69c797e91bf1841b5a3751b4b4ea6531fa8498f918b0bd200a85c7c04570a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f00d2fce1661cc6f10e2982ec23164c04e8216c9b6becd72c7dfa2c1500773`  
		Last Modified: Wed, 11 Jun 2025 16:22:16 GMT  
		Size: 202.8 MB (202765551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ace51316f37de564f1549a097ccad8107773f4a1ab8ef9b10c1d12891d19c2`  
		Last Modified: Thu, 26 Jun 2025 20:46:26 GMT  
		Size: 174.3 MB (174260340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88` - unknown; unknown

```console
$ docker pull rust@sha256:ac62b16c27941e28f0cb53f19d3bc71c672502ecc67c38d9ca95c3c429a8a559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15904301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b1db06222577a81afd4f1843567d7bda4a3674b70ec03948effb350c77543f`

```dockerfile
```

-	Layers:
	-	`sha256:e194bc445bfa04b2abdc4e4c1a1044a14a3bc323ba848a5084e53b129e21a97a`  
		Last Modified: Thu, 26 Jun 2025 20:45:04 GMT  
		Size: 15.9 MB (15891010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52324b0c09d8cd669336d9e92e9e0f7725c702d42c92cb272ff5611d1cdede19`  
		Last Modified: Thu, 26 Jun 2025 20:45:05 GMT  
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
$ docker pull rust@sha256:0b25ce5415397e604e8b05fb81496e2e932cd5226190aae57feefe5111f0902d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635974169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1726aeaf732f42a6bafa41db07ed616fab7d5b57de9c51cdb9cf2deae07af0a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcd3217ebdd78ee7f5f6a67c7b4b49ee252ec2305007272d04d562f9e83004`  
		Last Modified: Wed, 11 Jun 2025 17:40:53 GMT  
		Size: 25.7 MB (25657425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5e3e648b0af066a27f67ff1ab192ecc1e665ef5dd174521d0a856b9bff018`  
		Last Modified: Wed, 11 Jun 2025 22:39:56 GMT  
		Size: 69.8 MB (69839696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad59f4a8d63a9a6d3a38c0e8051f843741fd0dabd3b5114b4175e24dd0aab6f`  
		Last Modified: Wed, 11 Jun 2025 22:32:07 GMT  
		Size: 214.4 MB (214421221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bb55ec2c635976ec434105335e47f0492f045ced96a86aeb23414fed78db0f`  
		Last Modified: Thu, 26 Jun 2025 21:03:12 GMT  
		Size: 273.7 MB (273718470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88` - unknown; unknown

```console
$ docker pull rust@sha256:222537a02739997e871907c9ee5c541fdf9978c1506600702185cc11b3a0a24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15850871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712926ca1eda4b14f5a61a8ca974f155fc5bf765a95534e9d2416935d4f17744`

```dockerfile
```

-	Layers:
	-	`sha256:9e100efe9a1554a97c120beacd16067a091fbaac495418644f5de26fea5aafd8`  
		Last Modified: Thu, 26 Jun 2025 20:45:33 GMT  
		Size: 15.8 MB (15837664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638e899fbd6428c2fa049d7380fb089ad66a6550e78036d0b9603c2c58b6db1b`  
		Last Modified: Thu, 26 Jun 2025 20:45:34 GMT  
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
		Last Modified: Tue, 01 Jul 2025 19:42:30 GMT  
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
$ docker pull rust@sha256:fb1b9e6b795d92bd186972987462ff013f3280a19d499a181fbe82008ebf011f
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
$ docker pull rust@sha256:895ea71a7ae33c9cbc0fcbc94153438211130b013f617319f50e4160c81a220f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546878344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d78446a6d18fa5c39c70f6d9f3ef920d2cc7aaef913d70a144ed7ec3ab6cc80`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8855ed7a68d9f8fe7d302fae88c166a75915bfbd2d109d79128b51764e3ec`  
		Last Modified: Wed, 11 Jun 2025 13:11:47 GMT  
		Size: 59.7 MB (59656919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20141335d0d810c9798b867a5d9e5d431c308cc8d2a3e7473792f67b70aebe54`  
		Last Modified: Wed, 11 Jun 2025 20:18:23 GMT  
		Size: 175.3 MB (175295615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66c6df9d9091a8f6d9370d213c49202c7730465229248bb42768f524f2662d`  
		Last Modified: Thu, 26 Jun 2025 20:51:35 GMT  
		Size: 245.8 MB (245792958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b6fca0ae80c8939c1e4e08e56ec0210d2d79ec4ff585e954a3e49475a5eeb242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15678199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c6ebe2d6af8c1e6cbc28fcd0cc553d5117ace909aa53c42417b4855613b7f9`

```dockerfile
```

-	Layers:
	-	`sha256:732caeae73f5c54ec5f524c6fe0020017c0c58db473f8ff2a710de368676ff14`  
		Last Modified: Thu, 26 Jun 2025 20:44:51 GMT  
		Size: 15.7 MB (15664952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06bfcb4e7407db2632aded32db4a998203a2604e14ea343c041a906e564efe0`  
		Last Modified: Thu, 26 Jun 2025 20:44:52 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:07203b26f0bc7b37a78fd6c28206aaa083c42062c2361c0cb5e4e2de00a91a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513279152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69c797e91bf1841b5a3751b4b4ea6531fa8498f918b0bd200a85c7c04570a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f00d2fce1661cc6f10e2982ec23164c04e8216c9b6becd72c7dfa2c1500773`  
		Last Modified: Wed, 11 Jun 2025 16:22:16 GMT  
		Size: 202.8 MB (202765551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ace51316f37de564f1549a097ccad8107773f4a1ab8ef9b10c1d12891d19c2`  
		Last Modified: Thu, 26 Jun 2025 20:46:26 GMT  
		Size: 174.3 MB (174260340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ac62b16c27941e28f0cb53f19d3bc71c672502ecc67c38d9ca95c3c429a8a559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15904301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b1db06222577a81afd4f1843567d7bda4a3674b70ec03948effb350c77543f`

```dockerfile
```

-	Layers:
	-	`sha256:e194bc445bfa04b2abdc4e4c1a1044a14a3bc323ba848a5084e53b129e21a97a`  
		Last Modified: Thu, 26 Jun 2025 20:45:04 GMT  
		Size: 15.9 MB (15891010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52324b0c09d8cd669336d9e92e9e0f7725c702d42c92cb272ff5611d1cdede19`  
		Last Modified: Thu, 26 Jun 2025 20:45:05 GMT  
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
$ docker pull rust@sha256:0b25ce5415397e604e8b05fb81496e2e932cd5226190aae57feefe5111f0902d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635974169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1726aeaf732f42a6bafa41db07ed616fab7d5b57de9c51cdb9cf2deae07af0a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcd3217ebdd78ee7f5f6a67c7b4b49ee252ec2305007272d04d562f9e83004`  
		Last Modified: Wed, 11 Jun 2025 17:40:53 GMT  
		Size: 25.7 MB (25657425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5e3e648b0af066a27f67ff1ab192ecc1e665ef5dd174521d0a856b9bff018`  
		Last Modified: Wed, 11 Jun 2025 22:39:56 GMT  
		Size: 69.8 MB (69839696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad59f4a8d63a9a6d3a38c0e8051f843741fd0dabd3b5114b4175e24dd0aab6f`  
		Last Modified: Wed, 11 Jun 2025 22:32:07 GMT  
		Size: 214.4 MB (214421221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bb55ec2c635976ec434105335e47f0492f045ced96a86aeb23414fed78db0f`  
		Last Modified: Thu, 26 Jun 2025 21:03:12 GMT  
		Size: 273.7 MB (273718470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:222537a02739997e871907c9ee5c541fdf9978c1506600702185cc11b3a0a24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15850871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712926ca1eda4b14f5a61a8ca974f155fc5bf765a95534e9d2416935d4f17744`

```dockerfile
```

-	Layers:
	-	`sha256:9e100efe9a1554a97c120beacd16067a091fbaac495418644f5de26fea5aafd8`  
		Last Modified: Thu, 26 Jun 2025 20:45:33 GMT  
		Size: 15.8 MB (15837664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638e899fbd6428c2fa049d7380fb089ad66a6550e78036d0b9603c2c58b6db1b`  
		Last Modified: Thu, 26 Jun 2025 20:45:34 GMT  
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
		Last Modified: Tue, 01 Jul 2025 19:42:30 GMT  
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
$ docker pull rust@sha256:3f1357462f45bc05d87b57947b58f7643250f1bff197c3e8cdaf764430f74f5a
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
$ docker pull rust@sha256:3d5dcba2950d2d4acb0f1c3341e071f827a89d62ed59bf4093e1005573220814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.4 MB (528445849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c253817677603b767a9d700612a3cd865785f9e23e357620753b0581123fbd83`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
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
	-	`sha256:c43258def9bd93af20e1c5bd4e42a71d9db281a9fc468bbb5eb78d7a51c6472a`  
		Last Modified: Tue, 10 Jun 2025 22:47:56 GMT  
		Size: 49.0 MB (49043954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319bc9ba38020b34f4e3f562e110c9ab25e658493eaf95bfc783a633f2d4b036`  
		Last Modified: Wed, 11 Jun 2025 20:11:47 GMT  
		Size: 14.9 MB (14880672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc07acb5bb3458d1880be716fdb2bcc90e78327b21f1c1531b5e4bd0941213a8`  
		Last Modified: Wed, 11 Jun 2025 13:12:55 GMT  
		Size: 50.6 MB (50630824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734851a2b324bac96f57123943a6df950697f3e23e8b67c0c61d1bf8cb6ebe94`  
		Last Modified: Wed, 11 Jun 2025 20:11:59 GMT  
		Size: 168.1 MB (168096630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae769690ee9a1aeba88ad10dbdad1dabda3298645b352d6ab708aad2c05e2439`  
		Last Modified: Fri, 27 Jun 2025 00:47:06 GMT  
		Size: 245.8 MB (245793769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e56f6186facb077b70078f154b4e8cdb635365aacca7f2a5acaeeb4a22556c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15274568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876e8c569cb51753d776be9c901b3db68b92609e32242851a609000f68317398`

```dockerfile
```

-	Layers:
	-	`sha256:2d17e9bc89d8181e8e5c7f161121f4966b1f28643695cdf5d0d3bf9048db22ca`  
		Last Modified: Thu, 26 Jun 2025 20:45:18 GMT  
		Size: 15.3 MB (15263243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:007810245b707ec1d6e1631716a6a54ea20b381502a6bb617cb31243da1f3b33`  
		Last Modified: Thu, 26 Jun 2025 20:45:19 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d8bfc08f0c62d05daca481296ab000c26f146149c46d1d43a41d3e49f8566341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.7 MB (487719631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c70d925a62827811ff74f98444b6c54111dae39d583fbfcb78edd3409c732`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6f3b6fbce84c42871ea80f05b2c61e622e08647f7164e9a95a391926c1f714`  
		Last Modified: Wed, 11 Jun 2025 02:56:50 GMT  
		Size: 15.8 MB (15750566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7850095446c84fa9107622e378378aa7daf4b928caeecbc1149118900d32f7`  
		Last Modified: Wed, 11 Jun 2025 10:33:17 GMT  
		Size: 54.9 MB (54853082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2fd7e06d1539d559e26d6be731f625763a107e4ea18988324824efe75999cc`  
		Last Modified: Wed, 11 Jun 2025 19:39:52 GMT  
		Size: 190.6 MB (190602978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a453dd81708428a36251ceed4f7e001eecc28074e8b85eb0770abe54be6f673`  
		Last Modified: Thu, 26 Jun 2025 21:22:17 GMT  
		Size: 174.3 MB (174260704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7a966cad7400fb33ba761c570f273fc2b09b2016b7b7e68cd4179be0f6e6e9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15479015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fb3d5e288112029fa6c1e40d62d545e06ec84624a21e4858527769c5f300e7`

```dockerfile
```

-	Layers:
	-	`sha256:72917cdaacc8a67c2e396fd25bb0fae773e496622ac87d65315875d6aa2baa23`  
		Last Modified: Thu, 26 Jun 2025 20:45:29 GMT  
		Size: 15.5 MB (15467662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b6d77efe90961a274c606ebfdf56c8d015e7edef16f52e1fcae37862f92484f`  
		Last Modified: Thu, 26 Jun 2025 20:45:30 GMT  
		Size: 11.4 KB (11353 bytes)  
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
		Last Modified: Tue, 01 Jul 2025 17:58:05 GMT  
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
		Last Modified: Tue, 01 Jul 2025 17:58:05 GMT  
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
		Last Modified: Tue, 01 Jul 2025 17:56:06 GMT  
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

## `rust:1.88.0`

```console
$ docker pull rust@sha256:fb1b9e6b795d92bd186972987462ff013f3280a19d499a181fbe82008ebf011f
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
$ docker pull rust@sha256:895ea71a7ae33c9cbc0fcbc94153438211130b013f617319f50e4160c81a220f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546878344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d78446a6d18fa5c39c70f6d9f3ef920d2cc7aaef913d70a144ed7ec3ab6cc80`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8855ed7a68d9f8fe7d302fae88c166a75915bfbd2d109d79128b51764e3ec`  
		Last Modified: Wed, 11 Jun 2025 13:11:47 GMT  
		Size: 59.7 MB (59656919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20141335d0d810c9798b867a5d9e5d431c308cc8d2a3e7473792f67b70aebe54`  
		Last Modified: Wed, 11 Jun 2025 20:18:23 GMT  
		Size: 175.3 MB (175295615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66c6df9d9091a8f6d9370d213c49202c7730465229248bb42768f524f2662d`  
		Last Modified: Thu, 26 Jun 2025 20:51:35 GMT  
		Size: 245.8 MB (245792958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0` - unknown; unknown

```console
$ docker pull rust@sha256:b6fca0ae80c8939c1e4e08e56ec0210d2d79ec4ff585e954a3e49475a5eeb242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15678199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c6ebe2d6af8c1e6cbc28fcd0cc553d5117ace909aa53c42417b4855613b7f9`

```dockerfile
```

-	Layers:
	-	`sha256:732caeae73f5c54ec5f524c6fe0020017c0c58db473f8ff2a710de368676ff14`  
		Last Modified: Thu, 26 Jun 2025 20:44:51 GMT  
		Size: 15.7 MB (15664952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06bfcb4e7407db2632aded32db4a998203a2604e14ea343c041a906e564efe0`  
		Last Modified: Thu, 26 Jun 2025 20:44:52 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:07203b26f0bc7b37a78fd6c28206aaa083c42062c2361c0cb5e4e2de00a91a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513279152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69c797e91bf1841b5a3751b4b4ea6531fa8498f918b0bd200a85c7c04570a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f00d2fce1661cc6f10e2982ec23164c04e8216c9b6becd72c7dfa2c1500773`  
		Last Modified: Wed, 11 Jun 2025 16:22:16 GMT  
		Size: 202.8 MB (202765551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ace51316f37de564f1549a097ccad8107773f4a1ab8ef9b10c1d12891d19c2`  
		Last Modified: Thu, 26 Jun 2025 20:46:26 GMT  
		Size: 174.3 MB (174260340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0` - unknown; unknown

```console
$ docker pull rust@sha256:ac62b16c27941e28f0cb53f19d3bc71c672502ecc67c38d9ca95c3c429a8a559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15904301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b1db06222577a81afd4f1843567d7bda4a3674b70ec03948effb350c77543f`

```dockerfile
```

-	Layers:
	-	`sha256:e194bc445bfa04b2abdc4e4c1a1044a14a3bc323ba848a5084e53b129e21a97a`  
		Last Modified: Thu, 26 Jun 2025 20:45:04 GMT  
		Size: 15.9 MB (15891010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52324b0c09d8cd669336d9e92e9e0f7725c702d42c92cb272ff5611d1cdede19`  
		Last Modified: Thu, 26 Jun 2025 20:45:05 GMT  
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
$ docker pull rust@sha256:0b25ce5415397e604e8b05fb81496e2e932cd5226190aae57feefe5111f0902d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635974169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1726aeaf732f42a6bafa41db07ed616fab7d5b57de9c51cdb9cf2deae07af0a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcd3217ebdd78ee7f5f6a67c7b4b49ee252ec2305007272d04d562f9e83004`  
		Last Modified: Wed, 11 Jun 2025 17:40:53 GMT  
		Size: 25.7 MB (25657425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5e3e648b0af066a27f67ff1ab192ecc1e665ef5dd174521d0a856b9bff018`  
		Last Modified: Wed, 11 Jun 2025 22:39:56 GMT  
		Size: 69.8 MB (69839696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad59f4a8d63a9a6d3a38c0e8051f843741fd0dabd3b5114b4175e24dd0aab6f`  
		Last Modified: Wed, 11 Jun 2025 22:32:07 GMT  
		Size: 214.4 MB (214421221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bb55ec2c635976ec434105335e47f0492f045ced96a86aeb23414fed78db0f`  
		Last Modified: Thu, 26 Jun 2025 21:03:12 GMT  
		Size: 273.7 MB (273718470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0` - unknown; unknown

```console
$ docker pull rust@sha256:222537a02739997e871907c9ee5c541fdf9978c1506600702185cc11b3a0a24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15850871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712926ca1eda4b14f5a61a8ca974f155fc5bf765a95534e9d2416935d4f17744`

```dockerfile
```

-	Layers:
	-	`sha256:9e100efe9a1554a97c120beacd16067a091fbaac495418644f5de26fea5aafd8`  
		Last Modified: Thu, 26 Jun 2025 20:45:33 GMT  
		Size: 15.8 MB (15837664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638e899fbd6428c2fa049d7380fb089ad66a6550e78036d0b9603c2c58b6db1b`  
		Last Modified: Thu, 26 Jun 2025 20:45:34 GMT  
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
		Last Modified: Tue, 01 Jul 2025 19:42:30 GMT  
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
$ docker pull rust@sha256:fb1b9e6b795d92bd186972987462ff013f3280a19d499a181fbe82008ebf011f
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
$ docker pull rust@sha256:895ea71a7ae33c9cbc0fcbc94153438211130b013f617319f50e4160c81a220f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546878344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d78446a6d18fa5c39c70f6d9f3ef920d2cc7aaef913d70a144ed7ec3ab6cc80`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8855ed7a68d9f8fe7d302fae88c166a75915bfbd2d109d79128b51764e3ec`  
		Last Modified: Wed, 11 Jun 2025 13:11:47 GMT  
		Size: 59.7 MB (59656919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20141335d0d810c9798b867a5d9e5d431c308cc8d2a3e7473792f67b70aebe54`  
		Last Modified: Wed, 11 Jun 2025 20:18:23 GMT  
		Size: 175.3 MB (175295615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66c6df9d9091a8f6d9370d213c49202c7730465229248bb42768f524f2662d`  
		Last Modified: Thu, 26 Jun 2025 20:51:35 GMT  
		Size: 245.8 MB (245792958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b6fca0ae80c8939c1e4e08e56ec0210d2d79ec4ff585e954a3e49475a5eeb242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15678199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c6ebe2d6af8c1e6cbc28fcd0cc553d5117ace909aa53c42417b4855613b7f9`

```dockerfile
```

-	Layers:
	-	`sha256:732caeae73f5c54ec5f524c6fe0020017c0c58db473f8ff2a710de368676ff14`  
		Last Modified: Thu, 26 Jun 2025 20:44:51 GMT  
		Size: 15.7 MB (15664952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06bfcb4e7407db2632aded32db4a998203a2604e14ea343c041a906e564efe0`  
		Last Modified: Thu, 26 Jun 2025 20:44:52 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:07203b26f0bc7b37a78fd6c28206aaa083c42062c2361c0cb5e4e2de00a91a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513279152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69c797e91bf1841b5a3751b4b4ea6531fa8498f918b0bd200a85c7c04570a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f00d2fce1661cc6f10e2982ec23164c04e8216c9b6becd72c7dfa2c1500773`  
		Last Modified: Wed, 11 Jun 2025 16:22:16 GMT  
		Size: 202.8 MB (202765551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ace51316f37de564f1549a097ccad8107773f4a1ab8ef9b10c1d12891d19c2`  
		Last Modified: Thu, 26 Jun 2025 20:46:26 GMT  
		Size: 174.3 MB (174260340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ac62b16c27941e28f0cb53f19d3bc71c672502ecc67c38d9ca95c3c429a8a559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15904301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b1db06222577a81afd4f1843567d7bda4a3674b70ec03948effb350c77543f`

```dockerfile
```

-	Layers:
	-	`sha256:e194bc445bfa04b2abdc4e4c1a1044a14a3bc323ba848a5084e53b129e21a97a`  
		Last Modified: Thu, 26 Jun 2025 20:45:04 GMT  
		Size: 15.9 MB (15891010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52324b0c09d8cd669336d9e92e9e0f7725c702d42c92cb272ff5611d1cdede19`  
		Last Modified: Thu, 26 Jun 2025 20:45:05 GMT  
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
$ docker pull rust@sha256:0b25ce5415397e604e8b05fb81496e2e932cd5226190aae57feefe5111f0902d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635974169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1726aeaf732f42a6bafa41db07ed616fab7d5b57de9c51cdb9cf2deae07af0a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcd3217ebdd78ee7f5f6a67c7b4b49ee252ec2305007272d04d562f9e83004`  
		Last Modified: Wed, 11 Jun 2025 17:40:53 GMT  
		Size: 25.7 MB (25657425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5e3e648b0af066a27f67ff1ab192ecc1e665ef5dd174521d0a856b9bff018`  
		Last Modified: Wed, 11 Jun 2025 22:39:56 GMT  
		Size: 69.8 MB (69839696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad59f4a8d63a9a6d3a38c0e8051f843741fd0dabd3b5114b4175e24dd0aab6f`  
		Last Modified: Wed, 11 Jun 2025 22:32:07 GMT  
		Size: 214.4 MB (214421221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bb55ec2c635976ec434105335e47f0492f045ced96a86aeb23414fed78db0f`  
		Last Modified: Thu, 26 Jun 2025 21:03:12 GMT  
		Size: 273.7 MB (273718470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:222537a02739997e871907c9ee5c541fdf9978c1506600702185cc11b3a0a24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15850871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712926ca1eda4b14f5a61a8ca974f155fc5bf765a95534e9d2416935d4f17744`

```dockerfile
```

-	Layers:
	-	`sha256:9e100efe9a1554a97c120beacd16067a091fbaac495418644f5de26fea5aafd8`  
		Last Modified: Thu, 26 Jun 2025 20:45:33 GMT  
		Size: 15.8 MB (15837664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638e899fbd6428c2fa049d7380fb089ad66a6550e78036d0b9603c2c58b6db1b`  
		Last Modified: Thu, 26 Jun 2025 20:45:34 GMT  
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
		Last Modified: Tue, 01 Jul 2025 19:42:30 GMT  
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
$ docker pull rust@sha256:3f1357462f45bc05d87b57947b58f7643250f1bff197c3e8cdaf764430f74f5a
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
$ docker pull rust@sha256:3d5dcba2950d2d4acb0f1c3341e071f827a89d62ed59bf4093e1005573220814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.4 MB (528445849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c253817677603b767a9d700612a3cd865785f9e23e357620753b0581123fbd83`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
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
	-	`sha256:c43258def9bd93af20e1c5bd4e42a71d9db281a9fc468bbb5eb78d7a51c6472a`  
		Last Modified: Tue, 10 Jun 2025 22:47:56 GMT  
		Size: 49.0 MB (49043954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319bc9ba38020b34f4e3f562e110c9ab25e658493eaf95bfc783a633f2d4b036`  
		Last Modified: Wed, 11 Jun 2025 20:11:47 GMT  
		Size: 14.9 MB (14880672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc07acb5bb3458d1880be716fdb2bcc90e78327b21f1c1531b5e4bd0941213a8`  
		Last Modified: Wed, 11 Jun 2025 13:12:55 GMT  
		Size: 50.6 MB (50630824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734851a2b324bac96f57123943a6df950697f3e23e8b67c0c61d1bf8cb6ebe94`  
		Last Modified: Wed, 11 Jun 2025 20:11:59 GMT  
		Size: 168.1 MB (168096630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae769690ee9a1aeba88ad10dbdad1dabda3298645b352d6ab708aad2c05e2439`  
		Last Modified: Fri, 27 Jun 2025 00:47:06 GMT  
		Size: 245.8 MB (245793769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e56f6186facb077b70078f154b4e8cdb635365aacca7f2a5acaeeb4a22556c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15274568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876e8c569cb51753d776be9c901b3db68b92609e32242851a609000f68317398`

```dockerfile
```

-	Layers:
	-	`sha256:2d17e9bc89d8181e8e5c7f161121f4966b1f28643695cdf5d0d3bf9048db22ca`  
		Last Modified: Thu, 26 Jun 2025 20:45:18 GMT  
		Size: 15.3 MB (15263243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:007810245b707ec1d6e1631716a6a54ea20b381502a6bb617cb31243da1f3b33`  
		Last Modified: Thu, 26 Jun 2025 20:45:19 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.88.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d8bfc08f0c62d05daca481296ab000c26f146149c46d1d43a41d3e49f8566341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.7 MB (487719631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c70d925a62827811ff74f98444b6c54111dae39d583fbfcb78edd3409c732`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6f3b6fbce84c42871ea80f05b2c61e622e08647f7164e9a95a391926c1f714`  
		Last Modified: Wed, 11 Jun 2025 02:56:50 GMT  
		Size: 15.8 MB (15750566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7850095446c84fa9107622e378378aa7daf4b928caeecbc1149118900d32f7`  
		Last Modified: Wed, 11 Jun 2025 10:33:17 GMT  
		Size: 54.9 MB (54853082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2fd7e06d1539d559e26d6be731f625763a107e4ea18988324824efe75999cc`  
		Last Modified: Wed, 11 Jun 2025 19:39:52 GMT  
		Size: 190.6 MB (190602978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a453dd81708428a36251ceed4f7e001eecc28074e8b85eb0770abe54be6f673`  
		Last Modified: Thu, 26 Jun 2025 21:22:17 GMT  
		Size: 174.3 MB (174260704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.88.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7a966cad7400fb33ba761c570f273fc2b09b2016b7b7e68cd4179be0f6e6e9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15479015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fb3d5e288112029fa6c1e40d62d545e06ec84624a21e4858527769c5f300e7`

```dockerfile
```

-	Layers:
	-	`sha256:72917cdaacc8a67c2e396fd25bb0fae773e496622ac87d65315875d6aa2baa23`  
		Last Modified: Thu, 26 Jun 2025 20:45:29 GMT  
		Size: 15.5 MB (15467662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b6d77efe90961a274c606ebfdf56c8d015e7edef16f52e1fcae37862f92484f`  
		Last Modified: Thu, 26 Jun 2025 20:45:30 GMT  
		Size: 11.4 KB (11353 bytes)  
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
		Last Modified: Tue, 01 Jul 2025 17:58:05 GMT  
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
		Last Modified: Tue, 01 Jul 2025 17:58:05 GMT  
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
		Last Modified: Tue, 01 Jul 2025 17:56:06 GMT  
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
$ docker pull rust@sha256:fb1b9e6b795d92bd186972987462ff013f3280a19d499a181fbe82008ebf011f
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
$ docker pull rust@sha256:895ea71a7ae33c9cbc0fcbc94153438211130b013f617319f50e4160c81a220f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546878344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d78446a6d18fa5c39c70f6d9f3ef920d2cc7aaef913d70a144ed7ec3ab6cc80`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8855ed7a68d9f8fe7d302fae88c166a75915bfbd2d109d79128b51764e3ec`  
		Last Modified: Wed, 11 Jun 2025 13:11:47 GMT  
		Size: 59.7 MB (59656919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20141335d0d810c9798b867a5d9e5d431c308cc8d2a3e7473792f67b70aebe54`  
		Last Modified: Wed, 11 Jun 2025 20:18:23 GMT  
		Size: 175.3 MB (175295615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66c6df9d9091a8f6d9370d213c49202c7730465229248bb42768f524f2662d`  
		Last Modified: Thu, 26 Jun 2025 20:51:35 GMT  
		Size: 245.8 MB (245792958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b6fca0ae80c8939c1e4e08e56ec0210d2d79ec4ff585e954a3e49475a5eeb242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15678199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c6ebe2d6af8c1e6cbc28fcd0cc553d5117ace909aa53c42417b4855613b7f9`

```dockerfile
```

-	Layers:
	-	`sha256:732caeae73f5c54ec5f524c6fe0020017c0c58db473f8ff2a710de368676ff14`  
		Last Modified: Thu, 26 Jun 2025 20:44:51 GMT  
		Size: 15.7 MB (15664952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06bfcb4e7407db2632aded32db4a998203a2604e14ea343c041a906e564efe0`  
		Last Modified: Thu, 26 Jun 2025 20:44:52 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:07203b26f0bc7b37a78fd6c28206aaa083c42062c2361c0cb5e4e2de00a91a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513279152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69c797e91bf1841b5a3751b4b4ea6531fa8498f918b0bd200a85c7c04570a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f00d2fce1661cc6f10e2982ec23164c04e8216c9b6becd72c7dfa2c1500773`  
		Last Modified: Wed, 11 Jun 2025 16:22:16 GMT  
		Size: 202.8 MB (202765551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ace51316f37de564f1549a097ccad8107773f4a1ab8ef9b10c1d12891d19c2`  
		Last Modified: Thu, 26 Jun 2025 20:46:26 GMT  
		Size: 174.3 MB (174260340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:ac62b16c27941e28f0cb53f19d3bc71c672502ecc67c38d9ca95c3c429a8a559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15904301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b1db06222577a81afd4f1843567d7bda4a3674b70ec03948effb350c77543f`

```dockerfile
```

-	Layers:
	-	`sha256:e194bc445bfa04b2abdc4e4c1a1044a14a3bc323ba848a5084e53b129e21a97a`  
		Last Modified: Thu, 26 Jun 2025 20:45:04 GMT  
		Size: 15.9 MB (15891010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52324b0c09d8cd669336d9e92e9e0f7725c702d42c92cb272ff5611d1cdede19`  
		Last Modified: Thu, 26 Jun 2025 20:45:05 GMT  
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
$ docker pull rust@sha256:0b25ce5415397e604e8b05fb81496e2e932cd5226190aae57feefe5111f0902d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635974169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1726aeaf732f42a6bafa41db07ed616fab7d5b57de9c51cdb9cf2deae07af0a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcd3217ebdd78ee7f5f6a67c7b4b49ee252ec2305007272d04d562f9e83004`  
		Last Modified: Wed, 11 Jun 2025 17:40:53 GMT  
		Size: 25.7 MB (25657425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5e3e648b0af066a27f67ff1ab192ecc1e665ef5dd174521d0a856b9bff018`  
		Last Modified: Wed, 11 Jun 2025 22:39:56 GMT  
		Size: 69.8 MB (69839696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad59f4a8d63a9a6d3a38c0e8051f843741fd0dabd3b5114b4175e24dd0aab6f`  
		Last Modified: Wed, 11 Jun 2025 22:32:07 GMT  
		Size: 214.4 MB (214421221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bb55ec2c635976ec434105335e47f0492f045ced96a86aeb23414fed78db0f`  
		Last Modified: Thu, 26 Jun 2025 21:03:12 GMT  
		Size: 273.7 MB (273718470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:222537a02739997e871907c9ee5c541fdf9978c1506600702185cc11b3a0a24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15850871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712926ca1eda4b14f5a61a8ca974f155fc5bf765a95534e9d2416935d4f17744`

```dockerfile
```

-	Layers:
	-	`sha256:9e100efe9a1554a97c120beacd16067a091fbaac495418644f5de26fea5aafd8`  
		Last Modified: Thu, 26 Jun 2025 20:45:33 GMT  
		Size: 15.8 MB (15837664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638e899fbd6428c2fa049d7380fb089ad66a6550e78036d0b9603c2c58b6db1b`  
		Last Modified: Thu, 26 Jun 2025 20:45:34 GMT  
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
		Last Modified: Tue, 01 Jul 2025 19:42:30 GMT  
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
$ docker pull rust@sha256:3f1357462f45bc05d87b57947b58f7643250f1bff197c3e8cdaf764430f74f5a
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
$ docker pull rust@sha256:3d5dcba2950d2d4acb0f1c3341e071f827a89d62ed59bf4093e1005573220814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.4 MB (528445849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c253817677603b767a9d700612a3cd865785f9e23e357620753b0581123fbd83`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
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
	-	`sha256:c43258def9bd93af20e1c5bd4e42a71d9db281a9fc468bbb5eb78d7a51c6472a`  
		Last Modified: Tue, 10 Jun 2025 22:47:56 GMT  
		Size: 49.0 MB (49043954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319bc9ba38020b34f4e3f562e110c9ab25e658493eaf95bfc783a633f2d4b036`  
		Last Modified: Wed, 11 Jun 2025 20:11:47 GMT  
		Size: 14.9 MB (14880672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc07acb5bb3458d1880be716fdb2bcc90e78327b21f1c1531b5e4bd0941213a8`  
		Last Modified: Wed, 11 Jun 2025 13:12:55 GMT  
		Size: 50.6 MB (50630824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734851a2b324bac96f57123943a6df950697f3e23e8b67c0c61d1bf8cb6ebe94`  
		Last Modified: Wed, 11 Jun 2025 20:11:59 GMT  
		Size: 168.1 MB (168096630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae769690ee9a1aeba88ad10dbdad1dabda3298645b352d6ab708aad2c05e2439`  
		Last Modified: Fri, 27 Jun 2025 00:47:06 GMT  
		Size: 245.8 MB (245793769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e56f6186facb077b70078f154b4e8cdb635365aacca7f2a5acaeeb4a22556c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15274568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876e8c569cb51753d776be9c901b3db68b92609e32242851a609000f68317398`

```dockerfile
```

-	Layers:
	-	`sha256:2d17e9bc89d8181e8e5c7f161121f4966b1f28643695cdf5d0d3bf9048db22ca`  
		Last Modified: Thu, 26 Jun 2025 20:45:18 GMT  
		Size: 15.3 MB (15263243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:007810245b707ec1d6e1631716a6a54ea20b381502a6bb617cb31243da1f3b33`  
		Last Modified: Thu, 26 Jun 2025 20:45:19 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d8bfc08f0c62d05daca481296ab000c26f146149c46d1d43a41d3e49f8566341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.7 MB (487719631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c70d925a62827811ff74f98444b6c54111dae39d583fbfcb78edd3409c732`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6f3b6fbce84c42871ea80f05b2c61e622e08647f7164e9a95a391926c1f714`  
		Last Modified: Wed, 11 Jun 2025 02:56:50 GMT  
		Size: 15.8 MB (15750566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7850095446c84fa9107622e378378aa7daf4b928caeecbc1149118900d32f7`  
		Last Modified: Wed, 11 Jun 2025 10:33:17 GMT  
		Size: 54.9 MB (54853082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2fd7e06d1539d559e26d6be731f625763a107e4ea18988324824efe75999cc`  
		Last Modified: Wed, 11 Jun 2025 19:39:52 GMT  
		Size: 190.6 MB (190602978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a453dd81708428a36251ceed4f7e001eecc28074e8b85eb0770abe54be6f673`  
		Last Modified: Thu, 26 Jun 2025 21:22:17 GMT  
		Size: 174.3 MB (174260704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:7a966cad7400fb33ba761c570f273fc2b09b2016b7b7e68cd4179be0f6e6e9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15479015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fb3d5e288112029fa6c1e40d62d545e06ec84624a21e4858527769c5f300e7`

```dockerfile
```

-	Layers:
	-	`sha256:72917cdaacc8a67c2e396fd25bb0fae773e496622ac87d65315875d6aa2baa23`  
		Last Modified: Thu, 26 Jun 2025 20:45:29 GMT  
		Size: 15.5 MB (15467662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b6d77efe90961a274c606ebfdf56c8d015e7edef16f52e1fcae37862f92484f`  
		Last Modified: Thu, 26 Jun 2025 20:45:30 GMT  
		Size: 11.4 KB (11353 bytes)  
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
$ docker pull rust@sha256:fb1b9e6b795d92bd186972987462ff013f3280a19d499a181fbe82008ebf011f
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
$ docker pull rust@sha256:895ea71a7ae33c9cbc0fcbc94153438211130b013f617319f50e4160c81a220f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.9 MB (546878344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d78446a6d18fa5c39c70f6d9f3ef920d2cc7aaef913d70a144ed7ec3ab6cc80`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8855ed7a68d9f8fe7d302fae88c166a75915bfbd2d109d79128b51764e3ec`  
		Last Modified: Wed, 11 Jun 2025 13:11:47 GMT  
		Size: 59.7 MB (59656919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20141335d0d810c9798b867a5d9e5d431c308cc8d2a3e7473792f67b70aebe54`  
		Last Modified: Wed, 11 Jun 2025 20:18:23 GMT  
		Size: 175.3 MB (175295615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66c6df9d9091a8f6d9370d213c49202c7730465229248bb42768f524f2662d`  
		Last Modified: Thu, 26 Jun 2025 20:51:35 GMT  
		Size: 245.8 MB (245792958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:b6fca0ae80c8939c1e4e08e56ec0210d2d79ec4ff585e954a3e49475a5eeb242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15678199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c6ebe2d6af8c1e6cbc28fcd0cc553d5117ace909aa53c42417b4855613b7f9`

```dockerfile
```

-	Layers:
	-	`sha256:732caeae73f5c54ec5f524c6fe0020017c0c58db473f8ff2a710de368676ff14`  
		Last Modified: Thu, 26 Jun 2025 20:44:51 GMT  
		Size: 15.7 MB (15664952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06bfcb4e7407db2632aded32db4a998203a2604e14ea343c041a906e564efe0`  
		Last Modified: Thu, 26 Jun 2025 20:44:52 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:07203b26f0bc7b37a78fd6c28206aaa083c42062c2361c0cb5e4e2de00a91a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.3 MB (513279152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69c797e91bf1841b5a3751b4b4ea6531fa8498f918b0bd200a85c7c04570a19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f00d2fce1661cc6f10e2982ec23164c04e8216c9b6becd72c7dfa2c1500773`  
		Last Modified: Wed, 11 Jun 2025 16:22:16 GMT  
		Size: 202.8 MB (202765551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ace51316f37de564f1549a097ccad8107773f4a1ab8ef9b10c1d12891d19c2`  
		Last Modified: Thu, 26 Jun 2025 20:46:26 GMT  
		Size: 174.3 MB (174260340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:ac62b16c27941e28f0cb53f19d3bc71c672502ecc67c38d9ca95c3c429a8a559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15904301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b1db06222577a81afd4f1843567d7bda4a3674b70ec03948effb350c77543f`

```dockerfile
```

-	Layers:
	-	`sha256:e194bc445bfa04b2abdc4e4c1a1044a14a3bc323ba848a5084e53b129e21a97a`  
		Last Modified: Thu, 26 Jun 2025 20:45:04 GMT  
		Size: 15.9 MB (15891010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52324b0c09d8cd669336d9e92e9e0f7725c702d42c92cb272ff5611d1cdede19`  
		Last Modified: Thu, 26 Jun 2025 20:45:05 GMT  
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
$ docker pull rust@sha256:0b25ce5415397e604e8b05fb81496e2e932cd5226190aae57feefe5111f0902d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 MB (635974169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1726aeaf732f42a6bafa41db07ed616fab7d5b57de9c51cdb9cf2deae07af0a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcd3217ebdd78ee7f5f6a67c7b4b49ee252ec2305007272d04d562f9e83004`  
		Last Modified: Wed, 11 Jun 2025 17:40:53 GMT  
		Size: 25.7 MB (25657425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5e3e648b0af066a27f67ff1ab192ecc1e665ef5dd174521d0a856b9bff018`  
		Last Modified: Wed, 11 Jun 2025 22:39:56 GMT  
		Size: 69.8 MB (69839696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad59f4a8d63a9a6d3a38c0e8051f843741fd0dabd3b5114b4175e24dd0aab6f`  
		Last Modified: Wed, 11 Jun 2025 22:32:07 GMT  
		Size: 214.4 MB (214421221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bb55ec2c635976ec434105335e47f0492f045ced96a86aeb23414fed78db0f`  
		Last Modified: Thu, 26 Jun 2025 21:03:12 GMT  
		Size: 273.7 MB (273718470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:222537a02739997e871907c9ee5c541fdf9978c1506600702185cc11b3a0a24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15850871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712926ca1eda4b14f5a61a8ca974f155fc5bf765a95534e9d2416935d4f17744`

```dockerfile
```

-	Layers:
	-	`sha256:9e100efe9a1554a97c120beacd16067a091fbaac495418644f5de26fea5aafd8`  
		Last Modified: Thu, 26 Jun 2025 20:45:33 GMT  
		Size: 15.8 MB (15837664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638e899fbd6428c2fa049d7380fb089ad66a6550e78036d0b9603c2c58b6db1b`  
		Last Modified: Thu, 26 Jun 2025 20:45:34 GMT  
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
		Last Modified: Tue, 01 Jul 2025 19:42:30 GMT  
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
		Last Modified: Tue, 01 Jul 2025 17:58:05 GMT  
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
		Last Modified: Tue, 01 Jul 2025 17:58:05 GMT  
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
		Last Modified: Tue, 01 Jul 2025 17:56:06 GMT  
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
