## `rust:buster`

```console
$ docker pull rust@sha256:9fda27d89a8bd381f4a08f846f36160c4b76e214a9deb90b13d23a793105038f
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

### `rust:buster` - linux; amd64

```console
$ docker pull rust@sha256:2244124f5665bb11b9cfc5366e282dde8a07352a629b8acda6e444a6b0d9d67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.7 MB (489675206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271efa3fa4f8f11daabc83d0142e092de6daffa3a2b221c17cb11a018bf30f81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:41 GMT
ADD file:b604b7bddfed00352fcc1abb8f44014438aca55d833109520e80b61c5fb207a1 in / 
# Wed, 24 Apr 2024 03:28:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:13:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:14:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:15:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:dbd6422b1b97494149e51bbd6c24d444b4a8794d2702d105efce98c44de9ad50`  
		Last Modified: Wed, 24 Apr 2024 03:33:41 GMT  
		Size: 50.7 MB (50657502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3eeb481764e6e279258aa837b781d2473689eb7a7d79fc80fc0f4ea11407d3`  
		Last Modified: Wed, 24 Apr 2024 04:22:58 GMT  
		Size: 17.6 MB (17585553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1322649fbe6339542d838841a0f72dea49bb02186f02026edbca0748db168c1`  
		Last Modified: Wed, 24 Apr 2024 04:23:13 GMT  
		Size: 51.9 MB (51895971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf9ee9914dd7dd8911e1dfbcda44d2309024daab6b2d3a0cf1789cc5f01f9c5`  
		Last Modified: Wed, 24 Apr 2024 04:23:43 GMT  
		Size: 191.9 MB (191944705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8daa29db98552bd4644b287b2c5b65d0f6089996ae72babe1e3970c3a4d46a3`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 177.6 MB (177591475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:11c4ece20593157dfa975f92b01da46bfaafafa553e8b19e2ac4d0e1974b95e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15978515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7cdeb1b17b86871c4efdd6446468d6071547b02d1a9cec80a763b5e8e2e5a1`

```dockerfile
```

-	Layers:
	-	`sha256:eb7d78709672f7de3e63be46be4ed8232b21f4145da1800b695880acb36cc390`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 16.0 MB (15966858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c710547a52a67909ac042053e89dbcc77df5b5c9e23930cbbb0df3b6fb627ed`  
		Last Modified: Thu, 02 May 2024 17:53:24 GMT  
		Size: 11.7 KB (11657 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:f0d6a3697491ef047bd974db96c826fe4cc3a11c961d714f13c937689be291cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.5 MB (486503581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d485ccd86f883be8138643aac57cb92d94608bd0929b71f0a426da7c212ad139`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:eea1eb05334cd4d0032909b2c56fc86a54faad563cbc3d2d46e763ce9e8922ab in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6053d4fbe88696bd387c5a6ca72c4f07cd4ab05dd400053e07cbda873a2938d2`  
		Last Modified: Wed, 24 Apr 2024 04:12:15 GMT  
		Size: 46.1 MB (46129056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec1a754f2738b1bb75033d7a321adc0d1e46c1b687985d70ebf56ffb8d7cf7f`  
		Last Modified: Wed, 24 Apr 2024 05:05:04 GMT  
		Size: 16.2 MB (16216769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2938b8f8e3039d68edb4c9d824cc6012bb94d3556c6845983254f4c871a333b5`  
		Last Modified: Wed, 24 Apr 2024 05:05:23 GMT  
		Size: 47.4 MB (47410271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6bd2a5227e108925972240203c8ff1ce82cb985810155c1bdd663c0232b41e`  
		Last Modified: Wed, 24 Apr 2024 05:06:01 GMT  
		Size: 168.1 MB (168134979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec2d881cde81b17c2ea3e87c2a32efa48a01254a0e306533b24753e7c841c1f`  
		Last Modified: Thu, 25 Apr 2024 11:17:42 GMT  
		Size: 208.6 MB (208612506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:fda0c6676bd1bf7d474900b184290d33c60adc58f59dbb97966ccc150da8f71f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15780088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09070812226877a85f0c07f780b3a243a6cb81285e95ab0a94f7592262a0f549`

```dockerfile
```

-	Layers:
	-	`sha256:ce4758f9d183c378505d934a14473b7db2c541d5edc41649910956e20f216add`  
		Last Modified: Thu, 25 Apr 2024 11:17:38 GMT  
		Size: 15.8 MB (15769023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a3626852a89bad84cfd6e0f427ea81f25f9e0a8938da7446f85ddef3c332193`  
		Last Modified: Thu, 25 Apr 2024 11:17:37 GMT  
		Size: 11.1 KB (11065 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:aa0a37ca0de9da3c53e515026bbb65a2aa95a066bfe13d0ab3e1112125fa2b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.3 MB (544281487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a880268d891b71fc8f50cf500ef94142dccff47f9fd71c88d961e3344217d4af`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:5a7db8f66ffc46a108f386106163b47bdb4a3bcbe5341a94d47988b259039067 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:38adae2f446d050038d7d914eddb5b4a481b4c3e73ec18c36be90c376b639389`  
		Last Modified: Wed, 24 Apr 2024 04:15:06 GMT  
		Size: 49.5 MB (49453161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc15410e595a34b7a5d9e82b26d580e858211c5947bf56bb293ea57db35185c`  
		Last Modified: Wed, 24 Apr 2024 08:43:19 GMT  
		Size: 17.5 MB (17456193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8513aad98d9a17452335b87f52bab845a7a83392e5ebe6cc99b33a0959cf7a41`  
		Last Modified: Wed, 24 Apr 2024 08:43:33 GMT  
		Size: 52.2 MB (52231381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41858c667c6bef0ef068e6f0f96241c3650c1f4c036818f8797fd044dd3b1233`  
		Last Modified: Wed, 24 Apr 2024 08:43:58 GMT  
		Size: 183.5 MB (183524255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a853dfbd6891dda3b4b0471ba3a0cd3152aa09ecd2b5c7ab42200aecd2cb41`  
		Last Modified: Thu, 25 Apr 2024 19:28:10 GMT  
		Size: 241.6 MB (241616497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:b7f6e930546c81a9d424255969d9419adb42505a60d40a2f53b3daa5a73ce759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15968723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f3c9e2e42e3b699870f4260aaefb4706d542f913347642dd8a23ac91c6ec24`

```dockerfile
```

-	Layers:
	-	`sha256:2baa349b62478851aa805cc7cc782768dcd5056bdac80a21ad339628c269b1d8`  
		Last Modified: Thu, 25 Apr 2024 19:28:04 GMT  
		Size: 16.0 MB (15957718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86e545a9512d94d0f07fabb11f0896d725e3cff9c83c050ff5e1e00a487cdcb7`  
		Last Modified: Thu, 25 Apr 2024 19:28:04 GMT  
		Size: 11.0 KB (11005 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:buster` - linux; 386

```console
$ docker pull rust@sha256:fac6788e4941ab0701fc9c34271ef14eca43c4b5bb65215659beadd684f1300c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.1 MB (512108178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b640ea7f1e7531d4f5cfa3b7226a6b953c90e658857508596c6b5360e5d7de3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:31 GMT
ADD file:5f943bcdbbb65accdf0b3bc452a1d4fafd2c64a9c6f6b3010b2a7ca20bedef36 in / 
# Wed, 24 Apr 2024 03:39:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:32:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:33:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:34:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a3113a911224f7223aa235bbc20dff34c7d1419374b2180cf17ec274239d63d4`  
		Last Modified: Wed, 24 Apr 2024 03:44:44 GMT  
		Size: 51.4 MB (51420054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1354eeaeda7eb3c61cf02dbb765bed988acda27118f144f40318507dd7934295`  
		Last Modified: Wed, 24 Apr 2024 04:44:02 GMT  
		Size: 18.1 MB (18099027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3055ae20eecf0d5388e9ed336426983b625a70d36236930785aac17415cfcf3`  
		Last Modified: Wed, 24 Apr 2024 04:44:23 GMT  
		Size: 53.5 MB (53491779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761a4fb01a05271ea38a1437f27706939e45c0f2ea11a0b93f7920952ab0334a`  
		Last Modified: Wed, 24 Apr 2024 04:45:06 GMT  
		Size: 198.5 MB (198498122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1852dd56048b75a17b5ba9f4ad78c168193c3d5aa9c6c24d93d2ff9a7a35ddc`  
		Last Modified: Thu, 02 May 2024 17:53:31 GMT  
		Size: 190.6 MB (190599196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:03a4b3ad6cc7e27781766a25a7188463a05f7263903f27a6e5b55f75d55de506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15984068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf1cc48caf656945f2337b17cb68a8c439d69e5eddce9fc1556940a78d44291`

```dockerfile
```

-	Layers:
	-	`sha256:04e38e205fa8a7c96f3fa1b815f7508e1c7b9f6ace9f1bf30f96620714f7d623`  
		Last Modified: Thu, 02 May 2024 17:53:27 GMT  
		Size: 16.0 MB (15972439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:befe94823f0239850603d23141c164bf5a4967748e8ae0a9773cda0a9f98b922`  
		Last Modified: Thu, 02 May 2024 17:53:26 GMT  
		Size: 11.6 KB (11629 bytes)  
		MIME: application/vnd.in-toto+json
