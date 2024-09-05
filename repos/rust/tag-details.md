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
-	[`rust:1.80`](#rust180)
-	[`rust:1.80-alpine`](#rust180-alpine)
-	[`rust:1.80-alpine3.19`](#rust180-alpine319)
-	[`rust:1.80-alpine3.20`](#rust180-alpine320)
-	[`rust:1.80-bookworm`](#rust180-bookworm)
-	[`rust:1.80-bullseye`](#rust180-bullseye)
-	[`rust:1.80-slim`](#rust180-slim)
-	[`rust:1.80-slim-bookworm`](#rust180-slim-bookworm)
-	[`rust:1.80-slim-bullseye`](#rust180-slim-bullseye)
-	[`rust:1.80.1`](#rust1801)
-	[`rust:1.80.1-alpine`](#rust1801-alpine)
-	[`rust:1.80.1-alpine3.19`](#rust1801-alpine319)
-	[`rust:1.80.1-alpine3.20`](#rust1801-alpine320)
-	[`rust:1.80.1-bookworm`](#rust1801-bookworm)
-	[`rust:1.80.1-bullseye`](#rust1801-bullseye)
-	[`rust:1.80.1-slim`](#rust1801-slim)
-	[`rust:1.80.1-slim-bookworm`](#rust1801-slim-bookworm)
-	[`rust:1.80.1-slim-bullseye`](#rust1801-slim-bullseye)
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
$ docker pull rust@sha256:d22d8938f0403ee31c118b5bf2162b883313dd7f387f859d9f2accd7c884c385
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
$ docker pull rust@sha256:883df89a3ed53fb0e0f6a67d79cfebf72906d97f9d816379fdf941af969be1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529316453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a14ebf5765b504232d2db40bfcd2a69b22156ada6f3880a2c34f3819fbd115`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ff076d818ad6b8557e03e10c83657cc716ab287c8380054ff91571c8cae81`  
		Last Modified: Wed, 04 Sep 2024 23:02:08 GMT  
		Size: 211.3 MB (211266623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f8a55b70e1cdd0ddc6b738b3a1baeadd53644ee6819ff60426e800045a98b0`  
		Last Modified: Thu, 05 Sep 2024 00:29:41 GMT  
		Size: 180.3 MB (180291957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:6ba93cd0c1015d1e433471ab39bd16a063af791c7331e18df530f8e6fe722b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085cfe3bb88e92259308df253ca6817c99f844fa21d86e0c22fe8cf9636007eb`

```dockerfile
```

-	Layers:
	-	`sha256:01b822a94cc2d7c507e8248d8c5d3e6c9bd0ced556d1a385cb8329261573c353`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 15.4 MB (15445058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd49b3074e925710d484fdd75b4d3689f4de021889974dec39020d6925a4719`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:b6f344496c19f4a91adffeb1c6f3975ed4f0c134965451cc96505002f8a7bd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d72160a77779d619c0691d2d11e9cefcf875d6caba4743817d21439067c8493`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e3c71ceb3b7032e8a78ea70e306ec97b152570eeaae849a0c97bb61b2b12287f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe61db625a1b529903f1126ded0caa9e4e1c247503d524cd43bc15454b6bcc2f`  
		Last Modified: Tue, 13 Aug 2024 01:00:32 GMT  
		Size: 45.1 MB (45148160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06599d70e5763853acd56f8e4938729e068e7942382f335f96ce0ae3bc5a63a`  
		Last Modified: Tue, 13 Aug 2024 01:32:20 GMT  
		Size: 22.0 MB (21954622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3af44a3c0ce16617696528373b53738420f91f3383cda1666cc673cbf6fe50`  
		Last Modified: Tue, 13 Aug 2024 01:32:41 GMT  
		Size: 59.2 MB (59221928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dd2b78206591edf08b24f09f26f742a3d689be108f6e3cf74538c78a14b7d8`  
		Last Modified: Tue, 13 Aug 2024 01:33:16 GMT  
		Size: 175.2 MB (175182857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4fbda85fa1661a9607ed15220d6cd0ba0ea7cfe8f07296134db5ed818046e5`  
		Last Modified: Wed, 14 Aug 2024 00:19:33 GMT  
		Size: 216.6 MB (216645579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:1ddf44bae2a2ab49522a19c70acf650db42bb2f6c68e2dfba4087a2465283dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364116a8162d50ac678aca565a1904bfbfc433d01d7bfb4d35fa37480d1ee7d3`

```dockerfile
```

-	Layers:
	-	`sha256:2381d137772c59a7125907148fb80cbd972483f5c489ea3758959c92823577f7`  
		Last Modified: Wed, 14 Aug 2024 00:19:29 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:befe4b689653998a8d04333bd6495dbe1e85862cc244c47d41fe0a25d659ed10`  
		Last Modified: Wed, 14 Aug 2024 00:19:28 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fda6ddc43a715feab22a98e1bcd801537ce6788377cf1d4919e08819a335cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8219a5ff56d4a59051986054024af17d4463ef5e7adcdae8e770fb8af061687f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275677961327bd0cf394699228e29d7caf27f171c627899a20ebc9eeb550e209`  
		Last Modified: Tue, 13 Aug 2024 01:09:34 GMT  
		Size: 64.0 MB (63994880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46e144614e1ae9b82b5d89d16a31a506542733eabceebfac041e0192dfafcf4`  
		Last Modified: Tue, 13 Aug 2024 01:10:06 GMT  
		Size: 202.6 MB (202624176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8a9c35b14d62b7daaefd544a6bbd91b6c1fab2f57de7223cb3c2db641f8f3f`  
		Last Modified: Tue, 13 Aug 2024 19:47:59 GMT  
		Size: 249.9 MB (249924612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:94216dd82c491d7e6f65884930be2ef3b32567829f661b973bf6de9670caf8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8403ed68ffd2e12e6bb5977a46b702d64bfe7042a23546abf7e9a207f9a7b82a`

```dockerfile
```

-	Layers:
	-	`sha256:c73483c681ff733971d6bac2c66743acb42444bba080cb661d51c906d243b6de`  
		Last Modified: Tue, 13 Aug 2024 19:47:54 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27ab72a7b07fef9cb15504b90ff201b9db8849760efaab45970b5339508eecf2`  
		Last Modified: Tue, 13 Aug 2024 19:47:53 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:8f7ec0c462a97974a827203da3d48a0e0b650b3134b6ff62d4351bc4d35fd88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544833213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b757d10a8aa83b2245bf2670352842b8001028cf212163001100db5cdde0e97d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0a7648037128b800dbf0363e27e6092c0253e0bd9beeb38a8aa572225934be`  
		Last Modified: Wed, 04 Sep 2024 23:21:06 GMT  
		Size: 210.2 MB (210181614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff91319e9e7fc8f2ebbd39fb7eea49ff32d26c0a80075db4be2000172b1e2c2`  
		Last Modified: Thu, 05 Sep 2024 00:29:34 GMT  
		Size: 193.2 MB (193190646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:89423d1df8d449f51c36385120c91be4bda5ca07d565c86391e83b052273eee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15436735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d654f978ebaf05551dd313df3e6572228fc317f1462fbfdb238633e8f72fd6`

```dockerfile
```

-	Layers:
	-	`sha256:ea624d5326397b6cff430e813450f3b7fe48aa493d7c1d50fcd441a09ff02a90`  
		Last Modified: Thu, 05 Sep 2024 00:29:29 GMT  
		Size: 15.4 MB (15423818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb7e5ec2189b610823dc5ef4564f4af35bd76533a4a716c603c9ed8112e1c9f`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:4230383893f246794d2aec426cdeae0c6d6559692181a139b8035d7e0e9d73cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554124880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d39abdea1b0ddb7070a48b89cdc15e163bcde224eca74a0a407a3262dd26a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35476fbf45cb5153abf5ea2df7487a74d0cd0de327ba5e9e970713f9e385650`  
		Last Modified: Tue, 13 Aug 2024 01:35:51 GMT  
		Size: 214.3 MB (214264660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a28f21591d3325119c396461297085c135f02fe0c43f55e5d9d04babfe7f8a`  
		Last Modified: Tue, 13 Aug 2024 21:43:47 GMT  
		Size: 191.0 MB (191025993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:fbe15bbd473bc7a23be790e4137162ff70e31cbb32389f146816a3880926436a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a621b08bd27a06288b964fba10a38173fa5365c5ddc7e8a9cccb7618ca77ac`

```dockerfile
```

-	Layers:
	-	`sha256:327622dc45cc14d8fa9bfdeff84b04b9db53727ba825e799d576336b111a738f`  
		Last Modified: Tue, 13 Aug 2024 21:43:41 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a0869e8a6fa0e4af601c1b3715fc98fa182a33f1fb3f0f496d5860b0aee948a`  
		Last Modified: Tue, 13 Aug 2024 21:43:40 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:7b40e1bbb384a9e7239ae1b346dfdcddcc6425cad2d1117869ccdefaf0de3092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581466000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456a0c8f4b4dc0ce6ef7658d91e2dee89d72fc4c661d9f8cfe429d7bb25f907d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d84b8bb13cbf61ae13e4c378871c52c3e9b521657a5faa02f0159e1be542a05`  
		Last Modified: Tue, 13 Aug 2024 01:25:25 GMT  
		Size: 183.3 MB (183265629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7110931c79b785aa170a85a350cfeaf7e6a2f5422afbf81362184df95653f728`  
		Last Modified: Tue, 13 Aug 2024 20:55:34 GMT  
		Size: 263.1 MB (263095149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:4117efcb78d41d704ce0a167cacf739449fda5091e7871c7e274690dc616d093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971437f70ca6e9f6a749c7db65a07092f93076ec42375222e3ddc55b9a04a1a2`

```dockerfile
```

-	Layers:
	-	`sha256:9b04722e355f910725ee8dfca9c787edafbb9ce2d45729798f8e0e75d9f2f969`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2abf42730b95caa5d1a2d651db714bd4b84a8497980620b6f55cc3b01090eff8`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:b3ac1f65cf33390407c9b90558eb41e7a8311c47d836fca5800960f1aa2d11d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:25c79c9854cd4bedc797a88e2d4dc1b4502d22a540867fa66257e6e03c4c1d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279155377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204c24ee400cc1a13c13b275cb04657bc5e47150ce5a4e77d3a7671021b9a32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061bdf3a42c6c4489e9e78047cdaa3af6f7b63e5d255e0ab9e6660d180836f4`  
		Last Modified: Thu, 08 Aug 2024 20:02:39 GMT  
		Size: 55.3 MB (55346819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acee9c63bebda8ae8f027b6e99deee99e570d38430b1f5de3f271f853c530cc`  
		Last Modified: Thu, 08 Aug 2024 20:02:41 GMT  
		Size: 220.4 MB (220389518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:d7f847716cae21dc55ac84add1dab418798ef33b8624854fb6b8c65f17169302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b861f59014e11471235b45ca58fe55e1bce20e2d3235649938ddd8e10ac83b`

```dockerfile
```

-	Layers:
	-	`sha256:cda40d4b828cdfea673ac423a0571622627c241817509f9ba745a38be1560b4f`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e221181fdb20703a089d816b169375986ae47adf4002808cc72821fdf9b9e942`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1c9472feed43f2708eaa2821cf5f0a646160cee7be9d584bf730e755eedbee94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286589138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040de42a611e54d884e5a00d1765df3de096fba714c4defafc0750e79bcb340e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1b276de5f8a8a2fd3e6b931c4e180f78458c812dda2346f21361c13108618d`  
		Last Modified: Fri, 26 Jul 2024 00:29:37 GMT  
		Size: 53.0 MB (52995484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2abe5cb54c2cfbfce48a309498337e7a126ab4ea86b6df2ef36f1613354c5c4`  
		Last Modified: Thu, 08 Aug 2024 20:22:15 GMT  
		Size: 230.2 MB (230235196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:c808914252afc74e4ba729fb24e0bb95b91c9a2f8608b2a35bd39fc92b7d5a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27a7713ca3e5389a8f63774d2f2029f10a884a7ef5258c5a110ac3cc5fa9642`

```dockerfile
```

-	Layers:
	-	`sha256:dab1ad55931d3701c8a9c82cd1652b524d00f22c57bd6fc291789059b83165e3`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a90f930d575ecabd7599845ca4411c5bf521f8695acca03fbc6142619add3f7`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.20`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:d22d8938f0403ee31c118b5bf2162b883313dd7f387f859d9f2accd7c884c385
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
$ docker pull rust@sha256:883df89a3ed53fb0e0f6a67d79cfebf72906d97f9d816379fdf941af969be1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529316453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a14ebf5765b504232d2db40bfcd2a69b22156ada6f3880a2c34f3819fbd115`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ff076d818ad6b8557e03e10c83657cc716ab287c8380054ff91571c8cae81`  
		Last Modified: Wed, 04 Sep 2024 23:02:08 GMT  
		Size: 211.3 MB (211266623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f8a55b70e1cdd0ddc6b738b3a1baeadd53644ee6819ff60426e800045a98b0`  
		Last Modified: Thu, 05 Sep 2024 00:29:41 GMT  
		Size: 180.3 MB (180291957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:6ba93cd0c1015d1e433471ab39bd16a063af791c7331e18df530f8e6fe722b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085cfe3bb88e92259308df253ca6817c99f844fa21d86e0c22fe8cf9636007eb`

```dockerfile
```

-	Layers:
	-	`sha256:01b822a94cc2d7c507e8248d8c5d3e6c9bd0ced556d1a385cb8329261573c353`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 15.4 MB (15445058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd49b3074e925710d484fdd75b4d3689f4de021889974dec39020d6925a4719`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:b6f344496c19f4a91adffeb1c6f3975ed4f0c134965451cc96505002f8a7bd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d72160a77779d619c0691d2d11e9cefcf875d6caba4743817d21439067c8493`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e3c71ceb3b7032e8a78ea70e306ec97b152570eeaae849a0c97bb61b2b12287f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe61db625a1b529903f1126ded0caa9e4e1c247503d524cd43bc15454b6bcc2f`  
		Last Modified: Tue, 13 Aug 2024 01:00:32 GMT  
		Size: 45.1 MB (45148160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06599d70e5763853acd56f8e4938729e068e7942382f335f96ce0ae3bc5a63a`  
		Last Modified: Tue, 13 Aug 2024 01:32:20 GMT  
		Size: 22.0 MB (21954622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3af44a3c0ce16617696528373b53738420f91f3383cda1666cc673cbf6fe50`  
		Last Modified: Tue, 13 Aug 2024 01:32:41 GMT  
		Size: 59.2 MB (59221928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dd2b78206591edf08b24f09f26f742a3d689be108f6e3cf74538c78a14b7d8`  
		Last Modified: Tue, 13 Aug 2024 01:33:16 GMT  
		Size: 175.2 MB (175182857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4fbda85fa1661a9607ed15220d6cd0ba0ea7cfe8f07296134db5ed818046e5`  
		Last Modified: Wed, 14 Aug 2024 00:19:33 GMT  
		Size: 216.6 MB (216645579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1ddf44bae2a2ab49522a19c70acf650db42bb2f6c68e2dfba4087a2465283dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364116a8162d50ac678aca565a1904bfbfc433d01d7bfb4d35fa37480d1ee7d3`

```dockerfile
```

-	Layers:
	-	`sha256:2381d137772c59a7125907148fb80cbd972483f5c489ea3758959c92823577f7`  
		Last Modified: Wed, 14 Aug 2024 00:19:29 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:befe4b689653998a8d04333bd6495dbe1e85862cc244c47d41fe0a25d659ed10`  
		Last Modified: Wed, 14 Aug 2024 00:19:28 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fda6ddc43a715feab22a98e1bcd801537ce6788377cf1d4919e08819a335cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8219a5ff56d4a59051986054024af17d4463ef5e7adcdae8e770fb8af061687f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275677961327bd0cf394699228e29d7caf27f171c627899a20ebc9eeb550e209`  
		Last Modified: Tue, 13 Aug 2024 01:09:34 GMT  
		Size: 64.0 MB (63994880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46e144614e1ae9b82b5d89d16a31a506542733eabceebfac041e0192dfafcf4`  
		Last Modified: Tue, 13 Aug 2024 01:10:06 GMT  
		Size: 202.6 MB (202624176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8a9c35b14d62b7daaefd544a6bbd91b6c1fab2f57de7223cb3c2db641f8f3f`  
		Last Modified: Tue, 13 Aug 2024 19:47:59 GMT  
		Size: 249.9 MB (249924612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:94216dd82c491d7e6f65884930be2ef3b32567829f661b973bf6de9670caf8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8403ed68ffd2e12e6bb5977a46b702d64bfe7042a23546abf7e9a207f9a7b82a`

```dockerfile
```

-	Layers:
	-	`sha256:c73483c681ff733971d6bac2c66743acb42444bba080cb661d51c906d243b6de`  
		Last Modified: Tue, 13 Aug 2024 19:47:54 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27ab72a7b07fef9cb15504b90ff201b9db8849760efaab45970b5339508eecf2`  
		Last Modified: Tue, 13 Aug 2024 19:47:53 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:8f7ec0c462a97974a827203da3d48a0e0b650b3134b6ff62d4351bc4d35fd88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544833213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b757d10a8aa83b2245bf2670352842b8001028cf212163001100db5cdde0e97d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0a7648037128b800dbf0363e27e6092c0253e0bd9beeb38a8aa572225934be`  
		Last Modified: Wed, 04 Sep 2024 23:21:06 GMT  
		Size: 210.2 MB (210181614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff91319e9e7fc8f2ebbd39fb7eea49ff32d26c0a80075db4be2000172b1e2c2`  
		Last Modified: Thu, 05 Sep 2024 00:29:34 GMT  
		Size: 193.2 MB (193190646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:89423d1df8d449f51c36385120c91be4bda5ca07d565c86391e83b052273eee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15436735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d654f978ebaf05551dd313df3e6572228fc317f1462fbfdb238633e8f72fd6`

```dockerfile
```

-	Layers:
	-	`sha256:ea624d5326397b6cff430e813450f3b7fe48aa493d7c1d50fcd441a09ff02a90`  
		Last Modified: Thu, 05 Sep 2024 00:29:29 GMT  
		Size: 15.4 MB (15423818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb7e5ec2189b610823dc5ef4564f4af35bd76533a4a716c603c9ed8112e1c9f`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:4230383893f246794d2aec426cdeae0c6d6559692181a139b8035d7e0e9d73cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554124880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d39abdea1b0ddb7070a48b89cdc15e163bcde224eca74a0a407a3262dd26a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35476fbf45cb5153abf5ea2df7487a74d0cd0de327ba5e9e970713f9e385650`  
		Last Modified: Tue, 13 Aug 2024 01:35:51 GMT  
		Size: 214.3 MB (214264660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a28f21591d3325119c396461297085c135f02fe0c43f55e5d9d04babfe7f8a`  
		Last Modified: Tue, 13 Aug 2024 21:43:47 GMT  
		Size: 191.0 MB (191025993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:fbe15bbd473bc7a23be790e4137162ff70e31cbb32389f146816a3880926436a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a621b08bd27a06288b964fba10a38173fa5365c5ddc7e8a9cccb7618ca77ac`

```dockerfile
```

-	Layers:
	-	`sha256:327622dc45cc14d8fa9bfdeff84b04b9db53727ba825e799d576336b111a738f`  
		Last Modified: Tue, 13 Aug 2024 21:43:41 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a0869e8a6fa0e4af601c1b3715fc98fa182a33f1fb3f0f496d5860b0aee948a`  
		Last Modified: Tue, 13 Aug 2024 21:43:40 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:7b40e1bbb384a9e7239ae1b346dfdcddcc6425cad2d1117869ccdefaf0de3092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581466000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456a0c8f4b4dc0ce6ef7658d91e2dee89d72fc4c661d9f8cfe429d7bb25f907d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d84b8bb13cbf61ae13e4c378871c52c3e9b521657a5faa02f0159e1be542a05`  
		Last Modified: Tue, 13 Aug 2024 01:25:25 GMT  
		Size: 183.3 MB (183265629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7110931c79b785aa170a85a350cfeaf7e6a2f5422afbf81362184df95653f728`  
		Last Modified: Tue, 13 Aug 2024 20:55:34 GMT  
		Size: 263.1 MB (263095149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4117efcb78d41d704ce0a167cacf739449fda5091e7871c7e274690dc616d093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971437f70ca6e9f6a749c7db65a07092f93076ec42375222e3ddc55b9a04a1a2`

```dockerfile
```

-	Layers:
	-	`sha256:9b04722e355f910725ee8dfca9c787edafbb9ce2d45729798f8e0e75d9f2f969`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2abf42730b95caa5d1a2d651db714bd4b84a8497980620b6f55cc3b01090eff8`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:f6f599d3f027a97fb60cb87854199fcde390e25cee216712c3f9eede545b052e
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

### `rust:1-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:cd0a8eb7afeec51e842d834ddf4b153b583427c04da5ac5ef222046604f2318d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.9 MB (502931767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884e2fd2885bf130e08c231e991c8955ce71fb9d987128c310adc962761785db`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d691dff6d17d00b0cbbc4772eb805d97e02504d89ea3e5857cb97c943b74462`  
		Last Modified: Wed, 04 Sep 2024 23:02:33 GMT  
		Size: 54.7 MB (54726023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cfd30604666dfdd92bea930c06ee58dc927e0da651b862491af1648a4aca73`  
		Last Modified: Wed, 04 Sep 2024 23:03:03 GMT  
		Size: 197.1 MB (197067753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed0b0ded1b8b5f8453e7635369b38f8b2c318d0f51e26f0ad4269979ea9ba32`  
		Last Modified: Thu, 05 Sep 2024 00:29:16 GMT  
		Size: 180.3 MB (180292264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f2a08571ef0de6347d1fa328909f711aa08ca828ae893b1b9ec79d43dce4c54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15064067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd481bb1b4a6912e1c25b6c10d942ed60669c539876c401676bfb21ce5ba1b38`

```dockerfile
```

-	Layers:
	-	`sha256:62bbe7371ce9ed40e4bd78dc1e1895a7a86b51139e8a6c0ba845bb8a9e7c01d2`  
		Last Modified: Thu, 05 Sep 2024 00:29:12 GMT  
		Size: 15.1 MB (15052263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8510778438d2ad2268e7ca558d841d6f5554bde8515952028f0afb9fc9af50b5`  
		Last Modified: Thu, 05 Sep 2024 00:29:10 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:b9e1bff441726839efdfa70625797c71d12ed393eff196835675985011379a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.6 MB (499629389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232ed045be751771b4dd1a9891b4b8771355c7d382c7eacb30508c0719434f31`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:7674761630f1c6dfdf95da576bd19dbfe7bc4d942d11d31eff2012ec8b2c7ff1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a986643b6b9d356e3c44ee35fdd352a1064e1fb2a1524c0627e84ba34207b8e2`  
		Last Modified: Tue, 13 Aug 2024 01:01:15 GMT  
		Size: 50.2 MB (50242333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8868560f8e978ee832f67027b7330376be350ffacd30a199b730c72d9550757`  
		Last Modified: Tue, 13 Aug 2024 01:33:28 GMT  
		Size: 14.9 MB (14879497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7deb3ed53b620f0871f5051050fe0d850fd52da94803425820e75bb7b8d4e2e`  
		Last Modified: Tue, 13 Aug 2024 01:33:45 GMT  
		Size: 50.4 MB (50357748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e6955cecd9dc8a3cc8022dd624334d4f3abc81e5801bb1a1d3ddcedd0ef645`  
		Last Modified: Tue, 13 Aug 2024 01:34:17 GMT  
		Size: 167.5 MB (167504270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d727c90103f0458fc4e1233059a99a4449a5658b19c4c04577e90716624ce68`  
		Last Modified: Wed, 14 Aug 2024 00:15:35 GMT  
		Size: 216.6 MB (216645541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:791c2d9db3d160e7e2a93c07568a9ba817c8588b5b3cdd31d37d029feff257b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14865179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc5a22e7dce30f830f957bd7ca405686def79f80919b6f3216dc62e91b57d20`

```dockerfile
```

-	Layers:
	-	`sha256:ea5f09999dd237783aaffbaf7252ec89e60410eefce29c463657d21103fad00c`  
		Last Modified: Wed, 14 Aug 2024 00:15:31 GMT  
		Size: 14.9 MB (14853305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2c6135a6881efe9cfaee1c1973570d4094d9c8efd4330011c071c0287552ad3`  
		Last Modified: Wed, 14 Aug 2024 00:15:30 GMT  
		Size: 11.9 KB (11874 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1dc2b70be87ca21e1298d3966b4821a1f2af9ca4aeb9030f2843156acaabc871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564070284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac07cd629c9ba7cac0f43633a49d02c086f7d0a89d75cdbe31f5443ad59d12d3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3db3ee6245513b1422983db21d89f4f743f300e726af9eff6c9f7e2dddcb67`  
		Last Modified: Tue, 13 Aug 2024 01:10:18 GMT  
		Size: 15.7 MB (15749505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5265d6983e8ed11fd8dc48e17209d3479015214ac92f89f4ac51b2e65060840`  
		Last Modified: Tue, 13 Aug 2024 01:10:33 GMT  
		Size: 54.7 MB (54694302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6073a281eb20b3b43e3cc472efa9f868c8f75fc13cae51a5b10fbe8054bc0ba0`  
		Last Modified: Tue, 13 Aug 2024 01:11:01 GMT  
		Size: 190.0 MB (189971927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15778b247abba33689070973283c965347f8ff7110aed80aba5d5dba886c8645`  
		Last Modified: Tue, 13 Aug 2024 19:46:34 GMT  
		Size: 249.9 MB (249924629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:050d7ffca1af96c20c5a95e9bee8bcd60d8c633ad6a598ed9807cf27439bb339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15066748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc0ceb3fdbd1db1a0bd675c616fcf05e981968d3be62ab462b147b4db354be2`

```dockerfile
```

-	Layers:
	-	`sha256:f3db632e0133fc65815084a91d7a97b2ef1b92d6c4127dc1e3a5b0852c77df14`  
		Last Modified: Tue, 13 Aug 2024 19:46:25 GMT  
		Size: 15.1 MB (15054632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:244e55ed7bcf50ecd68fa3c5e2277c974b6fe67c02fafbffdea96539a80b40d8`  
		Last Modified: Tue, 13 Aug 2024 19:46:24 GMT  
		Size: 12.1 KB (12116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:0b422e50d57c5086836b9b8dca05019ed63192ac2333521c92bc739dbb756427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.5 MB (521530165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfe8c5eaa38c914901128e3ea98bc83c9a639434eaf17b029b52761c8f6ec1c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4533261556c046eefdf517bc6e06bc455b876caf2226aa504a13b5d66d250281`  
		Last Modified: Wed, 04 Sep 2024 23:21:18 GMT  
		Size: 16.3 MB (16268301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341d50e4bbed9704aae2147f28b4a07fc71b73539d282c37f60e183d38865daf`  
		Last Modified: Wed, 04 Sep 2024 23:21:37 GMT  
		Size: 56.0 MB (56030074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d04d357b859cf9b5eb038042f7df289289aee35371021b6ba1005ff2818f428`  
		Last Modified: Wed, 04 Sep 2024 23:22:18 GMT  
		Size: 200.0 MB (199965007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a20660c7aef3eb352454fc403634b2bcff1e7bdf3d17279cd89af22056aa8d`  
		Last Modified: Thu, 05 Sep 2024 00:29:13 GMT  
		Size: 193.2 MB (193190616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0d0978b42325c7b639503fb6f81b435992e69cbb7cfaf3e43d43c7b73fb50a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57f256b77b0a5a96e6a8ec76adfeb153cb387874a4c211a0315b1113bbf662f`

```dockerfile
```

-	Layers:
	-	`sha256:5bfb69f09b1dfbfac72a0286789043735bcd7e8a317c1ff5fdbcdb83d28c4cb9`  
		Last Modified: Thu, 05 Sep 2024 00:29:09 GMT  
		Size: 15.0 MB (15040800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab48a51d9f27782d97a1e808bbe2f638eb8b4a0edc389264cd649bfe7be2808`  
		Last Modified: Thu, 05 Sep 2024 00:29:08 GMT  
		Size: 11.8 KB (11775 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:4b102819b654a311a824ae3a605e6503b76070cd4c4dfc6c227ff67f300c9a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.0 MB (522017613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3b534b39a25e918707b482ef622be1a3c9c8a8fa0889209dc5e17728198e1b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:25dc93c8090a0afba4b41321f81883857bfdd6b30ea9f278833c5a5d9d16ad52 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:dad1c3eca3bf4b2a67cef1dbad507d7a913df7bbe1e3f88044230dd291ada39d`  
		Last Modified: Tue, 13 Aug 2024 00:26:46 GMT  
		Size: 59.0 MB (58954654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b50eef4accfc66462c4cf81c03bb57857b5f3ac891da5b87bfdf1ba826c9677`  
		Last Modified: Tue, 13 Aug 2024 01:36:03 GMT  
		Size: 16.8 MB (16765928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df0e65d951ce5d0b07cbb65477bbb01cfa607241b5c5855f4fb361bedfd1247`  
		Last Modified: Tue, 13 Aug 2024 01:36:21 GMT  
		Size: 58.9 MB (58872586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9438dc035d6f851416f6745a25baa330ca04b6013564731b2c42ddce3979a2ff`  
		Last Modified: Tue, 13 Aug 2024 01:36:57 GMT  
		Size: 196.4 MB (196398494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2565e4d615d926780548ef217b5b10b6f6720e401eba39fa2e54c34ac84bf`  
		Last Modified: Tue, 13 Aug 2024 21:41:58 GMT  
		Size: 191.0 MB (191025951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1447a0430183c6f9369fac6336bfeb4153f534eca6028b5b7f2a14f47a2eea7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15031565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4180a14646f843e73bc293d0bcf988986daa9a36f1818b643d0cbf4f72e8750b`

```dockerfile
```

-	Layers:
	-	`sha256:2e9e4840d282072216185364f3c9012dc3dd727785c3f7bcabcfba3f85cea47b`  
		Last Modified: Tue, 13 Aug 2024 21:41:47 GMT  
		Size: 15.0 MB (15019723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96395652f5022ec8fee2d3878beed560d61f66c18c72f6d1208e66097a7b25d6`  
		Last Modified: Tue, 13 Aug 2024 21:41:45 GMT  
		Size: 11.8 KB (11842 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:3944244146d900e21947895f40f80b74185b5ec24475ac7026203cf5835798ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 MB (559197374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3320425c6a524ca810ff5aa40074b451cbfd12bd85905918328c6f2c509542ea`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c695efccb58000e04eb154deca02ce22ea52fd05ee4246281c66bb7a42d20a96`  
		Last Modified: Tue, 13 Aug 2024 01:25:32 GMT  
		Size: 15.6 MB (15641934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3f87ffa253b4cb357637ad56494facf5bf533f6fd3bdf78f1066c6fb0fb23`  
		Last Modified: Tue, 13 Aug 2024 01:25:44 GMT  
		Size: 54.1 MB (54075217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b49e88f43277ce63fe01761080f821f3b3be9f581e45ed6dbb50b5168642a1`  
		Last Modified: Tue, 13 Aug 2024 01:26:08 GMT  
		Size: 173.1 MB (173060876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854c1c6359c025e4a47dfbac10a25e7961b24a754123354e9bc34bab7f277cd3`  
		Last Modified: Tue, 13 Aug 2024 20:53:28 GMT  
		Size: 263.1 MB (263095258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f3b7b40296ae25b3e80cc721493168b0e9a8b31191a5a589e1fdd64b7b46399e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf30e97755ca96ffe5387849e8ecfcbdf192586a462d01ace8c46d46294ea4bd`

```dockerfile
```

-	Layers:
	-	`sha256:14c9edf50d643bb3a3325e61fe0eca2f0e8449f141b26517a7cfb0ddd62f37be`  
		Last Modified: Tue, 13 Aug 2024 20:53:23 GMT  
		Size: 14.9 MB (14873217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c86f1e8337e8e681287c7507a3b747611ffa4a577e92858bcd2c92dc3271eba`  
		Last Modified: Tue, 13 Aug 2024 20:53:22 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:907ff4b3ee7df57149ffee04f606e0a08b9b2ed3507f00a19cf3c9c0f74b7681
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
$ docker pull rust@sha256:a5ec1fc7928df7d24504ba8d0e7d9d096513736c5e1b6ac2eac686324a7419a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280194591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d74dd89cb787e264870a35d96127262dd06602fa988a39dfcdcc0b1b87fbe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bf03ed1c368822e027a2732362680f56ce5137e91ba84ce386e51fd189061c`  
		Last Modified: Wed, 04 Sep 2024 23:12:37 GMT  
		Size: 251.1 MB (251068107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:70c0f4a4e29a19fbc259b978e407d0198b3ac61100c49416558e718dd524198c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01702ebd45abe4c0861513492e59d285a1ddae1839f8e5329d1860652f8d06f6`

```dockerfile
```

-	Layers:
	-	`sha256:c76a08813897d00f0e0cd93710bc88f5964d3f99c81a2b63b3b37de6b1b76a4b`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 3.9 MB (3945035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8859af7c414d89532ca7d9eaabba0766d80d3479215e254051332407fdcd00e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:cc2333aa663bbc92356ee4ef6f8d6b642b445e5e666fc37b3867b0d5a5a893bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289213250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e848b8369d06b2c98853e0ef79cb6d790e729403484bc5f943edb29e2b9de6c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee65094ca49c2c7edf34dada1ae62118e6659c97a5f195e52d279a877fc800fc`  
		Last Modified: Thu, 05 Sep 2024 12:10:55 GMT  
		Size: 264.5 MB (264494985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:f2f6983e05e6ff77da77143b68cc48199d9ab5a09fba06cbee4c136d9e6882dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afc164a0e9d2735af5dcca73cb4960c28e6606be6974bc2c6ce6d2b5ef62f0e`

```dockerfile
```

-	Layers:
	-	`sha256:27bae23be9fa45ed1c009e8d69e579013b3f8c8b8ca757f8f9013ad7d9d27438`  
		Last Modified: Thu, 05 Sep 2024 12:10:49 GMT  
		Size: 3.8 MB (3761492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d87d0772c2929243aa21fe4b3f0ff0ac589b73e19adfed9d306123093fca53ba`  
		Last Modified: Thu, 05 Sep 2024 12:10:48 GMT  
		Size: 13.2 KB (13155 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:bbaff9e88af760191966cb0beadf94d503e1fafcd63b5c5ccaaa03e5598564b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290925711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca74e88b45440ef8d55e5c25ed0f7f2e9dbb4f2a8bafec24e6cccd1107c80d47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f23ccaebd9d56a75909c850e6ab0aa6693c9f89ba57b9977dba601890f2d94`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 260.8 MB (260781417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:149c847e4d5940e34735ec36d6b663715f0fa8e9ee11a0282d4f1dd871808c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc742cbf65f608e8de19416358e8901fba122e86286e96175686e134e9ccf789`

```dockerfile
```

-	Layers:
	-	`sha256:b5443a5469154e30b37c7de0b36037a6e20bddc881a424cdccd8843d369dcf48`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 3.9 MB (3926448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513d8a278aa21dcacbe90a3c89ef597af1dff583466d0036a15dcb4031011e06`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:d2d2feff3c61a9801dbe7735d194d197592c10a07446ebb5f58c360d44704e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292910541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7509806f664093ad6ec12f7fb65501f3540a72ac9809b5258a8d9d45ece500`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49174d43929c3e7d189a8935d2a77a8a17ce21f7070c6f983f380f120cdb6ae`  
		Last Modified: Thu, 05 Sep 2024 06:24:07 GMT  
		Size: 259.8 MB (259788183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:8ea384b40e2596497636656084514cc2dbfed040b686146c648676e33089efde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d551dc594d848945573fc2616217aee09021e04156415504cb1e6928f3fc4ecc`

```dockerfile
```

-	Layers:
	-	`sha256:af2dbf67be2945aa925798a7e18da8e96c52f624747225bffbdd0072388ec033`  
		Last Modified: Thu, 05 Sep 2024 06:24:01 GMT  
		Size: 3.9 MB (3917197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec30cdde83a25decfe9823cb5f543ce23f66684e6eb8437b988758d6a1d5ae8`  
		Last Modified: Thu, 05 Sep 2024 06:24:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:5e90e95a277cd1027f1ae3ba58dbdd1931c63ea9df38cb2221b06fe6dcec728f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340720684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8674b49ddd39434ab78416cdec54b901fceb062293e8069f1f0471ce40433e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594be6304f123a21b952480d35d2ed44c27f35cfe89018bf16a599b5022cb653`  
		Last Modified: Thu, 05 Sep 2024 07:11:55 GMT  
		Size: 313.2 MB (313230363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:df46a7b656a5378d8e6f0d320f4b2e4e629806b496e187e4aafa54adf82aed84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6739776cf152581ed3a68005323f9befa6f39245508765ad2724fccb84d6524`

```dockerfile
```

-	Layers:
	-	`sha256:574a1afcca67c6ddd0a7e471fdca0a769f0620648631b878ad4399a3be51c698`  
		Last Modified: Thu, 05 Sep 2024 07:11:50 GMT  
		Size: 3.8 MB (3787360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:239faceff7d2873bf0a8f549a7a3bb22ddc18eea16d381f8e5c529f659546778`  
		Last Modified: Thu, 05 Sep 2024 07:11:49 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:907ff4b3ee7df57149ffee04f606e0a08b9b2ed3507f00a19cf3c9c0f74b7681
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
$ docker pull rust@sha256:a5ec1fc7928df7d24504ba8d0e7d9d096513736c5e1b6ac2eac686324a7419a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280194591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d74dd89cb787e264870a35d96127262dd06602fa988a39dfcdcc0b1b87fbe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bf03ed1c368822e027a2732362680f56ce5137e91ba84ce386e51fd189061c`  
		Last Modified: Wed, 04 Sep 2024 23:12:37 GMT  
		Size: 251.1 MB (251068107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:70c0f4a4e29a19fbc259b978e407d0198b3ac61100c49416558e718dd524198c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01702ebd45abe4c0861513492e59d285a1ddae1839f8e5329d1860652f8d06f6`

```dockerfile
```

-	Layers:
	-	`sha256:c76a08813897d00f0e0cd93710bc88f5964d3f99c81a2b63b3b37de6b1b76a4b`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 3.9 MB (3945035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8859af7c414d89532ca7d9eaabba0766d80d3479215e254051332407fdcd00e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:cc2333aa663bbc92356ee4ef6f8d6b642b445e5e666fc37b3867b0d5a5a893bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289213250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e848b8369d06b2c98853e0ef79cb6d790e729403484bc5f943edb29e2b9de6c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee65094ca49c2c7edf34dada1ae62118e6659c97a5f195e52d279a877fc800fc`  
		Last Modified: Thu, 05 Sep 2024 12:10:55 GMT  
		Size: 264.5 MB (264494985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f2f6983e05e6ff77da77143b68cc48199d9ab5a09fba06cbee4c136d9e6882dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afc164a0e9d2735af5dcca73cb4960c28e6606be6974bc2c6ce6d2b5ef62f0e`

```dockerfile
```

-	Layers:
	-	`sha256:27bae23be9fa45ed1c009e8d69e579013b3f8c8b8ca757f8f9013ad7d9d27438`  
		Last Modified: Thu, 05 Sep 2024 12:10:49 GMT  
		Size: 3.8 MB (3761492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d87d0772c2929243aa21fe4b3f0ff0ac589b73e19adfed9d306123093fca53ba`  
		Last Modified: Thu, 05 Sep 2024 12:10:48 GMT  
		Size: 13.2 KB (13155 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:bbaff9e88af760191966cb0beadf94d503e1fafcd63b5c5ccaaa03e5598564b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290925711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca74e88b45440ef8d55e5c25ed0f7f2e9dbb4f2a8bafec24e6cccd1107c80d47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f23ccaebd9d56a75909c850e6ab0aa6693c9f89ba57b9977dba601890f2d94`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 260.8 MB (260781417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:149c847e4d5940e34735ec36d6b663715f0fa8e9ee11a0282d4f1dd871808c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc742cbf65f608e8de19416358e8901fba122e86286e96175686e134e9ccf789`

```dockerfile
```

-	Layers:
	-	`sha256:b5443a5469154e30b37c7de0b36037a6e20bddc881a424cdccd8843d369dcf48`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 3.9 MB (3926448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513d8a278aa21dcacbe90a3c89ef597af1dff583466d0036a15dcb4031011e06`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d2d2feff3c61a9801dbe7735d194d197592c10a07446ebb5f58c360d44704e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292910541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7509806f664093ad6ec12f7fb65501f3540a72ac9809b5258a8d9d45ece500`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49174d43929c3e7d189a8935d2a77a8a17ce21f7070c6f983f380f120cdb6ae`  
		Last Modified: Thu, 05 Sep 2024 06:24:07 GMT  
		Size: 259.8 MB (259788183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8ea384b40e2596497636656084514cc2dbfed040b686146c648676e33089efde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d551dc594d848945573fc2616217aee09021e04156415504cb1e6928f3fc4ecc`

```dockerfile
```

-	Layers:
	-	`sha256:af2dbf67be2945aa925798a7e18da8e96c52f624747225bffbdd0072388ec033`  
		Last Modified: Thu, 05 Sep 2024 06:24:01 GMT  
		Size: 3.9 MB (3917197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec30cdde83a25decfe9823cb5f543ce23f66684e6eb8437b988758d6a1d5ae8`  
		Last Modified: Thu, 05 Sep 2024 06:24:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:5e90e95a277cd1027f1ae3ba58dbdd1931c63ea9df38cb2221b06fe6dcec728f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340720684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8674b49ddd39434ab78416cdec54b901fceb062293e8069f1f0471ce40433e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594be6304f123a21b952480d35d2ed44c27f35cfe89018bf16a599b5022cb653`  
		Last Modified: Thu, 05 Sep 2024 07:11:55 GMT  
		Size: 313.2 MB (313230363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:df46a7b656a5378d8e6f0d320f4b2e4e629806b496e187e4aafa54adf82aed84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6739776cf152581ed3a68005323f9befa6f39245508765ad2724fccb84d6524`

```dockerfile
```

-	Layers:
	-	`sha256:574a1afcca67c6ddd0a7e471fdca0a769f0620648631b878ad4399a3be51c698`  
		Last Modified: Thu, 05 Sep 2024 07:11:50 GMT  
		Size: 3.8 MB (3787360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:239faceff7d2873bf0a8f549a7a3bb22ddc18eea16d381f8e5c529f659546778`  
		Last Modified: Thu, 05 Sep 2024 07:11:49 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:3bddded5af7155cafc29701e0701bcf3712a407fc7d642423760ec266e5a0682
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

### `rust:1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:11fbefae37d29d4b00e0b566b044cc3a6b872505aef297eb9b155fdacf677a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271859977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8888f7ee42b36e189196bd0c8bcaa7b82dbe62234fd5dece168368ef9f93bc1b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009542abce00716699fc9f02523d81058a5e4a326eae717d2fea8c06f55be526`  
		Last Modified: Wed, 04 Sep 2024 23:12:34 GMT  
		Size: 240.4 MB (240431300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6b2212261e50269ab865ff857cfd68b718e0401726883d6493ee31389b62e67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c6bb2b68bcf2dfda78433017e4d559b0e95616710d78a278a33f9792c49d48`

```dockerfile
```

-	Layers:
	-	`sha256:d9798046ab832947c5ae4ab6c01783c3230b53dad783b0dc2cb0c1f33f4c18fe`  
		Last Modified: Wed, 04 Sep 2024 23:12:28 GMT  
		Size: 4.2 MB (4164313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ed06d2ab6037ccd8879f98a11ef9c5634091df7e2b0df0353a8abc4c0da8632`  
		Last Modified: Wed, 04 Sep 2024 23:12:28 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:10334b6ea7d1540cc93a254d83cd2523a51498acec6550d9c498e8a08d48cc5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285518044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985c6ec0023ef93ca3b509422da444dedbe01e3a9d5be254679b43319cbbf8cd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:c451ece1244c14bce110ffbe6906867ce12f8e88234988b0edba91009a9dbbf8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f572303598915f7fb61cc4b47f7207c9ee64d52b9db5fc03ee133ec2dd679347`  
		Last Modified: Wed, 04 Sep 2024 22:02:25 GMT  
		Size: 26.6 MB (26589615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6ad557e4a293fcec008cedd79106f6ef955c5e24dd1cf657b7e40744cbd440`  
		Last Modified: Thu, 05 Sep 2024 12:09:02 GMT  
		Size: 258.9 MB (258928429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:185308415291c86011485ca6ae5c6c9d24cd0c0455ce31e92cf3c83745b877e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bf9c70231335a286bd907aabb78dd6e765230974619f7450019bae997fdae2`

```dockerfile
```

-	Layers:
	-	`sha256:0ca59ac3c5a0d7f54b0976168e45637127fce7006546c43de9f9cd9f69156945`  
		Last Modified: Thu, 05 Sep 2024 12:08:56 GMT  
		Size: 4.0 MB (3973664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f211237bf8e70aada0e861f20fdf49b04c778600c8657efe317c065eefeb7569`  
		Last Modified: Thu, 05 Sep 2024 12:08:56 GMT  
		Size: 11.9 KB (11936 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea400ae221974016cf01cfc99716046022430cc14de5608db498729f7618f668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.7 MB (335717687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290fe501a9234536387b5b30c99f27e439d23d64536b7815fe2de01d3682d07f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cb6cdc1948b06794974ff2e98a7005fb4728291f972fd9fe6890a51b35589`  
		Last Modified: Tue, 13 Aug 2024 11:45:59 GMT  
		Size: 305.6 MB (305641600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a3676673a581a4a22ae35dba326c5d9ccd2bdbde7ba9cfab0820cb96773f78ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621cc11386fc3351be6a2c44213e137c509b73cbc571f6de7541e04cbe8a4ac1`

```dockerfile
```

-	Layers:
	-	`sha256:25d0ce1b84cd190aa843a54b2f062344d99aacfdeb1f4215da7fc975e859651e`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 4.2 MB (4161095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66c9bde30e15c9a5a38892f97be33009492c2633b0fd4b560fb3907e93ecf62`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 12.2 KB (12175 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:c57675f231e19c0114750c276bb686ec8f0125ca00ee3e1d1b5cbae8aa6e9c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286389854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688be6d01f10da5e726acf8027b050c5d0962197d8e667b43261dd385a0c4f33`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f518608d5d6e978d31e2f8814affa386d3c917837a7823597d8d0c86477c8ee`  
		Last Modified: Thu, 05 Sep 2024 00:29:16 GMT  
		Size: 254.0 MB (253976540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b8f569048c31e591add1ab0d8b9f3f7cdc3272c6072100db265bb675887e53bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b1c275df90e1f83fc7b09b7a4c32c00de4fcc7346e5ccb68c1c4d1125c6a8a`

```dockerfile
```

-	Layers:
	-	`sha256:c70252172c1a37c2fb6ce0894158a216a4c5a6219906aa119f3e9e9ba2a7a3e1`  
		Last Modified: Thu, 05 Sep 2024 00:29:11 GMT  
		Size: 4.2 MB (4156081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e4cc08677260612ec187771e82aba25a4655648cf3a308d21be1aac5637858`  
		Last Modified: Thu, 05 Sep 2024 00:29:11 GMT  
		Size: 11.8 KB (11837 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:3b063eaf3446b0a4b0201201275e496c4cd37e2df97786f5d7dc11872b49b3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281302014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dbc33dcd7620a227caf71dad7ca84f2c231ca26a65558ec553fc37860ad920`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb61bbbd90ca687d8cf9a0fa307847411b891a05ea61c9d5075175311224639a`  
		Last Modified: Thu, 05 Sep 2024 06:21:52 GMT  
		Size: 246.0 MB (246002740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d63496117c7b6330c99ea4b31e3cbc463e1a92f1262350984fe3b84bfb625403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc7ee7587c6a789c8c0cb6838e839d1bc47ef5a05fb52e1a8aecd9ba1309500`

```dockerfile
```

-	Layers:
	-	`sha256:e119f05f2002b1464fc5731d6d2308b0ee4020a17744313cb4811c29106c6988`  
		Last Modified: Thu, 05 Sep 2024 06:21:46 GMT  
		Size: 4.1 MB (4125251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a7aed5f5e3aaffc866e0aea2a3e9c3e60ffd7bd2e2c5f077eae9468fe3db810`  
		Last Modified: Thu, 05 Sep 2024 06:21:45 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:f454359a3d4de0bd0fb0c063a4b2366299600bdafe2a34fce998a23bd87a25b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.1 MB (335147088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295366e0c73019a39ee770be37d3e862fefdfb2d00b4f7c49596abdad9e970a7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16cb9b3555a4b7e7bf56b97db7af5a62cffeb6ab93ea0db4eb8789c042664f7`  
		Last Modified: Thu, 05 Sep 2024 07:10:02 GMT  
		Size: 305.5 MB (305483641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:12bb9211940c142484034d59efb2b6239d0aac58cdddb50774003ddf6be8b843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6295da41651110039f4ab6f25165e32bb9af3ac5f36ff76349f61c20645b6e6`

```dockerfile
```

-	Layers:
	-	`sha256:a827dd2d48d500c33de79a8d81e812dace7251b737e92fd0238c8aeabbf45f26`  
		Last Modified: Thu, 05 Sep 2024 07:09:57 GMT  
		Size: 4.0 MB (3996088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2044074a697d1c663a041eb3ace815004e270dbc711679b502f0c86f5edbb643`  
		Last Modified: Thu, 05 Sep 2024 07:09:57 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80`

```console
$ docker pull rust@sha256:d22d8938f0403ee31c118b5bf2162b883313dd7f387f859d9f2accd7c884c385
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

### `rust:1.80` - linux; amd64

```console
$ docker pull rust@sha256:883df89a3ed53fb0e0f6a67d79cfebf72906d97f9d816379fdf941af969be1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529316453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a14ebf5765b504232d2db40bfcd2a69b22156ada6f3880a2c34f3819fbd115`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ff076d818ad6b8557e03e10c83657cc716ab287c8380054ff91571c8cae81`  
		Last Modified: Wed, 04 Sep 2024 23:02:08 GMT  
		Size: 211.3 MB (211266623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f8a55b70e1cdd0ddc6b738b3a1baeadd53644ee6819ff60426e800045a98b0`  
		Last Modified: Thu, 05 Sep 2024 00:29:41 GMT  
		Size: 180.3 MB (180291957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80` - unknown; unknown

```console
$ docker pull rust@sha256:6ba93cd0c1015d1e433471ab39bd16a063af791c7331e18df530f8e6fe722b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085cfe3bb88e92259308df253ca6817c99f844fa21d86e0c22fe8cf9636007eb`

```dockerfile
```

-	Layers:
	-	`sha256:01b822a94cc2d7c507e8248d8c5d3e6c9bd0ced556d1a385cb8329261573c353`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 15.4 MB (15445058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd49b3074e925710d484fdd75b4d3689f4de021889974dec39020d6925a4719`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80` - linux; arm variant v7

```console
$ docker pull rust@sha256:b6f344496c19f4a91adffeb1c6f3975ed4f0c134965451cc96505002f8a7bd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d72160a77779d619c0691d2d11e9cefcf875d6caba4743817d21439067c8493`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e3c71ceb3b7032e8a78ea70e306ec97b152570eeaae849a0c97bb61b2b12287f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe61db625a1b529903f1126ded0caa9e4e1c247503d524cd43bc15454b6bcc2f`  
		Last Modified: Tue, 13 Aug 2024 01:00:32 GMT  
		Size: 45.1 MB (45148160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06599d70e5763853acd56f8e4938729e068e7942382f335f96ce0ae3bc5a63a`  
		Last Modified: Tue, 13 Aug 2024 01:32:20 GMT  
		Size: 22.0 MB (21954622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3af44a3c0ce16617696528373b53738420f91f3383cda1666cc673cbf6fe50`  
		Last Modified: Tue, 13 Aug 2024 01:32:41 GMT  
		Size: 59.2 MB (59221928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dd2b78206591edf08b24f09f26f742a3d689be108f6e3cf74538c78a14b7d8`  
		Last Modified: Tue, 13 Aug 2024 01:33:16 GMT  
		Size: 175.2 MB (175182857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4fbda85fa1661a9607ed15220d6cd0ba0ea7cfe8f07296134db5ed818046e5`  
		Last Modified: Wed, 14 Aug 2024 00:19:33 GMT  
		Size: 216.6 MB (216645579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80` - unknown; unknown

```console
$ docker pull rust@sha256:1ddf44bae2a2ab49522a19c70acf650db42bb2f6c68e2dfba4087a2465283dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364116a8162d50ac678aca565a1904bfbfc433d01d7bfb4d35fa37480d1ee7d3`

```dockerfile
```

-	Layers:
	-	`sha256:2381d137772c59a7125907148fb80cbd972483f5c489ea3758959c92823577f7`  
		Last Modified: Wed, 14 Aug 2024 00:19:29 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:befe4b689653998a8d04333bd6495dbe1e85862cc244c47d41fe0a25d659ed10`  
		Last Modified: Wed, 14 Aug 2024 00:19:28 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fda6ddc43a715feab22a98e1bcd801537ce6788377cf1d4919e08819a335cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8219a5ff56d4a59051986054024af17d4463ef5e7adcdae8e770fb8af061687f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275677961327bd0cf394699228e29d7caf27f171c627899a20ebc9eeb550e209`  
		Last Modified: Tue, 13 Aug 2024 01:09:34 GMT  
		Size: 64.0 MB (63994880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46e144614e1ae9b82b5d89d16a31a506542733eabceebfac041e0192dfafcf4`  
		Last Modified: Tue, 13 Aug 2024 01:10:06 GMT  
		Size: 202.6 MB (202624176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8a9c35b14d62b7daaefd544a6bbd91b6c1fab2f57de7223cb3c2db641f8f3f`  
		Last Modified: Tue, 13 Aug 2024 19:47:59 GMT  
		Size: 249.9 MB (249924612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80` - unknown; unknown

```console
$ docker pull rust@sha256:94216dd82c491d7e6f65884930be2ef3b32567829f661b973bf6de9670caf8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8403ed68ffd2e12e6bb5977a46b702d64bfe7042a23546abf7e9a207f9a7b82a`

```dockerfile
```

-	Layers:
	-	`sha256:c73483c681ff733971d6bac2c66743acb42444bba080cb661d51c906d243b6de`  
		Last Modified: Tue, 13 Aug 2024 19:47:54 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27ab72a7b07fef9cb15504b90ff201b9db8849760efaab45970b5339508eecf2`  
		Last Modified: Tue, 13 Aug 2024 19:47:53 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80` - linux; 386

```console
$ docker pull rust@sha256:8f7ec0c462a97974a827203da3d48a0e0b650b3134b6ff62d4351bc4d35fd88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544833213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b757d10a8aa83b2245bf2670352842b8001028cf212163001100db5cdde0e97d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0a7648037128b800dbf0363e27e6092c0253e0bd9beeb38a8aa572225934be`  
		Last Modified: Wed, 04 Sep 2024 23:21:06 GMT  
		Size: 210.2 MB (210181614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff91319e9e7fc8f2ebbd39fb7eea49ff32d26c0a80075db4be2000172b1e2c2`  
		Last Modified: Thu, 05 Sep 2024 00:29:34 GMT  
		Size: 193.2 MB (193190646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80` - unknown; unknown

```console
$ docker pull rust@sha256:89423d1df8d449f51c36385120c91be4bda5ca07d565c86391e83b052273eee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15436735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d654f978ebaf05551dd313df3e6572228fc317f1462fbfdb238633e8f72fd6`

```dockerfile
```

-	Layers:
	-	`sha256:ea624d5326397b6cff430e813450f3b7fe48aa493d7c1d50fcd441a09ff02a90`  
		Last Modified: Thu, 05 Sep 2024 00:29:29 GMT  
		Size: 15.4 MB (15423818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb7e5ec2189b610823dc5ef4564f4af35bd76533a4a716c603c9ed8112e1c9f`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80` - linux; ppc64le

```console
$ docker pull rust@sha256:4230383893f246794d2aec426cdeae0c6d6559692181a139b8035d7e0e9d73cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554124880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d39abdea1b0ddb7070a48b89cdc15e163bcde224eca74a0a407a3262dd26a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35476fbf45cb5153abf5ea2df7487a74d0cd0de327ba5e9e970713f9e385650`  
		Last Modified: Tue, 13 Aug 2024 01:35:51 GMT  
		Size: 214.3 MB (214264660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a28f21591d3325119c396461297085c135f02fe0c43f55e5d9d04babfe7f8a`  
		Last Modified: Tue, 13 Aug 2024 21:43:47 GMT  
		Size: 191.0 MB (191025993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80` - unknown; unknown

```console
$ docker pull rust@sha256:fbe15bbd473bc7a23be790e4137162ff70e31cbb32389f146816a3880926436a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a621b08bd27a06288b964fba10a38173fa5365c5ddc7e8a9cccb7618ca77ac`

```dockerfile
```

-	Layers:
	-	`sha256:327622dc45cc14d8fa9bfdeff84b04b9db53727ba825e799d576336b111a738f`  
		Last Modified: Tue, 13 Aug 2024 21:43:41 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a0869e8a6fa0e4af601c1b3715fc98fa182a33f1fb3f0f496d5860b0aee948a`  
		Last Modified: Tue, 13 Aug 2024 21:43:40 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80` - linux; s390x

```console
$ docker pull rust@sha256:7b40e1bbb384a9e7239ae1b346dfdcddcc6425cad2d1117869ccdefaf0de3092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581466000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456a0c8f4b4dc0ce6ef7658d91e2dee89d72fc4c661d9f8cfe429d7bb25f907d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d84b8bb13cbf61ae13e4c378871c52c3e9b521657a5faa02f0159e1be542a05`  
		Last Modified: Tue, 13 Aug 2024 01:25:25 GMT  
		Size: 183.3 MB (183265629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7110931c79b785aa170a85a350cfeaf7e6a2f5422afbf81362184df95653f728`  
		Last Modified: Tue, 13 Aug 2024 20:55:34 GMT  
		Size: 263.1 MB (263095149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80` - unknown; unknown

```console
$ docker pull rust@sha256:4117efcb78d41d704ce0a167cacf739449fda5091e7871c7e274690dc616d093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971437f70ca6e9f6a749c7db65a07092f93076ec42375222e3ddc55b9a04a1a2`

```dockerfile
```

-	Layers:
	-	`sha256:9b04722e355f910725ee8dfca9c787edafbb9ce2d45729798f8e0e75d9f2f969`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2abf42730b95caa5d1a2d651db714bd4b84a8497980620b6f55cc3b01090eff8`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-alpine`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.80-alpine` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-alpine3.19`

```console
$ docker pull rust@sha256:b3ac1f65cf33390407c9b90558eb41e7a8311c47d836fca5800960f1aa2d11d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.80-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:25c79c9854cd4bedc797a88e2d4dc1b4502d22a540867fa66257e6e03c4c1d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279155377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204c24ee400cc1a13c13b275cb04657bc5e47150ce5a4e77d3a7671021b9a32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061bdf3a42c6c4489e9e78047cdaa3af6f7b63e5d255e0ab9e6660d180836f4`  
		Last Modified: Thu, 08 Aug 2024 20:02:39 GMT  
		Size: 55.3 MB (55346819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acee9c63bebda8ae8f027b6e99deee99e570d38430b1f5de3f271f853c530cc`  
		Last Modified: Thu, 08 Aug 2024 20:02:41 GMT  
		Size: 220.4 MB (220389518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:d7f847716cae21dc55ac84add1dab418798ef33b8624854fb6b8c65f17169302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b861f59014e11471235b45ca58fe55e1bce20e2d3235649938ddd8e10ac83b`

```dockerfile
```

-	Layers:
	-	`sha256:cda40d4b828cdfea673ac423a0571622627c241817509f9ba745a38be1560b4f`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e221181fdb20703a089d816b169375986ae47adf4002808cc72821fdf9b9e942`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1c9472feed43f2708eaa2821cf5f0a646160cee7be9d584bf730e755eedbee94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286589138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040de42a611e54d884e5a00d1765df3de096fba714c4defafc0750e79bcb340e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1b276de5f8a8a2fd3e6b931c4e180f78458c812dda2346f21361c13108618d`  
		Last Modified: Fri, 26 Jul 2024 00:29:37 GMT  
		Size: 53.0 MB (52995484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2abe5cb54c2cfbfce48a309498337e7a126ab4ea86b6df2ef36f1613354c5c4`  
		Last Modified: Thu, 08 Aug 2024 20:22:15 GMT  
		Size: 230.2 MB (230235196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:c808914252afc74e4ba729fb24e0bb95b91c9a2f8608b2a35bd39fc92b7d5a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27a7713ca3e5389a8f63774d2f2029f10a884a7ef5258c5a110ac3cc5fa9642`

```dockerfile
```

-	Layers:
	-	`sha256:dab1ad55931d3701c8a9c82cd1652b524d00f22c57bd6fc291789059b83165e3`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a90f930d575ecabd7599845ca4411c5bf521f8695acca03fbc6142619add3f7`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-alpine3.20`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.80-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-bookworm`

```console
$ docker pull rust@sha256:d22d8938f0403ee31c118b5bf2162b883313dd7f387f859d9f2accd7c884c385
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

### `rust:1.80-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:883df89a3ed53fb0e0f6a67d79cfebf72906d97f9d816379fdf941af969be1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529316453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a14ebf5765b504232d2db40bfcd2a69b22156ada6f3880a2c34f3819fbd115`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ff076d818ad6b8557e03e10c83657cc716ab287c8380054ff91571c8cae81`  
		Last Modified: Wed, 04 Sep 2024 23:02:08 GMT  
		Size: 211.3 MB (211266623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f8a55b70e1cdd0ddc6b738b3a1baeadd53644ee6819ff60426e800045a98b0`  
		Last Modified: Thu, 05 Sep 2024 00:29:41 GMT  
		Size: 180.3 MB (180291957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:6ba93cd0c1015d1e433471ab39bd16a063af791c7331e18df530f8e6fe722b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085cfe3bb88e92259308df253ca6817c99f844fa21d86e0c22fe8cf9636007eb`

```dockerfile
```

-	Layers:
	-	`sha256:01b822a94cc2d7c507e8248d8c5d3e6c9bd0ced556d1a385cb8329261573c353`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 15.4 MB (15445058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd49b3074e925710d484fdd75b4d3689f4de021889974dec39020d6925a4719`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:b6f344496c19f4a91adffeb1c6f3975ed4f0c134965451cc96505002f8a7bd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d72160a77779d619c0691d2d11e9cefcf875d6caba4743817d21439067c8493`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e3c71ceb3b7032e8a78ea70e306ec97b152570eeaae849a0c97bb61b2b12287f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe61db625a1b529903f1126ded0caa9e4e1c247503d524cd43bc15454b6bcc2f`  
		Last Modified: Tue, 13 Aug 2024 01:00:32 GMT  
		Size: 45.1 MB (45148160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06599d70e5763853acd56f8e4938729e068e7942382f335f96ce0ae3bc5a63a`  
		Last Modified: Tue, 13 Aug 2024 01:32:20 GMT  
		Size: 22.0 MB (21954622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3af44a3c0ce16617696528373b53738420f91f3383cda1666cc673cbf6fe50`  
		Last Modified: Tue, 13 Aug 2024 01:32:41 GMT  
		Size: 59.2 MB (59221928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dd2b78206591edf08b24f09f26f742a3d689be108f6e3cf74538c78a14b7d8`  
		Last Modified: Tue, 13 Aug 2024 01:33:16 GMT  
		Size: 175.2 MB (175182857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4fbda85fa1661a9607ed15220d6cd0ba0ea7cfe8f07296134db5ed818046e5`  
		Last Modified: Wed, 14 Aug 2024 00:19:33 GMT  
		Size: 216.6 MB (216645579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1ddf44bae2a2ab49522a19c70acf650db42bb2f6c68e2dfba4087a2465283dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364116a8162d50ac678aca565a1904bfbfc433d01d7bfb4d35fa37480d1ee7d3`

```dockerfile
```

-	Layers:
	-	`sha256:2381d137772c59a7125907148fb80cbd972483f5c489ea3758959c92823577f7`  
		Last Modified: Wed, 14 Aug 2024 00:19:29 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:befe4b689653998a8d04333bd6495dbe1e85862cc244c47d41fe0a25d659ed10`  
		Last Modified: Wed, 14 Aug 2024 00:19:28 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fda6ddc43a715feab22a98e1bcd801537ce6788377cf1d4919e08819a335cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8219a5ff56d4a59051986054024af17d4463ef5e7adcdae8e770fb8af061687f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275677961327bd0cf394699228e29d7caf27f171c627899a20ebc9eeb550e209`  
		Last Modified: Tue, 13 Aug 2024 01:09:34 GMT  
		Size: 64.0 MB (63994880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46e144614e1ae9b82b5d89d16a31a506542733eabceebfac041e0192dfafcf4`  
		Last Modified: Tue, 13 Aug 2024 01:10:06 GMT  
		Size: 202.6 MB (202624176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8a9c35b14d62b7daaefd544a6bbd91b6c1fab2f57de7223cb3c2db641f8f3f`  
		Last Modified: Tue, 13 Aug 2024 19:47:59 GMT  
		Size: 249.9 MB (249924612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:94216dd82c491d7e6f65884930be2ef3b32567829f661b973bf6de9670caf8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8403ed68ffd2e12e6bb5977a46b702d64bfe7042a23546abf7e9a207f9a7b82a`

```dockerfile
```

-	Layers:
	-	`sha256:c73483c681ff733971d6bac2c66743acb42444bba080cb661d51c906d243b6de`  
		Last Modified: Tue, 13 Aug 2024 19:47:54 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27ab72a7b07fef9cb15504b90ff201b9db8849760efaab45970b5339508eecf2`  
		Last Modified: Tue, 13 Aug 2024 19:47:53 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bookworm` - linux; 386

```console
$ docker pull rust@sha256:8f7ec0c462a97974a827203da3d48a0e0b650b3134b6ff62d4351bc4d35fd88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544833213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b757d10a8aa83b2245bf2670352842b8001028cf212163001100db5cdde0e97d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0a7648037128b800dbf0363e27e6092c0253e0bd9beeb38a8aa572225934be`  
		Last Modified: Wed, 04 Sep 2024 23:21:06 GMT  
		Size: 210.2 MB (210181614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff91319e9e7fc8f2ebbd39fb7eea49ff32d26c0a80075db4be2000172b1e2c2`  
		Last Modified: Thu, 05 Sep 2024 00:29:34 GMT  
		Size: 193.2 MB (193190646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:89423d1df8d449f51c36385120c91be4bda5ca07d565c86391e83b052273eee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15436735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d654f978ebaf05551dd313df3e6572228fc317f1462fbfdb238633e8f72fd6`

```dockerfile
```

-	Layers:
	-	`sha256:ea624d5326397b6cff430e813450f3b7fe48aa493d7c1d50fcd441a09ff02a90`  
		Last Modified: Thu, 05 Sep 2024 00:29:29 GMT  
		Size: 15.4 MB (15423818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb7e5ec2189b610823dc5ef4564f4af35bd76533a4a716c603c9ed8112e1c9f`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:4230383893f246794d2aec426cdeae0c6d6559692181a139b8035d7e0e9d73cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554124880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d39abdea1b0ddb7070a48b89cdc15e163bcde224eca74a0a407a3262dd26a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35476fbf45cb5153abf5ea2df7487a74d0cd0de327ba5e9e970713f9e385650`  
		Last Modified: Tue, 13 Aug 2024 01:35:51 GMT  
		Size: 214.3 MB (214264660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a28f21591d3325119c396461297085c135f02fe0c43f55e5d9d04babfe7f8a`  
		Last Modified: Tue, 13 Aug 2024 21:43:47 GMT  
		Size: 191.0 MB (191025993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:fbe15bbd473bc7a23be790e4137162ff70e31cbb32389f146816a3880926436a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a621b08bd27a06288b964fba10a38173fa5365c5ddc7e8a9cccb7618ca77ac`

```dockerfile
```

-	Layers:
	-	`sha256:327622dc45cc14d8fa9bfdeff84b04b9db53727ba825e799d576336b111a738f`  
		Last Modified: Tue, 13 Aug 2024 21:43:41 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a0869e8a6fa0e4af601c1b3715fc98fa182a33f1fb3f0f496d5860b0aee948a`  
		Last Modified: Tue, 13 Aug 2024 21:43:40 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:7b40e1bbb384a9e7239ae1b346dfdcddcc6425cad2d1117869ccdefaf0de3092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581466000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456a0c8f4b4dc0ce6ef7658d91e2dee89d72fc4c661d9f8cfe429d7bb25f907d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d84b8bb13cbf61ae13e4c378871c52c3e9b521657a5faa02f0159e1be542a05`  
		Last Modified: Tue, 13 Aug 2024 01:25:25 GMT  
		Size: 183.3 MB (183265629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7110931c79b785aa170a85a350cfeaf7e6a2f5422afbf81362184df95653f728`  
		Last Modified: Tue, 13 Aug 2024 20:55:34 GMT  
		Size: 263.1 MB (263095149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4117efcb78d41d704ce0a167cacf739449fda5091e7871c7e274690dc616d093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971437f70ca6e9f6a749c7db65a07092f93076ec42375222e3ddc55b9a04a1a2`

```dockerfile
```

-	Layers:
	-	`sha256:9b04722e355f910725ee8dfca9c787edafbb9ce2d45729798f8e0e75d9f2f969`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2abf42730b95caa5d1a2d651db714bd4b84a8497980620b6f55cc3b01090eff8`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-bullseye`

```console
$ docker pull rust@sha256:f6f599d3f027a97fb60cb87854199fcde390e25cee216712c3f9eede545b052e
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

### `rust:1.80-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:cd0a8eb7afeec51e842d834ddf4b153b583427c04da5ac5ef222046604f2318d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.9 MB (502931767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884e2fd2885bf130e08c231e991c8955ce71fb9d987128c310adc962761785db`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d691dff6d17d00b0cbbc4772eb805d97e02504d89ea3e5857cb97c943b74462`  
		Last Modified: Wed, 04 Sep 2024 23:02:33 GMT  
		Size: 54.7 MB (54726023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cfd30604666dfdd92bea930c06ee58dc927e0da651b862491af1648a4aca73`  
		Last Modified: Wed, 04 Sep 2024 23:03:03 GMT  
		Size: 197.1 MB (197067753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed0b0ded1b8b5f8453e7635369b38f8b2c318d0f51e26f0ad4269979ea9ba32`  
		Last Modified: Thu, 05 Sep 2024 00:29:16 GMT  
		Size: 180.3 MB (180292264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f2a08571ef0de6347d1fa328909f711aa08ca828ae893b1b9ec79d43dce4c54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15064067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd481bb1b4a6912e1c25b6c10d942ed60669c539876c401676bfb21ce5ba1b38`

```dockerfile
```

-	Layers:
	-	`sha256:62bbe7371ce9ed40e4bd78dc1e1895a7a86b51139e8a6c0ba845bb8a9e7c01d2`  
		Last Modified: Thu, 05 Sep 2024 00:29:12 GMT  
		Size: 15.1 MB (15052263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8510778438d2ad2268e7ca558d841d6f5554bde8515952028f0afb9fc9af50b5`  
		Last Modified: Thu, 05 Sep 2024 00:29:10 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:b9e1bff441726839efdfa70625797c71d12ed393eff196835675985011379a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.6 MB (499629389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232ed045be751771b4dd1a9891b4b8771355c7d382c7eacb30508c0719434f31`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:7674761630f1c6dfdf95da576bd19dbfe7bc4d942d11d31eff2012ec8b2c7ff1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a986643b6b9d356e3c44ee35fdd352a1064e1fb2a1524c0627e84ba34207b8e2`  
		Last Modified: Tue, 13 Aug 2024 01:01:15 GMT  
		Size: 50.2 MB (50242333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8868560f8e978ee832f67027b7330376be350ffacd30a199b730c72d9550757`  
		Last Modified: Tue, 13 Aug 2024 01:33:28 GMT  
		Size: 14.9 MB (14879497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7deb3ed53b620f0871f5051050fe0d850fd52da94803425820e75bb7b8d4e2e`  
		Last Modified: Tue, 13 Aug 2024 01:33:45 GMT  
		Size: 50.4 MB (50357748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e6955cecd9dc8a3cc8022dd624334d4f3abc81e5801bb1a1d3ddcedd0ef645`  
		Last Modified: Tue, 13 Aug 2024 01:34:17 GMT  
		Size: 167.5 MB (167504270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d727c90103f0458fc4e1233059a99a4449a5658b19c4c04577e90716624ce68`  
		Last Modified: Wed, 14 Aug 2024 00:15:35 GMT  
		Size: 216.6 MB (216645541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:791c2d9db3d160e7e2a93c07568a9ba817c8588b5b3cdd31d37d029feff257b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14865179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc5a22e7dce30f830f957bd7ca405686def79f80919b6f3216dc62e91b57d20`

```dockerfile
```

-	Layers:
	-	`sha256:ea5f09999dd237783aaffbaf7252ec89e60410eefce29c463657d21103fad00c`  
		Last Modified: Wed, 14 Aug 2024 00:15:31 GMT  
		Size: 14.9 MB (14853305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2c6135a6881efe9cfaee1c1973570d4094d9c8efd4330011c071c0287552ad3`  
		Last Modified: Wed, 14 Aug 2024 00:15:30 GMT  
		Size: 11.9 KB (11874 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1dc2b70be87ca21e1298d3966b4821a1f2af9ca4aeb9030f2843156acaabc871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564070284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac07cd629c9ba7cac0f43633a49d02c086f7d0a89d75cdbe31f5443ad59d12d3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3db3ee6245513b1422983db21d89f4f743f300e726af9eff6c9f7e2dddcb67`  
		Last Modified: Tue, 13 Aug 2024 01:10:18 GMT  
		Size: 15.7 MB (15749505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5265d6983e8ed11fd8dc48e17209d3479015214ac92f89f4ac51b2e65060840`  
		Last Modified: Tue, 13 Aug 2024 01:10:33 GMT  
		Size: 54.7 MB (54694302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6073a281eb20b3b43e3cc472efa9f868c8f75fc13cae51a5b10fbe8054bc0ba0`  
		Last Modified: Tue, 13 Aug 2024 01:11:01 GMT  
		Size: 190.0 MB (189971927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15778b247abba33689070973283c965347f8ff7110aed80aba5d5dba886c8645`  
		Last Modified: Tue, 13 Aug 2024 19:46:34 GMT  
		Size: 249.9 MB (249924629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:050d7ffca1af96c20c5a95e9bee8bcd60d8c633ad6a598ed9807cf27439bb339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15066748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc0ceb3fdbd1db1a0bd675c616fcf05e981968d3be62ab462b147b4db354be2`

```dockerfile
```

-	Layers:
	-	`sha256:f3db632e0133fc65815084a91d7a97b2ef1b92d6c4127dc1e3a5b0852c77df14`  
		Last Modified: Tue, 13 Aug 2024 19:46:25 GMT  
		Size: 15.1 MB (15054632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:244e55ed7bcf50ecd68fa3c5e2277c974b6fe67c02fafbffdea96539a80b40d8`  
		Last Modified: Tue, 13 Aug 2024 19:46:24 GMT  
		Size: 12.1 KB (12116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bullseye` - linux; 386

```console
$ docker pull rust@sha256:0b422e50d57c5086836b9b8dca05019ed63192ac2333521c92bc739dbb756427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.5 MB (521530165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfe8c5eaa38c914901128e3ea98bc83c9a639434eaf17b029b52761c8f6ec1c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4533261556c046eefdf517bc6e06bc455b876caf2226aa504a13b5d66d250281`  
		Last Modified: Wed, 04 Sep 2024 23:21:18 GMT  
		Size: 16.3 MB (16268301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341d50e4bbed9704aae2147f28b4a07fc71b73539d282c37f60e183d38865daf`  
		Last Modified: Wed, 04 Sep 2024 23:21:37 GMT  
		Size: 56.0 MB (56030074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d04d357b859cf9b5eb038042f7df289289aee35371021b6ba1005ff2818f428`  
		Last Modified: Wed, 04 Sep 2024 23:22:18 GMT  
		Size: 200.0 MB (199965007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a20660c7aef3eb352454fc403634b2bcff1e7bdf3d17279cd89af22056aa8d`  
		Last Modified: Thu, 05 Sep 2024 00:29:13 GMT  
		Size: 193.2 MB (193190616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0d0978b42325c7b639503fb6f81b435992e69cbb7cfaf3e43d43c7b73fb50a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57f256b77b0a5a96e6a8ec76adfeb153cb387874a4c211a0315b1113bbf662f`

```dockerfile
```

-	Layers:
	-	`sha256:5bfb69f09b1dfbfac72a0286789043735bcd7e8a317c1ff5fdbcdb83d28c4cb9`  
		Last Modified: Thu, 05 Sep 2024 00:29:09 GMT  
		Size: 15.0 MB (15040800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab48a51d9f27782d97a1e808bbe2f638eb8b4a0edc389264cd649bfe7be2808`  
		Last Modified: Thu, 05 Sep 2024 00:29:08 GMT  
		Size: 11.8 KB (11775 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:4b102819b654a311a824ae3a605e6503b76070cd4c4dfc6c227ff67f300c9a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.0 MB (522017613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3b534b39a25e918707b482ef622be1a3c9c8a8fa0889209dc5e17728198e1b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:25dc93c8090a0afba4b41321f81883857bfdd6b30ea9f278833c5a5d9d16ad52 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:dad1c3eca3bf4b2a67cef1dbad507d7a913df7bbe1e3f88044230dd291ada39d`  
		Last Modified: Tue, 13 Aug 2024 00:26:46 GMT  
		Size: 59.0 MB (58954654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b50eef4accfc66462c4cf81c03bb57857b5f3ac891da5b87bfdf1ba826c9677`  
		Last Modified: Tue, 13 Aug 2024 01:36:03 GMT  
		Size: 16.8 MB (16765928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df0e65d951ce5d0b07cbb65477bbb01cfa607241b5c5855f4fb361bedfd1247`  
		Last Modified: Tue, 13 Aug 2024 01:36:21 GMT  
		Size: 58.9 MB (58872586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9438dc035d6f851416f6745a25baa330ca04b6013564731b2c42ddce3979a2ff`  
		Last Modified: Tue, 13 Aug 2024 01:36:57 GMT  
		Size: 196.4 MB (196398494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2565e4d615d926780548ef217b5b10b6f6720e401eba39fa2e54c34ac84bf`  
		Last Modified: Tue, 13 Aug 2024 21:41:58 GMT  
		Size: 191.0 MB (191025951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1447a0430183c6f9369fac6336bfeb4153f534eca6028b5b7f2a14f47a2eea7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15031565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4180a14646f843e73bc293d0bcf988986daa9a36f1818b643d0cbf4f72e8750b`

```dockerfile
```

-	Layers:
	-	`sha256:2e9e4840d282072216185364f3c9012dc3dd727785c3f7bcabcfba3f85cea47b`  
		Last Modified: Tue, 13 Aug 2024 21:41:47 GMT  
		Size: 15.0 MB (15019723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96395652f5022ec8fee2d3878beed560d61f66c18c72f6d1208e66097a7b25d6`  
		Last Modified: Tue, 13 Aug 2024 21:41:45 GMT  
		Size: 11.8 KB (11842 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:3944244146d900e21947895f40f80b74185b5ec24475ac7026203cf5835798ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 MB (559197374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3320425c6a524ca810ff5aa40074b451cbfd12bd85905918328c6f2c509542ea`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c695efccb58000e04eb154deca02ce22ea52fd05ee4246281c66bb7a42d20a96`  
		Last Modified: Tue, 13 Aug 2024 01:25:32 GMT  
		Size: 15.6 MB (15641934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3f87ffa253b4cb357637ad56494facf5bf533f6fd3bdf78f1066c6fb0fb23`  
		Last Modified: Tue, 13 Aug 2024 01:25:44 GMT  
		Size: 54.1 MB (54075217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b49e88f43277ce63fe01761080f821f3b3be9f581e45ed6dbb50b5168642a1`  
		Last Modified: Tue, 13 Aug 2024 01:26:08 GMT  
		Size: 173.1 MB (173060876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854c1c6359c025e4a47dfbac10a25e7961b24a754123354e9bc34bab7f277cd3`  
		Last Modified: Tue, 13 Aug 2024 20:53:28 GMT  
		Size: 263.1 MB (263095258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f3b7b40296ae25b3e80cc721493168b0e9a8b31191a5a589e1fdd64b7b46399e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf30e97755ca96ffe5387849e8ecfcbdf192586a462d01ace8c46d46294ea4bd`

```dockerfile
```

-	Layers:
	-	`sha256:14c9edf50d643bb3a3325e61fe0eca2f0e8449f141b26517a7cfb0ddd62f37be`  
		Last Modified: Tue, 13 Aug 2024 20:53:23 GMT  
		Size: 14.9 MB (14873217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c86f1e8337e8e681287c7507a3b747611ffa4a577e92858bcd2c92dc3271eba`  
		Last Modified: Tue, 13 Aug 2024 20:53:22 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-slim`

```console
$ docker pull rust@sha256:907ff4b3ee7df57149ffee04f606e0a08b9b2ed3507f00a19cf3c9c0f74b7681
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

### `rust:1.80-slim` - linux; amd64

```console
$ docker pull rust@sha256:a5ec1fc7928df7d24504ba8d0e7d9d096513736c5e1b6ac2eac686324a7419a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280194591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d74dd89cb787e264870a35d96127262dd06602fa988a39dfcdcc0b1b87fbe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bf03ed1c368822e027a2732362680f56ce5137e91ba84ce386e51fd189061c`  
		Last Modified: Wed, 04 Sep 2024 23:12:37 GMT  
		Size: 251.1 MB (251068107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim` - unknown; unknown

```console
$ docker pull rust@sha256:70c0f4a4e29a19fbc259b978e407d0198b3ac61100c49416558e718dd524198c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01702ebd45abe4c0861513492e59d285a1ddae1839f8e5329d1860652f8d06f6`

```dockerfile
```

-	Layers:
	-	`sha256:c76a08813897d00f0e0cd93710bc88f5964d3f99c81a2b63b3b37de6b1b76a4b`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 3.9 MB (3945035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8859af7c414d89532ca7d9eaabba0766d80d3479215e254051332407fdcd00e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:cc2333aa663bbc92356ee4ef6f8d6b642b445e5e666fc37b3867b0d5a5a893bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289213250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e848b8369d06b2c98853e0ef79cb6d790e729403484bc5f943edb29e2b9de6c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee65094ca49c2c7edf34dada1ae62118e6659c97a5f195e52d279a877fc800fc`  
		Last Modified: Thu, 05 Sep 2024 12:10:55 GMT  
		Size: 264.5 MB (264494985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim` - unknown; unknown

```console
$ docker pull rust@sha256:f2f6983e05e6ff77da77143b68cc48199d9ab5a09fba06cbee4c136d9e6882dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afc164a0e9d2735af5dcca73cb4960c28e6606be6974bc2c6ce6d2b5ef62f0e`

```dockerfile
```

-	Layers:
	-	`sha256:27bae23be9fa45ed1c009e8d69e579013b3f8c8b8ca757f8f9013ad7d9d27438`  
		Last Modified: Thu, 05 Sep 2024 12:10:49 GMT  
		Size: 3.8 MB (3761492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d87d0772c2929243aa21fe4b3f0ff0ac589b73e19adfed9d306123093fca53ba`  
		Last Modified: Thu, 05 Sep 2024 12:10:48 GMT  
		Size: 13.2 KB (13155 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim` - linux; 386

```console
$ docker pull rust@sha256:bbaff9e88af760191966cb0beadf94d503e1fafcd63b5c5ccaaa03e5598564b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290925711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca74e88b45440ef8d55e5c25ed0f7f2e9dbb4f2a8bafec24e6cccd1107c80d47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f23ccaebd9d56a75909c850e6ab0aa6693c9f89ba57b9977dba601890f2d94`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 260.8 MB (260781417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim` - unknown; unknown

```console
$ docker pull rust@sha256:149c847e4d5940e34735ec36d6b663715f0fa8e9ee11a0282d4f1dd871808c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc742cbf65f608e8de19416358e8901fba122e86286e96175686e134e9ccf789`

```dockerfile
```

-	Layers:
	-	`sha256:b5443a5469154e30b37c7de0b36037a6e20bddc881a424cdccd8843d369dcf48`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 3.9 MB (3926448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513d8a278aa21dcacbe90a3c89ef597af1dff583466d0036a15dcb4031011e06`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:d2d2feff3c61a9801dbe7735d194d197592c10a07446ebb5f58c360d44704e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292910541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7509806f664093ad6ec12f7fb65501f3540a72ac9809b5258a8d9d45ece500`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49174d43929c3e7d189a8935d2a77a8a17ce21f7070c6f983f380f120cdb6ae`  
		Last Modified: Thu, 05 Sep 2024 06:24:07 GMT  
		Size: 259.8 MB (259788183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim` - unknown; unknown

```console
$ docker pull rust@sha256:8ea384b40e2596497636656084514cc2dbfed040b686146c648676e33089efde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d551dc594d848945573fc2616217aee09021e04156415504cb1e6928f3fc4ecc`

```dockerfile
```

-	Layers:
	-	`sha256:af2dbf67be2945aa925798a7e18da8e96c52f624747225bffbdd0072388ec033`  
		Last Modified: Thu, 05 Sep 2024 06:24:01 GMT  
		Size: 3.9 MB (3917197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec30cdde83a25decfe9823cb5f543ce23f66684e6eb8437b988758d6a1d5ae8`  
		Last Modified: Thu, 05 Sep 2024 06:24:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim` - linux; s390x

```console
$ docker pull rust@sha256:5e90e95a277cd1027f1ae3ba58dbdd1931c63ea9df38cb2221b06fe6dcec728f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340720684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8674b49ddd39434ab78416cdec54b901fceb062293e8069f1f0471ce40433e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594be6304f123a21b952480d35d2ed44c27f35cfe89018bf16a599b5022cb653`  
		Last Modified: Thu, 05 Sep 2024 07:11:55 GMT  
		Size: 313.2 MB (313230363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim` - unknown; unknown

```console
$ docker pull rust@sha256:df46a7b656a5378d8e6f0d320f4b2e4e629806b496e187e4aafa54adf82aed84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6739776cf152581ed3a68005323f9befa6f39245508765ad2724fccb84d6524`

```dockerfile
```

-	Layers:
	-	`sha256:574a1afcca67c6ddd0a7e471fdca0a769f0620648631b878ad4399a3be51c698`  
		Last Modified: Thu, 05 Sep 2024 07:11:50 GMT  
		Size: 3.8 MB (3787360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:239faceff7d2873bf0a8f549a7a3bb22ddc18eea16d381f8e5c529f659546778`  
		Last Modified: Thu, 05 Sep 2024 07:11:49 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-slim-bookworm`

```console
$ docker pull rust@sha256:907ff4b3ee7df57149ffee04f606e0a08b9b2ed3507f00a19cf3c9c0f74b7681
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

### `rust:1.80-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:a5ec1fc7928df7d24504ba8d0e7d9d096513736c5e1b6ac2eac686324a7419a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280194591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d74dd89cb787e264870a35d96127262dd06602fa988a39dfcdcc0b1b87fbe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bf03ed1c368822e027a2732362680f56ce5137e91ba84ce386e51fd189061c`  
		Last Modified: Wed, 04 Sep 2024 23:12:37 GMT  
		Size: 251.1 MB (251068107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:70c0f4a4e29a19fbc259b978e407d0198b3ac61100c49416558e718dd524198c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01702ebd45abe4c0861513492e59d285a1ddae1839f8e5329d1860652f8d06f6`

```dockerfile
```

-	Layers:
	-	`sha256:c76a08813897d00f0e0cd93710bc88f5964d3f99c81a2b63b3b37de6b1b76a4b`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 3.9 MB (3945035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8859af7c414d89532ca7d9eaabba0766d80d3479215e254051332407fdcd00e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:cc2333aa663bbc92356ee4ef6f8d6b642b445e5e666fc37b3867b0d5a5a893bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289213250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e848b8369d06b2c98853e0ef79cb6d790e729403484bc5f943edb29e2b9de6c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee65094ca49c2c7edf34dada1ae62118e6659c97a5f195e52d279a877fc800fc`  
		Last Modified: Thu, 05 Sep 2024 12:10:55 GMT  
		Size: 264.5 MB (264494985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f2f6983e05e6ff77da77143b68cc48199d9ab5a09fba06cbee4c136d9e6882dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afc164a0e9d2735af5dcca73cb4960c28e6606be6974bc2c6ce6d2b5ef62f0e`

```dockerfile
```

-	Layers:
	-	`sha256:27bae23be9fa45ed1c009e8d69e579013b3f8c8b8ca757f8f9013ad7d9d27438`  
		Last Modified: Thu, 05 Sep 2024 12:10:49 GMT  
		Size: 3.8 MB (3761492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d87d0772c2929243aa21fe4b3f0ff0ac589b73e19adfed9d306123093fca53ba`  
		Last Modified: Thu, 05 Sep 2024 12:10:48 GMT  
		Size: 13.2 KB (13155 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:bbaff9e88af760191966cb0beadf94d503e1fafcd63b5c5ccaaa03e5598564b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290925711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca74e88b45440ef8d55e5c25ed0f7f2e9dbb4f2a8bafec24e6cccd1107c80d47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f23ccaebd9d56a75909c850e6ab0aa6693c9f89ba57b9977dba601890f2d94`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 260.8 MB (260781417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:149c847e4d5940e34735ec36d6b663715f0fa8e9ee11a0282d4f1dd871808c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc742cbf65f608e8de19416358e8901fba122e86286e96175686e134e9ccf789`

```dockerfile
```

-	Layers:
	-	`sha256:b5443a5469154e30b37c7de0b36037a6e20bddc881a424cdccd8843d369dcf48`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 3.9 MB (3926448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513d8a278aa21dcacbe90a3c89ef597af1dff583466d0036a15dcb4031011e06`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d2d2feff3c61a9801dbe7735d194d197592c10a07446ebb5f58c360d44704e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292910541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7509806f664093ad6ec12f7fb65501f3540a72ac9809b5258a8d9d45ece500`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49174d43929c3e7d189a8935d2a77a8a17ce21f7070c6f983f380f120cdb6ae`  
		Last Modified: Thu, 05 Sep 2024 06:24:07 GMT  
		Size: 259.8 MB (259788183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8ea384b40e2596497636656084514cc2dbfed040b686146c648676e33089efde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d551dc594d848945573fc2616217aee09021e04156415504cb1e6928f3fc4ecc`

```dockerfile
```

-	Layers:
	-	`sha256:af2dbf67be2945aa925798a7e18da8e96c52f624747225bffbdd0072388ec033`  
		Last Modified: Thu, 05 Sep 2024 06:24:01 GMT  
		Size: 3.9 MB (3917197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec30cdde83a25decfe9823cb5f543ce23f66684e6eb8437b988758d6a1d5ae8`  
		Last Modified: Thu, 05 Sep 2024 06:24:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:5e90e95a277cd1027f1ae3ba58dbdd1931c63ea9df38cb2221b06fe6dcec728f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340720684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8674b49ddd39434ab78416cdec54b901fceb062293e8069f1f0471ce40433e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594be6304f123a21b952480d35d2ed44c27f35cfe89018bf16a599b5022cb653`  
		Last Modified: Thu, 05 Sep 2024 07:11:55 GMT  
		Size: 313.2 MB (313230363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:df46a7b656a5378d8e6f0d320f4b2e4e629806b496e187e4aafa54adf82aed84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6739776cf152581ed3a68005323f9befa6f39245508765ad2724fccb84d6524`

```dockerfile
```

-	Layers:
	-	`sha256:574a1afcca67c6ddd0a7e471fdca0a769f0620648631b878ad4399a3be51c698`  
		Last Modified: Thu, 05 Sep 2024 07:11:50 GMT  
		Size: 3.8 MB (3787360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:239faceff7d2873bf0a8f549a7a3bb22ddc18eea16d381f8e5c529f659546778`  
		Last Modified: Thu, 05 Sep 2024 07:11:49 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80-slim-bullseye`

```console
$ docker pull rust@sha256:3bddded5af7155cafc29701e0701bcf3712a407fc7d642423760ec266e5a0682
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

### `rust:1.80-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:11fbefae37d29d4b00e0b566b044cc3a6b872505aef297eb9b155fdacf677a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271859977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8888f7ee42b36e189196bd0c8bcaa7b82dbe62234fd5dece168368ef9f93bc1b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009542abce00716699fc9f02523d81058a5e4a326eae717d2fea8c06f55be526`  
		Last Modified: Wed, 04 Sep 2024 23:12:34 GMT  
		Size: 240.4 MB (240431300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6b2212261e50269ab865ff857cfd68b718e0401726883d6493ee31389b62e67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c6bb2b68bcf2dfda78433017e4d559b0e95616710d78a278a33f9792c49d48`

```dockerfile
```

-	Layers:
	-	`sha256:d9798046ab832947c5ae4ab6c01783c3230b53dad783b0dc2cb0c1f33f4c18fe`  
		Last Modified: Wed, 04 Sep 2024 23:12:28 GMT  
		Size: 4.2 MB (4164313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ed06d2ab6037ccd8879f98a11ef9c5634091df7e2b0df0353a8abc4c0da8632`  
		Last Modified: Wed, 04 Sep 2024 23:12:28 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:10334b6ea7d1540cc93a254d83cd2523a51498acec6550d9c498e8a08d48cc5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285518044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985c6ec0023ef93ca3b509422da444dedbe01e3a9d5be254679b43319cbbf8cd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:c451ece1244c14bce110ffbe6906867ce12f8e88234988b0edba91009a9dbbf8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f572303598915f7fb61cc4b47f7207c9ee64d52b9db5fc03ee133ec2dd679347`  
		Last Modified: Wed, 04 Sep 2024 22:02:25 GMT  
		Size: 26.6 MB (26589615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6ad557e4a293fcec008cedd79106f6ef955c5e24dd1cf657b7e40744cbd440`  
		Last Modified: Thu, 05 Sep 2024 12:09:02 GMT  
		Size: 258.9 MB (258928429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:185308415291c86011485ca6ae5c6c9d24cd0c0455ce31e92cf3c83745b877e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bf9c70231335a286bd907aabb78dd6e765230974619f7450019bae997fdae2`

```dockerfile
```

-	Layers:
	-	`sha256:0ca59ac3c5a0d7f54b0976168e45637127fce7006546c43de9f9cd9f69156945`  
		Last Modified: Thu, 05 Sep 2024 12:08:56 GMT  
		Size: 4.0 MB (3973664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f211237bf8e70aada0e861f20fdf49b04c778600c8657efe317c065eefeb7569`  
		Last Modified: Thu, 05 Sep 2024 12:08:56 GMT  
		Size: 11.9 KB (11936 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea400ae221974016cf01cfc99716046022430cc14de5608db498729f7618f668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.7 MB (335717687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290fe501a9234536387b5b30c99f27e439d23d64536b7815fe2de01d3682d07f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cb6cdc1948b06794974ff2e98a7005fb4728291f972fd9fe6890a51b35589`  
		Last Modified: Tue, 13 Aug 2024 11:45:59 GMT  
		Size: 305.6 MB (305641600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a3676673a581a4a22ae35dba326c5d9ccd2bdbde7ba9cfab0820cb96773f78ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621cc11386fc3351be6a2c44213e137c509b73cbc571f6de7541e04cbe8a4ac1`

```dockerfile
```

-	Layers:
	-	`sha256:25d0ce1b84cd190aa843a54b2f062344d99aacfdeb1f4215da7fc975e859651e`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 4.2 MB (4161095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66c9bde30e15c9a5a38892f97be33009492c2633b0fd4b560fb3907e93ecf62`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 12.2 KB (12175 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:c57675f231e19c0114750c276bb686ec8f0125ca00ee3e1d1b5cbae8aa6e9c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286389854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688be6d01f10da5e726acf8027b050c5d0962197d8e667b43261dd385a0c4f33`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f518608d5d6e978d31e2f8814affa386d3c917837a7823597d8d0c86477c8ee`  
		Last Modified: Thu, 05 Sep 2024 00:29:16 GMT  
		Size: 254.0 MB (253976540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b8f569048c31e591add1ab0d8b9f3f7cdc3272c6072100db265bb675887e53bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b1c275df90e1f83fc7b09b7a4c32c00de4fcc7346e5ccb68c1c4d1125c6a8a`

```dockerfile
```

-	Layers:
	-	`sha256:c70252172c1a37c2fb6ce0894158a216a4c5a6219906aa119f3e9e9ba2a7a3e1`  
		Last Modified: Thu, 05 Sep 2024 00:29:11 GMT  
		Size: 4.2 MB (4156081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e4cc08677260612ec187771e82aba25a4655648cf3a308d21be1aac5637858`  
		Last Modified: Thu, 05 Sep 2024 00:29:11 GMT  
		Size: 11.8 KB (11837 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:3b063eaf3446b0a4b0201201275e496c4cd37e2df97786f5d7dc11872b49b3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281302014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dbc33dcd7620a227caf71dad7ca84f2c231ca26a65558ec553fc37860ad920`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb61bbbd90ca687d8cf9a0fa307847411b891a05ea61c9d5075175311224639a`  
		Last Modified: Thu, 05 Sep 2024 06:21:52 GMT  
		Size: 246.0 MB (246002740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d63496117c7b6330c99ea4b31e3cbc463e1a92f1262350984fe3b84bfb625403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc7ee7587c6a789c8c0cb6838e839d1bc47ef5a05fb52e1a8aecd9ba1309500`

```dockerfile
```

-	Layers:
	-	`sha256:e119f05f2002b1464fc5731d6d2308b0ee4020a17744313cb4811c29106c6988`  
		Last Modified: Thu, 05 Sep 2024 06:21:46 GMT  
		Size: 4.1 MB (4125251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a7aed5f5e3aaffc866e0aea2a3e9c3e60ffd7bd2e2c5f077eae9468fe3db810`  
		Last Modified: Thu, 05 Sep 2024 06:21:45 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80-slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:f454359a3d4de0bd0fb0c063a4b2366299600bdafe2a34fce998a23bd87a25b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.1 MB (335147088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295366e0c73019a39ee770be37d3e862fefdfb2d00b4f7c49596abdad9e970a7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16cb9b3555a4b7e7bf56b97db7af5a62cffeb6ab93ea0db4eb8789c042664f7`  
		Last Modified: Thu, 05 Sep 2024 07:10:02 GMT  
		Size: 305.5 MB (305483641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:12bb9211940c142484034d59efb2b6239d0aac58cdddb50774003ddf6be8b843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6295da41651110039f4ab6f25165e32bb9af3ac5f36ff76349f61c20645b6e6`

```dockerfile
```

-	Layers:
	-	`sha256:a827dd2d48d500c33de79a8d81e812dace7251b737e92fd0238c8aeabbf45f26`  
		Last Modified: Thu, 05 Sep 2024 07:09:57 GMT  
		Size: 4.0 MB (3996088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2044074a697d1c663a041eb3ace815004e270dbc711679b502f0c86f5edbb643`  
		Last Modified: Thu, 05 Sep 2024 07:09:57 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1`

```console
$ docker pull rust@sha256:d22d8938f0403ee31c118b5bf2162b883313dd7f387f859d9f2accd7c884c385
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

### `rust:1.80.1` - linux; amd64

```console
$ docker pull rust@sha256:883df89a3ed53fb0e0f6a67d79cfebf72906d97f9d816379fdf941af969be1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529316453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a14ebf5765b504232d2db40bfcd2a69b22156ada6f3880a2c34f3819fbd115`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ff076d818ad6b8557e03e10c83657cc716ab287c8380054ff91571c8cae81`  
		Last Modified: Wed, 04 Sep 2024 23:02:08 GMT  
		Size: 211.3 MB (211266623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f8a55b70e1cdd0ddc6b738b3a1baeadd53644ee6819ff60426e800045a98b0`  
		Last Modified: Thu, 05 Sep 2024 00:29:41 GMT  
		Size: 180.3 MB (180291957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1` - unknown; unknown

```console
$ docker pull rust@sha256:6ba93cd0c1015d1e433471ab39bd16a063af791c7331e18df530f8e6fe722b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085cfe3bb88e92259308df253ca6817c99f844fa21d86e0c22fe8cf9636007eb`

```dockerfile
```

-	Layers:
	-	`sha256:01b822a94cc2d7c507e8248d8c5d3e6c9bd0ced556d1a385cb8329261573c353`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 15.4 MB (15445058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd49b3074e925710d484fdd75b4d3689f4de021889974dec39020d6925a4719`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1` - linux; arm variant v7

```console
$ docker pull rust@sha256:b6f344496c19f4a91adffeb1c6f3975ed4f0c134965451cc96505002f8a7bd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d72160a77779d619c0691d2d11e9cefcf875d6caba4743817d21439067c8493`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e3c71ceb3b7032e8a78ea70e306ec97b152570eeaae849a0c97bb61b2b12287f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe61db625a1b529903f1126ded0caa9e4e1c247503d524cd43bc15454b6bcc2f`  
		Last Modified: Tue, 13 Aug 2024 01:00:32 GMT  
		Size: 45.1 MB (45148160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06599d70e5763853acd56f8e4938729e068e7942382f335f96ce0ae3bc5a63a`  
		Last Modified: Tue, 13 Aug 2024 01:32:20 GMT  
		Size: 22.0 MB (21954622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3af44a3c0ce16617696528373b53738420f91f3383cda1666cc673cbf6fe50`  
		Last Modified: Tue, 13 Aug 2024 01:32:41 GMT  
		Size: 59.2 MB (59221928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dd2b78206591edf08b24f09f26f742a3d689be108f6e3cf74538c78a14b7d8`  
		Last Modified: Tue, 13 Aug 2024 01:33:16 GMT  
		Size: 175.2 MB (175182857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4fbda85fa1661a9607ed15220d6cd0ba0ea7cfe8f07296134db5ed818046e5`  
		Last Modified: Wed, 14 Aug 2024 00:19:33 GMT  
		Size: 216.6 MB (216645579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1` - unknown; unknown

```console
$ docker pull rust@sha256:1ddf44bae2a2ab49522a19c70acf650db42bb2f6c68e2dfba4087a2465283dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364116a8162d50ac678aca565a1904bfbfc433d01d7bfb4d35fa37480d1ee7d3`

```dockerfile
```

-	Layers:
	-	`sha256:2381d137772c59a7125907148fb80cbd972483f5c489ea3758959c92823577f7`  
		Last Modified: Wed, 14 Aug 2024 00:19:29 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:befe4b689653998a8d04333bd6495dbe1e85862cc244c47d41fe0a25d659ed10`  
		Last Modified: Wed, 14 Aug 2024 00:19:28 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fda6ddc43a715feab22a98e1bcd801537ce6788377cf1d4919e08819a335cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8219a5ff56d4a59051986054024af17d4463ef5e7adcdae8e770fb8af061687f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275677961327bd0cf394699228e29d7caf27f171c627899a20ebc9eeb550e209`  
		Last Modified: Tue, 13 Aug 2024 01:09:34 GMT  
		Size: 64.0 MB (63994880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46e144614e1ae9b82b5d89d16a31a506542733eabceebfac041e0192dfafcf4`  
		Last Modified: Tue, 13 Aug 2024 01:10:06 GMT  
		Size: 202.6 MB (202624176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8a9c35b14d62b7daaefd544a6bbd91b6c1fab2f57de7223cb3c2db641f8f3f`  
		Last Modified: Tue, 13 Aug 2024 19:47:59 GMT  
		Size: 249.9 MB (249924612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1` - unknown; unknown

```console
$ docker pull rust@sha256:94216dd82c491d7e6f65884930be2ef3b32567829f661b973bf6de9670caf8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8403ed68ffd2e12e6bb5977a46b702d64bfe7042a23546abf7e9a207f9a7b82a`

```dockerfile
```

-	Layers:
	-	`sha256:c73483c681ff733971d6bac2c66743acb42444bba080cb661d51c906d243b6de`  
		Last Modified: Tue, 13 Aug 2024 19:47:54 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27ab72a7b07fef9cb15504b90ff201b9db8849760efaab45970b5339508eecf2`  
		Last Modified: Tue, 13 Aug 2024 19:47:53 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1` - linux; 386

```console
$ docker pull rust@sha256:8f7ec0c462a97974a827203da3d48a0e0b650b3134b6ff62d4351bc4d35fd88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544833213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b757d10a8aa83b2245bf2670352842b8001028cf212163001100db5cdde0e97d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0a7648037128b800dbf0363e27e6092c0253e0bd9beeb38a8aa572225934be`  
		Last Modified: Wed, 04 Sep 2024 23:21:06 GMT  
		Size: 210.2 MB (210181614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff91319e9e7fc8f2ebbd39fb7eea49ff32d26c0a80075db4be2000172b1e2c2`  
		Last Modified: Thu, 05 Sep 2024 00:29:34 GMT  
		Size: 193.2 MB (193190646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1` - unknown; unknown

```console
$ docker pull rust@sha256:89423d1df8d449f51c36385120c91be4bda5ca07d565c86391e83b052273eee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15436735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d654f978ebaf05551dd313df3e6572228fc317f1462fbfdb238633e8f72fd6`

```dockerfile
```

-	Layers:
	-	`sha256:ea624d5326397b6cff430e813450f3b7fe48aa493d7c1d50fcd441a09ff02a90`  
		Last Modified: Thu, 05 Sep 2024 00:29:29 GMT  
		Size: 15.4 MB (15423818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb7e5ec2189b610823dc5ef4564f4af35bd76533a4a716c603c9ed8112e1c9f`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1` - linux; ppc64le

```console
$ docker pull rust@sha256:4230383893f246794d2aec426cdeae0c6d6559692181a139b8035d7e0e9d73cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554124880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d39abdea1b0ddb7070a48b89cdc15e163bcde224eca74a0a407a3262dd26a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35476fbf45cb5153abf5ea2df7487a74d0cd0de327ba5e9e970713f9e385650`  
		Last Modified: Tue, 13 Aug 2024 01:35:51 GMT  
		Size: 214.3 MB (214264660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a28f21591d3325119c396461297085c135f02fe0c43f55e5d9d04babfe7f8a`  
		Last Modified: Tue, 13 Aug 2024 21:43:47 GMT  
		Size: 191.0 MB (191025993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1` - unknown; unknown

```console
$ docker pull rust@sha256:fbe15bbd473bc7a23be790e4137162ff70e31cbb32389f146816a3880926436a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a621b08bd27a06288b964fba10a38173fa5365c5ddc7e8a9cccb7618ca77ac`

```dockerfile
```

-	Layers:
	-	`sha256:327622dc45cc14d8fa9bfdeff84b04b9db53727ba825e799d576336b111a738f`  
		Last Modified: Tue, 13 Aug 2024 21:43:41 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a0869e8a6fa0e4af601c1b3715fc98fa182a33f1fb3f0f496d5860b0aee948a`  
		Last Modified: Tue, 13 Aug 2024 21:43:40 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1` - linux; s390x

```console
$ docker pull rust@sha256:7b40e1bbb384a9e7239ae1b346dfdcddcc6425cad2d1117869ccdefaf0de3092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581466000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456a0c8f4b4dc0ce6ef7658d91e2dee89d72fc4c661d9f8cfe429d7bb25f907d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d84b8bb13cbf61ae13e4c378871c52c3e9b521657a5faa02f0159e1be542a05`  
		Last Modified: Tue, 13 Aug 2024 01:25:25 GMT  
		Size: 183.3 MB (183265629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7110931c79b785aa170a85a350cfeaf7e6a2f5422afbf81362184df95653f728`  
		Last Modified: Tue, 13 Aug 2024 20:55:34 GMT  
		Size: 263.1 MB (263095149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1` - unknown; unknown

```console
$ docker pull rust@sha256:4117efcb78d41d704ce0a167cacf739449fda5091e7871c7e274690dc616d093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971437f70ca6e9f6a749c7db65a07092f93076ec42375222e3ddc55b9a04a1a2`

```dockerfile
```

-	Layers:
	-	`sha256:9b04722e355f910725ee8dfca9c787edafbb9ce2d45729798f8e0e75d9f2f969`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2abf42730b95caa5d1a2d651db714bd4b84a8497980620b6f55cc3b01090eff8`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-alpine`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.80.1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-alpine3.19`

```console
$ docker pull rust@sha256:b3ac1f65cf33390407c9b90558eb41e7a8311c47d836fca5800960f1aa2d11d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.80.1-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:25c79c9854cd4bedc797a88e2d4dc1b4502d22a540867fa66257e6e03c4c1d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279155377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204c24ee400cc1a13c13b275cb04657bc5e47150ce5a4e77d3a7671021b9a32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061bdf3a42c6c4489e9e78047cdaa3af6f7b63e5d255e0ab9e6660d180836f4`  
		Last Modified: Thu, 08 Aug 2024 20:02:39 GMT  
		Size: 55.3 MB (55346819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acee9c63bebda8ae8f027b6e99deee99e570d38430b1f5de3f271f853c530cc`  
		Last Modified: Thu, 08 Aug 2024 20:02:41 GMT  
		Size: 220.4 MB (220389518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:d7f847716cae21dc55ac84add1dab418798ef33b8624854fb6b8c65f17169302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b861f59014e11471235b45ca58fe55e1bce20e2d3235649938ddd8e10ac83b`

```dockerfile
```

-	Layers:
	-	`sha256:cda40d4b828cdfea673ac423a0571622627c241817509f9ba745a38be1560b4f`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e221181fdb20703a089d816b169375986ae47adf4002808cc72821fdf9b9e942`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1c9472feed43f2708eaa2821cf5f0a646160cee7be9d584bf730e755eedbee94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286589138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040de42a611e54d884e5a00d1765df3de096fba714c4defafc0750e79bcb340e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1b276de5f8a8a2fd3e6b931c4e180f78458c812dda2346f21361c13108618d`  
		Last Modified: Fri, 26 Jul 2024 00:29:37 GMT  
		Size: 53.0 MB (52995484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2abe5cb54c2cfbfce48a309498337e7a126ab4ea86b6df2ef36f1613354c5c4`  
		Last Modified: Thu, 08 Aug 2024 20:22:15 GMT  
		Size: 230.2 MB (230235196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:c808914252afc74e4ba729fb24e0bb95b91c9a2f8608b2a35bd39fc92b7d5a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27a7713ca3e5389a8f63774d2f2029f10a884a7ef5258c5a110ac3cc5fa9642`

```dockerfile
```

-	Layers:
	-	`sha256:dab1ad55931d3701c8a9c82cd1652b524d00f22c57bd6fc291789059b83165e3`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a90f930d575ecabd7599845ca4411c5bf521f8695acca03fbc6142619add3f7`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-alpine3.20`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.80.1-alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-bookworm`

```console
$ docker pull rust@sha256:d22d8938f0403ee31c118b5bf2162b883313dd7f387f859d9f2accd7c884c385
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

### `rust:1.80.1-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:883df89a3ed53fb0e0f6a67d79cfebf72906d97f9d816379fdf941af969be1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529316453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a14ebf5765b504232d2db40bfcd2a69b22156ada6f3880a2c34f3819fbd115`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ff076d818ad6b8557e03e10c83657cc716ab287c8380054ff91571c8cae81`  
		Last Modified: Wed, 04 Sep 2024 23:02:08 GMT  
		Size: 211.3 MB (211266623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f8a55b70e1cdd0ddc6b738b3a1baeadd53644ee6819ff60426e800045a98b0`  
		Last Modified: Thu, 05 Sep 2024 00:29:41 GMT  
		Size: 180.3 MB (180291957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:6ba93cd0c1015d1e433471ab39bd16a063af791c7331e18df530f8e6fe722b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085cfe3bb88e92259308df253ca6817c99f844fa21d86e0c22fe8cf9636007eb`

```dockerfile
```

-	Layers:
	-	`sha256:01b822a94cc2d7c507e8248d8c5d3e6c9bd0ced556d1a385cb8329261573c353`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 15.4 MB (15445058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd49b3074e925710d484fdd75b4d3689f4de021889974dec39020d6925a4719`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:b6f344496c19f4a91adffeb1c6f3975ed4f0c134965451cc96505002f8a7bd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d72160a77779d619c0691d2d11e9cefcf875d6caba4743817d21439067c8493`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e3c71ceb3b7032e8a78ea70e306ec97b152570eeaae849a0c97bb61b2b12287f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe61db625a1b529903f1126ded0caa9e4e1c247503d524cd43bc15454b6bcc2f`  
		Last Modified: Tue, 13 Aug 2024 01:00:32 GMT  
		Size: 45.1 MB (45148160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06599d70e5763853acd56f8e4938729e068e7942382f335f96ce0ae3bc5a63a`  
		Last Modified: Tue, 13 Aug 2024 01:32:20 GMT  
		Size: 22.0 MB (21954622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3af44a3c0ce16617696528373b53738420f91f3383cda1666cc673cbf6fe50`  
		Last Modified: Tue, 13 Aug 2024 01:32:41 GMT  
		Size: 59.2 MB (59221928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dd2b78206591edf08b24f09f26f742a3d689be108f6e3cf74538c78a14b7d8`  
		Last Modified: Tue, 13 Aug 2024 01:33:16 GMT  
		Size: 175.2 MB (175182857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4fbda85fa1661a9607ed15220d6cd0ba0ea7cfe8f07296134db5ed818046e5`  
		Last Modified: Wed, 14 Aug 2024 00:19:33 GMT  
		Size: 216.6 MB (216645579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1ddf44bae2a2ab49522a19c70acf650db42bb2f6c68e2dfba4087a2465283dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364116a8162d50ac678aca565a1904bfbfc433d01d7bfb4d35fa37480d1ee7d3`

```dockerfile
```

-	Layers:
	-	`sha256:2381d137772c59a7125907148fb80cbd972483f5c489ea3758959c92823577f7`  
		Last Modified: Wed, 14 Aug 2024 00:19:29 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:befe4b689653998a8d04333bd6495dbe1e85862cc244c47d41fe0a25d659ed10`  
		Last Modified: Wed, 14 Aug 2024 00:19:28 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fda6ddc43a715feab22a98e1bcd801537ce6788377cf1d4919e08819a335cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8219a5ff56d4a59051986054024af17d4463ef5e7adcdae8e770fb8af061687f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275677961327bd0cf394699228e29d7caf27f171c627899a20ebc9eeb550e209`  
		Last Modified: Tue, 13 Aug 2024 01:09:34 GMT  
		Size: 64.0 MB (63994880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46e144614e1ae9b82b5d89d16a31a506542733eabceebfac041e0192dfafcf4`  
		Last Modified: Tue, 13 Aug 2024 01:10:06 GMT  
		Size: 202.6 MB (202624176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8a9c35b14d62b7daaefd544a6bbd91b6c1fab2f57de7223cb3c2db641f8f3f`  
		Last Modified: Tue, 13 Aug 2024 19:47:59 GMT  
		Size: 249.9 MB (249924612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:94216dd82c491d7e6f65884930be2ef3b32567829f661b973bf6de9670caf8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8403ed68ffd2e12e6bb5977a46b702d64bfe7042a23546abf7e9a207f9a7b82a`

```dockerfile
```

-	Layers:
	-	`sha256:c73483c681ff733971d6bac2c66743acb42444bba080cb661d51c906d243b6de`  
		Last Modified: Tue, 13 Aug 2024 19:47:54 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27ab72a7b07fef9cb15504b90ff201b9db8849760efaab45970b5339508eecf2`  
		Last Modified: Tue, 13 Aug 2024 19:47:53 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:8f7ec0c462a97974a827203da3d48a0e0b650b3134b6ff62d4351bc4d35fd88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544833213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b757d10a8aa83b2245bf2670352842b8001028cf212163001100db5cdde0e97d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0a7648037128b800dbf0363e27e6092c0253e0bd9beeb38a8aa572225934be`  
		Last Modified: Wed, 04 Sep 2024 23:21:06 GMT  
		Size: 210.2 MB (210181614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff91319e9e7fc8f2ebbd39fb7eea49ff32d26c0a80075db4be2000172b1e2c2`  
		Last Modified: Thu, 05 Sep 2024 00:29:34 GMT  
		Size: 193.2 MB (193190646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:89423d1df8d449f51c36385120c91be4bda5ca07d565c86391e83b052273eee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15436735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d654f978ebaf05551dd313df3e6572228fc317f1462fbfdb238633e8f72fd6`

```dockerfile
```

-	Layers:
	-	`sha256:ea624d5326397b6cff430e813450f3b7fe48aa493d7c1d50fcd441a09ff02a90`  
		Last Modified: Thu, 05 Sep 2024 00:29:29 GMT  
		Size: 15.4 MB (15423818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb7e5ec2189b610823dc5ef4564f4af35bd76533a4a716c603c9ed8112e1c9f`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:4230383893f246794d2aec426cdeae0c6d6559692181a139b8035d7e0e9d73cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554124880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d39abdea1b0ddb7070a48b89cdc15e163bcde224eca74a0a407a3262dd26a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35476fbf45cb5153abf5ea2df7487a74d0cd0de327ba5e9e970713f9e385650`  
		Last Modified: Tue, 13 Aug 2024 01:35:51 GMT  
		Size: 214.3 MB (214264660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a28f21591d3325119c396461297085c135f02fe0c43f55e5d9d04babfe7f8a`  
		Last Modified: Tue, 13 Aug 2024 21:43:47 GMT  
		Size: 191.0 MB (191025993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:fbe15bbd473bc7a23be790e4137162ff70e31cbb32389f146816a3880926436a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a621b08bd27a06288b964fba10a38173fa5365c5ddc7e8a9cccb7618ca77ac`

```dockerfile
```

-	Layers:
	-	`sha256:327622dc45cc14d8fa9bfdeff84b04b9db53727ba825e799d576336b111a738f`  
		Last Modified: Tue, 13 Aug 2024 21:43:41 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a0869e8a6fa0e4af601c1b3715fc98fa182a33f1fb3f0f496d5860b0aee948a`  
		Last Modified: Tue, 13 Aug 2024 21:43:40 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:7b40e1bbb384a9e7239ae1b346dfdcddcc6425cad2d1117869ccdefaf0de3092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581466000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456a0c8f4b4dc0ce6ef7658d91e2dee89d72fc4c661d9f8cfe429d7bb25f907d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d84b8bb13cbf61ae13e4c378871c52c3e9b521657a5faa02f0159e1be542a05`  
		Last Modified: Tue, 13 Aug 2024 01:25:25 GMT  
		Size: 183.3 MB (183265629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7110931c79b785aa170a85a350cfeaf7e6a2f5422afbf81362184df95653f728`  
		Last Modified: Tue, 13 Aug 2024 20:55:34 GMT  
		Size: 263.1 MB (263095149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4117efcb78d41d704ce0a167cacf739449fda5091e7871c7e274690dc616d093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971437f70ca6e9f6a749c7db65a07092f93076ec42375222e3ddc55b9a04a1a2`

```dockerfile
```

-	Layers:
	-	`sha256:9b04722e355f910725ee8dfca9c787edafbb9ce2d45729798f8e0e75d9f2f969`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2abf42730b95caa5d1a2d651db714bd4b84a8497980620b6f55cc3b01090eff8`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-bullseye`

```console
$ docker pull rust@sha256:f6f599d3f027a97fb60cb87854199fcde390e25cee216712c3f9eede545b052e
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

### `rust:1.80.1-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:cd0a8eb7afeec51e842d834ddf4b153b583427c04da5ac5ef222046604f2318d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.9 MB (502931767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884e2fd2885bf130e08c231e991c8955ce71fb9d987128c310adc962761785db`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d691dff6d17d00b0cbbc4772eb805d97e02504d89ea3e5857cb97c943b74462`  
		Last Modified: Wed, 04 Sep 2024 23:02:33 GMT  
		Size: 54.7 MB (54726023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cfd30604666dfdd92bea930c06ee58dc927e0da651b862491af1648a4aca73`  
		Last Modified: Wed, 04 Sep 2024 23:03:03 GMT  
		Size: 197.1 MB (197067753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed0b0ded1b8b5f8453e7635369b38f8b2c318d0f51e26f0ad4269979ea9ba32`  
		Last Modified: Thu, 05 Sep 2024 00:29:16 GMT  
		Size: 180.3 MB (180292264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f2a08571ef0de6347d1fa328909f711aa08ca828ae893b1b9ec79d43dce4c54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15064067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd481bb1b4a6912e1c25b6c10d942ed60669c539876c401676bfb21ce5ba1b38`

```dockerfile
```

-	Layers:
	-	`sha256:62bbe7371ce9ed40e4bd78dc1e1895a7a86b51139e8a6c0ba845bb8a9e7c01d2`  
		Last Modified: Thu, 05 Sep 2024 00:29:12 GMT  
		Size: 15.1 MB (15052263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8510778438d2ad2268e7ca558d841d6f5554bde8515952028f0afb9fc9af50b5`  
		Last Modified: Thu, 05 Sep 2024 00:29:10 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:b9e1bff441726839efdfa70625797c71d12ed393eff196835675985011379a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.6 MB (499629389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232ed045be751771b4dd1a9891b4b8771355c7d382c7eacb30508c0719434f31`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:7674761630f1c6dfdf95da576bd19dbfe7bc4d942d11d31eff2012ec8b2c7ff1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a986643b6b9d356e3c44ee35fdd352a1064e1fb2a1524c0627e84ba34207b8e2`  
		Last Modified: Tue, 13 Aug 2024 01:01:15 GMT  
		Size: 50.2 MB (50242333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8868560f8e978ee832f67027b7330376be350ffacd30a199b730c72d9550757`  
		Last Modified: Tue, 13 Aug 2024 01:33:28 GMT  
		Size: 14.9 MB (14879497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7deb3ed53b620f0871f5051050fe0d850fd52da94803425820e75bb7b8d4e2e`  
		Last Modified: Tue, 13 Aug 2024 01:33:45 GMT  
		Size: 50.4 MB (50357748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e6955cecd9dc8a3cc8022dd624334d4f3abc81e5801bb1a1d3ddcedd0ef645`  
		Last Modified: Tue, 13 Aug 2024 01:34:17 GMT  
		Size: 167.5 MB (167504270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d727c90103f0458fc4e1233059a99a4449a5658b19c4c04577e90716624ce68`  
		Last Modified: Wed, 14 Aug 2024 00:15:35 GMT  
		Size: 216.6 MB (216645541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:791c2d9db3d160e7e2a93c07568a9ba817c8588b5b3cdd31d37d029feff257b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14865179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc5a22e7dce30f830f957bd7ca405686def79f80919b6f3216dc62e91b57d20`

```dockerfile
```

-	Layers:
	-	`sha256:ea5f09999dd237783aaffbaf7252ec89e60410eefce29c463657d21103fad00c`  
		Last Modified: Wed, 14 Aug 2024 00:15:31 GMT  
		Size: 14.9 MB (14853305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2c6135a6881efe9cfaee1c1973570d4094d9c8efd4330011c071c0287552ad3`  
		Last Modified: Wed, 14 Aug 2024 00:15:30 GMT  
		Size: 11.9 KB (11874 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1dc2b70be87ca21e1298d3966b4821a1f2af9ca4aeb9030f2843156acaabc871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564070284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac07cd629c9ba7cac0f43633a49d02c086f7d0a89d75cdbe31f5443ad59d12d3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3db3ee6245513b1422983db21d89f4f743f300e726af9eff6c9f7e2dddcb67`  
		Last Modified: Tue, 13 Aug 2024 01:10:18 GMT  
		Size: 15.7 MB (15749505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5265d6983e8ed11fd8dc48e17209d3479015214ac92f89f4ac51b2e65060840`  
		Last Modified: Tue, 13 Aug 2024 01:10:33 GMT  
		Size: 54.7 MB (54694302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6073a281eb20b3b43e3cc472efa9f868c8f75fc13cae51a5b10fbe8054bc0ba0`  
		Last Modified: Tue, 13 Aug 2024 01:11:01 GMT  
		Size: 190.0 MB (189971927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15778b247abba33689070973283c965347f8ff7110aed80aba5d5dba886c8645`  
		Last Modified: Tue, 13 Aug 2024 19:46:34 GMT  
		Size: 249.9 MB (249924629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:050d7ffca1af96c20c5a95e9bee8bcd60d8c633ad6a598ed9807cf27439bb339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15066748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc0ceb3fdbd1db1a0bd675c616fcf05e981968d3be62ab462b147b4db354be2`

```dockerfile
```

-	Layers:
	-	`sha256:f3db632e0133fc65815084a91d7a97b2ef1b92d6c4127dc1e3a5b0852c77df14`  
		Last Modified: Tue, 13 Aug 2024 19:46:25 GMT  
		Size: 15.1 MB (15054632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:244e55ed7bcf50ecd68fa3c5e2277c974b6fe67c02fafbffdea96539a80b40d8`  
		Last Modified: Tue, 13 Aug 2024 19:46:24 GMT  
		Size: 12.1 KB (12116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:0b422e50d57c5086836b9b8dca05019ed63192ac2333521c92bc739dbb756427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.5 MB (521530165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfe8c5eaa38c914901128e3ea98bc83c9a639434eaf17b029b52761c8f6ec1c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4533261556c046eefdf517bc6e06bc455b876caf2226aa504a13b5d66d250281`  
		Last Modified: Wed, 04 Sep 2024 23:21:18 GMT  
		Size: 16.3 MB (16268301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341d50e4bbed9704aae2147f28b4a07fc71b73539d282c37f60e183d38865daf`  
		Last Modified: Wed, 04 Sep 2024 23:21:37 GMT  
		Size: 56.0 MB (56030074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d04d357b859cf9b5eb038042f7df289289aee35371021b6ba1005ff2818f428`  
		Last Modified: Wed, 04 Sep 2024 23:22:18 GMT  
		Size: 200.0 MB (199965007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a20660c7aef3eb352454fc403634b2bcff1e7bdf3d17279cd89af22056aa8d`  
		Last Modified: Thu, 05 Sep 2024 00:29:13 GMT  
		Size: 193.2 MB (193190616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0d0978b42325c7b639503fb6f81b435992e69cbb7cfaf3e43d43c7b73fb50a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57f256b77b0a5a96e6a8ec76adfeb153cb387874a4c211a0315b1113bbf662f`

```dockerfile
```

-	Layers:
	-	`sha256:5bfb69f09b1dfbfac72a0286789043735bcd7e8a317c1ff5fdbcdb83d28c4cb9`  
		Last Modified: Thu, 05 Sep 2024 00:29:09 GMT  
		Size: 15.0 MB (15040800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab48a51d9f27782d97a1e808bbe2f638eb8b4a0edc389264cd649bfe7be2808`  
		Last Modified: Thu, 05 Sep 2024 00:29:08 GMT  
		Size: 11.8 KB (11775 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:4b102819b654a311a824ae3a605e6503b76070cd4c4dfc6c227ff67f300c9a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.0 MB (522017613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3b534b39a25e918707b482ef622be1a3c9c8a8fa0889209dc5e17728198e1b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:25dc93c8090a0afba4b41321f81883857bfdd6b30ea9f278833c5a5d9d16ad52 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:dad1c3eca3bf4b2a67cef1dbad507d7a913df7bbe1e3f88044230dd291ada39d`  
		Last Modified: Tue, 13 Aug 2024 00:26:46 GMT  
		Size: 59.0 MB (58954654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b50eef4accfc66462c4cf81c03bb57857b5f3ac891da5b87bfdf1ba826c9677`  
		Last Modified: Tue, 13 Aug 2024 01:36:03 GMT  
		Size: 16.8 MB (16765928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df0e65d951ce5d0b07cbb65477bbb01cfa607241b5c5855f4fb361bedfd1247`  
		Last Modified: Tue, 13 Aug 2024 01:36:21 GMT  
		Size: 58.9 MB (58872586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9438dc035d6f851416f6745a25baa330ca04b6013564731b2c42ddce3979a2ff`  
		Last Modified: Tue, 13 Aug 2024 01:36:57 GMT  
		Size: 196.4 MB (196398494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2565e4d615d926780548ef217b5b10b6f6720e401eba39fa2e54c34ac84bf`  
		Last Modified: Tue, 13 Aug 2024 21:41:58 GMT  
		Size: 191.0 MB (191025951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1447a0430183c6f9369fac6336bfeb4153f534eca6028b5b7f2a14f47a2eea7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15031565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4180a14646f843e73bc293d0bcf988986daa9a36f1818b643d0cbf4f72e8750b`

```dockerfile
```

-	Layers:
	-	`sha256:2e9e4840d282072216185364f3c9012dc3dd727785c3f7bcabcfba3f85cea47b`  
		Last Modified: Tue, 13 Aug 2024 21:41:47 GMT  
		Size: 15.0 MB (15019723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96395652f5022ec8fee2d3878beed560d61f66c18c72f6d1208e66097a7b25d6`  
		Last Modified: Tue, 13 Aug 2024 21:41:45 GMT  
		Size: 11.8 KB (11842 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:3944244146d900e21947895f40f80b74185b5ec24475ac7026203cf5835798ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 MB (559197374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3320425c6a524ca810ff5aa40074b451cbfd12bd85905918328c6f2c509542ea`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c695efccb58000e04eb154deca02ce22ea52fd05ee4246281c66bb7a42d20a96`  
		Last Modified: Tue, 13 Aug 2024 01:25:32 GMT  
		Size: 15.6 MB (15641934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3f87ffa253b4cb357637ad56494facf5bf533f6fd3bdf78f1066c6fb0fb23`  
		Last Modified: Tue, 13 Aug 2024 01:25:44 GMT  
		Size: 54.1 MB (54075217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b49e88f43277ce63fe01761080f821f3b3be9f581e45ed6dbb50b5168642a1`  
		Last Modified: Tue, 13 Aug 2024 01:26:08 GMT  
		Size: 173.1 MB (173060876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854c1c6359c025e4a47dfbac10a25e7961b24a754123354e9bc34bab7f277cd3`  
		Last Modified: Tue, 13 Aug 2024 20:53:28 GMT  
		Size: 263.1 MB (263095258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f3b7b40296ae25b3e80cc721493168b0e9a8b31191a5a589e1fdd64b7b46399e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf30e97755ca96ffe5387849e8ecfcbdf192586a462d01ace8c46d46294ea4bd`

```dockerfile
```

-	Layers:
	-	`sha256:14c9edf50d643bb3a3325e61fe0eca2f0e8449f141b26517a7cfb0ddd62f37be`  
		Last Modified: Tue, 13 Aug 2024 20:53:23 GMT  
		Size: 14.9 MB (14873217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c86f1e8337e8e681287c7507a3b747611ffa4a577e92858bcd2c92dc3271eba`  
		Last Modified: Tue, 13 Aug 2024 20:53:22 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-slim`

```console
$ docker pull rust@sha256:907ff4b3ee7df57149ffee04f606e0a08b9b2ed3507f00a19cf3c9c0f74b7681
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

### `rust:1.80.1-slim` - linux; amd64

```console
$ docker pull rust@sha256:a5ec1fc7928df7d24504ba8d0e7d9d096513736c5e1b6ac2eac686324a7419a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280194591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d74dd89cb787e264870a35d96127262dd06602fa988a39dfcdcc0b1b87fbe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bf03ed1c368822e027a2732362680f56ce5137e91ba84ce386e51fd189061c`  
		Last Modified: Wed, 04 Sep 2024 23:12:37 GMT  
		Size: 251.1 MB (251068107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:70c0f4a4e29a19fbc259b978e407d0198b3ac61100c49416558e718dd524198c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01702ebd45abe4c0861513492e59d285a1ddae1839f8e5329d1860652f8d06f6`

```dockerfile
```

-	Layers:
	-	`sha256:c76a08813897d00f0e0cd93710bc88f5964d3f99c81a2b63b3b37de6b1b76a4b`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 3.9 MB (3945035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8859af7c414d89532ca7d9eaabba0766d80d3479215e254051332407fdcd00e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:cc2333aa663bbc92356ee4ef6f8d6b642b445e5e666fc37b3867b0d5a5a893bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289213250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e848b8369d06b2c98853e0ef79cb6d790e729403484bc5f943edb29e2b9de6c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee65094ca49c2c7edf34dada1ae62118e6659c97a5f195e52d279a877fc800fc`  
		Last Modified: Thu, 05 Sep 2024 12:10:55 GMT  
		Size: 264.5 MB (264494985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:f2f6983e05e6ff77da77143b68cc48199d9ab5a09fba06cbee4c136d9e6882dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afc164a0e9d2735af5dcca73cb4960c28e6606be6974bc2c6ce6d2b5ef62f0e`

```dockerfile
```

-	Layers:
	-	`sha256:27bae23be9fa45ed1c009e8d69e579013b3f8c8b8ca757f8f9013ad7d9d27438`  
		Last Modified: Thu, 05 Sep 2024 12:10:49 GMT  
		Size: 3.8 MB (3761492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d87d0772c2929243aa21fe4b3f0ff0ac589b73e19adfed9d306123093fca53ba`  
		Last Modified: Thu, 05 Sep 2024 12:10:48 GMT  
		Size: 13.2 KB (13155 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim` - linux; 386

```console
$ docker pull rust@sha256:bbaff9e88af760191966cb0beadf94d503e1fafcd63b5c5ccaaa03e5598564b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290925711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca74e88b45440ef8d55e5c25ed0f7f2e9dbb4f2a8bafec24e6cccd1107c80d47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f23ccaebd9d56a75909c850e6ab0aa6693c9f89ba57b9977dba601890f2d94`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 260.8 MB (260781417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:149c847e4d5940e34735ec36d6b663715f0fa8e9ee11a0282d4f1dd871808c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc742cbf65f608e8de19416358e8901fba122e86286e96175686e134e9ccf789`

```dockerfile
```

-	Layers:
	-	`sha256:b5443a5469154e30b37c7de0b36037a6e20bddc881a424cdccd8843d369dcf48`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 3.9 MB (3926448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513d8a278aa21dcacbe90a3c89ef597af1dff583466d0036a15dcb4031011e06`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:d2d2feff3c61a9801dbe7735d194d197592c10a07446ebb5f58c360d44704e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292910541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7509806f664093ad6ec12f7fb65501f3540a72ac9809b5258a8d9d45ece500`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49174d43929c3e7d189a8935d2a77a8a17ce21f7070c6f983f380f120cdb6ae`  
		Last Modified: Thu, 05 Sep 2024 06:24:07 GMT  
		Size: 259.8 MB (259788183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:8ea384b40e2596497636656084514cc2dbfed040b686146c648676e33089efde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d551dc594d848945573fc2616217aee09021e04156415504cb1e6928f3fc4ecc`

```dockerfile
```

-	Layers:
	-	`sha256:af2dbf67be2945aa925798a7e18da8e96c52f624747225bffbdd0072388ec033`  
		Last Modified: Thu, 05 Sep 2024 06:24:01 GMT  
		Size: 3.9 MB (3917197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec30cdde83a25decfe9823cb5f543ce23f66684e6eb8437b988758d6a1d5ae8`  
		Last Modified: Thu, 05 Sep 2024 06:24:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim` - linux; s390x

```console
$ docker pull rust@sha256:5e90e95a277cd1027f1ae3ba58dbdd1931c63ea9df38cb2221b06fe6dcec728f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340720684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8674b49ddd39434ab78416cdec54b901fceb062293e8069f1f0471ce40433e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594be6304f123a21b952480d35d2ed44c27f35cfe89018bf16a599b5022cb653`  
		Last Modified: Thu, 05 Sep 2024 07:11:55 GMT  
		Size: 313.2 MB (313230363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:df46a7b656a5378d8e6f0d320f4b2e4e629806b496e187e4aafa54adf82aed84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6739776cf152581ed3a68005323f9befa6f39245508765ad2724fccb84d6524`

```dockerfile
```

-	Layers:
	-	`sha256:574a1afcca67c6ddd0a7e471fdca0a769f0620648631b878ad4399a3be51c698`  
		Last Modified: Thu, 05 Sep 2024 07:11:50 GMT  
		Size: 3.8 MB (3787360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:239faceff7d2873bf0a8f549a7a3bb22ddc18eea16d381f8e5c529f659546778`  
		Last Modified: Thu, 05 Sep 2024 07:11:49 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-slim-bookworm`

```console
$ docker pull rust@sha256:907ff4b3ee7df57149ffee04f606e0a08b9b2ed3507f00a19cf3c9c0f74b7681
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

### `rust:1.80.1-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:a5ec1fc7928df7d24504ba8d0e7d9d096513736c5e1b6ac2eac686324a7419a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280194591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d74dd89cb787e264870a35d96127262dd06602fa988a39dfcdcc0b1b87fbe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bf03ed1c368822e027a2732362680f56ce5137e91ba84ce386e51fd189061c`  
		Last Modified: Wed, 04 Sep 2024 23:12:37 GMT  
		Size: 251.1 MB (251068107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:70c0f4a4e29a19fbc259b978e407d0198b3ac61100c49416558e718dd524198c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01702ebd45abe4c0861513492e59d285a1ddae1839f8e5329d1860652f8d06f6`

```dockerfile
```

-	Layers:
	-	`sha256:c76a08813897d00f0e0cd93710bc88f5964d3f99c81a2b63b3b37de6b1b76a4b`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 3.9 MB (3945035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8859af7c414d89532ca7d9eaabba0766d80d3479215e254051332407fdcd00e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:cc2333aa663bbc92356ee4ef6f8d6b642b445e5e666fc37b3867b0d5a5a893bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289213250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e848b8369d06b2c98853e0ef79cb6d790e729403484bc5f943edb29e2b9de6c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee65094ca49c2c7edf34dada1ae62118e6659c97a5f195e52d279a877fc800fc`  
		Last Modified: Thu, 05 Sep 2024 12:10:55 GMT  
		Size: 264.5 MB (264494985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f2f6983e05e6ff77da77143b68cc48199d9ab5a09fba06cbee4c136d9e6882dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afc164a0e9d2735af5dcca73cb4960c28e6606be6974bc2c6ce6d2b5ef62f0e`

```dockerfile
```

-	Layers:
	-	`sha256:27bae23be9fa45ed1c009e8d69e579013b3f8c8b8ca757f8f9013ad7d9d27438`  
		Last Modified: Thu, 05 Sep 2024 12:10:49 GMT  
		Size: 3.8 MB (3761492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d87d0772c2929243aa21fe4b3f0ff0ac589b73e19adfed9d306123093fca53ba`  
		Last Modified: Thu, 05 Sep 2024 12:10:48 GMT  
		Size: 13.2 KB (13155 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:bbaff9e88af760191966cb0beadf94d503e1fafcd63b5c5ccaaa03e5598564b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290925711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca74e88b45440ef8d55e5c25ed0f7f2e9dbb4f2a8bafec24e6cccd1107c80d47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f23ccaebd9d56a75909c850e6ab0aa6693c9f89ba57b9977dba601890f2d94`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 260.8 MB (260781417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:149c847e4d5940e34735ec36d6b663715f0fa8e9ee11a0282d4f1dd871808c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc742cbf65f608e8de19416358e8901fba122e86286e96175686e134e9ccf789`

```dockerfile
```

-	Layers:
	-	`sha256:b5443a5469154e30b37c7de0b36037a6e20bddc881a424cdccd8843d369dcf48`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 3.9 MB (3926448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513d8a278aa21dcacbe90a3c89ef597af1dff583466d0036a15dcb4031011e06`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d2d2feff3c61a9801dbe7735d194d197592c10a07446ebb5f58c360d44704e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292910541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7509806f664093ad6ec12f7fb65501f3540a72ac9809b5258a8d9d45ece500`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49174d43929c3e7d189a8935d2a77a8a17ce21f7070c6f983f380f120cdb6ae`  
		Last Modified: Thu, 05 Sep 2024 06:24:07 GMT  
		Size: 259.8 MB (259788183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8ea384b40e2596497636656084514cc2dbfed040b686146c648676e33089efde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d551dc594d848945573fc2616217aee09021e04156415504cb1e6928f3fc4ecc`

```dockerfile
```

-	Layers:
	-	`sha256:af2dbf67be2945aa925798a7e18da8e96c52f624747225bffbdd0072388ec033`  
		Last Modified: Thu, 05 Sep 2024 06:24:01 GMT  
		Size: 3.9 MB (3917197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec30cdde83a25decfe9823cb5f543ce23f66684e6eb8437b988758d6a1d5ae8`  
		Last Modified: Thu, 05 Sep 2024 06:24:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:5e90e95a277cd1027f1ae3ba58dbdd1931c63ea9df38cb2221b06fe6dcec728f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340720684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8674b49ddd39434ab78416cdec54b901fceb062293e8069f1f0471ce40433e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594be6304f123a21b952480d35d2ed44c27f35cfe89018bf16a599b5022cb653`  
		Last Modified: Thu, 05 Sep 2024 07:11:55 GMT  
		Size: 313.2 MB (313230363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:df46a7b656a5378d8e6f0d320f4b2e4e629806b496e187e4aafa54adf82aed84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6739776cf152581ed3a68005323f9befa6f39245508765ad2724fccb84d6524`

```dockerfile
```

-	Layers:
	-	`sha256:574a1afcca67c6ddd0a7e471fdca0a769f0620648631b878ad4399a3be51c698`  
		Last Modified: Thu, 05 Sep 2024 07:11:50 GMT  
		Size: 3.8 MB (3787360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:239faceff7d2873bf0a8f549a7a3bb22ddc18eea16d381f8e5c529f659546778`  
		Last Modified: Thu, 05 Sep 2024 07:11:49 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.80.1-slim-bullseye`

```console
$ docker pull rust@sha256:3bddded5af7155cafc29701e0701bcf3712a407fc7d642423760ec266e5a0682
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

### `rust:1.80.1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:11fbefae37d29d4b00e0b566b044cc3a6b872505aef297eb9b155fdacf677a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271859977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8888f7ee42b36e189196bd0c8bcaa7b82dbe62234fd5dece168368ef9f93bc1b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009542abce00716699fc9f02523d81058a5e4a326eae717d2fea8c06f55be526`  
		Last Modified: Wed, 04 Sep 2024 23:12:34 GMT  
		Size: 240.4 MB (240431300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6b2212261e50269ab865ff857cfd68b718e0401726883d6493ee31389b62e67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c6bb2b68bcf2dfda78433017e4d559b0e95616710d78a278a33f9792c49d48`

```dockerfile
```

-	Layers:
	-	`sha256:d9798046ab832947c5ae4ab6c01783c3230b53dad783b0dc2cb0c1f33f4c18fe`  
		Last Modified: Wed, 04 Sep 2024 23:12:28 GMT  
		Size: 4.2 MB (4164313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ed06d2ab6037ccd8879f98a11ef9c5634091df7e2b0df0353a8abc4c0da8632`  
		Last Modified: Wed, 04 Sep 2024 23:12:28 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:10334b6ea7d1540cc93a254d83cd2523a51498acec6550d9c498e8a08d48cc5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285518044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985c6ec0023ef93ca3b509422da444dedbe01e3a9d5be254679b43319cbbf8cd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:c451ece1244c14bce110ffbe6906867ce12f8e88234988b0edba91009a9dbbf8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f572303598915f7fb61cc4b47f7207c9ee64d52b9db5fc03ee133ec2dd679347`  
		Last Modified: Wed, 04 Sep 2024 22:02:25 GMT  
		Size: 26.6 MB (26589615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6ad557e4a293fcec008cedd79106f6ef955c5e24dd1cf657b7e40744cbd440`  
		Last Modified: Thu, 05 Sep 2024 12:09:02 GMT  
		Size: 258.9 MB (258928429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:185308415291c86011485ca6ae5c6c9d24cd0c0455ce31e92cf3c83745b877e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bf9c70231335a286bd907aabb78dd6e765230974619f7450019bae997fdae2`

```dockerfile
```

-	Layers:
	-	`sha256:0ca59ac3c5a0d7f54b0976168e45637127fce7006546c43de9f9cd9f69156945`  
		Last Modified: Thu, 05 Sep 2024 12:08:56 GMT  
		Size: 4.0 MB (3973664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f211237bf8e70aada0e861f20fdf49b04c778600c8657efe317c065eefeb7569`  
		Last Modified: Thu, 05 Sep 2024 12:08:56 GMT  
		Size: 11.9 KB (11936 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea400ae221974016cf01cfc99716046022430cc14de5608db498729f7618f668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.7 MB (335717687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290fe501a9234536387b5b30c99f27e439d23d64536b7815fe2de01d3682d07f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cb6cdc1948b06794974ff2e98a7005fb4728291f972fd9fe6890a51b35589`  
		Last Modified: Tue, 13 Aug 2024 11:45:59 GMT  
		Size: 305.6 MB (305641600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a3676673a581a4a22ae35dba326c5d9ccd2bdbde7ba9cfab0820cb96773f78ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621cc11386fc3351be6a2c44213e137c509b73cbc571f6de7541e04cbe8a4ac1`

```dockerfile
```

-	Layers:
	-	`sha256:25d0ce1b84cd190aa843a54b2f062344d99aacfdeb1f4215da7fc975e859651e`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 4.2 MB (4161095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66c9bde30e15c9a5a38892f97be33009492c2633b0fd4b560fb3907e93ecf62`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 12.2 KB (12175 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:c57675f231e19c0114750c276bb686ec8f0125ca00ee3e1d1b5cbae8aa6e9c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286389854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688be6d01f10da5e726acf8027b050c5d0962197d8e667b43261dd385a0c4f33`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f518608d5d6e978d31e2f8814affa386d3c917837a7823597d8d0c86477c8ee`  
		Last Modified: Thu, 05 Sep 2024 00:29:16 GMT  
		Size: 254.0 MB (253976540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b8f569048c31e591add1ab0d8b9f3f7cdc3272c6072100db265bb675887e53bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b1c275df90e1f83fc7b09b7a4c32c00de4fcc7346e5ccb68c1c4d1125c6a8a`

```dockerfile
```

-	Layers:
	-	`sha256:c70252172c1a37c2fb6ce0894158a216a4c5a6219906aa119f3e9e9ba2a7a3e1`  
		Last Modified: Thu, 05 Sep 2024 00:29:11 GMT  
		Size: 4.2 MB (4156081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e4cc08677260612ec187771e82aba25a4655648cf3a308d21be1aac5637858`  
		Last Modified: Thu, 05 Sep 2024 00:29:11 GMT  
		Size: 11.8 KB (11837 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:3b063eaf3446b0a4b0201201275e496c4cd37e2df97786f5d7dc11872b49b3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281302014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dbc33dcd7620a227caf71dad7ca84f2c231ca26a65558ec553fc37860ad920`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb61bbbd90ca687d8cf9a0fa307847411b891a05ea61c9d5075175311224639a`  
		Last Modified: Thu, 05 Sep 2024 06:21:52 GMT  
		Size: 246.0 MB (246002740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d63496117c7b6330c99ea4b31e3cbc463e1a92f1262350984fe3b84bfb625403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc7ee7587c6a789c8c0cb6838e839d1bc47ef5a05fb52e1a8aecd9ba1309500`

```dockerfile
```

-	Layers:
	-	`sha256:e119f05f2002b1464fc5731d6d2308b0ee4020a17744313cb4811c29106c6988`  
		Last Modified: Thu, 05 Sep 2024 06:21:46 GMT  
		Size: 4.1 MB (4125251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a7aed5f5e3aaffc866e0aea2a3e9c3e60ffd7bd2e2c5f077eae9468fe3db810`  
		Last Modified: Thu, 05 Sep 2024 06:21:45 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.80.1-slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:f454359a3d4de0bd0fb0c063a4b2366299600bdafe2a34fce998a23bd87a25b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.1 MB (335147088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295366e0c73019a39ee770be37d3e862fefdfb2d00b4f7c49596abdad9e970a7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16cb9b3555a4b7e7bf56b97db7af5a62cffeb6ab93ea0db4eb8789c042664f7`  
		Last Modified: Thu, 05 Sep 2024 07:10:02 GMT  
		Size: 305.5 MB (305483641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.80.1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:12bb9211940c142484034d59efb2b6239d0aac58cdddb50774003ddf6be8b843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6295da41651110039f4ab6f25165e32bb9af3ac5f36ff76349f61c20645b6e6`

```dockerfile
```

-	Layers:
	-	`sha256:a827dd2d48d500c33de79a8d81e812dace7251b737e92fd0238c8aeabbf45f26`  
		Last Modified: Thu, 05 Sep 2024 07:09:57 GMT  
		Size: 4.0 MB (3996088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2044074a697d1c663a041eb3ace815004e270dbc711679b502f0c86f5edbb643`  
		Last Modified: Thu, 05 Sep 2024 07:09:57 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.19`

```console
$ docker pull rust@sha256:b3ac1f65cf33390407c9b90558eb41e7a8311c47d836fca5800960f1aa2d11d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:25c79c9854cd4bedc797a88e2d4dc1b4502d22a540867fa66257e6e03c4c1d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279155377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204c24ee400cc1a13c13b275cb04657bc5e47150ce5a4e77d3a7671021b9a32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061bdf3a42c6c4489e9e78047cdaa3af6f7b63e5d255e0ab9e6660d180836f4`  
		Last Modified: Thu, 08 Aug 2024 20:02:39 GMT  
		Size: 55.3 MB (55346819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acee9c63bebda8ae8f027b6e99deee99e570d38430b1f5de3f271f853c530cc`  
		Last Modified: Thu, 08 Aug 2024 20:02:41 GMT  
		Size: 220.4 MB (220389518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:d7f847716cae21dc55ac84add1dab418798ef33b8624854fb6b8c65f17169302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 KB (723898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b861f59014e11471235b45ca58fe55e1bce20e2d3235649938ddd8e10ac83b`

```dockerfile
```

-	Layers:
	-	`sha256:cda40d4b828cdfea673ac423a0571622627c241817509f9ba745a38be1560b4f`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 713.4 KB (713423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e221181fdb20703a089d816b169375986ae47adf4002808cc72821fdf9b9e942`  
		Last Modified: Thu, 08 Aug 2024 20:02:38 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1c9472feed43f2708eaa2821cf5f0a646160cee7be9d584bf730e755eedbee94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286589138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040de42a611e54d884e5a00d1765df3de096fba714c4defafc0750e79bcb340e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1b276de5f8a8a2fd3e6b931c4e180f78458c812dda2346f21361c13108618d`  
		Last Modified: Fri, 26 Jul 2024 00:29:37 GMT  
		Size: 53.0 MB (52995484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2abe5cb54c2cfbfce48a309498337e7a126ab4ea86b6df2ef36f1613354c5c4`  
		Last Modified: Thu, 08 Aug 2024 20:22:15 GMT  
		Size: 230.2 MB (230235196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:c808914252afc74e4ba729fb24e0bb95b91c9a2f8608b2a35bd39fc92b7d5a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 KB (760185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27a7713ca3e5389a8f63774d2f2029f10a884a7ef5258c5a110ac3cc5fa9642`

```dockerfile
```

-	Layers:
	-	`sha256:dab1ad55931d3701c8a9c82cd1652b524d00f22c57bd6fc291789059b83165e3`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 749.4 KB (749410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a90f930d575ecabd7599845ca4411c5bf521f8695acca03fbc6142619add3f7`  
		Last Modified: Thu, 08 Aug 2024 20:22:09 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.20`

```console
$ docker pull rust@sha256:1f5aff501e02c1384ec61bb47f89e3eebf60e287e6ed5d1c598077afc82e83d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:80caa4c1b5e4d2406ceec235e5f9b79098f56eca0b912a71d0a23284f86c7482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279321569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111551ce0f90369340081e58f9411eee8827414414296c5e232a277335e5d3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb6359d13591b600ca3a44dfa073de60c83f7ef4a56dcb3773e93f80ef3ad0`  
		Last Modified: Thu, 08 Aug 2024 20:02:44 GMT  
		Size: 55.3 MB (55309280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09478e90ebb6047ae5ea005dac56b379efbbe4edf6745b581ae262e0d37d99`  
		Last Modified: Thu, 08 Aug 2024 20:02:48 GMT  
		Size: 220.4 MB (220389397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:6a2e1ce57cd0a7f1fbf66a79ba4d92588683e54f34051a52213417bbd415815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.6 KB (722614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67cfa84ca778650d7ba26d744d6c2f7770367d48cabadada35fac97b9ee850`

```dockerfile
```

-	Layers:
	-	`sha256:229dd432527b0b4e7785a8aae6ec0fc6de115d52d72e97823eb19952c0381ed2`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 710.9 KB (710935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5366d1053e71bd7c3e97f538b9afad37314bc14498447a8cc9fd894130a59af3`  
		Last Modified: Thu, 08 Aug 2024 20:02:43 GMT  
		Size: 11.7 KB (11679 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ec57f09550fe1ca1ff01259ec3b73e41f71f25871b8193eaab303899b0e68b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002cbd9cfabb91632f82af75fa6884d57237607601f260c273e6abcdddf6910d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cdabcc618ad354d8fb66b09b06ae79e0efcac87d0d28de511d3f0fd90684bc`  
		Last Modified: Fri, 26 Jul 2024 00:30:47 GMT  
		Size: 52.9 MB (52946256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1e9307f69cc057090879db4d165747731bdb16c302df5ffb718e4c6f38df55`  
		Last Modified: Thu, 08 Aug 2024 20:23:21 GMT  
		Size: 230.2 MB (230235100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:b74a5a3c0fbac0a8f90593128b92d2bd190769a99a46876a0a62da2944269b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a95028a6104d4c42f4b84ccb7a785726e699c060508be9570512d30016c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f0a14786a45f1c10abf2a9c947fa36f1a428def8564ebed425854ce562d6f33`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 747.0 KB (746971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b6309811631534b2b7158c7e212299f3f6304968de341df876beeb00ce73a`  
		Last Modified: Thu, 08 Aug 2024 20:23:16 GMT  
		Size: 12.0 KB (12027 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:d22d8938f0403ee31c118b5bf2162b883313dd7f387f859d9f2accd7c884c385
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
$ docker pull rust@sha256:883df89a3ed53fb0e0f6a67d79cfebf72906d97f9d816379fdf941af969be1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529316453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a14ebf5765b504232d2db40bfcd2a69b22156ada6f3880a2c34f3819fbd115`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ff076d818ad6b8557e03e10c83657cc716ab287c8380054ff91571c8cae81`  
		Last Modified: Wed, 04 Sep 2024 23:02:08 GMT  
		Size: 211.3 MB (211266623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f8a55b70e1cdd0ddc6b738b3a1baeadd53644ee6819ff60426e800045a98b0`  
		Last Modified: Thu, 05 Sep 2024 00:29:41 GMT  
		Size: 180.3 MB (180291957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:6ba93cd0c1015d1e433471ab39bd16a063af791c7331e18df530f8e6fe722b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085cfe3bb88e92259308df253ca6817c99f844fa21d86e0c22fe8cf9636007eb`

```dockerfile
```

-	Layers:
	-	`sha256:01b822a94cc2d7c507e8248d8c5d3e6c9bd0ced556d1a385cb8329261573c353`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 15.4 MB (15445058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd49b3074e925710d484fdd75b4d3689f4de021889974dec39020d6925a4719`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:b6f344496c19f4a91adffeb1c6f3975ed4f0c134965451cc96505002f8a7bd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d72160a77779d619c0691d2d11e9cefcf875d6caba4743817d21439067c8493`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e3c71ceb3b7032e8a78ea70e306ec97b152570eeaae849a0c97bb61b2b12287f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe61db625a1b529903f1126ded0caa9e4e1c247503d524cd43bc15454b6bcc2f`  
		Last Modified: Tue, 13 Aug 2024 01:00:32 GMT  
		Size: 45.1 MB (45148160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06599d70e5763853acd56f8e4938729e068e7942382f335f96ce0ae3bc5a63a`  
		Last Modified: Tue, 13 Aug 2024 01:32:20 GMT  
		Size: 22.0 MB (21954622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3af44a3c0ce16617696528373b53738420f91f3383cda1666cc673cbf6fe50`  
		Last Modified: Tue, 13 Aug 2024 01:32:41 GMT  
		Size: 59.2 MB (59221928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dd2b78206591edf08b24f09f26f742a3d689be108f6e3cf74538c78a14b7d8`  
		Last Modified: Tue, 13 Aug 2024 01:33:16 GMT  
		Size: 175.2 MB (175182857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4fbda85fa1661a9607ed15220d6cd0ba0ea7cfe8f07296134db5ed818046e5`  
		Last Modified: Wed, 14 Aug 2024 00:19:33 GMT  
		Size: 216.6 MB (216645579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1ddf44bae2a2ab49522a19c70acf650db42bb2f6c68e2dfba4087a2465283dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364116a8162d50ac678aca565a1904bfbfc433d01d7bfb4d35fa37480d1ee7d3`

```dockerfile
```

-	Layers:
	-	`sha256:2381d137772c59a7125907148fb80cbd972483f5c489ea3758959c92823577f7`  
		Last Modified: Wed, 14 Aug 2024 00:19:29 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:befe4b689653998a8d04333bd6495dbe1e85862cc244c47d41fe0a25d659ed10`  
		Last Modified: Wed, 14 Aug 2024 00:19:28 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fda6ddc43a715feab22a98e1bcd801537ce6788377cf1d4919e08819a335cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8219a5ff56d4a59051986054024af17d4463ef5e7adcdae8e770fb8af061687f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275677961327bd0cf394699228e29d7caf27f171c627899a20ebc9eeb550e209`  
		Last Modified: Tue, 13 Aug 2024 01:09:34 GMT  
		Size: 64.0 MB (63994880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46e144614e1ae9b82b5d89d16a31a506542733eabceebfac041e0192dfafcf4`  
		Last Modified: Tue, 13 Aug 2024 01:10:06 GMT  
		Size: 202.6 MB (202624176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8a9c35b14d62b7daaefd544a6bbd91b6c1fab2f57de7223cb3c2db641f8f3f`  
		Last Modified: Tue, 13 Aug 2024 19:47:59 GMT  
		Size: 249.9 MB (249924612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:94216dd82c491d7e6f65884930be2ef3b32567829f661b973bf6de9670caf8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8403ed68ffd2e12e6bb5977a46b702d64bfe7042a23546abf7e9a207f9a7b82a`

```dockerfile
```

-	Layers:
	-	`sha256:c73483c681ff733971d6bac2c66743acb42444bba080cb661d51c906d243b6de`  
		Last Modified: Tue, 13 Aug 2024 19:47:54 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27ab72a7b07fef9cb15504b90ff201b9db8849760efaab45970b5339508eecf2`  
		Last Modified: Tue, 13 Aug 2024 19:47:53 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:8f7ec0c462a97974a827203da3d48a0e0b650b3134b6ff62d4351bc4d35fd88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544833213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b757d10a8aa83b2245bf2670352842b8001028cf212163001100db5cdde0e97d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0a7648037128b800dbf0363e27e6092c0253e0bd9beeb38a8aa572225934be`  
		Last Modified: Wed, 04 Sep 2024 23:21:06 GMT  
		Size: 210.2 MB (210181614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff91319e9e7fc8f2ebbd39fb7eea49ff32d26c0a80075db4be2000172b1e2c2`  
		Last Modified: Thu, 05 Sep 2024 00:29:34 GMT  
		Size: 193.2 MB (193190646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:89423d1df8d449f51c36385120c91be4bda5ca07d565c86391e83b052273eee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15436735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d654f978ebaf05551dd313df3e6572228fc317f1462fbfdb238633e8f72fd6`

```dockerfile
```

-	Layers:
	-	`sha256:ea624d5326397b6cff430e813450f3b7fe48aa493d7c1d50fcd441a09ff02a90`  
		Last Modified: Thu, 05 Sep 2024 00:29:29 GMT  
		Size: 15.4 MB (15423818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb7e5ec2189b610823dc5ef4564f4af35bd76533a4a716c603c9ed8112e1c9f`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:4230383893f246794d2aec426cdeae0c6d6559692181a139b8035d7e0e9d73cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554124880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d39abdea1b0ddb7070a48b89cdc15e163bcde224eca74a0a407a3262dd26a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35476fbf45cb5153abf5ea2df7487a74d0cd0de327ba5e9e970713f9e385650`  
		Last Modified: Tue, 13 Aug 2024 01:35:51 GMT  
		Size: 214.3 MB (214264660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a28f21591d3325119c396461297085c135f02fe0c43f55e5d9d04babfe7f8a`  
		Last Modified: Tue, 13 Aug 2024 21:43:47 GMT  
		Size: 191.0 MB (191025993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:fbe15bbd473bc7a23be790e4137162ff70e31cbb32389f146816a3880926436a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a621b08bd27a06288b964fba10a38173fa5365c5ddc7e8a9cccb7618ca77ac`

```dockerfile
```

-	Layers:
	-	`sha256:327622dc45cc14d8fa9bfdeff84b04b9db53727ba825e799d576336b111a738f`  
		Last Modified: Tue, 13 Aug 2024 21:43:41 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a0869e8a6fa0e4af601c1b3715fc98fa182a33f1fb3f0f496d5860b0aee948a`  
		Last Modified: Tue, 13 Aug 2024 21:43:40 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:7b40e1bbb384a9e7239ae1b346dfdcddcc6425cad2d1117869ccdefaf0de3092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581466000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456a0c8f4b4dc0ce6ef7658d91e2dee89d72fc4c661d9f8cfe429d7bb25f907d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d84b8bb13cbf61ae13e4c378871c52c3e9b521657a5faa02f0159e1be542a05`  
		Last Modified: Tue, 13 Aug 2024 01:25:25 GMT  
		Size: 183.3 MB (183265629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7110931c79b785aa170a85a350cfeaf7e6a2f5422afbf81362184df95653f728`  
		Last Modified: Tue, 13 Aug 2024 20:55:34 GMT  
		Size: 263.1 MB (263095149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4117efcb78d41d704ce0a167cacf739449fda5091e7871c7e274690dc616d093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971437f70ca6e9f6a749c7db65a07092f93076ec42375222e3ddc55b9a04a1a2`

```dockerfile
```

-	Layers:
	-	`sha256:9b04722e355f910725ee8dfca9c787edafbb9ce2d45729798f8e0e75d9f2f969`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2abf42730b95caa5d1a2d651db714bd4b84a8497980620b6f55cc3b01090eff8`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:f6f599d3f027a97fb60cb87854199fcde390e25cee216712c3f9eede545b052e
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

### `rust:bullseye` - linux; amd64

```console
$ docker pull rust@sha256:cd0a8eb7afeec51e842d834ddf4b153b583427c04da5ac5ef222046604f2318d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.9 MB (502931767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884e2fd2885bf130e08c231e991c8955ce71fb9d987128c310adc962761785db`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d691dff6d17d00b0cbbc4772eb805d97e02504d89ea3e5857cb97c943b74462`  
		Last Modified: Wed, 04 Sep 2024 23:02:33 GMT  
		Size: 54.7 MB (54726023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cfd30604666dfdd92bea930c06ee58dc927e0da651b862491af1648a4aca73`  
		Last Modified: Wed, 04 Sep 2024 23:03:03 GMT  
		Size: 197.1 MB (197067753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed0b0ded1b8b5f8453e7635369b38f8b2c318d0f51e26f0ad4269979ea9ba32`  
		Last Modified: Thu, 05 Sep 2024 00:29:16 GMT  
		Size: 180.3 MB (180292264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f2a08571ef0de6347d1fa328909f711aa08ca828ae893b1b9ec79d43dce4c54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15064067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd481bb1b4a6912e1c25b6c10d942ed60669c539876c401676bfb21ce5ba1b38`

```dockerfile
```

-	Layers:
	-	`sha256:62bbe7371ce9ed40e4bd78dc1e1895a7a86b51139e8a6c0ba845bb8a9e7c01d2`  
		Last Modified: Thu, 05 Sep 2024 00:29:12 GMT  
		Size: 15.1 MB (15052263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8510778438d2ad2268e7ca558d841d6f5554bde8515952028f0afb9fc9af50b5`  
		Last Modified: Thu, 05 Sep 2024 00:29:10 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:b9e1bff441726839efdfa70625797c71d12ed393eff196835675985011379a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.6 MB (499629389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232ed045be751771b4dd1a9891b4b8771355c7d382c7eacb30508c0719434f31`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:7674761630f1c6dfdf95da576bd19dbfe7bc4d942d11d31eff2012ec8b2c7ff1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a986643b6b9d356e3c44ee35fdd352a1064e1fb2a1524c0627e84ba34207b8e2`  
		Last Modified: Tue, 13 Aug 2024 01:01:15 GMT  
		Size: 50.2 MB (50242333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8868560f8e978ee832f67027b7330376be350ffacd30a199b730c72d9550757`  
		Last Modified: Tue, 13 Aug 2024 01:33:28 GMT  
		Size: 14.9 MB (14879497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7deb3ed53b620f0871f5051050fe0d850fd52da94803425820e75bb7b8d4e2e`  
		Last Modified: Tue, 13 Aug 2024 01:33:45 GMT  
		Size: 50.4 MB (50357748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e6955cecd9dc8a3cc8022dd624334d4f3abc81e5801bb1a1d3ddcedd0ef645`  
		Last Modified: Tue, 13 Aug 2024 01:34:17 GMT  
		Size: 167.5 MB (167504270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d727c90103f0458fc4e1233059a99a4449a5658b19c4c04577e90716624ce68`  
		Last Modified: Wed, 14 Aug 2024 00:15:35 GMT  
		Size: 216.6 MB (216645541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:791c2d9db3d160e7e2a93c07568a9ba817c8588b5b3cdd31d37d029feff257b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14865179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc5a22e7dce30f830f957bd7ca405686def79f80919b6f3216dc62e91b57d20`

```dockerfile
```

-	Layers:
	-	`sha256:ea5f09999dd237783aaffbaf7252ec89e60410eefce29c463657d21103fad00c`  
		Last Modified: Wed, 14 Aug 2024 00:15:31 GMT  
		Size: 14.9 MB (14853305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2c6135a6881efe9cfaee1c1973570d4094d9c8efd4330011c071c0287552ad3`  
		Last Modified: Wed, 14 Aug 2024 00:15:30 GMT  
		Size: 11.9 KB (11874 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1dc2b70be87ca21e1298d3966b4821a1f2af9ca4aeb9030f2843156acaabc871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564070284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac07cd629c9ba7cac0f43633a49d02c086f7d0a89d75cdbe31f5443ad59d12d3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3db3ee6245513b1422983db21d89f4f743f300e726af9eff6c9f7e2dddcb67`  
		Last Modified: Tue, 13 Aug 2024 01:10:18 GMT  
		Size: 15.7 MB (15749505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5265d6983e8ed11fd8dc48e17209d3479015214ac92f89f4ac51b2e65060840`  
		Last Modified: Tue, 13 Aug 2024 01:10:33 GMT  
		Size: 54.7 MB (54694302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6073a281eb20b3b43e3cc472efa9f868c8f75fc13cae51a5b10fbe8054bc0ba0`  
		Last Modified: Tue, 13 Aug 2024 01:11:01 GMT  
		Size: 190.0 MB (189971927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15778b247abba33689070973283c965347f8ff7110aed80aba5d5dba886c8645`  
		Last Modified: Tue, 13 Aug 2024 19:46:34 GMT  
		Size: 249.9 MB (249924629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:050d7ffca1af96c20c5a95e9bee8bcd60d8c633ad6a598ed9807cf27439bb339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15066748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc0ceb3fdbd1db1a0bd675c616fcf05e981968d3be62ab462b147b4db354be2`

```dockerfile
```

-	Layers:
	-	`sha256:f3db632e0133fc65815084a91d7a97b2ef1b92d6c4127dc1e3a5b0852c77df14`  
		Last Modified: Tue, 13 Aug 2024 19:46:25 GMT  
		Size: 15.1 MB (15054632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:244e55ed7bcf50ecd68fa3c5e2277c974b6fe67c02fafbffdea96539a80b40d8`  
		Last Modified: Tue, 13 Aug 2024 19:46:24 GMT  
		Size: 12.1 KB (12116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:0b422e50d57c5086836b9b8dca05019ed63192ac2333521c92bc739dbb756427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.5 MB (521530165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfe8c5eaa38c914901128e3ea98bc83c9a639434eaf17b029b52761c8f6ec1c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4533261556c046eefdf517bc6e06bc455b876caf2226aa504a13b5d66d250281`  
		Last Modified: Wed, 04 Sep 2024 23:21:18 GMT  
		Size: 16.3 MB (16268301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341d50e4bbed9704aae2147f28b4a07fc71b73539d282c37f60e183d38865daf`  
		Last Modified: Wed, 04 Sep 2024 23:21:37 GMT  
		Size: 56.0 MB (56030074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d04d357b859cf9b5eb038042f7df289289aee35371021b6ba1005ff2818f428`  
		Last Modified: Wed, 04 Sep 2024 23:22:18 GMT  
		Size: 200.0 MB (199965007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a20660c7aef3eb352454fc403634b2bcff1e7bdf3d17279cd89af22056aa8d`  
		Last Modified: Thu, 05 Sep 2024 00:29:13 GMT  
		Size: 193.2 MB (193190616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0d0978b42325c7b639503fb6f81b435992e69cbb7cfaf3e43d43c7b73fb50a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15052575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57f256b77b0a5a96e6a8ec76adfeb153cb387874a4c211a0315b1113bbf662f`

```dockerfile
```

-	Layers:
	-	`sha256:5bfb69f09b1dfbfac72a0286789043735bcd7e8a317c1ff5fdbcdb83d28c4cb9`  
		Last Modified: Thu, 05 Sep 2024 00:29:09 GMT  
		Size: 15.0 MB (15040800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab48a51d9f27782d97a1e808bbe2f638eb8b4a0edc389264cd649bfe7be2808`  
		Last Modified: Thu, 05 Sep 2024 00:29:08 GMT  
		Size: 11.8 KB (11775 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:4b102819b654a311a824ae3a605e6503b76070cd4c4dfc6c227ff67f300c9a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.0 MB (522017613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3b534b39a25e918707b482ef622be1a3c9c8a8fa0889209dc5e17728198e1b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:25dc93c8090a0afba4b41321f81883857bfdd6b30ea9f278833c5a5d9d16ad52 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:dad1c3eca3bf4b2a67cef1dbad507d7a913df7bbe1e3f88044230dd291ada39d`  
		Last Modified: Tue, 13 Aug 2024 00:26:46 GMT  
		Size: 59.0 MB (58954654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b50eef4accfc66462c4cf81c03bb57857b5f3ac891da5b87bfdf1ba826c9677`  
		Last Modified: Tue, 13 Aug 2024 01:36:03 GMT  
		Size: 16.8 MB (16765928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df0e65d951ce5d0b07cbb65477bbb01cfa607241b5c5855f4fb361bedfd1247`  
		Last Modified: Tue, 13 Aug 2024 01:36:21 GMT  
		Size: 58.9 MB (58872586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9438dc035d6f851416f6745a25baa330ca04b6013564731b2c42ddce3979a2ff`  
		Last Modified: Tue, 13 Aug 2024 01:36:57 GMT  
		Size: 196.4 MB (196398494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2565e4d615d926780548ef217b5b10b6f6720e401eba39fa2e54c34ac84bf`  
		Last Modified: Tue, 13 Aug 2024 21:41:58 GMT  
		Size: 191.0 MB (191025951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1447a0430183c6f9369fac6336bfeb4153f534eca6028b5b7f2a14f47a2eea7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15031565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4180a14646f843e73bc293d0bcf988986daa9a36f1818b643d0cbf4f72e8750b`

```dockerfile
```

-	Layers:
	-	`sha256:2e9e4840d282072216185364f3c9012dc3dd727785c3f7bcabcfba3f85cea47b`  
		Last Modified: Tue, 13 Aug 2024 21:41:47 GMT  
		Size: 15.0 MB (15019723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96395652f5022ec8fee2d3878beed560d61f66c18c72f6d1208e66097a7b25d6`  
		Last Modified: Tue, 13 Aug 2024 21:41:45 GMT  
		Size: 11.8 KB (11842 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; s390x

```console
$ docker pull rust@sha256:3944244146d900e21947895f40f80b74185b5ec24475ac7026203cf5835798ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 MB (559197374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3320425c6a524ca810ff5aa40074b451cbfd12bd85905918328c6f2c509542ea`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c695efccb58000e04eb154deca02ce22ea52fd05ee4246281c66bb7a42d20a96`  
		Last Modified: Tue, 13 Aug 2024 01:25:32 GMT  
		Size: 15.6 MB (15641934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3f87ffa253b4cb357637ad56494facf5bf533f6fd3bdf78f1066c6fb0fb23`  
		Last Modified: Tue, 13 Aug 2024 01:25:44 GMT  
		Size: 54.1 MB (54075217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b49e88f43277ce63fe01761080f821f3b3be9f581e45ed6dbb50b5168642a1`  
		Last Modified: Tue, 13 Aug 2024 01:26:08 GMT  
		Size: 173.1 MB (173060876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854c1c6359c025e4a47dfbac10a25e7961b24a754123354e9bc34bab7f277cd3`  
		Last Modified: Tue, 13 Aug 2024 20:53:28 GMT  
		Size: 263.1 MB (263095258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f3b7b40296ae25b3e80cc721493168b0e9a8b31191a5a589e1fdd64b7b46399e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf30e97755ca96ffe5387849e8ecfcbdf192586a462d01ace8c46d46294ea4bd`

```dockerfile
```

-	Layers:
	-	`sha256:14c9edf50d643bb3a3325e61fe0eca2f0e8449f141b26517a7cfb0ddd62f37be`  
		Last Modified: Tue, 13 Aug 2024 20:53:23 GMT  
		Size: 14.9 MB (14873217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c86f1e8337e8e681287c7507a3b747611ffa4a577e92858bcd2c92dc3271eba`  
		Last Modified: Tue, 13 Aug 2024 20:53:22 GMT  
		Size: 11.8 KB (11804 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:d22d8938f0403ee31c118b5bf2162b883313dd7f387f859d9f2accd7c884c385
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
$ docker pull rust@sha256:883df89a3ed53fb0e0f6a67d79cfebf72906d97f9d816379fdf941af969be1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.3 MB (529316453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a14ebf5765b504232d2db40bfcd2a69b22156ada6f3880a2c34f3819fbd115`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ff076d818ad6b8557e03e10c83657cc716ab287c8380054ff91571c8cae81`  
		Last Modified: Wed, 04 Sep 2024 23:02:08 GMT  
		Size: 211.3 MB (211266623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f8a55b70e1cdd0ddc6b738b3a1baeadd53644ee6819ff60426e800045a98b0`  
		Last Modified: Thu, 05 Sep 2024 00:29:41 GMT  
		Size: 180.3 MB (180291957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:6ba93cd0c1015d1e433471ab39bd16a063af791c7331e18df530f8e6fe722b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085cfe3bb88e92259308df253ca6817c99f844fa21d86e0c22fe8cf9636007eb`

```dockerfile
```

-	Layers:
	-	`sha256:01b822a94cc2d7c507e8248d8c5d3e6c9bd0ced556d1a385cb8329261573c353`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 15.4 MB (15445058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd49b3074e925710d484fdd75b4d3689f4de021889974dec39020d6925a4719`  
		Last Modified: Thu, 05 Sep 2024 00:29:38 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:b6f344496c19f4a91adffeb1c6f3975ed4f0c134965451cc96505002f8a7bd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.2 MB (518153146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d72160a77779d619c0691d2d11e9cefcf875d6caba4743817d21439067c8493`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e3c71ceb3b7032e8a78ea70e306ec97b152570eeaae849a0c97bb61b2b12287f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:fe61db625a1b529903f1126ded0caa9e4e1c247503d524cd43bc15454b6bcc2f`  
		Last Modified: Tue, 13 Aug 2024 01:00:32 GMT  
		Size: 45.1 MB (45148160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06599d70e5763853acd56f8e4938729e068e7942382f335f96ce0ae3bc5a63a`  
		Last Modified: Tue, 13 Aug 2024 01:32:20 GMT  
		Size: 22.0 MB (21954622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3af44a3c0ce16617696528373b53738420f91f3383cda1666cc673cbf6fe50`  
		Last Modified: Tue, 13 Aug 2024 01:32:41 GMT  
		Size: 59.2 MB (59221928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dd2b78206591edf08b24f09f26f742a3d689be108f6e3cf74538c78a14b7d8`  
		Last Modified: Tue, 13 Aug 2024 01:33:16 GMT  
		Size: 175.2 MB (175182857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4fbda85fa1661a9607ed15220d6cd0ba0ea7cfe8f07296134db5ed818046e5`  
		Last Modified: Wed, 14 Aug 2024 00:19:33 GMT  
		Size: 216.6 MB (216645579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:1ddf44bae2a2ab49522a19c70acf650db42bb2f6c68e2dfba4087a2465283dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15263583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364116a8162d50ac678aca565a1904bfbfc433d01d7bfb4d35fa37480d1ee7d3`

```dockerfile
```

-	Layers:
	-	`sha256:2381d137772c59a7125907148fb80cbd972483f5c489ea3758959c92823577f7`  
		Last Modified: Wed, 14 Aug 2024 00:19:29 GMT  
		Size: 15.3 MB (15250515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:befe4b689653998a8d04333bd6495dbe1e85862cc244c47d41fe0a25d659ed10`  
		Last Modified: Wed, 14 Aug 2024 00:19:28 GMT  
		Size: 13.1 KB (13068 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fda6ddc43a715feab22a98e1bcd801537ce6788377cf1d4919e08819a335cf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589724687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8219a5ff56d4a59051986054024af17d4463ef5e7adcdae8e770fb8af061687f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275677961327bd0cf394699228e29d7caf27f171c627899a20ebc9eeb550e209`  
		Last Modified: Tue, 13 Aug 2024 01:09:34 GMT  
		Size: 64.0 MB (63994880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46e144614e1ae9b82b5d89d16a31a506542733eabceebfac041e0192dfafcf4`  
		Last Modified: Tue, 13 Aug 2024 01:10:06 GMT  
		Size: 202.6 MB (202624176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8a9c35b14d62b7daaefd544a6bbd91b6c1fab2f57de7223cb3c2db641f8f3f`  
		Last Modified: Tue, 13 Aug 2024 19:47:59 GMT  
		Size: 249.9 MB (249924612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:94216dd82c491d7e6f65884930be2ef3b32567829f661b973bf6de9670caf8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15487566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8403ed68ffd2e12e6bb5977a46b702d64bfe7042a23546abf7e9a207f9a7b82a`

```dockerfile
```

-	Layers:
	-	`sha256:c73483c681ff733971d6bac2c66743acb42444bba080cb661d51c906d243b6de`  
		Last Modified: Tue, 13 Aug 2024 19:47:54 GMT  
		Size: 15.5 MB (15474240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27ab72a7b07fef9cb15504b90ff201b9db8849760efaab45970b5339508eecf2`  
		Last Modified: Tue, 13 Aug 2024 19:47:53 GMT  
		Size: 13.3 KB (13326 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:8f7ec0c462a97974a827203da3d48a0e0b650b3134b6ff62d4351bc4d35fd88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.8 MB (544833213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b757d10a8aa83b2245bf2670352842b8001028cf212163001100db5cdde0e97d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bdfed317a4eef020381a22fe8c7fa06bea7ff0b4a3da0d63ec90e0953da535`  
		Last Modified: Wed, 04 Sep 2024 23:19:58 GMT  
		Size: 24.9 MB (24895500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f610692db1620f4afe803908f30b5f7f161eb86c70e8b03501ba42c1b26b7ec`  
		Last Modified: Wed, 04 Sep 2024 23:20:20 GMT  
		Size: 66.0 MB (65990847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0a7648037128b800dbf0363e27e6092c0253e0bd9beeb38a8aa572225934be`  
		Last Modified: Wed, 04 Sep 2024 23:21:06 GMT  
		Size: 210.2 MB (210181614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff91319e9e7fc8f2ebbd39fb7eea49ff32d26c0a80075db4be2000172b1e2c2`  
		Last Modified: Thu, 05 Sep 2024 00:29:34 GMT  
		Size: 193.2 MB (193190646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:89423d1df8d449f51c36385120c91be4bda5ca07d565c86391e83b052273eee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15436735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d654f978ebaf05551dd313df3e6572228fc317f1462fbfdb238633e8f72fd6`

```dockerfile
```

-	Layers:
	-	`sha256:ea624d5326397b6cff430e813450f3b7fe48aa493d7c1d50fcd441a09ff02a90`  
		Last Modified: Thu, 05 Sep 2024 00:29:29 GMT  
		Size: 15.4 MB (15423818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeb7e5ec2189b610823dc5ef4564f4af35bd76533a4a716c603c9ed8112e1c9f`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:4230383893f246794d2aec426cdeae0c6d6559692181a139b8035d7e0e9d73cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.1 MB (554124880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d39abdea1b0ddb7070a48b89cdc15e163bcde224eca74a0a407a3262dd26a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee0fd668045667c6f72a45221a843b2814685439188d07b1defb9c75755e24`  
		Last Modified: Tue, 13 Aug 2024 01:34:46 GMT  
		Size: 25.7 MB (25695588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eed7e3592a50ab5e7544963d89fc48e8c78210f32cca0a16ecb3266ccbcc73`  
		Last Modified: Tue, 13 Aug 2024 01:35:09 GMT  
		Size: 69.6 MB (69581670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35476fbf45cb5153abf5ea2df7487a74d0cd0de327ba5e9e970713f9e385650`  
		Last Modified: Tue, 13 Aug 2024 01:35:51 GMT  
		Size: 214.3 MB (214264660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a28f21591d3325119c396461297085c135f02fe0c43f55e5d9d04babfe7f8a`  
		Last Modified: Tue, 13 Aug 2024 21:43:47 GMT  
		Size: 191.0 MB (191025993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:fbe15bbd473bc7a23be790e4137162ff70e31cbb32389f146816a3880926436a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15433363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a621b08bd27a06288b964fba10a38173fa5365c5ddc7e8a9cccb7618ca77ac`

```dockerfile
```

-	Layers:
	-	`sha256:327622dc45cc14d8fa9bfdeff84b04b9db53727ba825e799d576336b111a738f`  
		Last Modified: Tue, 13 Aug 2024 21:43:41 GMT  
		Size: 15.4 MB (15420335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a0869e8a6fa0e4af601c1b3715fc98fa182a33f1fb3f0f496d5860b0aee948a`  
		Last Modified: Tue, 13 Aug 2024 21:43:40 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:7b40e1bbb384a9e7239ae1b346dfdcddcc6425cad2d1117869ccdefaf0de3092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.5 MB (581466000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456a0c8f4b4dc0ce6ef7658d91e2dee89d72fc4c661d9f8cfe429d7bb25f907d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4892cafcdd92b58f81a3d2454bf31fc2ae1477e85040a44bd023ec333e8f8081`  
		Last Modified: Tue, 13 Aug 2024 01:24:43 GMT  
		Size: 24.0 MB (24048748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5671dc1d98954f99af5dadd617a0aa8b53840b28295900cb7cdd39eb592946`  
		Last Modified: Tue, 13 Aug 2024 01:24:58 GMT  
		Size: 63.1 MB (63125064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d84b8bb13cbf61ae13e4c378871c52c3e9b521657a5faa02f0159e1be542a05`  
		Last Modified: Tue, 13 Aug 2024 01:25:25 GMT  
		Size: 183.3 MB (183265629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7110931c79b785aa170a85a350cfeaf7e6a2f5422afbf81362184df95653f728`  
		Last Modified: Tue, 13 Aug 2024 20:55:34 GMT  
		Size: 263.1 MB (263095149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:4117efcb78d41d704ce0a167cacf739449fda5091e7871c7e274690dc616d093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971437f70ca6e9f6a749c7db65a07092f93076ec42375222e3ddc55b9a04a1a2`

```dockerfile
```

-	Layers:
	-	`sha256:9b04722e355f910725ee8dfca9c787edafbb9ce2d45729798f8e0e75d9f2f969`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 15.3 MB (15259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2abf42730b95caa5d1a2d651db714bd4b84a8497980620b6f55cc3b01090eff8`  
		Last Modified: Tue, 13 Aug 2024 20:55:29 GMT  
		Size: 13.0 KB (12966 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:907ff4b3ee7df57149ffee04f606e0a08b9b2ed3507f00a19cf3c9c0f74b7681
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
$ docker pull rust@sha256:a5ec1fc7928df7d24504ba8d0e7d9d096513736c5e1b6ac2eac686324a7419a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280194591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d74dd89cb787e264870a35d96127262dd06602fa988a39dfcdcc0b1b87fbe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bf03ed1c368822e027a2732362680f56ce5137e91ba84ce386e51fd189061c`  
		Last Modified: Wed, 04 Sep 2024 23:12:37 GMT  
		Size: 251.1 MB (251068107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:70c0f4a4e29a19fbc259b978e407d0198b3ac61100c49416558e718dd524198c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01702ebd45abe4c0861513492e59d285a1ddae1839f8e5329d1860652f8d06f6`

```dockerfile
```

-	Layers:
	-	`sha256:c76a08813897d00f0e0cd93710bc88f5964d3f99c81a2b63b3b37de6b1b76a4b`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 3.9 MB (3945035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8859af7c414d89532ca7d9eaabba0766d80d3479215e254051332407fdcd00e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:cc2333aa663bbc92356ee4ef6f8d6b642b445e5e666fc37b3867b0d5a5a893bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289213250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e848b8369d06b2c98853e0ef79cb6d790e729403484bc5f943edb29e2b9de6c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee65094ca49c2c7edf34dada1ae62118e6659c97a5f195e52d279a877fc800fc`  
		Last Modified: Thu, 05 Sep 2024 12:10:55 GMT  
		Size: 264.5 MB (264494985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:f2f6983e05e6ff77da77143b68cc48199d9ab5a09fba06cbee4c136d9e6882dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afc164a0e9d2735af5dcca73cb4960c28e6606be6974bc2c6ce6d2b5ef62f0e`

```dockerfile
```

-	Layers:
	-	`sha256:27bae23be9fa45ed1c009e8d69e579013b3f8c8b8ca757f8f9013ad7d9d27438`  
		Last Modified: Thu, 05 Sep 2024 12:10:49 GMT  
		Size: 3.8 MB (3761492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d87d0772c2929243aa21fe4b3f0ff0ac589b73e19adfed9d306123093fca53ba`  
		Last Modified: Thu, 05 Sep 2024 12:10:48 GMT  
		Size: 13.2 KB (13155 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:bbaff9e88af760191966cb0beadf94d503e1fafcd63b5c5ccaaa03e5598564b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290925711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca74e88b45440ef8d55e5c25ed0f7f2e9dbb4f2a8bafec24e6cccd1107c80d47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f23ccaebd9d56a75909c850e6ab0aa6693c9f89ba57b9977dba601890f2d94`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 260.8 MB (260781417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:149c847e4d5940e34735ec36d6b663715f0fa8e9ee11a0282d4f1dd871808c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc742cbf65f608e8de19416358e8901fba122e86286e96175686e134e9ccf789`

```dockerfile
```

-	Layers:
	-	`sha256:b5443a5469154e30b37c7de0b36037a6e20bddc881a424cdccd8843d369dcf48`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 3.9 MB (3926448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513d8a278aa21dcacbe90a3c89ef597af1dff583466d0036a15dcb4031011e06`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:d2d2feff3c61a9801dbe7735d194d197592c10a07446ebb5f58c360d44704e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292910541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7509806f664093ad6ec12f7fb65501f3540a72ac9809b5258a8d9d45ece500`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49174d43929c3e7d189a8935d2a77a8a17ce21f7070c6f983f380f120cdb6ae`  
		Last Modified: Thu, 05 Sep 2024 06:24:07 GMT  
		Size: 259.8 MB (259788183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:8ea384b40e2596497636656084514cc2dbfed040b686146c648676e33089efde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d551dc594d848945573fc2616217aee09021e04156415504cb1e6928f3fc4ecc`

```dockerfile
```

-	Layers:
	-	`sha256:af2dbf67be2945aa925798a7e18da8e96c52f624747225bffbdd0072388ec033`  
		Last Modified: Thu, 05 Sep 2024 06:24:01 GMT  
		Size: 3.9 MB (3917197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec30cdde83a25decfe9823cb5f543ce23f66684e6eb8437b988758d6a1d5ae8`  
		Last Modified: Thu, 05 Sep 2024 06:24:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:5e90e95a277cd1027f1ae3ba58dbdd1931c63ea9df38cb2221b06fe6dcec728f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340720684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8674b49ddd39434ab78416cdec54b901fceb062293e8069f1f0471ce40433e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594be6304f123a21b952480d35d2ed44c27f35cfe89018bf16a599b5022cb653`  
		Last Modified: Thu, 05 Sep 2024 07:11:55 GMT  
		Size: 313.2 MB (313230363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:df46a7b656a5378d8e6f0d320f4b2e4e629806b496e187e4aafa54adf82aed84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6739776cf152581ed3a68005323f9befa6f39245508765ad2724fccb84d6524`

```dockerfile
```

-	Layers:
	-	`sha256:574a1afcca67c6ddd0a7e471fdca0a769f0620648631b878ad4399a3be51c698`  
		Last Modified: Thu, 05 Sep 2024 07:11:50 GMT  
		Size: 3.8 MB (3787360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:239faceff7d2873bf0a8f549a7a3bb22ddc18eea16d381f8e5c529f659546778`  
		Last Modified: Thu, 05 Sep 2024 07:11:49 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:907ff4b3ee7df57149ffee04f606e0a08b9b2ed3507f00a19cf3c9c0f74b7681
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
$ docker pull rust@sha256:a5ec1fc7928df7d24504ba8d0e7d9d096513736c5e1b6ac2eac686324a7419a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280194591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d74dd89cb787e264870a35d96127262dd06602fa988a39dfcdcc0b1b87fbe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bf03ed1c368822e027a2732362680f56ce5137e91ba84ce386e51fd189061c`  
		Last Modified: Wed, 04 Sep 2024 23:12:37 GMT  
		Size: 251.1 MB (251068107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:70c0f4a4e29a19fbc259b978e407d0198b3ac61100c49416558e718dd524198c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01702ebd45abe4c0861513492e59d285a1ddae1839f8e5329d1860652f8d06f6`

```dockerfile
```

-	Layers:
	-	`sha256:c76a08813897d00f0e0cd93710bc88f5964d3f99c81a2b63b3b37de6b1b76a4b`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 3.9 MB (3945035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8859af7c414d89532ca7d9eaabba0766d80d3479215e254051332407fdcd00e2`  
		Last Modified: Wed, 04 Sep 2024 23:12:32 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:cc2333aa663bbc92356ee4ef6f8d6b642b445e5e666fc37b3867b0d5a5a893bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289213250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e848b8369d06b2c98853e0ef79cb6d790e729403484bc5f943edb29e2b9de6c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee65094ca49c2c7edf34dada1ae62118e6659c97a5f195e52d279a877fc800fc`  
		Last Modified: Thu, 05 Sep 2024 12:10:55 GMT  
		Size: 264.5 MB (264494985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f2f6983e05e6ff77da77143b68cc48199d9ab5a09fba06cbee4c136d9e6882dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afc164a0e9d2735af5dcca73cb4960c28e6606be6974bc2c6ce6d2b5ef62f0e`

```dockerfile
```

-	Layers:
	-	`sha256:27bae23be9fa45ed1c009e8d69e579013b3f8c8b8ca757f8f9013ad7d9d27438`  
		Last Modified: Thu, 05 Sep 2024 12:10:49 GMT  
		Size: 3.8 MB (3761492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d87d0772c2929243aa21fe4b3f0ff0ac589b73e19adfed9d306123093fca53ba`  
		Last Modified: Thu, 05 Sep 2024 12:10:48 GMT  
		Size: 13.2 KB (13155 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4ba626250746ad4489534889583f3610f9c975c35533b811df67cc134243c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344923440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e41f2eea73e4a60fd98d4bf20b3fcecb79a71b3bad09485c91f88f67d977226`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf51412034122c2dbea388e4b2d63f725423fd05f79506b09f9f2e6d241eaa7`  
		Last Modified: Tue, 13 Aug 2024 11:47:30 GMT  
		Size: 315.8 MB (315766912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3e210a91627c71cd919421c2b4aba707aed9e0d30bca13643f19e919af56ff22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb76b033bb0f457e5d06b339967844494d2d1578483b46a34854b3c6ad8df8e`

```dockerfile
```

-	Layers:
	-	`sha256:98a51b0b7d6c925ecacb05ad3413f9149ad596bf75aaa50296761155e31d5746`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 4.0 MB (3967400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c6bd4bff0426f91a0db015b5ff2aef9e1e2259732db26724f29d61da05fe5c`  
		Last Modified: Tue, 13 Aug 2024 11:47:24 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:bbaff9e88af760191966cb0beadf94d503e1fafcd63b5c5ccaaa03e5598564b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290925711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca74e88b45440ef8d55e5c25ed0f7f2e9dbb4f2a8bafec24e6cccd1107c80d47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f23ccaebd9d56a75909c850e6ab0aa6693c9f89ba57b9977dba601890f2d94`  
		Last Modified: Thu, 05 Sep 2024 00:29:28 GMT  
		Size: 260.8 MB (260781417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:149c847e4d5940e34735ec36d6b663715f0fa8e9ee11a0282d4f1dd871808c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc742cbf65f608e8de19416358e8901fba122e86286e96175686e134e9ccf789`

```dockerfile
```

-	Layers:
	-	`sha256:b5443a5469154e30b37c7de0b36037a6e20bddc881a424cdccd8843d369dcf48`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 3.9 MB (3926448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513d8a278aa21dcacbe90a3c89ef597af1dff583466d0036a15dcb4031011e06`  
		Last Modified: Thu, 05 Sep 2024 00:29:22 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:d2d2feff3c61a9801dbe7735d194d197592c10a07446ebb5f58c360d44704e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292910541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7509806f664093ad6ec12f7fb65501f3540a72ac9809b5258a8d9d45ece500`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49174d43929c3e7d189a8935d2a77a8a17ce21f7070c6f983f380f120cdb6ae`  
		Last Modified: Thu, 05 Sep 2024 06:24:07 GMT  
		Size: 259.8 MB (259788183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8ea384b40e2596497636656084514cc2dbfed040b686146c648676e33089efde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d551dc594d848945573fc2616217aee09021e04156415504cb1e6928f3fc4ecc`

```dockerfile
```

-	Layers:
	-	`sha256:af2dbf67be2945aa925798a7e18da8e96c52f624747225bffbdd0072388ec033`  
		Last Modified: Thu, 05 Sep 2024 06:24:01 GMT  
		Size: 3.9 MB (3917197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec30cdde83a25decfe9823cb5f543ce23f66684e6eb8437b988758d6a1d5ae8`  
		Last Modified: Thu, 05 Sep 2024 06:24:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:5e90e95a277cd1027f1ae3ba58dbdd1931c63ea9df38cb2221b06fe6dcec728f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340720684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8674b49ddd39434ab78416cdec54b901fceb062293e8069f1f0471ce40433e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594be6304f123a21b952480d35d2ed44c27f35cfe89018bf16a599b5022cb653`  
		Last Modified: Thu, 05 Sep 2024 07:11:55 GMT  
		Size: 313.2 MB (313230363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:df46a7b656a5378d8e6f0d320f4b2e4e629806b496e187e4aafa54adf82aed84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6739776cf152581ed3a68005323f9befa6f39245508765ad2724fccb84d6524`

```dockerfile
```

-	Layers:
	-	`sha256:574a1afcca67c6ddd0a7e471fdca0a769f0620648631b878ad4399a3be51c698`  
		Last Modified: Thu, 05 Sep 2024 07:11:50 GMT  
		Size: 3.8 MB (3787360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:239faceff7d2873bf0a8f549a7a3bb22ddc18eea16d381f8e5c529f659546778`  
		Last Modified: Thu, 05 Sep 2024 07:11:49 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:3bddded5af7155cafc29701e0701bcf3712a407fc7d642423760ec266e5a0682
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

### `rust:slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:11fbefae37d29d4b00e0b566b044cc3a6b872505aef297eb9b155fdacf677a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271859977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8888f7ee42b36e189196bd0c8bcaa7b82dbe62234fd5dece168368ef9f93bc1b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009542abce00716699fc9f02523d81058a5e4a326eae717d2fea8c06f55be526`  
		Last Modified: Wed, 04 Sep 2024 23:12:34 GMT  
		Size: 240.4 MB (240431300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6b2212261e50269ab865ff857cfd68b718e0401726883d6493ee31389b62e67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c6bb2b68bcf2dfda78433017e4d559b0e95616710d78a278a33f9792c49d48`

```dockerfile
```

-	Layers:
	-	`sha256:d9798046ab832947c5ae4ab6c01783c3230b53dad783b0dc2cb0c1f33f4c18fe`  
		Last Modified: Wed, 04 Sep 2024 23:12:28 GMT  
		Size: 4.2 MB (4164313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ed06d2ab6037ccd8879f98a11ef9c5634091df7e2b0df0353a8abc4c0da8632`  
		Last Modified: Wed, 04 Sep 2024 23:12:28 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:10334b6ea7d1540cc93a254d83cd2523a51498acec6550d9c498e8a08d48cc5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285518044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985c6ec0023ef93ca3b509422da444dedbe01e3a9d5be254679b43319cbbf8cd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:c451ece1244c14bce110ffbe6906867ce12f8e88234988b0edba91009a9dbbf8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f572303598915f7fb61cc4b47f7207c9ee64d52b9db5fc03ee133ec2dd679347`  
		Last Modified: Wed, 04 Sep 2024 22:02:25 GMT  
		Size: 26.6 MB (26589615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6ad557e4a293fcec008cedd79106f6ef955c5e24dd1cf657b7e40744cbd440`  
		Last Modified: Thu, 05 Sep 2024 12:09:02 GMT  
		Size: 258.9 MB (258928429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:185308415291c86011485ca6ae5c6c9d24cd0c0455ce31e92cf3c83745b877e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bf9c70231335a286bd907aabb78dd6e765230974619f7450019bae997fdae2`

```dockerfile
```

-	Layers:
	-	`sha256:0ca59ac3c5a0d7f54b0976168e45637127fce7006546c43de9f9cd9f69156945`  
		Last Modified: Thu, 05 Sep 2024 12:08:56 GMT  
		Size: 4.0 MB (3973664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f211237bf8e70aada0e861f20fdf49b04c778600c8657efe317c065eefeb7569`  
		Last Modified: Thu, 05 Sep 2024 12:08:56 GMT  
		Size: 11.9 KB (11936 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ea400ae221974016cf01cfc99716046022430cc14de5608db498729f7618f668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.7 MB (335717687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290fe501a9234536387b5b30c99f27e439d23d64536b7815fe2de01d3682d07f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cb6cdc1948b06794974ff2e98a7005fb4728291f972fd9fe6890a51b35589`  
		Last Modified: Tue, 13 Aug 2024 11:45:59 GMT  
		Size: 305.6 MB (305641600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a3676673a581a4a22ae35dba326c5d9ccd2bdbde7ba9cfab0820cb96773f78ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621cc11386fc3351be6a2c44213e137c509b73cbc571f6de7541e04cbe8a4ac1`

```dockerfile
```

-	Layers:
	-	`sha256:25d0ce1b84cd190aa843a54b2f062344d99aacfdeb1f4215da7fc975e859651e`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 4.2 MB (4161095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66c9bde30e15c9a5a38892f97be33009492c2633b0fd4b560fb3907e93ecf62`  
		Last Modified: Tue, 13 Aug 2024 11:45:52 GMT  
		Size: 12.2 KB (12175 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:c57675f231e19c0114750c276bb686ec8f0125ca00ee3e1d1b5cbae8aa6e9c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286389854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688be6d01f10da5e726acf8027b050c5d0962197d8e667b43261dd385a0c4f33`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f518608d5d6e978d31e2f8814affa386d3c917837a7823597d8d0c86477c8ee`  
		Last Modified: Thu, 05 Sep 2024 00:29:16 GMT  
		Size: 254.0 MB (253976540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b8f569048c31e591add1ab0d8b9f3f7cdc3272c6072100db265bb675887e53bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b1c275df90e1f83fc7b09b7a4c32c00de4fcc7346e5ccb68c1c4d1125c6a8a`

```dockerfile
```

-	Layers:
	-	`sha256:c70252172c1a37c2fb6ce0894158a216a4c5a6219906aa119f3e9e9ba2a7a3e1`  
		Last Modified: Thu, 05 Sep 2024 00:29:11 GMT  
		Size: 4.2 MB (4156081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e4cc08677260612ec187771e82aba25a4655648cf3a308d21be1aac5637858`  
		Last Modified: Thu, 05 Sep 2024 00:29:11 GMT  
		Size: 11.8 KB (11837 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:3b063eaf3446b0a4b0201201275e496c4cd37e2df97786f5d7dc11872b49b3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281302014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dbc33dcd7620a227caf71dad7ca84f2c231ca26a65558ec553fc37860ad920`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb61bbbd90ca687d8cf9a0fa307847411b891a05ea61c9d5075175311224639a`  
		Last Modified: Thu, 05 Sep 2024 06:21:52 GMT  
		Size: 246.0 MB (246002740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d63496117c7b6330c99ea4b31e3cbc463e1a92f1262350984fe3b84bfb625403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc7ee7587c6a789c8c0cb6838e839d1bc47ef5a05fb52e1a8aecd9ba1309500`

```dockerfile
```

-	Layers:
	-	`sha256:e119f05f2002b1464fc5731d6d2308b0ee4020a17744313cb4811c29106c6988`  
		Last Modified: Thu, 05 Sep 2024 06:21:46 GMT  
		Size: 4.1 MB (4125251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a7aed5f5e3aaffc866e0aea2a3e9c3e60ffd7bd2e2c5f077eae9468fe3db810`  
		Last Modified: Thu, 05 Sep 2024 06:21:45 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:f454359a3d4de0bd0fb0c063a4b2366299600bdafe2a34fce998a23bd87a25b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.1 MB (335147088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295366e0c73019a39ee770be37d3e862fefdfb2d00b4f7c49596abdad9e970a7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 08 Aug 2024 14:23:42 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Thu, 08 Aug 2024 14:23:42 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 14:23:42 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 08 Aug 2024 14:23:42 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.80.1
# Thu, 08 Aug 2024 14:23:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16cb9b3555a4b7e7bf56b97db7af5a62cffeb6ab93ea0db4eb8789c042664f7`  
		Last Modified: Thu, 05 Sep 2024 07:10:02 GMT  
		Size: 305.5 MB (305483641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:12bb9211940c142484034d59efb2b6239d0aac58cdddb50774003ddf6be8b843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6295da41651110039f4ab6f25165e32bb9af3ac5f36ff76349f61c20645b6e6`

```dockerfile
```

-	Layers:
	-	`sha256:a827dd2d48d500c33de79a8d81e812dace7251b737e92fd0238c8aeabbf45f26`  
		Last Modified: Thu, 05 Sep 2024 07:09:57 GMT  
		Size: 4.0 MB (3996088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2044074a697d1c663a041eb3ace815004e270dbc711679b502f0c86f5edbb643`  
		Last Modified: Thu, 05 Sep 2024 07:09:57 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json
